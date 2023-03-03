<script>
    import Sidebar from "./Sidebar.svelte";
    import SmallHeader from "../SmallHeader.svelte";
    import Avatar from "./Avatar.svelte";
    // import {Avatar}  from "flowbite-svelte";
</script>

<SmallHeader header="My Page" />

<div
    id="layout"
    class="mx-auto max-w-7xl py-6 sm:px-6 lg:px-8  max-h-full flex"
>
    <Sidebar />

    <div class="bg-slate-100 ml-3 flex items-center space-x-4">
        <Avatar />
        <div class="space-y-1 font-medium dark:text-white items-">
            <div>이름</div>
            <div class="text-sm text-gray-500 dark:text-gray-400">
                내 소개 글
            </div>
        </div>
    </div>
</div>
