<script>
    import { quill } from "svelte-quill";
    import SmallHeader from "../SmallHeader.svelte";
    import Button from "../../CustomComponent/Button.svelte";

    const options = {
        modules: {
            toolbar: [
                [{ header: [1, 2, 3, false] }],
                ["bold", "italic", "underline", "strike", "image"],
                ["link", "code-block"],
            ],
        },
        // placeholder: "Type something...",
        theme: "snow",
    };

    let content = { html: "", text: "" };
    $: console.log(content);
</script>

<svelte:head>
    <link href="//cdn.quilljs.com/1.3.6/quill.snow.css" rel="stylesheet" />
</svelte:head>

<SmallHeader header="Create Post" />

<div id="layout" class="mx-auto max-w-7xl py-6 sm:px-6 lg:px-8 max-h-full">
    <div class="w-[70%]">
        <div
            class="editor"
            use:quill={options}
            on:text-change={(e) => (content = e.detail)}
        />

        <button
            type="button"
            class="mt-3 text-center font-medium focus:ring-4 focus:outline-none inline-flex items-center justify-center px-5 py-2.5 text-sm text-white bg-blue-700 hover:bg-blue-800 focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800 rounded-lg"
            >저장</button
        >
    </div>

    <!-- <div>
        Resulting HTML:
        {@html content.html}
    </div> -->
</div>
