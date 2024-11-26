<script>
	let products = $state([
		{
			id: 1,
			name: 'VIP Rank',
			price: 9.99,
			advantages: ['Access to exclusive VIP areas', 'Special chat color', 'Daily bonus rewards']
		},
		{
			id: 2,
			name: 'MVP Rank',
			price: 19.99,
			advantages: ['All VIP perks', 'Exclusive pets', 'Fly mode in lobbies']
		},
		{
			id: 3,
			name: 'Elite Rank',
			price: 29.99,
			advantages: ['All MVP perks', 'Custom particle effects', 'Priority in server queues']
		}
	]);
</script>

<div class="container mx-auto p-4">
	<h1 class="mb-6 text-center text-2xl font-bold">Minecraft Ranks Shop</h1>

	<div class="grid grid-cols-1 gap-6 sm:grid-cols-2 lg:grid-cols-3">
		{#each products as product}
			<div class="flex flex-col rounded-lg border border-gray-300 shadow-lg">
				<div class="rounded-t-lg bg-blue-50 p-4 text-center">
					<h2 class="text-xl font-semibold text-blue-800">{product.name}</h2>
					<p class="text-lg font-bold text-green-600">${product.price.toFixed(2)}</p>
				</div>
				<div class="flex-grow p-4">
					<h3 class="mb-2 font-medium text-gray-800">Advantages:</h3>
					<ul class="list-inside list-disc space-y-1 text-gray-600">
						{#each product.advantages as advantage}
							<li>{advantage}</li>
						{/each}
					</ul>
				</div>
				<div class="p-4">
					<button class="w-full rounded-md bg-blue-500 p-2 text-white hover:bg-blue-600">
						Purchase
					</button>
				</div>
			</div>
		{/each}
	</div>
</div>
