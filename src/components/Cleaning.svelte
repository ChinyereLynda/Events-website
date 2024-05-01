<script>
  import Button from "../reusable/Button.svelte";
</script>

<div class="cleaning-container">
  <div class="cleaning-box container grid grid--2-cols">
    <div class="cleaning-text-box">
      <h3 class="heading-tertiary">Our Sparkling Touch</h3>
      <p class="cleaning-description"> Do you need a hand keeping things sparkling and spotless? Our experts have got your back. Whether it's your home, office, mall or event space, we'll handle all the grimy details so you don't have to. Our top-notch cleaning services will make your place look spick-and-span. Reach out today and let's get your space shining like new again!</p>
      <div class="cleaning-btn">
        <Button type="primary" inverse={true} on:click>Book Now</Button>
      </div>
    </div>  
    
    <div class="cleaning-img-box">
      <img src="/img/cleaning gloves.jpg" class="cleaning-image" alt="cleaning event"/>
    </div>
    
  </div>
</div>


<style>
  .cleaning-container {
    margin: 4.8rem auto 8rem auto;
  }

  .cleaning-box {
    align-items: center;
    column-gap: 3.2rem;
  }

  .cleaning-text-box{
    margin-left: 4.8rem;
  }

  .cleaning-description {
    font-size: 2rem;
    line-height: 1.8;
    margin-bottom: 3.2rem;
  }

  /* .cleaning-btn {
    text-align: center;
  } */

  .cleaning-img-box {
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .cleaning-image {
    width: 60%;
  }

  



</style>