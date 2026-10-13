<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Noel Vitalicio Jr. | Portfolio</title>
  <meta name="description" content="Portfolio of Noel Vitalicio Jr., Computer Engineering student and aspiring web/apps software developer">
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@400;500;600;700&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg: #ffffff;
      --text: #111111;
      --muted: #555555;
      --card: #ffffff;
      --border: #e8e8e8;
    }
    @media (prefers-color-scheme: dark) {
      :root {
        --bg: #0a0a0a;
        --text: #f5f5f5;
        --muted: #a3a3a3;
        --card: #141414;
        --border: #262626;
      }
    }
    * { box-sizing: border-box; margin: 0; padding: 0; }
    html { scroll-behavior: smooth; }
    body {
      font-family: "Quicksand", system-ui, -apple-system, "Segoe UI", Roboto, sans-serif;
      background: var(--bg);
      color: var(--text);
      line-height: 1.6;
    }
    a { color: inherit; text-decoration: none; }

    /* ---------- Layout ---------- */
    .layout { display: flex; min-height: 100vh; }

    /* ---------- Sidebar ---------- */
    .sidebar {
      width: 340px;
      flex-shrink: 0;
      position: sticky; top: 0; height: 100vh;
      display: flex; flex-direction: column; justify-content: flex-end;
      padding: 2.5rem 2rem;
      color: #fff;
      background:
        radial-gradient(ellipse at 20% 15%, rgba(214, 120, 60, .55), transparent 55%),
        radial-gradient(ellipse at 85% 45%, rgba(240, 150, 70, .45), transparent 50%),
        radial-gradient(ellipse at 10% 80%, rgba(120, 40, 25, .75), transparent 60%),
        linear-gradient(160deg, #2a1410 0%, #5b2a1c 35%, #8a4527 55%, #3a1a14 80%, #1a0c0a 100%);
    }
    .avatar {
      width: 120px; height: 120px;
      border-radius: 8px;
      background: rgba(0, 0, 0, .55);
      border: 1px solid rgba(255, 255, 255, .15);
      display: flex; align-items: center; justify-content: center;
      font-size: 2.6rem; font-weight: 700; color: #fff;
      object-fit: cover;
      margin-bottom: 1.5rem;
    }
    .name { font-size: 1.2rem; font-weight: 700; }
    .handle { font-size: .95rem; opacity: .85; margin-bottom: 1rem; }
    .role { font-size: 1.15rem; font-weight: 500; line-height: 1.35; margin-bottom: 1.25rem; }
    .meta { list-style: none; font-size: .85rem; margin-bottom: 1.25rem; }
    .meta li { display: flex; align-items: center; gap: .55rem; margin-bottom: .35rem; opacity: .95; }
    .meta a:hover { text-decoration: underline; }

    .social { display: flex; flex-wrap: wrap; gap: .5rem; }
    .social a {
      font-size: .8rem; font-weight: 600;
      padding: .35rem .8rem; border-radius: 999px;
      background: rgba(255, 255, 255, .14);
      border: 1px solid rgba(255, 255, 255, .22);
      transition: background .15s;
    }
    .social a:hover { background: rgba(255, 255, 255, .3); }

    /* ---------- Main ---------- */
    main { flex: 1; padding: 4rem 3.5rem 3rem; max-width: 960px; }
    section { margin-bottom: 4.5rem; scroll-margin-top: 2rem; }
    h2 { font-size: 2.4rem; font-weight: 600; letter-spacing: -.02em; margin-bottom: 1.75rem; }

    /* Intro */
    .intro .hello { color: var(--muted); font-weight: 600; margin-bottom: .5rem; }
    .intro h1 { font-size: clamp(2rem, 5vw, 2.8rem); font-weight: 700; line-height: 1.15; letter-spacing: -.02em; margin-bottom: 1rem; }
    .intro p { max-width: 60ch; color: var(--muted); font-weight: 500; margin-bottom: 1.5rem; }
    .btn {
      display: inline-block;
      background: var(--text); color: var(--bg);
      padding: .65rem 1.3rem; border-radius: 6px; font-weight: 600;
      margin: 0 .5rem .5rem 0;
    }
    .btn:hover { opacity: .85; }
    .btn.outline { background: transparent; color: var(--text); border: 2px solid var(--text); }

    /* Repo-style cards */
    .grid { display: grid; gap: 1.1rem; grid-template-columns: repeat(auto-fill, minmax(260px, 1fr)); }
    .card {
      display: block;
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 6px;
      padding: 1.1rem 1.2rem;
      transition: transform .15s, box-shadow .15s;
    }
    .card:hover { transform: translateY(-3px); box-shadow: 0 8px 24px rgba(0, 0, 0, .12); }
    .card h3 { font-size: 1.05rem; font-weight: 600; margin-bottom: .35rem; }
    .card p { font-size: .85rem; color: var(--muted); margin-bottom: .6rem; font-weight: 500; }
    .card .my-role { font-size: .8rem; font-weight: 600; color: var(--text); margin-bottom: .9rem; }
    .stats { display: flex; gap: 1rem; font-size: .75rem; color: var(--muted); font-weight: 600; }
    .stats span { display: inline-flex; align-items: center; gap: .3rem; }

    /* About */
    .about p { max-width: 62ch; color: var(--muted); font-weight: 500; margin-bottom: 1.25rem; }
    .skills { display: flex; flex-wrap: wrap; gap: .5rem; }
    .skills span {
      font-size: .85rem; font-weight: 600;
      border: 1px solid var(--border); background: var(--card);
      padding: .3rem .85rem; border-radius: 6px;
    }

    /* Education */
    .edu { border-left: 2px solid var(--border); padding-left: 1.25rem; }
    .edu .item { margin-bottom: 1.25rem; }
    .edu .item:last-child { margin-bottom: 0; }
    .edu .when { font-size: .85rem; color: var(--muted); font-weight: 500; }

    /* Contact */
    .contact-text { color: var(--muted); font-weight: 500; max-width: 55ch; margin-bottom: 1.5rem; }
    .contact-grid { display: grid; gap: 1.1rem; grid-template-columns: repeat(auto-fill, minmax(260px, 1fr)); }
    .contact-card {
      display: flex; align-items: center; gap: .9rem;
      background: var(--card); border: 1px solid var(--border);
      border-radius: 6px; padding: 1rem 1.2rem;
      transition: transform .15s, box-shadow .15s;
    }
    .contact-card:hover { transform: translateY(-3px); box-shadow: 0 8px 24px rgba(0, 0, 0, .12); }
    .contact-card .icon { font-size: 1.5rem; }
    .contact-card .label { display: block; font-size: .75rem; color: var(--muted); font-weight: 600; }
    .contact-card .value { font-weight: 600; font-size: .95rem; word-break: break-all; }

    footer { color: var(--muted); font-size: .85rem; font-weight: 500; }

    /* ---------- Mobile ---------- */
    @media (max-width: 860px) {
      .layout { flex-direction: column; }
      .sidebar { width: 100%; height: auto; position: static; padding: 3rem 1.5rem 2rem; }
      main { padding: 2.5rem 1.5rem; }
      h2 { font-size: 2rem; }
    }
  </style>
</head>
<body>
  <div class="layout">

    <!-- ===== LEFT PROFILE PANEL ===== -->
    <aside class="sidebar">
      <!-- To use a photo, replace the div below with:
           <img class="avatar" src="photo.jpg" alt="Noel Vitalicio Jr."> -->
      <div class="avatar" aria-hidden="true">NV</div>

      <div class="name">Noel Vitalicio Jr.</div>
      <div class="handle">@your-username</div>
      <div class="role">Computer Engineering Student &amp; Aspiring Web/Apps Software Developer</div>

      <ul class="meta">
        <li>🔗 <a href="https://your-username.github.io/">your-username.github.io</a></li>
        <li>📍 [Your City], Philippines</li>
        <li>🎓 ICCT Colleges</li>
      </ul>

      <div class="social">
        <a href="mailto:you@example.com">Email</a>
        <a href="https://github.com/your-username" target="_blank" rel="noopener">GitHub</a>
        <a href="https://www.linkedin.com/in/your-username" target="_blank" rel="noopener">LinkedIn</a>
        <a href="https://www.facebook.com/your-username" target="_blank" rel="noopener">Facebook</a>
      </div>
    </aside>

    <!-- ===== RIGHT CONTENT ===== -->
    <main>

      <section id="home" class="intro">
        <p class="hello">👋 Hello, welcome to my portfolio</p>
        <h1>I'm Noel Vitalicio Jr.</h1>
        <p>
          I'm a Computer Engineering student and an aspiring web and apps software
          developer. I enjoy building practical digital tools that solve real problems,
          and I'm always learning new technologies to turn ideas into working software.
          Take a look at my projects below.
        </p>
        <a href="#work" class="btn">View my work</a>
        <a href="#contact" class="btn outline">Contact me</a>
      </section>

      <section id="work">
        <h2>Work.</h2>
        <div class="grid">

          <a class="card" href="https://github.com/your-username/e-request" target="_blank" rel="noopener">
            <h3>E-Request</h3>
            <p>🏫 Centralized info platform for ICCT Colleges students: offices, services, requirements, and procedures in one place.</p>
            <div class="my-role">My role: Lead Backend Developer</div>
            <div class="stats">
              <span>&lt;/&gt; [Language]</span><span>★ 0</span><span>⑂ 0</span>
            </div>
          </a>

          <a class="card" href="https://github.com/your-username/project-two" target="_blank" rel="noopener">
            <h3>[Project Two]</h3>
            <p>[One-line description of what it does.]</p>
            <div class="stats">
              <span>&lt;/&gt; [Language]</span><span>★ 0</span><span>⑂ 0</span>
            </div>
          </a>

          <a class="card" href="https://github.com/your-username/project-three" target="_blank" rel="noopener">
            <h3>[Project Three]</h3>
            <p>[One-line description of what it does.]</p>
            <div class="stats">
              <span>&lt;/&gt; [Language]</span><span>★ 0</span><span>⑂ 0</span>
            </div>
          </a>

          <a class="card" href="https://github.com/your-username/project-four" target="_blank" rel="noopener">
            <h3>[Project Four]</h3>
            <p>[One-line description of what it does.]</p>
            <div class="stats">
              <span>&lt;/&gt; [Language]</span><span>★ 0</span><span>⑂ 0</span>
            </div>
          </a>

        </div>
      </section>

      <section id="about" class="about">
        <h2>About.</h2>
        <p>
          Hi, I'm Noel, a Computer Engineering student aiming to build a career in web and
          apps software development. I like the challenge of taking an idea from a rough
          concept to something people can actually use, from the interface to the logic
          running behind it.
        </p>
        <p>
          I'm currently looking for opportunities to learn and grow, such as internships,
          collaborations, and projects where I can sharpen my skills and contribute to a team.
        </p>
        <div class="skills">
          <span>HTML</span>
          <span>CSS</span>
          <span>JavaScript</span>
          <span>Backend Development</span>
          <span>Git &amp; GitHub</span>
          <span>[Add more]</span>
        </div>
      </section>

      <section id="education">
        <h2>Education.</h2>
        <div class="edu">
          <div class="item">
            <strong>Bachelor of Science in Computer Engineering</strong><br>
            ICCT Colleges
            <div class="when">[Year] – Present</div>
          </div>
          <div class="item">
            <strong>[Senior High School Strand]</strong><br>
            [Previous School]
            <div class="when">[Year] – [Year]</div>
          </div>
        </div>
      </section>

      <section id="contact">
        <h2>Contact.</h2>
        <p class="contact-text">
          I'm open to collaborations, internships, and new opportunities. Click any link
          below to reach me.
        </p>
        <div class="contact-grid">
          <a class="contact-card" href="mailto:you@example.com">
            <span class="icon">📧</span>
            <span><span class="label">Email</span><span class="value">you@example.com</span></span>
          </a>
          <a class="contact-card" href="https://github.com/your-username" target="_blank" rel="noopener">
            <span class="icon">🐙</span>
            <span><span class="label">GitHub</span><span class="value">github.com/your-username</span></span>
          </a>
          <a class="contact-card" href="https://www.linkedin.com/in/your-username" target="_blank" rel="noopener">
            <span class="icon">💼</span>
            <span><span class="label">LinkedIn</span><span class="value">linkedin.com/in/your-username</span></span>
          </a>
          <a class="contact-card" href="https://www.facebook.com/your-username" target="_blank" rel="noopener">
            <span class="icon">📘</span>
            <span><span class="label">Facebook</span><span class="value">facebook.com/your-username</span></span>
          </a>
          <a class="contact-card" href="tel:+639000000000">
            <span class="icon">📱</span>
            <span><span class="label">Phone</span><span class="value">+63 900 000 0000</span></span>
          </a>
        </div>
      </section>

      <footer>
        <p>&copy; 2026 Noel Vitalicio Jr. Hosted on GitHub Pages.</p>
      </footer>

    </main>
  </div>
</body>
</html>
