<script>
    import {Breadcrumb, BreadcrumbItem} from "flowbite-svelte";
    export let content;
</script>

<Breadcrumb
    aria-label="Solid background breadcrumb example"
    class="flex px-5 py-3 text-gray-700 border-2 rounded-lg  border-indigo-200 dark:bg-gray-800 dark:border-gray-700"
>
    <BreadcrumbItem href="/" home>홈</BreadcrumbItem>
    <BreadcrumbItem href="/">설정</BreadcrumbItem>
    <BreadcrumbItem>{content}</BreadcrumbItem>
</Breadcrumb>
