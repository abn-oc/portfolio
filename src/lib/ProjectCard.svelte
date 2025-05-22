<script lang="ts">
  export let title: string;
  export let description: string;
  export let link: string
</script>

<div class="bg-gray-800 rounded-xl p-6 shadow-lg flex flex-col gap-2">
  <h3 class="text-lg font-semibold text-blue-400">{title}</h3>
  <p class="text-gray-300">{description}</p>
  <a href={link} class="text-blue-300 hover:text-pink-400 transition hover:underline" aria-label="GitHub">visit repo ></a>
</div> 