<script>
    import { Label, Input, Helper } from "flowbite-svelte";
    import { InputAddon, ButtonGroup, Checkbox } from "flowbite-svelte";
    import Svg from "../../../../CustomComponent/Svg.svelte";
    import Avatar from "../../../../CustomComponent/Avatar.svelte";
    import Button from "../../../../CustomComponent/Button.svelte";
</script>

<!-- redirect to MyPage -->

<div id="layout" class="mx-auto max-w-7xl py-12 sm:px-6 lg:px-8  max-h-full">
    <div class="p-8 border w-[60%] m-auto shadow-lg">
        <h1 class="font-bold text-4xl mb-7">회원정보</h1>
        <!-- 사용자 -->
        <!-- 이름 -->
        <div class="mb-6">
            <Label for="website-admin" class="block mb-2">이름</Label>
            <ButtonGroup class="w-full">
                <InputAddon>
                    <Svg svgName="이름" />
                </InputAddon>
                <Input id="website-admin" placeholder="elonmusk" />
            </ButtonGroup>
        </div>

        <!-- 이메일 -->
        <div class="mb-6">
            <Label for="email" class="block mb-2">이메일</Label>
            <ButtonGroup class="w-full">
                <InputAddon>
                    <Svg svgName="이메일" />
                </InputAddon>
                <Input id="email" type="email" placeholder="name@gmail.com" />
            </ButtonGroup>
        </div>

        <!-- 전화번호 -->
        <div class="mb-6">
            <Label for="phoneNumber" class="block mb-2">전화번호</Label>
            <ButtonGroup class="w-full">
                <InputAddon>
                    <Svg svgName="전화번호" />
                </InputAddon>
                <Input
                    id="phoneNumber"
                    type="tel"
                    placeholder="010-####-####"
                />
            </ButtonGroup>
        </div>

        <!-- 소속 -->
        <div class="mb-6">
            <Label for="phoneNumber" class="block mb-2">소속</Label>
            <ButtonGroup class="w-full">
                <InputAddon>
                    <Svg svgName="소속" />
                </InputAddon>
                <Input
                    id="phoneNumber"
                    type="tel"
                    placeholder="010-####-####"
                />
            </ButtonGroup>
        </div>

        <div class="w-[70%] mb-6">
            <Label class="mb-3">프로필 사진</Label>
            <div class="flex items-center">
                <Avatar number="1" />
                <input
                    type="file"
                    id="user_avatar"
                    class="h-full w-full disabled:cursor-not-allowed disabled:opacity-50 focus:border-blue-500 focus:ring-blue-500 dark:focus:border-blue-500 dark:focus:ring-blue-500 bg-gray-50 text-gray-900 dark:bg-gray-700 dark:text-white dark:placeholder-gray-400 border-gray-300 dark:border-gray-600  text-sm rounded-lg border dark:text-gray-400"
                />
                <!-- <Fileupload {...fileuploadprops} /> -->
            </div>
        </div>

        <Button
            number="1"
            content="확인"
            location="/Login"
        />
    </div>
</div>
