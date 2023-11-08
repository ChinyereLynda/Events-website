<script>
import Tabs from '../reusable/Tabs.svelte';
import Button from '../reusable/Button.svelte';
//navigation tabs
let items = ['Home', 'About', 'Our Services', 'Gallery', 'Contact'];
let activeItem = 'Home';

const tabChange = (e) => {
	activeItem = e.detail;  
  // if (!items.includes(e.detail)) {activeItem = ''}
}

const clearActiveItem = () => {
  activeItem = '';
}
</script>

<nav class="main-nav">
    <Tabs {items} {activeItem} on:tabChange={tabChange} on:changeComponent /> 
    <div class="main-nav-btn">
      <Button bigger={true} on:goTo on:click={clearActiveItem}>Book Now</Button>
    </div>    
</nav>

<style>
  .main-nav {
    display: flex;
    align-items: center;
    gap: 3.2rem;
  }
  

/*******************************************/
/* MOBILE NAVIGATION BELOW 944px (Tablets)*/
/******************************************/
@media (max-width: 59em) {
  .main-nav {
    display: none;
  }
}



</style>