<script setup>
import { ref } from 'vue'

const message = ref('Hello World!')

function reverseMessage() {
  message.value = message.value.split('').reverse().join('')
}

function notify() {
  alert('탐색이 차단되었습니다.')
}
</script>

<template>
  <h1>{{ message }}</h1>
  
  <button @click="reverseMessage">거꾸로 출력하기</button>

  <button @click="message += '!'">느낌표 붙이기</button>

  <a href="https://vuejs.org" @click.prevent="notify">
    경고 메시지 띄우기
  </a>
  
</template>

<style>
button, a {
  display: block;
  margin-bottom: 1em;
}
</style>