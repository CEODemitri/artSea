<script lang="ts">
	import { goto } from '$app/navigation';

	function moveAround() {
		goto('/collections');
	}

	let elemCarousel: HTMLDivElement;
	const unsplashIds = [
		'vjUokUWbFOs',
		'1aJuPtQJX_I',
		'Jp6O3FFRdEI',
		'I3C_eojFVQY',
		's0fXOuyTH1M',
		'z_X0PxmBuIQ'
	];

	function carouselLeft(): void {
		const x =
			elemCarousel.scrollLeft === 0
				? elemCarousel.clientWidth * elemCarousel.childElementCount // loop
				: elemCarousel.scrollLeft - elemCarousel.clientWidth; // step left
		elemCarousel.scroll(x, 0);
	}

	function carouselRight(): void {
		const x =
			elemCarousel.scrollLeft === elemCarousel.scrollWidth - elemCarousel.clientWidth
				? 0 // loop
				: elemCarousel.scrollLeft + elemCarousel.clientWidth; // step right
		elemCarousel.scroll(x, 0);
	}
</script>

<h1 class="pb-3 pt-5 text-[52px]">ArtSea</h1>
<h2>Adventure off into a land like no other</h2>
<p>
	Welcome to a brandnew vision. Why wait on the world to create beautiful innovations. Lets step it
	up. Introducing a fresh perspective.
</p>
<div class="flex gap-5 p-5">
	<a href="/musuem" class="variant-filled-surface btn">
		<span class="material-symbols-outlined"> door_open </span>
		<span>Musuem</span>
	</a>
	<button type="button" class="myButton variant-ghost btn" on:click={moveAround}>
		<span class="material-symbols-outlined"> favorite </span>
		<span>Collections</span>
	</button>
</div>
<div>
	<div class="card grid grid-cols-[auto_1fr_auto] items-center gap-4 p-4">
		<!-- Button: Left -->
		<button type="button" class="variant-filled btn-icon" on:click={carouselLeft}>
			<i class="fa-solid fa-arrow-left" />
		</button>
		<!-- Full Images -->
		<div bind:this={elemCarousel} class="flex snap-x snap-mandatory overflow-x-auto scroll-smooth">
			{#each unsplashIds as unsplashId}
				<img
					class="w-[1024px] snap-center rounded-container-token"
					src="https://source.unsplash.com/{unsplashId}/1024x768"
					alt={unsplashId}
					loading="lazy"
				/>
			{/each}
		</div>
		<!-- Button: Right -->
		<button type="button" class="variant-filled btn-icon" on:click={carouselRight}>
			<i class="fa-solid fa-arrow-right" />
		</button>
	</div>
</div>

<style>
</style>
