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
  <h2 class="text-2xl font-bold text-slate-600 dark:text-zinc-200 mb-4">
    Work
  </h2>

  {#each works as work}
    <div class="flex gap-x-5 mb-5 last:mb-0 items-center">
      <img
        class="w-14 h-14 rounded-full lg:w-20 lg:h-20 object-cover"
        src={work.imgPath}
        alt={`${work.name} Logo`}
      />

      <div>
        <h3 class="text-lg font-bold text-zinc-800 dark:text-zinc-200">
          {work.name}
        </h3>

        <div class="flex gap-x-2 lg:flex-col lg:gap-y-1 text-xs">
          <p class="text-zinc-600 dark:text-zinc-400">{work.title}</p>
          <p class="text-zinc-500 dark:text-zinc-400">{work.time}</p>
        </div>
      </div>
    </div>
  {/each}

  <DownloadCV />
</Card>
