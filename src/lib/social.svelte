<script lang="ts">
	export let name: string;
	export let url: string;
	export let icon: any;
</script>

<a class="bg-neutral-50 text-neutral-950 font-semibold w-fit rounded-lg p-1 px-3 hover:bg-neutral-200 flex items-center gap-2" href={url} target="_blank">
	<div class="w-5">
		<!-- <svelte:component this={icon} /> -->
		{#if typeof icon === 'string'}
			<img src={icon} alt={name} />
		{:else}
			<svelte:component this={icon} />
		{/if}
	</div>
	{name}
</a>
