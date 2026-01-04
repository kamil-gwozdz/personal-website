<nav>
  Navigation:
  <ul>
    <li><a href="/">About Me</a></li>
    <li><a href="guest_list">Guest List</a></li>
    <li><a href="puzzlux">🧩 puzzlux</a></li>
  </ul>

  Socials:
  <ul>
    <li><a target="_blank" href="https://www.linkedin.com/in/kamil-gwóźdź-a5335b146/" rel="noreferrer">linkedin</a></li>
    <li><a target="_blank" href="https://stackoverflow.com/users/7987708/kamil-gwóźdź" rel="noreferrer">stack overflow</a></li>
    <li><a target="_blank" href="https://www.instagram.com/cynicalautism/" rel="noreferrer">instagram</a></li>
    <li><a target="_blank" href="https://github.com/kamil-gwozdz" rel="noreferrer">github</a></li>
  </ul>

  <p class="clock-mobile">Clock:<p>
  <canvas id="clock" class="clock-mobile" width="500" height="500"></canvas>
</nav>

<style>
  @media screen and (max-width: 600px) {
    .clock-mobile {
      visibility: hidden;
      clear: both;
      float: left;
      display: none;
    }
  }

    nav {
        float: left;
        width: fit-content;
        background: white;
        padding: 5px;
        height: 80vh;
    }

    @media not screen and (max-width: 600px) {
        nav {
            max-width: 10%;
        }
    }

    nav ul {
        padding: 0;
    }
</style>
