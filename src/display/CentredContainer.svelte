<div class="full-width-container">
  <div class="centred-child">
    <slot />
  </div>
</div>

<style>
  .full-width-container {
    width: 100vw;
    height: 100vh;
  }

  .centred-child {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100%;
  }
</style>
