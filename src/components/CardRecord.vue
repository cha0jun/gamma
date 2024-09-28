<script setup lang="ts">
import { ref } from 'vue';
import {
    Card,
    CardTitle,
    CardDescription,
 } from './ui/card';

 defineProps({
    Name: String,
    Provider: String,
    Details: {
        type: Array,
        required: true
    },
    ImgUrl: String
 })
</script>
<template>
    <Card class="flex p-5 rounded-2xl items-center">
        <img v-bind:src="ImgUrl" class="rounded-xl cc-small mr-10">
        <div class="grid grid-cols-1 gap-1">
            <CardTitle>{{ Name }}</CardTitle>
            <CardDescription>{{ Provider }}</CardDescription>
                <li v-for="detail in Details" 
                    :key="detail.id"
                    >{{ detail }}</li>
        </div>
    </Card>
</template>