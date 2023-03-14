<script>
    import SmallHeader from "../../../SmallHeader.svelte";
    import Sidebar from "../../../../CustomComponent/Sidebar.svelte";
    import {
        Label,
        Avatar,
        Input,
        Listgroup,
        ListgroupItem,
        Search,
        CloseButton,
    } from "flowbite-svelte";
    import Breadcrumb from "../../../../CustomComponent/Breadcrumb.svelte";
    import Button from "../../../../CustomComponent/Button.svelte";

    import { Textarea } from "flowbite-svelte";
    let textareaprops = {
        id: "message",
        name: "message",
        rows: 4,
        placeholder: "팀을 소개해주세요...",
    };
</script>

<!-- 팀 명  -->
<SmallHeader header="abcd" />
<div
    id="layout"
    class="max-w-7xl py-6 sm:px-6 lg:px-8  max-h-full flex m-auto justify-center"
>
    <Sidebar number="1" />
    <div class="ml-5 block w-[70%]">
        <Breadcrumb prevContent="내 팀" nextContent="설정" />

        <div class="mt-6 p-10 rounded-lg shadow-md border ">
            <h1 class="font-bold text-4xl mb-7">설정</h1>

            <div class="mb-6 w-[40%]">
                <Label for="default-input" class="block mb-2">팀 명</Label>
                <Input id="default-input" placeholder="Default input" />
            </div>

            <div class="mb-6 w-[60%]">
                <Label for="message" class="block mb-2">팀 소개</Label>
                <Textarea {...textareaprops} />
            </div>

            <div class="mb-6 w-[60%]">
                <div class="mb-6">
                    <Label for="phoneNumber" class="block mb-2"
                        >팀원 리스트</Label
                    >
                    <Search />
                </div>
                <Listgroup active>
                    <h3
                        class="text-center bg-blue-500 text-white font-bold rounded-t-lg"
                    >
                        팀원 목록
                    </h3>
                    <ListgroupItem class="text-base font-semibold gap-2">
                        <Avatar src="" size="xs" />Jese Leos

                        <CloseButton />
                    </ListgroupItem>
                    <ListgroupItem class="text-base font-semibold gap-2">
                        <Avatar src="" size="xs" />Robert Gouth

                        <CloseButton />
                    </ListgroupItem>
                </Listgroup>
            </div>

            <div class="w-[70%] mb-6">
                <Label class="mb-3">팀 배경 사진</Label>
                <div class="flex items-center">
                    <input
                        type="file"
                        id="user_avatar"
                        class="h-full w-full disabled:cursor-not-allowed disabled:opacity-50 focus:border-blue-500 focus:ring-blue-500 dark:focus:border-blue-500 dark:focus:ring-blue-500 bg-gray-50 text-gray-900 dark:bg-gray-700 dark:text-white dark:placeholder-gray-400 border-gray-300 dark:border-gray-600  text-sm rounded-lg border dark:text-gray-400"
                    />
                    <!-- <Fileupload {...fileuploadprops} /> -->
                </div>
            </div>
            
            <div class="mb-6 w-[40%]">
                <Label for="default-input" class="block mb-2">회의방 비밀번호</Label>
                <Input id="default-input" placeholder="Default input" />
            </div>

            <Button number="1" content="저장" />
        </div>
    </div>
</div>
