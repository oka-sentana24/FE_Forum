<script>
  import { Icon } from 'svelte-materialify';
  import { mdiMagnify,mdiClose } from '@mdi/js';
  let isOpenSearch = false;
</script>
<div class="main-search" on:click={()=> isOpenSearch = true}>
  <Icon path={mdiMagnify} />
</div>

{#if isOpenSearch}
  <!-- <div class="main-search w-full top-0 absolute p-3">
    <div class="container mx-3 md:container md:w-3/5 lg:container lg:w-full">
      <div class="flex flex-cols-2 items-center justify-between gap-3 w-full">
        <div class="flex flex-cols-2 gap-3 w-full">
          <span>
            <Icon path={mdiMagnify}/>
          </span>
          <input type="text" placeholder="Search from page" class="w-full border-0">
        </div>
        <div on:click="{()=> isOpenSearch = false}">
          <Icon path={mdiClose}/>
        </div>
      </div>
    </div>
  </div> -->
{/if}