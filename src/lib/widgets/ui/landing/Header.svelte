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
		{
			title: 'Nasi partnerzy',
			link: '#partnerzy'
		},
		{
			title: 'Kontakty',
			link: '#kontakty'
		}
	];
</script>

<header class="w-full bg-primary py-10">
	<nav class=" ">
		<div class="container mx-auto flex flex-col items-center p-6">
			<!-- <a href="#" class="mx-auto text-black">
				<img class="h-6 w-auto sm:h-7" src="https://merakiui.com/images/full-logo.svg" alt="" />
        Marine Stal Sp. z o. o.
			</a> -->

			<div class="flex w-full max-w-6xl flex-col items-center  ">
				<div style=" justify-content: space-between;" class="flex w-7/12  flex-row flex-wrap  ">
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
				<hr class="my-4  h-1 w-7/12 border-0 bg-blue-600 " />
			</div>
			<div class="flex items-center justify-center capitalize text-gray-600 ">
				{#each links as link}
					<a
						href={link.link}
						class="mx-2 border-b-2 border-transparent text-2xl font-bold text-white hover:border-blue-500 hover:text-gray-800 sm:mx-6"
						>{link.title}</a
					>
				{/each}
				<!-- <a
					href="#"
					class="mx-2 border-b-2 border-transparent hover:border-blue-500 hover:text-gray-800 sm:mx-6"
				>
					<svg class="h-5 w-5 fill-current" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"
						><path
							d="m.75 19h7.092c4.552 0 6.131-6.037 2.107-8.203 2.701-2.354 1.029-6.797-2.595-6.797h-6.604c-.414 0-.75.336-.75.75v13.5c0 .414.336.75.75.75zm.75-13.5h5.854c3.211 0 3.215 4.768 0 4.768h-5.854zm0 6.268h6.342c3.861 0 3.861 5.732 0 5.732h-6.342z"
						/><path
							d="m18.374 7.857c-3.259 0-5.755 2.888-5.635 5.159-.247 3.28 2.397 5.984 5.635 5.984 2.012 0 3.888-1.065 4.895-2.781.503-.857-.791-1.613-1.293-.76-.739 1.259-2.12 2.041-3.602 2.041-2.187 0-3.965-1.668-4.125-3.771 1.443.017 4.136-.188 8.987-.033.016 0 .027-.008.042-.008 2-.09-.189-5.831-4.904-5.831zm-3.928 4.298c1.286-3.789 6.718-3.676 7.89.064-4.064.097-6.496-.066-7.89-.064z"
						/><path d="m21.308 6.464c.993 0 .992-1.5 0-1.5h-5.87c-.993 0-.992 1.5 0 1.5z" /></svg
					>
				</a> -->
			</div>
		</div>
	</nav>
</header>
