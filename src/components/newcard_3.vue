<template>
    <div class="box_all">
    <div class="col" v-for="(n,i) in travelList" :key="n">
      <div class="card" style="width: 25rem;" >
        <img :src="n.img" class="card-img-top">
        <div class="card-body">
          <h3 class="card-title">{{ n.name }}</h3>
          <p>BookingPrice : {{n.price}}</p>
          <h6>Open: Everyday 8.00-18.00 </h6>

          <a class="btn btn-primary" @click="list_local_control(i.name, i.quantity)"> Booking </a>
        </div>
      </div>
    </div>
  </div>

</template>

<script setup>

import { ref } from 'vue';

const travelList=ref([
    {name:'Soul Cafe mju', price:40, img:"https://www.chiangmainews.co.th/wp-content/uploads/2022/09/29/2748665/1664423515_957631-chiangmainews.jpg", quantity: 0 ,
        text_box:'Location: 280 Nonghan Sansai Chiangmai.'   
    },])


</script>

<style>

.card-img-top{
height: 100%;
padding: 25px;

}
.box_all{
justify-content: center;
align-items: center;
margin-left: 30%;
text-align: center
}

</style>