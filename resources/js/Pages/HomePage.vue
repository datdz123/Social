<script setup>
import {Head, Link} from '@inertiajs/vue3';
import GroupList from "@/component/HomePage/GroupList.vue";
</script>

<template>
    <Head title="HomePage"/>
    <div class="grid grid-cols-12 gap-4">
        <div class="sm:col-span-3  p-6">
           <h2 class="text-[30px] font-bold pb-10">My Groups</h2>
            <div v-if="false" >
                  <p class="pt-5 text-[20px]"> You are not join any group</p>
            </div>
            <div v-else>
          <GroupList
              image="/image/avatar1.jpg"
              Title="Tiêu đề 1"
              Description="Lorem ipsum dolor sit amet consectetur adipiscing elit ad at risus,
               facilisis fermentum "
              ></GroupList>

                <GroupList
                    image="/image/avatar1.jpg"
                    Title="Tiêu đề 2"
                    Description="Lorem ipsum dolor sit amet consectetur adipiscing elit ad at risus,
                      facilisis fermentum"
                ></GroupList>
            </div>
        </div>
        <div class="lg:col-span-6">
            Posts
        </div>
        <div class="lg:col-span-3">
            Follows
        </div>
    </div>

</template>
