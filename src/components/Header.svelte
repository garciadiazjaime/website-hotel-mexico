<script>
  export let backgroundImage;
  export let bannerHeight = 390;
</script>
<style>
  .main {
    background-size: cover;
    background-position: center;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    padding: 40px 80px;
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
    align-self: flex-start;
    width: 100%;
    position: relative;
  }
  .icon {
    display: flex;
    align-self: flex-end;
    width: 100%;
  }
</style>

<div class="main" style="background-image: url({backgroundImage}); height: {bannerHeight}px">
  <div class="subheader">
    <slot name='subheader'></slot>
  </div>
  <h1><slot name="title"></slot></h1>
  <div class="icon" style="text-align: cehter;">
    <slot name="icon"></slot>
  </div>
</div>
