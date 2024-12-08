<template>
    <div class="page">
    
    </div>
    </template>
    
    <script setup lang="ts">
    var name = 'Tom'
    const setName = () => {
      name = 'Jerry'
    }

    const dz = 0
    
    defineExpose({dz,
        setName,
        name
    })
    // 通过编译宏 把想要暴露的内部属性和方法
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
    