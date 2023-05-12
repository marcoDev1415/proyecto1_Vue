<template>
   <h1>Counter</h1>
   <p>{{ counter }} <sup>2</sup> = {{ counter * counter }} </p>

   <p>{{ counter }} <sup>2</sup> = {{squareCounter}} </p>
   <p>{{ counter }} <sup>2</sup> = {{squareCounter}} </p>

   <p>{{ counter }} <sup>2</sup> = {{squareCounter}} </p>

   <p>{{ counter }} <sup>2</sup> = {{squareCounter}} </p>

   <p>{{ counter }} <sup>2</sup> = {{squareCounter}} </p>

   <p>{{ counter }} <sup>2</sup> = {{getValue()}} </p>
   
   <p>{{ counter }} <sup>2</sup> = {{getValue()}} </p>
  
   
   <p>{{ counter }} <sup>2</sup> = {{getValue()}} </p>
  
  
</template>
<script>
  export default{
    //name: 'counter
    data(){
      return{
        counter: 5

      }
    },
    methods:{
      getValue(){
        console.log('getValue');
        return this.counter * this.counter;
      }
    },
    computed:{
      squareCounter(){
        console.log('squareCounter')
        return this.counter * this.counter
      }
    }
  }
</script>
<style>
</style>