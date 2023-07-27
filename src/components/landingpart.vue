<template>
  <div class="container lg:px-10 mx-auto lg:pt-20 pt-28 flex items-center md:flex-row flex-col justify-center text-center md:text-start pb-10">
    <div class="maintext">
      <h1 class="giveasudo text-6xl font-bold text-red-900">EVOGYM</h1>
      <h3 class="text-2xl text-gray-800 mb-5 opacity-40">evolutionary fitness</h3>
      <p class="w-3/4 mb-5 mx-auto md:mx-0 text-pink-800">Lorem ipsum dolor sit amet consectetur adipisicing elit. Dignissimos expedita voluptatum neque minus odit?</p>
      <div class="flex gap-5 items-center justify-center md:justify-start">
        <a href="#" class="btn">Jion Now</a>
        <a href="#" class="underline text-red-500">Learn More</a>
      </div>
    </div>
    <div class="heroimg md:w-96">
      <img src="../assets/HomePageGraphic.png" class="w-full">
    </div>
  </div>
</template>

<script lang="ts">
  export default {
    
  }
</script>

<style scoped>
.giveasudo{
  position: relative;
  font-weight: 800;
}
.giveasudo::after{
  content: "EVOGYM";
  position: absolute;
  top:0;
  left:0;
  font-size:60px;
  transform: translate(10%,-75%) scale(1.5);
  color:gray;
  opacity: 0.4;
}
@media (max-width:1023px) {
  .giveasudo::after{
    display: none;
  }
}
</style>