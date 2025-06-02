<script lang="ts">
	import Dividor from '$lib/dividor.svelte';
	import Social from '$lib/social.svelte';
	import FaGithub from 'svelte-icons/fa/FaGithub.svelte';
	import FaLinkedinIn from 'svelte-icons/fa/FaLinkedinIn.svelte';
</script>

<div class="h-screen w-screen bg-neutral-950 py-12">
	<div class="flex flex-col gap-4 text-white mx-auto w-[80vw] overflow-hidden">
		<h1 class="text-3xl">Abdullah Ihtasham</h1>
		<p class="text-md">A 2nd Year CS Student from FAST NUCES Lahore. Currently focusing on web dev.</p>
		<div class="flex flex-row gap-4">
			<Social name="Linkedin" url="#" icon={FaLinkedinIn} />
			<Social name="Github" url="#" icon={FaGithub} />
		</div>
		<Dividor />
		<h2 class="text-2xl">Projects</h2>
	</div>
</div>
