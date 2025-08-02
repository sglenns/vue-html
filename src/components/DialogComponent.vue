<script setup lang="ts">
import { useTemplateRef, watch } from 'vue'

type DialogComponentProps = {
  openDialog: boolean
}

const props = withDefaults(defineProps<DialogComponentProps>(), {
  openDialog: false,
})

const dialog = useTemplateRef('dialog-component')

watch(
  () => props.openDialog,
  (newOpenDialog) => {
    console.log({ newOpenDialog })
    if (newOpenDialog) {
      dialog.value?.showModal()
    } else {
      dialog.value?.close()
    }
  },
  { immediate: true }
)
</script>

<template>
  <dialog ref="dialog-component">
    <slot name="default">I'm a dialog</slot>
    <form method="dialog">
      <button>OK</button>
    </form>
  </dialog>
</template>

<style scoped></style>
