<script lang="ts">
  import { fade } from 'svelte/transition';
  let show: boolean = true;

  function dismiss(): void {
    show = false;
  }
</script>

{#if show}
  <div
    class="fixed top-3 left-1/2 -translate-x-1/2 z-50 w-[95vw] max-w-md rounded-2xl shadow-xl bg-gray-900/95 border border-pink-400/40 text-pink-200 px-4 py-3 flex justify-between items-center md:hidden"
    transition:fade
  >
    <div>
      <p class="font-bold text-base mb-1">Notice</p>
      <p class="text-xs">This website is better experienced on desktop.</p>
    </div>
    <button
      class="ml-4 bg-pink-400/20 text-pink-200 font-semibold rounded px-3 py-1 hover:bg-pink-400/40 transition"
      on:click={dismiss}
    >
      Okay
    </button>
  </div>
{/if}