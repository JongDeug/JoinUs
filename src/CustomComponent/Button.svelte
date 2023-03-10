<script>
    export let number;
    export let content;
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
        href="#"
        class="block shadow-md mt-5 py-3 text-center font-bold text-1xl focus:ring-4 focus:outline-none text-white bg-blue-600 hover:bg-blue-800 focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800 rounded-lg"
        >{content}</a
    >
{:else if number == 2}
    <button
        type="button"
        border="true"
        class="text-center font-medium focus:ring-4 focus:outline-none inline-flex items-center justify-center px-5 py-[0.85rem] leading-none text-sm text-white bg-gray-800 hover:bg-gray-900 focus:ring-gray-300 dark:bg-gray-800 dark:hover:bg-gray-700 dark:focus:ring-gray-700 rounded-lg"
        >중복 확인</button
    >
{/if}
