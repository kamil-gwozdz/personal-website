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
    new rainbowCursor({length: 35, size: 5, element: document.querySelector("html")});

    (function titleScroller(text) {
      document.title = text;
      setTimeout(function () {
        titleScroller(text.substr(1) + text.substr(0, 1));
      }, 500);
    }(document.title + "  |  "));

    var clock = document.getElementById("clock");
    var ctx = clock.getContext("2d");

    ctx.strokeStyle = '#00ffff';
    ctx.lineWidth = 17;
    ctx.shadowBlur= 15;
    ctx.shadowColor = '#00ffff'

    window.onresize = function () {
      clock.style.width = '100%';
    }
    clock.style.width = '100%';

    function degToRad(degree){
      var factor = Math.PI/180;
      return degree*factor;
    }

    function renderTime(){
      var now = new Date();
      var today = now.toDateString();
      var time = now.toLocaleTimeString();
      var hrs = now.getHours();
      var min = now.getMinutes();
      var sec = now.getSeconds();
      var mil = now.getMilliseconds();
      var smoothsec = sec+(mil/1000);
      var smoothmin = min+(smoothsec/60);

      //Background
      let gradient = ctx.createRadialGradient(250, 250, 5, 250, 250, 300);
      gradient.addColorStop(0, "#03303a");
      gradient.addColorStop(1, "black");
      ctx.fillStyle = gradient;
      //ctx.fillStyle = 'rgba(00 ,00 , 00, 1)';
      ctx.fillRect(0, 0, 500, 500);
      //Hours
      ctx.beginPath();
      ctx.arc(250,250,200, degToRad(270), degToRad((hrs*30)-90));
      ctx.stroke();
      //Minutes
      ctx.beginPath();
      ctx.arc(250,250,170, degToRad(270), degToRad((smoothmin*6)-90));
      ctx.stroke();
      //Seconds
      ctx.beginPath();
      ctx.arc(250,250,140, degToRad(270), degToRad((smoothsec*6)-90));
      ctx.stroke();
      //Date
      ctx.font = "25px Comic Sans MS";
      ctx.fillStyle = 'rgba(00, 255, 255, 1)'
      ctx.fillText(today, 175, 250);
      //Time
      ctx.font = "25px Comic Sans MS Bold";
      ctx.fillStyle = 'rgba(00, 255, 255, 1)';
      ctx.fillText(time+":"+mil, 175, 280);

    }
    setInterval(renderTime, 40);

    let frame = 0;
    function animateCursor() {
      document.getElementsByTagName('html')[0].style.cursor = `url('/cursor_frames/${frame}.png'), auto`;
      frame += 1;
      frame %= 4;
    }
    setInterval(animateCursor, 100);
  });
</script>

<Header />
<main>
  <Navbar />
  <article>
    <slot></slot>
  </article>
</main>
<Footer />

<style>
  main {
      height: 75%;
  }
</style>
