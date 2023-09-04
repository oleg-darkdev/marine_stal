<script>
	import { CountUp } from 'countup.js';
	import { onMount } from 'svelte';

	onMount(() => {
		const workersCountUp = new CountUp('workers', 50, { enableScrollSpy: true, duration: 6 }),
			partnersCountUp = new CountUp('partners', 12, { enableScrollSpy: true, duration: 6 }),
			progectsCountUp = new CountUp('progects', 9, { enableScrollSpy: true, duration: 8 }),
			experienceCountUp = new CountUp('experience', 10, { enableScrollSpy: true, duration: 13 }),
			metresCountUp = new CountUp('metres', 400, { enableScrollSpy: true, duration: 6 }),
			hoursCountUp = new CountUp('hours', 900000, { enableScrollSpy: true, duration: 14 });
	});

	const stats = [
		{
			title: 'Lat na rynku',
			id: 'experience'
		},
		{
			title: 'Pracowników w firmie',
			id: 'workers'
		},
		{
			title: 'Firmy partnerskie',
			id: 'partners'
		},
		{
			title: 'Zrealizowane projekty',
			id: 'progects'
		},

		// {
		// 	title: 'Czas pracy godzin',
		// 	id: 'hours'
		// },
		// {
		// 	title: 'Pomiar terytoriuma firmy',
		// 	id: 'metres'
		// }
	];
</script>

<div
	class=" container mx-auto grid  max-w-6xl grid-cols-2 justify-center gap-4 text-center lg:grid-cols-3"
>
	{#each stats as stat}
		<div class=" flex  flex-col items-center justify-center">
			<p id={stat.id} class="text-6xl font-bold leading-none text-white lg:text-8xl" />
			<p class="text-md min-w-md text-center text-white ">{stat.title}</p>
		</div>
	{/each}
</div>
