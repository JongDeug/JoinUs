<script>
    export let title;
    export let writer;
    export let createTime;
    export let hit;
</script>

<tr class="bg-white border-b dark:bg-gray-800 dark:border-gray-700">
    <th
        scope="row"
        class="px-6 py-4 font-medium text-gray-900 whitespace-nowrap dark:text-white border border-slate-200"
    >
        {title}
    </th>
    <td class="px-6 py-4 border border-slate-200"> {writer}</td>
    <td class="px-6 py-4 border border-slate-200"> {createTime}</td>
    <td class="px-6 py-4 border border-slate-200"> {hit}</td>
</tr>
