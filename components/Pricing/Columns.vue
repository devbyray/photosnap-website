<script lang="ts" setup>
const prices = [
	{
		title: 'Basic',
		price: '19.00',
		yearlyPrice: '19.00',
		monthlyPrice: '29.00',
		description: 'Includes basic usage of our platform. Recommended for new and aspiring photographers.',
		dark: false
	},
	{
		title: 'Pro',
		price: '39.00',
		yearlyPrice: '39.00',
		monthlyPrice: '49.00',
		description: 'More advanced features available. Recommended for photography veterans and professionals.',
		dark: true
	},
	{
		title: 'Business',
		price: '99.00',
		yearlyPrice: '99.00',
		monthlyPrice: '109.00',
		description: 'Additional features available such as more detailed metrics. Recommended for business owners.',
		dark: false
	}
]
const monthlyScheme = ref(false)
const toggleScheme = () => {
	monthlyScheme.value = !monthlyScheme.value
}
</script>

<template>
	<div class="bg-white dark:bg-gray-400 py-16 px-4">
		<div class="mx-auto py-16">
			<div class="flex justify-center items-center gap-6">
				<span @click="toggleScheme" class="text-[18px]" :class="{ 'text-black font-semibold': monthlyScheme, 'text-gray-700': !monthlyScheme }"
					>Monthly</span
				>
				<div>
					<label
						for="paymentScheme"
						class="relative cursor-pointer block w-[64px] bg-gray-200 dark:bg-gray-500 p-1 rounded-full mx-2"
					>
						<input v-model="monthlyScheme" id="paymentScheme" type="checkbox" class="hidden" />
						<div
							class="bg-black rounded-full w-[24px] h-[24px] transition ease-in-out delay-50"
							:class="{ 'translate-x-[130%]': !monthlyScheme }"
						></div>
					</label>
				</div>
				<span @click="toggleScheme" class="text-[18px]" :class="{ 'text-black font-semibold': !monthlyScheme, 'text-gray-700': monthlyScheme }"
					>Yearly</span
				>
			</div>
		</div>

		<div class="grid gap-4 mx-auto max-w-3xl lg:max-w-6xl lg:grid-cols-3">
			<template v-for="price in prices">
				<PricingCard
					:title="price.title"
					:price="monthlyScheme ? price.monthlyPrice : price.yearlyPrice"
					:description="price.description"
					:dark="price.dark"
				/>
			</template>
		</div>
	</div>
</template>
