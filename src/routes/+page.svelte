<script>
	import {
		About,
		Partners,
		Slider,
		Header,
		Progects,
		Stats,
		Gallery,
		Contact
	} from '../lib/widgets/';
	import { BottomWave } from '../lib/shared';
	import { portfolio, partners } from '../lib/shared';
</script>

<svelte:head>
	<title>Statki | Marine stal | Gdańsk</title>
</svelte:head>

<Header />

<video
	class="video-hero z-1 rounded-lg"
	poster="./images/gallery/1.jpg"
	playsinline
	autoplay
	muted
	loop
>
	<source src="/videos/hero_short_mini.mp4" />
</video>

<section class=" z-10 min-h-screen">
	<div class="mix-blend-mode  flex w-full flex-col items-center justify-center text-center">
		<h2
			class="max-w-5xl text-center text-4xl font-bold leading-none tracking-tighter text-neutral-50 md:text-5xl lg:max-w-7xl lg:text-6xl"
		>
			Witamy w <br class="hidden lg:block" /><span class="font-black text-white "
				>Marine Stal Sp. z o. o.</span
			>
		</h2>
	</div>
</section>

<main class="-mt-14 overflow-hidden bg-primary ">
	<div class="hero flex min-h-screen flex-col overflow-hidden">
		<h1
			style="right: 11%"
			class="absolute top-10 max-w-5xl text-2xl font-bold leading-none tracking-tighter text-white md:text-5xl lg:max-w-7xl lg:text-6xl"
		>
			Marine Stal Sp. z o. o.
		</h1>
		<svg class="wave-top " width="100" viewBox="0 0 2400 500">
			<path
				fill-rule="evenodd"
				clip-rule="evenodd"
				d="M0 108.306L50 114.323C100 120.34 200 132.374 300 168.476C400 204.578 500 264.749 600 246.698C700 228.647 800 132.374 900 108.306C1000 84.2382 1100 132.374 1150 156.442L1200 180.51V-8.5451e-06H1150C1100 -8.5451e-06 1000 -8.5451e-06 900 -8.5451e-06C800 -8.5451e-06 700 -8.5451e-06 600 -8.5451e-06C500 -8.5451e-06 400 -8.5451e-06 300 -8.5451e-06C200 -8.5451e-06 100 -8.5451e-06 50 -8.5451e-06H0V108.306Z"
				fill="#0099FF"
			/>
		</svg>
		<a name="o-nas" />
		<About />
	</div>

	<section class="bg-primary">
		<BottomWave bgColor="bg-primary" fill="#00008b" />

		<Stats />

		<!-- <BottomWave bgColor="bg-white" fill="#0099FF" /> -->
		<svg width="100" class="w-full  bg-white" viewBox="0 0 1440 320"
			><path
				fill="#0099ff"
				fill-opacity="1"
				d="M0,160L48,181.3C96,203,192,245,288,256C384,267,480,245,576,224C672,203,768,181,864,181.3C960,181,1056,203,1152,202.7C1248,203,1344,181,1392,170.7L1440,160L1440,0L1392,0C1344,0,1248,0,1152,0C1056,0,960,0,864,0C768,0,672,0,576,0C480,0,384,0,288,0C192,0,96,0,48,0L0,0Z"
			/></svg
		>
	</section>

	<section class=" w-full bg-white">
		<!-- <BottomWave bgColor="bg-primary" fill="#fff" /> -->
		<a name="partnerzy" />

		<Partners {partners} />
		<BottomWave bgColor="bg-secondary" fill="#fff" />
	</section>

	<section class=" w-full bg-secondary ">
		<a name="projekty" />

		<Progects progects={portfolio} />
	</section>

	<section>
		<svg width="100" class="-mt-20 w-full" viewBox="0 0 1440 320"
			><path
				fill="#00008b"
				fill-opacity="1"
				d="M0,160L48,181.3C96,203,192,245,288,256C384,267,480,245,576,224C672,203,768,181,864,181.3C960,181,1056,203,1152,202.7C1248,203,1344,181,1392,170.7L1440,160L1440,0L1392,0C1344,0,1248,0,1152,0C1056,0,960,0,864,0C768,0,672,0,576,0C480,0,384,0,288,0C192,0,96,0,48,0L0,0Z"
			/></svg
		>
		<a name="portfolio" />

		<Slider {portfolio} />
	</section>
	<!-- <BottomWave bgColor="bg-secondary" fill="#fff" /> -->

	<a name="kontakty" />

	<section class="grid  grid-cols-2 gap-4 py-12 px-4 md:grid-cols-4">
		<Gallery />
	</section>

	<!-- <Contact /> -->
</main>

<!-- </div> -->
<style>
	.hero {
		position: relative;
		display: flex;
		justify-content: center;
		align-items: center;
		background-color: darkblue;
		text-align: center;
		color: white;
		box-sizing: border-box;
		padding: 1rem;
	}

	.wave-top {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
	}

	.justify-content {
		justify-content: space-between;
	}

	.mix-blend-mode {
		mix-blend-mode: screen;
	}
	.video-hero {
		position: absolute;
		top: 26%;
		left: 0;
		width: 100%;
		height: 100%;
		object-fit: cover;
		object-position: center;
	}
</style>
