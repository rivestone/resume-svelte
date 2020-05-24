<script>
export let projects;
</script>

<div>
  <h3>Projects</h3>
  {#each projects as project}
    <div>{project.name}</div>
    <a href={project.link}>project link</a>
    <span>{project.description}</span>
  {/each}
</div>
