<script lang="ts" setup>
useSeoMeta({
	title: 'Photosnap | Home',
	description: 'Photosnap is a platform for photographers and visual storytellers. We make it easy to share photos, tell stories and connect with others.',
})
</script>
<template>
	<NuxtLayout>
		<HomeRows />
		<HomeStories />
		<HomeFeatures />
	</NuxtLayout>
</template>
