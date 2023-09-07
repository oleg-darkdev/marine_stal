<script>
	export let step;
</script>

<div
	class=" flex flex-col items-center overflow-x-hidden md:w-full md:px-5 lg:w-full lg:px-5"
>
	<div class="flex flex-wrap py-1 md:flex-nowrap md:py-4 lg:py-8">
		<div class="mb-2 flex flex-shrink-0 flex-col md:mb-0 md:w-64   md:px-4 lg:px-4">
			<span
				class="text-thin  text-center text-3xl font-black leading-none text-blue-600 md:text-left lg:text-left lg:text-4xl"
			>
				{step.date}
			</span>
			<span
				class="mt-1 text-center  text-xs font-bold leading-relaxed text-gray-700 md:text-left lg:text-left"
				>{step.title}</span
			>
			<div class=" ">
				<img
					async
					src={step.img}
					alt="Stan na dzień: {step.date}"
					class="mt-2  h-[350px]  max-w-sm rounded object-cover object-center opacity-75 grayscale filter hover:opacity-100 lg:h-full lg:w-full"
				/>
			</div>
		</div>
		<div class="prose-1xl prose text-gray-600 lg:px-0 md:px-0 px-10 md:flex-grow">
			{#each step.desc as desc}
				<p>
					{desc}
				</p>
			{/each}
		</div>
	</div>
</div>
