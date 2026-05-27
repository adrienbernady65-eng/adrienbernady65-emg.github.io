# adrienbernady65-emg.github.io[portfolio.html](https://github.com/user-attachments/files/28325896/portfolio.html)
[rapport_stage_premier.pdf](https://github.com/user-attachments/files/28325886/rapport_stage_premier.pdf)
[Rapport_de_stage.pdf](https://github.com/user-attachments/files/28325885/Rapport_de_stage.pdf)
[Rapport de stage.docx](https://github.com/user-attachments/files/28325882/Rapport.de.stage.docx)
[Projet_PHP_compte_rendue.pdf](https://github.com/user-attachments/files/28325878/Projet_PHP_compte_rendue.pdf)
[Projet_bar_compte_rendue.pdf](https://github.com/user-attachments/files/28325875/Projet_bar_compte_rendue.pdf)
[Projet_Android_Studio_compte_rendue.pdf](https://github.com/user-attachments/files/28325870/Projet_Android_Studio_compte_rendue.pdf)
[CV.pdf](https://github.com/user-attachments/files/28325862/CV.pdf)
<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Portfolio</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Sans:ital,wght@0,300;0,400;0,500;1,300&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg: #0d0d0d;
    --surface: #161616;
    --surface2: #1f1f1f;
    --border: rgba(255,255,255,0.08);
    --accent: #c8f56a;
    --accent2: #6af5c8;
    --text: #f0ede6;
    --muted: #888880;
    --font-head: 'Syne', sans-serif;
    --font-body: 'DM Sans', sans-serif;
  }

  html { scroll-behavior: smooth; }

  body {
    font-family: var(--font-body);
    background: var(--bg);
    color: var(--text);
    min-height: 100vh;
    overflow-x: hidden;
    margin-left: 100px;
  }



  /* ═══ NAVBAR ═══ */
.navbar {
  position: fixed; top: 0; left: 0; right: 0; z-index: 100;
  background: rgba(13,13,13,0.88);
  backdrop-filter: blur(16px);
  border-bottom: 1px solid var(--border);
}
.nav-inner {
  display: flex; align-items: center; justify-content: space-between;
  padding: 0 3rem; height: 64px;
}
.nav-logo {
  font-family: var(--font-head);
  font-weight: 800; font-size: 1.1rem;
  color: var(--accent);
  letter-spacing: -0.02em;
  text-decoration: none;
}
.nav-links { display: flex; gap: 0.5rem; list-style: none; }
.nav-links li a {
  font-size: 0.85rem; font-weight: 500;
  color: var(--muted);
  text-decoration: none;
  padding: 0.45rem 1.1rem;
  border-radius: 99px;
  border: 1px solid transparent;
  transition: all 0.2s;
  display: block;
}
  .nav-links a:hover, .nav-links a.active {
    color: var(--accent);
    border-color: var(--border);
    background: var(--surface2);
  }

  .nav-links a.active { color: var(--accent); }
/* Lien actif via :has() — aucun JS */
body:not(:has(:target)) .nav-links li a[href="#page-home"],
body:has(#page-home:target) .nav-links li a[href="#page-home"],
body:has(#page-stages:target) .nav-links li a[href="#page-stages"],
body:has(#page-projets:target) .nav-links li a[href="#page-projets"],
body:has(#page-veille:target) .nav-links li a[href="#page-veille"] {
  color: var(--text);
  border-color: var(--border);
  background: var(--surface2);
}

  /* ── PAGES ── */

  .page { display: none; }
  .page:target { display: block; }
  #page-home { display: block; }               /* accueil visible par défaut */
  body:has(#page-stages:target) #page-home,
  body:has(#page-projets:target) #page-home,
  body:has(#page-veille:target) #page-home { display: none; }

  /* ── HOME ── */
  .hero {
    min-height: calc(100vh - 80px);
    display: flex; flex-direction: column; justify-content: center;
    padding: 4rem 3rem 3rem;
    position: relative; overflow: hidden;
  }

  .hero::before {
    content: '';
    position: absolute; top: -30%; right: -10%;
    width: 600px; height: 600px; border-radius: 50%;
    background: radial-gradient(circle, rgba(200,245,106,0.07) 0%, transparent 70%);
    pointer-events: none;
  }

  .hero-tag {
    font-size: 0.75rem; font-weight: 500; letter-spacing: 0.12em;
    text-transform: uppercase; color: var(--accent);
    margin-bottom: 1.5rem;
    display: flex; align-items: center; gap: 0.6rem;
  }

  .hero-tag::before {
    content: ''; width: 28px; height: 1px; background: var(--accent);
  }

  .hero h1 {
    font-family: var(--font-head);
    font-size: clamp(3rem, 7vw, 6rem);
    font-weight: 800; line-height: 1.0;
    letter-spacing: -0.04em;
    margin-bottom: 1.5rem;
  }

  .hero h1 span { color: var(--accent); }

  .hero-desc {
    font-size: 1.05rem; color: var(--muted); font-weight: 300;
    max-width: 500px; line-height: 1.7;
    margin-bottom: 3rem;
  }

  .hero-cta { display: flex; gap: 1rem; flex-wrap: wrap; }

  .btn {
    display: inline-flex; align-items: center; gap: 0.5rem;
    padding: 0.85rem 2rem; border-radius: 99px;
    font-family: var(--font-body); font-size: 0.9rem; font-weight: 500;
    text-decoration: none; cursor: pointer; border: none;
    transition: all 0.2s;
  }

  .btn-primary {
    background: var(--accent); color: #0d0d0d;
  }
  .btn-primary:hover { background: #d4fc7a; transform: translateY(-1px); }

  .btn-outline {
    background: transparent; color: var(--text);
    border: 1px solid var(--border);
  }
  .btn-outline:hover { border-color: rgba(255,255,255,0.3); background: var(--surface2); }

  .hero-stats {
    display: flex; gap: 3rem; margin-top: 5rem;
    padding-top: 3rem; border-top: 1px solid var(--border);
  }

  .stat-num {
    font-family: var(--font-head); font-size: 2.2rem; font-weight: 800;
    color: var(--accent); line-height: 1;
  }

  .stat-label { font-size: 0.8rem; color: var(--muted); margin-top: 0.3rem; }

  /* ── SECTION HEADER ── */
  .section { padding: 5rem 3rem; }

  .section-header { margin-bottom: 3.5rem; }

  .section-tag {
    font-size: 0.7rem; font-weight: 500; letter-spacing: 0.15em;
    text-transform: uppercase; color: var(--accent);
    display: flex; align-items: center; gap: 0.5rem;
    margin-bottom: 1rem;
  }

  .section-tag::before { content: ''; width: 20px; height: 1px; background: var(--accent); }

  .section-title {
    font-family: var(--font-head); font-size: clamp(1.8rem, 4vw, 2.8rem);
    font-weight: 800; line-height: 1.1; letter-spacing: -0.03em;
  }

  .section-desc { color: var(--muted); margin-top: 0.8rem; max-width: 500px; font-weight: 300; }

  /* ── CARDS GRID ── */
  .cards-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); gap: 1.5rem; }

  .card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 16px;
    padding: 2rem;
    transition: all 0.25s;
    position: relative; overflow: hidden;
  }

  .card::before {
    content: ''; position: absolute; top: 0; left: 0; right: 0; height: 2px;
    background: linear-gradient(90deg, var(--accent), var(--accent2));
    opacity: 0; transition: opacity 0.25s;
  }

  .card:hover { border-color: rgba(255,255,255,0.15); transform: translateY(-3px); }
  .card:hover::before { opacity: 1; }

  .card-label {
    font-size: 0.7rem; font-weight: 500; letter-spacing: 0.12em;
    text-transform: uppercase; color: var(--accent);
    margin-bottom: 0.8rem;
  }

  .card-title {
    font-family: var(--font-head); font-size: 1.25rem;
    font-weight: 700; margin-bottom: 0.6rem;
  }

  .card-desc { color: var(--muted); font-size: 0.9rem; line-height: 1.6; font-weight: 300; }

  .card-meta {
    display: flex; align-items: center; justify-content: space-between;
    margin-top: 1.5rem; padding-top: 1.5rem; border-top: 1px solid var(--border);
  }

  .card-period { font-size: 0.8rem; color: var(--muted); }

  .tag {
    display: inline-flex; align-items: center;
    padding: 0.2rem 0.6rem; border-radius: 99px;
    font-size: 0.72rem; font-weight: 500;
    background: rgba(200,245,106,0.1); color: var(--accent);
    border: 1px solid rgba(200,245,106,0.2);
  }

  .tags { display: flex; flex-wrap: wrap; gap: 0.4rem; margin-top: 1rem; }

  /* ── STAGE PAGE ── */
  .timeline { position: relative; padding-left: 2rem; }
  .timeline::before {
    content: ''; position: absolute; left: 0; top: 0; bottom: 0;
    width: 1px; background: var(--border);
  }

  .timeline-item { position: relative; margin-bottom: 3rem; }
  .timeline-item::before {
    content: ''; position: absolute; left: -2rem; top: 0.4rem;
    width: 8px; height: 8px; border-radius: 50%;
    background: var(--accent); margin-left: -4px;
    box-shadow: 0 0 0 3px rgba(200,245,106,0.15);
  }

  .timeline-date { font-size: 0.75rem; color: var(--accent); font-weight: 500; margin-bottom: 0.5rem; }
  .timeline-company { font-family: var(--font-head); font-size: 1.3rem; font-weight: 700; margin-bottom: 0.3rem; }
  .timeline-role { color: var(--muted); font-size: 0.9rem; margin-bottom: 0.8rem; }
  .timeline-desc { color: var(--muted); font-size: 0.9rem; line-height: 1.7; font-weight: 300; }

  .timeline-skills { display: flex; flex-wrap: wrap; gap: 0.4rem; margin-top: 1rem; }

  /* ── VEILLE ── */
  .veille-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(280px, 1fr)); gap: 1.2rem; }

  .veille-card {
    background: var(--surface); border: 1px solid var(--border);
    border-radius: 12px; padding: 1.5rem;
    transition: all 0.2s;
  }

  .veille-card:hover { border-color: rgba(255,255,255,0.15); }

  .veille-icon {
    width: 40px; height: 40px; border-radius: 10px;
    background: rgba(200,245,106,0.1);
    display: flex; align-items: center; justify-content: center;
    font-size: 1.2rem; margin-bottom: 1rem;
  }

  .veille-topic { font-family: var(--font-head); font-weight: 700; margin-bottom: 0.4rem; }
  .veille-desc { color: var(--muted); font-size: 0.85rem; line-height: 1.6; font-weight: 300; }

  .source-list { margin-top: 1rem; }
  .source-item {
    font-size: 0.8rem; color: var(--muted);
    padding: 0.3rem 0; border-bottom: 1px solid var(--border);
    display: flex; align-items: center; gap: 0.4rem;
  }
  .source-item:last-child { border-bottom: none; }
  .source-item::before { content: '→'; color: var(--accent); font-size: 0.7rem; }

  /* ── FOOTER ── */
  footer {
    padding: 3rem; border-top: 1px solid var(--border);
    text-align: center; color: var(--muted); font-size: 0.85rem;
  }

  /* ── RESPONSIVE ── */
  @media (max-width: 768px) {
    nav { padding: 1rem 1.5rem; }
    .nav-logo { font-size: 1rem; }
    .nav-links a { padding: 0.4rem 0.7rem; font-size: 0.8rem; }
    .hero, .section { padding-left: 1.5rem; padding-right: 1.5rem; }
    .hero-stats { gap: 2rem; flex-wrap: wrap; }
  }
</style>
</head>
<body>

<nav class="navbar" id="navbar">
  <div class="nav-inner">
    <div class="nav-logo">PORTFOLIO</div>
    <ul class="nav-links">
      <li><a href="#page-home">Accueil</a></li>
      <li><a href="#page-stages">Stages</a></li>
      <li><a href="#page-projets">Projets</a></li>
      <li><a href="#page-CV">CV</a></li>
    </ul>
  </div>
</nav>

<!-- ── PAGE ACCUEIL ── -->
<div class="page active" id="page-home">
  <section class="hero">
    <div class="hero-tag">Étudiant en BTS SIO</div>
    <h1>Adrien<br><span>Bernady</span></h1>
    <div class="hero-stats">
      <div>
        <div class="stat-num">3+</div>
        <div class="stat-label">Projets réalisés</div>
      </div>
      <div>
        <div class="stat-num">2</div>
        <div class="stat-label">Stages effectués</div>
      </div>
  </section>

  <section class="section" style="padding-top: 2rem;">
    <div class="section-header">
      <div class="section-tag">Compétences</div>
      <h2 class="section-title">Ce que je maîtrise</h2>
    </div>
    <div class="cards-grid">
      <div class="card">
        <div class="card-label">Frontend</div>
        <div class="card-title">Développement Web</div>
        <div class="card-desc">Création d'interfaces modernes et responsives avec les technologies actuelles.</div>
        <div class="tags">
          <span class="tag">HTML/CSS</span>
          <span class="tag">JavaScript</span>
        </div>
      </div>
      <div class="card">
        <div class="card-label">Backend</div>
        <div class="card-title">Programmation Serveur</div>
        <div class="card-desc">Développement d'APIs et gestion de bases de données relationnelles.</div>
        <div class="tags">
          <span class="tag">PHP</span>
          <span class="tag">SQL</span>
        </div>
      </div>
    </div>
  </section>
</div>

<!-- ── PAGE STAGES ── -->
<div class="page" id="page-stages">
  <section class="section">
    <div class="section-header">
      <div class="section-tag">Expériences</div>
      <h1 class="section-title">Mes stages</h1>
      <p class="section-desc">Retour d'expérience sur mes périodes en entreprise et les compétences acquises.</p>
    </div>

    <div style="display:grid;grid-template-columns:1fr 2fr;gap:3rem;align-items:start;">
      <div class="timeline">
        <div class="timeline-item">
          <div class="timeline-date">26/05/2025 – 27/05/2025</div>
          <div class="timeline-company">ACS Engineering</div>
          <div class="timeline-role">Administrateur Réseau Stagiaire</div>
          <div class="timeline-desc">
           Participation au déploiement et à la configuration d'une infrastructure réseau hybride.
           Mise en place de VLANs, intégration Active Directory avec synchronisation Entra ID (Azure AD), configuration de serveurs (web, SQL, administration)</div>
          <div class="timeline-skills">
            <span class="tag">AD</span>
            <span class="tag">Entra id</span>
          </div>
        </div>

        <div class="timeline-item">
          <div class="timeline-date">19/01/2026 – 20/02/2026</div>
          <div class="timeline-company">Les Tablier Solidaire</div>
          <div class="timeline-role">Stagiaire Développeur Fullstack</div>
          <div class="timeline-desc">
            Développement d'une application de gestion des employée en local via le language HTML, CSS, javascript pour le Front-end et PHP, SQL pour le Back-end 
          </div>
          <div class="timeline-skills">
            <span class="tag">HTML</span>
            <span class="tag">CSS</span>
            <span class="tag">PHP</span>
            <span class="tag">SQL</span>
          </div>
        </div>
      </div>

      <div>
        <div class="card" style="margin-bottom:1.5rem;">
          <div class="card-label">Premier stage · Bilan</div>
          <div class="card-title">ACS Engineering — Administrateur Réseau</div>
          <div class="card-desc" style="margin-top:0.8rem;margin-bottom:1rem;">
            Ce stage m'a permis de découvrir a quoi ressemble une infrastructure réseaux. J'ai pus la faire en grande partie grace a mon maitre de stage qui m'éguillait.
          </div>
          <div style="padding:1rem;background:var(--surface2);border-radius:10px;margin-top:1rem;">
            <div style="font-size:0.75rem;color:var(--accent);font-weight:500;margin-bottom:0.5rem;">COMPÉTENCES CLÉS DÉVELOPPÉES</div>
            <div style="color:var(--muted);font-size:0.85rem;line-height:1.8;">
              ✓ Administration Windows Server (Active Directory, DNS, DHCP)<br>
              ✓ Configuration de routage inter-VLAN sur équipement Cisco<br>
            </div>
          </div>
          <div style="margin-top:1.4rem;display:flex;justify-content:flex-end;">
            <a class="btn btn-primary" style="font-size:0.82rem;padding:0.6rem 1.5rem;" href="rapport_stage_premier.pdf" target="_blank" >
              📄 Rapport de stage
            </a>
          </div>
        </div>

        <div class="card">
          <div class="card-label">Deuxième stage · Bilan</div>
          <div class="card-title">Les Tablier Solidaire — Développeur Fullstack</div>
          <div class="card-desc" style="margin-top:0.8rem;margin-bottom:1rem;">
            Stage axé sur le développement d'une application web de gestion interne en local. 
            J'ai dû analyser les besoins métier, concevoir la base de données (MCD), 
            et développer une solution complète (front, back, SQL) adaptée aux contraintes 
            d'une structure associative.
          </div>
          <div style="padding:1rem;background:var(--surface2);border-radius:10px;margin-top:1rem;">
            <div style="font-size:0.75rem;color:var(--accent);font-weight:500;margin-bottom:0.5rem;">COMPÉTENCES CLÉS DÉVELOPPÉES</div>
            <div style="color:var(--muted);font-size:0.85rem;line-height:1.8;">
              ✓ Conception et modélisation de base de données (MCD, SQL)<br>
              ✓ Développement back-end en PHP<br>
              ✓ Création d'interfaces web en HTML/CSS<br>
            </div>
          </div>
          <div style="margin-top:1.4rem;display:flex;justify-content:flex-end;">
            <a class="btn btn-primary" style="font-size:0.82rem;padding:0.6rem 1.5rem;" href="Rapport_de_stage.pdf" target="_blank" >
              📄 Rapport de stage
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</div>

<!-- ── PAGE PROJETS ── -->
<div class="page" id="page-projets">
  <section class="section">
    <div class="section-header">
      <div class="section-tag">Réalisations</div>
      <h1 class="section-title">Mes projets</h1>
      <p class="section-desc">Projets scolaires développés au fil de ma formation.</p>
    </div>

    <div class="cards-grid">
      <div class="card">
        <div class="card-label">Projet Scolaire - Bar à thème</div>
        <div class="card-title">Site web éphémère</div>
        <div class="card-desc">Site web full-stack permettant de pratiquer les notion vue en cours.</div>
        <div class="tags">
          <span class="tag">HTML</span>
          <span class="tag">CSS</span>
          <span class="tag">JavaScript</span>
          <span class="tag">PHP</span>
          <span class="tag">SQL</span>
        </div>
        <div class="card-meta">
          <span class="card-period">2024 - 2025</span>
        </div>
        <div style="margin-top:1.4rem;display:flex;justify-content:flex-end;">
            <a class="btn btn-primary" style="font-size:0.82rem;padding:0.6rem 1.5rem;" href="Projet_bar_compte_rendue.pdf" target="_blank" >
              📄 Compte rendue Bar à thème
            </a>
          </div>
      </div>

      <div class="card">
        <div class="card-label">Projet Scolaire - Android Studio</div>
        <div class="card-title">GSB</div>
        <div class="card-desc">Application mobile pour la gestion des visiteurs médicaux.</div>
        <div class="tags">
          <span class="tag">Java</span>
          <span class="tag">SQLite</span>
          <span class="tag">XML</span>
        </div>
        <div class="card-meta">
          <span class="card-period">2025</span>
        </div>
        <div style="margin-top:1.4rem;display:flex;justify-content:flex-end;">
            <a class="btn btn-primary" style="font-size:0.82rem;padding:0.6rem 1.5rem;" href="Projet_Android_Studio_compte_rendue.pdf" target="_blank" >
              📄 Compte rendue Androide Studio
            </a>
          </div>
      </div>

      <div class="card">
        <div class="card-label">Projet Scolaire - PHP</div>
        <div class="card-title">API REST — MVC</div>
        <div class="card-desc">Conception et développement d'une API REST complète pour </div>
        <div class="tags">
          <span class="tag">Python</span>
          <span class="tag">FastAPI</span>
          <span class="tag">SQLite</span>
        </div>
        <div class="card-meta">
          <span class="card-period">2023</span>
          <span class="tag">Terminé</span>
        </div>
        <div style="margin-top:1.4rem;display:flex;justify-content:flex-end;">
            <a class="btn btn-primary" style="font-size:0.82rem;padding:0.6rem 1.5rem;" href="Projet_PHP_compte_rendue.pdf" target="_blank" >
              📄 Compte rendue PHP
            </a>
          </div>
      </div>


      <div class="card" style="border-style:dashed;border-color:rgba(255,255,255,0.12);display:flex;align-items:center;justify-content:center;flex-direction:column;text-align:center;min-height:200px;cursor:default;">
        <div style="font-size:2rem;margin-bottom:0.5rem;opacity:0.3;">+</div>
        <div style="color:var(--muted);font-size:0.85rem;">Projet à venir</div>
      </div>
    </div>
  </section>
</div>


<!-- ── PAGE STAGES ── -->
<div class="page" id="page-CV">
  <section class="section">
    <div class="section-header">
      <h1 class="section-title">Mon CV</h1>
      <p class="section-desc">Un aperçu de mon parcours académique, mes compétences et mes expériences professionnelles.</p>
    </div>

    <div style="padding:2rem;background:var(--surface);border:1px solid var(--border);border-radius:16px;">
      <a class="btn btn-primary" href="CV.pdf" target="_blank">
        📄 Mon CV
      </a>
    </div>
  </section>
</body>
</html>
