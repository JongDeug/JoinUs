<script>
    import { Label, Input, } from "flowbite-svelte";
    import Button from "../../../CustomComponent/Button.svelte";
</script>

<!-- redirect to login -->

<div id="layout" class="mx-auto max-w-7xl py-12 sm:px-6 lg:px-8  max-h-full">
    <div class="p-8 border w-[60%] m-auto shadow-lg">
        <h1 class="font-bold text-4xl mb-7">비밀번호 찾기</h1>

        <div class="mb-6">
            <Label for="success" class="block mb-2">아이디</Label>
            <Input id="success" placeholder="Success input" />
        </div>
        <div class="mb-6">
            <Label for="success" class="block mb-2">이메일</Label>
            <Input id="success" placeholder="Success input" />
        </div>

        <Button number="1" content="확인" />

        <div class="mt-4 text-center">
            <a href="/Login/ForgotPwd/ForgotId" class="text-blue-700 underline"
                >아이디를 잊으셨나요?</a
            >
        </div>
    </div>
</div>
