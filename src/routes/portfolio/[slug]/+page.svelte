<script>
	import { page } from '$app/stores';
	import { portfolio, BottomWave } from '../../../lib/shared';
	import { PortfolioStep } from '../../../lib/entities/';
	import { ProgectGallery, Progects, BreadCrumbs } from '../../../lib/widgets';

	const progectData = portfolio.find((u) => u.link == $page.params.slug);
</script>

<svelte:head>
	<title>Statki | Marine stal | Gdańsk</title>
</svelte:head>

<BreadCrumbs link={$page.params.slug} />
<main class="bg-base">
	<section
		class="h-[32rem] w-full bg-cover bg-center"
		style="background-image: url('/images/portfolio/{progectData.link}/{progectData.banner}');"
	>
		<div class="flex h-full w-full items-center justify-center bg-blue-600/40">
			<div class="text-center">
				<h1
					class="  mb-10 text-4xl font-black leading-none tracking-tighter text-white md:text-5xl  lg:text-6xl"
				>
					Projekt: <span class="text-blue-300">{progectData.title}</span>
				</h1>
				<a
					href="#about"
					class=" w-full transform rounded-md bg-white px-8 py-4 text-lg font-medium capitalize text-blue-600 transition-colors duration-300 hover:bg-blue-500 hover:text-white focus:bg-blue-500 focus:outline-none lg:w-auto"
					>Więcej informacji</a
				>
			</div>
		</div>
	</section>

	<section class=" mx-auto w-full lg:px-5 md:px-5 px-1 py-12  ">
		<div class="prose-2xl prose mx-auto mb-2 flex w-full flex-col text-left">
			<div class="mb-5 border-b border-gray-200">
				<div class="-mt-2 flex flex-col text-gray-500">
					<h5 class="text-lg">
						Data realizacji: <span class="font-black text-blue-500">12-03-2021</span>
					</h5>
					<div class="-mt-2 text-lg">
						<p class=" ">
							Wykonawca: <span class="text-2xl font-bold">Marine Stal Sp. z o. o.</span>
						</p>
						<p class="-mt-6  ">
							Klient: <span class="text-2xl font-bold">{progectData.client}</span>
						</p>
					</div>
					<a name="about" />
				</div>
			</div>
			<!-- max-w-6xl text-2xl font-bold leading-none tracking-tighter text-white md:text-5xl lg:max-w-2xl lg:text-6xl -->
			<h1 class="font-bold leading-none tracking-tighter text-gray-600">{progectData.title}</h1>
			{#each progectData.fullDesc[0] as desc}
				<p class="mt-1 text-gray-500">{desc}</p>
			{/each}

			<PortfolioStep step={progectData.steps[0]} />

			{#each progectData.fullDesc[1] as desc}
				<p class="mt-1 text-gray-500">{desc}</p>
			{/each}

			<PortfolioStep step={progectData.steps[1]} />

			{#each progectData.fullDesc[2] as desc}
				<p class="mt-1 text-gray-500">{desc}</p>
			{/each}

			<PortfolioStep step={progectData.steps[2]} />

			<!-- <h2>"Focus on the customer journey"</h2>
		<p>
			If you could do that, that would be great this is a no-brainer, or Q1 regroup. Groom the
			backlog what do you feel you would bring to the table if you were hired for this position.
			Back of the net. Scope creep can you slack it to me? shotgun approach build on a culture of
			contribution and inclusion please advise soonest.
		</p>
		<h3>Is a no-brainer, or Q1 regroup.</h3>
		<p>
			Gain traction make it more corporate please we need to harvest synergy effects not enough
			bandwidth, and we want to empower the team with the right tools and guidance to uplevel our
			craft and build better nor low-hanging fruit the right info at the right time to the right
			people.
		</p> -->
		</div>
	</section>

	<ProgectGallery path={progectData.link} images={progectData.gallery} />

	<BottomWave bgColor="bg-secondary" fill="#fff" />

	<section class=" w-full bg-secondary lg:py-0 py-8 lg:px-0 px-6">
		<a name="projekty" />

		<Progects progects={portfolio} />
	</section>
	<svg width="100" class="hidden-sm -mt-20 w-full" viewBox="0 0 1440 320"
		><path
			fill="#00008b"
			fill-opacity="1"
			d="M0,160L48,181.3C96,203,192,245,288,256C384,267,480,245,576,224C672,203,768,181,864,181.3C960,181,1056,203,1152,202.7C1248,203,1344,181,1392,170.7L1440,160L1440,0L1392,0C1344,0,1248,0,1152,0C1056,0,960,0,864,0C768,0,672,0,576,0C480,0,384,0,288,0C192,0,96,0,48,0L0,0Z"
		/></svg
	>
</main>

<style>
	@media (max-width: 768px) {
		:global(.hidden-sm) {
			display: none;
		}
	}
</style>
