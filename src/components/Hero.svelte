<script>
  import Button from "../reusable/Button.svelte";
  import ClientLogos from "../reusable/ClientLogos.svelte";

</script>

<section class="section-hero">
  <div class="hero-container">
      <div class="hero-text-box">
          <h1 class="heading-primary">Lorem ipsum dolor sit amet, consectetur adipisicing elit.</h1>
          <p class="hero-description">Lorem ipsum dolor sit amet consectetur adipisicing elit. Illum quisquam nulla, non vero voluptatum blanditiis quis, ex dolorem, necessitatibus maiores culpa ducimus sed dicta doloribus!</p>
          <div class="btn-wrap">
            <Button type="primary" bigger={true} inverse={false} on:click>Book Now</Button>
          </div> 
          <div class="client-box">
            <ClientLogos />
            <p class="client-text">Super <span>memories</span> created for our clients! </p>
        </div>
      </div>

    <div class="hero-img-box">
      <img src="/img/image1.jpg" class="hero-img" alt="hero image"/>
    </div>
  </div>
</section>

<style>
  .section-hero  {
    margin-bottom: 9.6rem;
  }

  .hero-container {
    /* max-width: 130rem; */
    margin: 0 auto;
    position: relative;
  }
  
  .hero-text-box {    
    max-width: 60rem;
    margin: 0 auto;
    background: rgb(179, 179, 220, 0.9);
    color: #0C2D48;
    position: absolute;
    top: 0;
    bottom: 0;
    padding: 9.6rem 1.4rem 0 2.4rem;    
  }
  
  .hero-description {
    font-size: 2rem;
    line-height: 1.6;
    margin-bottom: 4.8rem ;
  }

  .hero-img {
    width: 100%;
    height: 100vh;
  }
  
  /* .btn-wrap {
    text-align: right;
  } */

  .client-box {
    display: flex;
    align-items: center;
    gap: 1.6rem;
    margin-top: 8rem;
  }

  .client-text {
    font-size: 1.8rem;
    font-weight: 600;
  }

  .client-text span{
    color: gold;
    font-weight: 700;
  }

</style>