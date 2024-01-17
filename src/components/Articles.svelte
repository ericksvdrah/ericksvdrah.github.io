<script>
  export let articles = [];
</script>

{#each articles as { title, description }}
  <article>
    <h1 class="mb-2 font-bold">{title}</h1>
    <p class="text-sm">
      {description}
    </p>
  </article>
{/each}
