<script>
    import Sidebar from "./Sidebar.svelte";
    import SmallHeader from "../SmallHeader.svelte";
    import { Breadcrumb, BreadcrumbItem } from "flowbite-svelte";
    import { Label, Input, InputAddon, ButtonGroup } from "flowbite-svelte";
</script>

<SmallHeader header="My Page" />

<div
    id="layout"
    class="mx-auto max-w-7xl py-6 sm:px-6 lg:px-8  max-h-full flex"
>
    <Sidebar />

    <!-- 분리해야함 -->
    <div class="ml-3 block w-[100%]">
        <Breadcrumb aria-label="Solid background breadcrumb example" solid>
            <BreadcrumbItem href="/" home>홈</BreadcrumbItem>
            <BreadcrumbItem href="/">설정</BreadcrumbItem>
            <BreadcrumbItem>회원정보 수정</BreadcrumbItem>
        </Breadcrumb>

        <div class="mt-3 p-10 rounded-lg bg-gray-50">
            <!-- 이름 -->
            <div class="mb-6 w-[40%]">
                <Label for="website-admin" class="block mb-2">이름</Label>
                <ButtonGroup class="w-full">
                    <InputAddon>
                        <svg
                            xmlns="http://www.w3.org/2000/svg"
                            width="20"
                            height="20"
                            viewBox="0 0 24 24"
                            fill="none"
                            stroke="#000000"
                            stroke-width="2"
                            stroke-linecap="round"
                            stroke-linejoin="round"
                            ><path
                                d="M20 21v-2a4 4 0 0 0-4-4H8a4 4 0 0 0-4 4v2"
                            /><circle cx="12" cy="7" r="4" /></svg
                        >
                    </InputAddon>
                    <Input id="website-admin" placeholder="elonmusk" />
                </ButtonGroup>
            </div>

            <!-- 이메일 -->
            <div class="mb-6 w-[40%]">
                <Label for="email" class="block mb-2">이메일</Label>
                <ButtonGroup class="w-full">
                    <InputAddon>
                        <svg
                            aria-hidden="true"
                            class="w-5 h-5 text-gray-500 dark:text-gray-400"
                            fill="currentColor"
                            viewBox="0 0 20 20"
                            xmlns="http://www.w3.org/2000/svg"
                            ><path
                                d="M2.003 5.884L10 9.882l7.997-3.998A2 2 0 0016 4H4a2 2 0 00-1.997 1.884z"
                            /><path
                                d="M18 8.118l-8 4-8-4V14a2 2 0 002 2h12a2 2 0 002-2V8.118z"
                            /></svg
                        >
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
                        <svg
                            xmlns="http://www.w3.org/2000/svg"
                            width="20"
                            height="20"
                            viewBox="0 0 24 24"
                            fill="none"
                            stroke="#000000"
                            stroke-width="2"
                            stroke-linecap="round"
                            stroke-linejoin="round"
                            ><path
                                d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z"
                            /></svg
                        >
                    </InputAddon>
                    <Input
                        id="phoneNumber"
                        type="tel"
                        placeholder="010-####-####"
                    />
                </ButtonGroup>
            </div>
        </div>
    </div>
</div>
