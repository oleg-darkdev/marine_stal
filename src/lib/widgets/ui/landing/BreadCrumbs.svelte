<script>
	export let link;
</script>

<div class="bg-blue-600">
	<div class=" container mx-auto flex  items-center overflow-x-auto whitespace-nowrap px-6 py-4">
		<a href="#" class="text-white ">
			<svg
				xmlns="http://www.w3.org/2000/svg"
				class="h-5 w-5 fill-white"
				viewBox="0 0 20 20"
			>
				<path
					d="M10.707 2.293a1 1 0 00-1.414 0l-7 7a1 1 0 001.414 1.414L4 10.414V17a1 1 0 001 1h2a1 1 0 001-1v-2a1 1 0 011-1h2a1 1 0 011 1v2a1 1 0 001 1h2a1 1 0 001-1v-6.586l.293.293a1 1 0 001.414-1.414l-7-7z"
				/>
			</svg>
		</a>

		<span class="mx-5 text-gray-500 rtl:-scale-x-100 ">
			<svg
				xmlns="http://www.w3.org/2000/svg"
				class="h-5 w-5 fill-white"
				viewBox="0 0 20 20"
			>
				<path
					fill-rule="evenodd"
					d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z"
					clip-rule="evenodd"
				/>
			</svg>
		</span>

		<a href="#" class="text-white hover:underline "> Portfolio </a>

		<span class="mx-5 text-gray-500 rtl:-scale-x-100 ">
			<svg
				xmlns="http://www.w3.org/2000/svg"
				class="h-5 w-5 fill-white"
				viewBox="0 0 20 20"
			>
				<path
					fill-rule="evenodd"
					d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z"
					clip-rule="evenodd"
				/>
			</svg>
		</span>

		<a href="#" class="text-white font-bold hover:underline ">Projekt: {link} </a>
	</div>
</div>
