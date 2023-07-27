<script setup lang="ts">
  import Header from "./components/Header.vue"
  import LandingPart from "./components/landingpart.vue"
  import LandingComapnyIcons from "./components/Landingcompanyicons.vue"

  import Benifits from "./components/Benifits.vue"
  import Benifitsflex from "./components/Benifitsflex.vue"

  import OurClass from "./components/OurClass.vue"
  import OurclassSideScollerVue from "./components/OurclassSideScoller.vue"

  import ContactUsVue from "./components/ContactUs.vue"

  import Footer from "./components/Footer.vue"
</script>

<template>
  <div>
    <div class="min-h-screen bg-pink-100 justify-between flex-col flex">
    <Header />
    <LandingPart />
    <LandingComapnyIcons />
    </div>  
    <div class="p-10" id="Benifits">
      <Benifits />
      <Benifitsflex />
    </div>
    <div class="bg-pink-300 py-10" id="Our-Classes">
      <OurClass />
      <OurclassSideScollerVue />
    </div>
    <div class="py-10" id="Contact-Us">
      <ContactUsVue />
    </div>
    <div class="bg-pink-300">
      <Footer />
    </div>
  </div>
</template>

<style>
*{
  padding:0;
  margin:0;
  box-sizing: border-box;
}
body{
  font-family: 'Roboto', sans-serif;
}
html{
  scroll-behavior: smooth;
}
</style>
