<script lang="ts">
	import favicon from '$lib/assets/favicon.svg';
	import "../app.css";

	let { children } = $props();


</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<nav>
	<ul class="flex gap-4 p-4 bg-gray-800 text-white">
		<li><a href="/" class="hover:underline">Dashboard</a></li>
		<li><a href="/projects" class="hover:underline">Projects</a></li>
		<li><a href="/tasks" class="hover:underline">Tasks</a></li>
	</ul>
</nav>

<style lang="postcss">
  @reference "tailwindcss";

  :global(html) {
    background-color: theme(--color-gray-100);
  }
</style>

{@render children()}
