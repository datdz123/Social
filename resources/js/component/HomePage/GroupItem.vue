<script setup>
defineProps({
    image: {
        type: String,
    },
    Title: {
        type: String,
    },
    Description: {
        type: String,
    },
});
</script>

<template>

    <div class="flex items-start  cursor-pointer hover:bg-gray-300 mb-5 mt-5">
        <div class="">
            <img class=" sm:w-[60px] max-w-[60px] rounded-full" :src="image">
        </div>
        <div class="">
            <h2 class="text-[25px] sm:text-[18px] font-bold  ">
                {{Title}}
            </h2>
            <p class="text-[18px] sm:text-[16px]">
                {{Description}}
            </p>
        </div>
    </div>
</template>

<style scoped>

</style>
