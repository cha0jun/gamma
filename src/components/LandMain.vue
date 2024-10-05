<script setup lang="ts">

import CardList from '@/components/CardList.vue'
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


const cardItems = ref([
  {id:0, 
    name: "Simply Cash", 
    provider: "Standard Chartered",
    details:['Receive S$30 Caltex vouchers', '6 x S$5 off each fuel purchase', 'Convert your transactions into interest-free instalments with EasyPay', 'Exciting shopping and lifestyle benefits with The GoodLife'], 
    imgurl:"https://av.sc.com/sg/content/images/sg-simply-cash-cards-webpage-360-X-360-AT.png"},

{id:1,
  name: "Citi Cash Back+ Card", 
  provider: "Citibank", 
  details: ['1.6% cash back on your eligible spend all year round', 'No minimum spend required and no cap on cash back earned', 'Cash back earned does not expire', 'Redeem your cash back instantly on-the go', 'Earn 0.4% Bonus Cash Back on your eligible spend if you are a Citi Plus customer who is the Primary Account Holder of a Citi Interest Booster Account'], 
  imgurl:"https://photos.cdn-moneysmart.com/credit_cards/uploads/products/images/image_url_2021-09-29_Details%20-%20Logo%20-%20Citi%20Cashback%20Plus.png"}]);


// filter selected spend category
const filterSelectedCat = (id:number) =>{
  console.log(id);
  
}
</script>

<template>
  <div class="flex flex-col gap-7">
      <CategoryGroup :catItems="catItems" @categorySelected="filterSelectedCat">       
      </CategoryGroup> 
      <CardList v-bind:card-items="cardItems"></CardList>
 </div>
</template>