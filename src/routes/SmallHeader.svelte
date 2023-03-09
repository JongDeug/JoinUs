<script>
    export let header;
    export let padding;
</script>

<!-- padding이 undefined일 경우-->
{#if !padding}
    <header class="bg-white shadow">
        <div class="mx-auto max-w-7xl py-6 px-4 sm:px-6 lg:px-8">
            <h1 class="text-3xl font-bold tracking-tight text-gray-900">
                {header}
            </h1>
        </div>
    </header>
<!-- padding이 존재하면 -->
{:else}
    <header class="bg-white shadow">
        <div class="mx-auto max-w-7xl py-6 px-4 sm:px-6 lg:px-{padding}">
            <h1 class="text-3xl font-bold tracking-tight text-gray-900">
                {header}
            </h1>
        </div>
    </header>
{/if}
