<template>
   <div>
      <label>
         Cathetus1
         <input type="text" v-model="cathetus1">
      </label> <br>
      <label>
         Cathetus2
         <input type="text" v-model="cathetus2">
      </label><br>
      <button @click="getHypotenuse">
         Calculate!
      </button> <br>
      <label>
         Hypotenuse
         <input type="text" v-model="resHyp">     Ви тільки виводите гіпотенузу, тому достаньо односторонньої привязки даних <input type="text" :value="resHyp"> 
      </label>
   </div>
</template>

<script>
   export default {
      name:'MyCalc',
      data(){
        return {
           cathetus1:0,
           cathetus2:0,
           resHyp:0,
        } 
      },
      methods:{
         getHypotenuse(){
            this.resHyp=Math.sqrt(Math.pow(parseFloat(this.cathetus1),2)+Math.pow(parseFloat(this.cathetus2),2))
         }
      }
      
   }
</script>

<style lang="scss" scoped>

</style>
