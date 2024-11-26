<script>
	let products = $state([
		{
			id: 1,
			name: 'PRO',
			price: 7.27,
			advantages: ['cool']
		},
		{
			id: 2,
			name: 'LEGEND',
			price: 727,
			advantages: ['idk']
		},
		{
			id: 3,
			name: 'Hacker',
			price: 72.7,
			advantages: ['i forgor']
		}
	]);
</script>

<div class="container mx-auto p-4">
	<h1 class="mb-6 text-center text-2xl font-bold text-white">Deeka shop</h1>

	<div class="grid grid-cols-1 gap-6 sm:grid-cols-2 lg:grid-cols-3">
		{#each products as product}
			<div
				class="flex flex-col rounded-lg border border-white border-opacity-40 bg-white bg-opacity-10 shadow-lg"
			>
				<div class="rounded-t-lg bg-white bg-opacity-20 p-4">
					<h2 class="text-center text-xl font-semibold text-white">{product.name}</h2>
					<p class="text-center text-lg font-bold text-green-300">${product.price.toFixed(2)}</p>
				</div>
				<div class="flex-grow p-4 text-white">
					<h3 class="mb-2 font-medium">Advantages:</h3>
					<ul class="list-inside list-disc space-y-1">
						{#each product.advantages as advantage}
							<li>{advantage}</li>
						{/each}
					</ul>
				</div>
				<div class="p-4">
					<button class="w-full rounded-lg bg-blue-600 p-2 text-white"> Purchase </button>
				</div>
			</div>
		{/each}
	</div>
</div>
