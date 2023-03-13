<script>
    import { Breadcrumb, BreadcrumbItem } from "flowbite-svelte";
    export let prevContent;
    export let nextContent;
</script>

    <Breadcrumb
        aria-label="Solid background breadcrumb example"
        class="flex px-5 py-3 text-gray-700 border-2 rounded-lg  border-indigo-200 dark:bg-gray-800 dark:border-gray-700"
    >
        <BreadcrumbItem href="/" home>홈</BreadcrumbItem>
        <BreadcrumbItem href="/">{prevContent}</BreadcrumbItem>
        <BreadcrumbItem>{nextContent}</BreadcrumbItem>
    </Breadcrumb>