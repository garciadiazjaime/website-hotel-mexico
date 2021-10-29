<script>
  export let backgroundImage;
</script>
<style>
  .main {
    background-size: cover;
    background-position: center;
    height: 390px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 0 40px;
    box-sizing: border-box;

  }
  h1 {
    display: flex;
    color: white;
    font-size: 48px;
    text-indent: -170px;
    padding-left: 170px;
  }
  .subheader {
    display: flex;
    align-self: flex-start;
    width: 100%;
  }
  .icon {
    display: flex;
    align-self: flex-end;
    width: 100%;
  }
</style>

<div class="main" style="background-image: url({backgroundImage});">
  <div class="subheader">
    <slot name='subheader'></slot>
  </div>
  <h1><slot name="title"></slot></h1>
  <div class="icon"><slot name="icon"></slot></div>
</div>
