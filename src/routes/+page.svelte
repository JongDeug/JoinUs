<script>
    import SmallHeader from "./SmallHeader.svelte";
    import Svg from "../CustomComponent/Svg.svelte";
    import DropdownItem from "../CustomComponent/DropdownItem.svelte";
    import TableHeader from "../CustomComponent/TableHeader.svelte";
    import TableRow from "../CustomComponent/TableRow.svelte";
    import Button from "../CustomComponent/Button.svelte";
    import { Pagination } from "flowbite-svelte";
    import { page } from "$app/stores";

    let dropdownStatus = false;
    const handleDropdownStatus = () => {
        dropdownStatus = !dropdownStatus;
    };

    let board = [
        { title: "test1", writer: "kim", createTime: "2023-03-10", hit: "30" },
        { title: "test2", writer: "kim", createTime: "2023-03-10", hit: "30" },
        { title: "test3", writer: "kim", createTime: "2023-03-10", hit: "30" },
        { title: "test4", writer: "kim", createTime: "2023-03-10", hit: "30" },
        { title: "test5", writer: "kim", createTime: "2023-03-10", hit: "30" },
        { title: "test5", writer: "kim", createTime: "2023-03-10", hit: "30" },
    ];

    let helper = { start: 1, end: 10, total: 100 };
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
</script>

<SmallHeader header="Board" />

<div id="layout" class="mx-auto max-w-7xl py-6 sm:px-6 lg:px-8  max-h-full">
    <div class="relative overflow-x-auto mt-6">
        <div class="block sm:flex items-center justify-between pb-4">
            <div class="mb-3 sm:mb-0">
                <button
                    class="inline-flex items-center text-gray-500 bg-white border border-gray-300 focus:outline-none hover:bg-gray-100  focus:ring-gray-200 font-medium rounded-lg text-sm px-3 py-1.5 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark:focus:ring-gray-700"
                    type="button"
                    on:click={handleDropdownStatus}
                >
                    <Svg svgName="??????" />
                    ?????? 30???
                    <Svg svgName="?????? ?????????" />
                </button>

                <!-- Dropdown menu -->
                {#if dropdownStatus}
                    <div
                        class="z-10 w-48 bg-white border-2 divide-y divide-gray-100 rounded-lg shadow dark:bg-gray-700 dark:divide-gray-600 {dropdownStatus}"
                        style="position: absolute; inset: auto auto 0px 0px; margin: 0px; transform: translate3d(4px, -210px, 0px);"
                    >
                        <ul
                            class="p-3 space-y-1 text-sm text-gray-700 dark:text-gray-200"
                        >
                            <!-- {#each dropdownContents as item}
                                    <DropdownItem
                                        id={item.id}
                                        label={item.content}
                                    />
                                {/each} -->
                            <DropdownItem id="1" label="??????" />
                            <DropdownItem id="2" label="?????? ?????????" />
                            <DropdownItem id="3" label="?????? 30???" />
                            <DropdownItem id="4" label="?????? ???" />
                            <DropdownItem id="5" label="??????" />
                        </ul>
                    </div>
                {/if}
            </div>

            <label for="table-search" class="sr-only">Search</label>
            <div class="relative">
                <div
                    class="absolute inset-y-0 left-0 flex items-center pl-3 pointer-events-none"
                >
                    <Svg svgName="??????" />
                </div>
                <input
                    type="text"
                    id="table-search"
                    class="block p-2 pl-10 text-sm text-gray-900 border border-gray-300 rounded-lg w-80 bg-gray-50 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
                    placeholder="??????"
                />
            </div>
        </div>

        <table
            class="w-full text-sm text-left text-gray-500 dark:text-gray-400 border-slate-300 border-collapse border"
        >
            <thead
                class="text-xs text-gray-700 uppercase bg-gray-50 dark:bg-gray-700 dark:text-gray-400"
            >
                <tr>
                    <TableHeader style="pr-80" content="??????" />
                    <TableHeader content="?????????" />
                    <TableHeader content="??????" />
                    <TableHeader content="?????????" />
                </tr>
            </thead>
            <tbody>
                {#each board as item}
                    <TableRow
                        title={item.title}
                        writer={item.writer}
                        createTime={item.createTime}
                        hit={item.hit}
                    />
                {/each}
            </tbody>
        </table>

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
                >
                Entries
            </div>

            <Button number="3" content="????????? ??????" />
        </div>

        <div class="flex justify-center">
            <Pagination {pages} on:previous={previous} on:next={next} />
        </div>
    </div>
    <!-- /End replace -->
</div>
