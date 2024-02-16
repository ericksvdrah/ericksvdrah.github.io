<script>
  export let articles = [];
</script>

<div class="articles lg:col-span-2">
  <h2 class="text-2xl font-bold text-slate-600 dark:text-zinc-200 mb-8">
    Recent Posts
  </h2>

  <div class="flex flex-col gap-y-8">
    {#each articles as { title, description, url }}
      <article
        class="group relative flex flex-col items-start p-4 transition-all duration-300 ease-in-out border border-transparent hover:border-slate-300 dark:hover:border-zinc-700 rounded-lg"
      >
        <h3
          class="text-lg font-semibold tracking-tight text-zinc-800 dark:text-zinc-200 mb-2"
        >
          <a
            href={url}
            target="_blank"
            rel="noopener noreferrer"
            class="hover:underline"
          >
            {title}
          </a>
        </h3>

        <p class="text-sm text-zinc-600 dark:text-zinc-400">
          {description}
        </p>
      </article>
    {/each}

    {#if articles.length > 10}
      <button
        class="mt-4 px-6 py-2 bg-slate-600 dark:bg-zinc-800 text-white rounded-full self-center hover:bg-slate-700 dark:hover:bg-zinc-700 transition-colors"
      >
        See More
      </button>
    {/if}
  </div>
</div>
