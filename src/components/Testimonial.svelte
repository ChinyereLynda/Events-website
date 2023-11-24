<script>
  import CarouselTestimonial from "../reusable/CarouselTestimonial.svelte";

  const testimonials = [
		{author: 'Albert Eze', src: '/img/Testimonial1.jpg', alt: 'Testimonial Image', quote: 'Great job.', job: 'Senior Product Manager at EFG Company', id: 1},
    {author: 'Kelvin Breeze', src: '/img/Testimonial1.jpg', alt: 'Testimonial Image', quote: 'Excellent', job: 'Manager at HIJ Company', id: 2},
		{author: 'Brian Okwu', src: '/img/Testimonial1.jpg', alt: 'Testimonial Image', quote: 'Splendid', job: 'HR at KLM Company', id: 3},
		{author: 'Elizabeth Maya', src: '/img/Testimonial1.jpg', alt: 'Testimonial Image', quote: 'Fantabulous', job: 'Project Coordinator at OPQ Company', id: 4},
		{author: 'Drake Chew', src: '/img/Testimonial1.jpg', alt: 'Testimonial Image', quote: 'Nice one', job: 'Development Manager at RST Company', id: 5},
	];

</script>

<section class="section-testimonials">
  <h1 class="testimonial-heading heading-secondary">From Our Clients...</h1>
  <CarouselTestimonial {testimonials} />  

<!-- ****************************************************************************************************** -->
  <!-- {#each testimonials as testimonial} -->
  <!-- <div class="testimonial-box">
    <img class="testimonial-img" src="/img/Testimonial1.jpg" alt="Testimonial Image" />
    <blockquote class="testimonial">
      <p class="testimonial-text">"Lorem ipsum dolor sit amet consectetur adipisicing elit. Et excepturi nihil perferendis deserunt error! Nemo quisquam ipsa qui praesentium eaque. Cum assumenda placeat ipsam saepe eligendi quidem omnis rem illum."</p>
      <p class="testimonial-author">Albert Eze</p>
      <p class="testimonial-job">Senior Product Manager at EFG Company</p>
    </blockquote>

      <button class="btn btn--left"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="btn-icon">
        <path stroke-linecap="round" stroke-linejoin="round" d="M15.75 19.5L8.25 12l7.5-7.5" />
      </svg>
      </button>
      <button class="btn btn--right"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="btn-icon">
        <path stroke-linecap="round" stroke-linejoin="round" d="M8.25 4.5l7.5 7.5-7.5 7.5" />
      </svg>      
      </button>
      <div class="dots">
        <button class="dot dot--fill">&nbsp;</button>
        <button class="dot">&nbsp;</button>
        <button class="dot">&nbsp;</button>
        <button class="dot">&nbsp;</button>        
      </div>
  </div> -->
  <!-- {/each} -->
  
</section>

 <style>
  .section-testimonials {
    margin-bottom: 4.8rem;
    /* background-color:  #ced5da; */
    /* padding: 4.8rem 0 ; */

  }

  .testimonial-heading {
    color: #333;
    text-align: center;
  }

  /* 
  .testimonial-box {
    width: 80rem;
    margin: 9.6rem auto;
    background-color: #0C2D48;
    padding: 3.2rem 4.8rem 3.2rem 8rem;

    border-radius: 9px;
    position: relative;

    display: flex;
    align-items: center;
    gap: 8rem;
  }

  .testimonial-img {
    height: 20rem;
    border-radius: 9px;
    transform: scale(1.5);
    box-shadow: 0 12px 24px rgba(0, 0, 0, 0.25)
  }

  .testimonial-text {
    font-size: 1.8rem;
    font-weight: 500;
    line-height: 1.5;
    margin-bottom: 3.2rem;
    color: #e7eaed;
  }

  .testimonial-author {
    font-size: 1.4rem;
    margin-bottom: 0.4rem;
    color: #ced5da;
  }

  .testimonial-job {
    font-size: 1.2rem;
    color: #ced5da;
  }*/

  /* CONTROLS */
  /*.btn {
    background-color: #fff;
    border: none;
    height: 4rem;
    width: 4rem;
    border-radius: 50%;
    position: absolute;
    box-shadow: 0 12px 24px rgba(0, 0, 0, 0.2) ;
    cursor: pointer;    

    display: flex;
    align-items: center;
    justify-content: center;
  }

  .btn--left {
    left: 0;
    top: 50%;
    transform: translate(-50%, -50%);
  }

  .btn--right {
    right: 0;
    top: 50%;
    transform: translate(50%, -50%);
  }

  .btn-icon {
    height: 2.4rem;
    width: 2.4rem;
    stroke: #0C2D48;
  }

  .dots {
    position: absolute;
    left: 50%;
    bottom: 0;
    transform: translate(-50%, 3.2rem);

    display: flex;
    gap: 1.2rem;
  }

  .dot {
    height: 12px;
    width: 12px;
    background-color: #fff;
    border: 2px solid #0C2D48;
    border-radius: 50%;
    cursor: pointer;
  }

  .dot--fill {
    background-color: #0C2D48;
  }
  */

</style> 