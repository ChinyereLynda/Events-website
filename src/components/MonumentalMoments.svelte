<script>
  import Button from "../reusable/Button.svelte";


const monumentalMoments = [
		{src: '/img/gallery/corprt event.jpg', alt: 'captured moments', figCaption: 'Our Event', id: 1},
    {src: '/img/gallery/commerce.jpg', alt: 'captured moments', figCaption: 'Our Event', id: 2},
    {src: '/img/gallery/wedding.jpg', alt: 'captured moments', figCaption: 'Our Event', id: 3},
    {src: '/img/gallery/commerce.jpg', alt: 'captured moments', figCaption: 'Our Event', id: 4},
    {src: '/img/gallery/corprt event.jpg', alt: 'captured moments', figCaption: 'Our Event', id: 5},
    {src: '/img/gallery/wedding.jpg', alt: 'captured moments', figCaption: 'Our Event', id: 6},    
	];
</script>

<div class="moments-container">
  <div class="monumental-moments-container grid grid--2-cols">
    <div class="moments-img-box">
      {#each monumentalMoments as moment}
      <figure class="moments-item">
        <img src={moment.src} class="moments-image" alt={moment.alt}/>
        <!-- <figcaption>{moment.figCaption}</figcaption> -->
      </figure>
      {/each}      
    </div>

    <div class="moments-text-box">
      <h3 class="heading-tertiary">Our Memorable Events</h3>
      <p class="moments-description">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Fugit, ut illo ducimus possimus doloribus error alias tempore, aut explicabo accusamus modi, iste nemo quaerat culpa. Illum blanditiis nesciunt commodi maxime! Lorem ipsum dolor sit amet consectetur adipisicing elit. Amet rerum omnis aliquid, impedit dicta corporis neque esse nemo voluptatibus. </p>
      <div class="moments-btn">
        <Button type="primary" inverse={true}>Book Now</Button>
      </div>
    </div>      
  </div>
</div>


<style>
  .moments-container {
  }

  .monumental-moments-container {
    align-items: center;
  }

  .moments-img-box {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.6rem;
    padding: 1.6rem;
  }

  .moments-item {}
    
  .moments-image {
    display: block;
    width: 100%;
  }

  .moments-text-box {
    margin: 4.8rem 4.8rem 8rem auto;
  }

  .heading-tertiary {
    text-align: center;
  }

  .moments-description {
    font-size: 2rem;
    line-height: 1.8;
    margin-bottom: 3.2rem;
  }

  .moments-btn {
    text-align: center;
  }

</style>