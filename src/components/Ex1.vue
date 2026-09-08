<script setup>

import { ref } from 'vue';

// const cls = ref('circle')
const id = ref('circle')

function mOver() {
    // add code here
    // cls.value = "square"
    id.value = "square"
}

function mOut() {
    // add code here
    // cls.value = "circle"
    id.value = "circle"
}
</script>

<template>
    <!-- modify code below -->
    <!-- <div id="shape" :class="cls" @mouseover="mOver" @mouseout="mOut"> -->
    <div :id="id" @mouseover="mOver" @mouseout="mOut">
        Mouse Over Me
    </div>

</template>

<style scoped>
/*
#shape {
    width: 150px;
    height: 150px;
    background-color: goldenrod;
    text-align: center;
    padding-top: 60px;
}

.circle {
    border-radius: 50%;
}

.square {
    border-radius: 0%;
}
*/
#square {
    width: 150px;
    height: 150px;
    background-color: goldenrod;
    text-align: center;
    padding-top: 60px;
}

#circle {
    width: 150px;
    height: 150px;
    border-radius: 50%;
    background-color: goldenrod;
    text-align: center;
    padding-top: 60px;
}

</style>