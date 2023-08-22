<template>
    <div id="TopNav" class="flex justify-between items-center w-full border-b h-[61px] bg-white px-6">
        <!-- Part 1: Logo -->
        <div class="flex justify-start items-center w-1/3">
            <NuxtLink to="/">
                <img width="115" src="~/assets/images/tiktok-logo.png" alt="">
            </NuxtLink>
        </div>

        <!-- Part 2: Search Bar -->
        <div class="hidden md:flex justify-center items-center w-1/3 bg-[#F1F1F2] p-1 rounded-full">
            <input type="text" class="w-full pl-3 my-2 bg-transparent placeholder-[#838383] text-[15px] focus:outline-none"
                placeholder="Search Accounts" />

            <div class="px-3 py-1 flex items-center border-l border-l-gray-300">
                <Icon name="eva:search-outline" color="#A1A2A7" size="22" />
            </div>
        </div>

        <!-- Part 3: Buttons -->
        <div class="flex justify-end items-center w-1/3">
            <button class="flex items-center border rounded-sm px-3 py-[6px] hover:bg-gray-100 mr-2">
                <Icon name="mdi:plus" color="#000000" size="22" />
                <span class="px-2 font-medium text-[15px]">upload</span>
            </button>
            <div v-if="false">
                <button class="p-2 items-center rounded-md  px-3 py-[6px] bg-[#f02c56]">
                    <span class="px-2 font-medium text-[15px] text-white">log in</span>
                </button>
                <Icon name="ph:dots-three-vertical-bold" class='ml-4' color="#161724" size="22"></Icon>
            </div>

            <div class="flex items-center">
                <Icon name="bi:send" class="mx-4" color="#161724" size="25"></Icon>
                <Icon name="codicon:inbox" class='mr-4' color="#161724" size="25"></Icon>

                <div class="relative">
                    <button
                    @click="$event => showMenu = ! showMenu"
                    >
                        <img src="https://picsum.photos/200/200" class="rounded-full" width="33" alt="">
                    </button>

                    <div
                    v-if="showMenu"
                    id="dropdown-profile"
                        class="absolute bg-white rounded-lg  w-[200px] shadow-md p-2 top-[43px] -right-2">

                        <NuxtLink @click="showMenu = false"
                            class="flex items-center justify-start py-3 px-2 hover:bg-gray-100 cursor-pointer">
                            <Icon name="ph:user" size="20" />
                            <span class="pl-2 font-semibold text-md">profile</span>
                        </NuxtLink>
                        <div class="flex items-center justify-start py-3 px-1.5 hover:bg-gray-100 border-t cursor-pointer">
                            <Icon name="ic:outline-login" size="20" />
                            <span class="pl-2 font-semibold text-md">log out</span>
                        </div>
                    </div>

                </div>
            </div>
        </div>
    </div>
</template>
  

<script setup>
const route = useRoute()
let showMenu = ref(false);
</script>