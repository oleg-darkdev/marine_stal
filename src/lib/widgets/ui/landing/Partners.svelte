<script>
	export let partners;
</script>

<div class="relative mx-auto w-full max-w-7xl items-center px-5  pb-20 md:px-12 lg:px-16 ">
	<div class="mx-auto flex w-full text-left">
		<div class="relative mx-auto inline-flex items-center align-middle">
			<div class="pb-12 text-center">
				<h2
					class="max-w-5xl text-2xl font-bold leading-none tracking-tighter text-blue-500 md:text-5xl lg:max-w-7xl lg:text-6xl"
				>
					Nasi partnerzy
				</h2>
			</div>
		</div>
	</div>

	<div class="mx-auto text-center">
		<div class="mx-auto grid grid-cols-5 gap-4 lg:grid-cols-3">
			{#each partners as partner}
				<a href={partner.link} target="_blank">
					<img
						class="rouded-lg m-4 mx-auto h-4  rounded bg-blue-500 p-2 shadow shadow-xl lg:h-32"
						src="./images/logos/{partner.logo}"
						alt={partner.title}
					/>
				</a>
			{/each}
		</div>
	</div>
</div>
