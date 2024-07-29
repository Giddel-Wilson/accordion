<script>
  import Content from "./Content.svelte";
</script>

<main>
  <div class="faq">
    <span class="star"></span>
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
    width: 100px;
    height: 10vh;
    background: url(../public/assets/images/star.png);
    background-repeat: no-repeat;
    background-size: contain;
    border: 1px solid black;
  }
</style>
