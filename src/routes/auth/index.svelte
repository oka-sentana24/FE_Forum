<main class="content-login">
  <div class="title">
    Signin
  </div>
  <div class="description">
      Belum memiliki akun? <span class="sub">hubungi pihak sekolah</span>.
  </div>
  <form class="form">
    <TextInput label="Nip/Nisn" type="text" name="username"/>
    <TextInput label="password" type="password" name="password" iconName1={mdiEye} iconName2={mdiEyeOff} typeIcon='text'/>
    <div class="forgot">
      <span>Forgot password?</span>
    </div>
    <div class="checkbox">
      <Checkbox checked={false}>Remember me.</Checkbox>
    </div>
    <div class="submite">
       Sign in
    </div>
  </form>
</main>

<script>
  import TextInput from '$lib/components/TextField/text-input.svelte';
  import { Checkbox } from 'svelte-materialify';
  import { mdiEyeOff, mdiEye } from '@mdi/js';
</script>