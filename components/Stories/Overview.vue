<script lang="ts" setup>
const featuredStory = {
      title: 'Hazy Full Moon Of Appalachia',
      image: 'moon-of-appalacia',
      date: 'March 2nd 2020',
      author: 'John Appleseed',
      description: 'The dissected plateau area, while not actually made up of geological mountains, is popularly called "mountains," especially in eastern Kentucky and West Virginia, and while the ridges are not high, the terrain is extremely rugged.'
}
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
	},
	{
		title: 'World Tour 2019',
		image: 'world-tour',
            date: 'April 7th 2020',
            author: 'Timothy Wagner'
	},
	{
		title: 'Unforseen Corners',
		image: 'unforeseen-corners',
            date: 'April 3rd 2020',
            author: 'William Malcolm'
	},
	{
		title: 'King on Africa: Part ||',
		image: 'king-on-africa',
            date: 'March 29th 2020',
            author: 'Tim Hillenburg'
	},
	{
		title: 'The Trip To Nowhere',
		image: 'trip-to-nowhere',
            date: 'March 21st 2020',
            author: 'Felicia Rourke'
      },
      {
            title: 'Rage of The Sea',
            image: 'rage-of-the-sea',
            date: 'March 19th 2020',
            author: 'Mohammed Abdul'
      },
      {
            title: 'Running Free',
            image: 'running-free',
            date: 'March 16th 2020',
            author: 'Michelle'
      },
      {
            title: 'Behind the Waves',
            image: 'behind-the-waves',
            date: 'March 11th 2020',
            author: 'Lamarr Wilson'
      },
      {
            title: 'Calm Waters',
            image: 'calm-waters',
            date: 'March 9th 2020',
            author: 'Samantha Brooke'
      },
      {
            title: 'The Milky Way',
            image: 'milky-way',
            date: 'March 5th 2020',
            author: 'Benjamin Cruz'
      },
      {
            title: 'Night at The Dark Forest',
            image: 'dark-forest',
            date: 'March 4th 2020',
            author: 'Mohammed Abdul'
      },
      {
            title: 'Somwarpet’s Beauty',
            image: 'somwarpet',
            date: 'March 1st 2020',
            author: 'Michelle'
      },
      {
            title: 'Land of Dreams',
            image: 'land-of-dreams',
            date: 'February 25th 2020',
            author: 'William Malcolm'
      }
]
</script>

<template>
	<section class="mx-auto max-w-screen-2xl">
            <StoriesBigCard class="col-span-4" :title="featuredStory.title" :image="featuredStory.image" :date="featuredStory.date" :author="featuredStory.author" :description="featuredStory.description" />
		<div class="sm:grid sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4">
			<template v-for="story in stories">
				<StoriesCard :title="story.title" :image="story.image" :date="story.date" :author="story.author" />
			</template>
		</div>
	</section>
</template>
