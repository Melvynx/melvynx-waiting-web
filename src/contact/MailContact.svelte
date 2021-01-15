<script>
  let value;
</script>

<div>
  <input bind:value placeholder="Mail Subject" />
  {#if value}
    <a class="send-mail-btn" href="mailto:melvynmal@gmai.com?subject={value}">
      <span>Send mail</span>
    </a>
  {/if}
</div>

<style>
  div {
    display: flex;
    flex-direction: column;
    margin: 16px;
  }

  .send-mail-btn {
    cursor: pointer;
    height: 32px;
    background-color: #ffffff;
    border: 1px solid rgba(212, 212, 216, 0.76);
    border-radius: 2px;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .send-mail-btn:active {
    background-color: rgba(212, 212, 216, 0.76);
  }

  .send-mail-btn > span {
    opacity: 1;
    color: #000000;
    font-weight: 500;
  }

  input {
    background-color: var(--bg-color);
    color: var(--text-color);
  }
</style>
