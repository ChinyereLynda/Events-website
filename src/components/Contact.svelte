<script>
import Form from "./Form.svelte";
</script>

<section class="section-contact">
  <div class="contact-container">
      <div class="contact-text-box">
          <h1 class="heading-primary">Contact Us</h1>
          <p class="contact-description">Lorem ipsum dolor sit amet consectetur adipisicing elit. Illum quisquam nulla, non vero voluptatum blanditiis quis, ex dolorem, necessitatibus maiores culpa ducimus sed dicta doloribus!</p>          
      </div>

      <div class="contact-img-box">
        <img src="/img/image7.jpg" class="contact-img" alt="gallery image"/>
      </div>
  </div>
  
  <Form />
</section>

<style>
  .section-contact  {
    margin-bottom: 9.6rem;
  }

  .contact-container {
    margin: 0 auto 8rem;
    position: relative;
  }
  
  .contact-text-box {    
    max-width: 70%;
    max-height: 70%;
    margin: 0 auto;
    /* background: rgb(179, 179, 220, 0.8); */
    background: rgba(207, 213, 217, 0.8);
    color: darkblue;
    position: absolute;
    top: 50%;
    transform: translate(0, -50%);
    padding: 4.8rem 1.4rem 0 2.4rem;    
  }
  
  .contact-description {
    font-size: 2rem;
    line-height: 1.6;
    margin-bottom: 4.8rem ;
  }

  .contact-img {
    width: 100%;
    max-height: 60vh;
  }

  
  </style>