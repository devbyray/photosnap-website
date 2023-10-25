import { TheGradient } from '#build/components';
<script lang="ts" setup>
const props = defineProps({
	title: {
		type: String,
		required: true
	},
	price: {
		type: String,
		required: true
	},
	description: {
		type: String,
		required: true
	},
	dark: {
		type: Boolean,
		required: false,
		default: false
	},
	gradient: {
		type: Boolean,
		required: false,
		default: false
	}
})
</script>

<template>
	<div :class="{'md:py-8': !props?.dark}" class="md:w-[33%] mx-auto">
		<div class="px-8 py-16 relative" :class="{ 'bg-[#F5F5F5] dark:bg-gray-300': !props?.dark, 'bg-black text-white md:py-24': props?.dark }">
			<TheGradient v-if="props?.dark" class="absolute top-0 left-0" />
			<div class="mx-auto max-w-[275px] flex flex-col items-center gap-8">
				<h2 class="text-[25px] leading-[25px] font-semibold tracking-wide">{{ props?.title }}</h2>
				<p class="mb-4 opacity-60">
					{{ props?.description }}
				</p>
				<div class="flex flex-col items-center">
					<strong class="text-[40px] leading-[48px] font-semibold">${{ props?.price }}</strong>
					<span>per month</span>
				</div>
				<Button class="w-full" :dark="props?.dark">Pick a plan</Button>
			</div>
		</div>
	</div>
</template>
