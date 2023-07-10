<script setup>
import {ref} from 'vue';
import Tabs from '@/components/Tabs.vue';

const tabs = [
    {name: 'About', label: 'О проекте'},
    {name: 'Vue', label: 'Про Vue'},
    {name: 'React', label: 'Про React'}
]

const selectedTab = ref('Vue')

const changeTab = (tabName) => {
    selectedTab.value = tabName
}

</script>

<template>
    <h1 class="heading-1">Tabs</h1>
    <Tabs
        :names="tabs"
        :selectedTab ="selectedTab"
        @changeTab="changeTab"
    >
    <div v-if="selectedTab === 'About'">Lorem, ipsum dolor sit amet consectetur adipisicing elit. </div>
    <div v-if="selectedTab === 'Vue'">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eum ex, sequi impedit rem laborum accusamus nostrum! </div>
    <div v-if="selectedTab === 'React'">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Assumenda possimus nemo fugiat quo perspiciatis ipsam, excepturi, facere dolorum asperiores voluptas eveniet, eum dignissimos natus vero? Assumenda facere aliquam tempore reprehenderit.</div>

    </Tabs>
</template>