<script lang="ts">
  const features = [
    { icon: "🔢", title: "Classic Sudoku", desc: "Standard rules - fill the grid with digits 1-9" },
    { icon: "🌡️", title: "Thermometer", desc: "Digits increase from the bulb to the end of the thermometer" },
    { icon: "🐴", title: "Knight", desc: "Cells a knight's move apart must be different" },
    { icon: "🗡️", title: "Killer", desc: "Digits in cages must sum to the given value" },
    { icon: "🏹", title: "Arrow", desc: "Digits on the arrow sum to the digit in the circle" },
  ];
</script>

<div class="puzzlux-page">
  <!-- Hero Section -->
  <section class="hero">
    <div class="hero-content">
      <h1 class="logo">🧩 puzzlux</h1>
      <p class="tagline">The ultimate Sudoku game for iOS</p>
      <p class="subtitle">Classic sudoku and extended variants in one app</p>
      
      <a href="https://apps.apple.com/app/puzzlux" target="_blank" rel="noreferrer" class="app-store-btn">
        <img src="https://developer.apple.com/assets/elements/badges/download-on-the-app-store.svg" alt="Download on the App Store" />
      </a>
    </div>
  </section>

  <!-- Features Section -->
  <section class="features">
    <h2>🎮 Game Modes</h2>
    <div class="features-grid">
      {#each features as feature}
        <div class="feature-card">
          <span class="feature-icon">{feature.icon}</span>
          <h3>{feature.title}</h3>
          <p>{feature.desc}</p>
        </div>
      {/each}
    </div>
  </section>
</div>

<style>
  .puzzlux-page {
    background: linear-gradient(135deg, #1a1a2e 0%, #16213e 50%, #0f3460 100%);
    color: white;
    min-height: 100vh;
    font-family: 'comicNeue', sans-serif;
  }

  section {
    padding: 40px 20px;
    max-width: 900px;
    margin: 0 auto;
  }

  h2 {
    text-align: center;
    font-size: 2em;
    margin-bottom: 30px;
    color: #00d4ff;
  }

  /* Hero */
  .hero {
    text-align: center;
    padding: 80px 20px;
    background: linear-gradient(180deg, rgba(0,212,255,0.1) 0%, transparent 100%);
  }

  .logo {
    font-size: 4em;
    margin: 0;
    background: linear-gradient(45deg, #00d4ff, #7b2cbf);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .tagline {
    font-size: 1.5em;
    color: #00d4ff;
    margin: 10px 0;
  }

  .subtitle {
    font-size: 1.1em;
    color: #aaa;
    margin-bottom: 30px;
  }

  .app-store-btn {
    display: inline-block;
    transition: transform 0.3s ease;
  }

  .app-store-btn:hover {
    transform: scale(1.05);
  }

  .app-store-btn img {
    height: 60px;
  }

  /* Features */
  .features-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
    gap: 20px;
  }

  .feature-card {
    background: rgba(255,255,255,0.05);
    border-radius: 15px;
    padding: 25px;
    text-align: center;
    border: 1px solid rgba(255,255,255,0.1);
    transition: transform 0.3s ease, background 0.3s ease;
  }

  .feature-card:hover {
    transform: translateY(-5px);
    background: rgba(255,255,255,0.1);
  }

  .feature-icon {
    font-size: 3em;
    display: block;
    margin-bottom: 15px;
  }

  .feature-card h3 {
    margin: 0 0 10px;
    color: #00d4ff;
  }

  .feature-card p {
    margin: 0;
    font-size: 0.9em;
    color: #ccc;
  }

  @media (max-width: 600px) {
    .logo {
      font-size: 2.5em;
    }

    .tagline {
      font-size: 1.2em;
    }
  }
</style>
