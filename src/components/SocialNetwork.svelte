<script>
  import LinkIcon from './LinkIcon.svelte';
  import GitHub from './icons/GitHub.svelte';
  import X from './icons/X.svelte';
  import Mail from './icons/Mail.svelte';
  import LinkedIn from './icons/LinkedIn.svelte';
  // import DevTo from './icons/DevTo.svelte';

  const links = [
    { href: 'https://www.github.com/ericksvdrah', Icon: GitHub },
    { href: 'https://www.twitter.com/ericksvdrah', Icon: X },
    { href: 'mailto:esvdrah@gmail.com', Icon: Mail },
    { href: 'https://www.linkedin.com/in/erick-saavedra-dev/', Icon: LinkedIn },
    // { href: 'https://dev.to/ericksk', Icon: DevTo },
  ];
</script>

<nav class="flex flex-row gap-x-4">
  {#each links as link}
    <LinkIcon href={link.href}>
      <svelte:component this={link.Icon} />
    </LinkIcon>
  {/each}
</nav>
