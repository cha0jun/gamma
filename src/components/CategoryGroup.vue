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

const emit = defineEmits(['categorySelected']);

const onPressed = (id?:number) => {

emit('categorySelected', id);
};

</script>
<template>
        <ToggleGroup type="multiple" variant="outline" size="lg">
                <ToggleGroupItem 
                    v-for="cat in props.catItems" 
                    :key="cat.id" 
                    :value="cat.name??''" 
                    @click="onPressed(cat.id)">
                        {{ cat.name }}
                    </ToggleGroupItem>
        </ToggleGroup>
</template>