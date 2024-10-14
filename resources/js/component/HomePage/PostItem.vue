<script setup>

import CreatePost from "@/component/HomePage/CreatePost.vue";
import {Disclosure, DisclosureButton, DisclosurePanel} from "@headlessui/vue";
import {ChevronUpIcon} from '@heroicons/vue/20/solid'


defineProps({
    post: Object
})


const truncateBody = (body) => {
    return body.length > 50 ? body.substring(0, 50) + '...' : body;
};
</script>

<template>
    <div class="p-5 mt-3 bg-white">
        <div class="flex items-center">
            <a href="javascript:void(0)">
                <img :src="post.user.avatar" class="w-[40px] rounded-full">
            </a>
            <div class="mx-2">
                <a href="javascript:void(0)">
                    <p class="font-bold">{{ post.user.name }} </p>
                </a>
                <small class="text-gray-400">{{ post.created_at }}</small>
            </div>
        </div>
        <div>

            <Disclosure v-slot="{ open }">
                <p v-if="!open" class="px-4 pb-2 pt-4 text-sm text-gray-500"> {{ truncateBody(post.body) }} </p>
                <DisclosurePanel v-if="open" class="px-4 pb-2 pt-4 text-sm text-gray-500">
                    {{ post.body }}
                </DisclosurePanel>
                <DisclosureButton
                    class="flex w-full justify-between rounded-lg  px-4 py-2 text-left text-sm font-medium   "
                >
                    <span class="text-blue-500">{{ open ? 'Read Less' : 'Read More' }}</span>

                </DisclosureButton>
            </Disclosure>
            <div class="grid grid-cols-3 gap-3">
                <div v-for="(image, index) in post.images" :key="index" class="relative group">
                    <img :src="image.url" class="w-full h-auto">
                    <a :href="image.url" download class="absolute inset-0 flex items-center justify-center bg-black bg-opacity-50 opacity-0 group-hover:opacity-100 transition-opacity">
                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-8 h-8 text-white">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M12 16.5v-12m0 12l-3-3m3 3l3-3m-6 3h6m-6 0H6m6 0h6" />
                        </svg>
                    </a>
                </div>
            </div>
            <div class="flex justify-around mt-4">
                <div class="flex-grow mx-1">
                    <button class="flex items-center justify-center w-full bg-blue-100 text-blue-500 hover:bg-blue-200 px-3 py-2 rounded">
                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-6">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M6.633 10.25c.806 0 1.533-.446 2.031-1.08a9.041 9.041 0 0 1 2.861-2.4c.723-.384 1.35-.956 1.653-1.715a4.498 4.498 0 0 0 .322-1.672V2.75a.75.75 0 0 1 .75-.75 2.25 2.25 0 0 1 2.25 2.25c0 1.152-.26 2.243-.723 3.218-.266.558.107 1.282.725 1.282m0 0h3.126c1.026 0 1.945.694 2.054 1.715.045.422.068.85.068 1.285a11.95 11.95 0 0 1-2.649 7.521c-.388.482-.987.729-1.605.729H13.48c-.483 0-.964-.078-1.423-.23l-3.114-1.04a4.501 4.501 0 0 0-1.423-.23H5.904m10.598-9.75H14.25M5.904 18.5c.083.205.173.405.27.602.197.4-.078.898-.523.898h-.908c-.889 0-1.713-.518-1.972-1.368a12 12 0 0 1-.521-3.507c0-1.553.295-3.036.831-4.398C3.387 9.953 4.167 9.5 5 9.5h1.053c.472 0 .745.556.5.96a8.958 8.958 0 0 0-1.302 4.665c0 1.194.232 2.333.654 3.375Z" />
                        </svg>

                        Like
                    </button>
                </div>
                <div class="flex-grow mx-1">
                    <button class="flex items-center justify-center w-full bg-green-100 text-green-500 hover:bg-green-200 px-3 py-2 rounded">
                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-6">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M7.5 8.25h9m-9 3H12m-9.75 1.51c0 1.6 1.123 2.994 2.707 3.227 1.129.166 2.27.293 3.423.379.35.026.67.21.865.501L12 21l2.755-4.133a1.14 1.14 0 0 1 .865-.501 48.172 48.172 0 0 0 3.423-.379c1.584-.233 2.707-1.626 2.707-3.228V6.741c0-1.602-1.123-2.995-2.707-3.228A48.394 48.394 0 0 0 12 3c-2.392 0-4.744.175-7.043.513C3.373 3.746 2.25 5.14 2.25 6.741v6.018Z" />
                        </svg>

                        Comment
                    </button>
                </div>
            </div>
        </div>
    </div>

</template>

<style scoped>

</style>
