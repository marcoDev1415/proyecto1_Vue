<template>
   <h1>{{changeValor}}</h1>
   <p>{{ counter + start }} <sup>2</sup> = {{ counter * counter }} </p>
 
   <p> Valor original {{ acum }} = {{ counter }} </p>
    
   <div>
     <div>
      <button class="myButton" @click = "increment()" >Sumar</button>
     </div>
     <div class="marginTop">
      <button class="myButton2" v-on:click = "decremente()" >Restar</button>
     </div>
   </div>
</template>
<script>

  export default{

    props: {
      title: String,
      start: {
        type : Number ,
        default : 100
        //required: true
      } 
    },
    //name: 'counter
    data(){
      return{
        counter: 5,
        acum:0

      }
    },
    methods:{
      getValue(){
        console.log('getValue');
        return this.counter * this.counter;
      },
      increment(){
        this.acum = this.counter;
        return this.counter = this.counter + 1;
      },
      decremente(){
        this.acum = this.counter;
        return this.counter = this.counter - 1;
      }
      
    },
    computed:{
      squareCounter(){
        console.log('squareCounter')
        return this.counter * this.counter;
      },
      changeValor(){
           if (this.title !== undefined){
            return this.title
           }else{
            return 'counter'
           }
          return this.title
      }
     
    }
  }
</script>
<style>

.myButton {
	background-color:#44c767;
	border-radius:28px;
	border:1px solid #18ab29;
	display:inline-block;
	cursor:pointer;
	color:#ffffff;
	font-family:Arial;
	font-size:17px;
	padding:16px 31px;
	text-decoration:none;
	text-shadow:0px 1px 0px #2f6627;
}


.myButton2 {
	background-color:#449dc7;
	border-radius:28px;
	border:1px solid #449dc7;
	display:inline-block;
	cursor:pointer;
	color:#ffffff;
	font-family:Arial;
	font-size:17px;
	padding:16px 31px;
	text-decoration:none;
	text-shadow:0px 1px 0px #2f6627;
}
.myButton:hover {
	background-color:#5cbf2a;
}
.myButton:active {
	position:relative;
	top:1px;
}


.marginTop{

  margin-top: 1%;
}

.myButton2:hover {
	background-color:#5cbf2a;
}
.myButton2:active {
	position:relative;
	top:1px;
}

        
</style>