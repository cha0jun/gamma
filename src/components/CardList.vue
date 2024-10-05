<script setup lang="ts">
import {
    Card,
    CardTitle,
    CardDescription,
 } from './ui/card';


 interface CardDetails {
    id?: number
    name?: string
    provider?: string
    details?: string[]
    imgurl?: string
 }

 interface CardItems {
    cardItems?: CardDetails[]
 }
 
const props = defineProps<CardItems>();

</script>
<template>
        <Card id="ccList" class="p-10 rounded-2xl flex flex-col gap-7">
            <Card id="ccRecord" class="flex p-5 rounded-2xl items-center"
            v-for="card in props.cardItems"
            :key="card.id">
                <img v-bind:src="card.imgurl" class="rounded-xl cc-small mr-10">
                <div class="grid grid-cols-1 gap-1">
                    <CardTitle>{{ card.name }}</CardTitle>
                    <CardDescription>{{ card.provider }}</CardDescription>
                    <li v-for="detail in card.details">{{ detail }}</li>
                </div>
            </Card>
        </Card>
</template>