<script>
  import {TextField, Icon} from 'svelte-materialify';
  import './text-input.scss';
  import { createEventDispatcher } from 'svelte';
  export let label='';
  export let name='';
  export let type='';
  export let placeholder='';
  export let value='';
  export let rules = '';
  export let iconName1 = '';
  export let iconName2 = '';
  let shown = false;
  let show = false;

  let dispatch = createEventDispatcher();

  export function onShow() {
      shown = !shown;
      dispatch('show', shown);
  }
</script>
<div class="main-input">
  <TextField filled name={name} type={type} placeholder={placeholder} {value} rules={rules} class="field">
    <div slot="append" on:click={onShow}>
      <div on:click={() => {
        show = !show;
      }}>
       <Icon path={show ? iconName1 : iconName2} />
    </div>
      <!-- <Icon path={1} /> -->
    </div>
    <div class="content-input">
      <span>
        {label}
      </span>
    </div>
  </TextField>
</div>