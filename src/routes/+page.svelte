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
					Artsea is a new company, rooted deeply in Creating and Inspiring. We are bringing passion
					to the market.
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
		<h3 class="mt-4 text-lg font-semibold">We all have a journey.</h3>
		<p class="mt-2 text-sm text-gray-500">
			To stay up to date with our vision/roadmap, use the button below for a calendar view.
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
	<div class="container px-4 md:px-6">
		<div class="flex flex-col items-center space-y-4 text-center">
			<h1 class="text-3xl font-bold tracking-tighter sm:text-4xl md:text-5xl lg:text-6xl/none">
				Discover Unique Artwork
			</h1>
			<p
				class="mx-auto max-w-[700px] text-gray-500 md:text-xl/relaxed lg:text-base/relaxed xl:text-xl/relaxed dark:text-gray-400"
			>
				Our platform brings together a diverse collection of artists from around the world, offering
				you a unique selection of artwork to discover and collect.
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
					src="/placeholder.svg"
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
<!-- feature section end -->

<!-- inspiration section start -->
<h2 class="mt-10 px-6 text-2xl">What Inspires Us</h2>
<div class="flex w-full flex-col items-center gap-4">
	<div
		class="bg-card text-card-foreground flex w-full flex-col items-center rounded-lg border p-4 shadow-sm"
		data-v0-t="card"
	>
		<svg
			xmlns="http://www.w3.org/2000/svg"
			width="24"
			height="24"
			viewBox="0 0 24 24"
			fill="none"
			stroke="currentColor"
			stroke-width="2"
			stroke-linecap="round"
			stroke-linejoin="round"
			class="h-12 w-12 text-gray-900 dark:text-gray-50"
		>
			<path d="M17.5 19H9a7 7 0 1 1 6.71-9h1.79a4.5 4.5 0 1 1 0 9Z"></path>
		</svg>
		<h3 class="mt-4 whitespace-nowrap text-lg font-semibold tracking-tight">Cloud Storage</h3>
		<p class="mt-2 text-sm text-gray-500 dark:text-gray-400">
			Store your data securely in the cloud with our encrypted storage solutions.
		</p>
	</div>
	<div
		class="bg-card text-card-foreground flex w-full flex-col items-center rounded-lg border p-4 shadow-sm"
		data-v0-t="card"
	>
		<svg
			xmlns="http://www.w3.org/2000/svg"
			width="24"
			height="24"
			viewBox="0 0 24 24"
			fill="none"
			stroke="currentColor"
			stroke-width="2"
			stroke-linecap="round"
			stroke-linejoin="round"
			class="h-12 w-12 text-gray-900 dark:text-gray-50"
		>
			<path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10"></path>
			<path d="m9 12 2 2 4-4"></path>
		</svg>
		<h3 class="mt-4 whitespace-nowrap text-lg font-semibold tracking-tight">Secure Access</h3>
		<p class="mt-2 text-sm text-gray-500 dark:text-gray-400">
			Protect your data with our advanced security measures and access controls.
		</p>
	</div>
	<div
		class="bg-card text-card-foreground flex w-full flex-col items-center rounded-lg border p-4 shadow-sm"
		data-v0-t="card"
	>
		<svg
			xmlns="http://www.w3.org/2000/svg"
			width="24"
			height="24"
			viewBox="0 0 24 24"
			fill="none"
			stroke="currentColor"
			stroke-width="2"
			stroke-linecap="round"
			stroke-linejoin="round"
			class="h-12 w-12 text-gray-900 dark:text-gray-50"
		>
			<line x1="12" x2="12" y1="20" y2="10"></line>
			<line x1="18" x2="18" y1="20" y2="4"></line>
			<line x1="6" x2="6" y1="20" y2="16"></line>
		</svg>
		<h3 class="mt-4 whitespace-nowrap text-lg font-semibold tracking-tight">Analytics</h3>
		<p class="mt-2 text-sm text-gray-500 dark:text-gray-400">
			Get insights into your data with our powerful analytics tools.
		</p>
	</div>
	<div
		class="bg-card text-card-foreground flex w-full flex-col items-center rounded-lg border p-4 shadow-sm"
		data-v0-t="card"
	>
		<svg
			xmlns="http://www.w3.org/2000/svg"
			width="24"
			height="24"
			viewBox="0 0 24 24"
			fill="none"
			stroke="currentColor"
			stroke-width="2"
			stroke-linecap="round"
			stroke-linejoin="round"
			class="h-12 w-12 text-gray-900 dark:text-gray-50"
		>
			<circle cx="12" cy="12" r="10"></circle>
			<line x1="2" x2="22" y1="12" y2="12"></line>
			<path
				d="M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"
			></path>
		</svg>
		<h3 class="mt-4 whitespace-nowrap text-lg font-semibold tracking-tight">Global Network</h3>
		<p class="mt-2 text-sm text-gray-500 dark:text-gray-400">
			Access your data from anywhere in the world through our global network.
		</p>
	</div>
