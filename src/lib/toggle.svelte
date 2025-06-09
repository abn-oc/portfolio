<script lang="ts">
	let darkMode = false;
	function toggle() {
		darkMode = !darkMode;
		window.document.body.classList.toggle('dark');
	}
</script>

<button
	on:click={toggle}
	class="p-2 rounded cursor-pointer text-xl hover:bg-gray-900/25"
>
	{#if darkMode}
		<span>🌙</span>
	{:else}
		<span>☀️</span>
	{/if}
</button>