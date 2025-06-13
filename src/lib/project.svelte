<script lang="ts">
	import FaExternalLinkAlt from 'svelte-icons/fa/FaExternalLinkAlt.svelte';
	import FaGithub from 'svelte-icons/fa/FaGithub.svelte';

	export let name: string;
	export let description: string;
	export let tags: string[];
	export let image: string;
	export let Link: string | null;
	export let github: string | null;
</script>

<div
	class="flex sm:w-1/4 w-1/1 flex-col gap-1 rounded-md border shadow-sm transition-shadow duration-100 hover:shadow-md"
	style="background: var(--card-bg); border-color: var(--card-border);"
>
	<img src={image} alt={name} class="h-48 w-full object-cover rounded-t-md" />

	<div class="flex flex-col gap-2 p-2 px-4">
		<p class="text-xl font-semibold" style="color: var(--card-text);">{name}</p>

		<p class="text-sm" style="color: var(--card-text-secondary);">{description}</p>

		<div class="flex flex-wrap gap-2">
			{#each tags as tag}
				<span
					class="rounded-full border px-3 py-1 text-xs"
					style="border-color: var(--card-border); color: var(--card-text); background: var(--card-bg);"
					>{tag}</span
				>
			{/each}
		</div>

		<div class="mt-2 ml-auto flex gap-4">
			{#if Link}
				<a
					href={Link}
					target="_blank"
					class="flex items-center gap-1 text-sm hover:underline"
					style="color: var(--card-text);"
				>
					<div class="h-8 w-8 hover:opacity-80">
						<FaExternalLinkAlt />
					</div>
				</a>
			{/if}
			{#if github}
				<a
					href={github}
					target="_blank"
					class="flex items-center gap-1 text-sm hover:underline"
					style="color: var(--card-text);"
				>
					<div class="h-8 w-8 hover:opacity-80">
						<FaGithub />
					</div>
				</a>
			{/if}
		</div>
	</div>
</div>
