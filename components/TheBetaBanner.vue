<script setup lang="ts"></script>

<template>
	<section class="relative transition bg-black">
		<div class="relative overflow-hidden flex">
			<picture>
				<source media="(min-width: 641px)" srcset="/images/shared/tablet/bg-beta.jpg" />
				<source media="(min-width: 1024px)" srcset="/images/shared/desktop/bg-beta.jpg" />
				<img
					src="/images/shared/mobile/bg-beta.jpg"
					alt="Create and share your photo stories."
					class="object-cover w-full h-full absolute bottom-0 left-0"
				/>
			</picture>

			<footer
				class="text-white w-full h-full bg-gradient-to-b from-white/0 to-black/75 z-[10]"
			>
				<div class="mx-auto max-w-screen-2xl flex justify-between sm:items-center flex-col sm:flex-row px-8 py-16 gap-1">
					<h2
						class="text-[32px] leading-[40px] max-w-[400px] md:text-[40px] md:leading-[48px] uppercase font-semibold tracking-wide mb-8"
					>
						We're in beta. <br />
						Get your invite today!
					</h2>
					<nuxt-link to="/" class="text-sm uppercase flex gap-4 items-center text-white"
						><span>Get an invite</span>
						<img src="/images/shared/desktop/arrow-white.svg" class="max-h-[12px]"
					/></nuxt-link>
				</div>
			</footer>
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
