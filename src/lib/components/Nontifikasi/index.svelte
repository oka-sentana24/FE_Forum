<div class="main-nontifikasi" on:click={show}>
  <Icon path={mdiBellOutline}/>
</div>
{#if isNontifikasi}
  <div class="nontifikasi">
    <div class="header">
      <div class="title">
        <span>Nontification</span>
        <span><Icon path={mdiEmailOpenOutline}/></span>
      </div>
    </div>
    <div class="content">
      <div class="no-nontifikasi">
       <span class="icon">
        <Icon path={mdiBellOutline}/>
       </span>
       <div class="content-nodata">
        <span class="title">
          No notifications
        </span>
        <span class="sub">
          When you have notifications, they will appear here.
        </span>
       </div>
      </div>
    </div>
  </div>
{/if}

<script>
  import "./nontifikasi.scss"
  import {Card,Icon, ListItem} from 'svelte-materialify';
  import { mdiBellOutline, mdiEmailOpenOutline } from '@mdi/js';
  import { createEventDispatcher } from 'svelte';
  let isNontifikasi = false;
  let dispatch = createEventDispatcher();

  function show() {
    isNontifikasi = !isNontifikasi;
      dispatch('show', isNontifikasi);
  }
</script>