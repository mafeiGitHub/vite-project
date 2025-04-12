

<script setup lang="ts">
import {reactive, toRef, toRefs} from "vue";


let person = reactive({
  name: '张三',
  age: 18,
  tel: '13888888888',
  gender:'man'
})
let {name,age} = toRefs(person)
let gender = toRef(person,'gender')


// 方法
function changeName() {
  name.value = '李四'//注意：此时这么修改name页面是不变化的
}
function changeAge() {
  console.log(person)
  age.value += 1 //注意：此时这么修改age页面是不变化的
}

function showTel() {
  alert(person.tel)
}
function changeGender() {
  gender.value = 'women'
}
</script>

<template>
  <div class="person">
    <h2>姓名:{{ name }}</h2>
    <h2>年龄:{{ age }}</h2>
    <h2>性别:{{ gender }}</h2>

    <button @click="changeName">修改名字</button>
    <button @click="changeAge">修改年龄</button>
    <button @click="showTel">点击查看联系方式</button>
    <button @click="changeGender">修改性别</button>
  </div>
</template>

<style scoped>

</style>
