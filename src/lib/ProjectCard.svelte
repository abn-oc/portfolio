<script lang="ts">
  export let title: string;
  export let description: string;
</script>

<div class="bg-gray-800 rounded-xl p-6 shadow-lg flex flex-col gap-2">
  <h3 class="text-lg font-semibold text-pink-400">{title}</h3>
  <p class="text-gray-300">{description}</p>
</div> 