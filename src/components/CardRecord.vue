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
    Details: Array,
    ImgUrl: String
 })
</script>
<template>
    <Card class="flex p-5">
        <img v-bind:src="ImgUrl" class="rounded-xl cc-small mr-10">
        <div class="grid grid-cols-1 gap-2.5">
            <CardTitle>{{ Name }}</CardTitle>
            <CardDescription>{{ Provider }}</CardDescription>
            <p>{{ Details }}</p>
        </div>
    </Card>
</template>