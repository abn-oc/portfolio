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
	class="flex w-1/4 flex-col gap-1 rounded-md border border-neutral-300 shadow-sm transition-shadow duration-100 hover:shadow-md"
>
	<img src={image} alt={name} class="h-auto w-full object-cover rounded-t-md" />

	<div class="flex flex-col gap-2 p-2 px-4">
		<p class="text-xl font-semibold text-neutral-900">{name}</p>

		<p class="text-sm text-neutral-700">{description}</p>

		<div class="flex flex-wrap gap-2">
			{#each tags as tag}
				<span
					class="rounded-full border border-blue-300 bg-blue-100 px-3 py-1 text-xs text-blue-600"
					>{tag}</span
				>
			{/each}
		</div>

		<div class="mt-2 ml-auto flex gap-4">
			{#if Link}
				<a
					href={Link}
					target="_blank"
					class="flex items-center gap-1 text-sm text-blue-600 hover:underline"
				>
					<div class="h-8 w-8 hover:text-blue-800">
						<FaExternalLinkAlt />
					</div>
				</a>
			{/if}
			{#if github}
				<a
					href={github}
					target="_blank"
					class="flex items-center gap-1 text-sm text-gray-700 hover:underline"
				>
					<div class="h-8 w-8 hover:text-neutral-950">
						<FaGithub />
					</div>
				</a>
			{/if}
		</div>
	</div>
</div>
