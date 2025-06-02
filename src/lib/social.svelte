<script lang="ts">
	export let name: string;
	export let url: string;
</script>

<a class="bg-neutral-50 text-neutral-950 font-semibold w-fit rounded-lg p-1 px-3 hover:bg-neutral-200" href={url}>
	{name}
</a>
