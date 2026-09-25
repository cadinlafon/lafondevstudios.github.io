```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <meta name="description" content="LaFon Dev Studios builds software, open-source tools, and technology projects.">
  <meta name="author" content="LaFon Dev Studios">

  <title>LaFon Dev Studios</title>

  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family:
        -apple-system,
        BlinkMacSystemFont,
        "Segoe UI",
        Roboto,
        Helvetica,
        Arial,
        sans-serif;
      background: #0b0f14;
      color: #f5f7fa;
      line-height: 1.6;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    .container {
      width: min(1100px, 92%);
      margin: 0 auto;
    }

    /* NAVIGATION */

    nav {
      position: sticky;
      top: 0;
      z-index: 100;
      backdrop-filter: blur(14px);
      background: rgba(11, 15, 20, 0.82);
      border-bottom: 1px solid #202833;
    }

    .nav-inner {
      height: 70px;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .logo {
      font-size: 1.1rem;
      font-weight: 800;
      letter-spacing: -0.03em;
    }

    .logo span {
      color: #6ea8fe;
    }

    .nav-links {
      display: flex;
      gap: 26px;
      list-style: none;
    }

    .nav-links a {
      color: #aeb8c4;
      font-size: 0.95rem;
      transition: color 0.2s ease;
    }

    .nav-links a:hover {
      color: #ffffff;
    }

    /* HERO */

    .hero {
      min-height: 650px;
      display: flex;
      align-items: center;
      position: relative;
      overflow: hidden;
    }

    .hero::before {
      content: "";
      position: absolute;
      width: 600px;
      height: 600px;
      border-radius: 50%;
      background: rgba(65, 105, 225, 0.12);
      filter: blur(100px);
      top: -250px;
      right: -150px;
      pointer-events: none;
    }

    .hero-content {
      max-width: 780px;
      position: relative;
      z-index: 1;
    }

    .eyebrow {
      display: inline-block;
      padding: 7px 13px;
      border: 1px solid #283443;
      border-radius: 999px;
      color: #9eb7d3;
      background: #111821;
      font-size: 0.85rem;
      margin-bottom: 25px;
    }

    h1 {
      font-size: clamp(3rem, 8vw, 6rem);
      line-height: 0.98;
      letter-spacing: -0.065em;
      margin-bottom: 28px;
    }

    h1 span {
      color: #6ea8fe;
    }

    .hero p {
      max-width: 650px;
      color: #aeb8c4;
      font-size: 1.2rem;
      margin-bottom: 35px;
    }

    .buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 13px;
    }

    .button {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      padding: 12px 19px;
      border-radius: 9px;
      border: 1px solid #2a3543;
      background: #151c25;
      color: #ffffff;
      font-weight: 600;
      transition:
        transform 0.2s ease,
        background 0.2s ease,
        border-color 0.2s ease;
    }

    .button:hover {
      transform: translateY(-2px);
      background: #1b2531;
      border-color: #3d4c5f;
    }

    .button.primary {
      background: #6ea8fe;
      border-color: #6ea8fe;
      color: #08111c;
    }

    .button.primary:hover {
      background: #82b4ff;
    }

    /* SECTIONS */

    section {
      padding: 100px 0;
      border-top: 1px solid #1d252f;
    }

    .section-heading {
      margin-bottom: 45px;
    }

    .section-heading h2 {
      font-size: 2.3rem;
      letter-spacing: -0.04em;
      margin-bottom: 10px;
    }

    .section-heading p {
      color: #8f9baa;
      max-width: 650px;
    }

    /* PROJECTS */

    .projects {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 20px;
    }

    .project {
      display: flex;
      flex-direction: column;
      padding: 28px;
      min-height: 260px;
      border: 1px solid #252e39;
      border-radius: 15px;
      background: #10161e;
      transition:
        transform 0.2s ease,
        border-color 0.2s ease;
    }

    .project:hover {
      transform: translateY(-4px);
      border-color: #3b4a5c;
    }

    .project-icon {
      width: 45px;
      height: 45px;
      display: flex;
      align-items: center;
      justify-content: center;
      border-radius: 10px;
      background: #192231;
      margin-bottom: 20px;
      font-size: 1.3rem;
    }

    .project h3 {
      font-size: 1.35rem;
      margin-bottom: 9px;
    }

    .project p {
      color: #929dab;
      font-size: 0.95rem;
      margin-bottom: 20px;
    }

    .project-link {
      margin-top: auto;
      color: #76adff;
      font-weight: 600;
      font-size: 0.9rem;
    }

    /* ABOUT */

    .about {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 60px;
      align-items: start;
    }

    .about h2 {
      font-size: 2.3rem;
      letter-spacing: -0.04em;
      margin-bottom: 15px;
    }

    .about p {
      color: #9aa5b2;
      margin-bottom: 15px;
    }

    .values {
      display: grid;
      gap: 15px;
    }

    .value {
      padding: 20px;
      border: 1px solid #252e39;
      border-radius: 12px;
      background: #10161e;
    }

    .value h3 {
      margin-bottom: 5px;
    }

    .value p {
      margin: 0;
      font-size: 0.9rem;
    }

    /* OPEN SOURCE */

    .opensource {
      padding: 35px;
      border: 1px solid #293544;
      border-radius: 16px;
      background:
        linear-gradient(
          135deg,
          #111a25,
          #0e141b
        );
    }

    .opensource h2 {
      font-size: 2rem;
      margin-bottom: 12px;
    }

    .opensource p {
      color: #9ba6b3;
      max-width: 700px;
      margin-bottom: 25px;
    }

    /* FOOTER */

    footer {
      padding: 35px 0;
      border-top: 1px solid #1d252f;
      color: #788492;
      font-size: 0.9rem;
    }

    .footer-inner {
      display: flex;
      justify-content: space-between;
      gap: 20px;
      flex-wrap: wrap;
    }

    .footer-links {
      display: flex;
      gap: 20px;
    }

    .footer-links a:hover {
      color: #ffffff;
    }

    /* MOBILE */

    @media (max-width: 750px) {
      .nav-links {
        display: none;
      }

      .hero {
        min-height: 570px;
      }

      .hero p {
        font-size: 1.05rem;
      }

      .projects {
        grid-template-columns: 1fr;
      }

      .about {
        grid-template-columns: 1fr;
        gap: 35px;
      }

      section {
        padding: 70px 0;
      }
    }
  </style>
</head>

<body>

  <!-- NAVIGATION -->

  <nav>
    <div class="container nav-inner">
      <a href="#" class="logo">
        LaFon <span>Dev Studios</span>
      </a>

      <ul class="nav-links">
        <li><a href="#projects">Projects</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#opensource">Open Source</a></li>
        <li>
          <a
            href="https://github.com/lafondevstudios"
            target="_blank"
            rel="noopener"
          >
            GitHub
          </a>
        </li>
      </ul>
    </div>
  </nav>


  <!-- HERO -->

  <main>

    <section class="hero">
      <div class="container">
        <div class="hero-content">

          <div class="eyebrow">
            Software · Technology · Open Source
          </div>

          <h1>
            Building useful<br>
            <span>software.</span>
          </h1>

          <p>
            LaFon Dev Studios builds software, developer tools,
            and open-source projects designed to solve real-world
            problems and make technology more useful.
          </p>

          <div class="buttons">
            <a href="#projects" class="button primary">
              Explore Projects
            </a>

            <a
              href="https://github.com/lafondevstudios"
              class="button"
              target="_blank"
              rel="noopener"
            >
              View GitHub
            </a>
          </div>

        </div>
      </div>
    </section>


    <!-- PROJECTS -->

    <section id="projects">

      <div class="container">

        <div class="section-heading">
          <h2>Projects</h2>

          <p>
            A collection of applications, developer tools,
            experiments, and open-source software.
          </p>
        </div>

        <div class="projects">

          <!-- MONETA -->

          <a
            class="project"
            href="https://github.com/cadinlafon/monetafinance"
            target="_blank"
            rel="noopener"
          >
            <div class="project-icon">💰</div>

            <h3>Moneta</h3>

            <p>
              A personal finance platform for tracking money,
              transactions, budgets, goals, accounts, and more.
            </p>

            <span class="project-link">
              View project →
            </span>
          </a>


          <!-- MONETA EMAIL SYNC -->

          <a
            class="project"
            href="https://github.com/cadinlafon/Moneta-Email-Sync"
            target="_blank"
            rel="noopener"
          >
            <div class="project-icon">📧</div>

            <h3>Moneta Email Sync</h3>

            <p>
              An open-source tool for turning financial emails
              into structured transaction data for personal
              finance applications.
            </p>

            <span class="project-link">
              View project →
            </span>
          </a>


          <!-- SERMON AUDIO -->

          <a
            class="project"
            href="https://github.com/cadinlafon/sermon-audio-app"
            target="_blank"
            rel="noopener"
          >
            <div class="project-icon">🎧</div>

            <h3>Sermon Audio</h3>

            <p>
              A modern audio application for organizing,
              discovering, and listening to sermons and
              teaching.
            </p>

            <span class="project-link">
              View project →
            </span>
          </a>


          <!-- OOPS WRONG VILLAGE -->

          <a
            class="project"
            href="https://github.com/cadinlafon"
            target="_blank"
            rel="noopener"
          >
            <div class="project-icon">🎮</div>

            <h3>More Projects</h3>

            <p>
              Games, experiments, utilities, and other projects
              are available on GitHub.
            </p>

            <span class="project-link">
              Browse GitHub →
            </span>
          </a>

        </div>

      </div>

    </section>


    <!-- ABOUT -->

    <section id="about">

      <div class="container">

        <div class="about">

          <div>
            <h2>About LaFon Dev Studios</h2>

            <p>
              LaFon Dev Studios is an independent software
              development studio focused on building useful,
              practical technology.
            </p>

            <p>
              Projects range from personal finance software
              and developer tools to applications, experiments,
              and open-source projects.
            </p>
          </div>

          <div class="values">

            <div class="value">
              <h3>🛠 Build</h3>
              <p>
                Create practical software that solves real
                problems.
              </p>
            </div>

            <div class="value">
              <h3>🌎 Open</h3>
              <p>
                Share useful tools and make projects accessible
                to other developers.
              </p>
            </div>

            <div class="value">
              <h3>💡 Experiment</h3>
              <p>
                Explore new technologies and turn interesting
                ideas into working projects.
              </p>
            </div>

          </div>

        </div>

      </div>

    </section>


    <!-- OPEN SOURCE -->

    <section id="opensource">

      <div class="container">

        <div class="opensource">

          <h2>Open Source</h2>

          <p>
            Many LaFon Dev Studios projects are available on
            GitHub. Explore the source code, documentation,
            issues, and development history.
          </p>

          <a
            href="https://github.com/cadinlafon"
            class="button"
            target="_blank"
            rel="noopener"
          >
            Explore GitHub →
          </a>

        </div>

      </div>

    </section>

  </main>


  <!-- FOOTER -->

  <footer>

    <div class="container footer-inner">

      <div>
        © 2026 LaFon Dev Studios
      </div>

      <div class="footer-links">

        <a
          href="https://github.com/cadinlafon"
          target="_blank"
          rel="noopener"
        >
          GitHub
        </a>

        <a href="#projects">
          Projects
        </a>

        <a href="#about">
          About
        </a>

      </div>

    </div>

  </footer>

</body>
</html>
```
