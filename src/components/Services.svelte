<script>

import Tabs from '../reusable/Tabs.svelte';
import Events from './Events.svelte';

let items = ['Events', 'Cleaning Services', 'Monumental Moments'];
let activeItem = 'Events';
const color = '#fff';
const background = 'darkblue';
const gap = '0';
const border = '#fff solid 1px';
const padding = '0.4rem 1.2rem';
const borderRadius = '6px';

const tabChange = (e) => {
	activeItem = e.detail;  
}


</script>

<section class="section-services">
  <div class="services-container">
      <div class="services-text-box">
          <h1 class="heading-primary">Our Services</h1>
          <p class="services-description">Lorem ipsum dolor sit amet consectetur adipisicing elit. Illum quisquam nulla, non vero voluptatum blanditiis quis, ex dolorem.</p>          
      </div>

      <div class="services-img-box">
        <img src="/img/image1.jpg" class="services-img" alt="services image"/>
      </div>
  </div>
  <div class="services-tabs">
    <Tabs {borderRadius} {border} {padding} {gap} {color} {background} {items} {activeItem} on:tabChange={tabChange}/>
    
    {#if activeItem === 'Events'}
      <Events />
			{:else if activeItem === 'Cleaning Services'}
			<p> Cleaning Services here!</p>
			{:else if activeItem === 'Monumental Moments'}
			<p>Monumental Moments here!</p>
		{/if}

  </div>
</section>

<style>
  .services-container {
    margin: 0 auto;
    position: relative;
  }
  
  .services-text-box {    
    max-width: 70%;
    max-height: 70%;
    margin: 0 auto;
    background: rgb(179, 179, 220, 0.8);
    color: darkblue;
    position: absolute;
    top: 50%;
    transform: translate(0, -50%);
    padding: 4.8rem 1.4rem 0 2.4rem;    
  }
  
  .services-description {
    font-size: 2rem;
    line-height: 1.6;
    margin-bottom: 4.8rem ;
  }

  .services-img {
    width: 100%;
    max-height: 60vh;
  }

  .services-tabs {
    margin: 0 auto;
    margin-top: 4.8rem;
  }
    
</style>