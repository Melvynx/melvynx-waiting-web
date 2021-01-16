<script>
  import MelvynxLogo from './animation/MelvynxLogoAnim.svelte';
  import WrittingEffect from './animation/WrittingEffect.svelte';
  import Contact from './contact/Contact.svelte';
  import BackgroundApp from './display/BackgroundApp.svelte';
  import { mainText } from './melvynx-data';
</script>

<main class="app">
  <BackgroundApp>
    <div class="logo-container">
      <MelvynxLogo />
    </div>
    <WrittingEffect text={mainText} />
    <Contact />
  </BackgroundApp>
</main>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Roboto+Mono:wght@200;400&display=swap');

  .app {
    --bg-color: #1d1d1d;
    --text-color: #f0f0f0;
    background-color: var(--bg-color);
  }
  .logo-container {
    margin: 16px;
  }
</style>
