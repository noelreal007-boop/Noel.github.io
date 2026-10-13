<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>[Your Name] | Portfolio</title>
  <meta name="description" content="Portfolio of [Your Name]">
  <style>
    :root {
      --bg: #ffffff;
      --text: #1f2937;
      --muted: #6b7280;
      --card: #f3f4f6;
      --accent: #2563eb;
    }
    @media (prefers-color-scheme: dark) {
      :root {
        --bg: #0f172a;
        --text: #e5e7eb;
        --muted: #94a3b8;
        --card: #1e293b;
        --accent: #60a5fa;
      }
    }
    * { box-sizing: border-box; margin: 0; padding: 0; }
    html { scroll-behavior: smooth; }
    body {
      font-family: system-ui, -apple-system, "Segoe UI", Roboto, sans-serif;
      background: var(--bg);
      color: var(--text);
      line-height: 1.6;
    }
    a { color: var(--accent); text-decoration: none; }
    a:hover { text-decoration: underline; }
    .container { max-width: 800px; margin: 0 auto; padding: 0 1.25rem; }

    header {
      position: sticky; top: 0;
      background: var(--bg);
      border-bottom: 1px solid var(--card);
      z-index: 10;
    }
    nav { display: flex; justify-content: space-between; align-items: center; padding: 1rem 0; }
    nav .logo { font-weight: 700; color: var(--text); }
    nav ul { display: flex; gap: 1.25rem; list-style: none; }

    section { padding: 3.5rem 0; }
    h1 { font-size: 2.5rem; line-height: 1.2; }
    h2 { font-size: 1.5rem; margin-bottom: 1.25rem; }
    .tagline { color: var(--muted); font-size: 1.15rem; margin: 0.75rem 0 1.5rem; }

    .btn {
      display: inline-block;
      background: var(--accent);
      color: #fff;
      padding: 0.6rem 1.2rem;
      border-radius: 8px;
      font-weight: 600;
    }
    .btn:hover { text-decoration: none; opacity: 0.9; }
    .btn.outline { background: transparent; color: var(--accent); border: 2px solid var(--accent); margin-left: 0.5rem; }

    .skills { display: flex; flex-wrap: wrap; gap: 0.5rem; margin-top: 1rem; }
    .skills span { background: var(--card); padding: 0.35rem 0.8rem; border-radius: 999px; font-size: 0.9rem; }

    .projects { display: grid; gap: 1rem; grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); }
    .card { background: var(--card); padding: 1.25rem; border-radius: 12px; }
    .card h3 { margin-bottom: 0.4rem; }
    .card p { color: var(--muted); font-size: 0.95rem; margin-bottom: 0.75rem; }

    footer { text-align: center; color: var(--muted); padding: 2rem 0; border-top: 1px solid var(--card); font-size: 0.9rem; }
  </style>
</head>
<body>

  <header>
    <div class="container">
      <nav>
        <a href="#" class="logo">[Your Name]</a>
        <ul>
          <li><a href="#about">About</a></li>
          <li><a href="#projects">Projects</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <main class="container">
    <section id="home">
      <h1>Hi, I'm [Noel Vitalicio Jr.] </h1>
      <p class="tagline">[Your role,BSCOE Student / Aspiring Web Developer]</p>
      <a href="#projects" class="btn">View my work</a>
      <a href="#contact" class="btn outline">Contact me</a>
    </section>

    <section id="about">
      <h2>About Me</h2>
      <p>
        [Write 2–3 sentences about yourself: what you study or do, what you enjoy building,
        and what you're currently learning.]
      </p>
      <div class="skills">
        <span>HTML</span>
        <span>CSS</span>
        <span>JavaScript</span>
        <span>Git &amp; GitHub</span>
        <span>[Add more]</span>
      </div>
    </section>

    <section id="projects">
      <h2>Projects</h2>
      <div class="projects">
        <div class="card">
          <h3>[Project One]</h3>
          <p>[Short description of what it does and what you used to build it.]</p>
          <a href="https://github.com/[username]/[repo]">View on GitHub →</a>
        </div>
        <div class="card">
          <h3>[Project Two]</h3>
          <p>[Short description of what it does and what you used to build it.]</p>
          <a href="https://github.com/[username]/[repo]">View on GitHub →</a>
        </div>
        <div class="card">
          <h3>[Project Three]</h3>
          <p>[Short description of what it does and what you used to build it.]</p>
          <a href="https://github.com/[username]/[repo]">View on GitHub →</a>
        </div>
      </div>
    </section>

    <section id="contact">
      <h2>Contact</h2>
      <p>Want to work together or just say hi?</p>
      <p>
         <a href="mailto:[you@example.com]">[you@example.com]</a><br>
         <a href="https://github.com/[username]">github.com/[username]</a><br>
         <a href="https://linkedin.com/in/[username]">LinkedIn</a>
      </p>
    </section>
  </main>

  <footer>
    <p>&copy; 2026 [Your Name]. Built with HTML &amp; CSS.</p>
  </footer>

</body>
</html>
