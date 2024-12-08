<template>
<div>
    {{ msg }}
<br>
{{ count }}
</div>

</template>

<script setup lang="ts">
defineProps({
    msg: String,
    count:Number

})

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