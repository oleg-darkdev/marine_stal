<script>
	const links = [
		// {
		// 	title: 'Główna',
		// 	link: ''
		// },
		{
			title: 'O nas',
			link: '#o-nas'
		},
		{
			title: 'Portfolio',
			link: '#portfolio'
		},
		{
			title: 'Projekty',
			link: '#projekty'
		},
		// {
		// 	title: 'Nasi partnerzy',
		// 	link: '#partnerzy'
		// },
		{
			title: 'Kontakty',
			link: '#kontakty'
		}
	];

	let showNav = false;
</script>

<header class="z-10 w-full bg-primary py-6 ">
	<div class="flex h-40  flex-col items-center">
		<div class="flex w-full max-w-6xl flex-col items-center  ">
			<div class="justify-content flex lg:w-7/12 w-11/12  flex-row flex-wrap  ">
				<a
					href=""
					class="text-md mx-2 border-b-2 border-transparent font-medium text-white hover:text-blue-700 sm:mx-6"
				>
					marinestal.gdansk@gmail.com
				</a>
				<p
					class="text-md mx-2 border-b-2 border-transparent font-medium text-white hover:text-blue-700 sm:mx-6"
				>
					+48 502 674 091
				</p>
			</div>
			<hr class="my-4  h-1 lg:w-7/12 w-11/12 border-0 bg-blue-600 " />
		</div>

		<div class="container mx-auto flex items-center justify-between md:justify-center md:space-x-8">
			<div class="dropdown">
				<button
					title="Button"
					on:click={() => (showNav = !showNav)}
					type="button"
					class="p-4 md:hidden"
				>
					<svg
						xmlns="http://www.w3.org/2000/svg"
						fill="none"
						viewBox="0 0 24 24"
						stroke="currentColor"
						class="h-6 w-6 dark:text-gray-100"
					>
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d="M4 6h16M4 12h16M4 18h16"
						/>
					</svg>
				</button>
				<ul
					tabindex="0"
					class="menu-sm dropdown-content menu rounded-box z-[1] mt-3 w-52 bg-base-100 p-6 shadow"
				>
					{#each links as link}
						<li class="flex">
							<a
								href={link.link}
								class="mx-2 border-b-2 border-transparent text-2xl font-bold text-blue-600 hover:border-blue-500 hover:text-blue-900 sm:mx-6"
								>{link.title}</a
							>
						</li>
					{/each}
				</ul>
			</div>

			<ul class="hidden items-stretch space-x-3 md:flex">
				{#each links.slice(0, 2) as link}
					<li class="flex">
						<a
							href={link.link}
							class="mx-2 border-b-2 border-transparent text-2xl font-bold text-white hover:border-blue-500 hover:text-gray-800 sm:mx-6"
							>{link.title}</a
						>
					</li>
				{/each}
			</ul>

			<a
				rel="noopener noreferrer"
				href="#"
				aria-label="Back to homepage"
				class="flex items-center p-2"
			>
				<svg
					xmlns="http://www.w3.org/2000/svg"
					viewBox="0 0 100 50"
					fill="currentColor"
					class="h-20 w-auto text-white "
					><path
						class="cls-1"
						d="M17,30.25a.56.56,0,0,1-.45.31c-.17,0-.24-.14-.16-.31l1.44-3,4.29-8.9c1.27-2.64.15-4.78-2.49-4.78s-5.81,2.14-7.08,4.78l-7.23,15s0,0,0,0a1.56,1.56,0,0,1-1.25.83c-.16,0-.23-.14-.15-.31l.26-.55h0l9.5-19.72A11.74,11.74,0,0,0,5.37,19.8a.55.55,0,0,1-.45.3c-.17,0-.24-.13-.16-.3A12.79,12.79,0,0,1,14.3,13h0l.56,0c.17,0,.24.13.16.3l-1.26,2.61A9.4,9.4,0,0,1,20,13c2.35,0,3.62,1.51,3.35,3.61A9.67,9.67,0,0,1,30.13,13c3,0,4.23,2.42,2.8,5.39L25.44,33.92c-.66,1.38-.08,2.49,1.29,2.49.17,0,.24.14.16.31a.55.55,0,0,1-.45.3c-1.71,0-2.43-1.39-1.61-3.1l7.49-15.55c1.27-2.64.16-4.78-2.48-4.78S24,15.73,22.75,18.37l-4.28,8.9Z"
					/><path
						class="cls-1"
						d="M39,25.77l-1.12,2.32a3.07,3.07,0,0,1-2.47,1.67.94.94,0,0,1-1-1.07,4.31,4.31,0,0,1-2.61,1.07c-1.42,0-2-1.15-1.33-2.57l1.36-2.83a4.76,4.76,0,0,1,3.82-2.58,1.49,1.49,0,0,1,1.53.93l.3-.63a.54.54,0,0,1,.44-.3c.17,0,.24.14.16.3l-1.1,2.28-1.36,2.83-.44.9c-.28.6,0,1.08.55,1.08a2,2,0,0,0,1.59-1.08l1.12-2.32a.57.57,0,0,1,.44-.3C39,25.47,39,25.61,39,25.77Zm-4,1.42,1.36-2.83c.53-1.09.07-2-1-2a3.34,3.34,0,0,0-2.39,2l-1.36,2.83c-.53,1.09-.31,2,.48,2A3.65,3.65,0,0,0,34.93,27.19Z"
					/><path
						class="cls-1"
						d="M42.85,22.07a.55.55,0,0,1-.44.29,3.34,3.34,0,0,0-2.39,2l-2.21,4.58-.26.54a.53.53,0,0,1-.44.3c-.46,0-.66-.38-.43-.84l3-6.31.26-.54a.54.54,0,0,1,.44-.3.47.47,0,0,1,.53.49,3.74,3.74,0,0,1,1.75-.49C42.86,21.77,42.93,21.9,42.85,22.07Z"
					/><path
						class="cls-1"
						d="M46.39,25.77l-1,2.05a3.56,3.56,0,0,1-2.87,1.94c-1.07,0-1.52-.87-1-1.94L44,22.62l.26-.54a.54.54,0,0,1,.44-.3c.46,0,.66.38.44.84l-2.51,5.2c-.35.73-.28,1.35.16,1.35a2.49,2.49,0,0,0,2-1.35l1-2.05a.55.55,0,0,1,.44-.29C46.4,25.48,46.47,25.61,46.39,25.77Zm-1.47-5a1,1,0,0,1,.84-.56c.31,0,.45.25.3.56a1,1,0,0,1-.85.57C44.9,21.34,44.77,21.09,44.92,20.77Z"
					/><path
						class="cls-1"
						d="M53.5,25.77l-1.12,2.32a3.07,3.07,0,0,1-2.47,1.67c-.92,0-1.31-.75-.86-1.67l1.8-3.74c.52-1.09.06-2-1-2a3.3,3.3,0,0,0-2.38,2l-2.2,4.57-.26.54a.55.55,0,0,1-.45.3c-.46,0-.65-.38-.43-.84l3-6.3.26-.54a.55.55,0,0,1,.45-.3.47.47,0,0,1,.52.5,3.76,3.76,0,0,1,1.75-.5c1.42,0,2,1.16,1.33,2.57l-1.8,3.74c-.28.6,0,1.08.56,1.08a2,2,0,0,0,1.59-1.08l1.11-2.32a.55.55,0,0,1,.44-.29C53.51,25.48,53.58,25.61,53.5,25.77Z"
					/><path
						class="cls-1"
						d="M60.09,25.53a8.58,8.58,0,0,1-6.32,3.64c-.79,0-1-.89-.49-2l.13-.26h1.43a4.77,4.77,0,0,0,3.82-2.57c.68-1.42.08-2.58-1.34-2.58a4.73,4.73,0,0,0-3.81,2.58l-1.37,2.83c-.68,1.42-.08,2.57,1.34,2.57,2.56,0,5.57-1.81,7.23-4.22Zm-5.44-1.17a3.31,3.31,0,0,1,2.39-2c1.09,0,1.54.89,1,2a3.63,3.63,0,0,1-2.93,2H53.7Z"
					/><path
						class="cls-2"
						d="M64.77,17.37a2.15,2.15,0,0,0-1.4.44A1.48,1.48,0,0,0,62.83,19a1.77,1.77,0,0,0,.39,1.22,2.54,2.54,0,0,0,1.06.67,11.61,11.61,0,0,0,1.43.42c.51.13,1,.28,1.55.45a7.81,7.81,0,0,1,1.43.66,2.81,2.81,0,0,1,1,1.13,3.75,3.75,0,0,1,.4,1.81,3.94,3.94,0,0,1-1.4,3A5.3,5.3,0,0,1,65,29.67a6,6,0,0,1-3.75-1.1,3.64,3.64,0,0,1-1.43-3.07h3.07a1.88,1.88,0,0,0,2.14,1.88,2.23,2.23,0,0,0,1.55-.51,1.71,1.71,0,0,0,.58-1.36,1.54,1.54,0,0,0-.76-1.34,5.65,5.65,0,0,0-1.83-.73c-.71-.17-1.43-.36-2.15-.6a4,4,0,0,1-1.84-1.21,3.36,3.36,0,0,1-.76-2.3,3.81,3.81,0,0,1,1.41-3.1,5.5,5.5,0,0,1,3.63-1.17,5.8,5.8,0,0,1,3.56,1,3.91,3.91,0,0,1,1.47,3.08H66.77a1.94,1.94,0,0,0-.62-1.3A2,2,0,0,0,64.77,17.37Z"
					/><path
						class="cls-2"
						d="M77.29,27.11h1.37v2.41H76.84a4,4,0,0,1-2.68-.79,3.31,3.31,0,0,1-.94-2.64V20.56H72V18.21h1.2v-2.8H76.1v2.8h2.54v2.35H76.1v5.53a1,1,0,0,0,.27.79A1.38,1.38,0,0,0,77.29,27.11Z"
					/><path
						class="cls-2"
						d="M81.63,28a5.89,5.89,0,0,1-1.52-4.19,5.87,5.87,0,0,1,1.51-4.18A5,5,0,0,1,85.46,18,4,4,0,0,1,89,20V18.21h2.86V29.52H89v-1.9a4,4,0,0,1-3.57,2.07A5,5,0,0,1,81.63,28Zm6.48-1.73a3.29,3.29,0,0,0,.9-2.44,3.3,3.3,0,0,0-.9-2.45,2.95,2.95,0,0,0-4.19,0A3.26,3.26,0,0,0,83,23.85a3.32,3.32,0,0,0,.9,2.45,2.89,2.89,0,0,0,4.18,0Z"
					/><path class="cls-2" d="M94.94,29.52V14.41h2.88V29.52Z" /></svg
				>
			</a>

			<ul class="hidden items-stretch space-x-3 md:flex">
				<!-- <li class="flex">
				<a rel="noopener noreferrer" href="#" class="flex items-center px-4 -mb-1 border-b-2 dark:border-transparent">Link</a>
			</li> -->

				{#each links.slice(2, 4) as link}
					<li class="flex">
						<a
							href={link.link}
							class="mx-2 border-b-2 border-transparent text-2xl font-bold text-white hover:border-blue-500 hover:text-gray-800 sm:mx-6"
							>{link.title}</a
						>
					</li>
				{/each}
			</ul>
		</div>
	</div>
</header>
