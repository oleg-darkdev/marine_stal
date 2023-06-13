<script>
	import { About, Partners, Slider, Header, Progects, Stats, Gallery } from '../lib/widgets/';
	import { BottomWave } from '../lib/shared';
	import { portfolio, partners } from '../lib/shared';

	// const wave1 =
	// 		'M0,64L17.1,101.3C34.3,139,69,213,103,240C137.1,267,171,245,206,224C240,203,274,181,309,165.3C342.9,900,377,139,411,122.7C445.7,107,480,85,514,96C548.6,107,583,149,617,192C651.4,235,686,277,720,272C754.3,267,789,213,823,197.3C857.1,181,891,203,926,192C960,181,994,139,1029,106.7C1062.9,75,1097,53,1131,64C1165.7,75,1200,117,1234,144C1268.6,171,1303,181,1337,154.7C1371.4,128,1406,64,1423,32L1440,0L1440,320L1422.9,320C1405.7,320,1371,320,1337,320C1302.9,320,1269,320,1234,320C1200,320,1166,320,1131,320C1097.1,320,1063,320,1029,320C994.3,320,960,320,926,320C891.4,320,857,320,823,320C788.6,320,754,320,720,320C685.7,320,651,320,617,320C582.9,320,549,320,514,320C480,320,446,320,411,320C377.1,320,343,320,309,320C274.3,320,240,320,206,320C171.4,320,137,320,103,320C68.6,320,34,320,17,320L0,320Z',
	// 	wave2 =
	// 		'M0 250L50 244.048C100 238.095 200 226.19 300 226.19C400 226.19 500 238.095 600 232.143C700 226.19 800 202.381 900 196.429C1000 190.476 1100 202.381 1150 208.333L1200 214.286V0H1150C1100 0 1000 0 900 0C800 0 700 0 600 0C500 0 400 0 300 0C200 0 100 0 50 0H0V250Z',
	// 	wave3 =
	// 		'M0 250L50 238.095C100 226.19 200 202.381 300 166.667C400 130.952 500 83.3333 600 101.19C700 119.048 800 202.381 900 214.286C1000 226.19 1100 166.667 1150 136.905L1200 107.143V0H1150C1100 0 1000 0 900 0C800 0 700 0 600 0C500 0 400 0 300 0C200 0 100 0 50 0H0V250Z',
	// 	wave4 =
	// 		'M0 125L50 111.111C100 97.2222 200 69.4444 300 97.2222C400 125 500 208.333 600 236.111C700 263.889 800 236.111 900 229.167C1000 222.222 1100 236.111 1150 243.056L1200 250V0H1150C1100 0 1000 0 900 0C800 0 700 0 600 0C500 0 400 0 300 0C200 0 100 0 50 0H0V125Z';
</script>

<svelte:head>
	<title>Statki | Marine stal | Gdańsk</title>
</svelte:head>

