<script setup lang="ts">
const props = defineProps({
	classLeft: {
		type: String,
		default: ''
	},
	classRight: {
		type: String,
		default: ''
	},
	classContainer: {
		type: String,
		default: ''
	},
	mobileReverse: {
		type: Boolean,
		default: false
	},
	gradientBar: {
		type: Boolean,
		default: false
	}
})
</script>

<template>
	<section :class="props?.classContainer">
		<div
		class="mx-auto max-w-8xl overflow-hidden flex sm:grid sm:grid-cols-3 md:grid-cols-7"
			:class="mobileReverse ? 'flex-col-reverse' : 'flex-col'"
		>
			<div class="px-4 lg:px-0 sm:col-span-2 md:col-span-3 flex justify-center items-center relative" :class="props?.classLeft">
				<div :class="{'textbox': props?.gradientBar}" class="max-w-[316px] md:max-w-[387px] md:px-6 flex flex-col gap-8 justify-start items-start py-16">
					<div class="relative">
						<slot name="left" />
					</div>
				</div>
			</div>
			<div class="sm:col-span-1 md:col-span-4 overflow-hidden" :class="props?.classRight">
				<slot name="right" />
			</div>
		</div>
	</section>
</template>

<style>
.textbox:after {
	content: '';
    background-image: linear-gradient(4deg, var(--gradient-yellow), var(--gradient-pink), var(--gradient-blue));
	@apply w-[128px] md:w-[6px] h-[6px] md:h-[50%] absolute top-0 md:top-[25%] md:left-0;
}
</style>