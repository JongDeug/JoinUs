<script>
    import { AccordionItem, Accordion } from "flowbite-svelte";
</script>

<header class="bg-white shadow">
    <div class="mx-auto max-w-7xl py-6 px-4 sm:px-6 lg:px-8">
        <h1 class="text-3xl font-bold tracking-tight text-gray-900">FAQ</h1>
    </div>
</header>

<div id="layout" class="mx-auto max-w-7xl py-6 sm:px-6 lg:px-8  max-h-full">
    <Accordion>
        <AccordionItem>
            <span slot="header" class="text-base flex gap-2 items-center">
                <svg
                    class="w-5 h-5 mr-2 shrink-0"
                    fill="currentColor"
                    viewBox="0 0 20 20"
                    xmlns="http://www.w3.org/2000/svg"
                    ><path
                        fill-rule="evenodd"
                        d="M18 10a8 8 0 11-16 0 8 8 0 0116 0zm-8-3a1 1 0 00-.867.5 1 1 0 11-1.731-1A3 3 0 0113 8a3.001 3.001 0 01-2 2.83V11a1 1 0 11-2 0v-1a1 1 0 011-1 1 1 0 100-2zm0 8a1 1 0 100-2 1 1 0 000 2z"
                        clip-rule="evenodd"
                    /></svg
                >
                <span>What is Flowbite?</span>
            </span>
            <p class="mb-2 text-gray-500 dark:text-gray-400">
                Lorem ipsum dolor sit amet, consectetur adipisicing elit. Illo
                ab necessitatibus sint explicabo...
            </p>
            <p class="text-gray-500 dark:text-gray-400">
                Check out this guide to learn how to <a
                    href="/"
                    target="_blank"
                    rel="noreferrer"
                    class="text-blue-600 dark:text-blue-500 hover:underline"
                    >get started</a
                > and start websites even faster with components on top of Tailwind
                CSS.
            </p>
        </AccordionItem>
        <AccordionItem>
            <span slot="header" class="text-base flex gap-2 items-center">
                <svg
                    class="w-5 h-5 mr-2 shrink-0"
                    fill="currentColor"
                    viewBox="0 0 20 20"
                    xmlns="http://www.w3.org/2000/svg"
                    ><path
                        fill-rule="evenodd"
                        d="M18 10a8 8 0 11-16 0 8 8 0 0116 0zm-8-3a1 1 0 00-.867.5 1 1 0 11-1.731-1A3 3 0 0113 8a3.001 3.001 0 01-2 2.83V11a1 1 0 11-2 0v-1a1 1 0 011-1 1 1 0 100-2zm0 8a1 1 0 100-2 1 1 0 000 2z"
                        clip-rule="evenodd"
                    /></svg
                >
                <span> My Header 2</span>
            </span>
            <p class="mb-2 text-gray-500 dark:text-gray-400">
                Lorem ipsum dolor sit amet, consectetur adipisicing elit. Illo
                ab necessitatibus sintexplicabo...
            </p>
        </AccordionItem>
    </Accordion>
</div>
