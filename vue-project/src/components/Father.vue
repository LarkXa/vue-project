<template>
 
<div class="fm">
    <p>This is father page</p>
<Son msg="'hello'" :count="count"/>
<button @click="addCount">Add</button>
</div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import Son from './Son.vue';
const count = ref(0)
const addCount = () => {
    count.value++
}
setTimeout(() => {
    count.value = 10
}, 3000);


</script>

<style scoped>
.fm {
    height: 500px;
    width: 500px;
    background-color: #c09292;
    display: flex;
    justify-content: center; /* 水平居中 */
    align-items: center; /* 垂直居中 */
    text-align: center; /* 如果想让文本水平居中 */
}
</style>
