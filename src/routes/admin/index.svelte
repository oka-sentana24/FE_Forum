<main class="main-admin">
  <div class="header">
    <div class="admin-content">
      <div class="left-content">
        <Breadcrumbs {items}/>
      </div>
      <div class="right-content">
        <span>
          <Search/>
        </span>
        <span>
         <Message/>
        </span>
        <span>
          <Nontifikasi/>
        </span>
        <span>
          <Avatar/>
        </span>
      </div>
    </div>
    <div class="page-title">
      Dasboard
    </div>
  </div>
</main>
<script>
  import Avatar from '$lib/components/Avatar/index.svelte'
  import Nontifikasi from '$lib/components/Nontifikasi/index.svelte'
  import Message from '$lib/components/Message/index.svelte'
  import Search from '$lib/components/Search/index.svelte'
  import { Breadcrumbs } from 'svelte-materialify';

  const items = [
    { text: 'Dashboard', href: '/components/breadcrumbs/' },
    { text: 'Link 1', href: '/components/breadcrumbs/' },
    { text: 'Link 2', disabled: true },
  ];
</script>