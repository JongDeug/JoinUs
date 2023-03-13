<script>
    export let header;
</script>

<header class="bg-white shadow">
    <div
        class="mx-auto max-w-7xl py-6 px-4 sm:px-6 {header == 'Board' | header == 'My Team' | header == 'FAQ'
            ? 'lg:px-8'
            : 'lg:px-20'}"
    >
        <h1 class="text-3xl font-bold tracking-tight text-gray-900">
            {header}
        </h1>
    </div>
</header>
