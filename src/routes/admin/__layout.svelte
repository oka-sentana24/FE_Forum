<svelte:head>
  <title>SvelteKit Material UI</title>
</svelte:head>

<!-- <center>
  <ThemeButton />

  <div>
    <Button variant='unelevated'>
      <Label>Click</Label>
    </Button>
  </div>
</center> -->
<div class="main-admin">
  <div class="content">
    <div class="mini-side">
      <Miniside/>
    </div>
    <div class="sidebar">
      <Sidebar/>
    </div>
    <div class="main-pages">
      <slot/>
    </div>
  </div>
</div>

<script>
  // import Button, { Label } from '@smui/button';
  // import ThemeButton from '$lib/ThemeButton.svelte';
  import Miniside from '$lib/components/mini-sidebar.svelte'
  import Sidebar from '$lib/components/sidebar.svelte'
</script>
