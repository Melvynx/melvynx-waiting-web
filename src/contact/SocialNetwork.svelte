<script>
  import { githublink } from '../melvynx-data';
</script>

<div>
  <a href={githublink} title="my github page">
    <img class="github" src="images/github-logo.png" alt="github logo" />
  </a>
</div>

<style>
  div {
    display: flex;
    justify-content: center;
  }

  img {
    max-width: 32px;
    margin: 8px;
  }

  .github {
    background-color: white;
    border-radius: 50%;
  }
</style>