</div>
<!-- inspiration section end -->

<section class="w-full py-12 md:py-24 lg:py-32 xl:py-48">
	<div class="px-4 md:px-6">
		<div class="grid items-center gap-6">
			<div class="flex flex-col justify-center space-y-8 text-center">
				<div class="space-y-2">
					<h1 class=" text-3xl font-bold tracking-tighter sm:text-5xl xl:text-6xl/none">
						Pioneering a new future.
					</h1>
					<p class="mx-auto max-w-[600px] md:text-xl dark:text-zinc-100">
						Stand with us as we make waves producing the arts of our generations. The goal has been
						set by ancestors and descendants.
					</p>
				</div>
				<div class="mx-auto w-full max-w-full space-y-4">
					<div class="grid grid-cols-3 gap-8">
						<div class="flex flex-col items-center space-y-2 rounded-lg border-gray-800 p-4">
							<svg
								xmlns="http://www.w3.org/2000/svg"
								width="24"
								height="24"
								viewBox="0 0 24 24"
								fill="none"
								stroke="currentColor"
								stroke-width="2"
								stroke-linecap="round"
								stroke-linejoin="round"
								class="mb-2 h-6 w-6"
							>
								<polyline points="22 12 16 12 14 15 10 15 8 12 2 12"></polyline>
								<path
									d="M5.45 5.11 2 12v6a2 2 0 0 0 2 2h16a2 2 0 0 0 2-2v-6l-3.45-6.89A2 2 0 0 0 16.76 4H7.24a2 2 0 0 0-1.79 1.11z"
								></path>
							</svg>
							<h2 class="text-xl font-bold">Your Smarter Inbox</h2>
							<p class="dark:text-zinc-100">
								Our Smart Inbox feature helps you manage your emails efficiently by prioritizing
								important emails.
							</p>
						</div>
						<div class="flex flex-col items-center space-y-2 rounded-lg border-gray-800 p-4">
							<svg
								xmlns="http://www.w3.org/2000/svg"
								width="24"
								height="24"
								viewBox="0 0 24 24"
								fill="none"
								stroke="currentColor"
								stroke-width="2"
								stroke-linecap="round"
								stroke-linejoin="round"
								class="mb-2 h-6 w-6"
							>
								<path d="m8 6 4-4 4 4"></path>
								<path d="M12 2v10.3a4 4 0 0 1-1.172 2.872L4 22"></path>
								<path d="m20 22-5-5"></path>
							</svg>
							<h2 class="text-xl font-bold">Seamless Integration</h2>
							<p class="dark:text-zinc-100">
								Seamless Integration allows you to connect with your favorite apps and services
								without leaving your inbox.
							</p>
						</div>
						<div class="flex flex-col items-center space-y-2 rounded-lg border-gray-800 p-4">
							<svg
								xmlns="http://www.w3.org/2000/svg"
								width="24"
								height="24"
								viewBox="0 0 24 24"
								fill="none"
								stroke="currentColor"
								stroke-width="2"
								stroke-linecap="round"
								stroke-linejoin="round"
								class="mb-2 h-6 w-6"
							>
								<path
									d="M12.22 2h-.44a2 2 0 0 0-2 2v.18a2 2 0 0 1-1 1.73l-.43.25a2 2 0 0 1-2 0l-.15-.08a2 2 0 0 0-2.73.73l-.22.38a2 2 0 0 0 .73 2.73l.15.1a2 2 0 0 1 1 1.72v.51a2 2 0 0 1-1 1.74l-.15.09a2 2 0 0 0-.73 2.73l.22.38a2 2 0 0 0 2.73.73l.15-.08a2 2 0 0 1 2 0l.43.25a2 2 0 0 1 1 1.73V20a2 2 0 0 0 2 2h.44a2 2 0 0 0 2-2v-.18a2 2 0 0 1 1-1.73l.43-.25a2 2 0 0 1 2 0l.15.08a2 2 0 0 0 2.73-.73l.22-.39a2 2 0 0 0-.73-2.73l-.15-.08a2 2 0 0 1-1-1.74v-.5a2 2 0 0 1 1-1.74l.15-.09a2 2 0 0 0 .73-2.73l-.22-.38a2 2 0 0 0-2.73-.73l-.15.08a2 2 0 0 1-2 0l-.43-.25a2 2 0 0 1-1-1.73V4a2 2 0 0 0-2-2z"
								></path>
								<circle cx="12" cy="12" r="3"></circle>
							</svg>
							<h2 class="text-xl font-bold">Advanced Customization</h2>
							<p class="dark:text-zinc-100">
								With Advanced Customization, you can personalize your email client to suit your
								preferences and work style.
							</p>
						</div>
						<div class="flex flex-col items-center space-y-2 rounded-lg border-gray-800 p-4">
							<svg
								xmlns="http://www.w3.org/2000/svg"
								width="24"
								height="24"
								viewBox="0 0 24 24"
								fill="none"
								stroke="currentColor"
								stroke-width="2"
								stroke-linecap="round"
								stroke-linejoin="round"
								class="mb-2 h-6 w-6"
							>
								<circle cx="11" cy="11" r="8"></circle>
								<path d="m21 21-4.3-4.3"></path>
							</svg>
							<h2 class="text-xl font-bold">Powerful Search</h2>
							<p class=" dark:text-zinc-100">
								Our Powerful Search feature allows you to find any email, contact, or file in
								seconds.
							</p>
						</div>
						<div class="flex flex-col items-center space-y-2 rounded-lg border-gray-800 p-4">
							<svg
								xmlns="http://www.w3.org/2000/svg"
								width="24"
								height="24"
								viewBox="0 0 24 24"
								fill="none"
								stroke="currentColor"
								stroke-width="2"
								stroke-linecap="round"
								stroke-linejoin="round"
								class="mb-2 h-6 w-6"
							>
								<rect width="18" height="11" x="3" y="11" rx="2" ry="2"></rect>
								<path d="M7 11V7a5 5 0 0 1 10 0v4"></path>
							</svg>
							<h2 class="text-xl font-bold">Reliable Security</h2>
							<p class=" dark:text-zinc-100">
								With Reliable Security, your data is always safe and protected.
							</p>
						</div>
						<div class="flex flex-col items-center space-y-2 rounded-lg border-gray-800 p-4">
							<svg
								xmlns="http://www.w3.org/2000/svg"
								width="24"
								height="24"
								viewBox="0 0 24 24"
								fill="none"
								stroke="currentColor"
								stroke-width="2"
								stroke-linecap="round"
								stroke-linejoin="round"
								class="mb-2 h-6 w-6"
							>
								<path d="m8 6 4-4 4 4"></path>
								<path d="M12 2v10.3a4 4 0 0 1-1.172 2.872L4 22"></path>
								<path d="m20 22-5-5"></path>
							</svg>
							<h2 class="text-xl font-bold">Easy Collaboration</h2>
							<p class=" dark:text-zinc-100">
								Easy Collaboration allows you to share and edit documents with your team in real
								time.
							</p>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</section>

<!-- about us section start -->
<section
	class="flex flex-col items-center justify-center gap-6 px-4 py-6 md:flex-row md:items-start md:gap-12 md:px-6 md:py-12"
>
	<img
		src=""
		alt="About Us"
		width="500"
		height="500"
		class="h-64 w-full rounded-lg object-cover md:h-auto md:w-1/2"
		style="aspect-ratio: 500 / 500; object-fit: cover;"
	/>
	<div class="space-y-4 md:w-1/2">
		<h2 class="text-3xl font-bold tracking-tighter md:text-4xl lg:text-5xl">About Us</h2>
		<p class="text-gray-500 md:text-lg lg:text-xl">
			We are a team of passionate individuals committed to building the best web experiences. Our
			mission is to empower teams of all sizes to create and innovate.
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
