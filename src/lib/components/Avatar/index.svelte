<script>
  import "./avatar.scss"
  import {ListItem, Avatar,Icon} from 'svelte-materialify';
  import { mdiAccountCircleOutline, mdiCog, mdiLogout } from '@mdi/js';
  import { createEventDispatcher } from 'svelte';
  let isOpenProfile = false;
  let dispatch = createEventDispatcher();

  function show() {
    isOpenProfile = !isOpenProfile;
      dispatch('show', isOpenProfile);
  }
</script>
<div class="main-avatar" on:click={show}>
  <Avatar size="36px" class="avatar"><b>MS</b></Avatar>
</div>
{#if isOpenProfile}
  <div class="setting-profile">
    <ListItem>
      <div slot="prepend">
        <Avatar><img src="//picsum.photos/100?random=1" alt="Avatar" /></Avatar>
      </div>
      Study Group
      <span slot="subtitle"> <b>John Doe</b> - This is my message </span>
    </ListItem>
    <hr class="line"/>
    <div class="profile">
      <span><Icon path={mdiAccountCircleOutline}/></span>
      <span>Profile</span>
    </div>
    <div class="setting">
      <span><Icon path={mdiCog} /></span>
      <span>Profile</span>
    </div>
    <hr class="line"/>
    <div class="signout">
        <span><Icon path={mdiLogout} /></span>
        <span>Sign out</span>
    </div>
  </div>
{/if}