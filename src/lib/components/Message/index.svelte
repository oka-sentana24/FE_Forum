<div class="main-message" on:click={show}>
  <Icon path={mdiInformationOutline}/>
</div>
{#if isNontifikasi}
  <div class="message">
    <div class="header">
      <div class="title">
        <span>Message</span>
        <span><Icon path={mdiEmailOpenOutline}/></span>
      </div>
    </div>
    <div class="content">
      <div class="no-nontifikasi">
       <span class="icon">
        <Icon path={mdiInformationOutline}/>
       </span>
       <div class="content-nodata">
        <span class="title">
          No message
        </span>
        <span class="sub">
          When you have message, they will appear here.
        </span>
       </div>
      </div>
    </div>
  </div>
{/if}

<script>
  import "./message.scss"
  import {Card,Icon, ListItem} from 'svelte-materialify';
  import { mdiInformationOutline, mdiEmailOpenOutline } from '@mdi/js';
  import { createEventDispatcher } from 'svelte';
  let isNontifikasi = false;
  let dispatch = createEventDispatcher();

  function show() {
    isNontifikasi = !isNontifikasi;
      dispatch('show', isNontifikasi);
  }
</script>