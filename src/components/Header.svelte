<script>
  import Logo from "../reusable/Logo.svelte";
  import MobileNav from "./MobileNav.svelte";
  import Navigation from "./Navigation.svelte";

</script>

<header class="header">
  <Logo on:goToHome />
  <Navigation on:changeComponent on:goTo/>
  <!-- <MobileNav /> -->
</header>

<style>
  .header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: darkblue;
    /* It will be sticky */
    height: 8rem;
    padding: 0 4.8rem;
  }



/*******************************************/
/* MOBILE NAVIGATION BELOW 944px (Tablets)*/
/******************************************/
/* @media (max-width: 59em) {
  .header {
    width: 100%;
    height: 100vh; 
    align-items: flex-start;
    padding: 2.4rem ;
    
  }
}  */


</style>