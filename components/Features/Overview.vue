<script lang="ts" setup>
const features = [
	{
		image: 'responsive',
		title: '100% Responsive',
		description:
			'No matter which the device you’re on, our site is fully responsive and stories look beautiful on any screen.'
	},
	{
		image: 'no-limit',
		title: 'No Photo Upload Limit',
		description:
			'Our tool has no limits on uploads or bandwidth. Freely upload in bulk and share all of your stories in one go.'
	},
	{
		image: 'embed',
		title: 'Available to Embed',
		description: 'Embed Tweets, Facebook posts, Instagram media, Vimeo or YouTube videos, Google Maps, and more.'
    },
    {
        image: 'custom-domain',
        title: 'Custom Domain',
        description: 'With Photosnap subscriptions you can host your stories on your own domain. You can also remove our branding!'
    },
    {
        image: 'boost-exposure',
        title: 'Boost Your Exposure',
        description: 'Users that viewed your story or gallery can easily get notifed of new and featured stories with our built in mailing list.'
    },
    {
        image: 'drag-drop',
        title: 'Drag & Drop Image',
        description: 'Easily drag and drop your image and get beautiful shots everytime. No over the top tooling to add friction to creating stories.'
    }
]
</script>

<template>
    <section class="mx-auto max-w-screen-2xl bg-white dark:bg-gray-400">
		<div
			class="mx-auto max-w-6xl flex flex-col items-center md:grid md:grid-cols-3 py-24 sm:py-32 gap-20 sm:gap-16"
		>
			<template v-for="feature in features">
				<FeaturesCol :title="feature.title" :image="feature.image" :description="feature.description" />
			</template>
		</div>
	</section>
</template>
