<script>
	const gallery = [
		['1.jpg', '2.jpg', '3.jpg'],
		['4.jpg', '5.jpg', '6.jpg'],
		['7.jpg', '8.jpg', '9.jpg'],
		['10.jpg', '11.jpg', '12.jpg']
	];
</script>

{#each gallery as imgCollection}
	<div class="grid gap-4">
		<div>
			<img
				class="blur-xs hover:contrast-none h-auto max-w-full transform  rounded-lg  grayscale filter transition delay-150 duration-300 ease-in-out  hover:-translate-y-8 hover:blur-none hover:filter-none"
				src="/images/gallery/{imgCollection[0]}"
				alt=""
			/>
		</div>
		<div>
			<img
				class="blur-xs hover:contrast-none h-auto max-w-full transform  rounded-lg  grayscale filter transition delay-150 duration-300 ease-in-out  hover:-translate-y-8 hover:blur-none hover:filter-none"
				src="/images/gallery/{imgCollection[1]}"
				alt=""
			/>
		</div>
		<div>
			<img
				class="blur-xs hover:contrast-none h-auto max-w-full transform  rounded-lg  grayscale filter transition delay-150 duration-300 ease-in-out  hover:-translate-y-8 hover:blur-none hover:filter-none"
				src="/images/gallery/{imgCollection[3]}"
				alt=""
			/>
		</div>
	</div>
{/each}
