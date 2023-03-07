<script>
    import Avatar from "../../CustomComponent/Avatar.svelte";
    import Button from "../../CustomComponent/Button.svelte";
</script>

<!-- background -->
<div id="layout">
    <div class="relative">
        <div class="h-48 bg-black" />
        <!-- profile -->
        <div
            class="w-[80%] h-80 rounded-xl bg-white absolute top-[70%] left-1/2  transform -translate-x-1/2 shadow-md border"
        >
            <Avatar number="0" />
            <Button number="0" />

            <div class="text-center mt-32">
                <div class="font-bold text-3xl">김종환</div>
                <div class="mt-3">다 같이 힘냅시다.</div>
                <div class="mt-3">금오공대 컴퓨터소프트웨어공학과</div>
            </div>
        </div>
    </div>

    <div class="w-[80%] h-[100px] mt-72 bg-white m-auto shadow-lg border rounded-xl" />
</div>
