<script lang="ts">
export default {
  name: 'App',
  data() {
    return {
      name: '马飞',
      age: 18,
      tel: '16637809505'

    }
  }, methods: {
    changeName() {
      this.name = 'mafei'
    },
    changeAge() {
      this.age += 1
    },
    showTel() {
      alert('1154196461')
    }
  }
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
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}

.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}

.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
