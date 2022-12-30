<template>
  <div :style="{
  'clip-path': `polygon(0 ${topLeft}px, 100% ${topRight}px, 100% calc(100% - ${bottomRight}px), 0 calc(100% - ${bottomLeft}px))`,
  'padding-top': `${paddingTop}px`,
  'padding-bottom': `${paddingBottom}px`,
  'margin-top': `-${inset ? 0 : paddingTop}px`,
  'overflow-x': 'hidden'
}">
    <slot />
  </div>
</template>

<script setup lang="ts">

const props = withDefaults(defineProps<{
  topLeft?: number,
  topRight?: number,
  bottomLeft?: number,
  bottomRight?: number,
  inset?: boolean
}>(), {
  topLeft: 0,
  topRight: 0,
  bottomLeft: 0,
  bottomRight: 0,
  inset: false
})

const paddingTop = computed(() => Math.max(props.topLeft, props.topRight));
const paddingBottom = computed(() => Math.max(props.bottomLeft, props.bottomRight));

// setup code
</script>
