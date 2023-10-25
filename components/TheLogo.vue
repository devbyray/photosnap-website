<script lang="ts" setup>
const props = defineProps({
    black: {
        type: Boolean,
        value: false
    }
})
console.log('props: ', props)

const path = props.black ? 'images/logo-black.svg' : 'images/logo.svg'
</script>

<template>
  <nuxt-link to="/">
    <img :src="path" class="min-w-[170px]" />
  </nuxt-link>
</template>
