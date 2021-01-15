<script>
  import { spring } from 'svelte/motion';
  import MelvynxLogoSvg from './MelvynxLogoSvg.svelte';
  import { pannable } from './pannable';

  let coords = spring({ x: 0, y: 0 }, { stiffness: 0.4, damping: 0.2 });

  function handlePanStart() {
    coords.stiffness = coords.damping = 0.3;
  }

  function handlePanMove(event) {
    coords.update(($coords) => ({
      x: $coords.x + event.detail.dx,
      y: $coords.y + event.detail.dy,
    }));
  }

  function handlePanEnd() {
    coords.set({ x: 0, y: 0 });
  }
</script>

<div class="melvynx-logo-root">
  <div class="egg">
    <img src="images/hello.gif" alt="hello everyone" />
  </div>
  <div
    class="melvynx-logo-box"
    use:pannable
    on:panstart={handlePanStart}
    on:panmove={handlePanMove}
    on:panend={handlePanEnd}
    style="
    transform:
      translate({$coords.x}px, {$coords.y}px)
      rotate({$coords.x *
      $coords.y *
      0.001}deg)
  "
  >
    <MelvynxLogoSvg />
  </div>
</div>

<style>
  :global(.melvynx-logo-root) {
    --width: 140px;
    --height: 185px;
  }

  .melvynx-logo-box {
    position: relative;
    left: calc(50% - var(--width) / 2);
    top: calc(50% - var(--height) / 2);
    background-color: var(--bg-color);
    width: var(--width);
    height: var(--height);
    cursor: move;
  }

  .egg {
    position: absolute;
    width: var(--width);
  }
  .egg > img {
    width: var(--width);
  }
</style>
