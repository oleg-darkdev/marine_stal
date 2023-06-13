<script>
	import { onMount } from 'svelte';

	let photos = [];

	onMount(() => {
		document.addEventListener('DOMContentLoaded', function () {
			var lazyVideos = [].slice.call(document.querySelectorAll('video.lazy'));

			console.log(lazyVideos);
			if ('IntersectionObserver' in window) {
				var lazyVideoObserver = new IntersectionObserver(function (entries, observer) {
					entries.forEach(function (video) {
						if (video.isIntersecting) {
							for (var source in video.target.children) {
								var videoSource = video.target.children[source];
								if (typeof videoSource.tagName === 'string' && videoSource.tagName === 'SOURCE') {
									videoSource.src = videoSource.dataset.src;
								}
							}

							video.target.load();
							video.target.classList.remove('lazy');
							lazyVideoObserver.unobserve(video.target);
						}
					});
				});

				lazyVideos.forEach(function (lazyVideo) {
					lazyVideoObserver.observe(lazyVideo);
				});
			}
		});
	});

	const features = [
		`Wykonujemy prefabrykację rur.`,
		`Prace ślusarskie wraz z montażem na jednostkach`,
		`kilka lat wykonujemy prace dla Mostostalu Chojnice Sp.z.o.o. sp.k.`

		// `Współpracujemy ze stoczniami:`
	];

</script>

<div class="mx-auto px-4 py-12 sm:px-6 md:px-12 lg:px-24 lg:py-24 2xl:max-w-7xl 2xl:px-12">
	<div class="mx-auto flex flex-wrap items-center 2xl:max-w-7xl">
		<div
			class="mt-40 mb-16 flex flex-col items-start text-left md:mb-0 lg:w-1/2 lg:flex-grow lg:pr-24"
		>
			<span class="mb-4 text-xs font-bold uppercase tracking-widest text-blue-600"> O nas </span>
			<h1
				class="mb-6 text-4xl text-base font-bold leading-none tracking-tighter md:text-7xl lg:text-5xl"
			>
				Medium length display headline.
			</h1>
			<p class="mb-6 text-left text-base text-base leading-relaxed">
				Firma wykonuje prace montersko-spawalnicze konstrukcji stalowych i aluminiowych. Zakres prac
				obejmuje prefabrykacje sekcji jak i budowę całych jednostek.
			</p>
			<div class="space-y-2">
				{#each features as feature}
					<p class="-mx-2 flex items-center text-base">
						<svg
							xmlns="http://www.w3.org/2000/svg"
							class="mx-2 h-6 w-6 text-blue-500"
							fill="none"
							viewBox="0 0 24 24"
							stroke="currentColor"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								stroke-width="2"
								d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"
							/>
						</svg>

						<span class="mx-2"> {feature}</span>
					</p>
				{/each}
			</div>
		</div>
		<div class=" w-full rounded-xl lg:w-5/6 lg:max-w-lg xl:mt-0">
			<div>
				<div class="relative w-full max-w-lg">
					<!-- <div
						class="animate-blob absolute -left-4 top-0 h-72 w-72 rounded-full bg-violet-300 opacity-70 mix-blend-multiply blur-xl filter"
					/> -->

					<!-- <div
						class="animate-blob animation-delay-4000 absolute -bottom-24 right-20 h-72 w-72 rounded-full bg-fuchsia-300 opacity-70 mix-blend-multiply blur-xl filter"
					/> -->
					<div class="relative">
						<video
							class="mx-auto -mt-40  rounded-lg object-cover object-center shadow-2xl"
							src="https://web.archive.org/web/20230607110206/https://video.wixstatic.com/video/c84a50_ea41e4766a644bae811b5b5bac265d5f/720p/mp4/file.mp4"
							autoplay
						/>
						<!-- preload="none" -->

						<!-- <img
								class="mx-auto -mt-40 rounded-lg object-cover object-center shadow-2xl"
								alt="hero"
								async
								src="https://www.globalmarineinsurance.com/wp-content/uploads/2018/06/photo-copy.jpg"
							/> -->
					</div>
				</div>
			</div>
		</div>
	</div>
</div>

<!--
<div
	class="container mx-auto flex flex-col space-y-6 px-6 py-10 lg:h-[32rem] lg:flex-row lg:items-center lg:py-16"
>
	<div class="w-full lg:w-1/2">
		<div class="lg:max-w-lg">
			<h1 class="text-3xl font-semibold tracking-wide text-gray-800 dark:text-white lg:text-4xl">
				Find your premium new glasses exported from US
			</h1>
			<p class="mt-4 text-gray-600 dark:text-gray-300">
				We work with the best remunated glasses dealers in US to find your new glasses.
			</p>
			<div class="mt-8 grid gap-6 sm:grid-cols-2">
				<div class="-px-3 flex items-center text-gray-800 dark:text-gray-200">
					<svg
						class="mx-3 h-5 w-5"
						xmlns="http://www.w3.org/2000/svg"
						fill="none"
						viewBox="0 0 24 24"
						stroke="currentColor"
					>
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d="M5 13l4 4L19 7"
						/>
					</svg>

					<span class="mx-3">Premium selection</span>
				</div>

				<div class="-px-3 flex items-center text-gray-800 dark:text-gray-200">
					<svg
						class="mx-3 h-5 w-5"
						xmlns="http://www.w3.org/2000/svg"
						fill="none"
						viewBox="0 0 24 24"
						stroke="currentColor"
					>
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d="M5 13l4 4L19 7"
						/>
					</svg>

					<span class="mx-3">Insurance</span>
				</div>

				<div class="-px-3 flex items-center text-gray-800 dark:text-gray-200">
					<svg
						class="mx-3 h-5 w-5"
						xmlns="http://www.w3.org/2000/svg"
						fill="none"
						viewBox="0 0 24 24"
						stroke="currentColor"
					>
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d="M5 13l4 4L19 7"
						/>
					</svg>

					<span class="mx-3">All legal documents</span>
				</div>

				<div class="-px-3 flex items-center text-gray-800 dark:text-gray-200">
					<svg
						class="mx-3 h-5 w-5"
						xmlns="http://www.w3.org/2000/svg"
						fill="none"
						viewBox="0 0 24 24"
						stroke="currentColor"
					>
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d="M5 13l4 4L19 7"
						/>
					</svg>

					<span class="mx-3">From US glasses dealers</span>
				</div>

				<div class="-px-3 flex items-center text-gray-800 dark:text-gray-200">
					<svg
						class="mx-3 h-5 w-5"
						xmlns="http://www.w3.org/2000/svg"
						fill="none"
						viewBox="0 0 24 24"
						stroke="currentColor"
					>
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d="M5 13l4 4L19 7"
						/>
					</svg>

					<span class="mx-3">Payment Security</span>
				</div>

				<div class="-px-3 flex items-center text-gray-800 dark:text-gray-200">
					<svg
						class="mx-3 h-5 w-5"
						xmlns="http://www.w3.org/2000/svg"
						fill="none"
						viewBox="0 0 24 24"
						stroke="currentColor"
					>
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d="M5 13l4 4L19 7"
						/>
					</svg>

					<span class="mx-3">Fast shipping (+ Express)</span>
				</div>
			</div>
		</div>
	</div>

	<div class="flex h-96 w-full items-center justify-center lg:w-1/2">
		<img
			class="h-full w-full max-w-2xl rounded-md object-cover"
			src="https://images.unsplash.com/photo-1555181126-cf46a03827c0?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80"
			alt="glasses photo"
		/>
	</div>
</div> -->
