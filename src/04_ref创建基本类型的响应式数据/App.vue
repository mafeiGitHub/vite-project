<script setup lang="ts">
import {ref} from "vue";

// 数据（注意：此时的name、age、tel都不是响应式数据）
let name = ref('张三')
let age = ref(18)
let tel = '13888888888'

// 方法
function changeName(){
  name.value = '李四'//注意：此时这么修改name页面是不变化的
}
function changeAge(){
  console.log(age)
  age.value += 1 //注意：此时这么修改age页面是不变化的
}
function showTel(){
  alert(tel)
}
</script>

<template>
  <div class="person">
    <h2>姓名:{{ name }}</h2>
    <h2>年龄:{{ age }}</h2>
    <button @click="changeName">修改名字</button>
    <button @click="changeAge">修改年龄</button>
    <button @click="showTel">点击查看联系方式</button>
  </div>
</template>

<style scoped>

</style>
