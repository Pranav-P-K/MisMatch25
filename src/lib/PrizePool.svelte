<script lang="ts">
  import { fade } from 'svelte/transition';
  import { onMount } from 'svelte';
  
  let prizeAmount = 0;
  const targetAmount = 10000;
  
  onMount(() => {
    let step = Math.ceil(targetAmount / 50);
    let interval = setInterval(() => {
      prizeAmount += step;
      if (prizeAmount >= targetAmount) {
        prizeAmount = targetAmount;
        clearInterval(interval);
      }
    }, 30); 
  });
</script>

<svelte:head>
  <link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap" rel="stylesheet">
</svelte:head>

<div id="prize" class="relative mx-auto max-w-3xl p-6 mt-32 mb-16">
  <div class="rounded-lg border border-purple-500 bg-black/90 p-8 shadow-[0_0_20px_rgba(0,149,255,0.5)] backdrop-blur-sm">
    <h2 class="arcade-text mb-6 text-center text-2xl text-[#04d1d1]">
      Prize Pool
    </h2>
    <div class="relative flex md:flex-row md:gap-4 flex-col items-center justify-center">
      <img src="/coins.png" class="w-27 text-purple-500" alt="controller" />
      <p class="arcade-text text-center text-4xl md:text-5xl lg:text-7xl text-[#fffb14]" transition:fade={{ duration: 2000 }}>
        {prizeAmount.toLocaleString()}
      </p>
    </div>
  </div>
</div>

<style>
  :global(.arcade-text) {
    font-family: 'Press Start 2P', cursive;
    text-shadow: 0 0 10px;
  }
</style>
