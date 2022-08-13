<script>
  import { page } from '$app/stores';
  import logo from './svelte-logo.svg';
  let date = new Date();
</script>

<header class="navigation">
  <div class="nav-parent">
    <div class="container-lg">
      <div class="nav-grid-parent">
        <a href="/" aria-current="page" class="nav-main-link">DEMARI</a>
        <div class="nav-middle-parent">
            <div>

              <div>SW22</div>
            </div>
            <div>


              Detroit, Michigan
              <span>{date.getTimezoneOffset()}</span>
            </div>

        </div>
        <div class="nav-menu-parent">
          <a class="nav-child">Bio</a>
          <a class="nav-child">works</a>
          <a class="nav-child">Contact</a>

        </div>
        <div>
        </div>
      </div>


      </div>


    </div>
    <div class="thin-line"></div>

</header>

<style>
  header {
    background-color: #0D0D0D;
    color: white;
    position: fixed;
    top: 0px;
    z-index: 18;
    width: 100%;

  }

  .nav-parent {
    z-index: 20;
    display: -webkit-box;
    display: -webkit-flex;
    display: flex;
    padding-top: 1.6em;

    -webkit-box-align: center;
    align-items: center;
    background-color: #0d0d0d;
  }
  .thin-line {
    width: 100vw;
    height: 0.5px;
    background-color: white;
    opacity: 0.1;
  }
  .container-lg {
    width: 95%;
    margin-right: auto;
    margin-left: auto;
  }
  .nav-grid-parent {
    display: grid;
    -webkit-box-align: center;
    align-items: center;
    grid-auto-columns: 1fr;
    grid-column-gap: 16px;
    grid-row-gap: 16px;
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: auto;
    font-weight: 400;
  }
  .nav-main-link {
    max-width: 100%;
    display: inline-block;
    color: inherit;
    line-height: 1;
    text-decoration: none;

  }
  .nav-middle-parent {
    display: grid;
    grid-auto-columns: 1fr;
    grid-column-gap: 0px;
    grid-row-gap: 0px;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: auto;

  }
  .nav-menu-parent {
    grid-column-start: span 1;
    grid-column-end: span 1;
    grid-row-start: span 1;
    grid-row-end: span 1;
  }
  .nav-child {
    max-width: 100%;
    display: inline-block;
  }



a, div {
  display: inline-block;
  margin-left: 1em;
  font-weight: 300;
  font-size: 0.9rem;


}
</style>
