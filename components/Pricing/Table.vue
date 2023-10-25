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
	<div class="bg-white dark:bg-gray-400 py-16">
		<div class="max-w-3xl mx-auto">
            <h2
             class="text-[40px] leading-[48px] font-semibold tracking-wide text-center uppercase mb-8"
            >
                Compare
            </h2>
			<table class="uppercase text-[12px] w-full">
				<thead>
					<tr>
						<th>The Features</th>
						<th>Basic</th>
						<th>Pro</th>
						<th>Business</th>
					</tr>
				</thead>
				<tbody>
					<template v-for="feature in tableFeatures">
						<tr>
							<td>{{ feature.feature }}</td>
							<td>
								<span v-if="feature.basic">
									<img src="/images/pricing/desktop/check.svg" alt="check" />
								</span>
							</td>
							<td>
								<span v-if="feature.pro">
									<img src="/images/pricing/desktop/check.svg" alt="check" />
								</span>
							</td>
							<td>
								<span v-if="feature.business">
									<img src="/images/pricing/desktop/check.svg" alt="check" />
								</span>
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
	@apply py-4;
}
th:first-child,
td:first-child {
	@apply pl-4;
}
td span {
	@apply flex items-center justify-center;
}
tr {
	@apply border-b border-gray-300 dark:border-gray-500;
}
thead tr {
    @apply border-gray-600 dark:border-gray-800;
}
</style>
