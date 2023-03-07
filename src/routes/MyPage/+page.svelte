<script>
    import Sidebar from "./Sidebar.svelte";
    import SmallHeader from "../SmallHeader.svelte";
</script>

<SmallHeader header="My Page" />

<div
    id="layout"
    class="mx-auto max-w-7xl py-6 sm:px-6 lg:px-8  max-h-full flex"
>
    <Sidebar />
</div>
