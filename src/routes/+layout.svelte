<script>
    import "../app.css";
    import Header from "./Header.svelte";
    import Footer from "./Footer.svelte";
</script>

<div class="min-h-full">
    <Header />
    <main class="min-h-[700px] w-full">
        <slot />
    </main>
    <Footer />
</div>
