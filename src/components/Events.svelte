<script>
  import Button from "../reusable/Button.svelte";
    
</script>

<div class="events-container">
  <div class="container grid grid--3-cols margin-bottom-md">
    <div class="events">
      <img 
        src="/img/corprt event.jpg" 
        class="events-img" 
        alt="corporate-events-img" 
        />
      <div class="event-written-content">
        <div class="event-tag">
          <span class="tag tag--corporate">Corporate</span>
        </div>
        <p class="card-title">Corporate Events</p>
        <ul class="event-attributes">
          <li class="event-attribute">
            <ion-icon class="event-icon" name="briefcase-outline"></ion-icon>
            <span>Professional</span>
          </li>
          <li class="event-attribute">
            <ion-icon class="event-icon" name="happy-outline"></ion-icon>
            <span>Satisfactory</span>
          </li>
          <li class="event-attribute">
            <ion-icon class="event-icon" name="aperture-outline"></ion-icon>
            <span>Lorem ipsum dolor</span>
          </li>
          <li class="event-attribute">
            <ion-icon class="event-icon" name="alarm-outline"></ion-icon>
            <span>Lorem ipsum</span>
          </li>
        </ul>

        <div class="event-btn">
          <Button type="primary" inverse={true} on:click>Book Now</Button>
        </div>

      </div>  
    </div>

    <div class="events">
      <img 
        src="/img/commerce.jpg" 
        class="events-img" 
        alt="commercial-events-img" 
        />
      <div class="event-written-content">
        <div class="event-tag">
          <span class="tag tag--commercial">Social</span>
        </div>
        <p class="card-title">Social Events</p>
        <ul class="event-attributes">
          <li class="event-attribute">
            <ion-icon class="event-icon" name="briefcase-outline"></ion-icon>
            <span>Professional</span>
          </li>
          <li class="event-attribute">
            <ion-icon class="event-icon" name="happy-outline"></ion-icon>
            <span>Satisfactory</span>
          </li>
          <li class="event-attribute">
            <ion-icon class="event-icon" name="aperture-outline"></ion-icon>
            <span>Lorem ipsum dolor</span>
          </li>
          <li class="event-attribute">
            <ion-icon class="event-icon" name="alarm-outline"></ion-icon>
            <span>Lorem ipsum</span>
          </li>
        </ul>

        <div class="event-btn">
          <Button type="primary" inverse={true} on:click>Book Now</Button>
        </div>

      </div>  
    </div>    

    <div class="events weddings">
      <img 
        src="/img/wedding.jpg" 
        class="events-img" 
        alt="wedding-events-img" 
        />
      <div class="event-written-content">
        <div class="event-tag">
          <span class="tag tag--wedding">Outdoor Events</span>
        </div>
        <p class="card-title">Weddings</p>
        <ul class="event-attributes">
          <li class="event-attribute">
            <ion-icon class="event-icon" name="briefcase-outline"></ion-icon>
            <span>Professional</span>
          </li>
          <li class="event-attribute">
            <ion-icon class="event-icon" name="happy-outline"></ion-icon>
            <span>Satisfactory</span>
          </li>
          <li class="event-attribute">
            <ion-icon class="event-icon" name="aperture-outline"></ion-icon>
            <span>Lorem ipsum dolor</span>
          </li>
          <li class="event-attribute">
            <ion-icon class="event-icon" name="alarm-outline"></ion-icon>
            <span>Lorem ipsum</span>
          </li>
        </ul>

        <div class="event-btn">
          <Button type="primary" inverse={true} on:click>Book Now</Button>
        </div>

      </div>  
    </div>    
  </div>
</div>

<style>
  .events-container {
    margin: 4.8rem auto 8rem auto;
    /* padding: 4.8rem 0; */
    /* background-color:#fff; */
  }

  .events {
    box-shadow: 0 2.4rem 4.8rem rgba(0, 0, 0, 0.075);
    border-radius: 11px;
    overflow: hidden;
    transition: all 0.4s;
  }
  .events:hover {
    transform: translateY(-1.2rem);
    box-shadow: 0 3.2rem 6.4rem rgba(0, 0, 0, 0.06);
  }
  .events-img {
    width:100%; /*Please use appropriate image size*/
    /* height: 35%; */
  }

  .event-written-content {
    padding: 3.2rem 4.8rem 4.8rem 4.8rem;
  }

  .event-tag {
    margin-bottom: 1.2rem;
  }

  .tag {
    display: inline-block;
    padding: 0.4rem 0.8rem;
    font-size: 1.2rem;
    text-transform: uppercase;
    color: #333;
    border-radius: 100px;
    font-weight: 600;
  }
  
  .tag--corporate {
    background-color: #13AEEC;
  }

  .tag--commercial {
    background-color: #0C2D48;
    color: #fff;
  }

  .tag--wedding {
    background-color: cyan;
  }

  .card-title {
    font-size: 2.4rem;
    color:  #0C2D48;
    font-weight: 600;
    margin-bottom: 3.2rem;
  }

  .event-attributes {
    list-style: none; 
    display: flex;   
    flex-direction: column;
    gap: 1.8rem;
    margin-bottom: 1.8rem;
  }

  .event-attribute {
    font-size: 1.8rem;
    display: flex;
    align-items: center;
    gap: 1.6rem;
  }

  .event-icon {
    height: 2.4rem;
    width: 2.4rem;
    color: #0C2D48;
  }

  .event-btn {
    text-align: center;
  }

/*******************************************/
/* MOBILE NAVIGATION BELOW 944px (Tablets)*/
/******************************************/
@media (max-width: 59em) {
  .event-written-content {
    padding: 2.4rem 3.2rem 3.2rem 3.2rem;
  }

  .events {
    max-width: 38.56rem;
    grid-column: 1 / -1;
    justify-self: center;
  } 
}

    
</style>