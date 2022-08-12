<script>
  import { page } from '$app/stores';
  import logo from './svelte-logo.svg';
  let date = new Date();
</script>

<header class="navigation">
  <div class="nav-parent">

    <div>
     First 
    </div>
    <div>
     Second 
     {date.toUTCString()}
    </div>
    <div>
     <a>Bio</a>
     <a>works</a>
     <a>Contact</a>
    </div>
  </div>
</header>
<div class="thin-line"></div>

<style>
  header {
    display: flex;
    height: 10vh;
    width: 100%;

    align-items: center;
    background-color: #0D0D0D;
    color: white;

  }

  .nav-parent {
    display: grid;
    width: 100%;
    -webkit-box-align: center;
    grid-auto-columns: 1fr;
    grid-column-gap: 16px;
    grid-row-gap: 16px;
    grid-template-columns: repeat(3, 1fr);
    justify-content: center;
    grid-template-rows: auto;
    align-items: center;
    padding: 2rem;
  }
  .thin-line {
    width: 100vw;
    height: 0.5px;
    background-color: white;
    opacity: 0.1;
  }



a, div {
  display: inline-block;
  margin-left: 1em;
  font-weight: 300;
  font-size: 0.9rem;


}
</style>
