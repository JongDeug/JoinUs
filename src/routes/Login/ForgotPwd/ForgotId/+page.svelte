<script>
    import { Label, Input } from "flowbite-svelte";
    import Button from "../../../../CustomComponent/Button.svelte";
</script>

<!-- redirect to login -->

<div id="layout" class="mx-auto max-w-7xl py-12 sm:px-6 lg:px-8  max-h-full">
    <div class="p-8 border w-[60%] m-auto shadow-lg">
        <h1 class="font-bold text-4xl mb-7">아이디 찾기</h1>

        <div class="mb-6">
            <Label for="success" class="block mb-2">이름</Label>
            <Input id="success" placeholder="Success input" />
        </div>
        <div class="mb-6">
            <Label for="success" class="block mb-2">이메일</Label>
            <Input id="success" placeholder="Success input" type="email" />
        </div>

        <div class="mb-6">
            <Label for="success" class="block mb-2">전화번호</Label>
            <Input id="success" placeholder="010-1234-1234" type="tel" />
        </div>

        <Button number="1" content="확인" />
    </div>
</div>
