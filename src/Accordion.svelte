<script>
  import Content from "./Content.svelte";
</script>

<main>
  <div class="faq">
    <img src="./icon-star.svg" alt="" class="star">
    <h1>FAQs</h1>
  </div>
  <br />
  <Content />
</main>

<style>
  main {
    font-family: Verdana, Geneva, Tahoma, sans-serif;
  }
  .faq {
    width: 100%;
    height: 15vh;
    margin-right: 40vb;
    display: flex;
    align-items: center;
    justify-content: start;
    padding-top: 50px;
  }
  .faq h1 {
    font-size: 50px;
    margin-left: 20px;
  }
  .star {
    width: 50px;
}
</style>
