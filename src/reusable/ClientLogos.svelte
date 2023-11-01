<script>
  let clients = [
    {src: "/img/clientlogos/client1.jpg", alt: "logo 1", id: 1},
    {src: "/img/clientlogos/client2.jpg", alt: "logo 2", id: 2},
    {src: "/img/clientlogos/client3.jpg", alt: "logo 3", id: 3},
    {src: "/img/clientlogos/client4.png", alt: "logo 4", id: 4},
    {src: "/img/clientlogos/client5.jpeg", alt: "logo 5", id: 5},
  ];
</script>


<div class="clients">
  {#each clients as client}
    <img src={client.src} alt={client.alt} class= "client-logos"/>
  {/each}
</div>

<style>
  .clients {
    display: flex;
  }

  .client-logos {
    height: 4.8rem;
    width: 4.8rem;
    border-radius: 50%;
    margin-right: -1.6rem;
    border: 3px solid rgb(179, 179, 220, 0.9);
  }

  .client-logos:last-child {
    margin: 0;
  }

</style>

