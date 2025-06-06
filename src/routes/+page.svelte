<script lang="ts">
	import Dividor from '$lib/dividor.svelte';
	import Social from '$lib/social.svelte';
	import Project from '$lib/project.svelte';
	import FaGithub from 'svelte-icons/fa/FaGithub.svelte';
	import FaLinkedinIn from 'svelte-icons/fa/FaLinkedinIn.svelte';
	import FaPhoneAlt from 'svelte-icons/fa/FaPhoneAlt.svelte'
	import FaRegEnvelope from 'svelte-icons/fa/FaRegEnvelope.svelte'
</script>

<!-- screen -->
<div class="flex h-screen w-screen flex-col gap-8">
	<!-- header -->
	<div class="flex w-[100vw] h-45 flex-row bg-blue-800 px-24 text-white">
		<div class="flex flex-col gap-4 py-8">
			<h1 class="text-3xl">Abdullah Ihtasham</h1>
			<p class="text-md">
				A 2nd Year CS Student from FAST NUCES Lahore. Currently focusing on web dev.
			</p>
			<div class="flex flex-row gap-4">
				<Social name="Linkedin" url="https://www.linkedin.com/in/abdullah-ihtasham-738011223/" icon={FaLinkedinIn} />
				<Social name="Github" url="https://github.com/abn-oc" icon={FaGithub} />
				<Social name="Leetcode" url="https://leetcode.com/u/abnoc/" icon="/leetcode.svg" />
			</div>
		</div>
		<img src="/me.png" alt="me" class="ml-auto mr-18 relative top-5">
	</div>
	<!-- Projects -->
	<div class="flex flex-col px-24 flex-grow">
		<h2 class="text-2xl">Projects</h2>
		<!-- projects -->
		<div class="mt-4 flex flex-row gap-4">
			<Project
				name="12 Beads"
				description="Local two player Board game"
				tags={['C++', 'Raylib']}
				image="/12beads.png"
				Link=""
				github="https://github.com/abn-oc/12-Beads"
			/>
		</div>
	</div>
	<!-- Footer -->
	 <div class="bg-blue-800 flex flex-row justify-evenly p-4 text-white">
		<div class="flex flex-row gap-4 items-center">
			<div class="w-5"><FaRegEnvelope/></div>
			<p>abdullah.iht22@gmail.com</p>
		</div>
		<div class="flex flex-row gap-4 items-center">
			<div class="w-4"><FaPhoneAlt/></div>
			<p>+92 300 4602868</p>
		</div>
	 </div>
</div>
