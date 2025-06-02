<script lang="ts">
	import Dividor from '$lib/dividor.svelte';
	import Social from '$lib/social.svelte';
	import DiGithubBadge from 'svelte-icons/di/DiGithubBadge.svelte';
    import FaLinkedinIn from 'svelte-icons/fa/FaLinkedinIn.svelte'
</script>

<div class="flex h-screen w-screen flex-col bg-neutral-950 text-white">
	<h1>Abdullah Ihtasham</h1>
	<p>A 2nd Year CS Student from FAST NUCES Lahore. Currently focusing on web dev.</p>
	<div class="flex flex-row gap-4">
		<Social name="Linkedin" url="#" />
		<Social name="Github" url="#" />
	</div>
	<Dividor />
	<h2>Projects</h2>
</div>
