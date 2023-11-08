<script>
  import emailjs from '@emailjs/browser';
  import Button from '../reusable/Button.svelte';

  // setConfig({
  //   duration: 4000,
  //   position: 'top-right',
  // })


  // const successToast = () => {
  //   toast('Message Sent', {
  //     duration: 2000, 
  //     position: 'bottom-right', 
  //     style: {
  //       background: '#0C2D48', 
  //       color: '#fff',
  //     }
  //   });
  // }

  // const errorToast = () => {
  //   toast('Message not Sent', {
  //     duration: 2000, 
  //     position: 'bottom-right', 
  //     style: {
  //       background: 'red', 
  //       color: '#fff',
  //     }
  //   });
  // }

  function sendEmail(e) {
    emailjs.sendForm('service_ocap148', 'template_x072ls9', e.target, 'ZVEFfqRykdXODmBP6')
      .then((result) => {
          console.log('SUCCESS!', result.text);
          // successToast();
          e.target.reset();
      }, (error) => {
          console.log('FAILED...', error.text);
          // errorToast();
      });
  }

</script>

<section class="section-form">
  <div class="container">
    <div class="form-box">
      <div class="form-text-box">
        <h2 class="heading-secondary">Let's create a wonderful experience!</h2>

        <p class="form-text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptatibus quidem iusto architecto doloremque.</p>

        <form class="contact-form" on:submit|preventDefault={sendEmail}>
          <div>
            <label for="name">Name</label>
            <input type="text" id="name" name="user_name"/>
          </div>
          <div>
            <label for="email">Email</label>
            <input type="email" id="email" name="user_email" required/>
          </div>
          <div>
            <label for="message">Message</label>
            <textarea id="message" name="message"></textarea>
          </div>
          <div>
            <Button>Send</Button>
            <!-- <input type="submit" value="Book Now"/> -->
          </div>
        </form>
      </div>

      <div class="form-img-box" role="img" aria-label="classy-event"></div>
    </div>
  </div>
  
</section>

<style>
.section-form {
  padding: 4.8rem 0;
}

.form-box {
  display: grid;
  grid-template-columns: 2fr 1fr;
  box-shadow: 0 2.4rem 4.8rem rgba(0, 0, 0, 0.075);
  border-radius: 11px;
  background-image: linear-gradient(to right bottom, #3d576d, #0C2D48);
  overflow: hidden;

/* temp */
  /* height: 50rem; */
}

.form-text-box{
  padding: 4.8rem 6.4rem 6.4rem 6.4rem;
  color: #fff;
}

.form-text {
  font-size: 1.8rem;
  line-height: 1.8;
  margin-bottom: 4.8rem;
}

.form-img-box {
  background-image: linear-gradient(
    to right bottom,
   rgb(61, 87, 108, 0.4), 
   rgb(12, 44, 70, 0.4)
   ),
   url("/img/image6.jpg");
  background-size: cover;
  background-position: center;
}

.contact-form {
  display: flex;
  flex-direction: column;
  justify-items: center;
  gap: 2.4rem;
}

.contact-form label {
  display: block;
  font-size: 1.6rem;
  font-weight: 500;
  margin-bottom: 1.2rem;
}

.contact-form input, 
.contact-form textarea {
  width: 100%;
  padding: 1.2rem;
  font-size: 1.8rem;
  font-family: inherit;
  border: none;
  background-color: #e7eaed;
  border-radius: 9px;
  box-shadow: 0 1px 2px rgba(0, 0, 0, 0.1);
}

.contact-form *:focus {
  outline: none;
  box-shadow: 0 0 0 0.8rem rgba(18, 175, 237, 0.5);
}


</style>