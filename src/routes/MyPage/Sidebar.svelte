<script>
    import {
        Sidebar,
        SidebarGroup,
        SidebarItem,
        SidebarBrand,
        SidebarWrapper,
        SidebarDropdownItem,
        SidebarDropdownWrapper,
    } from "flowbite-svelte";
    let spanClass = "flex-1 ml-3 whitespace-nowrap";

    let site = {
        name: "JoinUs",
        href: "/",
        img: "/images/JoinUs.png",
    };
</script>

<Sidebar>
    <div
        class="overflow-y-auto py-4 px-3  dark:bg-gray-800 rounded-lg"
    >
        <SidebarGroup>
            <SidebarBrand {site} />
            <!-- <SidebarItem label="소개페이지">
                <svelte:fragment slot="icon">
                    <svg
                        xmlns="http://www.w3.org/2000/svg"
                        fill="none"
                        viewBox="0 0 24 24"
                        stroke-width="1.5"
                        stroke="currentColor"
                        class="w-6 h-6"
                        ><path
                            stroke-linecap="round"
                            stroke-linejoin="round"
                            d="M10.5 6a7.5 7.5 0 107.5 7.5h-7.5V6z"
                        /><path
                            stroke-linecap="round"
                            stroke-linejoin="round"
                            d="M13.5 10.5H21A7.5 7.5 0 0013.5 3v7.5z"
                        /></svg
                    >
                </svelte:fragment>
            </SidebarItem> -->
            <SidebarDropdownWrapper label="회원정보">
                <svelte:fragment slot="icon">
                    <svg
                        xmlns="http://www.w3.org/2000/svg"
                        fill="none"
                        viewBox="0 0 24 24"
                        stroke-width="1.5"
                        stroke="currentColor"
                        class="w-6 h-6"
                        ><path
                            stroke-linecap="round"
                            stroke-linejoin="round"
                            d="M15.75 6a3.75 3.75 0 11-7.5 0 3.75 3.75 0 017.5 0zM4.501 20.118a7.5 7.5 0 0114.998 0A17.933 17.933 0 0112 21.75c-2.676 0-5.216-.584-7.499-1.632z"
                        /></svg
                    >
                </svelte:fragment>
                <SidebarDropdownItem label="회원정보 수정" href="/MyPage"/>
                <SidebarDropdownItem label="비밀번호 변경" href="/MyPage/ChangePwd"/>
                <SidebarDropdownItem label="회원 탈퇴" />
            </SidebarDropdownWrapper>

            <!-- <SidebarItem label="쪽지" {spanClass}>
                <svelte:fragment slot="icon">
                    <svg
                        xmlns="http://www.w3.org/2000/svg"
                        fill="none"
                        viewBox="0 0 24 24"
                        stroke-width="1.5"
                        stroke="currentColor"
                        class="w-6 h-6"
                        ><path
                            stroke-linecap="round"
                            stroke-linejoin="round"
                            d="M9 3.75H6.912a2.25 2.25 0 00-2.15 1.588L2.35 13.177a2.25 2.25 0 00-.1.661V18a2.25 2.25 0 002.25 2.25h15A2.25 2.25 0 0021.75 18v-4.162c0-.224-.034-.447-.1-.661L19.24 5.338a2.25 2.25 0 00-2.15-1.588H15M2.25 13.5h3.86a2.25 2.25 0 012.012 1.244l.256.512a2.25 2.25 0 002.013 1.244h3.218a2.25 2.25 0 002.013-1.244l.256-.512a2.25 2.25 0 012.013-1.244h3.859M12 3v8.25m0 0l-3-3m3 3l3-3"
                        /></svg
                    >
                </svelte:fragment>
                <svelte:fragment slot="subtext">
                    <span
                        class="inline-flex justify-center items-center p-3 ml-3 w-3 h-3 text-sm font-medium text-blue-600 bg-blue-200 rounded-full dark:bg-blue-900 dark:text-blue-200"
                        >3</span
                    >
                </svelte:fragment>
            </SidebarItem> -->
            <SidebarItem label="내 팀" href="/MyPage/MyTeam">
                <svelte:fragment slot="icon">
                    <svg
                        xmlns="http://www.w3.org/2000/svg"
                        width="24"
                        height="24"
                        viewBox="0 0 24 24"
                        fill="none"
                        stroke="#000000"
                        stroke-width="2"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        ><path
                            d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"
                        /><circle cx="9" cy="7" r="4" /><path
                            d="M23 21v-2a4 4 0 0 0-3-3.87"
                        /><path d="M16 3.13a4 4 0 0 1 0 7.75" /></svg
                    >
                </svelte:fragment>
            </SidebarItem>
            <SidebarItem label="내가 작성한 게시글">
                <svelte:fragment slot="icon">
                    <svg
                        xmlns="http://www.w3.org/2000/svg"
                        fill="none"
                        viewBox="0 0 24 24"
                        stroke-width="1.5"
                        stroke="currentColor"
                        class="w-6 h-6"
                    >
                        <path
                            d="M16 4h2a2 2 0 0 1 2 2v14a2 2 0 0 1-2 2H6a2 2 0 0 1-2-2V6a2 2 0 0 1 2-2h2"
                        />
                        <rect x="8" y="2" width="8" height="4" rx="1" ry="1" />
                    </svg>
                </svelte:fragment>
            </SidebarItem>
            <SidebarItem label="Log out">
                <svelte:fragment slot="icon">
                    <svg
                        xmlns="http://www.w3.org/2000/svg"
                        fill="none"
                        viewBox="0 0 24 24"
                        stroke-width="1.5"
                        stroke="currentColor"
                        class="w-6 h-6"
                    >
                        <path
                            d="M10 3H6a2 2 0 0 0-2 2v14c0 1.1.9 2 2 2h4M16 17l5-5-5-5M19.8 12H9"
                        />
                    </svg>
                </svelte:fragment>
            </SidebarItem>
            <!-- <hr class="h-px my-8 bg-gray-200 border-2 dark:bg-gray-700" /> -->
        </SidebarGroup>
    </div>
</Sidebar>
