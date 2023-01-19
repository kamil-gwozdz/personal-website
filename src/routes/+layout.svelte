<script context="module">
  import { rainbowCursor } from 'cursor-effects';
</script>

<script lang="ts">
  import { onMount } from "svelte";

  import Footer from "$lib/components/Footer.svelte";
  import Navbar from "$lib/components/Navbar.svelte";
  import Header from "$lib/components/header/Header.svelte";
  import "../styles.css"

  onMount(() => {
    new rainbowCursor({length: 35, size: 5});
  });
</script>

<Header />
<Navbar />
<article>
  <slot></slot>
</article>
<Footer />
