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

	import Icon from 'svelte-icons-pack/Icon.svelte';
	import AiOutlineNodeExpand from 'svelte-icons-pack/ai/AiOutlineNodeExpand';
</script>

<!-- hero section start -->
<!-- hero section 1 -->
<section class="w-full py-12 md:py-24 lg:py-32">
	<div class="px-4 md:px-6">
		<div class="flex flex-col items-center justify-center space-y-4 text-center">
			<div class="space-y-2">
				<div class="inline-block rounded-lg bg-gray-100 px-3 py-1 text-sm dark:bg-gray-800">
					Made in Love
				</div>
				<h2 class="text-3xl font-bold tracking-tighter sm:text-5xl">
					Imagine a world of Innovation for everyone.
				</h2>
				<p
					class="max-w-[900px] text-gray-500 md:text-xl/relaxed lg:text-base/relaxed xl:text-xl/relaxed dark:text-gray-400"
				>
					Art by Demitri Da Vinci.
				</p>
			</div>
			<div class="flex flex-col gap-2 min-[400px]:flex-row">
				<a href="/musuem">
					<span
						class="inline-flex h-10 items-center justify-center rounded-md bg-gray-900 px-8 text-sm font-medium text-gray-50 shadow transition-colors hover:bg-gray-900/90 focus-visible:outline-none focus-visible:ring-1 focus-visible:ring-gray-950 disabled:pointer-events-none disabled:opacity-50 dark:bg-gray-50 dark:text-gray-900 dark:hover:bg-gray-50/90 dark:focus-visible:ring-gray-300"
						>Visit Musuem</span
					>
				</a>
				<a
					class="inline-flex h-10 items-center justify-center rounded-md border border-gray-200 bg-white px-8 text-sm font-medium shadow-sm transition-colors hover:bg-gray-100 hover:text-gray-900 focus-visible:outline-none focus-visible:ring-1 focus-visible:ring-gray-950 disabled:pointer-events-none disabled:opacity-50 dark:border-gray-800 dark:bg-gray-950 dark:hover:bg-gray-800 dark:hover:text-gray-50 dark:focus-visible:ring-gray-300"
					href="/collections"
				>
					Shop Collection
				</a>
			</div>
			<!-- using for example. does work -->
			<Icon src={AiOutlineNodeExpand} />
		</div>
	</div>
</section>

<!-- hero section 2 -->
<div
	class="bg-card text-card-foreground transform rounded-lg shadow-sm transition-transform duration-500 hover:scale-105 hover:shadow-lg"
	data-v0-t="card"
>
	<div class="px-6 py-3">
		<img
			src="../odyssey.jpeg"
			alt="AI artowrk of ceoDemitri in uniform standing at a window in the Hanging Gardens on Jupite"
			class="h-64 w-full rounded-lg object-cover lg:h-[600px]"
			style="aspect-ratio: 200 / 400; object-fit: cover;"
		/>
		<h3 class="mt-4 text-lg font-semibold">Welcome to my journey.</h3>
		<p class="mt-2 text-sm text-gray-500">
			To stay up to date with our vision/roadmap, use the button below for a calendar view of
			special dates.
		</p>
		<button
			class="ring-offset-background focus-visible:ring-ring mt-4 inline-flex h-10 items-center justify-center whitespace-nowrap rounded bg-gray-900 px-4 py-2 text-sm font-medium text-white transition-colors duration-300 hover:bg-gray-700 focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-offset-2 disabled:pointer-events-none disabled:opacity-50"
		>
			Calendar
		</button>
	</div>
</div>
<!-- hero section end -->

