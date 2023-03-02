<script>
    import "../app.css";
    import Header from "./Header.svelte";
    import Footer from "./Footer.svelte";

    import Headercopy from "./Headercopy.svelte";
</script>

<div class="min-h-full">
    <!-- <Header /> -->
    <Headercopy/>
    <main class="min-h-[700px]">
        <slot />
    </main>
    <Footer />
</div>
