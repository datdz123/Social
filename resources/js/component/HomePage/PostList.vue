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
    images:[
        {
        url:"https://cdn.cloudflare.steamstatic.com/steamcommunity/public/images/avatars/b6/b6bd805df958f963b383d8733e8cda2f474176c1_full.jpg",
        },
        {
        url:"https://cdn.cloudflare.steamstatic.com/steamcommunity/public/images/avatars/68/68b306f2a0c18481f357efa5055977a3d472c616_full.jpg",
        },
        {
        url:"https://cdn.cloudflare.steamstatic.com/steamcommunity/public/images/avatars/68/68ec5646825cd6c5d20ed7820026b3f247ea5121_full.jpg",
        },
            ]


}
</script>

<template>
    <PostItem :post="post1"
    />
</template>

<style scoped>

</style>
