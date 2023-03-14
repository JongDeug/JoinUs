<script>
    import SmallHeader from "../SmallHeader.svelte";
    import { Tabs, TabItem } from "flowbite-svelte";
    import {
        Table,
        TableBody,
        TableBodyCell,
        TableBodyRow,
        TableHead,
        TableHeadCell,
        Checkbox,
        Pagination,
    } from "flowbite-svelte";
    import Button from "../../CustomComponent/Button.svelte";
    import { page } from "$app/stores";

    let helper = { start: 1, end: 10, total: 100 };
    $: activeUrl = $page.url.searchParams.get("page");
    let pages = [
        { name: 1, href: "/components/pagination?page=1" },
        { name: 2, href: "/components/pagination?page=2" },
        { name: 3, href: "/components/pagination?page=3" },
        { name: 4, href: "/components/pagination?page=4" },
        { name: 5, href: "/components/pagination?page=5" },
    ];

    $: {
        pages.forEach((page) => {
            let splitUrl = page.href.split("?");
            let queryString = splitUrl.slice(1).join("?");
            const hrefParams = new URLSearchParams(queryString);
            let hrefValue = hrefParams.get("page");
            if (hrefValue === activeUrl) {
                page.active = true;
            } else {
                page.active = false;
            }
        });
        pages = pages;
    }

    const previous = () => {
        alert(
            "Previous btn clicked. Make a call to your server to fetch data."
        );
    };
    const next = () => {
        alert("Next btn clicked. Make a call to your server to fetch data.");
    };
</script>

<SmallHeader header="Post Message" />

<div id="layout" class="mx-auto max-w-7xl py-6 sm:px-6 lg:px-8  max-h-full">
    <div class="relative overflow-x-auto mt-6">
        <Tabs>
            <TabItem open>
                <span slot="title">받은 쪽지</span>

                <Table class="mb-6">
                    <TableHead>
                        <TableHeadCell class="!p-4">
                            <Checkbox />
                        </TableHeadCell>
                        <TableHeadCell>보낸 사람</TableHeadCell>
                        <TableHeadCell>제목</TableHeadCell>
                        <TableHeadCell>날짜</TableHeadCell>
                        <TableHeadCell>읽음 상태</TableHeadCell>
                    </TableHead>
                    <TableBody class="divide-y">
                        <TableBodyRow>
                            <TableBodyCell class="!p-4">
                                <Checkbox />
                            </TableBodyCell>
                            <TableBodyCell>Apple MacBook Pro 17"</TableBodyCell>
                            <TableBodyCell>Sliver</TableBodyCell>
                            <TableBodyCell>Laptop</TableBodyCell>
                            <TableBodyCell>Yes</TableBodyCell>
                        </TableBodyRow>
                        <TableBodyRow>
                            <TableBodyCell class="!p-4">
                                <Checkbox />
                            </TableBodyCell>
                            <TableBodyCell>Microsoft Surface Pro</TableBodyCell>
                            <TableBodyCell>White</TableBodyCell>
                            <TableBodyCell>Laptop PC</TableBodyCell>
                            <TableBodyCell>Laptop PC</TableBodyCell>
                        </TableBodyRow>
                        <TableBodyRow>
                            <TableBodyCell class="!p-4">
                                <Checkbox />
                            </TableBodyCell>
                            <TableBodyCell>Magic Mouse 2</TableBodyCell>
                            <TableBodyCell>Black</TableBodyCell>
                            <TableBodyCell>Accessories</TableBodyCell>
                            <TableBodyCell>Yes</TableBodyCell>
                        </TableBodyRow>
                    </TableBody>
                </Table>

                <div class="flex justify-between">
                    <Button usage="PostMessageDeleteBtn" content="삭제" />
                    <Button usage="PostMessageSendBtn" content="쪽지 보내기" />
                </div>

                <div class="flex justify-center">
                    <Pagination {pages} on:previous={previous} on:next={next} />
                </div>
            </TabItem>

            <TabItem>
                <span slot="title">보낸 쪽지</span>
                <Table class="mb-6">
                    <TableHead>
                        <TableHeadCell class="!p-4">
                            <Checkbox />
                        </TableHeadCell>
                        <TableHeadCell>받은 사람</TableHeadCell>
                        <TableHeadCell>제목</TableHeadCell>
                        <TableHeadCell>날짜</TableHeadCell>
                        <TableHeadCell>읽음 상태</TableHeadCell>
                    </TableHead>
                    <TableBody class="divide-y">
                        <TableBodyRow>
                            <TableBodyCell class="!p-4">
                                <Checkbox />
                            </TableBodyCell>
                            <TableBodyCell>Apple MacBook Pro 17"</TableBodyCell>
                            <TableBodyCell>Sliver</TableBodyCell>
                            <TableBodyCell>Laptop</TableBodyCell>
                            <TableBodyCell>Yes</TableBodyCell>
                        </TableBodyRow>
                        <TableBodyRow>
                            <TableBodyCell class="!p-4">
                                <Checkbox />
                            </TableBodyCell>
                            <TableBodyCell>Microsoft Surface Pro</TableBodyCell>
                            <TableBodyCell>White</TableBodyCell>
                            <TableBodyCell>Laptop PC</TableBodyCell>
                            <TableBodyCell>Laptop PC</TableBodyCell>
                        </TableBodyRow>
                        <TableBodyRow>
                            <TableBodyCell class="!p-4">
                                <Checkbox />
                            </TableBodyCell>
                            <TableBodyCell>Magic Mouse 2</TableBodyCell>
                            <TableBodyCell>Black</TableBodyCell>
                            <TableBodyCell>Accessories</TableBodyCell>
                            <TableBodyCell>Yes</TableBodyCell>
                        </TableBodyRow>
                    </TableBody>
                </Table>

                <div class="flex justify-between">
                    <Button usage="PostMessageDeleteBtn" content="삭제" />
                    <Button usage="PostMessageSendBtn" content="쪽지 보내기" />
                </div>

                <div class="flex justify-center">
                    <Pagination {pages} on:previous={previous} on:next={next} />
                </div>
            </TabItem>
        </Tabs>
    </div>
</div>
