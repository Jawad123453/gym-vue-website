<template>
     <div class="fixed w-full z-50" :class="startscoll?'bg-pink-200':'bg-transparent'">
        <div class="container flex justify-between items-center mx-auto gap-10 lg:px-10 px-5 py-5">
        <div>
            <img src="../assets/Logo.png" alt="">
        </div>
        <div class="flex justify-between items-center flex-1">
            <div class="w-full flex justify-end md:hidden cursor-pointer" @click="showthebar">
                <i class="fa-solid fa-bars text-white rounded-3xl bg-orange-400 w-8 h-8 flex justify-center items-center md:hidden"></i>
            </div>
            <ul class="mainul md:flex md:gap-3 md:items-center hidden" :class="barstate==true?'makingitapper':''">
                <div class="realwidth md:hidden block text-end">
                    <i class="fa-solid fa-xmark text-xl  cursor-pointer" @click="showthebar"></i>
                </div>
                <li v-for="(list,index) in liststring" :key="index"><a :href="list.mainalink" class="cursor-pointer text-black hover:text-red-500" @click="handtheclick(index)" :class="{ 'activebtn': selectedIndex === index }">{{ list.namelist }}</a></li>
            </ul>
            <ul class="md:flex gap-3 items-center hidden">
                <li class="cursor-pointer text-black hover:text-red-500">Sign In</li>
                <li class="btn">Become a Member</li>
            </ul>
        </div>
        
     </div>
    </div>
</template>

<script lang="ts">
import { ref } from 'vue'
    export default{
        data() {
            return {
                barstate:false,
                selectedIndex: 0,
                liststring:[
                    {namelist:"Home",mainalink:"#"},
                    {namelist:"Benifits",mainalink:"#Benifits"},
                    {namelist:"Our Classes",mainalink:"#Our-Classes"},
                    {namelist:"Contact Us",mainalink:"#Contact-Us"}
                ]
            }
        },
        methods: {
            handtheclick(index:number){
                this.selectedIndex = index;
            },
            showthebar(){
                return this.barstate = !this.barstate
            },
        },
        setup(){
            const startscoll=ref(false);
            const selectedIndex=ref(0)

            window.addEventListener("scroll",function(){
                if(this.window.scrollY === 0){
                    return startscoll.value=false
                }else{
                    return startscoll.value=true
                }
            })

            window.addEventListener("scroll",function(){
                if(this.window.scrollY > 600 && this.window.scrollY < 1450){
                    selectedIndex.value = 1
                }
                else if(this.window.scrollY > 1450 && this.window.scrollY < 1923){
                    selectedIndex.value = 2
                }
                else if(this.window.scrollY > 1923){
                    selectedIndex.value = 3
                }
                else if(this.window.scrollY >= 0 && this.window.scrollY < 600){
                    return selectedIndex.value = 0
                }
            })

            return {startscoll ,selectedIndex}
        }
    }
</script>

<style scoped>
.makingitapper{
    background-color: pink;
    width:300px;
    height:100vh;
    position: absolute;
    top:0;
    right:0;
    display: flex;
    flex-direction: column;
    gap:30px;
    align-items: center;
}
.realwidth{
    width:calc(100% - 50px);
    margin: 40px 10px 0;
}
.activebtn{
    color:rgb(239 68 68);
}
</style>