<script setup>

import PostItem from "@/component/HomePage/PostItem.vue";
const post1={
    user:{
        id:1,
        name:"John Doe",
        avatar:"https://cdn.cloudflare.steamstatic.com/steamcommunity/public/images/avatars/d1/d1697d20ad05795d151693103e165f038a877f5d_full.jpg",
    },
    body:"Lorem ipsum dolor sit amet consectetur adipiscing, elit leo ad cras a neque, iaculis sed porta in congue. Ut molestie mattis convallis faucibus eu cras dictumst fermentum, malesuada condimentum ad arcu sed id mollis enim, donec feugiat blandit netus eros libero penatibus. ",
    created_at:"2021-10-10 10:10:10",

}
</script>

<template>
    <PostItem :post="post1"
    />
</template>

<style scoped>

</style>
