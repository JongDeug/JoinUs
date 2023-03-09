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
    <div class="flex justify-center">
        <a
            href="#"
            class="text-center font-bold text-1xl focus:ring-4 focus:outline-none inline-flex items-center justify-center px-80 py-3 text-white bg-blue-700 hover:bg-blue-800 focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800 rounded-lg"
            >{content}</a
        >
    </div>
{/if}
