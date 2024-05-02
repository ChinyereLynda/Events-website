<script>
  import Logo from "../reusable/Logo.svelte";
  import Tabs from "../reusable/Tabs.svelte";

  let items = ['Home', 'About', 'Our Services', 'Gallery', 'Contact', 'Terms'];
  let activeItem = '';
  let footer = true;
  

const tabChange = (e) => {
	activeItem = e.detail;  
}
</script>

<footer class="footer">
  <div class="container grid grid--3-cols">

    <div class="logo-col">  
      <div class="footer-logo">
        <Logo on:goToHome />
      </div>
      <ul class="social-links">
        <li><a class="social-link" href="#top" target="_blank"><ion-icon class="social-icon" name="logo-instagram"></ion-icon></a></li>
        <li><a class="social-link" href="#top" target="_blank"><ion-icon class="social-icon" name="logo-facebook"></ion-icon></a></li>
        <li><a class="social-link" href="#top" target="_blank"><ion-icon class="social-icon" name="logo-twitter"></ion-icon></a></li>
      </ul>

      <p> 
      <a class="copyright"> Copyright &copy; Ella Valdez Ltd. All rights reserved </a> <br />
      <a class="copyright" href="https://paschalogu.com" target="_blank"> Built with &hearts; by Paschal Ogu. </a> 
      </p>
    </div>

    <div class="address-col">
      <p class="footer-heading">Contact us</p>
      <address class="contacts">
        <!-- <p class="address">63 Lorem St., 2nd Floor, Ipso Lorem.</p> -->
        <p>
          <a class="social-link" href="tel:234 703 7386 459">+234 814 612 476</a><br />
          <a class="social-link" href="mailto:info@ellavaldezltd.com">info@ellavaldezltd.com</a>
        </p>
      </address>
    </div>

    <nav class="nav-col">
      <p class="footer-heading">Company</p>
      <Tabs {items} {activeItem} {footer} on:tabChange={tabChange} on:changeComponent />
    </nav>
  </div>
</footer>

<style>
  .footer {
    background-color: #e7eaed;
    padding: 6.4rem 0;
    border-top: 1px solid #eee;
  } 

  /* .grid--footer {
    grid-template-columns: 2fr 1fr 1fr;
  } */

  .logo-col {
    display: flex;
    flex-direction: column;
  }

  .footer-logo {
    margin-bottom: 2.4rem;
  }

  .social-links {
    list-style: none;
    display: flex;
    gap: 2.4rem;
  }

  .social-link:link, 
  .social-link:visited {
    text-decoration: none;
    font-size: 1.6rem;
    color: #767676;  
    transition: all 0.3s;
  }

  .social-link:hover, 
  .social-link:active {
    color: darkblue;
  }

  .social-icon {
    width:2.4rem;
    height: 2.4rem;
  }

  .copyright {
    font-size: 1.4rem;
    line-height: 1.6;
    color: #767676;
    margin-top: auto;
  }

  .footer-heading {
    font-size: 1.8rem;
    font-weight: 500;
    margin-bottom: 3.2rem;
  }

  .contacts {
    font-style: normal;
    font-size: 1.6rem;
    line-height: 1.6;

  }

  .address {
    margin-bottom: 1.8rem;
  }

/*******************************************/
/* MOBILE NAVIGATION BELOW 944px (Tablets)*/
/******************************************/
@media (max-width: 59em) {
  .grid--3-cols {
    grid-template-columns: repeat(3, 1fr);
  }
}

/**************************************************/
/* MOBILE NAVIGATION BELOW 544px (Phones)*/
/**************************************************/
@media (max-width: 34em) {
  .grid--3-cols {
    grid-template-columns: 1fr;   
  }

  .grid {
    row-gap: 4.8rem;
  }

  .footer-heading {   
    margin-bottom: 1.8rem;
  }
}


</style>