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

<div class="mx-auto grid max-w-3xl grid-cols-3 gap-y-10">
	{#each progects as progect}
		<a class="" href="/portfolio/{progect.link}">
			<div class="flex w-full">
				<div
					class="h-90 relative m-1 flex transform flex-col items-start rounded-xl bg-white shadow-2xl transition delay-150 duration-300 ease-in-out md:-ml-16 md:w-80 md:hover:-translate-x-16 md:hover:-translate-y-8"
				>
					<img
						class="w-full rounded-t-xl object-cover object-center md:h-36 lg:h-48"
						src="images/portfolio/{progect.link}/{progect.img}"
						alt="{progect.title}"
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
			</div>
		</a>
	{/each}
</div>
