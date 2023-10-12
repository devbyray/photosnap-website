<template>
	<NuxtLayout>
		<section class="grid grid-cols-7">
			<div class="col-span-3 bg-black text-white flex justify-center items-center">
				<div class="max-w-[500px] flex flex-col gap-4 justify-start items-start">
					<h2 class="text-6xl uppercase font-semibold tracking-wide">Create and share your photo stories.</h2>
					<p class="opacity-60">
						Photosnap is a platform for photographers and visual storytellers. We make it easy to share
						photos, tell stories and connect with others.
					</p>
                    <nuxt-link to="/" class="text-sm uppercase flex gap-4 items-center"><span>Get an invite</span> <img src="/images/shared/desktop/arrow-white.svg" class="max-h-[12px]" /></nuxt-link>
				</div>
			</div>
			<div class="col-span-4">
				<img src="/images/home/desktop/create-and-share.jpg" alt="Create and share your photo stories." class="object-contain w-full" />
			</div>
		</section>
	</NuxtLayout>
</template>
