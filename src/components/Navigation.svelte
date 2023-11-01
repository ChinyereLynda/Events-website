<script>
import Tabs from '../reusable/Tabs.svelte';
import Button from '../reusable/Button.svelte';
// import MobileNav from './MobileNav.svelte';
//navigation tabs
let items = ['Home', 'About', 'Our Services', 'Gallery', 'Contact'];
let activeItem = 'Home';

const tabChange = (e) => {
	activeItem = e.detail;  
}

const clearActiveItem = () => {
  activeItem = '';
}

</script>

<nav class="main-nav">
  <div class="links-nav">
    <Tabs {items} {activeItem} on:tabChange={tabChange} on:changeComponent /> <!--Please specify if column={true} in @media max-width=59em -->
    <div class="main-nav-btn">
      <Button bigger={true} on:goTo on:click={clearActiveItem}>Book Now</Button>
    </div>
  </div>
</nav>

<style>
  .links-nav {
    display: flex;
    align-items: center;
    gap: 3.2rem;
  }

/*******************************************/
/* MOBILE NAVIGATION BELOW 944px (Tablets)*/
/******************************************/
/* @media (max-width: 59em) {
  .main-nav {
    background-color: rgba(255, 0, 0, 0.623);
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100vh;

    display: flex;
    align-items: center;
    justify-content: center;      
  }

  .links-nav {
    flex-direction: column;
    gap: 4.8rem;
  }  
} */



</style>