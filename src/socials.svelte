<script>
export let socials;
</script>
  <ul>
    {#each socials as social}
      <li>
        <a href={social.link}>{social.name}</a>
      </li>
    {/each}
  </ul>
<style>

  li{
    font-size: 18px;
    margin-bottom: 10px;
    font-family: "Verdana", sans-serif;
  }
  a{
    padding: 0 10px;
    text-decoration: none;
    color: #143038;
    border-bottom: 2px solid rgba(48, 113, 133, 0.2);
  }
  a:hover, a:focus {
    border-bottom: 2px solid #5296ab;
  }
</style>
