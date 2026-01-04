<script lang="ts">
  const features = [
    { icon: "🔢", title: "Klasyczne Sudoku", desc: "Standardowe zasady - wypełnij siatkę cyframi 1-9" },
    { icon: "🌡️", title: "Termometr", desc: "Cyfry rosną od bańki do końca termometru" },
    { icon: "🐴", title: "Rycerz", desc: "Komórki oddalone o ruch skoczka muszą się różnić" },
    { icon: "🗡️", title: "Killer", desc: "Suma cyfr w klatkach musi zgadzać się z podaną wartością" },
    { icon: "🏹", title: "Strzałka", desc: "Cyfry na strzałce sumują się do cyfry w kółku" },
  ];

  const difficulties = [
    { name: "Łatwy", desc: "Idealne na początek", color: "#4CAF50" },
    { name: "Średni", desc: "Umiarkowane wyzwanie", color: "#FFC107" },
    { name: "Trudny", desc: "Wymaga zaawansowanych technik", color: "#FF9800" },
    { name: "Super Trudny", desc: "Dla ekspertów!", color: "#F44336" },
  ];

  const gameModes = [
    { icon: "🧘", name: "Relax", desc: "Bez stresu - nielimitowane podpowiedzi" },
    { icon: "📝", name: "Normal", desc: "Pokazuje błędy podczas gry" },
    { icon: "🏆", name: "Challenge", desc: "Błąd kończy grę - dla prawdziwych mistrzów!" },
  ];
</script>

<div class="puzzlux-page">
  <!-- Hero Section -->
  <section class="hero">
    <div class="hero-content">
      <h1 class="logo">🧩 puzzlux</h1>
      <p class="tagline">Najlepsza gra Sudoku na iOS</p>
      <p class="subtitle">Klasyczne sudoku i rozszerzone warianty w jednej aplikacji</p>
      
      <a href="https://apps.apple.com/app/puzzlux" target="_blank" rel="noreferrer" class="app-store-btn">
        <img src="https://developer.apple.com/assets/elements/badges/download-on-the-app-store.svg" alt="Pobierz w App Store" />
      </a>
    </div>
  </section>

  <!-- Features Section -->
  <section class="features">
    <h2>🎮 Tryby gry</h2>
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

  <!-- Difficulties Section -->
  <section class="difficulties">
    <h2>📊 Poziomy trudności</h2>
    <div class="difficulty-list">
      {#each difficulties as diff}
        <div class="difficulty-item" style="--accent: {diff.color}">
          <span class="difficulty-name">{diff.name}</span>
          <span class="difficulty-desc">{diff.desc}</span>
        </div>
      {/each}
    </div>
  </section>

  <!-- Game Modes Section -->
  <section class="game-modes">
    <h2>🎯 Tryby rozgrywki</h2>
    <div class="modes-grid">
      {#each gameModes as mode}
        <div class="mode-card">
          <span class="mode-icon">{mode.icon}</span>
          <h3>{mode.name}</h3>
          <p>{mode.desc}</p>
        </div>
      {/each}
    </div>
  </section>

  <!-- Features List -->
  <section class="highlights">
    <h2>✨ Funkcje</h2>
    <ul class="highlights-list">
      <li>🏆 Game Center - rankingi i osiągnięcia</li>
      <li>☁️ Synchronizacja iCloud między urządzeniami</li>
      <li>🎯 Wyzwania od znajomych</li>
      <li>📈 Szczegółowe statystyki</li>
      <li>🌙 Tryb ciemny i jasny</li>
      <li>📱 Wsparcie dla iPhone i iPad</li>
      <li>✏️ Notatki ołówkowe</li>
      <li>💡 System podpowiedzi</li>
    </ul>
  </section>

  <!-- CTA Section -->
  <section class="cta">
    <h2>Gotowy na wyzwanie? 🧠</h2>
    <p>Pobierz puzzlux i sprawdź swoje umiejętności logiczne!</p>
    <a href="https://apps.apple.com/app/puzzlux" target="_blank" rel="noreferrer" class="app-store-btn">
      <img src="https://developer.apple.com/assets/elements/badges/download-on-the-app-store.svg" alt="Pobierz w App Store" />
    </a>
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

  /* Difficulties */
  .difficulty-list {
    display: flex;
    flex-direction: column;
    gap: 15px;
  }

  .difficulty-item {
    background: rgba(255,255,255,0.05);
    border-radius: 10px;
    padding: 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-left: 4px solid var(--accent);
    transition: transform 0.3s ease;
  }

  .difficulty-item:hover {
    transform: translateX(10px);
  }

  .difficulty-name {
    font-weight: bold;
    font-size: 1.2em;
    color: var(--accent);
  }

  .difficulty-desc {
    color: #aaa;
  }

  /* Game Modes */
  .modes-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 20px;
  }

  .mode-card {
    background: rgba(255,255,255,0.05);
    border-radius: 15px;
    padding: 30px;
    text-align: center;
    border: 1px solid rgba(255,255,255,0.1);
    transition: transform 0.3s ease;
  }

  .mode-card:hover {
    transform: scale(1.05);
  }

  .mode-icon {
    font-size: 3em;
    display: block;
    margin-bottom: 15px;
  }

  .mode-card h3 {
    margin: 0 0 10px;
    color: #ffd700;
  }

  .mode-card p {
    margin: 0;
    color: #ccc;
  }

  /* Highlights */
  .highlights-list {
    list-style: none;
    padding: 0;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 15px;
  }

  .highlights-list li {
    background: rgba(255,255,255,0.05);
    padding: 15px 20px;
    border-radius: 10px;
    font-size: 1.1em;
    transition: background 0.3s ease;
  }

  .highlights-list li:hover {
    background: rgba(255,255,255,0.1);
  }

  /* CTA */
  .cta {
    text-align: center;
    padding: 60px 20px;
    background: linear-gradient(180deg, transparent 0%, rgba(0,212,255,0.1) 100%);
  }

  .cta h2 {
    color: white;
    font-size: 2.5em;
  }

  .cta p {
    font-size: 1.2em;
    color: #aaa;
    margin-bottom: 30px;
  }

  @media (max-width: 600px) {
    .logo {
      font-size: 2.5em;
    }

    .tagline {
      font-size: 1.2em;
    }

    .difficulty-item {
      flex-direction: column;
      text-align: center;
      gap: 5px;
    }
  }
</style>
