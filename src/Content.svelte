<script>
  import { accordionContent } from "./ContentData";

  let isOpen = null;
  let collapse = (i) => {
    isOpen = isOpen === i ? null : i;
  };
</script>

{#each accordionContent as { heading, _content }, i}
  <div class="accord">
    <button
      class="accordBtn"
      class:active={isOpen === i}
      on:click={() => collapse(i)}
    >
      <div class="div">
        <h4>{heading}</h4>
        {#if isOpen === i}
        <button class="minusBtn">━</button>
        {:else}
        <button class="plusBtn">+</button>
        {/if}
      </div>
    </button>
    <div class="panel" class:open-panel={isOpen === i}>
      {_content}
    </div>
  </div>
{/each}

<style>
  .accord {
    /* margin: 20px 0 0 0; */
    padding: 20px 0 7px 0;
    border-bottom: 2px solid whitesmoke;
    box-shadow: 0 0 2px whitesmoke;
  }
  .accord:last-child {
    border-bottom: none;
  }

  .div h4 {
    font-size: 15px;
  }

  .plusBtn {
    border-radius: 100%;
    font-size: 12px;
    font-weight: 600;
    background-color: blueviolet;
    color: white;
    padding: 10px;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 21px;
    width: 21px;
    margin-left: auto;
  }
  .minusBtn {
    border-radius: 100%;
    font-size: 12px;
    font-weight: 600;
    background-color: black;
    color: white;
    padding: 10px;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 21px;
    width: 21px;
    margin-left: auto;
  }

  .div {
    display: flex;
    justify-content: center;
    text-align: start;
    align-items: center;
  }

  .panel {
    text-align: start;
    font-size: 15px;
    font-weight: 500;
    line-height: 25px;
    color: gray;
    padding: 20px 0;
    display: none;
    transition: max-height 0.3s ease-out;
  }

  .open-panel {
    display: block;
  }

  div button {
    background-color: transparent;
    border: none;
    width: 100%;
    height: 100%;
  }
</style>
