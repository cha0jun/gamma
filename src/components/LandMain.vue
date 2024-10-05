<script setup lang="ts">
import {
  Card
} from '@/components/ui/card'

import CardRecord from '@/components/CardRecord.vue'
import CategoryGroup from '@/components/CategoryGroup.vue'
import { ref } from 'vue';


const catItems = ref([
    { id: 0, name: 'Local General Spending', isActive: false },
    { id: 1, name: 'Shopping', isActive: false },
    { id: 2, name: 'Foreign Currency Spending', isActive: false },
    { id: 3, name: 'Dining', isActive: false },
    { id: 4, name: 'Paywave/Mobile', isActive: false },
    { id: 5, name: 'Utilities', isActive: false }
  ]);

// filter selected spend category
const filterSelectedCat = (id:number) =>{
  console.log(id);
  
}
</script>

<template>
  <div class="flex flex-col gap-7">
    <div id="ccCompare">
      <CategoryGroup :catItems="catItems" @categorySelected="filterSelectedCat"></CategoryGroup> 
    </div> 
    <div id="ccList" class="">
      <Card class="p-10 rounded-2xl">
          <CardRecord 
            name = "Simply Cash"
            provider = "Standard Chartered"
            :details = "['Receive S$30 Caltex vouchers', '6 x S$5 off each fuel purchase', 'Convert your transactions into interest-free instalments with EasyPay', 'Exciting shopping and lifestyle benefits with The GoodLife']"
            imgurl = "https://av.sc.com/sg/content/images/sg-simply-cash-cards-webpage-360-X-360-AT.png">

          </CardRecord>
      </Card>
    </div>
 </div>
</template>