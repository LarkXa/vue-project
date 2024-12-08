<template>
    <div class="page">
    <h1 ref="RefH">This is Ref H1 Welcom </h1>
    <input type="text" v-model="msg">
    <h3>{{ msg }}</h3>
    <ImpComp ref="RefImp" />
    </div>
    </template>
    
    <script setup lang="ts">
import { onMounted, ref } from 'vue';
import ImpComp from './ImpComp.vue';
    const RefH = ref(null)
    const RefImp = ref(null)
    const msg = ref('Hello world')

    onMounted(()=>{
        console.log(RefH.value)
        console.log(RefImp.value)

    })

    </script>
    
    <style scoped>
    .page {
        height: 400px;
        width: 500px;
        background-color: #e8cece;
        display: flex;
        justify-content: center; /* 水平居中 */
        align-items: center; /* 垂直居中 */
        text-align: center; /* 如果想让文本水平居中 */
    }
    </style>
    