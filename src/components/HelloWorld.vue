<script setup>
import { ref } from 'vue'

defineProps({
  msg: String,
})

const count = ref(0)
</script>

<template>
 
 <div class="calculator">
        <input type="text" id="display" readonly>
        <div class="buttons">
            <button data-value="7">7</button>
            <button data-value="8">8</button>
            <button data-value="9">9</button>
            <button data-value="/">/</button>
            <button data-value="4">4</button>
            <button data-value="5">5</button>
            <button data-value="6">6</button>
            <button data-value="*">*</button>
            <button data-value="1">1</button>
            <button data-value="2">2</button>
            <button data-value="3">3</button>
            <button data-value="-">-</button>
            <button data-value="0">0</button>
            <button data-value=".">.</button>
            <button data-value="=">=</button>
            <button data-value="+">+</button>
        </div>
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
