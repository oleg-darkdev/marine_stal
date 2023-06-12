<script>
	import { portfolio, partners } from '../../../shared';

	const workPlaces = [
		{
			title: 'Spawacz',
			link: ''
		},
		{
			title: 'Monter elementów metalowych',
			link: ''
		},
		{
			title: 'Ślusarze',
			link: ''
		}
	];
</script>

<footer class="bg-white w-full" aria-labelledby="footer-heading">
	<!-- <h2 id="footer-heading" class="sr-only">Footer</h2> -->

	<div class="mx-auto max-w-7xl px-4 py-12 sm:px-6 lg:px-16">
		<div class="xl:grid xl:grid-cols-3 xl:gap-8">
			<div class="text-white xl:col-span-1">
				<a
					href="./"
					class="tracking-relaxed  transform text-lg font-bold tracking-tighter text-blue-600 transition duration-500 ease-in-out lg:pr-8"
				>
					Marine Stal Sp. z o. o.
				</a>
				<p class="text-medium mt-2 w-1/2 font-bold text-blue-600">dakartj@wp.pl</p>
				<p class="text-medium mt-2 w-1/2 font-bold text-blue-600">+48 502 674 091</p>
				<p class="text-medium mt-2 w-1/2 font-bold text-blue-600">Przełom 11, 80-643 Gdańsk</p>
				<p class="text-medium mt-2 w-1/2 font-bold text-gray-500">💙 Poland</p>
			</div>
			<div class="mt-12 grid grid-cols-2 gap-8 xl:col-span-2 xl:mt-0">
				<div class="md:grid md:grid-cols-2 md:gap-8">
					<div>
						<h3 class="text-sm font-bold uppercase tracking-wider text-blue-500">Oferty pracy</h3>
						<ul role="list" class="mt-4 space-y-2">
							{#each workPlaces as work}
								<li>
									<a
										href={work.link}
										target="_blank"
										class="text-base font-normal text-gray-500 hover:text-blue-600"
									>
										{work.title}
									</a>
								</li>
							{/each}
						</ul>
					</div>
					<div class="mt-12 md:mt-0">
						<h3 class="text-sm font-bold uppercase tracking-wider text-blue-500">Nasi partnerzy</h3>
						<ul role="list" class="mt-4 space-y-2">
							{#each partners as partner}
								<li>
									<a
										href={partner.link}
										target="_blank"
										class="text-base font-normal text-gray-500 hover:text-blue-600"
									>
										{partner.title}
									</a>
								</li>
							{/each}
						</ul>
					</div>
				</div>
				<div class="md:grid md:grid-cols-2 md:gap-8">
					<div>
						<h3 class="text-sm font-bold uppercase tracking-wider text-blue-500">Nasi Projekty</h3>
						<ul role="list" class="mt-4 space-y-2">
							{#each portfolio as progect}
								<li>
									<a
										href='./portfolio/{progect.link}'
										class="text-base font-normal text-gray-500 hover:text-blue-600"
									>
										{progect.title}
									</a>
								</li>
							{/each}
						</ul>
					</div>

					<div class="mt-12 md:mt-0">
						<h3 class="text-sm font-bold uppercase tracking-wider text-blue-500">Media</h3>
						<ul role="list" class="mt-4 space-y-2">
							<li>
								<a
									href="https://www.facebook.com/Marine-STAL-100547828579764/"
									class="text-base font-normal text-gray-500 hover:text-blue-600"
								>
									Facebook
								</a>
							</li>
						</ul>
					</div>
				</div>
			</div>
		</div>
	</div>
	<div class="mx-auto max-w-7xl bg-gray-50 px-4 py-12 sm:px-6 lg:px-16">
		<div class="flex flex-wrap items-baseline">
			<span class="mt-2 text-sm font-light text-gray-500">
				Copyright © 2012 - 2023
				<a
					href="https://marinestal.com"
					class="text-wickedblue mx-2 hover:text-gray-500"
					rel="noopener noreferrer">Marine Stal Sp. z o. o.</a
				>. Since 2012
			</span>
		</div>
	</div>
</footer>
