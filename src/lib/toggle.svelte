<script lang="ts">
	let darkMode = false;
	function toggle() {
        darkMode = !darkMode;
        window.document.body.classList.toggle('dark');
    }
</script>

<button on:click={toggle} class="border p-1 rounded-xl">
	{#if darkMode }
		Go light
	{:else}
		Go dark
	{/if}
</button>