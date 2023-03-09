<script>
    import SmallHeader from "./SmallHeader.svelte";
    import Svg from "../CustomComponent/Svg.svelte";
    import DropdownItem from "../CustomComponent/DropdownItem.svelte";
    import TableHeader from "../CustomComponent/TableHeader.svelte";
    import TableRow from "../CustomComponent/TableRow.svelte";

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
</script>

<SmallHeader header="Board" />

<div id="layout" class="mx-auto max-w-7xl py-6 sm:px-6 lg:px-8  max-h-full">
    <!-- Replace with your content -->
    <div class="px-4 py-6 sm:px-2">
        <!-- <div
                    class="h-96 rounded-lg border-4 border-dashed border-gray-200"
                /> -->

        <div class="relative overflow-x-auto sm:rounded-lg p-1">
            <div class="block sm:flex items-center justify-between pb-4">
                <div class="mb-3 sm:mb-0">
                    <button
                        class="inline-flex items-center text-gray-500 bg-white border border-gray-300 focus:outline-none hover:bg-gray-100  focus:ring-gray-200 font-medium rounded-lg text-sm px-3 py-1.5 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark:focus:ring-gray-700"
                        type="button"
                        on:click={handleDropdownStatus}
                    >
                        <Svg svgName="시계" />
                        지난 30일
                        <Svg svgName="아래 화살표" />
                    </button>

                    <!-- Dropdown menu -->
                    {#if dropdownStatus}
                        <div
                            class="z-10 w-48 bg-white border-2 divide-y divide-gray-100 rounded-lg shadow dark:bg-gray-700 dark:divide-gray-600 {dropdownStatus}"
                            style="position: absolute; inset: auto auto 0px 0px; margin: 0px; transform: translate3d(4px, -260px, 0px);"
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
                                <DropdownItem id="1" label="어제" />
                                <DropdownItem id="2" label="지난 일주일" />
                                <DropdownItem id="3" label="지난 30일" />
                                <DropdownItem id="4" label="저번 달" />
                                <DropdownItem id="5" label="작년" />
                            </ul>
                        </div>
                    {/if}
                </div>

                <label for="table-search" class="sr-only">Search</label>
                <div class="relative">
                    <div
                        class="absolute inset-y-0 left-0 flex items-center pl-3 pointer-events-none"
                    >
                        <Svg svgName="검색" />
                    </div>
                    <input
                        type="text"
                        id="table-search"
                        class="block p-2 pl-10 text-sm text-gray-900 border border-gray-300 rounded-lg w-80 bg-gray-50 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
                        placeholder="검색"
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
                        <TableHeader style="pr-80" content="제목" />
                        <TableHeader content="글쓴이" />
                        <TableHeader content="날짜" />
                        <TableHeader content="조회수" />
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

            <nav
                class="flex items-center justify-between pt-4"
                aria-label="Table navigation"
            >
                <span
                    class="text-sm font-normal text-gray-500 dark:text-gray-400"
                    >Showing <span
                        class="font-semibold text-gray-900 dark:text-white"
                        >1-10</span
                    >
                    of
                    <span class="font-semibold text-gray-900 dark:text-white"
                        >1000</span
                    ></span
                >

                <ul class="inline-flex items-center -space-x-px">
                    <li>
                        <a
                            href="#"
                            class="block px-3 py-2 ml-0 leading-tight text-gray-500 bg-white border border-gray-300 rounded-l-lg hover:bg-gray-100 hover:text-gray-700 dark:bg-gray-800 dark:border-gray-700 dark:text-gray-400 dark:hover:bg-gray-700 dark:hover:text-white"
                        >
                            <span class="sr-only">Previous</span>
                            <svg
                                class="w-5 h-5"
                                aria-hidden="true"
                                fill="currentColor"
                                viewBox="0 0 20 20"
                                xmlns="http://www.w3.org/2000/svg"
                                ><path
                                    fill-rule="evenodd"
                                    d="M12.707 5.293a1 1 0 010 1.414L9.414 10l3.293 3.293a1 1 0 01-1.414 1.414l-4-4a1 1 0 010-1.414l4-4a1 1 0 011.414 0z"
                                    clip-rule="evenodd"
                                /></svg
                            >
                        </a>
                    </li>
                    <li>
                        <a
                            href="#"
                            class="block px-3 py-2 leading-tight text-gray-500 bg-white border border-gray-300 hover:bg-gray-100 hover:text-gray-700 dark:bg-gray-800 dark:border-gray-700 dark:text-gray-400 dark:hover:bg-gray-700 dark:hover:text-white"
                            >1</a
                        >
                    </li>
                    <li>
                        <a
                            href="#"
                            class="block px-3 py-2 leading-tight text-gray-500 bg-white border border-gray-300 hover:bg-gray-100 hover:text-gray-700 dark:bg-gray-800 dark:border-gray-700 dark:text-gray-400 dark:hover:bg-gray-700 dark:hover:text-white"
                            >2</a
                        >
                    </li>
                    <li>
                        <a
                            href="#"
                            aria-current="page"
                            class="block z-10 px-3 py-2 leading-tight text-blue-600 border border-blue-300 bg-blue-50 hover:bg-blue-100 hover:text-blue-700 dark:border-gray-700 dark:bg-gray-700 dark:text-white"
                            >3</a
                        >
                    </li>
                    <li>
                        <a
                            href="#"
                            class="block px-3 py-2 leading-tight text-gray-500 bg-white border border-gray-300 hover:bg-gray-100 hover:text-gray-700 dark:bg-gray-800 dark:border-gray-700 dark:text-gray-400 dark:hover:bg-gray-700 dark:hover:text-white"
                            >...</a
                        >
                    </li>
                    <li>
                        <a
                            href="#"
                            class="block px-3 py-2 leading-tight text-gray-500 bg-white border border-gray-300 hover:bg-gray-100 hover:text-gray-700 dark:bg-gray-800 dark:border-gray-700 dark:text-gray-400 dark:hover:bg-gray-700 dark:hover:text-white"
                            >100</a
                        >
                    </li>
                    <li>
                        <a
                            href="#"
                            class="block px-3 py-2 leading-tight text-gray-500 bg-white border border-gray-300 rounded-r-lg hover:bg-gray-100 hover:text-gray-700 dark:bg-gray-800 dark:border-gray-700 dark:text-gray-400 dark:hover:bg-gray-700 dark:hover:text-white"
                        >
                            <span class="sr-only">Next</span>
                            <svg
                                class="w-5 h-5"
                                aria-hidden="true"
                                fill="currentColor"
                                viewBox="0 0 20 20"
                                xmlns="http://www.w3.org/2000/svg"
                                ><path
                                    fill-rule="evenodd"
                                    d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z"
                                    clip-rule="evenodd"
                                /></svg
                            >
                        </a>
                    </li>
                </ul>
            </nav>
        </div>
    </div>
    <!-- /End replace -->
</div>
