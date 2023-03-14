<script>
    import SmallHeader from "../../SmallHeader.svelte";
    import Sidebar from "../../../CustomComponent/Sidebar.svelte";
    import { Blockquote, Heading, CloseButton, Img } from "flowbite-svelte";
    import { Listgroup, ListgroupItem, Avatar } from "flowbite-svelte";
    import Breadcrumb from "../../../CustomComponent/Breadcrumb.svelte";
</script>

<!-- 팀 명  -->
<SmallHeader header="abcd" />
<div
    id="layout"
    class="max-w-7xl py-6 sm:px-6 lg:px-8  max-h-full flex m-auto justify-center"
>
    <Sidebar number="1" />

    <div class="ml-5 block w-[70%]">
        <Breadcrumb prevContent="내 팀" nextContent="대시보드" />

        <div class="flex justify-between mb-6 mt-6">
            <div class="rounded-lg shadow-md border w-[30%] p-5">
                팀장 <p class="text-3xl">asd</p>
            </div>
            <div class="rounded-lg shadow-md border w-[30%] p-5">
                팀원 수
                <p class="text-3xl">3</p>
            </div>
            <div class="rounded-lg shadow-md border w-[30%] p-5">
                팀 상태 <p class="text-3xl">in progress</p>
            </div>
        </div>

        <div class="rounded-lg shadow-md border p-10">
            <!-- <Img src="/images/image.png" size="max-w-lg" /> -->
            <div
                class="flex justify-center items-center mb-10 h-60 bg-gray-300 rounded dark:bg-gray-700"
            >
                <svg
                    width="48"
                    height="48"
                    class="text-gray-200 dark:text-gray-600"
                    xmlns="http://www.w3.org/2000/svg"
                    aria-hidden="true"
                    fill="currentColor"
                    viewBox="0 0 640 512"
                    ><path
                        d="M480 80C480 35.82 515.8 0 560 0C604.2 0 640 35.82 640 80C640 124.2 604.2 160 560 160C515.8 160 480 124.2 480 80zM0 456.1C0 445.6 2.964 435.3 8.551 426.4L225.3 81.01C231.9 70.42 243.5 64 256 64C268.5 64 280.1 70.42 286.8 81.01L412.7 281.7L460.9 202.7C464.1 196.1 472.2 192 480 192C487.8 192 495 196.1 499.1 202.7L631.1 419.1C636.9 428.6 640 439.7 640 450.9C640 484.6 612.6 512 578.9 512H55.91C25.03 512 .0006 486.1 .0006 456.1L0 456.1z"
                    /></svg
                >
            </div>
            <Heading tag="h1" class="mb-10">JoinUs</Heading>
            <Blockquote size="xl" class="mb-10">
                <svg
                    aria-hidden="true"
                    class="w-10 h-10 text-gray-400 dark:text-gray-600"
                    viewBox="0 0 24 27"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                    ><path
                        d="M14.017 18L14.017 10.609C14.017 4.905 17.748 1.039 23 0L23.995 2.151C21.563 3.068 20 5.789 20 8H24V18H14.017ZM0 18V10.609C0 4.905 3.748 1.038 9 0L9.996 2.151C7.563 3.068 6 5.789 6 8H9.983L9.983 18L0 18Z"
                        fill="currentColor"
                    /></svg
                >
                "Flowbite is just awesome. It contains tons of predesigned components
                and pages starting from login screen to complex dashboard. Perfect
                choice for your next SaaS application."
            </Blockquote>

            <Listgroup active class="mb-10">
                <h3
                    class="text-center bg-blue-500 text-white font-bold rounded-t-lg"
                >
                    팀원 목록
                </h3>
                <ListgroupItem class="text-base font-semibold gap-2">
                    <Avatar src="" size="xs" />Jese Leos
                    <CloseButton />
                </ListgroupItem>
                <ListgroupItem class="text-base font-semibold gap-2">
                    <Avatar src="" size="xs" />Robert Gouth
                    <CloseButton />
                </ListgroupItem>
            </Listgroup>

            <a
                href="#"
                class="block p-3 shadow-md text-center font-bold text-2xl focus:ring-4 focus:outline-none text-white bg-blue-600 hover:bg-blue-800 focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800 rounded-lg"
            >
                회의 시작하기
                <!-- <svg
                        class="ml-2 -mr-1 w-5 h-5"
                        fill="currentColor"
                        viewBox="0 0 20 20"
                        xmlns="http://www.w3.org/2000/svg"
                        ><path
                            fill-rule="evenodd"
                            d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z"
                            clip-rule="evenodd"
                        /></svg
                    > -->
            </a>
        </div>
    </div>
</div>
