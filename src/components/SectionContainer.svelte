<script>
  export let className = '';
</script>

<section
  class={`w-full mx-auto ${className} lg:w-[1024px] bg-white text-black dark:bg-gray-900 dark:text-white`}
>
  <slot />
</section>
