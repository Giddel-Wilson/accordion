<script>
    import Accordion from "./Accordion.svelte";
</script>
<main>
  <div class="card">
    <Accordion />
  </div>
</main>

<style>
  .card {
    background-color: white;
    overflow-x: hidden;
    width: 600px;
    height: auto;
    border-radius: 20px;
    display: flex;
    flex-direction: column;
    padding: 0 50px 60px 50px;
  }
</style>
