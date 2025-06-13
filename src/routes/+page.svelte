<script lang="ts">
	import Dividor from '$lib/dividor.svelte';
	import Social from '$lib/social.svelte';
	import Project from '$lib/project.svelte';
	import FaGithub from 'svelte-icons/fa/FaGithub.svelte';
	import FaLinkedinIn from 'svelte-icons/fa/FaLinkedinIn.svelte';
	import FaPhoneAlt from 'svelte-icons/fa/FaPhoneAlt.svelte';
	import FaRegEnvelope from 'svelte-icons/fa/FaRegEnvelope.svelte';
	import { copyClipboard } from '$lib/copy.svelte';
	import Toggle from '$lib/toggle.svelte';
</script>

<!-- screen -->
<div class="flex h-screen w-screen flex-col gap-8">
	<!-- header -->
	<div
		class="flex h-auto w-full flex-col-reverse flex-wrap px-12 text-white sm:h-45 sm:flex-row sm:px-24 sm:overflow-hidden"
		style="background: var(--header-bg);"
	>
		<div class="flex flex-col gap-4 py-8">
			<div class="flex flex-row gap-2 items-center">
				<h1 class="text-center text-3xl sm:text-left">Abdullah Ihtasham</h1>
				<Toggle />
			</div>
			<p class="text-md text-center sm:text-left">
				A 2nd Year CS Student from FAST NUCES Lahore. Currently focusing on web dev.
			</p>
			<div class="flex flex-row flex-wrap justify-center gap-4 sm:justify-start">
				<Social
					name="Linkedin"
					url="https://www.linkedin.com/in/abdullah-ihtasham-738011223/"
					icon={FaLinkedinIn}
				/>
				<Social name="Github" url="https://github.com/abn-oc" icon={FaGithub} />
				<Social name="Leetcode" url="https://leetcode.com/u/abnoc/" icon="/leetcode.svg" />
			</div>
		</div>
		<img src="/me.png" alt="me" class="relative top-5 mx-auto h-45 w-45 sm:mr-18 sm:ml-auto" />
	</div>
	<!-- Projects -->
	<div class="flex flex-grow flex-col px-12 sm:px-24">
		<h2 class="text-2xl">Projects</h2>
		<!-- projects -->
		<div class="mt-4 flex flex-col flex-wrap gap-4 sm:flex-row">
			<Project
				name="Watch Next"
				description="WatchList + Reviews writing webapp"
				tags={['Nextjs', 'Supabase', 'Shadcn']}
				image="/watch-next.png"
				Link="https://watch-next-drab.vercel.app/"
				github="https://github.com/abn-oc/watch-next"
			/>
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
	<div
		class="flex flex-col justify-evenly gap-4 p-8 py-8 text-white sm:flex-row sm:gap-0 sm:p-4 sm:py-4"
		style="background: var(--header-bg);"
	>
		<div class="flex flex-row items-center gap-4">
			<div class="w-5"><FaRegEnvelope /></div>
			<!-- <p>abdullah.iht22@gmail.com</p> -->
			<button
				class="hover:cursor-pointer hover:text-gray-300"
				onclick={() => copyClipboard('abdullah.iht22@gmail.com')}>abdullah.iht22@gmail.com</button
			>
		</div>
		<div class="flex flex-row items-center gap-4">
			<div class="w-4"><FaPhoneAlt /></div>
			<!-- <p>+92 300 4602868</p> -->
			<button
				class="hover:cursor-pointer hover:text-gray-300"
				onclick={() => copyClipboard('+92 300 4602868')}>+92 300 4602868</button
			>
		</div>
	</div>
</div>

<style>
	:root {
		--bg-color: #ffffff;
		--text-color: #000000;
		--header-bg: #1e40af; /* blue-800 */
		--card-bg: #ffffff;
		--card-border: #e5e7eb;
		--card-text: #111827;
		--card-text-secondary: #4b5563;
		--social-bg: #f9fafb;
		--social-text: #111827;
		--social-hover: #e5e7eb;
	}

	:global(body) {
		background: var(--bg-color);
		color: var(--text-color);
	}

	:global(body.dark) {
		--bg-color: #111827;
		--text-color: #ffffff;
		--header-bg: #1f2937;
		--card-bg: #1f2937;
		--card-border: #374151;
		--card-text: #f9fafb;
		--card-text-secondary: #d1d5db;
		--social-bg: #374151;
		--social-text: #f9fafb;
		--social-hover: #4b5563;
	}
</style>
