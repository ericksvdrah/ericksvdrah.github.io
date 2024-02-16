<script>
  const cvUrl = '/resume.pdf';
</script>

<button
  type="button"
  class="bg-slate-600 dark:bg-zinc-800 text-white hover:bg-slate-700 dark:hover:bg-zinc-700 transition-colors px-4 py-2 rounded-lg inline-flex items-center justify-center"
  on:click={() => window.open(cvUrl, '_blank')}
>
  Descargar CV
</button>