<Header />
<main class="overflow-hidden bg-primary  ">
	<!-- <div class="flex-1 overflow-y-scroll "> -->
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

	<!-- Container for demo purpose -->
	<!-- Section: Design Block -->

	<!-- <section class="-mt-20 mb-32 text-center">
		<div class=" md:px-12">
			<div class="container mx-auto xl:px-32">
				<div class="grid items-center lg:grid-cols-2">
					<div class="mb-12 md:mt-12 lg:mt-0 lg:mb-0">
						<div
							class="relative z-[1] block rounded-lg bg-[hsla(0,0%,100%,0.55)] px-6 py-12 shadow-[0_2px_15px_-3px_rgba(0,0,0,0.07),0_10px_20px_-2px_rgba(0,0,0,0.04)] backdrop-blur-[30px] dark:bg-[hsla(0,0%,5%,0.7)] dark:shadow-black/20 md:px-12 lg:-mr-14"
						>
							<h2 class="mb-12 text-3xl font-bold">Contact us</h2>
							<form>
								<div class="relative mb-6" data-te-input-wrapper-init>
									<input
										type="text"
										class="peer block min-h-[auto] w-full rounded border-0 bg-transparent py-[0.32rem] px-3 leading-[1.6] outline-none transition-all duration-200 ease-linear focus:placeholder:opacity-100 peer-focus:text-primary data-[te-input-state-active]:placeholder:opacity-100 motion-reduce:transition-none dark:text-neutral-200 dark:placeholder:text-neutral-200 dark:peer-focus:text-primary [&:not([data-te-input-placeholder-active])]:placeholder:opacity-0"
										id="exampleInput90"
										placeholder="Name"
									/>
									<label
										class="pointer-events-none absolute top-0 left-3 mb-0 max-w-[90%] origin-[0_0] truncate pt-[0.37rem] leading-[1.6] text-neutral-500 transition-all duration-200 ease-out peer-focus:-translate-y-[0.9rem] peer-focus:scale-[0.8] peer-focus:text-primary peer-data-[te-input-state-active]:-translate-y-[0.9rem] peer-data-[te-input-state-active]:scale-[0.8] motion-reduce:transition-none dark:text-neutral-200 dark:peer-focus:text-primary"
										for="exampleInput90"
										>Name
									</label>
								</div>
								<div class="relative mb-6" data-te-input-wrapper-init>
									<input
										type="email"
										class="peer block min-h-[auto] w-full rounded border-0 bg-transparent py-[0.32rem] px-3 leading-[1.6] outline-none transition-all duration-200 ease-linear focus:placeholder:opacity-100 peer-focus:text-primary data-[te-input-state-active]:placeholder:opacity-100 motion-reduce:transition-none dark:text-neutral-200 dark:placeholder:text-neutral-200 dark:peer-focus:text-primary [&:not([data-te-input-placeholder-active])]:placeholder:opacity-0"
										id="exampleInput91"
										placeholder="Email address"
									/>
									<label
										class="pointer-events-none absolute top-0 left-3 mb-0 max-w-[90%] origin-[0_0] truncate pt-[0.37rem] leading-[1.6] text-neutral-500 transition-all duration-200 ease-out peer-focus:-translate-y-[0.9rem] peer-focus:scale-[0.8] peer-focus:text-primary peer-data-[te-input-state-active]:-translate-y-[0.9rem] peer-data-[te-input-state-active]:scale-[0.8] motion-reduce:transition-none dark:text-neutral-200 dark:peer-focus:text-primary"
										for="exampleInput91"
										>Email address
									</label>
								</div>
								<div class="relative mb-6" data-te-input-wrapper-init>
									<textarea
										class="peer block min-h-[auto] w-full rounded border-0 bg-transparent py-[0.32rem] px-3 leading-[1.6] outline-none transition-all duration-200 ease-linear focus:placeholder:opacity-100 data-[te-input-state-active]:placeholder:opacity-100 motion-reduce:transition-none dark:text-neutral-200 dark:placeholder:text-neutral-200 [&:not([data-te-input-placeholder-active])]:placeholder:opacity-0"
										id="exampleFormControlTextarea1"
										rows="3"
										placeholder="Your message"
									/>
									<label
										for="exampleFormControlTextarea1"
										class="pointer-events-none absolute top-0 left-3 mb-0 max-w-[90%] origin-[0_0] truncate pt-[0.37rem] leading-[1.6] text-neutral-500 transition-all duration-200 ease-out peer-focus:-translate-y-[0.9rem] peer-focus:scale-[0.8] peer-focus:text-primary peer-data-[te-input-state-active]:-translate-y-[0.9rem] peer-data-[te-input-state-active]:scale-[0.8] motion-reduce:transition-none dark:text-neutral-200 dark:peer-focus:text-primary"
										>Message</label
									>
								</div>
								<div class="mb-6 inline-block min-h-[1.5rem] justify-center pl-[1.5rem] md:flex">
									<input
										class="relative float-left mt-[0.15rem] mr-[6px] -ml-[1.5rem] h-[1.125rem] w-[1.125rem] appearance-none rounded-[0.25rem] border-[0.125rem] border-solid border-neutral-300 outline-none before:pointer-events-none before:absolute before:h-[0.875rem] before:w-[0.875rem] before:scale-0 before:rounded-full before:bg-transparent before:opacity-0 before:shadow-[0px_0px_0px_13px_transparent] before:content-[''] checked:border-primary checked:bg-primary checked:before:opacity-[0.16] checked:after:absolute checked:after:ml-[0.25rem] checked:after:-mt-px checked:after:block checked:after:h-[0.8125rem] checked:after:w-[0.375rem] checked:after:rotate-45 checked:after:border-[0.125rem] checked:after:border-t-0 checked:after:border-l-0 checked:after:border-solid checked:after:border-white checked:after:bg-transparent checked:after:content-[''] hover:cursor-pointer hover:before:opacity-[0.04] hover:before:shadow-[0px_0px_0px_13px_rgba(0,0,0,0.6)] focus:shadow-none focus:transition-[border-color_0.2s] focus:before:scale-100 focus:before:opacity-[0.12] focus:before:shadow-[0px_0px_0px_13px_rgba(0,0,0,0.6)] focus:before:transition-[box-shadow_0.2s,transform_0.2s] focus:after:absolute focus:after:z-[1] focus:after:block focus:after:h-[0.875rem] focus:after:w-[0.875rem] focus:after:rounded-[0.125rem] focus:after:content-[''] checked:focus:before:scale-100 checked:focus:before:shadow-[0px_0px_0px_13px_#3b71ca] checked:focus:before:transition-[box-shadow_0.2s,transform_0.2s] checked:focus:after:ml-[0.25rem] checked:focus:after:-mt-px checked:focus:after:h-[0.8125rem] checked:focus:after:w-[0.375rem] checked:focus:after:rotate-45 checked:focus:after:rounded-none checked:focus:after:border-[0.125rem] checked:focus:after:border-t-0 checked:focus:after:border-l-0 checked:focus:after:border-solid checked:focus:after:border-white checked:focus:after:bg-transparent dark:border-neutral-600 dark:checked:border-primary dark:checked:bg-primary dark:focus:before:shadow-[0px_0px_0px_13px_rgba(255,255,255,0.4)] dark:checked:focus:before:shadow-[0px_0px_0px_13px_#3b71ca]"
										type="checkbox"
										value=""
										id="exampleCheck96"
										checked
									/>
									<label
										class="inline-block pl-[0.15rem] hover:cursor-pointer"
										for="exampleCheck96"
									>
										Send me a copy of this message
									</label>
								</div>
								<button
									type="button"
									data-te-ripple-init
									data-te-ripple-color="light"
									class="hover:bg-primary-600 focus:bg-primary-600 active:bg-primary-700 inline-block w-full rounded bg-primary px-6 pt-2.5 pb-2 text-xs font-medium uppercase leading-normal text-white shadow-[0_4px_9px_-4px_#3b71ca] transition duration-150 ease-in-out hover:shadow-[0_8px_9px_-4px_rgba(59,113,202,0.3),0_4px_18px_0_rgba(59,113,202,0.2)] focus:shadow-[0_8px_9px_-4px_rgba(59,113,202,0.3),0_4px_18px_0_rgba(59,113,202,0.2)] focus:outline-none focus:ring-0 active:shadow-[0_8px_9px_-4px_rgba(59,113,202,0.3),0_4px_18px_0_rgba(59,113,202,0.2)] dark:shadow-[0_4px_9px_-4px_rgba(59,113,202,0.5)] dark:hover:shadow-[0_8px_9px_-4px_rgba(59,113,202,0.2),0_4px_18px_0_rgba(59,113,202,0.1)] dark:focus:shadow-[0_8px_9px_-4px_rgba(59,113,202,0.2),0_4px_18px_0_rgba(59,113,202,0.1)] dark:active:shadow-[0_8px_9px_-4px_rgba(59,113,202,0.2),0_4px_18px_0_rgba(59,113,202,0.1)] lg:mb-0"
								>
									Send
								</button>
							</form>
						</div>
					</div>
					<div class="md:mb-12 lg:mb-0">
						<div class="relative h-[700px] rounded-lg shadow-lg dark:shadow-black/20">
							<iframe
								src="https://maps.google.com/maps?q=manhatan&t=&z=13&ie=UTF8&iwloc=&output=embed"
								class="absolute left-0 top-0 h-full w-full rounded-lg"
								frameborder="0"
								allowfullscreen
							/>
						</div>
					</div>
				</div>
			</div>
		</div>
	</section>
   -->
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
</style>
