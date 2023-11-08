<script>  
import { createEventDispatcher } from "svelte";
const dispatch = createEventDispatcher();

export let type = 'primary';
export let bigger = false;
export let inverse = false;

const handleBtnClick = (e) => {
  const btn = e.target;
  dispatch('goTo', btn);
}

const ctaToContact = (e) => {
  const btn = e.target;
  dispatch('ctaToContact', btn);
}

</script>

<button class={type} class:bigger={bigger} class:inverse={inverse} on:click={handleBtnClick} on:click={ctaToContact} on:click >
  <slot></slot>
</button>

<style>
  button{
    border: 0;
    cursor: pointer; 
    border-radius: 6px;
    padding: 0.8rem 1.2rem;
    font-weight: 600;
    box-shadow: 1px 2px 3px rgba(0, 0, 0, 0.2);
  }

  .primary {
    background: gold;
    color: #0C2D48;
    transition: all 0.3s;
  }

  .primary:hover {
    background: #e6c200;
  }

  .secondary {
    background: #0C2D48;
    color: #fff;
  }

  .bigger {
    padding: 0.8rem 1.2rem;
    font-size: 2.0rem;
  }

  .primary.inverse {
    color: gold;
    background: #00008b;
    border: 0.2rem solid #ffd700;
  }

  .secondary.inverse {
    color:#fff;
    background: darkblue;
    border: 0.2rem solid #fff;
  }




</style>