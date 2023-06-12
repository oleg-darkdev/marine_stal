<script>
	import { onMount } from 'svelte';
	export let portfolio;
	import anime from 'animejs/lib/anime.min.js';
	let slider = '',
		img = '',
		content = '';
	let items = [''];
	let tempItems;

	let nextBtn = '',
		prevBtn = '';

	let isPlaying = false,
		current = 0;

	onMount(() => {
		const sliderTemp = slider.querySelector('.slider');
		const items = sliderTemp.querySelectorAll('.item');
		const nextBtn = slider.querySelector('.slider .nav .next');
		const prevBtn = slider.querySelector('.slider .nav .prev');
		items.forEach((item) => {
			const textWrapper = item.querySelector('.wrap');
			textWrapper.innerHTML = textWrapper.textContent.replace(
				/\S/g,
				"<span class='letter'>$&</span>"
			);
		});

		nextBtn.onclick = next;
		prevBtn.onclick = prev;

		function next() {
			if (isPlaying) return;
			isPlaying = true;
			const newIndex = current === items.length - 1 ? 0 : current + 1;

			console.log('next');
			updateSlider(newIndex);
		}

		function prev() {
			console.log('prev');

			if (isPlaying) return;
			isPlaying = true;
			const newIndex = current === 0 ? items.length - 1 : current - 1;
			console.log(current);

			updateSlider(newIndex);
		}

		function updateSlider(newIndex) {
			const currentItem = items[current];
			const newItem = items[newIndex];

			function callback() {
				currentItem.classList.remove('is-active');
				newItem.classList.add('is-active');
				current = newIndex;
				isPlaying = false;
			}

			anim(currentItem, newItem, callback);
		}

		function anim(current, next, callback) {
			const currentImgs = current.querySelectorAll('.img');
			const currentText = current.querySelectorAll('.content .letter');
			const nextImgs = next.querySelectorAll('.img');
			const nextText = next.querySelectorAll('.content .letter');

			const duration = 400;
			const offset = '-=' + 300;
			const imgOffset = duration * 0.8;

			const tl = anime.timeline({
				easing: 'easeInOutQuint',
				duration: duration,
				complete: callback
			});

			// Add children
			tl.add({
				targets: currentText,
				translateY: [0, '-.75em'],
				/*clipPath: ['polygon(0 0, 100% 0, 100% 100%, 0% 100%)', 'polygon(0 100%, 100% 100%, 100% 100%, 0% 100%)'],*/
				opacity: [1, 0],
				easing: 'easeInQuint',
				duration: 600,
				delay: (el, i) => 10 * (i + 1)
			})
				.add(
					{
						targets: currentImgs[0],
						translateY: -600,
						rotate: [0, '-15deg'],
						opacity: [1, 0],
						easing: 'easeInCubic'
					},
					offset
				)
				.add(
					{
						targets: currentImgs[1],
						translateY: -600,
						rotate: [0, '15deg'],
						opacity: [1, 0],
						easing: 'easeInCubic'
					},
					'-=' + imgOffset
				)
				.add(
					{
						targets: currentImgs[2],
						translateY: -600,
						rotate: [0, '-15deg'],
						opacity: [1, 0],
						easing: 'easeInCubic'
					},
					'-=' + imgOffset
				)
				.add(
					{
						targets: currentImgs[3],
						translateY: -600,
						rotate: [0, '15deg'],
						opacity: [1, 0],
						easing: 'easeInCubic'
					},
					'-=' + imgOffset
				)
				.add({
					targets: current,
					opacity: 0,
					duration: 10,
					easing: 'easeInCubic'
				})
				.add(
					{
						targets: next,
						opacity: 1,
						duration: 10
					},
					offset
				)
				.add(
					{
						targets: nextImgs[0],
						translateY: [600, 0],
						rotate: ['15deg', 0],
						opacity: [0, 1],
						easing: 'easeOutCubic'
					},
					offset
				)
				.add(
					{
						targets: nextImgs[1],
						translateY: [600, 0],
						rotate: ['-15deg', 0],
						opacity: [0, 1],
						easing: 'easeOutCubic'
					},
					'-=' + imgOffset
				)
				.add(
					{
						targets: nextImgs[2],
						translateY: [600, 0],
						rotate: ['15deg', 0],
						opacity: [0, 1],
						easing: 'easeOutCubic'
					},
					'-=' + imgOffset
				)
				.add(
					{
						targets: nextImgs[3],
						translateY: [600, 0],
						rotate: ['-15deg', 0],
						opacity: [0, 1],
						easing: 'easeOutCubic'
					},
					'-=' + imgOffset
				)
				.add(
					{
						targets: nextText,
						translateY: ['.75em', 0],
						/*clipPath: ['polygon(0 0, 100% 0, 100% 0, 0 0)','polygon(0 0, 100% 0, 100% 100%, 0% 100%)'],*/
						opacity: [0, 1],
						easing: 'easeOutQuint',
						duration: 600,
						delay: (el, i) => 10 * (i + 1)
					},
					offset
				);
		}
	});
</script>

