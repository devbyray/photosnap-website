<script lang="ts" setup>
useSeoMeta({
	title: 'Photosnap | Features',
	description: 'Photosnap is a platform for photographers and visual storytellers. We make it easy to share photos, tell stories and connect with others.',
})
</script>

<template>
	<NuxtLayout>
		<div class="mx-auto max-w-screen-2xl">
			<GridTextLeft classLeft="bg-black text-white" mobileReverse gradientBar>
				<template v-slot:left>
					<h2
						class="text-[32px] leading-[40px] md:text-[40px] md:leading-[48px] uppercase font-semibold tracking-wide mb-8"
					>
						Features
					</h2>
					<p class="opacity-60 mb-6">
						We make sure all of our features are designed to be loved by every aspiring and even professional photograpers who wanted to share their stories.
					</p>
				</template>
				<template v-slot:right>
					<picture>
						<source
							media="(min-width: 641px and max-width: 1024px)"
							srcset="/images/features/tablet/hero.jpg"
						/>
						<source media="(min-width: 1024px)" srcset="/images/features/desktop/hero.jpg">
						<img
							src="/images/features/mobile/hero.jpg"
							alt="Create and share your photo stories."
							class="object-cover w-full h-full"
						/>
					</picture>
				</template>
			</GridTextLeft>
		</div>
		<FeaturesOverview />
        <TheBetaBanner />
	</NuxtLayout>
</template>
