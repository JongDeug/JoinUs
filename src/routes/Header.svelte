<script>
    import { fade, fly } from "svelte/transition";
    import { clickOutside } from "./clickOutside";

    // import { createEventDispatcher } from "svelte";
    // const dispatch = createEventDispatcher();

    let profileStatus = false;

    const handleProfileStatus = () => {
        profileStatus = !profileStatus;
    };

    let mobileMenu = false;
    const handleMobileStauts = () => {
        mobileMenu = !mobileMenu;
    };

    let current = "Board";
    const clickBoard = () => {
        current = "Board";
    };
    const clickMyTeam = () => {
        current = "MyTeam";
    };
    const clickFAQ = () => {
        current = "FAQ";
    };
</script>

<nav class="bg-[#95E0C8]">
    <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
        <div class="flex h-16 items-center justify-between">
            <div class="flex items-center">
                <div class="flex-shrink-0 text-4xl font-pacifco">
                    <a href="/" on:click={clickBoard} class="flex content-center">
                        <img src="/images/JoinUs.png" alt="" class="w-11 h-11 mr-3" />
                        Join.us
                    </a>
                </div>
                <div class="hidden md:block">
                    <div class="ml-10 flex items-baseline space-x-4">
                        <!-- Current: "bg-gray-900 text-white", Default: "text-gray-300 hover:bg-gray-700 hover:text-white" -->
                        <a
                            href="/"
                            class="{current === 'Board'
                                ? 'bg-gray-900 text-white'
                                : ''} hover:bg-gray-700 hover:text-white px-3 py-2 rounded-md text-sm font-medium focus:ring-4 focus:outline-none"
                            on:click={clickBoard}
                            aria-current="page">게시판</a
                        >

                        <a
                            href="MyTeam"
                            class="{current === 'MyTeam'
                                ? 'bg-gray-900 text-white'
                                : ''} hover:bg-gray-700 hover:text-white px-3 py-2 rounded-md text-sm font-medium focus:ring-4 focus:outline-none"
                            on:click={clickMyTeam}>내 팀</a
                        >

                        <a
                            href="FAQ"
                            class="{current === 'FAQ'
                                ? 'bg-gray-900 text-white'
                                : ''} hover:bg-gray-700 hover:text-white px-3 py-2 rounded-md text-sm font-medium focus:ring-4 focus:outline-none"
                            on:click={clickFAQ}>FAQ</a
                        >
                    </div>
                </div>
            </div>
            <div class="hidden md:block">
                <div class="ml-4 flex items-center md:ml-6">
                    <!-- 로그인 상태가 아니라면 -->
                    <!-- 회원 가입 -->
                    <div class="ml-2">
                        <a
                            href="Signup"
                            class="bg-gray-900 text-white px-3 py-2 rounded-md text-sm font-medium focus:ring-4 focus:outline-none"
                            aria-current="page">회원가입</a
                        >
                    </div>
                    <!-- 로그인 -->
                    <div class="ml-2">
                        <a
                            href="/Login"
                            class="bg-gray-900 text-white px-3 py-2 rounded-md text-sm font-medium focus:ring-4 focus:outline-none"
                            aria-current="page">로그인</a
                        >
                    </div>

                    <!-- 로그인인 상태라면 -->
                    <div class="ml-4 flex items-center md:ml-6">
                        <!-- 알림 버튼 -->
                        <button
                            type="button"
                            class="rounded-full bg-gray-800 p-1 text-gray-400 hover:text-white focus:outline-none focus:ring-2 focus:ring-white focus:ring-offset-2 focus:ring-offset-gray-800"
                        >
                            <span class="sr-only">View notifications</span>
                            <svg
                                class="h-6 w-6"
                                fill="none"
                                viewBox="0 0 24 24"
                                stroke-width="1.5"
                                stroke="currentColor"
                                aria-hidden="true"
                            >
                                <path
                                    stroke-linecap="round"
                                    stroke-linejoin="round"
                                    d="M14.857 17.082a23.848 23.848 0 005.454-1.31A8.967 8.967 0 0118 9.75v-.7V9A6 6 0 006 9v.75a8.967 8.967 0 01-2.312 6.022c1.733.64 3.56 1.085 5.455 1.31m5.714 0a24.255 24.255 0 01-5.714 0m5.714 0a3 3 0 11-5.714 0"
                                />
                            </svg>
                        </button>
                        
                        <!-- 프로필 사진 -->
                        <div class="relative ml-3">
                            <button
                                type="button"
                                class="flex max-w-xs items-center rounded-full bg-gray-800 text-sm focus:outline-none focus:ring-2 focus:ring-white focus:ring-offset-2 focus:ring-offset-gray-800"
                                id="user-menu-button"
                                aria-expanded="false"
                                aria-haspopup="true"
                                on:click={handleProfileStatus}
                            >
                                <span class="sr-only">Open my profile</span>
                                <img
                                    class="h-8 w-8 rounded-full"
                                    src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
                                    alt=""
                                />
                            </button>

                            <!-- 프로필 사진 클릭 시 -->
                            {#if profileStatus}
                                <div
                                    class="absolute right-[-5px] z-10 mt-2 w-48 origin-top-right rounded-md bg-white py-1 shadow-lg ring-1 ring-black ring-opacity-5 focus:outline-none"
                                    role="menu"
                                    aria-orientation="vertical"
                                    aria-labelledby="user-menu-button"
                                    tabindex="-1"
                                    transition:fade={{ duration: 90 }}
                                    use:clickOutside
                                    on:clickOutside={handleProfileStatus}
                                >
                                    <!-- Active: "bg-gray-100", Not Active: "" -->
                                    <a
                                        href="/Profile"
                                        class="block px-4 py-2 m-2 text-sm text-gray-700 rounded-lg hover:bg-slate-300 font-bold"
                                        role="menuitem"
                                        tabindex="-1"
                                        id="user-menu-item-0">Jong Hwan Kim <br/>@id</a
                                    >

                                    <hr
                                        class="h-px mt-3 mb-2 bg-gray-200 border-0 dark:bg-gray-700 "
                                    />

                                    <a
                                        href="/MyPage"
                                        class="block px-4 py-2 m-2 text-sm  text-gray-700 rounded-lg hover:bg-slate-300"
                                        role="menuitem"
                                        tabindex="-1"
                                        id="user-menu-item-1">설정</a
                                    >

                                    <a
                                        href="/MyPage"
                                        class="block px-4 py-2 m-2 text-sm  text-gray-700 rounded-lg hover:bg-slate-300"
                                        role="menuitem"
                                        tabindex="-1"
                                        id="user-menu-item-1"
                                        >쪽지
                                    </a>
                                    <hr
                                        class="h-px my-2 bg-gray-200 border-0 dark:bg-gray-700 "
                                    />

                                    <a
                                        href="#"
                                        class="block px-4 py-2 m-2 text-sm text-gray-700 rounded-lg hover:bg-slate-300"
                                        role="menuitem"
                                        tabindex="-1"
                                        id="user-menu-item-2">로그아웃</a
                                    >
                                </div>
                            {/if}
                        </div>
                    </div>
                </div>
            </div>
            <div class="-mr-2 flex md:hidden">
                <!-- Mobile menu button -->
                <button
                    type="button"
                    class="inline-flex items-center justify-center rounded-md bg-gray-800 p-2 text-gray-400 hover:bg-gray-700 hover:text-white focus:outline-none focus:ring-2 focus:ring-white focus:ring-offset-2 focus:ring-offset-gray-800"
                    aria-controls="mobile-menu"
                    aria-expanded="false"
                    on:click={handleMobileStauts}
                >
                    <span class="sr-only">Open main menu</span>

                    <svg
                        class="block h-6 w-6"
                        xmlns="http://www.w3.org/2000/svg"
                        fill="none"
                        viewBox="0 0 24 24"
                        stroke-width="1.5"
                        stroke="currentColor"
                        aria-hidden="true"
                    >
                        <path
                            stroke-linecap="round"
                            stroke-linejoin="round"
                            d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
                        />
                    </svg>

                    <svg
                        class="hidden h-6 w-6"
                        xmlns="http://www.w3.org/2000/svg"
                        fill="none"
                        viewBox="0 0 24 24"
                        stroke-width="1.5"
                        stroke="currentColor"
                        aria-hidden="true"
                    >
                        <path
                            stroke-linecap="round"
                            stroke-linejoin="round"
                            d="M6 18L18 6M6 6l12 12"
                        />
                    </svg>
                </button>
            </div>
        </div>
    </div>

    {#if mobileMenu}
        <!-- Mobile menu, show/hide based on menu state. -->
        <div
            class="md:hidden"
            id="mobile-menu"
            transition:fly={{ y: -10, duration: 400 }}
        >
            <div class="space-y-1 px-2 pt-2 pb-3 sm:px-3">
                <!-- Current: "bg-gray-900 text-white", Default: "text-gray-300 hover:bg-gray-700 hover:text-white" -->
                <a
                    href="#"
                    class="bg-gray-900 text-white block px-3 py-2 rounded-md text-base font-medium"
                    aria-current="page">게시판</a
                >

                <a
                    href="#"
                    class="text-gray-300 hover:bg-gray-700 hover:text-white block px-3 py-2 rounded-md text-base font-medium"
                    >내 팀</a
                >

                <a
                    href="#"
                    class="text-gray-300 hover:bg-gray-700 hover:text-white block px-3 py-2 rounded-md text-base font-medium"
                    >F&Q</a
                >
            </div>
            <!-- 반응형 -->
            <div class="border-t border-gray-700 pt-4 pb-3">
                <div class="flex items-center px-5">
                    <div class="flex-shrink-0">
                        <img
                            class="h-10 w-10 rounded-full"
                            src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
                            alt=""
                        />
                    </div>
                    <div class="ml-3">
                        <div
                            class="text-base font-medium leading-none text-white"
                        >
                            Tom Cook
                        </div>
                        <div
                            class="text-sm font-medium leading-none text-gray-400"
                        >
                            tom@example.com
                        </div>
                    </div>
                    <button
                        type="button"
                        class="ml-auto flex-shrink-0 rounded-full bg-gray-800 p-1 text-gray-400 hover:text-white focus:outline-none focus:ring-2 focus:ring-white focus:ring-offset-2 focus:ring-offset-gray-800"
                    >
                        <span class="sr-only">View notifications</span>
                        <svg
                            class="h-6 w-6"
                            xmlns="http://www.w3.org/2000/svg"
                            fill="none"
                            viewBox="0 0 24 24"
                            stroke-width="1.5"
                            stroke="currentColor"
                            aria-hidden="true"
                        >
                            <path
                                stroke-linecap="round"
                                stroke-linejoin="round"
                                d="M14.857 17.082a23.848 23.848 0 005.454-1.31A8.967 8.967 0 0118 9.75v-.7V9A6 6 0 006 9v.75a8.967 8.967 0 01-2.312 6.022c1.733.64 3.56 1.085 5.455 1.31m5.714 0a24.255 24.255 0 01-5.714 0m5.714 0a3 3 0 11-5.714 0"
                            />
                        </svg>
                    </button>
                </div>
                <div class="mt-3 space-y-1 px-2">
                    <a
                        href="#"
                        class="block rounded-md px-3 py-2 text-base font-medium text-gray-400 hover:bg-gray-700 hover:text-white"
                        >Your Profile</a
                    >

                    <a
                        href="#"
                        class="block rounded-md px-3 py-2 text-base font-medium text-gray-400 hover:bg-gray-700 hover:text-white"
                        >Settings</a
                    >

                    <a
                        href="#"
                        class="block rounded-md px-3 py-2 text-base font-medium text-gray-400 hover:bg-gray-700 hover:text-white"
                        >Sign out</a
                    >
                </div>
            </div>
        </div>
    {/if}
</nav>
