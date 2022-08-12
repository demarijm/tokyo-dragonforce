<script context="module">
  export const prerender = true;
  import Marquee from 'svelte-fast-marquee';
  let play = true;
</script>

<script>
  import Counter from '$lib/Counter.svelte';
import AboutSection from '$lib/AboutSection.svelte';
</script>

<svelte:head>
  <title>Home</title>
  <meta name="description" content="Svelte demo app" />
</svelte:head>

<section>

    <div class="first-view">
      <div class="hero-grid">
        <div class="node-1">
          
        </div>
        <div class="node-2">
          <div class="text-node-2">
            <p> Thanks for visiting, you can find me in these places </p>

          </div>
        </div>
        <div class="node-1">
        </div>

      </div>
      <div class="marquee">

        <Marquee pauseOnHover={true} direction='right' play={play}>
          <h1 class="marquee-text">DEMARI</h1>
          <h1 class="dot">&#183;</h1>
          <h1 class="marquee-text">MILLER</h1>
          <h1 class="marquee-text">DEMARI</h1>
          <h1 class="dot">&#183;</h1>
          <h1 class="marquee-text">MILLER</h1>
        </Marquee>
      </div>
    </div>
    <AboutSection />



</section>

<style>
  .first-view {
    position: relative;
    color: white;
    height: 80vh;
    width: 100%;
    overflow-x: hidden;
  }
  .marquee {
    position: absolute;
    bottom: 0;
  }
  .marquee-text {
    font-size: 8rem;
    color: white;
    text-shadow: 0 0 10px black;
    line-height: 0%;
    font-weight: 400;
  }
  .dot {
    font-size: 6rem;
    line-height: 0%;
  }
  .hero-grid {
    display: grid;
    -webkit-box-align: center;
    align-items: center;
    grid-auto-columns: 1fr;
    grid-column-gap: 16px;
    grid-row-gap: 16px;
    grid-template-columns: 1fr 1.25fr 1fr;
    grid-template-rows: auto;
  }
  .node-1 {
    grid-column-start: span 1;
    grid-column-end: span 1;
    grid-row-start: span 1;
    grid-row-end: span 1;
  }
  .node-2 {
    display: grid;
    grid-auto-columns: 1fr;
    grid-column-gap: 0px;
    grid-row-gap: 0px;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: auto;
  }
  .text-node-2 {
    grid-column-start: 2;
    grid-column-end: 3;
    grid-row-start: 1;
    grid-row-end: 2;
  }

  section {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background-color: #0D0D0D;
    color: white;
    height: 100vh;

  }

  h1 {
    width: 100%;
  }
</style>
