<template>
  <h1>Vue JS</h1>
  <CarO/>
  <CarC/>
  
  
</template>

<script>
import CarC from "./components/CarComposition";
import CarO from "./components/CarOptions";

export default {
  components:{
    CarC, CarO
  }
}
</script>

<style>

</style>
