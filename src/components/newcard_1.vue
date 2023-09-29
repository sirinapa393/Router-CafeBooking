<template>
    <div class="box_all">
    <div class="col" v-for="(n,i) in travelList" :key="n">
      <div class="card" style="width: 25rem;" >
        <img :src="n.img" class="card-img-top">
        <div class="card-body">
          <h3 class="card-title">{{ n.name }}</h3>
          <p>BookingPrice : {{n.price}}</p>
          <h6>Open: Mom-Fri 8.00-18.00 Sat-Sun 9.00-17.00</h6>
          

          <a class="btn btn-primary" @click="list_local_control(i.name, i.quantity)"> Booking </a>
        </div>
      </div>
    </div>
  </div>

</template>

<script setup>

import { ref } from 'vue';

const travelList=ref([
    {name: 'Tree&Co',  price:50, img:"https://www.chiangmainews.co.th/wp-content/uploads/2022/09/29/2748665/1664422853_404447-chiangmainews.jpg", quantity: 0 ,
        text_box:' Location: Maejo University Business Faculty.'
    }])


</script>

<style>

.card-img-top{
height: 100%;
padding: 25px;
border-radius: 60px;


}
.box_all{
justify-content: center;
align-items: center;
margin-left: 30%;
text-align: center;
border-radius: 60px;

}
.btn.btn-primary{
background-color: rgb(0, 0, 0);
}

</style>