<script>
  import Accordion from "./Accordion.svelte";
</script>

<main>
  <div class="card">
    <Accordion />
  </div>
</main>

<style>
  main {
    display: flex;
  }
  .card {
    background-color: white;
    overflow-x: hidden;
    width: 600px;
    height: fit-content;
    border-radius: 20px;
    display: flex;
    flex-direction: column;
    padding: 0 50px 30px 50px;
    transition: max-height 0.3s ease-out;
  }
  ::-webkit-scrollbar {
    background-color: transparent;
  }

  @media only screen and (max-width: 640px) {
    .card {
      width: 90vw;
      height: fit-content;
      padding: 0 30px 30px 30px;
      margin: 4em 0 0 0;
    }
  }
   
</style>
