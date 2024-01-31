<footer>
  <marquee><p>Kamil Gwóźdź © <span id="year"></span></p></marquee>
</footer>

<style>
    footer {
        background-color: #777;
        text-align: center;
        color: white;
        height: 6vh;
        position: absolute;
        width: 100%;
        bottom: 0;
        display: flex;
        flex-wrap: wrap;
        align-content: center;
    }

    footer marquee p {
        margin: 0;
    }

    footer marquee {
        padding: 10px;
    }
</style>

<script lang="ts">
  import { onMount } from 'svelte';

  onMount(() => {
    const yearElement = document.getElementById("year");
    if (yearElement) {
      yearElement.innerHTML = new Date().getFullYear().toString();
    }
  });
</script>
