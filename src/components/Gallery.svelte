<script>
  import Button from "../reusable/Button.svelte";


  const gallery = [
		{src: '/img/gallery/corprt event.jpg', alt: 'captured moments', figCaption: 'Our Event', id: 1},
    {src: '/img/gallery/commerce.jpg', alt: 'captured moments', figCaption: 'Our Event', id: 2},
    {src: '/img/gallery/wedding.jpg', alt: 'captured moments', figCaption: 'Our Event', id: 3},
    {src: '/img/gallery/commerce.jpg', alt: 'captured moments', figCaption: 'Our Event', id: 4},
    {src: '/img/gallery/corprt event.jpg', alt: 'captured moments', figCaption: 'Our Event', id: 5},
    {src: '/img/gallery/wedding.jpg', alt: 'captured moments', figCaption: 'Our Event', id: 6},
    {src: '/img/gallery/commerce.jpg', alt: 'captured moments', figCaption: 'Our Event', id: 4},
    {src: '/img/gallery/corprt event.jpg', alt: 'captured moments', figCaption: 'Our Event', id: 5},
    {src: '/img/gallery/wedding.jpg', alt: 'captured moments', figCaption: 'Our Event', id: 6},
    {src: '/img/gallery/commerce.jpg', alt: 'captured moments', figCaption: 'Our Event', id: 4},
	];

</script>

<section class="section-gallery">
  <div class="gallery-container">
      <div class="gallery-text-box">
          <h1 class="heading-primary">Gallery</h1>
          <p class="gallery-description">Lorem ipsum dolor sit amet consectetur adipisicing elit. Illum quisquam nulla, non vero voluptatum blanditiis quis, ex dolorem, necessitatibus maiores culpa ducimus sed dicta doloribus!</p>          
      </div>

      <div class="gallery-img-box">
        <img src="/img/image7.jpg" class="gallery-img" alt="gallery image"/>
      </div>
  </div>


  <div class="moments-gallery container">
    <div class="moments-gallery-text-box">
      <h3 class="heading-tertiary">Our Memorable Events</h3>
      <p class="moments-gallery-description">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Fugit, ut illo ducimus possimus doloribus error alias tempore, aut explicabo accusamus modi, iste nemo quaerat culpa. Illum blanditiis nesciunt commodi maxime! Lorem ipsum dolor sit amet consectetur adipisicing elit. Amet rerum omnis aliquid, impedit dicta corporis neque esse nemo voluptatibus. Accusamus nam, officia aliquid perspiciatis nobis fugiat laborum blanditiis consectetur eos? </p>
    </div> 
    
    <div class="moments-gallery-box">
      {#each gallery as picture}
      <figure class="moments-gallery-item">
        <img src={picture.src} class="moments-gallery-image" alt={picture.alt}/>
        <!-- <figcaption>{moment.figCaption}</figcaption> -->
      </figure>
      {/each}      
    </div>

    <div class="gallery-btn">
      <a href="#">
        <Button type="primary" bigger={true} >Veiw Our Gallery</Button>
      </a>
    </div>

  </div>
</section>

<style>
  .section-gallery  {
    margin-bottom: 9.6rem;
  }

  .gallery-container {
    margin: 0 auto;
    position: relative;
  }
  
  .gallery-text-box {    
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
  
  .gallery-description {
    font-size: 2rem;
    line-height: 1.6;
    margin-bottom: 4.8rem ;
  }

  .gallery-img {
    width: 100%;
    max-height: 60vh;
  }

  .moments-gallery-text-box {
    padding: 4.8rem 0;
  }

  .heading-tertiary {
    text-align: center;
  }
  
  .moments-gallery-description {
    font-size: 2rem;
    line-height: 1.8;
  }

  .moments-gallery-box {
    display: grid;
    grid-template-columns: repeat(5, 1fr);
    align-items: center;
    gap: 1.6rem;
    margin-bottom: 4.8rem;

  }

  .moments-gallery-item {
    overflow: hidden;
  }

  .moments-gallery-image {
    display: block;
    width: 100%;
    transition: all 0.4s;
  }

  .moments-gallery-image:hover {
    transform: scale(1.1);
  }

  .gallery-btn {
    text-align: center;
  }

  </style>