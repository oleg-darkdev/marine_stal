<script>
	const stats = [
		{
			title: 'Lorem impsum',
			text: '50+',
			id: 1
		},
		{
			title: 'Lorem impsum',
			text: '90000',
			id: 2
		},
		{
			title: 'Lorem impsum',
			text: '130+',
			id: 3
		},
		{
			title: 'Lorem impsum',
			text: '12',
			id: 4
		},
		{
			title: 'Lorem impsum',
			text: '7',
			id: 5
		},
		{
			title: 'Lorem impsum',
			text: '8+',
			id: 6
		}
	];
</script>

<div
	class=" container mx-auto grid  max-w-4xl grid-cols-2 justify-center gap-4 text-center lg:grid-cols-3"
>
	{#each stats as stat}
		<div class="m-2 flex flex-col justify-start">
			<p class="text-4xl font-bold leading-none text-white lg:text-8xl">{stat.text}</p>
			<p class="text-md sm:text-base">{stat.title}</p>
		</div>
	{/each}
</div>
