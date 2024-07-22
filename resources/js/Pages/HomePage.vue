<script setup>
import {Head, Link} from '@inertiajs/vue3';
import GroupList from "@/component/HomePage/GroupList.vue";
import AuthenticatedLayout from "@/Layouts/AuthenticatedLayout.vue";
import GroupItem from "@/component/HomePage/GroupItem.vue";
import TextInput from "@/Components/TextInput.vue";
import FollowList from "@/component/HomePage/FollowList.vue";
import CreatePost from "@/component/HomePage/CreatePost.vue";
import PostList from "@/component/HomePage/PostList.vue";
</script>

<template>
    <AuthenticatedLayout>
    <Head title="HomePage"/>
        <div class="px-3">
    <div class="grid grid-cols-12 gap-4">
        <div class="sm:col-span-3  p-6">
           <h2 class="lg:text-[30px] sm:text-[20px] font-bold pb-5">My Groups</h2>
            <text-input :model-value="search" placeholder="Search group"></text-input>
            <div v-if="false" >
                  <p class="pt-5 text-[20px]"> You are not join any group</p>
            </div>
            <div v-else >
                <GroupList/>
            </div>
        </div>
        <div class="lg:col-span-6">
            <CreatePost/>
            <PostList/>
        </div>
        <div class="lg:col-span-3 p-6">
            <h2 class="lg:text-[30px] sm:text-[20px] font-bold pb-5">My Follows</h2>
            <text-input :model-value="search" placeholder="Search group"></text-input>
                <FollowList/>
        </div>
    </div>
        </div>
    </AuthenticatedLayout>
</template>
