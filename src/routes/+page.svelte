<script lang="ts">
	import Dividor from '$lib/dividor.svelte';
	import Social from '$lib/social.svelte';
	import Project from '$lib/project.svelte';
	import FaGithub from 'svelte-icons/fa/FaGithub.svelte';
	import FaLinkedinIn from 'svelte-icons/fa/FaLinkedinIn.svelte';
</script>

<!-- screen -->
<div class="flex h-screen w-screen flex-col gap-8">
	<!-- header -->
	<div class="flex w-[100vw] flex-col gap-4 bg-blue-800 px-24 py-8 text-white">
		<h1 class="text-3xl">Abdullah Ihtasham</h1>
		<p class="text-md">
			A 2nd Year CS Student from FAST NUCES Lahore. Currently focusing on web dev.
		</p>
		<div class="flex flex-row gap-4">
			<Social name="Linkedin" url="#" icon={FaLinkedinIn} />
			<Social name="Github" url="#" icon={FaGithub} />
		</div>
	</div>
	<!-- Projects -->
	<div class="flex flex-col px-24">
		<h2 class="text-2xl">Projects</h2>
		<!-- projects -->
		<div>
			<Project
				name="pname"
				description="app i made"
				tags={['skill1', 'skill2']}
				Link=""
				github=""
			/>
		</div>
	</div>
</div>
