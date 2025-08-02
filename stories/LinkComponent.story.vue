<script setup lang="ts">
import LinkComponent from '../src/components/LinkComponent.vue'
</script>

<template>
  <Story title="Links" :layout="{ type: 'grid', width: '45%' }">
    <Variant title="default">
      <LinkComponent href="#">Link</LinkComponent>
      <LinkComponent href="#" color="info">Link</LinkComponent>
      <LinkComponent href="#" color="warning">Link</LinkComponent>
      <LinkComponent href="#" color="danger">Link</LinkComponent>
    </Variant>
  </Story>
</template>
