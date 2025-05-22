<script lang="ts">
	import MobileBanner from '$lib/MobileBanner.svelte';
	import '../app.css';
</script>

<!-- Outer wrapper: gradient and centering only on sm and up -->
<div class="min-h-screen bg-gray-900 dark bg-gradient-to-br from-gray-900 to-gray-800 sm:flex sm:items-center sm:justify-center">
  <MobileBanner />
  <!-- Card: only on sm and up -->
  <div class="w-full sm:max-w-5xl sm:rounded-3xl sm:shadow-2xl sm:bg-gray-900/90 sm:dark:bg-gray-900/90 sm:p-0 sm:overflow-hidden sm:flex sm:flex-col">
    <!-- Banner: only on sm and up -->
    <div class="hidden sm:flex h-48 w-full bg-gradient-to-r from-indigo-700 via-purple-700 to-pink-700 items-end justify-start relative">
      <img src="/banner.jpg" alt="Banner" class="absolute inset-0 w-full h-full object-cover opacity-40 pointer-events-none select-none" />
      <div class="z-10 p-6">
        <h1 class="text-3xl font-bold text-white drop-shadow-lg">My Portfolio</h1>
      </div>
    </div>
    <div class="flex flex-col sm:flex-row flex-1 min-h-[100vh] sm:min-h-[400px]">
      <!-- Navigation: horizontal on mobile, vertical on sm+ -->
      <nav class="w-full sm:w-48 flex flex-row sm:flex-col gap-2 bg-gray-800/80 p-2 sm:p-6 border-b sm:border-b-0 sm:border-r border-gray-700 justify-center sm:justify-start">
        <a href="/" class="flex-1 sm:flex-none text-base sm:text-lg font-medium text-gray-200 hover:text-pink-400 transition rounded-lg px-2 py-2 sm:px-3 sm:py-2 text-center">Welcome</a>
        <a href="/aboutme" class="flex-1 sm:flex-none text-base sm:text-lg font-medium text-gray-200 hover:text-pink-400 transition rounded-lg px-2 py-2 sm:px-3 sm:py-2 text-center">about</a>
        <a href="/projects" class="flex-1 sm:flex-none text-base sm:text-lg font-medium text-gray-200 hover:text-pink-400 transition rounded-lg px-2 py-2 sm:px-3 sm:py-2 text-center">projects</a>
        <a href="/skills" class="flex-1 sm:flex-none text-base sm:text-lg font-medium text-gray-200 hover:text-pink-400 transition rounded-lg px-2 py-2 sm:px-3 sm:py-2 text-center">skills</a>
      </nav>
      <!-- Main Content -->
      <main class="flex-1 p-4 sm:p-8 flex flex-col items-center justify-center min-w-0">
        <slot />
      </main>
      <!-- Socials: horizontal on mobile, vertical on sm+ -->
      <aside class="w-full sm:w-48 flex flex-row sm:flex-col items-center sm:items-end justify-center sm:justify-between p-2 sm:p-6 bg-gray-800/80 border-t sm:border-t-0 sm:border-l border-gray-700 gap-3 sm:gap-0">
        <div class="flex flex-row sm:flex-col gap-3 items-center sm:items-end w-full sm:w-auto justify-center">
          <a href="#" class="text-gray-300 hover:text-pink-400 transition" aria-label="GitHub">github</a>
          <a href="#" class="text-gray-300 hover:text-pink-400 transition" aria-label="LinkedIn">linkedin</a>
          <a href="#" class="text-gray-300 hover:text-pink-400 transition" aria-label="Instagram">instagram</a>
        </div>
      </aside>
    </div>
  </div>
</div>
