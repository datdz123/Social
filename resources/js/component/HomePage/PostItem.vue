<script setup>

import CreatePost from "@/component/HomePage/CreatePost.vue";
import {Disclosure, DisclosureButton, DisclosurePanel} from "@headlessui/vue";
import { ChevronUpIcon } from '@heroicons/vue/20/solid'


defineProps({
    post:Object
})


const truncateBody = (body) => {
    return body.length > 50 ? body.substring(0, 50) + '...' : body;
};
</script>

<template>
<div class="p-5">
    <div class="flex items-center">
        <a href="javascript:void(0)">
        <img :src="post.user.avatar" class="w-[40px] rounded-full">
        </a>
        <div class="mx-2">
            <a href="javascript:void(0)">
        <p class="font-bold">{{post.user.name}} </p>
            </a>
        <small class="text-gray-400">{{post.created_at}}</small>
        </div>
    </div>
    <div>

                <Disclosure v-slot="{ open }">
                    <p v-if="!open" class="px-4 pb-2 pt-4 text-sm text-gray-500"> {{truncateBody(post.body)}} </p>
                    <DisclosurePanel v-if="open" class="px-4 pb-2 pt-4 text-sm text-gray-500">
                        {{post.body}}
                    </DisclosurePanel>
                    <DisclosureButton
                        class="flex w-full justify-between rounded-lg  px-4 py-2 text-left text-sm font-medium   "
                    >
                        <span  class="text-blue-500">{{open ? 'Read Less' : 'Read More' }}</span>

                    </DisclosureButton>

                </Disclosure>
            </div>
        </div>

</template>

<style scoped>

</style>
