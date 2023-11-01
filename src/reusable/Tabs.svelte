<script>
  import { createEventDispatcher } from "svelte"; 
  const dispatch = createEventDispatcher();

  export let items;
  export let activeItem;
  export let color;
  export let background;
  export let gap;
  export let border;
  export let padding;
  export let borderRadius;




</script>

<div class="tabs">
  <ul class="tabs-list" style={`gap:${gap}`}>     
    {#each items as item}
      <li 
      on:click={() => dispatch('tabChange', item)} 
      on:click={() => dispatch('changeComponent', item)}
      style={`color:${color}; background:${background}; border:${border}; padding:${padding}; border-radius:${borderRadius}`}>
        <div class:active={item === activeItem} class="item">{item}</div>
      </li>
    {/each}
  </ul>

</div>

<style>
  
  .tabs-list {
    list-style-type: none;
    display: flex;
    justify-content: center;
    gap: 3.2rem;
    padding: 0;
  }

  li {
    font-size: 2rem;
    color: #fff;
    cursor: pointer;
  }

  .active {
    color: gold;
    border-bottom: 2px solid gold;
  }

  .item:hover {
    color: gold;
    font-weight: 500;
    transition: all 0.3s;
  }



/*******************************************/
/* MOBILE NAVIGATION BELOW 944px (Tablets)*/
/******************************************/
/* @media (max-width: 59em) {
  .tabs-list {                   
    flex-direction: column;
    gap: 4.8rem;
    align-items: center;
  }
  
} */




</style>