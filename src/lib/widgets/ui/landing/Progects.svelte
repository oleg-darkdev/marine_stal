<script>
	export let progects;
</script>

<div class="relative mx-auto  mb-8 w-full max-w-7xl items-center px-5 md:px-12 lg:px-16 ">
	<div class="mx-auto flex w-full text-left">
		<div class="relative mx-auto inline-flex items-center align-middle">
			<div class="text-center">
				<h1
					class="max-w-6xl text-2xl font-bold leading-none tracking-tighter text-white md:text-5xl lg:max-w-2xl lg:text-6xl"
				>
					Nasze projekty w ciągu ostatnich dwóch lat
				</h1>
				<p class="mx-auto mt-4 max-w-xl text-base leading-relaxed text-neutral-100">
					Zakres prac obejmuje prefabrykacje sekcji jak i budowę całych jednostek. Wykonujemy też
					prefabrykację rur oraz prace ślusarskie wraz z montażem na jednostkach.
				</p>
			</div>
		</div>
	</div>
</div>

<div class="container mx-auto grid gap-4 lg:pb-24 md:pb-24  md:px-6 lg:w-8/12 lg:grid-cols-3 ">
	<!-- grid gap-x-6 lg:grid-cols-3 lg:gap-x-12 -->
	{#each progects as progect}
		<a class="mb-2 " href="/portfolio/{progect.link}" target="_blank">
			<div
				class="mb-6  rounded-2xl shadow-2xl   transition delay-150 duration-300 ease-in-out md:w-80 md:hover:-translate-x-16 md:hover:-translate-y-8 lg:mb-0"
			>
				<div class="relative  bg-cover bg-no-repeat">
					<img
						src="/images/portfolio/{progect.link}/{progect.img}"
						alt={progect.title}
						class="w-full rounded-t-xl object-cover object-center h-48 lg:h-64"
					/>
					<div
						class="absolute top-0 right-0 bottom-0 left-0 h-full w-full bg-[hsla(0,0%,98.4%,0.2)] bg-fixed opacity-0 transition duration-300 ease-in-out hover:opacity-100"
					/>
					<svg
						class="absolute left-0 bottom-0 fill-blue-500 text-white"
						xmlns="http://www.w3.org/2000/svg"
						viewBox="0 0 1440 320"
					>
						<path
							d="M0,288L48,272C96,256,192,224,288,197.3C384,171,480,149,576,165.3C672,181,768,235,864,250.7C960,267,1056,245,1152,250.7C1248,256,1344,288,1392,304L1440,320L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"
						/>
					</svg>
				</div>
				<div class="-mt-2 rounded-b-2xl bg-blue-500 px-4 pt-2 pb-6 text-white">
					<h4 class="text-2xl font-semibold ">
						<span class="">{progect.title}</span>
					</h4>
					<p class="leading-relax mt-4 text-base font-normal ">
						{progect.shortDesc}
					</p>
				</div>
			</div>
			<!-- <div class="flex w-full">
				<div
					class="h-90 relative m-1 flex transform flex-col items-start rounded-xl bg-white shadow-2xl transition delay-150 duration-300 ease-in-out md:-ml-16 md:w-80 md:hover:-translate-x-16 md:hover:-translate-y-8"
				>
					<img
						class="w-full rounded-t-xl object-cover object-center md:h-36 lg:h-48"
						src="/images/portfolio/{progect.link}/{progect.img}"
						alt={progect.title}
					/>
					<div class="px-4 py-6">
						<h4 class="mt-4 text-2xl font-semibold text-neutral-600">
							<span class="">{progect.title}</span>
						</h4>
						<p class="leading-relax mt-4 text-base font-normal text-gray-500">
							{progect.shortDesc}
						</p>
					</div>
				</div>
			</div> -->
		</a>
	{/each}
</div>
