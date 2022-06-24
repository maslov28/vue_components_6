<template>
  <ul>
    <li>Сверстать инпут</li>
    <li>сделать так, чтобы при открытии страницы у инпута был активный фокус</li>
  </ul>
  <input type="text" ref="myInput" />
</template>

<script>
import {ref, onMounted} from 'vue'

export default {
  setup() {
    const myInput = ref(null)

    onMounted(() => {
      myInput.value.focus()
    })

    return {
      myInput
    }
  }
}
</script>