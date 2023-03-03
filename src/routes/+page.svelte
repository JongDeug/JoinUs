<script>
    import SmallHeader from "./SmallHeader.svelte";
</script>

<SmallHeader header="Board" />

<div id="layout" class="mx-auto max-w-7xl py-6 sm:px-6 lg:px-8  max-h-full">
    <!-- Replace with your content -->
    <div class="px-4 py-6 sm:px-0">
        <!-- <div
                    class="h-96 rounded-lg border-4 border-dashed border-gray-200"
                /> -->

        <div class="relative overflow-x-auto sm:rounded-lg">
            <div class="block sm:flex items-center justify-between pb-4">
                <div class="mb-3 sm:mb-0">
                    <button
                        id="dropdownRadioButton"
                        data-dropdown-toggle="dropdownRadio"
                        class="shadow-md inline-flex items-center text-gray-500 bg-white border border-gray-300 focus:outline-none hover:bg-gray-100 focus:ring-4 focus:ring-gray-200 font-medium rounded-lg text-sm px-3 py-1.5 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark:focus:ring-gray-700"
                        type="button"
                    >
                        <svg
                            class="w-4 h-4 mr-2 text-gray-400"
                            aria-hidden="true"
                            fill="currentColor"
                            viewBox="0 0 20 20"
                            xmlns="http://www.w3.org/2000/svg"
                            ><path
                                fill-rule="evenodd"
                                d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-12a1 1 0 10-2 0v4a1 1 0 00.293.707l2.828 2.829a1 1 0 101.415-1.415L11 9.586V6z"
                                clip-rule="evenodd"
                            /></svg
                        >
                        2학년
                        <svg
                            class="w-3 h-3 ml-2"
                            aria-hidden="true"
                            fill="none"
                            stroke="currentColor"
                            viewBox="0 0 24 24"
                            xmlns="http://www.w3.org/2000/svg"
                            ><path
                                stroke-linecap="round"
                                stroke-linejoin="round"
                                stroke-width="2"
                                d="M19 9l-7 7-7-7"
                            /></svg
                        >
                    </button>
                    <!-- Dropdown menu -->
                    <div
                        id="dropdownRadio"
                        class="z-10 hidden w-48 bg-white divide-y divide-gray-100 rounded-lg shadow dark:bg-gray-700 dark:divide-gray-600"
                        data-popper-reference-hidden=""
                        data-popper-escaped=""
                        data-popper-placement="top"
                        style="position: absolute; inset: auto auto 0px 0px; margin: 0px; transform: translate3d(522.5px, 3847.5px, 0px);"
                    >
                        <ul
                            class="p-3 space-y-1 text-sm text-gray-700 dark:text-gray-200"
                            aria-labelledby="dropdownRadioButton"
                        >
                            <li>
                                <div
                                    class="flex items-center p-2 rounded hover:bg-gray-100 dark:hover:bg-gray-600"
                                >
                                    <input
                                        id="filter-radio-example-1"
                                        type="radio"
                                        value=""
                                        name="filter-radio"
                                        class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 dark:focus:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600"
                                    />
                                    <label
                                        for="filter-radio-example-1"
                                        class="w-full ml-2 text-sm font-medium text-gray-900 rounded dark:text-gray-300"
                                        >Last day</label
                                    >
                                </div>
                            </li>
                            <li>
                                <div
                                    class="flex items-center p-2 rounded hover:bg-gray-100 dark:hover:bg-gray-600"
                                >
                                    <input
                                        checked=""
                                        id="filter-radio-example-2"
                                        type="radio"
                                        value=""
                                        name="filter-radio"
                                        class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 dark:focus:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600"
                                    />
                                    <label
                                        for="filter-radio-example-2"
                                        class="w-full ml-2 text-sm font-medium text-gray-900 rounded dark:text-gray-300"
                                        >Last 7 days</label
                                    >
                                </div>
                            </li>
                            <li>
                                <div
                                    class="flex items-center p-2 rounded hover:bg-gray-100 dark:hover:bg-gray-600"
                                >
                                    <input
                                        id="filter-radio-example-3"
                                        type="radio"
                                        value=""
                                        name="filter-radio"
                                        class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 dark:focus:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600"
                                    />
                                    <label
                                        for="filter-radio-example-3"
                                        class="w-full ml-2 text-sm font-medium text-gray-900 rounded dark:text-gray-300"
                                        >Last 30 days</label
                                    >
                                </div>
                            </li>
                            <li>
                                <div
                                    class="flex items-center p-2 rounded hover:bg-gray-100 dark:hover:bg-gray-600"
                                >
                                    <input
                                        id="filter-radio-example-4"
                                        type="radio"
                                        value=""
                                        name="filter-radio"
                                        class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 dark:focus:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600"
                                    />
                                    <label
                                        for="filter-radio-example-4"
                                        class="w-full ml-2 text-sm font-medium text-gray-900 rounded dark:text-gray-300"
                                        >Last month</label
                                    >
                                </div>
                            </li>
                            <li>
                                <div
                                    class="flex items-center p-2 rounded hover:bg-gray-100 dark:hover:bg-gray-600"
                                >
                                    <input
                                        id="filter-radio-example-5"
                                        type="radio"
                                        value=""
                                        name="filter-radio"
                                        class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 dark:focus:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600"
                                    />
                                    <label
                                        for="filter-radio-example-5"
                                        class="w-full ml-2 text-sm font-medium text-gray-900 rounded dark:text-gray-300"
                                        >Last year</label
                                    >
                                </div>
                            </li>
                        </ul>
                    </div>
                </div>
                <label for="table-search" class="sr-only">Search</label>
                <div class="relative shadow-md">
                    <div
                        class="shawdow-md absolute inset-y-0 left-0 flex items-center pl-3 pointer-events-none"
                    >
                        <svg
                            class="w-5 h-5 text-gray-500 dark:text-gray-400"
                            aria-hidden="true"
                            fill="currentColor"
                            viewBox="0 0 20 20"
                            xmlns="http://www.w3.org/2000/svg"
                            ><path
                                fill-rule="evenodd"
                                d="M8 4a4 4 0 100 8 4 4 0 000-8zM2 8a6 6 0 1110.89 3.476l4.817 4.817a1 1 0 01-1.414 1.414l-4.816-4.816A6 6 0 012 8z"
                                clip-rule="evenodd"
                            /></svg
                        >
                    </div>
                    <input
                        type="text"
                        id="table-search"
                        class="block p-2 pl-10 text-sm text-gray-900 border border-gray-300 rounded-lg w-80 bg-gray-50 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
                        placeholder="Search for items"
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
                        <th
                            scope="col"
                            class="pl-6 pr-80 py-3 border border-slate-200"
                        >
                            제목
                        </th>
                        <th
                            scope="col"
                            class="px-6 py-3 border border-slate-200"
                        >
                            글쓴이
                        </th>
                        <th
                            scope="col"
                            class="px-6 py-3 border border-slate-200"
                        >
                            날짜
                        </th>
                        <th
                            scope="col"
                            class="px-6 py-3 border border-slate-200"
                        >
                            조회수
                        </th>
                    </tr>
                </thead>
                <tbody>
                    <tr
                        class="bg-white border-b dark:bg-gray-800 dark:border-gray-700"
                    >
                        <th
                            scope="row"
                            class="px-6 py-4 font-medium text-gray-900 whitespace-nowrap dark:text-white border border-slate-200"
                        >
                            Apple MacBook Pro 17"
                        </th>
                        <td class="px-6 py-4 border border-slate-200">
                            Sliver
                        </td>
                        <td class="px-6 py-4 border border-slate-200">
                            Laptop
                        </td>
                        <td class="px-6 py-4 border border-slate-200">
                            $2999
                        </td>
                    </tr>
                    <tr
                        class="bg-white border-b dark:bg-gray-800 dark:border-gray-700"
                    >
                        <th
                            scope="row"
                            class="px-6 py-4 font-medium text-gray-900 whitespace-nowrap dark:text-white border border-slate-200"
                        >
                            Microsoft Surface Pro
                        </th>
                        <td class="px-6 py-4 border border-slate-200">
                            White
                        </td>
                        <td class="px-6 py-4 border border-slate-200">
                            Laptop PC
                        </td>
                        <td class="px-6 py-4 border border-slate-200">
                            $1999
                        </td>
                    </tr>
                    <tr class="bg-white dark:bg-gray-800">
                        <th
                            scope="row"
                            class="px-6 py-4 font-medium text-gray-900 whitespace-nowrap dark:text-white border border-slate-200"
                        >
                            Magic Mouse 2
                        </th>
                        <td class="px-6 py-4 border border-slate-200">
                            Black
                        </td>
                        <td class="px-6 py-4 border border-slate-200">
                            Accessories
                        </td>
                        <td class="px-6 py-4 border border-slate-200"> $99 </td>
                    </tr>
                    <tr class="bg-white dark:bg-gray-800">
                        <th
                            scope="row"
                            class="px-6 py-4 font-medium text-gray-900 whitespace-nowrap dark:text-white border border-slate-200"
                        >
                            Magic Mouse 2
                        </th>
                        <td class="px-6 py-4 border border-slate-200">
                            Black
                        </td>
                        <td class="px-6 py-4 border border-slate-200">
                            Accessories
                        </td>
                        <td class="px-6 py-4 border border-slate-200"> $99 </td>
                    </tr>
                    <tr class="bg-white dark:bg-gray-800">
                        <th
                            scope="row"
                            class="px-6 py-4 font-medium text-gray-900 whitespace-nowrap dark:text-white border border-slate-200"
                        >
                            Magic Mouse 2
                        </th>
                        <td class="px-6 py-4 border border-slate-200">
                            Black
                        </td>
                        <td class="px-6 py-4 border border-slate-200">
                            Accessories
                        </td>
                        <td class="px-6 py-4 border border-slate-200"> $99 </td>
                    </tr>
                    <tr class="bg-white dark:bg-gray-800">
                        <th
                            scope="row"
                            class="px-6 py-4 font-medium text-gray-900 whitespace-nowrap dark:text-white border border-slate-200"
                        >
                            Magic Mouse 2
                        </th>
                        <td class="px-6 py-4 border border-slate-200">
                            Black
                        </td>
                        <td class="px-6 py-4 border border-slate-200">
                            Accessories
                        </td>
                        <td class="px-6 py-4 border border-slate-200"> $99 </td>
                    </tr>
                    <tr class="bg-white dark:bg-gray-800">
                        <th
                            scope="row"
                            class="px-6 py-4 font-medium text-gray-900 whitespace-nowrap dark:text-white border border-slate-200"
                        >
                            Magic Mouse 2
                        </th>
                        <td class="px-6 py-4 border border-slate-200">
                            Black
                        </td>
                        <td class="px-6 py-4 border border-slate-200">
                            Accessories
                        </td>
                        <td class="px-6 py-4 border border-slate-200"> $99 </td>
                    </tr>
                </tbody>
            </table>
        </div>

        <nav
            class="flex items-center justify-between pt-4"
            aria-label="Table navigation"
        >
            <span class="text-sm font-normal text-gray-500 dark:text-gray-400"
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
    <!-- /End replace -->
</div>
