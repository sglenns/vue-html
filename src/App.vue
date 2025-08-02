<script setup lang="ts">
import DialogComponent from './components/DialogComponent.vue'
import ButtonComponent from './components/ButtonComponent.vue'

import { ref } from 'vue'

const openDialog = ref(false)
</script>

<template>
  <header>header</header>
  <main>
    <h1>vue-html</h1>
    <p>Just another component library in the making</p>
    ({{ openDialog }})
    <ButtonComponent @click.prevent="() => (openDialog = !openDialog)">Open Dialog</ButtonComponent>
    <DialogComponent :open-dialog="openDialog">Dialog</DialogComponent>
  </main>
  <aside>aside</aside>
  <footer>footer</footer>
</template>

<style scoped></style>
