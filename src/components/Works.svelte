<script>
  import Card from './Card.svelte';
  import DownloadCV from './DownloadCV.svelte';

  const works = [
    {
      name: 'Bsale Perú',
      title: 'Full Stack Developer',
      imgPath: './bsale_peru.jpg',
      time: '10-2022 - Current',
    },
    {
      name: 'Disruptive Studio',
      title: 'Backend Developer',
      imgPath: './disruptive_studio.jpg',
      time: '04-2022 - 10-2022',
    },
  ];
</script>

<Card>
  <h2 class="text-2xl font-bold text-slate-600">Work</h2>

  {#each works as work}
    <div class="flex gap-x-5 [&:not(:last-child)]:mb-5">
      <img
        class="size-14 rounded-full lg:size-20"
        src={work.imgPath}
        alt={`${work.name} Logo`}
      />

      <div>
        <h1 class="text-sm font-bold mb-2">{work.name}</h1>

        <div class="flex gap-x-2 text-xs lg:flex-col">
          <p class="text-zinc-500">{work.title}</p>
          <p class="text-zinc-400">{work.time}</p>
        </div>
      </div>
    </div>
  {/each}

  <!-- TODO: change bgcolor -->
  <DownloadCV />
</Card>
