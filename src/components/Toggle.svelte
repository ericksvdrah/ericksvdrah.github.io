<script>
  import { onMount } from 'svelte';
  import Light from './icons/Light.svelte';
  import Night from './icons/Night.svelte';

  let isDarkMode = false;

  const updateTheme = (darkMode) => {
    document.documentElement.classList.toggle('dark', darkMode);
    localStorage.setItem('theme', darkMode ? 'dark' : 'light');
  };

  const toggleTheme = () => {
    isDarkMode = !isDarkMode;
    updateTheme(isDarkMode);
  };

  onMount(() => {
    isDarkMode = localStorage.getItem('theme') === 'dark';
    updateTheme(isDarkMode);
  });
</script>

<button
  on:click={toggleTheme}
  class="h-12 w-12 rounded-lg p-2 hover:bg-gray-100 dark:hover:bg-gray-700"
>
  {#if isDarkMode}
    <Light />
  {:else}
    <Night />
  {/if}
</button>
