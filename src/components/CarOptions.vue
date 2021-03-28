<template>
  <h2>Coche negro Options API</h2>
  <p> Marca: {{ brand }}</p>
  <p> Modelo: {{ model }}</p>
  
  <p> Precio: $ {{ price }}</p>
  <p> Potencia: {{ power }} CV</p>
  
  <button @click="upPower(100)">Aumentar</button>
  <button @click="downPower(100)">Disminuir</button>
</template>

<script>


export default {
  
   ///Composition API
    data(){
      return{
        brand: "Seat",
        model:"Leon",
        color:["Azul", "Rojo", "Verde"],
        price:23000,
        power: 60,
        mensaje:{
          title:"Hola Mundo",
          text:"adios"
        }
      };
    },
    methods:{
      upPower(newPower){
        //console.log("aumentando potencia ->" + newPower);
        this.power = this.power+newPower;
        //this.power++;
      },
      downPower(newPower){
        //console.log("bajando potencia ->" + newPower)
        this.power = this.power-newPower;
        //this.power--;  
     }
    }
}
</script>

<style>

</style>