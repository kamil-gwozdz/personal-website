<script lang="ts">
  import Footer from "$lib/components/Footer.svelte";
  import Navbar from "$lib/components/Navbar.svelte";
  import Header from "$lib/components/header/Header.svelte";
  import "../styles.css"
</script>

<Header />
<Navbar />
<article>
  <slot></slot>
</article>
<Footer />
