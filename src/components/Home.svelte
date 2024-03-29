<script>
	import Hero from "./Hero.svelte";
  import WhoWeAre from "./WhoWeAre.svelte";
  import { onMount } from 'svelte';

  onMount(() => {
    window.scrollTo({
      top: 0,
      left: 0,
      behavior: 'smooth',
    });
  });
</script>

<div>
  <Hero on:click />
  <WhoWeAre />
</div>

<style>

</style>