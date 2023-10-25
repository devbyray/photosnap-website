<script lang="ts" setup>
const stories = [
	{
		title: 'The Mountains',
		image: 'mountains',
            date: 'April 16th 2020',
            author: 'John Appleseed'
	},
	{
		title: 'Sunset Cityscapes',
		image: 'cityscapes',
            date: 'April 14th 2020',
            author: 'Benjamin Cruz'
	},
	{
		title: '18 Days Voyage',
		image: '18-days-voyage',
            date: 'April 11th 2020',
            author: 'Alexei Borodin'
	},
	{
		title: 'Architecturals',
		image: 'architecturals',
            date: 'April 9th 2020',
            author: 'Samantha Brooke'
	}
]
</script>

<template>
	<section>
		<div class="mx-auto max-w-screen-2xl sm:grid sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4">
			<template v-for="(story, index) in stories">
				<StoriesCard :title="story.title" :image="story.image" :date="story.date" :author="story.author" :async="index > 6" />
			</template>
		</div>
	</section>
</template>
