<script>
  import Tabs from "../reusable/Tabs.svelte";
  import Button from "../reusable/Button.svelte";

  export let showMobileNav = false;
  
  let items = ['Home', 'About', 'Our Services', 'Gallery', 'Contact'];
  let activeItem = 'Home';
  let column = true;
  

const tabChange = (e) => {
	activeItem = e.detail;  
}

const clearActiveItem = () => {
  activeItem = '';
}
</script>

{#if showMobileNav}
  <nav class="mobile-nav">  
    <div class="mobile-btn">
      <button class="btn-mobile-nav" on:click>
        <ion-icon class="icon-mobile-nav" name="close-outline"></ion-icon>
      </button>   
    </div>   

    <div class="mobile-nav-links">
      <Tabs {items} {activeItem} {column} on:tabChange={tabChange} on:changeComponent />
      <div class="main-nav-btn">
        <Button bigger={true} on:goTo on:click={clearActiveItem}>Book Now</Button>
      </div>
    </div>
  </nav>
{/if}


<style>
  .mobile-nav {
    background-color: rgba(12, 44, 70, 0.7);
    width: 100%;
    height: 100vh;
    position: fixed;
    z-index: 1;
  }

  .mobile-btn {
    display: flex;
    justify-content: right;
  }

  .btn-mobile-nav{
    margin: 2.4rem  4.8rem ;
    border: none;
    background-color: rgba(0, 0, 139, 0.26);
    cursor: pointer;
    
  }

  .icon-mobile-nav{
    height: 3.2rem;
    width: 3.2rem;
    color: #fff;
}

  .mobile-nav-links {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    gap: 4.8rem;
  }
  

</style>