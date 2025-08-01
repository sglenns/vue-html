<script setup lang="ts">
type LinkComponentProps = {
  color?: 'primary' | 'info' | 'warning' | 'danger'
}

const props = withDefaults(defineProps<LinkComponentProps>(), {
  variant: 'normal',
  size: 'medium',
  color: 'primary',
})
</script>

<template>
  <a class="lnk" :class="`lnk--${props.color}`">
    <slot name="default">Click Me</slot>
  </a>
</template>

<style scoped>
.lnk {
  color: var(--main-color);
  &:hover {
    color: var(--main-color-hover);
    text-decoration: underline;
  }
  &:visited {
    color: var(--main-color-visited);
  }
}

/** COLORS */
.lnk--primary {
  --main-color: var(--color-primary);
  --main-color-hover: var(--color-primary-light);
  --main-color-visited: var(--color-primary-dark);
}
.lnk--info {
  --main-color: var(--color-info);
  --main-color-hover: var(--color-info-light);
  --main-color-visited: var(--color-info-dark);
}
.lnk--warning {
  --main-color: var(--color-warning);
  --main-color-hover: var(--color-warning-light);
  --main-color-visited: var(--color-warning-dark);
}
.lnk--danger {
  --main-color: var(--color-danger);
  --main-color-hover: var(--color-danger-light);
  --main-color-visited: var(--color-danger-dark);
}
</style>
