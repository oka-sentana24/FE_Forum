<script>
  import { Breadcrumbs,List, ListGroup, ListItem, Avatar,Icon, Divider, Button} from 'svelte-materialify';
  import { mdiAccountCircleOutline, mdiCog, mdiLogout } from '@mdi/js';
  import { createEventDispatcher } from 'svelte';
  let isOpenProfile = false;
  let dispatch = createEventDispatcher();

  function show() {
    isOpenProfile = !isOpenProfile;
      dispatch('show', isOpenProfile);
  }
</script>
<div class="profile cursor-pointer" on:click={show}>
  <Avatar size="36px" class="red white-text"><b>MS</b></Avatar>
</div>
{#if isOpenProfile}
  <div class="main-profile">
    <ListItem>
      <div slot="prepend">
        <Avatar><img src="//picsum.photos/100?random=1" alt="Avatar" /></Avatar>
      </div>
      Study Group
      <span slot="subtitle"> <b>John Doe</b> - This is my message </span>
    </ListItem>
    <hr class="line"/>
      <div class="flex flex-cols-2 w-full gap-3 p-3">
        <span><Icon path={mdiAccountCircleOutline}/></span>
        <span>Profile</span>
      </div>
      <div class="flex flex-cols-2 w-full gap-3 p-3">
        <span><Icon path={mdiCog} /></span>
        <span>Profile</span>
      </div>
    <hr class="line"/>
    <ListItem>
      <div class="logout flex flex-cols-2 w-full gap-3 items-center h-5">
          <span><Icon path={mdiLogout} /></span>
          <span>Sign out</span>
      </div>
    </ListItem>
  </div>
{/if}