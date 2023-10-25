<script setup lang="ts">
const props = defineProps({
	image: {
		type: String,
		required: true
	},
	title: {
		type: String,
		required: true
	},
	date: {
		type: String,
		required: true
	},
	author: {
		type: String,
		required: true
	},
	description: {
		type: String,
		required: true
	}
})

const hover = ref(false)
function toggleHover() {
	hover.value = true
}
function leaveHover() {
	hover.value = false
}

const imageMobile = `/images/stories/mobile/${props.image}.jpg`
const imageDesktop = `/images/stories/desktop/${props.image}.jpg`
</script>

<template>
	<div class="relative transition min-h-[650px] flex" @mouseover="toggleHover" @mouseleave="leaveHover">
		<nuxt-link to="/" class="flex flex-col md:flex-row w-full">
			<picture class="w-full">
				<source media="(max-width: 640px)" :srcset="imageMobile" />
				<source media="(min-width: 1024px)" :srcset="imageDesktop" />
				<img :src="imageDesktop" alt="Beautiful stories every time" class="object-cover h-full w-full" />
			</picture>
			<footer
				class="bg-black md:bg-transparent md:absolute md:bottom-0 md:left-0 flex justify-center md:flex-col md:justify-end px-8 py-16 md:py-0 gap-1 text-white w-full h-full bg-gradient-to-b from-white/0 to-black/75"
			>
				<div class="flex flex-col h-full md:pl-24 justify-center max-w-5xl z-[1]">
					<div class="flex flex-col md:max-w-[387px] gap-5">
						<span class="uppercase">Last month's featured story</span>
						<h3 class="text-[40px] leading-[48px] font-semibold tracking-wide uppercase">
							{{ props?.title }}
						</h3>
						<span
							><span class="opacity-60 inline-block mr-1">{{ props?.date }}</span> by
							{{ props?.author }}</span
						>
						<p class="mb-4 opacity-60">{{ props?.description }}</p>
						<div class="flex gap-4 items-center">
							<span class="uppercase text-sm">Read the story</span>
							<img src="/images/shared/desktop/arrow-white.svg" alt="arrow right" class="max-h-[12px]" />
						</div>
					</div>
				</div>
				<div class="absolute bottom-0 left-0 transition" :class="{'opacity-0': !hover, 'opacity-0 md:opacity-50': hover}"><img src="/images/stories/desktop/big-card-hover.png" /></div>
			</footer>
		</nuxt-link>
	</div>
</template>
