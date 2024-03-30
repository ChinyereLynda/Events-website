<script>
import { Router, Link, Route } from "svelte-routing";
import Home from "./components/Home.svelte";
import Header from  "./components/Header.svelte";
import About from "./components/About.svelte";
import Services from "./components/Services.svelte";
import MobileNavView from "./components/MobileNavView.svelte";
import Footer from "./components/Footer.svelte";
import Gallery from "./components/Gallery.svelte";
import Contact from "./components/Contact.svelte";
import Cta from "./components/Cta.svelte";
import Testimonial from "./components/Testimonial.svelte";
import CtaGallery from "./components/CtaGallery.svelte";
import TermsAndConditions from "./components/TermsAndConditions.svelte";

let showMobileNav = false;
const toggleMobilNavView = () => {
	showMobileNav = !showMobileNav;
}

let items = ['Home', 'About', 'Our Services', 'Gallery', 'Contact', 'Terms'];
let activeComponent = 'Home';


const changeComponent = (e) => {
	activeComponent = e.detail;
	if (showMobileNav == true) 
	showMobileNav = !showMobileNav;

}

const contactComponent = () => {	
	activeComponent = 'Contact';
	if (showMobileNav == true) 
	showMobileNav = !showMobileNav;
}

const goToHome = () => {
	activeComponent = 'Home';
}

// export let url = "";
</script>

<!-- <Router {url}>
  <nav>
		<div class="link-list">
			<Link to="/">Home</Link>
			<Link to="/about">About</Link>
			<Link to="/services">Our Services</Link>
			<Link to="/gallery">Gallery</Link>
			<Link to="/contact">Contact</Link>
		</div>
    

  </nav>
  <div>
		<Route path="/"><Home /></Route>
    <Route path="/about" component={About} />
    <Route path="/services" component={Services} />
    <Route path="/gallery" component={Gallery} />
    <Route path="/contact" component={Contact} />
  </div>
</Router> -->



<MobileNavView on:changeComponent={changeComponent} on:goTo={contactComponent} {showMobileNav} on:click={toggleMobilNavView}/>

<Header on:changeComponent={changeComponent} on:goTo={contactComponent} on:goToHome={goToHome} on:click={toggleMobilNavView}/>
<main>
	{#if activeComponent === 'Home'}
		<Home on:click={contactComponent} />
			{:else if activeComponent === 'About'}
			<About />
			{:else if activeComponent === 'Our Services'}
			<Services on:click={contactComponent}/>
			{:else if activeComponent === 'Gallery'}
			<Gallery />	
			{:else if activeComponent === 'Contact'}
			<Contact />
			{:else if activeComponent === 'Terms'}
			<TermsAndConditions />
			{/if}

			<!-- {#if activeComponent !== 'Contact'} -->
			{#if activeComponent !== 'Contact' && activeComponent !== 'Terms'}
			<CtaGallery />
			<Testimonial />
			<Cta on:ctaToContact={contactComponent} />			
			{/if}
			
</main>
<!-- <Testimonial />
<Cta on:ctaToContact={contactComponent} /> -->
<Footer on:changeComponent={changeComponent} />



<style>
	/* @media (min-width: 640px) {
		main {
			max-width: none;
		}
	} */
	/* .link-list {
    display: flex;
		align-items: center,
    justify-content: center;
    gap: 4.8rem;
    padding: 0;
  } */

	/* link {
		text-decoration: none;

	} */

	
</style>