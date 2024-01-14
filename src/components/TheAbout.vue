<script setup lang="ts">
import AboutItem from './AboutItem.vue';
import { useCounterStore } from '@/stores/counter';

const counter = useCounterStore();
// counter.increment()
defineProps<{
    desc: string
}>()
</script>
<template>
    <div>
        <AboutItem>
            <template #icon> <button @click="counter.increment">{{ counter.count }}</button> </template>
            <template #heading> This is the about page </template>
            <p>
                {{ desc }}
            </p>
        </AboutItem>
        <AboutItem>
            <template #icon> World </template>
            <template #heading> I am learning </template>
            <p>
                Yay!
            </p>
        </AboutItem>
    </div>
</template>
<style scoped lang="scss">
</style>