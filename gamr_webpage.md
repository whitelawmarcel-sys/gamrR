<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>gamR — A tiny arcade</title>
  <link rel="icon" href="/favicon.svg?v=2" type="image/svg+xml">
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap" rel="stylesheet">
  
  <style>
    :root {
      --bg-color: #0f172a;
      --card-bg: #1e293b;
      --text-main: #f8fafc;
      --text-muted: #94a3b8;
      --accent: #38bdf8;
      --accent-dot: #f43f5e;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: 'Inter', system-ui, -apple-system, sans-serif;
      background-color: var(--bg-color);
      color: var(--text-main);
      display: flex;
      flex-direction: column;
      min-height: 100vh;
      padding: 2rem 1rem;
    }

    header {
      text-align: center;
      margin-bottom: 2.5rem;
    }

    header h1 {
      font-size: 3rem;
      font-weight: 800;
      letter-spacing: -0.05em;
    }

    header h1 span {
      color: var(--accent-dot);
    }

    header p {
      color: var(--text-muted);
      margin-top: 0.5rem;
      font-size: 1.1rem;
    }

    main {
      flex: 1;
      max-width: 900px;
      width: 100%;
      margin: 0 auto;
    }

    .controls {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 2rem;
    }

    .games-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
      gap: 1.5rem;
    }

    .game-card {
      background-color: var(--card-bg);
      border-radius: 12px;
      padding: 1.5rem;
      border: 1px solid rgba(255, 255, 255, 0.05);
      transition: transform 0.2s ease, box-shadow 0.2s ease;
    }

    .game-card:hover {
      transform: translateY(-4px);
      box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.3);
    }

    footer {
      text-align: center;
      margin-top: 4rem;
      padding-top: 2rem;
      border-top: 1px solid rgba(255, 255, 255, 0.1);
      color: var(--text-muted);
      font-size: 0.9rem;
    }

    footer a {
      color: var(--accent);
      text-decoration: none;
    }

    footer a:hover {
      text-decoration: underline;
    }
  </style>
</head>
<body>

  <header>
    <h1>gamR<span>.</span></h1>
    <p>A tiny arcade of little games. Pick one.</p>
  </header>

  <main>
    <div class="controls">
      <div role="group" aria-label="Which games to show">
        <!-- Filter buttons or tags can go here -->
      </div>
    </div>

    <section class="games-grid" aria-label="Games">
      <!-- Game cards will load here -->
    </section>
  </main>

  <footer>
    <p>gamR — more games landing soon.</p>
    <p><a href="/admin">Manage links</a></p>
  </footer>

</body>
</html>