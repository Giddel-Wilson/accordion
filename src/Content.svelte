<script>
  import { accordionContent } from "./ContentData";

  let isOpen = false;
  let collapse = () => {
    isOpen = !isOpen;
  }
</script>

{#each accordionContent as { heading, _content }}
  <div class="accord">
    <button class="accordBtn" class:active={isOpen} on:click={collapse}>
      <div class="div">
        <h4>{heading}</h4>
        <button class="btn">━</button>
      </div>
    </button>
    <div class="panel" class:open-panel={isOpen}>
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
  
  .btn {
    border-radius: 100%;
    font-size: 12px;
    font-weight: 600;
    background-color: black;
    color: white;
    padding: 10px;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 20px;
    width: 20px;
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
  }

  .open-panel {
    display: block;
  }

  .div button {
    text-align: start;
    background-color: blueviolet;
    font-size: 13px;
  }

  div button {
    background-color: transparent;
    border: none;
    width: 100%;
    height: 100%;
  }
  /* .accordBtn:active {
    background-color: blue;
  } */
</style>
