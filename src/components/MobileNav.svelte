<script>

</script>

<button class="btn-mobile-nav">
  <ion-icon class="icon-mobile-nav" name="menu-outline"></ion-icon>
  <ion-icon class="icon-mobile-nav" name="close-outline"></ion-icon>
</button>



<style>
.btn-mobile-nav{
  border: none;
  background-color: darkblue;
  cursor: pointer;

  display: none;
}

.icon-mobile-nav{
  height: 3.2rem;
  width: 3.2rem;
  color: #fff;
}

.icon-mobile-nav[name="close-outline"] {
  display: none;
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

