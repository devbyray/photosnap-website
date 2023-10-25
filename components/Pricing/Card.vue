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
	<div :class="{'lg:py-14': !props?.dark}" class="">
		<div class="px-10 py-10 relative" :class="{ 'bg-[#F5F5F5] dark:bg-gray-300': !props?.dark, 'bg-black text-white lg:py-24': props?.dark }">
			<TheGradient v-if="props?.dark" class="absolute top-0 left-0 md:hidden lg:block" />
			<TheGradient v-if="props?.dark" vertical class="absolute top-0 left-0 hidden md:block lg:hidden" />
			<div class="mx-auto grid md:grid-cols-5 lg:grid-cols-1 gap-8 md:gap-4 lg:flex lg:flex-col lg:gap-8">
				<h2 class="text-[25px] leading-[25px] font-semibold tracking-wide md:col-start-1 md:col-span-2">{{ props?.title }}</h2>
				<p class="mb-4 opacity-60 md:col-start-1 md:col-span-2">
					{{ props?.description }}
				</p>
				<div class="flex flex-col items-center md:col-start-5 md:row-start-1 md:row-span-2 md:items-end lg:items-center">
					<strong class="text-[40px] leading-[48px] font-semibold">${{ props?.price }}</strong>
					<span>per month</span>
				</div>
				<Button class="w-full md:col-start-1 md:col-span-2" :dark="props?.dark">Pick a plan</Button>
			</div>
		</div>
	</div>
</template>
