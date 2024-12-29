<script setup>
import {ref} from 'vue'

const count = ref(0)

function increment() {
  count.value++
}

function decrement(){
  count.value--
}
</script>

<template>
  <span class="p-4 accent-red-300">{{ count }}</span>
  <button @click="increment" class="bg-green-300">Увеличить</button>
  <button @click="decrement" class="bg-red-300">Уменьшить</button>
</template>

