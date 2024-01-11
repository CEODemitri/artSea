<script>
	import { goto } from '$app/navigation';

	function moveAround() {
		goto('/collections');
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

<style>
</style>
