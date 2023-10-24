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
	}
})
</script>

<template>
	<section :class="props?.classContainer">
		<div
			class="mx-auto max-w-8xl overflow-hidden flex sm:grid sm:grid-cols-3 md:grid-cols-7"
			:class="mobileReverse ? 'flex-col-reverse' : 'flex-col'"
		>
			<div class="sm:col-span-1 md:col-span-4 overflow-hidden" :class="props?.classLeft">
				<slot name="left" />
			</div>

			<div class="sm:col-span-2 md:col-span-3 flex justify-center items-center" :class="props?.classRight">
				<div class="max-w-[316px] md:max-w-[387px] md:px-6 flex flex-col gap-8 justify-start items-start py-16">
					<slot name="right" />
				</div>
			</div>
		</div>
	</section>
</template>
