<template>
    <div class="box_all">
    <div class="col" v-for="(n,i) in travelList" :key="n">
      <div class="card" style="width: 25rem;" >
        <img :src="n.img" class="card-img-top">
        <div class="card-body">
          <h3 class="card-title">{{ n.name }}</h3>
          <p>BookingPrice : {{n.price}}</p>
          <h6>Open: Everyday 12.00-22.00</h6>

          <a class="btn btn-primary" @click="list_local_control(i.name, i.quantity)"> Booking </a>
        </div>
      </div>
    </div>
  </div>

</template>

<script setup>

import { ref } from 'vue';

const travelList=ref([
    {name:'Kanom mae',  price:30, img:"https://www.chiangmainews.co.th/wp-content/uploads/2022/09/29/2748665/1664423059_641434-chiangmainews.jpg", quantity: 0 ,
    text_box:' Location: 185/5 Sahakorn road Nonghan Sansai Chiangmai.'}])

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