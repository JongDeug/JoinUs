<script>
    import SmallHeader from "../../../SmallHeader.svelte";
    import Sidebar from "../../../../CustomComponent/Sidebar.svelte";
    import Breadcrumb from "../../../../CustomComponent/Breadcrumb.svelte";
    import FullCalendar, { Draggable } from "svelte-fullcalendar";
    import daygridPlugin from "@fullcalendar/daygrid";
    import interactionPlugin from "@fullcalendar/interaction";
    import timegridPlugin from "@fullcalendar/timegrid";

    let options = {
        initialView: "dayGridMonth",
        plugins: [interactionPlugin, daygridPlugin, timegridPlugin],
        events: [{ id: 1, title: "New Event", start: new Date() }],
        dateClick: handleDateClick,
        editable: true,
        selectable: true,
        select: (info) => {
            console.log(info.start);
        },
        eventClick: (info) => {
            console.log(info.event.id); // event에 위 처럼 id를 설정할 수 있고 그 아이디를 통해 events 배열에서 걸러서 지울 수 있음.
            // 즉 중요한 db는 events 객체임!
            // info.event.remove();
        },
    };

    function handleDateClick(event) {
        if (
            confirm("Would you like to add an event to " + event.dateStr + " ?")
        ) {
            const { events } = options;
            const calendarEvents = [
                ...events,
                {
                    title: "New Event",
                    start: event.date,
                    allDay: event.allDay,
                },
            ];
            options = {
                ...options,
                events: calendarEvents,
            };

            console.log(options);
        }
    }
</script>

<SmallHeader header="abcd" />
<div
    id="layout"
    class="max-w-7xl py-6 sm:px-6 lg:px-8  max-h-full flex m-auto justify-center"
>
    <Sidebar number="1" />

    <div class="ml-5 block w-[70%]">
        <Breadcrumb prevContent="내 팀" nextContent="캘린더" />

        <div class="rounded-lg shadow-md border p-10 mt-6">
            <h1 class="font-bold text-4xl mb-7">캘린더</h1>
                <FullCalendar {options} />
        </div>
    </div>
</div>