<div class="" bind:this={slider}>
	<div class="slider">
		<div class="nav">
			<div class="next" />
			<div class="prev" />
			<!-- <a href="" class="explore-btn">Czytaj więcej</a> -->
		</div>

		<div class="item is-active">
			<div class="content" bind:this={content}>
				<h2 class="wrap">{portfolio[0].title}</h2>
			</div>
			<div class="imgs">
				<div class="grid " bind:this={img}>
					<div class="img img-1">
						<img src="images/portfolio/{portfolio[0].link}/{portfolio[0].gallery[1]}" />
					</div>

					<div class="img img-2">
						<img src="images/portfolio/{portfolio[0].link}/{portfolio[0].gallery[1]}" />
					</div>

					<div class="img img-3">
						<img src="images/portfolio/{portfolio[0].link}/{portfolio[0].gallery[2]}" />
					</div>

					<div class="img img-4">
						<img src="images/portfolio/{portfolio[0].link}/{portfolio[0].gallery[3]}" />
					</div>
				</div>
			</div>
		</div>
		<div class="item ">
			<div class="content" bind:this={content}>
				<div class="wrap">{portfolio[1].title}</div>
			</div>
			<div class="imgs">
				<div class="grid " bind:this={img}>
					<div class="img img-1">
						<img src="images/portfolio/{portfolio[1].link}/{portfolio[1].gallery[1]}" />
					</div>

					<div class="img img-2">
						<img src="images/portfolio/{portfolio[1].link}/{portfolio[1].gallery[1]}" />
					</div>

					<div class="img img-3">
						<img src="images/portfolio/{portfolio[1].link}/{portfolio[1].gallery[2]}" />
					</div>

					<div class="img img-4">
						<img src="images/portfolio/{portfolio[1].link}/{portfolio[1].gallery[3]}" />
					</div>
				</div>
			</div>
		</div>
	</div>
</div>

<style>
	.slider {
		height: 100vh;
		width: 100vw;
		/* background-color: #0a0908; */
		display: flex;
		align-items: center;
		justify-content: center;
		color: white;
		position: relative;
		overflow: hidden;
		transition: background-color 2s;
	}

	.slider .item .imgs {
		position: relative;
		width: 60%;
		padding-top: 60%;
	}
	.slider .item .imgs .grid {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		display: grid;
		grid-template-columns: repeat(12, 1fr);
		grid-template-rows: repeat(12, 1fr);
		grid-column-gap: 32px;
		grid-row-gap: 32px;
		transform: rotate(-20deg);
		opacity: 0.65;
	}

	.slider .item {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		display: flex;
		align-items: center;
		justify-content: center;
	}
	.slider .item .img {
		width: 100%;
		height: 100%;
		position: relative;
		will-change: transform;
		will-change: opacity;
	}
	.slider .item .img img {
		position: absolute;
		top: 0;
		width: 100%;
		height: 100%;
		object-fit: cover;
		position: relative;
		-webkit-filter: contrast(110%) brightness(110%) saturate(130%);
		filter: contrast(110%) brightness(110%) saturate(130%);
	}
	.slider .item .img img::before {
		content: '';
		display: block;
		height: 100%;
		width: 100%;
		top: 0;
		left: 0;
		position: absolute;
		pointer-events: none;
		mix-blend-mode: screen;
		background: rgba(243, 106, 188, 0.3);
	}
	.slider .item .img-1 {
		grid-area: 1/1/7/5;
	}
	.slider .item .img-2 {
		grid-area: 2/5/7/13;
	}
	.slider .item .img-3 {
		grid-area: 7/1/12/9;
	}
	.slider .item .img-4 {
		grid-area: 7/9/13/13;
	}
	.slider .item .content {
		position: absolute;
		z-index: 2;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		display: flex;
		align-items: center;
		justify-content: center;
		line-height: 1.15;
		font-size: 8rem;
		font-weight: 700;
	}
	.slider .item .content .wrap {
		text-align: center;
		text-shadow: 1px 1px 4px rgba(10, 9, 8, 0.2);
		width: 100%;
		max-width: 600px;
		line-height: 1;
	}
	.slider .item .content .wrap .letter {
		display: inline-block;
	}

	.slider .nav .next,
	.slider .nav .prev {
		height: 6rem;
		width: 6rem;
		position: absolute;
		top: calc(50% - 1rem);
		cursor: pointer;
		z-index: 3;
		transition: transform 0.3s;
	}
	.slider .nav .next {
		right: 6rem;
		background-image: url("data:image/svg+xml,%3C?xml version='1.0' encoding='utf-8'?%3E %3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='white'%3E%3Cpath d='M 19 8 L 19 11 L 1 11 L 1 13 L 19 13 L 19 16 L 23 12 L 19 8 z' fill='white'/%3E%3C/svg%3E");
	}
	.slider .nav .next:hover {
		transform: translateX(0.5rem);
	}
	.slider .nav .prev {
		left: 6rem;
		background-image: url("data:image/svg+xml,%3C?xml version='1.0' encoding='utf-8'?%3E %3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='white'%3E%3Cpath d='M 5 8 L 1 12 L 5 16 L 5 13 L 23 13 L 23 11 L 5 11 L 5 8 z' fill='white'/%3E%3C/svg%3E");
	}
	.slider .nav .prev:hover {
		transform: translateX(-0.5rem);
	}
	.slider .nav .explore-btn {
		z-index: 4;
		position: absolute;
		bottom: 2rem;
		left: calc(50% - 4rem);
		width: 8em;
		text-align: center;
		padding: 1rem 0;
		border: solid 2px white;
		background: transparent;
		color: white;
		transition: background-color 0.3s;
		cursor: pointer;
	}
	.slider .nav .explore-btn:hover {
		color: #0a0908;
		background: white;
	}

	.slider .item:not(.is-active) {
		opacity: 0;
		pointer-events: none;
	}
</style>
