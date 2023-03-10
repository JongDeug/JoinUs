<script>
    import Sidebar from "./Sidebar.svelte";
    import SmallHeader from "../SmallHeader.svelte";
    import {
        Label,
        Input,
        InputAddon,
        ButtonGroup,
        Checkbox,
    } from "flowbite-svelte";
    import Svg from "../../CustomComponent/Svg.svelte";
    import Avatar from "../../CustomComponent/Avatar.svelte";
    import Button from "../../CustomComponent/Button.svelte";
    import Breadcrumb from "../../CustomComponent/Breadcrumb.svelte";

    // file input tag의 id 설정
    let fileuploadprops = {
        id: "user_avatar",
    };
</script>

<SmallHeader header="My Page" padding=24/>

<div
    id="layout"
    class="max-w-7xl py-6 sm:px-6 lg:px-8  max-h-full flex m-auto justify-center"
>
    <Sidebar />

    <!-- 분리해야함 -->
    <div class="ml-5 block w-[70%]">
    
        <Breadcrumb content="회원정보 수정" />

        <!-- 사용자 -->
        <div class="mt-3 p-10 rounded-lg shadow-md border ">
                <h1 class="font-bold text-4xl mb-7">사용자</h1>
                <!-- 이름 -->
                <div class="mb-6 w-[40%]">
                    <Label for="website-admin" class="block mb-2">이름</Label>
                    <ButtonGroup class="w-full">
                        <InputAddon>
                            <Svg svgName="이름" />
                        </InputAddon>
                        <Input id="website-admin" placeholder="elonmusk" />
                    </ButtonGroup>
                </div>

                <!-- 이메일 -->
                <div class="mb-6 w-[40%]">
                    <Label for="email" class="block mb-2">이메일</Label>
                    <ButtonGroup class="w-full">
                        <InputAddon>
                            <Svg svgName="이메일" />
                        </InputAddon>
                        <Input
                            id="email"
                            type="email"
                            placeholder="name@gmail.com"
                        />
                    </ButtonGroup>
                </div>

                <!-- 전화번호 -->
                <div class="mb-6 w-[40%]">
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
                <div class="mb-6 w-[40%]">
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

                <div class="w-[70%]">
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
        </div>

        <!-- 개인 포트폴리오 -->
        <div class="mt-3 p-10 rounded-lg  shadow-md border">
                <h1 class="font-bold text-4xl mb-7">개인 포트폴리오</h1>
                <!-- 간단한 자기소개 -->
                <div class="mb-6 w-[40%]">
                    <Label for="default-input" class="block mb-2"
                        >간단한 자기소개</Label
                    >
                    <Input id="default-input" placeholder="Default input" />
                </div>

                <!-- 웹사이트 -->
                <div class="mb-6 w-[40%]">
                    <Label for="default-input" class="block mb-2"
                        >웹사이트</Label
                    >
                    <Input id="default-input" placeholder="Default input" />
                </div>

                <!-- 깃허브 주소 -->
                <div class="mb-6 w-[40%]">
                    <Label for="default-input" class="block mb-2"
                        >깃허브 주소</Label
                    >
                    <Input id="default-input" placeholder="Default input" />
                </div>

                <!-- 기술스택 -->
                <div class="mb-6 w-[40%]">
                    <Label for="default-input" class="block mb-2"
                        >기술스택</Label
                    >
                    <div class="grid grid-cols-2 gap-4">
                        <Checkbox>Default checkbox</Checkbox>
                        <Checkbox checked>Checked state</Checkbox>
                        <Checkbox checked>Checked state</Checkbox>
                        <Checkbox checked>Checked state</Checkbox>
                    </div>
                </div>
        </div>

        <!-- 저장 버튼 -->
        <!-- <div class="mt-3 p-2 rounded-lg  shadow-md border "> -->
            <Button number=1 content="회원정보 수정 확인" />
        <!-- </div> -->
    </div>
</div>
