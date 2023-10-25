<template>
	<button><slot /></button>
</template>

<style scoped>
button {
	@apply bg-black hover:bg-[#DFDFDF] text-white hover:text-black px-6 py-2 h-[40px] text-sm uppercase border-none hover:border-none transition-all duration-300 ease-in-out;
}
</style>
