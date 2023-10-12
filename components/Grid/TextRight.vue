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
			class="mx-auto max-w-8xl overflow-hidden flex md:grid md:grid-cols-3 lg:grid-cols-7"
			:class="mobileReverse ? 'flex-col-reverse' : 'flex-col'"
		>
			<div class="md:col-span-1 lg:col-span-4 overflow-hidden" :class="props?.classLeft">
				<slot name="left" />
			</div>

			<div class="md:col-span-2 lg:col-span-3 flex justify-center items-center" :class="props?.classRight">
				<div class="max-w-[316px] lg:max-w-[387px] flex flex-col gap-8 justify-start items-start py-16">
					<slot name="right" />
				</div>
			</div>
		</div>
	</section>
</template>
