<script>
    import "../app.css";
    import Header from "./Header.svelte";
    import Footer from "./Footer.svelte";
</script>

<div class="min-h-full">
    <!-- <Header /> -->
    <Header />
    <main class="min-h-[700px]">
        <slot />
    </main>
    <Footer />
</div>
