<script>
    import SmallHeader from "../SmallHeader.svelte";
    // import {Card} from "flowbite-svelte"
    import Card from "../../CustomComponent/Card.svelte";
    import CardPlaceholder from "../../CustomComponent/CardPlaceholder.svelte";
</script>

<SmallHeader header="My Team" />

<div id="layout" class="mx-auto max-w-7xl py-6 sm:px-6 lg:px-8  max-h-full">
    <div class="grid grid-cols-4 grid-rows-2 gap-4">
        <Card />
        <Card img="/images/image.png"/>
        
        <CardPlaceholder />
        <CardPlaceholder />
        <CardPlaceholder />
        <CardPlaceholder />
        <CardPlaceholder />
        <CardPlaceholder />
    </div>
</div>
