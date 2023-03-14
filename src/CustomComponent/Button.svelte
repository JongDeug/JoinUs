<script>
    export let number;
    export let content;
    export let location;
    export let usage;
    export let btnClass;
</script>

{#if number == 0}
    <div class="absolute right-[6%] top-[15%]">
        <a
            href="/"
            class="text-center font-bold focus:ring-4 focus:outline-none inline-flex items-center justify-center px-5 py-2.5 text-sm text-white bg-blue-700 hover:bg-blue-800 focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800 rounded-lg"
            >Edit Profile</a
        >
    </div>
{:else if number == 1}
    <a
        href={location}
        class="block shadow-md mt-5 py-3 text-center font-bold text-1xl focus:ring-4 focus:outline-none text-white bg-blue-600 hover:bg-blue-800 focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800 rounded-lg"
        >{content}</a
    >
{:else if number == 2}
    <button
        type="button"
        border="true"
        class="w-[100px] p-[0.71rem] ml-3 text-center font-medium focus:ring-4 focus:outline-none  items-center justify-center text-sm text-white bg-gray-800 hover:bg-gray-900 focus:ring-gray-300 dark:bg-gray-800 dark:hover:bg-gray-700 dark:focus:ring-gray-700 rounded-lg"
        >중복 확인</button
    >
{:else if number == 3}
    <button
        type="button"
        class="text-center font-medium focus:ring-4 focus:outline-none inline-flex items-center justify-center px-5 py-2.5 text-sm text-white bg-blue-700 hover:bg-blue-800 focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800 rounded-lg"
        >{content}</button
    >
{:else if usage == "PostMessageDeleteBtn"}
    <button
        type="button"
        class="text-center font-medium focus:ring-4 focus:outline-none inline-flex items-center justify-center px-5 py-2.5 text-sm text-white bg-red-700 hover:bg-red-800 focus:ring-red-300 dark:bg-red-600 dark:hover:bg-red-700 dark:focus:ring-red-800 rounded-lg"
        >{content}</button
    >
{:else if usage == "PostMessageSendBtn"}
    <button
        type="button"
        class="text-center font-medium focus:ring-4 focus:outline-none inline-flex items-center justify-center px-5 py-2.5 text-sm text-white bg-blue-800 hover:bg-blue-900 focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800 rounded-lg"
        >{content}</button
    >

{/if}
