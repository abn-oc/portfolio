<script lang="ts">
  import ProjectCard from '$lib/ProjectCard.svelte';
</script>

<div class="w-full flex flex-col items-center gap-4">
  <h2 class="text-2xl font-bold text-gray-100 mb-2">Projects</h2>
  <div class="grid grid-cols-1 md:grid-cols-2 gap-6 w-full max-w-3xl">
    <ProjectCard title="Project One" description="A short description of your first project." />
    <ProjectCard title="Project Two" description="A short description of your second project." />
  </div>
</div> 