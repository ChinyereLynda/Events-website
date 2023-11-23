<script>
  import Button from "../reusable/Button.svelte";
</script>

<section class="section-cta">
  <div class="cta-backgroundimg-holder" role="img" aria-label="glass with juice and herbs">
    <div class="cta-box">
      <div class="cta-text-box">
        <h2 class="cta-caption">Create your Wonderful Moment Now!</h2>
        <div class="cta-button">
          <Button type="primary" bigger={true} on:ctaToContact>Send Request</Button>
        </div>
      </div>
    </div>
  </div>
</section>

<style>  
  .cta-backgroundimg-holder {
    background-image: linear-gradient(
    to right bottom,
    rgb(61, 87, 108, 0.6), 
    rgb(12, 44, 70, 0.6)
    ),
    url("/img/image6.jpg");
    background-size: cover;
    background-position: center;
    position: relative;
    height: 35rem;
  }

  .cta-box {
    position: absolute;
    top: 50%;
    right: 50%;
    transform: translate(50%, -50%);
  }

  .cta-text-box {
    display: grid;
    grid-template-columns: 4fr 1.5fr;
    align-items: center;
    gap: 9.6rem;

  }

  .cta-caption {
  color: #fff;
  font-size: 4.2rem;
  font-weight: 700;
  line-height: 1.05;
  letter-spacing: -0.5px;
  }



</style>