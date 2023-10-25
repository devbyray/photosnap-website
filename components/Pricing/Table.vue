<script lang="ts" setup>
const tableFeatures = [
	{
		feature: 'Unlimited Story Posting',
		basic: true,
		pro: true,
		business: true
	},
	{
		feature: 'Unlimited Photo Upload',
		basic: true,
		pro: true,
		business: true
	},
	{
		feature: 'Embedding Custom Content',
		basic: false,
		pro: true,
		business: true
	},
	{
		feature: 'Customize Metadata',
		basic: false,
		pro: true,
		business: true
	},
	{
		feature: 'Advanced Metrics',
		basic: false,
		pro: false,
		business: true
	},
	{
		feature: 'Photo Downloads',
		basic: false,
		pro: false,
		business: true
	},
	{
		feature: 'Search Engine Indexing',
		basic: false,
		pro: false,
		business: true
	},
	{
		feature: 'Custom Analytics',
		basic: false,
		pro: false,
		business: true
	}
]
</script>

<template>
	<div class="bg-white dark:bg-gray-400 pt-16 pb-24">
		<div class="max-w-sm md:max-w-3xl mx-auto px-8">
			<h2 class="text-[40px] leading-[48px] font-semibold tracking-wide text-center uppercase mb-8">Compare</h2>
			<table class="uppercase text-[12px] w-full">
				<thead>
					<tr>
						<th>The Features</th>
						<th class="hidden md:table-cell">Basic</th>
						<th class="hidden md:table-cell">Pro</th>
						<th class="hidden md:table-cell">Business</th>
					</tr>
				</thead>
				<tbody>
					<template v-for="feature in tableFeatures">
						<tr class="grid grid-cols-3 md:table-row">
							<td class="col-span-3 mb-2 font-bold md:mb-0 md:font-normal">{{ feature.feature }}</td>
							<td class="col-start-1">
								<div class="flex flex-col items-start gap-1 md:gap-0 md:flex-row md:justify-center">
									<div class="md:hidden">Basic</div>
									<span v-if="feature.basic">
										<img src="/images/pricing/desktop/check.svg" alt="check" />
									</span>
								</div>
							</td>
							<td class="col-start-2">
								<div class="flex flex-col items-start gap-1 md:gap-0 md:flex-row md:justify-center">
									<div class="md:hidden">Pro</div>
									<span v-if="feature.pro">
										<img src="/images/pricing/desktop/check.svg" alt="check" />
									</span>
								</div>
							</td>
							<td class="col-start-3">
								<div class="flex flex-col items-start gap-1 md:gap-0 md:flex-row md:justify-center">
									<div class="md:hidden">Business</div>
									<span v-if="feature.business">
										<img src="/images/pricing/desktop/check.svg" alt="check" />
									</span>
								</div>
							</td>
						</tr>
					</template>
				</tbody>
			</table>
		</div>
	</div>
</template>

<style scoped>
th {
	@apply py-4 text-center;
}
th:first-child {
	@apply text-left;
}
th:nth-child(2),
th:nth-child(3),
th:nth-child(4) {
	@apply w-[150px];
}
td {
	@apply md:py-4;
}
th:first-child,
td:first-child {
	@apply md:pl-4;
}
td span {
	@apply flex items-center justify-center;
}
tr {
	@apply border-b border-gray-300 dark:border-gray-500 py-4;
}
thead tr {
	@apply border-gray-600 dark:border-gray-800;
}
</style>
