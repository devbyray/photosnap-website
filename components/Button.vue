<script lang="ts" setup>
const props = defineProps({
	dark: {
		type: Boolean,
		required: false,
		default: false
	}
})
</script>

<template>
	<button :class="{'bg-black hover:bg-[#DFDFDF] text-white hover:text-black' : !props?.dark, 'bg-white text-black hover:bg-[#ccc] dark:bg-gray-300': props?.dark}"><slot /></button>
</template>

<style scoped>
button {
	@apply px-6 py-2 h-[40px] text-sm uppercase border-none hover:border-none transition-all duration-300 ease-in-out;
}
</style>
