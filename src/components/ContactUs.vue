<template>
  <div class="container lg:px-10 px-5 mx-auto text-center md:text-start mb-10">
    <h1 class="uppercase text-red-900 text-2xl font-extrabold mb-2"><span class="text-red-400">Jion Now</span> To get in shap</h1>
    <p class="text-pink-800 md:w-3/4 w-full md:mx-0 mx-auto">Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum cumque fugiat similique aspernatur inventore perspiciatis expedita optio, eveniet hic ut necessitatibus nisi venia.</p>
    <div class="flex md:justify-between flex-col md:flex-row mt-10 gap-10">
      <form action="" class="flex flex-col gap-3 flex-1">
        <input type="text" placeholder="Name" class="inputbtn">
        <input type="email" placeholder="Email" class="inputbtn">
        <textarea  placeholder="Massage" class="inputbtn" rows="5"></textarea>
        <button type="submit" class="uppercase btn w-fit mt-5 md:mx-0 mx-auto">Submite</button>
      </form>
      <div class="giveasudo">
        <img src="../assets/ContactUsPageGraphic.png" class="w-full" alt="">
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">

</script>

<style scoped>
.giveasudo{
  position: relative;
}
.giveasudo::after{
  content: "EVOGYM";
  position: absolute;
  bottom:0;
  left:50%;
  font-size:65px;
  font-weight: 800;
  transform: translate(-50%,50%) scale(1.5);
  color:gray;
  opacity: 0.4;
  z-index: -1;
}
@media (max-width:767px) {
  .giveasudo::after{
    font-size:85px;
  }
}
@media (max-width:550px) {
  .giveasudo::after{
    font-size:50px;
  }
}
</style>