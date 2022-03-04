<script>
  import '../../theme/tailwind.scss'
  import { Breadcrumbs, Avatar,Icon } from 'svelte-materialify';
  import { mdiSearchWeb, mdiAlertCircle, mdiBellBadge } from '@mdi/js';
  import Profile from "$lib/components/Avatar/index.svelte";
  import Search from '$lib/components/Search/index.svelte'

  const items = [
    { text: 'Dashboard', href: '/components/breadcrumbs/' },
    { text: 'Link 1', href: '/components/breadcrumbs/' },
    { text: 'Link 2', disabled: true },
  ];
</script>
<main>
  <div class="main header mx-3">
    <div class="flex flex-cols-md justify-between items-center">
      <div>
        <Breadcrumbs {items} />
      </div>
      <div class="flex flex-cols-2 gap-5 items-center">
        <span><Search/></span>
        <span><Icon path={mdiAlertCircle} /></span>
        <span><Icon path={mdiBellBadge} /></span>
        <span><Profile/></span>
      </div>
    </div>
  </div>
  <div class="main-title">
    <span>Dasboard</span>
  </div>
</main>