<script>
    import SmallHeader from "../../SmallHeader.svelte";
    import Sidebar from "../Sidebar.svelte";
    import {
        Label,
        ButtonGroup,
        InputAddon,
        Input,
        Helper,
    } from "flowbite-svelte";
    import Button from "../../../CustomComponent/Button.svelte";
    import Breadcrumb from "../../../CustomComponent/Breadcrumb.svelte";
</script>

<SmallHeader header="My Page" padding="24" />

<div
    id="layout"
    class="max-w-7xl py-6 sm:px-6 lg:px-8  max-h-full flex m-auto justify-center"
>
    <Sidebar />

    <!-- 비밀번호 변경 -->
    <div class="ml-5 block w-[70%]">
        <Breadcrumb content="비밀번호 변경" />

        <div class="mt-3 p-10 rounded-lg shadow-md border">
            <!-- <div class="border-2 rounded-md p-10"> -->
            <h1 class="font-bold text-4xl mb-7">비밀번호 변경</h1>
            <!-- 이름 -->
            <div class="mb-6 w-[40%]">
                <Label for="default-input" class="block mb-2"
                    >현재 비밀번호</Label
                >
                <Input id="default-input" placeholder="Default input" />
            </div>

            <div class="mb-6 w-[40%]">
                <Label for="error" color="red" class="block mb-2"
                    >비밀번호 변경</Label
                >
                <Input id="error" color="red" placeholder="Success input" />
                <Helper class="mt-2" color="red"
                    ><span class="font-medium">Well done!</span> Some success messsage.</Helper
                >
            </div>

            <div class="mb-6 w-[40%]">
                <Label for="error" color="red" class="block mb-2"
                    >비밀번호 변경 확인</Label
                >
                <Input id="error" color="red" placeholder="Success input" />
                <Helper class="mt-2" color="red"
                    ><span class="font-medium">Well done!</span> Some success messsage.</Helper
                >
            </div>
            <!-- </div> -->
        </div>

        <!-- 저장 버튼 -->
        <!-- <div class="mt-3 p-2 rounded-lg shadow-md border "> -->
            <Button number="1" content="비밀번호 변경 확인" />
        <!-- </div> -->
    </div>
</div>
