
<main>
  <div class="filter-button" on:click={show}>Filter
    <Icon path={mdiChevronUp} rotate={isOpenFilter ? 0 : 180} />
  </div>
  {#if isOpenFilter}
    test
  {/if}
</main>

<script>
  import { Icon, ListItem } from 'svelte-materialify';
  import "./filter.scss"
  import { mdiHome, mdiCog, mdiChevronUp } from '@mdi/js';
  import { createEventDispatcher } from 'svelte';
  let isOpenFilter = false;
  let dispatch = createEventDispatcher();

  function show() {
    isOpenFilter = !isOpenFilter;
      dispatch('show', isOpenFilter);
  }
</script>