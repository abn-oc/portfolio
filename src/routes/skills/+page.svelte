<script lang="ts">
  import SkillBadge from '$lib/SkillBadge.svelte';
</script>

<div class="w-full flex flex-col items-center gap-4">
  <h2 class="text-2xl font-bold text-gray-100 mb-2">Skills</h2>
  <div class="flex flex-wrap gap-3 justify-center w-full max-w-2xl">
    <SkillBadge skill="Svelte" />
    <SkillBadge skill="TypeScript" />
    <SkillBadge skill="TailwindCSS" />
    <SkillBadge skill="Node.js" />
    <SkillBadge skill="Python" />
    <SkillBadge skill="React" />
    <SkillBadge skill="SQL" />
  </div>
</div>