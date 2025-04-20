<footer>
  <div class="footer-scroll">
    <p>Kamil Gwóźdź © <span id="year"></span></p>
  </div>
</footer>

<style>
    footer {
        background-color: #777;
        text-align: center;
        color: white;
        height: 6vh;
        position: fixed;
        width: 100vw;
        left: 0;
        bottom: 0;
        display: flex;
        align-items: center;
        justify-content: center;
        z-index: 100;
        overflow: hidden;
    }
    .footer-scroll {
        width: 100vw;
        overflow: hidden;
        white-space: nowrap;
        display: flex;
        align-items: center;
        justify-content: flex-start;
    }
    .footer-scroll p {
        display: inline-block;
        margin: 0;
        padding: 10px 0;
        font-size: 1.1em;
        animation: scroll-left 15s linear infinite;
        min-width: 100vw;
    }
    @keyframes scroll-left {
        0% {
            transform: translateX(100vw);
        }
        100% {
            transform: translateX(-100vw);
        }
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
