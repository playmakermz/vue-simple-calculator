<script setup>
import { ref } from 'vue'

const myForm = ref() // Ini adalh stance 

function mySys(nilai){
  try {
    let abc = parseInt(myForm.value)
    myForm.value += nilai 
  } catch (e) {
    myForm.value = ''
  }
 
}

function myClear(){
  myForm.value = ''
}

function Calculate(){
  try {
    myForm.value = eval(myForm.value)
  } catch (e) {
    myForm.value = 'Error'
  }
}


</script>

<template>
 
 <div class="calculator">
   <form @submit.prevent="">
    <input v-model="myForm" required placeholder="0">
    <div class="buttons">
      <button @click="mySys('7')">7</button>
      <button @click="mySys('8')">8</button>
      <button @click="mySys('9')">9</button>
      <button @click="mySys('/')">/</button>
      <button @click="mySys('4')">4</button>
      <button @click="mySys('5')">5</button>
      <button @click="mySys('6')">6</button>
      <button @click="mySys('*')">*</button>
      <button @click="mySys('1')">1</button>
      <button @click="mySys('2')">2</button>
      <button @click="mySys('3')">3</button>
      <button @click="mySys('-')">-</button>
      <button @click="mySys('0')">0</button>
      <button @click="mySys('.')">.</button>
      <button @click="Calculate()">=</button>
      <button @click="mySys('+')">+</button>

      <button @click="myClear()">Clear</button>
      <button @click="mySys('.')">Delete</button>

    </div>
   </form>
  </div>

</template>

<style scoped>
 .calculator {
            width: 200px;
            background-color: #f0f0f0;
            padding: 10px;
        }

        #display {
            width: 100%;
            padding: 5px;
            font-size: 20px;
            text-align: right;
            margin-bottom: 10px;
            background-color: #fff;
            border: 1px solid #ccc;
        }

        .buttons {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            grid-gap: 5px;
        }

        button {
            padding: 10px;
            font-size: 18px;
            background-color: #fff;
            border: 1px solid #ccc;
        }

        button:hover {
            background-color: #eee;
        }
</style>
