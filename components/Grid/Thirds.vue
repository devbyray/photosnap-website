<template>
	<section class="flex flex-col-reverse sm:grid sm:grid-cols-3 md:grid-cols-7">
		<div class="sm:col-span-2 md:col-span-3 bg-black text-white flex justify-center items-center">
			<slot name="left" />
		</div>

		<div class="sm:col-span-1 md:col-span-4">
			<slot name="right" />
		</div>
	</section>
</template>
