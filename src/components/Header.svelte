<script>
  import Logo from "../reusable/Logo.svelte";
  import DesktopNavigation from "./DesktopNavigation.svelte";


</script>

<header class="header">
  <Logo on:goToHome />
  <div class="header-nav">
    <DesktopNavigation on:changeComponent on:goTo/>
    <button class="btn-mobile-nav" on:click>
      <ion-icon class="icon-mobile-nav" name="menu-outline"></ion-icon>
    </button>
  </div>
</header>

<style>
  .header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: #0C2D48;
    /* It will be sticky */
    height: 8rem;
    padding: 0 4.8rem;
  }

  .header-nav {
    display: flex;
    align-items: center;
    gap: 3.2rem;
  }

  .btn-mobile-nav{
    border: none;
    background-color: #0C2D48;
    cursor: pointer;

    display: none;
  }

  .icon-mobile-nav{
    height: 3.2rem;
    width: 3.2rem;
    color: #fff;
}


/*******************************************/
/* MOBILE NAVIGATION BELOW 944px (Tablets)*/
/******************************************/
@media (max-width: 59em) {
  .btn-mobile-nav {
    display: block;
  }
}  
</style>