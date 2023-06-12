<script>
	const gallery = [
		['/images/gallery/1.jpg', '/images/gallery/2.jpg', '/images/gallery/3.jpg'],
		['/images/gallery/4.jpg', '/images/gallery/5.jpg', '/images/gallery/6.jpg'],
		['/images/gallery/7.jpg', '/images/gallery/8.jpg', '/images/gallery/9.jpg'],
		['/images/gallery/10.jpg', '/images/gallery/11.jpg', '/images/gallery/12.jpg']
	];
</script>

{#each gallery as imgCollection}
	<div class="grid gap-4">
		<div>
			<img
				class="blur-xs hover:contrast-none h-auto max-w-full transform  rounded-lg  grayscale filter transition delay-150 duration-300 ease-in-out  hover:-translate-y-8 hover:blur-none hover:filter-none"
				src={imgCollection[0]}
				alt=""
			/>
		</div>
		<div>
			<img
				class="blur-xs hover:contrast-none h-auto max-w-full transform  rounded-lg  grayscale filter transition delay-150 duration-300 ease-in-out  hover:-translate-y-8 hover:blur-none hover:filter-none"
				src={imgCollection[1]}
				alt=""
			/>
		</div>
		<div>
			<img
				class="blur-xs hover:contrast-none h-auto max-w-full transform  rounded-lg  grayscale filter transition delay-150 duration-300 ease-in-out  hover:-translate-y-8 hover:blur-none hover:filter-none"
				src={imgCollection[3]}
				alt=""
			/>
		</div>
	</div>
{/each}
