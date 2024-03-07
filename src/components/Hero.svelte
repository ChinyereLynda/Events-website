<script>
  import Button from "../reusable/Button.svelte";
  // import { slide } from 'svelte/transition';
  // import { onMount } from 'svelte';
  import ClientLogos from "../reusable/ClientLogos.svelte";


  const heroImage = [
		{src: '/img/image7.jpg', alt: 'hero image',  id: 1}    
	];

  // let slideElement = false;

  // onMount(() => {
  //   slideElement = true;
  // }); 
</script>

<section class="section-hero">
  <div class="hero-container">
      <div class="hero-text-box">
          <h1 class="heading-primary">Dazzling Events, Sparkling Spaces</h1>
          <p class="hero-description">Ella Valdez handles the details so you can enjoy the memory.</p>
          <div class="btn-wrap">
            <Button type="secondary" bigger={true} inverse={false} on:click>Book Now</Button>
          </div> 
          <!-- <div class="client-box">
            <ClientLogos />
            <p class="client-text">Super <span>memories</span> created for our clients! </p>
        </div> -->
      </div>

    <!-- {#if slideElement} -->
    <div class="hero-img-box">
      <img src="/img/image7.jpg" class="hero-img" alt="hero image" />
    </div>
    <!-- {/if} in:slide={{delay: 200, axis: "x"}} -->
  </div>
</section>

<style>
  .section-hero  {
    margin-bottom: 9.6rem;
  }

  .hero-container {
    /* max-width: 130rem; */
    margin: 0 auto;
    position: relative;
  }
  
  .hero-text-box {    
    max-width: 60rem;
    margin: 0 auto;
    /* background: rgba(112, 207, 245, 0.8) ; */
    /* background: rgba(208, 239, 251, 0.8); */
    /* background: rgba(19, 174, 236, 0.8); */
    /* background: #13AEEC; */
    background: rgba(207, 213, 217, 0.8);
    color: #0C2D48;
    position: absolute;
    top: 0;
    bottom: 0;
    padding: 9.6rem 1.4rem 0 2.4rem;    
  }
  
  .hero-description {
    font-size: 2rem;
    line-height: 1.6;
    margin-bottom: 4.8rem ;
  }

  .hero-img-box {
    transition: all 0.4s;
  }
  
  .hero-img {
    display: block;
    width: 100%;
    height: 100vh;    
  }
    
  /* .btn-wrap {
    text-align: right;
  } */

  /* .client-box {
    display: flex;
    align-items: center;
    gap: 1.6rem;
    margin-top: 8rem;
  }

  .client-text {
    font-size: 1.8rem;
    font-weight: 600;
  }

  .client-text span{
    color: gold;
    font-weight: 700;
  } */

</style>