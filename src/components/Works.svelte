<script>
  export let works = [];
</script>

{#each works as work}
  <div class="flex gap-x-5 [&:not(:last-child)]:mb-5">
    <img
      class="size-14 lg:size-20 rounded-full"
      src={work.imgPath}
      alt={`${work.name} Logo`}
    />

    <div>
      <h1 class="text-sm font-bold mb-2">{work.name}</h1>

      <div class="flex gap-x-2 lg:flex-col text-xs lg:text-sm">
        <p>{work.title}</p>
        <p>{work.time}</p>
      </div>
    </div>
  </div>
{/each}
