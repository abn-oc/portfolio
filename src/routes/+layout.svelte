<script lang="ts">
	import '../app.css';
</script>

<div class="min-h-screen flex items-center justify-center bg-gradient-to-br from-gray-900 to-gray-800 dark">
  <div class="w-full max-w-5xl rounded-3xl shadow-2xl bg-gray-900/90 dark:bg-gray-900/90 p-0 overflow-hidden flex flex-col">
    <!-- Banner -->
    <div class="h-48 w-full bg-gradient-to-r from-indigo-700 via-purple-700 to-pink-700 flex items-end justify-start relative">
      <img src="/banner.jpg" alt="Banner" class="absolute inset-0 w-full h-full object-cover opacity-40 pointer-events-none select-none" />
      <div class="z-10 p-6">
        <h1 class="text-3xl font-bold text-white drop-shadow-lg">My Portfolio</h1>
      </div>
    </div>
    <div class="flex flex-1 min-h-[400px]">
      <!-- Navigation -->
      <nav class="w-48 flex flex-col gap-2 bg-gray-800/80 p-6 border-r border-gray-700">
        <a href="/" class="text-lg font-medium text-gray-200 hover:text-pink-400 transition rounded-lg px-3 py-2">Welcome</a>
        <a href="/aboutme" class="text-lg font-medium text-gray-200 hover:text-pink-400 transition rounded-lg px-3 py-2">about</a>
        <a href="/projects" class="text-lg font-medium text-gray-200 hover:text-pink-400 transition rounded-lg px-3 py-2">projects</a>
        <a href="/skills" class="text-lg font-medium text-gray-200 hover:text-pink-400 transition rounded-lg px-3 py-2">skills</a>
      </nav>
      <!-- Main Content -->
      <main class="flex-1 p-8 flex flex-col items-center justify-center">
        <slot />
      </main>
      <!-- Socials -->
      <aside class="w-48 flex flex-col items-end justify-between p-6 bg-gray-800/80 border-l border-gray-700">
        <div class="flex flex-col gap-4 items-end">
          <a href="#" class="text-gray-300 hover:text-pink-400 transition" aria-label="GitHub">github</a>
          <a href="#" class="text-gray-300 hover:text-pink-400 transition" aria-label="GitHub">linkedin</a>
          <a href="#" class="text-gray-300 hover:text-pink-400 transition" aria-label="GitHub">instagram</a>
        </div>
      </aside>
    </div>
  </div>
</div>
