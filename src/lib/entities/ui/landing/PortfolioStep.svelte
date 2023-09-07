<script>
	export let step;
</script>

<div class=" flex lg:w-full md:w-full  overflow-x-hidden flex-col items-center lg:px-5 md:px-5">
	<div class="flex flex-wrap lg:py-8 md:py-4 py-1 md:flex-nowrap">
		<div class="mb-2 flex flex-shrink-0 flex-col lg:px-4 md:px-4   md:mb-0 md:w-64">
			<strong
				class="text-thin flex text-left text-2xl font-black leading-none text-blue-600 lg:text-4xl"
			>
				{step.date}
			</strong>
			<span class="mt-1 text-xs font-bold leading-relaxed text-gray-700">{step.title}</span>
			<img
				async
				src={step.img}
				alt="Stan na dzień: {step.date}"
				class="mt-2  grayscale  filter lg:h-full h-[350px] max-w-sm lg:w-full rounded object-cover object-center opacity-75 hover:opacity-100"
			/>
		</div>
		<div class="prose-1xl prose text-gray-600 md:flex-grow">
			{#each step.desc as desc}
				<p>
					{desc}
				</p>
			{/each}
		</div>
	</div>
</div>
