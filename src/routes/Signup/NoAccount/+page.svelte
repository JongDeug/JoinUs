<script>
    import { Label, Input, Helper } from "flowbite-svelte";
    import Button from "../../../CustomComponent/Button.svelte";
</script>

<!-- redirect to MyPage -->

<div id="layout" class="mx-auto max-w-7xl py-12 sm:px-6 lg:px-8  max-h-full">
    <div class="p-8 border w-[60%] m-auto shadow-lg">
        <h1 class="font-bold text-4xl mb-7">회원가입</h1>

        <div class="mb-6">
            <Label for="success" color="green" class="block mb-2">아이디</Label>

            <div class="flex items-center">
                <Input id="success" color="green" placeholder="Success input" />
                <Button number="2" />
            </div>

            <Helper class="mt-2" color="green"
                ><span class="font-medium">Well done!</span> Some success messsage.</Helper
            >
        </div>

        <div class="mb-6">
            <Label for="success" color="green" class="block mb-2"
                >비밀번호</Label
            >
            <Input id="success" color="green" placeholder="Success input" />
            <Helper class="mt-2" color="green"
                ><span class="font-medium">Well done!</span> Some success messsage.</Helper
            >
        </div>
        <div class="mb-6">
            <Label for="success" color="green" class="block mb-2"
                >비밀번호 확인</Label
            >
            <Input id="success" color="green" placeholder="Success input" />
            <Helper class="mt-2" color="green"
                ><span class="font-medium">Well done!</span> Some success messsage.</Helper
            >
        </div>

        <div class="mb-6">
            <Label for="success" color="green" class="block mb-2">이메일</Label>
            <Input
                id="success"
                color="green"
                placeholder="Success input"
                type="email"
            />
            <Helper class="mt-2" color="green"
                ><span class="font-medium">Well done!</span> Some success messsage.</Helper
            >
        </div>

        <Button
            number="1"
            content="다음"
            location="/Signup/NoAccount/Profile"
        />
    </div>
</div>
