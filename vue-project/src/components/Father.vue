<template>
 
<div class="fm">
    <p>This is father page</p>
<Son msg="'hello'" :count="count" @msg-trans="getMsg"/>
<!-- 子组件通过自定义事件 接收父组件传递的参数 -->
<button @click="addCount">Add</button>
<br>
{{ sonMsg }}
</div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import Son from './Son.vue';
const count = ref(0)
const sonMsg = ref('')
const addCount = () => {
    count.value++
}
const getMsg = (msg:string) => {
    console.log(msg)
    sonMsg.value = msg
}

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
