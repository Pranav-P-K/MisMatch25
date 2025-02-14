<script lang="ts">
  import { fade } from 'svelte/transition';
</script>

<svelte:head>
  <link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap" rel="stylesheet">
</svelte:head>

<div class="relative mx-auto max-w-3xl p-6">
  <div class="rounded-lg border border-purple-500 bg-black/90 p-8 shadow-[0_0_20px_rgba(0,149,255,0.5)] backdrop-blur-sm">
    <h2 class="arcade-text mb-6 text-center text-2xl text-[#04d1d1]">
      Prize Pool
    </h2>
    <div class="relative flex md:flex-row md:gap-4 flex-col items-center justify-center">
      <img src="/coins.png" class="w-27 text-purple-500" alt="controller" />
      <p class="arcade-text text-center text-xl text-[#FF1493]">
          It's a Surprise!<br>
          <br>
        It's hugeeee!
      </p>
      <div class="absolute -inset-1 -z-10 blur animation:pulse" transition:fade="{{ duration: 2000 }}">
      </div>
  </div>
</div>
</div>
<style>
  :global(.arcade-text) {
    font-family: 'Press Start 2P', cursive;
    text-shadow: 0 0 10px;
  }

  .blur {
    animation: pulse 2s infinite;
  }

  @keyframes pulse {
    0%, 100% { opacity: 0.5; }
    50% { opacity: 0.8; }
  }
</style>