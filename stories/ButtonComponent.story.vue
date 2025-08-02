<script setup lang="ts">
import ButtonComponent from '../src/components/ButtonComponent.vue'
</script>

<template>
  <Story title="Links" :layout="{ type: 'grid', width: '45%' }">
    <Variant title="default">
      <ButtonComponent>Button</ButtonComponent>
      <ButtonComponent color="info">Button</ButtonComponent>
      <ButtonComponent color="warning">Button</ButtonComponent>
      <ButtonComponent color="danger">Button</ButtonComponent>
    </Variant>
    <Variant title="default disabled">
      <ButtonComponent disabled>Button</ButtonComponent>
      <ButtonComponent disabled color="info">Button</ButtonComponent>
      <ButtonComponent disabled color="warning">Button</ButtonComponent>
      <ButtonComponent disabled color="danger">Button</ButtonComponent>
    </Variant>
    <Variant title="outline">
      <ButtonComponent variant="outline">Button</ButtonComponent>
      <ButtonComponent variant="outline" color="info">Button</ButtonComponent>
      <ButtonComponent variant="outline" color="warning">Button</ButtonComponent>
      <ButtonComponent variant="outline" color="danger">Button</ButtonComponent>
    </Variant>
    <Variant title="outline disabled">
      <ButtonComponent disabled variant="outline">Button</ButtonComponent>
      <ButtonComponent disabled variant="outline" color="info">Button</ButtonComponent>
      <ButtonComponent disabled variant="outline" color="warning">Button</ButtonComponent>
      <ButtonComponent disabled variant="outline" color="danger">Button</ButtonComponent>
    </Variant>
  </Story>
</template>
