<template>
   <div>
      <h1>Конвертер з гривні в долари</h1>
      <label>
         Гривні:
      <input type="number" v-model="num1">
      </label><br>
      <label>
         Долари:
      <input type="number" v-model="num2">    Долари тільки виводяться, тому достатньо односторонньої при"вязки даних
      </label><br>
      <button @click="convert">
         Перевести!
      </button>
   </div>
</template>

<script>
   export default {
      name:'converter',
      data(){
         return {
            num1:0,
            num2:0
         }
      },
      methods:{
         convert(){
            this.num2=this.num1/27.3            
         }
      }
      
   }
</script>

<style lang="css">
h1 {
   color: blue;   
}
button {
   background-color: cadetblue;
}
</style>
