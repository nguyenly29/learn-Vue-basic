<template>
  <div>
    <h1>Đây là Trang Chủ</h1>
    <p>Nội dung trang chủ đã hiển thị thành công!</p>
    <h2>{{name}}</h2>
    <input type="text" v-model="name"/>
    <h2>{{count}}</h2>
    <button @click="handleClick">Click Me</button> <hr/>
    <button @click="toggleMenu">On / Off</button>
    <h3 v-if="isOpenMenu">Display</h3>
    <ul v-for="(hs, index) in students" :key="hs.id">
      <li>{{hs.name}}</li>
      <button @click="remove(index)">Delete</button>
    </ul>
  </div>
</template>
<script setup>
import { ref } from 'vue'
const name = ref('Hello')
const count = ref(0)

// xu ly nut button thi khong can value 
const handleClick = () => {
  count.value++
}

const isOpenMenu = ref(true)
const toggleMenu = () => {
  isOpenMenu.value = !isOpenMenu.value
}

const students = ref([
  { id: 1, name: "Alex" },
  { id: 2, name: "Vinni" },
  { id: 3, name: "Antony" }
])

const remove = (index) => {
  students.value.splice(index, 1)
}

</script>
<style scoped>
ul {
  display: flex;
  justify-content: left;
  align-items: center;
  gap: 10px
}
</style>