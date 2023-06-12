<script>
	const gallery = [
		[1, 2, 3],
		[4, 5, 6],
		[7, 8, 9],
		[10, 11, 12]
	];
</script>

	{#each gallery as imgCollection}
		<div class="grid gap-4">
			<div>
				<img
					class="blur-xs hover:contrast-none h-auto max-w-full transform  rounded-lg  grayscale filter transition delay-150 duration-300 ease-in-out  hover:-translate-y-8 hover:blur-none hover:filter-none"
					src="/images/gallery/{imgCollection[0]}.jpg"
					alt=""
				/>
			</div>
			<div>
				<img
					class="blur-xs hover:contrast-none h-auto max-w-full transform  rounded-lg  grayscale filter transition delay-150 duration-300 ease-in-out  hover:-translate-y-8 hover:blur-none hover:filter-none"
					src="/images/gallery/{imgCollection[1]}.jpg"
					alt=""
				/>
			</div>
			<div>
				<img
					class="blur-xs hover:contrast-none h-auto max-w-full transform  rounded-lg  grayscale filter transition delay-150 duration-300 ease-in-out  hover:-translate-y-8 hover:blur-none hover:filter-none"
					src="/images/gallery/{imgCollection[3]}.jpg"
					alt=""
				/>
			</div>
		</div>
	{/each}
