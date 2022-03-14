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
      Siswa
    </div>
  </div>
</main>
<section class="main-section">
  <div class="header-section">
    <div class="section-header">
      <div>
        <Filter/>
      </div>
      <div>
        <Button>new</Button>
      </div>
    </div>
  </div>
  <DataTable columns={columns} datas={datas}/>
</section>
<script lang="ts">
  import Avatar from '$lib/components/Avatar/index.svelte'
  import Nontifikasi from '$lib/components/Nontifikasi/index.svelte'
  import Message from '$lib/components/Message/index.svelte'
  import Search from '$lib/components/Search/index.svelte'
  import { Breadcrumbs, Button } from 'svelte-materialify'
  import DataTable from '$lib/components/DataTable/index.svelte'
  import Filter from '$lib/components/Filter/index.svelte'

  const items = [
    { text: 'Dashboard', href: '/components/breadcrumbs/' },
    { text: 'Link 1', href: '/components/breadcrumbs/' },
    { text: 'Link 2', disabled: true },
  ];

  let columns = ["Nisn", "Nama", "Jurusan", "Kelas", "Alamat", "Jenis Kelamin", "Tempat lahir", "Agama", "No tlp", "Email"]
  // let datas: Siswa[] = [
  //   {
  //     id:'1',
  //     nama:'oka sentana',
  //     jurusan:'multimedia',
  //     kelas:'III',
  //     alamat:'br.roban bitera',
  //     jenis_kelamin:'laki-laki',
  //     tempat_lahir:'gianyar',
  //     agama:'hindu',
  //     no_tlp:'083115427108',
  //     email:"test@gmail.com"
  //   }
  // ]
 let datas = [
    ["170030299", "oka sentana", "multimedia","III", "br.roban bitera","laki-laki", "gianyar","hindu","083115427108", "test@gmail.com"],
    ["170030299", "oka sentana", "multimedia","III", "br.roban bitera","laki-laki", "gianyar","hindu","083115427108", "test@gmail.com"],
    ["170030299", "oka sentana", "multimedia","III", "br.roban bitera","laki-laki", "gianyar","hindu","083115427108", "test@gmail.com"],
    ["170030299", "oka sentana", "multimedia","III", "br.roban bitera","laki-laki", "gianyar","hindu","083115427108", "test@gmail.com"],
    ["170030299", "oka sentana", "multimedia","III", "br.roban bitera","laki-laki", "gianyar","hindu","083115427108", "test@gmail.com"],
    ["170030299", "oka sentana", "multimedia","III", "br.roban bitera","laki-laki", "gianyar","hindu","083115427108", "test@gmail.com"],
    ["170030299", "oka sentana", "multimedia","III", "br.roban bitera","laki-laki", "gianyar","hindu","083115427108", "test@gmail.com"],
    ["170030299", "oka sentana", "multimedia","III", "br.roban bitera","laki-laki", "gianyar","hindu","083115427108", "test@gmail.com"],
    ["170030299", "oka sentana", "multimedia","III", "br.roban bitera","laki-laki", "gianyar","hindu","083115427108", "test@gmail.com"],
    ["170030299", "oka sentana", "multimedia","III", "br.roban bitera","laki-laki", "gianyar","hindu","083115427108", "test@gmail.com"],
    ["170030299", "oka sentana", "multimedia","III", "br.roban bitera","laki-laki", "gianyar","hindu","083115427108", "test@gmail.com"],
    ["170030299", "oka sentana", "multimedia","III", "br.roban bitera","laki-laki", "gianyar","hindu","083115427108", "test@gmail.com"],
    ["170030299", "oka sentana", "multimedia","III", "br.roban bitera","laki-laki", "gianyar","hindu","083115427108", "test@gmail.com"],
    ["170030299", "oka sentana", "multimedia","III", "br.roban bitera","laki-laki", "gianyar","hindu","083115427108", "test@gmail.com"],
    ["170030299", "oka sentana", "multimedia","III", "br.roban bitera","laki-laki", "gianyar","hindu","083115427108", "test@gmail.com"],
    ["170030299", "oka sentana", "multimedia","III", "br.roban bitera","laki-laki", "gianyar","hindu","083115427108", "test@gmail.com"],
    ["170030299", "oka sentana", "multimedia","III", "br.roban bitera","laki-laki", "gianyar","hindu","083115427108", "test@gmail.com"],
    ["170030299", "oka sentana", "multimedia","III", "br.roban bitera","laki-laki", "gianyar","hindu","083115427108", "test@gmail.com"],
    ["170030299", "oka sentana", "multimedia","III", "br.roban bitera","laki-laki", "gianyar","hindu","083115427108", "test@gmail.com"],
    ["170030299", "oka sentana", "multimedia","III", "br.roban bitera","laki-laki", "gianyar","hindu","083115427108", "test@gmail.com"],
    ["170030299", "oka sentana", "multimedia","III", "br.roban bitera","laki-laki", "gianyar","hindu","083115427108", "test@gmail.com"],
  ]
</script>