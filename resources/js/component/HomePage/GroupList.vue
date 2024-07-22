
<script>

import {defineComponent} from "vue";
import GroupItem from "@/component/HomePage/GroupItem.vue";

export default defineComponent({
    components: {GroupItem}
})
</script>
<template>
    <GroupItem
        image="/image/avatar1.jpg"
        Title="Tiêu đề 1"
        Description="Lorem ipsum dolor sit amet consectetur adipiscing elit ad at risus,
               facilisis fermentum "
    ></GroupItem>

    <GroupItem
        image="/image/avatar1.jpg"
        Title="Tiêu đề 2"
        Description="Lorem ipsum dolor sit amet consectetur adipiscing elit ad at risus,
                      facilisis fermentum"
    ></GroupItem>
</template>
<style scoped>

</style>
