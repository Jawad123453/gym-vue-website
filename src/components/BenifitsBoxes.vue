<template>
  <div class="grid xl:grid-cols-3 md:grid-cols-2 gap-3">
    <div v-for="box in boxarray">
      <BBox :boxarray="box"/>
    </div>
  </div>
</template>

<script lang="ts">
import BBox from './BBox.vue';
export default{
  components:{BBox},
  data() {
    return {
      boxarray:[
        {smallicon:"fa-solid fa-house-medical-circle-check",h4text:"State of art and fuction",ptext:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas quos reiciendis",alink:"#"},
        {smallicon:"fa-solid fa-people-group",h4text:"State of art and fuction",ptext:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas quos reiciendis",alink:"#"},
        {smallicon:"fa-solid fa-graduation-cap",h4text:"State of art and fuction",ptext:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas quos reiciendis",alink:"#"}
      ]
    }
  },
}
</script>

<style lang="scss" scoped>

</style>