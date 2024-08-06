<script>
  import Card from "./Card.svelte";
</script>

<main>
  <Card />

  <!-- <div class="attribution">
    Challenge by <a
      href="https://www.frontendmentor.io?ref=challenge"
      target="_blank">Frontend Mentor</a
    >. Coded by <a href="giddelwilson-v2.netlify.app">Giddel Wilson</a>.
  </div> -->
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
  @media only screen and (max-width: 640px) {
    main {
      max-width: none;
    }
  }


  /* .attribution {
    font-size: 11px;
    text-align: center;
  }

  .attribution a {
    color: hsl(228, 45%, 44%);
  } */
</style>
