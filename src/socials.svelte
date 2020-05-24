<script>
export let socials;
</script>

<div>
  <h3>Social links</h3>
  <ul>
    {#each socials as social}
      <li>
        <a href={social.link}>{social.name}</a>
      </li>
    {/each}
  </ul>
</div>

<style>
  :global(ul) {
    padding: 0;
    list-style-type: none;
  }
  a {
    text-decoration: none;
    color: #242535;
    border-bottom: 2px solid rgba(0, 0, 0, 0.1);
  }
  a:hover, a:focus {
    border-bottom: 2px solid #000;
  }
</style>
