<template>
	<header class="bg-white">
		<div class="header-wrapper">
            <div>
                Photosnap
            </div>
			<nav>
				<nuxt-link to="/">Stories</nuxt-link>
				<nuxt-link to="/features">Features</nuxt-link>
				<nuxt-link to="/pricing">Pricing</nuxt-link>
			</nav>
            <div>
                <button>Get an invite</button>
            </div>
		</div>
	</header>
</template>

<style scoped>
    header {
        padding: 1rem 0;
    }
    .header-wrapper {
        @apply mx-auto max-w-5xl flex justify-between
    }
    nav {
        @apply flex gap-4 items-center;
    }
    nav a {
        @apply text-gray-500 uppercase text-sm;
    }
    nav a:hover {
        color: #000;
    }
    button {
        @apply bg-black hover:bg-[#DFDFDF] text-white hover:text-black px-4 py-2 text-sm uppercase border-none hover:border-none transition-all duration-300 ease-in-out;
    }
</style>
