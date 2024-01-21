<script>
  export let articles = [];
</script>

<div class="articles lg:col-span-2">
  <h2 class="text-2xl font-bold text-slate-600 mb-8">Recent posts</h2>

  <div class="flex flex-col gap-y-8">
    {#each articles as { title, description, url }}
      <!-- TODO: hover fix responsive -->
      <!-- TODO: add see more button for 10 articles -->
      <article class="group relative flex flex-col items-start">
        <h3 class="text-base font-semibold tracking-tight text-zinc-800">
          <div
            class="absolute -inset-x-4 -inset-y-4 z-0 scale-95 bg-zinc-200 opacity-0 transition group-hover:scale-100 group-hover:opacity-100 sm:-inset-x-6 sm:rounded-2xl"
          ></div>
          <a href={url} target="_blank" rel="noopener noreferrer">
            <span
              class="absolute -inset-x-4 -inset-y-6 z-20 sm:-inset-x-6 sm:rounded-2xl"
            ></span>
            <span class="relative z-10">{title}</span>
          </a>
        </h3>

        <p class="relative z-10 mt-2 text-sm text-zinc-600">
          {description}
        </p>
      </article>
    {/each}
  </div>
</div>
