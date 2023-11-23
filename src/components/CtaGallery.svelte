<script>
  import Button from "../reusable/Button.svelte";
</script>

<section class="section-cta-gallery">
  <div class="cta-gallery-backgroundimg-holder" role="img" aria-label="glass with juice and herbs">
    <div class="cta-gallery-box">
      <div class="cta-gallery-text-box">
        <h2 class="cta-gallery-caption">Our Beautiful Gallery</h2>
        <div class="cta-gallery-button">
          <a href="#">
            <Button bigger={true} >Veiw Our Gallery</Button>
          </a>
        </div>
      </div>
    </div>
  </div>
</section>

<style>  
.section-cta-gallery {
  margin-bottom: 3.2rem;
}

.cta-gallery-backgroundimg-holder {
  background-image: linear-gradient(
  to right bottom,
  rgb(61, 87, 108, 0.6), 
  rgb(12, 44, 70, 0.6)
  ),
  url("/img/wedding.jpg");
  background-size: cover;
  background-position: center;
  height: 35rem;
  position: relative;
}  

.cta-gallery-text-box {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 3.2rem;

  position: absolute;
  top: 50%;
  right: 50%;
  transform: translate(50%, -50%);
  }

.cta-gallery-caption {
  color: #fff;
  font-size: 4.2rem;
  font-weight: 700;
  line-height: 1.05;
  letter-spacing: -0.5px;
  }



</style>