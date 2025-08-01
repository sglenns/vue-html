<script setup lang="ts">
import ButtonComponent from '../src/components/ButtonComponent.vue'
</script>

<template>
  <Story>
    <Variant title="default">
      <ButtonComponent>Button</ButtonComponent>
    </Variant>
    <Variant title="outline">
      <ButtonComponent variant="outline">Button</ButtonComponent>
    </Variant>
  </Story>
</template>
