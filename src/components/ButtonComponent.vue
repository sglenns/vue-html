<script setup lang="ts">
type ButtonComponentProps = {
  size?: 'small' | 'medium' | 'large'
  color?: 'primary' | 'info' | 'warning' | 'danger'
  variant?: 'normal' | 'outline'
}

const props = withDefaults(defineProps<ButtonComponentProps>(), {
  variant: 'normal',
  size: 'medium',
  color: 'primary',
})
</script>

<template>
  <button class="btn" :class="`btn--${props.size} btn--${props.color} btn--${props.variant}`">
    <slot name="default">Click Me</slot>
  </button>
</template>

<style scoped>
.btn {
  border-width: 1px;
  border-style: solid;
  border-color: var(--main-color);
  background-color: var(--main-color);
  color: white;
  &:hover {
    background-color: var(--main-color-hover);
    color: white;
  }
  &:disabled {
    background-color: var(--main-color-disabled);
  }
}

/** VARIANTS */
.btn--outline {
  border-color: var(--main-color);
  background-color: white;
  color: var(--main-color);
  &:hover {
    color: white;
  }
  &:disabled {
    color: var(--main-color);
  }
}

/** SIZES */
.btn--small {
  padding: 0.25em 0.5em;
  font-size: 0.8em;
}
.btn--medium {
  padding: 0.5em 1em;
  font-size: 1em;
}
.btn--large {
  padding: 0.75em 1.5em;
  font-size: 1.2em;
}

/** COLORS */
.btn--primary {
  --main-color: var(--color-primary);
  --main-color-hover: var(--color-primary-light);
  --main-color-disabled: var(--color-primary-dark);
}
.btn--info {
  --main-color: var(--color-info);
  --main-color-hover: var(--color-info-light);
  --main-color-disabled: var(--color-info-dark);
}
.btn--warning {
  --main-color: var(--color-warning);
  --main-color-hover: var(--color-warning-light);
  --main-color-disabled: var(--color-warning-dark);
}
.btn--danger {
  --main-color: var(--color-danger);
  --main-color-hover: var(--color-danger-light);
  --main-color-disabled: var(--color-danger-dark);
}
</style>
