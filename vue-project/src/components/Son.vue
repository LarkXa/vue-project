<template>
<div>
    {{ msg }}
<br>
{{ count }}

<button @click="transMsg">transMsg</button>

</div>

</template>

<script setup lang="ts">
defineProps({
    msg: String,
    count:Number

})

const emit = defineEmits(['msg-trans'])
//通过defineEmits编译器宏生成emit方法

const transMsg = () => {
    emit('msg-trans', 'This from Son component')
    // 触发自定义事件msg-trans  传递参数
}

</script>

<style scoped>
div {
    height: 400px;
    width: 300px;
    background-color: #cb7070;
     /* 使用flex布局 */
    display: flex;
    justify-content: center; /* 水平居中 */
    align-items: center; /* 垂直居中 */
    text-align: center; /* 如果想让文本水平居中 */
}

</style>