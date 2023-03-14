<script>
    import SmallHeader from "../../../SmallHeader.svelte";
    import Sidebar from "../../../../CustomComponent/Sidebar.svelte";
    import Breadcrumb from "../../../../CustomComponent/Breadcrumb.svelte";
    import FullCalendar, { Draggable } from "svelte-fullcalendar";
    import daygridPlugin from "@fullcalendar/daygrid";
    import interactionPlugin from "@fullcalendar/interaction";
    import resourceTimelinePlugin from "@fullcalendar/resource-timeline";

    let options = {
        initialView: "dayGridMonth",
        plugins: [interactionPlugin, daygridPlugin, resourceTimelinePlugin],
        events: [
            { title: "event 1", date: "2023-03-14" },
            { title: "event 2", date: "2019-04-02" },
        ],
        dateClick: (event) => {
            alert("date click!" + event.dateStr);
        },
        droppable: true,
    };
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
            <Draggable eventData={{ title: "my event", duration: "02:00" }}>
                Drag me!
            </Draggable>

            <FullCalendar {options} />
        </div>
    </div>
</div>
