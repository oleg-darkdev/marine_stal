<script>
	import { CountUp } from 'countup.js';
	import { onMount } from 'svelte';

	onMount(() => {
		const workersCountUp = new CountUp('workers', 50, { enableScrollSpy: true, duration: 6 }),
			hoursCountUp = new CountUp('hours', 900000, { enableScrollSpy: true, duration: 8 }),
			partnersCountUp = new CountUp('partners', 12, { enableScrollSpy: true, duration: 6 }),
			// progectsCountUp = new CountUp('progects', 9, { enableScrollSpy: true, duration: 8 }),
			experienceCountUp = new CountUp('experience', 10, { enableScrollSpy: true, duration: 13 });
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
			title: 'Czas pracy na projektach',
			id: 'hours'
		}
	];
</script>

<div
	class=" container mx-auto grid  max-w-4xl grid-cols-2 justify-center text-center lg:grid-cols-4"
>
	{#each stats as stat}
		<div class=" flex w-3/12 flex-col justify-start">
			<p id={stat.id} class="text-4xl font-bold leading-none text-white lg:text-8xl" />
			<p class="text-md sm:text-base">{stat.title}</p>
		</div>
	{/each}
</div>
