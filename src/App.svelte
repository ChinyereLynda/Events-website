<script>
import Home from "./components/Home.svelte";
import Header from  "./components/Header.svelte";
import About from "./components/About.svelte";
import Services from "./components/Services.svelte";
import MobileNavView from "./components/MobileNavView.svelte";

let showMobileNav = false;
const toggleMobilNavView = () => {
	showMobileNav = !showMobileNav;
}

let activeComponent = 'Home';


const changeComponent = (e) => {
	activeComponent = e.detail;
}

const contactComponent = () => {
	activeComponent = 'Contact';
}

const goToHome = () => {
	activeComponent = 'Home';
}
</script>

<MobileNavView {showMobileNav} on:click={toggleMobilNavView}/>

<Header on:changeComponent={changeComponent} on:goTo={contactComponent} on:goToHome={goToHome} on:click={toggleMobilNavView}/>
<main>
	{#if activeComponent === 'Home'}
		<Home on:click={contactComponent} />
			{:else if activeComponent === 'About'}
			<About />
			{:else if activeComponent === 'Our Services'}
			<Services />
			{:else if activeComponent === 'Gallery'}
				<p>Gallery Component Goes Here</p>
			{:else if activeComponent === 'Contact'}
				<p>Contact Component Goes Here</p>
			{/if}
</main>

<style>
	/* @media (min-width: 640px) {
		main {
			max-width: none;
		}
	} */















	
</style>