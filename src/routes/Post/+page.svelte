<script>
    import { quill } from "svelte-quill";
    import SmallHeader from "../SmallHeader.svelte";

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

<div id="layout" class="mx-auto max-w-7xl py-6 sm:px-6 lg:px-8 max-h-full flex justify-center">
    <div class="w-[70%] h-[530px] shadow-lg ">
        <div
            class="editor"
            use:quill={options}
            on:text-change={(e) => (content = e.detail)}
        />

        <!-- Resulting HTML:
        {@html content.html} -->
    </div>
</div>
