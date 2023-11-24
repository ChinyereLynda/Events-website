<script>
  import Button from "../reusable/Button.svelte";
</script>

<div class="cleaning-container">
  <div class="cleaning-box container grid grid--2-cols">
    <div class="cleaning-text-box">
      <h3 class="heading-tertiary">Our Sparkling Touch</h3>
      <p class="cleaning-description">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Fugit, ut illo ducimus possimus doloribus error alias tempore, aut explicabo accusamus modi, iste nemo quaerat culpa. Illum blanditiis nesciunt commodi maxime! Lorem ipsum dolor sit amet consectetur adipisicing elit. Amet rerum omnis aliquid, impedit dicta corporis neque esse nemo voluptatibus. Accusamus nam, officia aliquid perspiciatis nobis fugiat laborum blanditiis consectetur eos.</p>
      <div class="cleaning-btn">
        <Button type="primary" inverse={true}>Book Now</Button>
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