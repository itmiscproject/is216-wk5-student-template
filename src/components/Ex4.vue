<script setup>
import { ref } from 'vue'
const items = ref(['keyboard', 'mouse', 'iPhone', 'macbook', 'adapter'])
const newItem = ref('')

function add() {
    items.value.push(newItem.value)
    newItem.value = ''
}   
</script>

<template>
    <h2>Shopping Cart</h2>
    <ul>
        <li v-for="(item, i) in items">
            {{item}}
        <button @click="items.splice(i, 1)">Delete!</button> </li>
    </ul>
    <input @keyup.enter="add" v-model="newItem"/>
    <button @click="add">Add!</button>    
</template>
