<script>
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

let showMobileNav = false;
const toggleMobilNavView = () => {
	showMobileNav = !showMobileNav;
}

let items = ['Home', 'About', 'Our Services', 'Gallery', 'Contact'];
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
</script>

<MobileNavView on:changeComponent={changeComponent} on:goTo={contactComponent} {showMobileNav} on:click={toggleMobilNavView}/>

<Header on:changeComponent={changeComponent} on:goTo={contactComponent} on:goToHome={goToHome} on:click={toggleMobilNavView}/>
<main>
	{#if activeComponent === 'Home'}
		<Home on:click={contactComponent} />
			{:else if activeComponent === 'About'}
			<About />
			{:else if activeComponent === 'Our Services'}
			<Services />
			{:else if activeComponent === 'Gallery'}
			<Gallery />
			{:else if activeComponent === 'Contact'}
			<Contact />
			{/if}

			{#if activeComponent !== 'Contact'}
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















	
</style>