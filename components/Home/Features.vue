<script lang="ts" setup>
const features = [
    {
        image: 'responsive',
        title: '100% Responsive',
        description: 'No matter which the device you’re on, our site is fully responsive and stories look beautiful on any screen.'
    },
    {
        image: 'no-limit',
        title: 'No Photo Upload Limit',
        description: 'Our tool has no limits on uploads or bandwidth. Freely upload in bulk and share all of your stories in one go.'
    },
    {
        image: 'embed',
        title: 'Available to Embed',
        description: 'Embed Tweets, Facebook posts, Instagram media, Vimeo or YouTube videos, Google Maps, and more.'
    }
]
</script>

<template>
    <section class="mx-auto max-w-screen-2xl bg-white dark:bg-gray-400">
        <div class="mx-auto max-w-6xl flex flex-col items-center md:grid md:grid-cols-3 py-24 sm:py-32 gap-20 sm:gap-16">

            <template v-for="(feature, index) in features">
				<FeaturesCol :title="feature.title" :image="feature.image" :description="feature.description" />
			</template>
        </div>
    </section>
</template>