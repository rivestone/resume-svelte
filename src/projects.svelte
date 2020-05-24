<script>
export let projects;
</script>

<div class="resume-block">
  <h3>Projects</h3>
  <ul>
    {#each projects as project}
    <li>
      <div class="project-name">{project.name}</div>
      <a href={project.link}>project link</a>
      <p>{project.description}</p>
    </li>
    {/each}
  </ul>
</div>

<style>
  ul{
    text-align: left;
  }
  p{
    color: rgb(48, 113, 133);
  }
  a{
    text-decoration: none;
    color: #143038;
    border-bottom: 2px solid rgba(48, 113, 133, 0.2);
  }
  a:hover, a:focus {
    border-bottom: 2px solid #5296ab;
  }
  .project-name{
    font-size: 20px;
  }
</style>
