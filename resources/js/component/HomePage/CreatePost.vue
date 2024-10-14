<script setup>



import {ref} from "vue";

const clickCreatePost = ref(false);

function toggleCreatePost() {
    clickCreatePost.value = !clickCreatePost.value;
}

</script>

<template>
    <div class=" p-5  text-gray-400 rounded-l-md bg-white">
        <div @click="toggleCreatePost" class="border-gray-200 border  p-3">
            Click here to create new post
        </div>
    </div>
    <div v-if="clickCreatePost" class="flex justify-between items-center px-5">
        <button type="button" class="text-sm font-semibold leading-6 text-gray-900">Cancel</button>
        <button type="submit" class="rounded-md bg-indigo-600 px-3 py-2 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600">Save</button>
    </div>
</template>

<style scoped>

</style>
