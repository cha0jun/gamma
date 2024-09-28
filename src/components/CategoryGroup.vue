<script setup lang="ts">
import ref from 'vue';
import { ToggleGroup, ToggleGroupItem } from '@/components/ui/toggle-group'
import { Card } from '@/components/ui/card'
import defineProps from 'vue';

const props = defineProps({
    catItems: {
        type: Array,
        required: true,
    },
});

const emit = defineEmits(['categorySelected']);

const onPressed = (id) => {

emit('categorySelected', id);
};

</script>
<template>
        <ToggleGroup type="multiple" variant="outline" size="lg">
                <ToggleGroupItem 
                    v-for="cat in catItems" 
                    :key="cat.id" 
                    :value="cat.name" 
                    @click="onPressed(cat.id)">
                        {{ cat.name }}
                    </ToggleGroupItem>
        </ToggleGroup>
</template>