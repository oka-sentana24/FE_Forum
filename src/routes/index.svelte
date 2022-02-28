<svelte:head>
  <title>SvelteKit Material UI</title>
</svelte:head>

<center>
  <ThemeButton />

  <div>
    <Button class="button">
      <Label>Click</Label>
    </Button>
  </div>
</center>

<script>
  import Button, { Label } from '@smui/button';
  import ThemeButton from '$lib/ThemeButton.svelte';
</script>