<!-- feature section start -->
<section class="w-full py-12 md:py-24 lg:py-32">
	<div class="container m-auto px-4 md:px-6">
		<div class="flex flex-col items-center space-y-4 text-center">
			<h1 class="text-3xl font-bold tracking-tighter sm:text-4xl md:text-5xl lg:text-6xl/none">
				Discover A New Perspective
			</h1>
			<p
				class="mx-auto max-w-[700px] text-gray-500 md:text-xl/relaxed lg:text-base/relaxed xl:text-xl/relaxed dark:text-gray-400"
			>
				Today we start humbly, pioneering a fresh venture. Explore with me.
			</p>
		</div>
		<div
			class="mx-auto mt-12 grid max-w-5xl items-start gap-8 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4"
		>
			<div class="grid gap-1">
				<img
					alt="Artwork 1"
					class="aspect-[1/1] overflow-hidden rounded-lg object-cover object-center"
					height="200"
					src="/discover/fish.png"
					width="200"
				/>
				<h3 class="text-lg font-bold">Artwork Title 1</h3>
				<p class="text-sm text-gray-500 dark:text-gray-400">Artist Name 1</p>
			</div>
			<div class="grid gap-1">
				<img
					alt="Artwork 2"
					class="aspect-[1/1] overflow-hidden rounded-lg object-cover object-center"
					height="200"
					src="/placeholder.svg"
					width="200"
				/>
				<h3 class="text-lg font-bold">Artwork Title 2</h3>
				<p class="text-sm text-gray-500 dark:text-gray-400">Artist Name 2</p>
			</div>
			<div class="grid gap-1">
				<img
					alt="Artwork 3"
					class="aspect-[1/1] overflow-hidden rounded-lg object-cover object-center"
					height="200"
					src="/placeholder.svg"
					width="200"
				/>
				<h3 class="text-lg font-bold">Artwork Title 3</h3>
				<p class="text-sm text-gray-500 dark:text-gray-400">Artist Name 3</p>
			</div>
			<div class="grid gap-1">
				<img
					alt="Artwork 4"
					class="aspect-[1/1] overflow-hidden rounded-lg object-cover object-center"
					height="200"
					src="/placeholder.svg"
					width="200"
				/>
				<h3 class="text-lg font-bold">Artwork Title 4</h3>
				<p class="text-sm text-gray-500 dark:text-gray-400">Artist Name 4</p>
			</div>
		</div>
	</div>
</section>

<!-- about us section start -->
<section
	class="flex flex-col items-center justify-center gap-6 px-4 py-6 md:flex-row md:items-start md:gap-12 md:px-6 md:py-12"
>
	<img
		src="/about/me.png"
		alt="About Us"
		width="500"
		height="500"
		class="h-64 w-full rounded-lg md:h-auto md:w-1/2"
		style="aspect-ratio: 500 / 500; object-fit: cover;"
	/>
	<div class="space-y-4 md:w-1/2">
		<h2 class="text-3xl font-bold tracking-tighter md:text-4xl lg:text-5xl">About Us</h2>
		<p class="text-gray-500 md:text-lg lg:text-xl">
			Born in America, I feel my real home is the earth. I ignore these imaginary lines to draw my
			own reality.
		</p>
		<a
			class="inline-flex h-10 items-center justify-center rounded-md bg-gray-900 px-8 text-sm font-medium text-gray-50 shadow transition-colors hover:bg-gray-900/90 focus-visible:outline-none focus-visible:ring-1 focus-visible:ring-gray-950 disabled:pointer-events-none disabled:opacity-50 dark:bg-gray-50 dark:text-gray-900 dark:hover:bg-gray-50/90 dark:focus-visible:ring-gray-300"
			href="#"
		>
			Learn More
		</a>
		<div class="mt-4 flex space-x-4">
			<a href="#">
				<img
					src=""
					alt="Avatar 1"
					width="50"
					height="50"
					class="rounded-full"
					style="aspect-ratio: 50 / 50; object-fit: cover;"
				/>
			</a>
			<a href="#">
				<img
					src=""
					alt="Avatar 2"
					width="50"
					height="50"
					class="rounded-full"
					style="aspect-ratio: 50 / 50; object-fit: cover;"
				/>
			</a>
			<a href="#">
				<img
					src=""
					alt="Avatar 3"
					width="50"
					height="50"
					class="rounded-full"
					style="aspect-ratio: 50 / 50; object-fit: cover;"
				/>
			</a>
		</div>
	</div>
</section>

<!-- about us section end -->

<style>
</style>
