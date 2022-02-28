<main class="side">
  <!-- <List> -->
    <div class="title">
      <span>
        ONE_SKA
      </span>
    </div>
    <div class="sidebar-url">
        {#each items as item}
            <div class="side">
                <a class:active={$page.url.pathname === item.path} href={item.path}>
                  <div class="side-item">
                    <!-- <span><Icon path={item.icon} /></span> -->
                    <span>{item.text}</span>
                  </div>
                </a>
            </div>
        {/each}
    </div>
    <!-- </List> -->
</main>

<script>
  import { page } from "$app/stores"
  const items = [
    { text: 'Dasboard', path:'/admin' },
    { text: 'Kelola Siswa',path:'/admin/siswa' },
    // { text: 'Kelola Guru',path:'/admin/guru' },
    // { text: 'Kelola Kelas', path:'/admin/kelas' },
  ];
</script>