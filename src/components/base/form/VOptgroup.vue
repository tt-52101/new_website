<script setup lang="ts">
import { reactive } from 'vue';
import { useVFieldContext } from '/@src/composable/useVFieldContext';

const vFieldContext = reactive(
  useVFieldContext({
    create: false,
    help: 'VOptgroup',
  })
);
</script>

<template>
  <optgroup>
    <slot v-bind="vFieldContext" />
  </optgroup>
</template>

<style scoped lang="scss">
optgroup {
  padding: 0.5em 1em;

  :deep(option) {
    &::before {
      content: '' !important;
    }
  }
}

optgroup[disabled] {
  pointer-events: none;
  opacity: 0.4;
  cursor: default !important;

  :deep(option[disabled]) {
    opacity: 1;
  }
}
</style>
