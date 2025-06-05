<script lang="ts">
	export let name: String;
	export let description: String;
	export let tags: String[];
    export let Link: string | null;
    export let github: string | null;
</script>

<div class="border">
	<p class="text-bold">
		{name}
	</p>
	<p class="text-neutral-500">
		{description}
	</p>
	{#each tags as tag}
		<p class="text-blue-500">tag</p>
	{/each}
    {#if Link}
    <a href={Link}>linkkk</a>
    {/if}
    {#if github}
    <a href={github}>githubbb</a>
    {/if}
</div>
