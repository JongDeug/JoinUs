<script>
    import { Card, Button } from "flowbite-svelte";
    import SmallHeader from "../SmallHeader.svelte";
    import Empty from "../../CustomComponent/Empty.svelte";
</script>

<SmallHeader header="My Team" />

<div id="layout" class="mx-auto max-w-7xl py-6 sm:px-6 lg:px-8  max-h-full">
    <div class="grid grid-cols-4 grid-rows-2 gap-4">
        <div>
            <Card img="/images/image.png" class="h-full">
                <h5
                    class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white"
                >
                    JoinUs
                </h5>
                <p
                    class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight"
                >
                    Here are the biggest enterprise technology acquisitions of
                    2021 so far, in reverse chronological order.
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
            </Card>
        </div>
        <div>
            <Card img="/images/image.png" class="h-full">
                <h5
                    class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white"
                >
                    abcd 
                </h5>
                <p
                    class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight"
                >
                    Here are the biggest enterprise technology acquisitions of
                    2021 so far, in reverse chronological order.
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
            </Card>
        </div>
        <Empty />
        <Empty />
        <Empty />
        <Empty />
        <Empty />
        <Empty />
    </div>
</div>
