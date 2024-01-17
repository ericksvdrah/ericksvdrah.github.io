<script>
  import Night from './icons/Night.svelte';
  import Light from './icons/Light.svelte';

  export let darkMode = false;
</script>

<button
  on:click={() => (darkMode = !darkMode)}
  class="h-12 w-12 rounded-lg p-2 hover:bg-gray-100 dark:hover:bg-gray-700"
>
  {#if darkMode}
    <Night />
  {:else}
    <Light />
  {/if}
</button>
