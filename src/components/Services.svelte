<script>
import Tabs from '../reusable/Tabs.svelte';
import Cleaning from './Cleaning.svelte';
import Events from './Events.svelte';
import MonumentalMoments from './MonumentalMoments.svelte';

let items = ['Events', 'Cleaning Services', 'Monumental Moments'];
let activeItem = 'Events';
let services = true;

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
        <img src="/img/image7.jpg" class="services-img" alt="services image"/>
      </div>
  </div>
  <div class="services-tabs">
    <Tabs {items} {activeItem} {services} on:tabChange={tabChange}/>
    
    {#if activeItem === 'Events'}
      <Events />
			{:else if activeItem === 'Cleaning Services'}
      <Cleaning />
			{:else if activeItem === 'Monumental Moments'}
			<MonumentalMoments />
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