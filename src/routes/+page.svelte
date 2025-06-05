<script lang="ts">
	import Dividor from '$lib/dividor.svelte';
	import Social from '$lib/social.svelte';
	import FaGithub from 'svelte-icons/fa/FaGithub.svelte';
	import FaLinkedinIn from 'svelte-icons/fa/FaLinkedinIn.svelte';
</script>

<!-- screen -->
<div class="h-screen w-screen flex flex-col gap-8">
	<!-- header -->
	<div class="flex flex-col w-[100vw] gap-4 py-8 px-24 bg-blue-800 text-white">
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
	 </div>
</div>