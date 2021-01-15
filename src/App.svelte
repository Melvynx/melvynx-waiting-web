<script>
  import MelvynxLogo from './animation/MelvynxLogoAnim.svelte';

  import WrittingEffect from './animation/WrittingEffect.svelte';
  import Contact from './contact/Contact.svelte';
  import CentredContainer from './display/CentredContainer.svelte';
</script>

<main class="app">
  <CentredContainer>
    <div class="logo-container">
      <MelvynxLogo />
    </div>
    <WrittingEffect
      text={"If you see this page 👁 it means I haven't finished my site yet.\nBut something heavy 🔥 is coming."}
    />
    <Contact />
  </CentredContainer>
</main>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Roboto+Mono:wght@200;400&display=swap');

  .app {
    --bg-color: #1d1d1d;
    --base: 8;
    --text-color: #f0f0f0;
    background-color: var(--bg-color);
  }
  .logo-container {
    margin: 16px;
  }
</style>
