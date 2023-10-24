<script lang="ts" setup>
const props = defineProps({
  vertical: {
    type: Boolean,
    default: false,
  },
});
</script>

<template>
  <div
    class=""
    :class="{ 'w-full h-[6px] gradient': !props.vertical, 'w-[6px] h-full gradient': props.vertical }"
  ></div>
</template>

<style>
.gradient {
    background-image: linear-gradient(2deg, var(--gradient-yellow), var(--gradient-pink), var(--gradient-blue));
}
</style>
