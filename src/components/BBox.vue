<template>
  <div class="p-8 w-full flex flex-col text-center border border-gray-500 rounded gap-3">
    <div class="bg-pink-200 rounded-full flex justify-center items-center w-14 h-14 mx-auto">
      <i :class="boxarray.smallicon" class="text-xl text-red-900"></i>
    </div>    
    <h4 class="text-red-900 font-semibold">{{ boxarray.h4text }}</h4>
    <p class="text-pink-800">{{boxarray.ptext}}</p>
    <a :href="boxarray.alink" class="underline text-red-500">Learn More</a>
  </div>
</template>

<script lang="ts">
  export default {
    props:["boxarray"]
  }
</script>

<style lang="scss" scoped>

</style>