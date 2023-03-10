<script>
    import SmallHeader from "../../SmallHeader.svelte";
    import Sidebar from "../Sidebar.svelte";
    import Breadcrumb from "../../../CustomComponent/Breadcrumb.svelte";

    import {
        Table,
        TableBody,
        TableBodyCell,
        TableBodyRow,
        TableHead,
        TableHeadCell,
        Checkbox,
        Pagination
    } from "flowbite-svelte";

    import { page } from "$app/stores";

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

    <!-- 비밀번호 변경 -->
    <div class="ml-5 block w-[70%]">
        <Breadcrumb content="내가 작성한 게시글" />

        <div class="mt-3 p-10 rounded-lg shadow-md border">
            <h1 class="font-bold text-4xl mb-7">내가 작성한 게시글</h1>
            <Table hoverable={true}>
                <TableHead>
                    <TableHeadCell class="!p-4">
                        <Checkbox />
                    </TableHeadCell>
                    <TableHeadCell>제목</TableHeadCell>
                    <TableHeadCell>글쓴이</TableHeadCell>
                    <TableHeadCell>날짜</TableHeadCell>
                    <TableHeadCell>조회수</TableHeadCell>
                    <TableHeadCell>
                        <span class="sr-only"> Edit </span>
                    </TableHeadCell>
                </TableHead>
                <TableBody class="divide-y">
                    <TableBodyRow>
                        <TableBodyCell class="!p-4">
                            <Checkbox />
                        </TableBodyCell>
                        <TableBodyCell>Apple MacBook Pro 17"</TableBodyCell>
                        <TableBodyCell>Sliver</TableBodyCell>
                        <TableBodyCell>Laptop</TableBodyCell>
                        <TableBodyCell>$2999</TableBodyCell>
                        <TableBodyCell>
                            <a
                                href="/tables"
                                class="font-medium text-blue-600 hover:underline dark:text-blue-500"
                            >
                                Edit
                            </a>
                        </TableBodyCell>
                    </TableBodyRow>
                    <TableBodyRow>
                        <TableBodyCell class="!p-4">
                            <Checkbox />
                        </TableBodyCell>
                        <TableBodyCell>Microsoft Surface Pro</TableBodyCell>
                        <TableBodyCell>White</TableBodyCell>
                        <TableBodyCell>Laptop PC</TableBodyCell>
                        <TableBodyCell>$1999</TableBodyCell>
                        <TableBodyCell>
                            <a
                                href="/tables"
                                class="font-medium text-blue-600 hover:underline dark:text-blue-500"
                            >
                                Edit
                            </a>
                        </TableBodyCell>
                    </TableBodyRow>
                    <TableBodyRow>
                        <TableBodyCell class="!p-4">
                            <Checkbox />
                        </TableBodyCell>
                        <TableBodyCell>Magic Mouse 2</TableBodyCell>
                        <TableBodyCell>Black</TableBodyCell>
                        <TableBodyCell>Accessories</TableBodyCell>
                        <TableBodyCell>$99</TableBodyCell>
                        <TableBodyCell>
                            <a
                                href="/tables"
                                class="font-medium text-blue-600 hover:underline dark:text-blue-500"
                            >
                                Edit
                            </a>
                        </TableBodyCell>
                    </TableBodyRow>
                </TableBody>
            </Table>

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
