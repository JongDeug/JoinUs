<!-- <div
    class="relative flex justify-center items-center rounded-full p-1 ring-2 ring-gray-300 dark:ring-gray-500 w-60 h-60 bg-gray-100 dark:bg-gray-600 text-gray-600 dark:text-gray-300"
>
    <svg
        class="text-gray-400 bg-gray-100 dark:bg-gray-600 rounded-full"
        fill="currentColor"
        viewBox="0 0 16 16"
        xmlns="http://www.w3.org/2000/svg"
        ><path
            fill-rule="evenodd"
            d="M8 9a3 3 0 100-6 3 3 0 000 6zm-7 9a7 7 0 1114 0H3z"
            clip-rule="evenodd"
        /></svg
    >
</div> -->
<script>
    export let number;
</script>

<!-- 이미지가 없을 때 -->

{#if number == 0}
    <div
        class="absolute left-1/2 transform -translate-x-1/2 -translate-y-1/2 rounded-full p-1 ring-8 ring-black dark:ring-gray-500 w-40 h-40 bg-gray-100 dark:bg-gray-600 text-gray-600 dark:text-gray-300"
    >
        <svg
            class="text-gray-400 bg-gray-100 dark:bg-gray-600 rounded-full"
            fill="currentColor"
            viewBox="0 0 16 16"
            xmlns="http://www.w3.org/2000/svg"
            ><path
                fill-rule="evenodd"
                d="M8 9a3 3 0 100-6 3 3 0 000 6zm-7 9a7 7 0 1114 0H3z"
                clip-rule="evenodd"
            /></svg
        >
    </div>
{:else if number == 1}
    <!-- 이미지 있을 때 -->
    <img
        alt=""
        src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
        class="mr-5 rounded-full p-1 ring-2 ring-gray-300 dark:ring-gray-500 w-14 h-14 bg-gray-100 dark:bg-gray-600 text-gray-600 dark:text-gray-300"
    />
{/if}
