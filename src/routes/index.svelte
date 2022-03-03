<svelte:head>
  <title>SvelteKit Material UI</title>
</svelte:head>

<center>
  <ThemeButton />

  <div>
    <Button class="button bg-slate-900">
      <Label>Click</Label>
    </Button>
    <TextInput label="test" type="text" name="test" rules={emailRules} iconName1={mdiMenuUp} iconName2={mdiMenuDown} bind:this={child} on:show={e => child.shown = e.detail}/>
    {#if child && child.shown}
      <div>Hidden child is shown!</div>
    {/if}
    <TextInput label="test" type="text" name="test" rules={emailRules}/>
  </div>
</center>

<script lang='ts'>
  import Button, { Label } from '@smui/button';
  import ThemeButton from '$lib/ThemeButton.svelte';
  import TextInput from '$lib/components/TextField/text-input.svelte';
  import { mdiMenuDown, mdiMenuUp } from '@mdi/js';
  let child;
  const emailRules = [
    (v) => !!v || 'Required',
    (v) => v.length <= 25 || 'Max 25 characters',
    (v) => {
      const pattern = /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
      return pattern.test(v) || 'Invalid e-mail.';
    },
  ];
</script>
