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
    <div class="flex items-start  cursor-pointer hover:bg-gray-300 ">
        <div class="">
            <img class="lg:w-[80px] sm:w-full rounded-full" :src="image">
        </div>
        <div class="">
            <h2 class="text-[25px] font-bold">
                {{Title}}
            </h2>
            <p class="text-[15px]">
               {{Description}}
            </p>
        </div>
    </div>
</template>

<style scoped>

</style>
