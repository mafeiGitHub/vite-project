<script setup lang="ts">
import { ref} from "vue";


let person = ref({
  name: '张三',
  age: 18,
  tel: '13888888888',
  gender:'man'
})


// 方法
function changeName() {
  person.value.name = '李四'//注意：此时这么修改name页面是不变化的
}
function changeAge() {
  console.log(person)
  person.value.age += 1 //注意：此时这么修改age页面是不变化的
}

function showTel() {
  alert(person.value.tel)
}
</script>

<template>
  <div class="person">
    <h2>姓名:{{ person.name }}</h2>
    <h2>年龄:{{ person.age }}</h2>
    <button @click="changeName">修改名字</button>
    <button @click="changeAge">修改年龄</button>
    <button @click="showTel">点击查看联系方式</button>
  </div>
</template>

<style scoped>

</style>
