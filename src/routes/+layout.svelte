<script lang="ts">
  import Footer from "$lib/components/Footer.svelte";
  import Header from "$lib/components/header/Header.svelte";
  import "../styles.css"
</script>

<Header />
<slot></slot>
<Footer />
