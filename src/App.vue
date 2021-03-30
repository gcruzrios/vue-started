<template>
  <h1>Vue JS</h1>
  <Car :power="power" :upPower="upPower" @downPower="downPower"/>
  
  
</template>

<script>
import {ref} from "vue"
import Car from "./components/Car";
//import CarO from "./components/CarOptions";

export default {
  components:{
    Car
  },
  setup(){
    let power= ref(30);


    const upPower = (newPower) => {
        //console.log("aumentando potencia");
        power.value++;
        //console.log(power.value);
        //power.value= power.value+newPower;
    };
    const downPower = (newPower) => {
        //console.log("bajando potencia")
        power.value--;
     };
  return{
    power, upPower, downPower
  };
 }
}
</script>

<style>

</style>
