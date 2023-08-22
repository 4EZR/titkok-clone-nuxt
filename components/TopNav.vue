<template>

    <div id="TopNav" class="fixed bg-white z-30 flex items-center w-full border-b h-[61px]">
        <div :class="route.fullpath === '/' ? 'max-w-[1150px]' : ''"
            class="flex items-center justify-between w-full  mx-auto">
            <div :class="route.fullpath === '/' ? 'w-[80%]' : 'lg:w-[20%] w-[70%]'"
                class="flex items-center justify-between w-full  mx-auto">

                <NuxtLink to="/">
                    <img width="115" src="~/assets/images/tiktok-logo.png" alt="">
                </NuxtLink>

            </div>
            <div class="hidden md:flex items-center bg-[#F1F1F2] p-1 rounded-full max-w-[380px] w-full">
                <input
                    type="text"
                    class="w-full pl-3 my-2 bg-transparent placeholder-[#838383] text-[15px] focus:outline-none"
                    placeholder="Search Accounts" />

                <div>
                    <Icon name="eva:search-outline" color="#A1A2A7" size="22"/>
                </div>

            </div>
            <div class="flex items-center justify-end gap-3 min-w-[275px] max-w-[320px] w-full">
                <button>
                    Upload
                </button>

            </div>

        </div>

    </div>
</template>

<script setup>
const route = useRoute()
</script>