<script setup lang="ts">
const props = defineProps({
    image: {
        type: String,
        required: true,
    },
    title: {
        type: String,
        required: true,
    },
    description: {
        type: String,
        required: true,
    },
})

const imagePath = `/images/features/desktop/${ props.image }.svg`
</script>

<template>
	<div class="flex flex-col justify-center items-center gap-4 text-center max-w-[310px] md:max-w-[457px]">
		<div class="h-[72px] flex items-center">
            <img :src="imagePath" alt="responsive" class="max-w-[70px] mb-8" />
        </div>
		<h3 class="text-[24px] leading-[32px] font-semibold tracking-wide mb-4">{{ props?.title }}</h3>
		<p class="text-black/60">
			{{ props?.description }}
		</p>
	</div>
</template>
