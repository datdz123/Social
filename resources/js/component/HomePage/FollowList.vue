
<script>

import {defineComponent} from "vue";
import GroupItem from "@/component/HomePage/GroupItem.vue";
import FollowItem from "@/component/HomePage/FollowItem.vue";

export default defineComponent({
    components: {FollowItem, GroupItem}
})
</script>
<template>
    <FollowItem
        image="/image/avatar1.jpg"
        Title="Tiêu đề 1"

    ></FollowItem>

    <FollowItem
        image="/image/avatar1.jpg"
        Title="Tiêu đề 2"
    ></FollowItem>
</template>
<style scoped>

</style>
