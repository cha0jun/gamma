<script setup lang="ts">
import {
    Card,
    CardTitle,
    CardDescription,
 } from './ui/card';

 interface CardDetails {
    name?: string
    provider?: string
    details?: string[]
    imgurl?: string
 }
 
const props = defineProps<CardDetails>();

</script>
<template>
    <Card class="flex p-5 rounded-2xl items-center">
        <img v-bind:src="props.imgurl" class="rounded-xl cc-small mr-10">
        <div class="grid grid-cols-1 gap-1">
            <CardTitle>{{ props.name }}</CardTitle>
            <CardDescription>{{ props.provider }}</CardDescription>
                <li v-for="detail in props.details">{{ detail }}</li>
        </div>
    </Card>
</template>