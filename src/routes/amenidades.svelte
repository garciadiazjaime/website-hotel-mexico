<script>
  import Header from '../components/Header.svelte';
  import Nav from '../components/Nav.svelte';
</script>
<Header
  backgroundImage="https://picsum.photos/1000/620?random=1"
  bannerHeight="620"
>
 <span slot="subheader">
  <h3>Hotel México en la piel</h3>
  <a class="header-link" href="/reservaciones">Reserva</a>
 </span>
 <span slot="title">
  Un homenaje<br>a nuestro México
 </span>
 <div slot="icon" style="margin: 0 auto;">
  <img src="https://picsum.photos/100/100?random=15" alt="icon" />
</div>
</Header>
<Nav />
<style>
  h3 {
    color: white;
    text-transform: uppercase;
    font-size: 20px;
  }
  .header-link {
    text-transform: uppercase;
    font-size: 14px;
    color: white;
    display: block;
    position: absolute;
    right: 0;
    top: 0;
    text-decoration: none;
  }

</style>
