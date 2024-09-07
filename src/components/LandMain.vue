<script setup lang="ts">
import {
  Card
} from '@/components/ui/card'

import CardRecord from '@/components/CardRecord.vue'
</script>

<template>
    <Card class="p-10">
        <CardRecord 
        Name = "Simply Cash"
        Provider = "Standard Chartered"
        :Details = "['Receive S$30 Caltex vouchers, 6 x S$5 off each fuel purchase Convert your transactions into interest-free instalments with EasyPay Exciting shopping and lifestyle benefits with The GoodLife']"
        ImgUrl = "https://av.sc.com/sg/content/images/sg-simply-cash-cards-webpage-360-X-360-AT.png">

        </CardRecord>
    </Card>
  </template>