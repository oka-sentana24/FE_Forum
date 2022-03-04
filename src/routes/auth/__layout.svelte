<script>
  import { Card } from 'svelte-materialify';
  import "../../theme/tailwind.scss"
  import Loader from '$lib/components/Loader/index.svelte';
</script>
<main class="auth">
  <div class="container mx-auto h-screen">
    <div class='md:flex mdflex-cols-2 md:mx-5'>
      <div class="content md:h-screen">
        <div class="static hidden">
          <span class="title">
            Welcome to <br /> E-Forum Diskusi
            <br /> SMK NEGERI 1 GIANYAR</span
          >
          <br />
          <span class="desc">
            SMK Negeri 1 Gianyar berdiri pada tahun 1969 yang bernama SMEA <br /> yang berstatus
            swasta. Dalam perkembangannya SMEA swasta <br />ini mendapat sambutan yang sangat baik
            dari masyarakat,<br />
            terbukti dengan setiap tahun jumlah siswa yang mendaftar <br />ke sekolah ini semakin
            meningkat.
            <div class="visi">
              <span class="visi-title"> VISI : </span>
              <br />
              Mewujudkan sekolah unggul dalam bidang Bismen <br />serta TI berlandaskan imtaq, seni
              dan budaya bermental <br />wirausaha serta berdaya saing global
            </div>
            <div class="misi">
              <span class="visi-title">MISI :</span>
              <ul>
                <li>Melaksanakan Diklat dibidang bisnis dan Manajemen.</li>
                <li>Melaksanakan Diklat dibidang Teknologi dan Komunikasi.</li>
                <li>Melaksanakan diklat dengan menggunakan pendekatan saintifik.</li>
                <li>Melaksanakan kerja sama dengan Du/Di</li>
                <li>Melaksanakan ekstrakurikuler sesuai dengan bakat dan minat siswa</li>
              </ul>
            </div>
          </span>
        </div>
        <div class="d-flex justify-center mt-4 mb-4">
          <Card class="main-card">
            <slot/>
          </Card>
        </div>
      </div>
    </div>
  </div>
</main> 