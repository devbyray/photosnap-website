<script lang="ts" setup>
const mobileSub = ref(false)
const toggleMobileSub = () => {
	mobileSub.value = !mobileSub.value
}
</script>

<template>
	<header class="bg-white dark:bg-gray-400 w-full flex">
		<div class="desktop-header-wrapper">
			<div><TheLogo black /></div>
			<nav class="links">
				<nuxt-link to="/stories">Stories</nuxt-link>
				<nuxt-link to="/features">Features</nuxt-link>
				<nuxt-link to="/pricing">Pricing</nuxt-link>
			</nav>
			<div class="invite">
				<Button>Get an invite</Button>
			</div>
		</div>
		<div class="mobile-header-wrapper">
			<div class="flex justify-between w-full">
				<TheLogo black />
				<button class="bg-transparant" @click="toggleMobileSub">
					<img
						class="transition"
						:class="{ 'w-0 opacity-0': !mobileSub, 'opacity-100': mobileSub }"
						src="/images/shared/mobile/close.svg"
					/>
					<img
						class="transition"
						:class="{ 'opacity-100': !mobileSub, 'w-0 opacity-0': mobileSub }"
						src="/images/shared/mobile/menu.svg"
					/>
				</button>
			</div>
		</div>
		<div
			class="mobile-toggle"
			:class="{ 'hidden w-0 opacity-0': !mobileSub, '-top-10 w-full opacity-100': mobileSub }"
		>
			<nav class="links">
				<nuxt-link to="/stories">Stories</nuxt-link>
				<nuxt-link to="/features">Features</nuxt-link>
				<nuxt-link to="/pricing">Pricing</nuxt-link>
			</nav>
			<div class="invite">
				<Button>Get an invite</Button>
			</div>
		</div>
	</header>
	<div
		class="overlay"
		:class="{ 'w-0 h-0 opacity-0': !mobileSub, 'opacity-50 w-full h-full md:h-0 md:opacity-0 md:w-0': mobileSub }"
		@click="mobileSub = false"
	></div>
</template>

<style scoped>
header {
	@apply py-4 h-[72px] flex flex-col items-start justify-center px-4 sticky top-0 z-[20];
}
.desktop-header-wrapper {
	@apply mx-auto max-w-5xl w-full hidden md:flex md:justify-between items-center;
}
.mobile-header-wrapper {
	@apply mx-auto max-w-5xl md:hidden flex flex-col w-full px-2;
}
.mobile-toggle {
	@apply transition absolute overflow-hidden top-[72px] left-0 flex flex-col gap-6 bg-white dark:bg-gray-400 px-8 py-4 pb-8 justify-center items-center md:hidden z-[9] md:w-0;
}
.overlay {
	@apply transition absolute overflow-hidden top-[72px] left-0 bg-black z-[8] cursor-pointer;
}
.mobile-toggle .links {
	@apply flex flex-col gap-6;
}
.mobile-toggle .invite {
	@apply w-full border-t-2 border-gray-100 dark:border-gray-500 pt-4;
}
.mobile-toggle .invite button {
	@apply w-full;
}
nav {
	@apply flex gap-8 items-center;
}
nav a {
	@apply text-gray-500 dark:text-gray-700 dark:hover:underline uppercase text-sm;
}
nav a:hover {
	color: #000;
}
</style>
