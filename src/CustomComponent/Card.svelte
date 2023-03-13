<script>
    import { Button } from "flowbite-svelte";
    export let img;
</script>

<div>
    <div
        class="bg-white dark:bg-gray-800 text-gray-500 dark:text-gray-400 rounded-lg border border-gray-200 dark:border-gray-700 shadow-md flex max-w-sm flex-col p-4 sm:p-6 h-full"
    >
        {#if !!img}
            <img
                class="flex justify-center items-center mb-4 h-48 rounded "
                src="/images/image.png"
                alt=""
            />
        {:else}
            <div
                class="flex justify-center items-center mb-4 h-48 bg-gray-300 rounded dark:bg-gray-700"
            >
                <svg
                    width="48"
                    height="48"
                    class="text-gray-200 dark:text-gray-600"
                    xmlns="http://www.w3.org/2000/svg"
                    aria-hidden="true"
                    fill="currentColor"
                    viewBox="0 0 640 512"
                    ><path
                        d="M480 80C480 35.82 515.8 0 560 0C604.2 0 640 35.82 640 80C640 124.2 604.2 160 560 160C515.8 160 480 124.2 480 80zM0 456.1C0 445.6 2.964 435.3 8.551 426.4L225.3 81.01C231.9 70.42 243.5 64 256 64C268.5 64 280.1 70.42 286.8 81.01L412.7 281.7L460.9 202.7C464.1 196.1 472.2 192 480 192C487.8 192 495 196.1 499.1 202.7L631.1 419.1C636.9 428.6 640 439.7 640 450.9C640 484.6 612.6 512 578.9 512H55.91C25.03 512 .0006 486.1 .0006 456.1L0 456.1z"
                    /></svg
                >
            </div>
        {/if}

        <h5
            class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white"
        >
            abcd
        </h5>
        <p
            class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight"
        >
            Here are the biggest enterprise technology acquisitions of 2021 so
            far, in reverse chronological order.
        </p>
        <Button>
            Read more <svg
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke-width="1.5"
                stroke="currentColor"
                class="w-5 h-5 ml-2"
                ><path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    d="M13.5 4.5L21 12m0 0l-7.5 7.5M21 12H3"
                /></svg
            >
        </Button>
    </div>
</div>
