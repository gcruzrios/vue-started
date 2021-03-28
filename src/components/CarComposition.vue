<template>
  <h2>Coche negro Composition API</h2>
  <p> Marca: {{ brand }}</p>
  <p> Modelo: {{ model }}</p>
  <p> Color: 
    <span v-for="(color, index) in colors" :key="index" >
      {{ index }}:{{ color }} - 
    </span>
  </p>
  <p> Power: {{ power }}</p>
  <button @click="upPower(100)">Aumentar</button>
  <button @click="downPower(100)">Disminuir</button>
  <!-- <ul>
    <li v-for="(color, index) in colors" :key="index">
      {{ index }}:{{ color }} -
    </li>
  </ul>
  <p>Potencias Urbanas: menor de 300 CV</p>
  <ul>
     <template v-for="(power, index) in powers" :key="index">
          <li v-if = "power < 240 ">
             Urbana: {{power}}
          </li>
          <li v-else-if = "power ===240" >Hibrido {{ power }}</li>
          <li v-else >
             Carrera: {{power}}
          </li>
          <li v-if = "power === 600 ">
             Super: {{power}}
          </li>
      </template>
  </ul>

  <p>Potencias Pista: mayor de 300 CV</p>
  <ul>
     <template v-for="(power, index) in powers" :key="index">
          <li v-if = "power > 299 ">
              {{power}}
          </li>
          
      </template>
  </ul> -->

  <p> Precio: $ {{ price }}</p>
  
  {{mensaje.title}} {{mensaje.text}}
</template>

<script>

import { ref } from "vue";

export default {
    
    //Composition API
    setup(){
      const brand= "Audi";
      const model= "A4";
      const colors=["Azul", "Rojo", "Verde", "Amarillo"];
      const price=45000;
      let power =ref(40);
      const powers= [60, 80, 120, 160, 200, 240, 300, 390, 540, 600];

      const mensaje = {
            title:"Hola Mundo",
           text:"adios"
         }
      
      const upPower = (newPower) => {
        console.log("aumentando potencia");
        //console.log(power.value);
        power.value= power.value+newPower;
      }
      const downPower = () => {
        console.log("bajando potencia")
        power.value= power.value-newPower;
     }
      
      return { brand, model, colors, price, power, powers, mensaje, upPower, downPower }
    }
}
</script>

<style>

</style>