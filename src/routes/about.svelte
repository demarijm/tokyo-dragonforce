<script>
	import { onMount } from "svelte";
	import { gsap } from "gsap";
  import Marquee from "svelte-fast-marquee";

	let box;

	onMount(() => {
	  gsap.to(box, { y: "-120%", duration: 1, ease: "power2.inOut" });
	});
</script>

<style>
  main {
    font-family: sans-serif;
    text-align: center;
    background-color: brown;
  }
  h1 {
    font-size: 13rem;
    line-height: 0%;
  }
  .box {
    height: 70vh;
    width: 100vw;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    background-color: black;
    font-weight: 600;
    color: #fff;
    margin: 0 auto;
    visibitliy: hidden;
  }

</style>

<main>
	<div class="box" bind:this={box}>Hello</div>
  <div>

<Marquee>
  <h1>Demari</h1>
</Marquee>
</div>

</main>