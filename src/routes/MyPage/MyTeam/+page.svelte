<script>
    import {
        Table,
        TableBody,
        TableBodyCell,
        TableBodyRow,
        TableHead,
        TableHeadCell,
        TableSearch,
        Breadcrumb,
        BreadcrumbItem,
    } from "flowbite-svelte";
    import SmallHeader from "../../SmallHeader.svelte";
    import Sidebar from "../Sidebar.svelte";


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
</script>

<SmallHeader header="My Page" padding="24" />

<div
    id="layout"
    class="max-w-7xl py-6 sm:px-6 lg:px-8  max-h-full flex m-auto justify-center"
>
    <Sidebar />
    <div class="ml-3 block w-[70%]">
        <Breadcrumb aria-label="Solid background breadcrumb example" solid>
            <BreadcrumbItem href="/" home>홈</BreadcrumbItem>
            <BreadcrumbItem href="/">설정</BreadcrumbItem>
            <BreadcrumbItem>내 팀</BreadcrumbItem>
        </Breadcrumb>

        <div class="mt-3 p-5 rounded-lg bg-gray-50">
            <div class="border-2 rounded-md p-10">
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
                                <TableBodyCell>  <a
                                    href="/tables"
                                    class="font-medium text-blue-600 hover:underline dark:text-blue-500"
                                >
                                    Edit
                                </a></TableBodyCell>
                            </TableBodyRow>
                        {/each}
                    </TableBody>
                </TableSearch>

            </div>
        </div>
    </div>
</div>
