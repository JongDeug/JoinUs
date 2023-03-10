<script>
    import {
        Table,
        TableBody,
        TableBodyCell,
        TableBodyRow,
        TableHead,
        TableHeadCell,
        TableSearch,
        Pagination,
    } from "flowbite-svelte";
    import Breadcrumb from "../../../CustomComponent/Breadcrumb.svelte";
    import SmallHeader from "../../SmallHeader.svelte";
    import Sidebar from "../Sidebar.svelte";
    import { page } from "$app/stores";

    let searchTerm = "";
    let items = [
        { id: 1, maker: "Toyota", type: "ABC", make: 2017 },
        { id: 2, maker: "Ford", type: "CDE", make: 2018 },
        { id: 3, maker: "Volvo", type: "FGH", make: 2019 },
        { id: 4, maker: "Saab", type: "IJK", make: 2020 },
    ];
    $: filteredItems = items.filter(
        (item) =>
            item.maker.toLowerCase().indexOf(searchTerm.toLowerCase()) !== -1
    );

    $: activeUrl = $page.url.searchParams.get("page");
    let pages = [
        { name: 1, href: "/components/pagination?page=1" },
        { name: 2, href: "/components/pagination?page=2" },
        { name: 3, href: "/components/pagination?page=3" },
        { name: 4, href: "/components/pagination?page=4" },
        { name: 5, href: "/components/pagination?page=5" },
    ];

    $: {
        pages.forEach((page) => {
            let splitUrl = page.href.split("?");
            let queryString = splitUrl.slice(1).join("?");
            const hrefParams = new URLSearchParams(queryString);
            let hrefValue = hrefParams.get("page");
            if (hrefValue === activeUrl) {
                page.active = true;
            } else {
                page.active = false;
            }
        });
        pages = pages;
    }

    const previous = () => {
        alert(
            "Previous btn clicked. Make a call to your server to fetch data."
        );
    };
    const next = () => {
        alert("Next btn clicked. Make a call to your server to fetch data.");
    };

    let helper = { start: 1, end: 10, total: 100 };
</script>

<SmallHeader header="My Page" padding="24" />

<div
    id="layout"
    class="max-w-7xl py-6 sm:px-6 lg:px-8  max-h-full flex m-auto justify-center"
>
    <Sidebar />
    <div class="ml-5 block w-[70%]">
        <Breadcrumb content="내 팀" />

        <div class="mt-3 p-10 rounded-lg border shadow-md">
            <h1 class="font-bold text-4xl mb-7">내 팀 목록</h1>

            <TableSearch
                color="green"
                placeholder="Search by maker name"
                hoverable={true}
                bind:inputValue={searchTerm}
            >
                <TableHead>
                    <TableHeadCell>ID</TableHeadCell>
                    <TableHeadCell>팀 명</TableHeadCell>
                    <TableHeadCell>팀원 수</TableHeadCell>
                    <TableHeadCell>생성일자</TableHeadCell>
                    <TableHeadCell>편집</TableHeadCell>
                </TableHead>
                <TableBody class="divide-y">
                    {#each filteredItems as item}
                        <TableBodyRow>
                            <TableBodyCell>{item.id}</TableBodyCell>
                            <TableBodyCell>{item.maker}</TableBodyCell>
                            <TableBodyCell>{item.type}</TableBodyCell>
                            <TableBodyCell>{item.make}</TableBodyCell>
                            <TableBodyCell>
                                <a
                                    href="/tables"
                                    class="font-medium text-blue-600 hover:underline dark:text-blue-500"
                                >
                                    Edit
                                </a></TableBodyCell
                            >
                        </TableBodyRow>
                    {/each}
                </TableBody>
            </TableSearch>

             <div class="flex mt-5 justify-between">
                <div class="text-sm text-gray-700 dark:text-gray-400">
                    Showing <span
                        class="font-semibold text-gray-900 dark:text-white"
                        >{helper.start}</span
                    >
                    to
                    <span class="font-semibold text-gray-900 dark:text-white"
                        >{helper.end}</span
                    >
                    of
                    <span class="font-semibold text-gray-900 dark:text-white"
                        >{helper.total}</span
                    > Entries
                </div>

                <Pagination {pages} on:previous={previous} on:next={next} />
            </div>
        </div>
    </div>
</div>
