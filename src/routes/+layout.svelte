<script lang="ts">
  import '@fontsource/poppins/400.css'
  import '@fontsource/poppins/600.css'
  import '@fontsource/poppins/700.css'
  import '$lib/base.css'
  import Navbar from '$lib/components/Navbar.svelte'
  import Footer from '$lib/components/Footer.svelte'
</script>

<div class="flex min-h-screen flex-col">
  <Navbar />
  <div>
    <slot />
  </div>
  <Footer />
</div>

<style global>
  body,
  html {
    margin: 0;
    padding: 0;
    height: 100%;
  }
</style>
