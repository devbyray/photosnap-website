

<template>
	<NuxtLayout>
		<div class="mx-auto max-w-screen-2xl">
			<GridTextLeft classLeft="bg-black text-white" mobileReverse gradientBar>
				<template v-slot:left>
					<h2
						class="text-[32px] leading-[40px] md:text-[40px] md:leading-[48px] uppercase font-semibold tracking-wide mb-8"
					>
						Pricing
					</h2>
					<p class="opacity-60 mb-6">
						Create a your stories, Photosnap is a platform for photographers and visual storytellers. It’s
						the simple way to create and share your photos.
					</p>
				</template>
				<template v-slot:right>
					<picture>
						<source
							media="(min-width: 641px and max-width: 1024px)"
							srcset="/images/pricing/tablet/hero.jpg"
						/>
						<source media="(min-width: 1024px)" srcset="/images/pricing/desktop/hero.jpg" />
						<img
							src="/images/pricing/mobile/hero.jpg"
							alt="Create and share your photo stories."
							class="object-cover w-full h-full"
						/>
					</picture>
				</template>
			</GridTextLeft>
		</div>
		<PricingColumns />
        <PricingTable />
	</NuxtLayout>
</template>
