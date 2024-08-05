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

  @media only screen and (380px <= width < 768px) {
    .card {
      width: 44vb;
      height: fit-content;
      padding: 0 30px 30px 30px;
    }
  }
  @media only screen and (360 < width <= 380px) {
    .card {
      width: 52vb;
      height: fit-content;
      padding: 0 30px 30px 30px;
    }
  }
  @media only screen and (345px <= width <= 360px) {
    .card {
      width: 45vb;
      height: fit-content;
      padding: 0 30px 30px 30px;
    }
  }
  @media only screen and (width < 345px) {
    .card {
      width: 36.5vb;
      height: fit-content;
      padding: 0 30px 30px 30px;
    }
  }
  @media only screen and (width < 345px) {
    .card {
      width: 50%;
      height: fit-content;
      padding: 0 30px 30px 30px;
    }
  }
  @media (width: 1024px) and (height: 1024px) {
    .card {
      width: 50vb;
      padding: 0 30px 50px 30px;
    }
  }
  @media (width: 540px) and (height: 720px) {
    .card {
      width: 60vb;
      padding: 0 30px 50px 30px;
    }
  }
  
</style>
