<script setup>
import {ref, watch, reactive} from 'vue'

const inputValue = ref(``)
const user = reactive({
  name: 'Maxim',
  age: 20,
})
const newName = ref(``)

function changeUserName(){
  user.name = newName.value
}

watch(inputValue, () => {
  console.log(`Новое значение Value = ${inputValue.value}`)
})

</script>

<template>
  <input v-model="inputValue" class="border" placeholder="Напишите что-нибудь">
  <div>Введенное значение: {{ inputValue }}</div>
  <div>
    <p>Информация о пользователе {{ user.name }} следующая: его возраст - {{ user.age }}</p>
    <input v-model="newName" placeholder="Новое имя">
    <button @click="changeUserName" class="px-4 bg-green-500">Поменять имя пользователя</button>
  </div>
</template>

