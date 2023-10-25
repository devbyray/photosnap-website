<script lang="ts" setup>
const prices = [
	{
		title: 'Basic',
		price: '19.00',
		description: 'Includes basic usage of our platform. Recommended for new and aspiring photographers.',
		dark: false
	},
	{
		title: 'Pro',
		price: '39.00',
		description: 'More advanced features available. Recommended for photography veterans and professionals.',
		dark: true
	},
	{
		title: 'Business',
		price: '99.00',
		description: 'Additional features available such as more detailed metrics. Recommended for business owners.',
		dark: false
	}
]
</script>

<template>
	<div class="bg-white dark:bg-gray-400 py-16 px-4">
		<div class="grid gap-4 mx-auto max-w-3xl lg:max-w-6xl lg:grid-cols-3">
			<template v-for="price in prices">
				<PricingCard
					:title="price.title"
					:price="price.price"
					:description="price.description"
					:dark="price.dark"
				/>
			</template>
		</div>
	</div>
</template>
