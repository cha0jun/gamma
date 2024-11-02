<script setup lang="ts">
import { ToggleGroup, ToggleGroupItem } from '@/components/ui/toggle-group'
import { defineProps } from 'vue';

interface CategoryItem {
        id?: number
        name?: string
        isActive?: boolean
}

interface CategoryGroupProps {
    catItems?: CategoryItem[]
}

const props = defineProps<CategoryGroupProps>();

const emit = defineEmits(['category-selected']);

const onPressed = (id?:number) => {

emit('category-selected', id);
};

</script>
<template>
        <ToggleGroup type="multiple" variant="outline" size="lg" class="initial flex-wrap grow gap-4">
                <ToggleGroupItem 
                    v-for="cat in props.catItems" 
                    :key="cat.id" 
                    :value="cat.name??''" 
                    @click="onPressed(cat.id)">
                        {{ cat.name }}
                    </ToggleGroupItem>
        </ToggleGroup>
</template>