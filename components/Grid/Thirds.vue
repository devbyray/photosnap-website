<template>
	<section class="flex flex-col-reverse md:grid md:grid-cols-3 lg:grid-cols-7">
		<div class="md:col-span-2 lg:col-span-3 bg-black text-white flex justify-center items-center">
			<slot name="left" />
		</div>

		<div class="md:col-span-1 lg:col-span-4">
			<slot name="right" />
		</div>
	</section>
</template>
