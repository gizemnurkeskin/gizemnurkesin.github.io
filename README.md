# gizemnurkesin.github.io
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Gizem Nur Keskin — Performance Marketing Specialist</title>
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet" />
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --white:   #FAFAF8;
    --ink:     #1A1A18;
    --mid:     #6B6B66;
    --light:   #E8E8E4;
    --accent:  #2D6A4F;
    --accent2: #B7D4C8;
    --serif: 'DM Serif Display', Georgia, serif;
    --sans:  'DM Sans', system-ui, sans-serif;
  }

  html { scroll-behavior: smooth; }

  body {
    background: var(--white);
    color: var(--ink);
    font-family: var(--sans);
    font-weight: 300;
    line-height: 1.65;
    font-size: 16px;
  }

  /* ── NAV ─────────────────────────────────── */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    display: flex; justify-content: space-between; align-items: center;
    padding: 1.25rem 4vw;
    background: var(--white);
    border-bottom: 1px solid var(--light);
  }
  .nav-name {
    font-family: var(--serif);
    font-size: 1.05rem;
    letter-spacing: .01em;
  }
  .nav-right { display: flex; align-items: center; gap: 2rem; }
  .nav-links { display: flex; gap: 2rem; }
  .nav-links a {
    font-size: .85rem;
    font-weight: 400;
    letter-spacing: .06em;
    text-transform: uppercase;
    color: var(--mid);
    text-decoration: none;
    transition: color .2s;
  }
  .nav-links a:hover { color: var(--accent); }

  /* ── LANG TOGGLE ─────────────────────────── */
  .lang-toggle {
    display: flex;
    border: 1px solid var(--light);
    overflow: hidden;
  }
  .lang-btn {
    padding: .35rem .7rem;
    font-size: .75rem;
    font-weight: 500;
    letter-spacing: .08em;
    text-transform: uppercase;
    background: none;
    border: none;
    cursor: pointer;
    color: var(--mid);
    transition: background .15s, color .15s;
    font-family: var(--sans);
  }
  .lang-btn.active {
    background: var(--accent);
    color: #fff;
  }
  .lang-btn:not(.active):hover { background: var(--light); }

  /* ── HERO ────────────────────────────────── */
  .hero {
    min-height: 100vh;
    display: flex; flex-direction: column; justify-content: flex-end;
    padding: 8rem 4vw 5rem;
    border-bottom: 1px solid var(--light);
    position: relative;
    overflow: hidden;
  }
  .hero::before {
    content: '';
    position: absolute; inset: 0;
    background-image:
      linear-gradient(var(--light) 1px, transparent 1px),
      linear-gradient(90deg, var(--light) 1px, transparent 1px);
    background-size: 48px 48px;
    opacity: .55;
    animation: grid-shift 30s linear infinite;
  }
  @keyframes grid-shift {
    from { background-position: 0 0, 0 0; }
    to   { background-position: 48px 48px, 48px 48px; }
  }
  .hero-content { position: relative; max-width: 860px; }
  .hero-eyebrow {
    font-size: .8rem;
    font-weight: 500;
    letter-spacing: .14em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 1.2rem;
  }
  .hero h1 {
    font-family: var(--serif);
    font-size: clamp(2.8rem, 7vw, 5.5rem);
    line-height: 1.08;
    letter-spacing: -.01em;
    margin-bottom: 1.6rem;
  }
  .hero h1 em { font-style: italic; color: var(--accent); }
  .hero-sub {
    font-size: 1.1rem;
    color: var(--mid);
    max-width: 540px;
    line-height: 1.7;
    margin-bottom: 2.4rem;
  }
  .hero-cta {
    display: inline-block;
    padding: .75rem 2rem;
    background: var(--accent);
    color: #fff;
    text-decoration: none;
    font-size: .85rem;
    font-weight: 500;
    letter-spacing: .06em;
    text-transform: uppercase;
    transition: background .2s;
  }
  .hero-cta:hover { background: #1e4d38; }

  /* ── SECTIONS ────────────────────────────── */
  section { padding: 5rem 4vw; border-bottom: 1px solid var(--light); }
  .section-inner { max-width: 900px; margin: 0 auto; }
  .section-label {
    font-size: .75rem;
    letter-spacing: .14em;
    text-transform: uppercase;
    color: var(--accent);
    font-weight: 500;
    margin-bottom: 2.5rem;
  }
  h2 {
    font-family: var(--serif);
    font-size: clamp(1.8rem, 4vw, 2.8rem);
    line-height: 1.2;
    margin-bottom: 1.6rem;
  }

  /* ── ABOUT ───────────────────────────────── */
  .about-grid {
    display: grid;
    grid-template-columns: 3fr 2fr;
    gap: 4rem;
    align-items: start;
  }
  .about-text p { color: var(--mid); margin-bottom: 1rem; }
  .about-stats { display: flex; flex-direction: column; gap: 1.5rem; }
  .stat { border-left: 2px solid var(--accent2); padding-left: 1rem; }
  .stat-number { font-family: var(--serif); font-size: 2.2rem; color: var(--accent); line-height: 1; }
  .stat-label { font-size: .8rem; color: var(--mid); margin-top: .2rem; }

  /* ── SKILLS ──────────────────────────────── */
  .skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    gap: .6rem;
  }
  .skill-tag {
    padding: .6rem 1rem;
    border: 1px solid var(--light);
    font-size: .82rem;
    color: var(--mid);
    background: #fff;
    transition: border-color .2s, color .2s;
    cursor: default;
  }
  .skill-tag:hover { border-color: var(--accent); color: var(--accent); }

  /* ── EXPERIENCE ──────────────────────────── */
  .timeline { display: flex; flex-direction: column; gap: 0; }
  .job {
    display: grid;
    grid-template-columns: 200px 1fr;
    gap: 2rem;
    padding: 2rem 0;
    border-top: 1px solid var(--light);
  }
  .job:last-child { border-bottom: 1px solid var(--light); }
  .job-meta { padding-top: .15rem; }
  .job-company { font-weight: 500; font-size: .9rem; color: var(--ink); }
  .job-dates { font-size: .78rem; color: var(--mid); margin-top: .25rem; }
  .job-title { font-family: var(--serif); font-size: 1.15rem; margin-bottom: .75rem; }
  .job ul { list-style: none; display: flex; flex-direction: column; gap: .5rem; }
  .job ul li { font-size: .9rem; color: var(--mid); padding-left: 1rem; position: relative; }
  .job ul li::before { content: '→'; position: absolute; left: 0; color: var(--accent); font-size: .8rem; }

  /* ── CONTACT ─────────────────────────────── */
  .contact-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 3rem; align-items: start; }
  .contact-line { display: flex; align-items: center; gap: .75rem; margin-bottom: 1rem; }
  .contact-line a { color: var(--mid); text-decoration: none; font-size: .95rem; transition: color .2s; }
  .contact-line a:hover { color: var(--accent); }
  .contact-dot { width: 6px; height: 6px; background: var(--accent); border-radius: 50%; flex-shrink: 0; }
  .edu-block { margin-top: 1rem; }
  .edu-block .school { font-family: var(--serif); font-size: 1.1rem; margin-bottom: .25rem; }
  .edu-block .degree { font-size: .9rem; color: var(--mid); }
  .edu-block .year   { font-size: .8rem; color: var(--mid); margin-top: .2rem; }

  /* ── FOOTER ──────────────────────────────── */
  footer { padding: 2rem 4vw; display: flex; justify-content: space-between; font-size: .78rem; color: var(--mid); }

  /* ── RESPONSIVE ──────────────────────────── */
  @media (max-width: 700px) {
    .nav-links { display: none; }
    .about-grid, .contact-grid { grid-template-columns: 1fr; gap: 2rem; }
    .job { grid-template-columns: 1fr; gap: .5rem; }
    .job-meta { padding-top: 0; }
  }

  @media (prefers-reduced-motion: reduce) {
    .hero::before { animation: none; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <span class="nav-name">Gizem Nur Keskin</span>
  <div class="nav-right">
    <div class="nav-links">
      <a href="#about"      data-en="About"      data-tr="Hakkımda">About</a>
      <a href="#skills"     data-en="Skills"     data-tr="Yetkinlikler">Skills</a>
      <a href="#experience" data-en="Experience" data-tr="Deneyim">Experience</a>
      <a href="#contact"    data-en="Contact"    data-tr="İletişim">Contact</a>
    </div>
    <div class="lang-toggle">
      <button class="lang-btn active" onclick="setLang('en')">EN</button>
      <button class="lang-btn"        onclick="setLang('tr')">TR</button>
    </div>
  </div>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-content">
    <p class="hero-eyebrow" data-en="Performance Marketing &amp; User Acquisition" data-tr="Performans Pazarlama &amp; Kullanıcı Kazanımı">Performance Marketing &amp; User Acquisition</p>
    <h1 data-en="Turning <em>data</em><br>into growth." data-tr="<em>Veriyi</em><br>büyümeye dönüştürüyorum.">Turning <em>data</em><br>into growth.</h1>
    <p class="hero-sub" data-en="4+ years driving customer acquisition and demand generation across B2B and B2C markets — through paid media, structured experimentation, and creative strategy." data-tr="B2B ve B2C pazarlarında 4+ yıldır müşteri kazanımı ve talep oluşturma süreçlerini yönetiyorum — ücretli medya, yapılandırılmış deneyler ve yaratıcı strateji aracılığıyla.">4+ years driving customer acquisition and demand generation across B2B and B2C markets — through paid media, structured experimentation, and creative strategy.</p>
    <a class="hero-cta" href="#contact" data-en="Get in touch" data-tr="İletişime geç">Get in touch</a>
  </div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="section-inner">
    <p class="section-label" data-en="About" data-tr="Hakkımda">About</p>
    <div class="about-grid">
      <div class="about-text">
        <h2 data-en="Performance marketer with a creative edge." data-tr="Yaratıcı bir bakış açısıyla performans pazarlamacısı.">Performance marketer with a creative edge.</h2>
        <p data-en="I specialise in paid media strategy across Meta, Google, LinkedIn, and Microsoft Ads — combining rigorous campaign experimentation with creative thinking to acquire high-quality users at scale." data-tr="Meta, Google, LinkedIn ve Microsoft Ads platformlarında ücretli medya stratejisi konusunda uzmanlaşıyorum; titiz kampanya deneyleri ile yaratıcı düşünceyi bir araya getirerek büyük ölçekte yüksek kaliteli kullanıcılar kazanıyorum.">I specialise in paid media strategy across Meta, Google, LinkedIn, and Microsoft Ads — combining rigorous campaign experimentation with creative thinking to acquire high-quality users at scale.</p>
        <p data-en="Beyond the dashboards, I've built a personal brand of 20K+ followers from scratch, which keeps my instincts for storytelling and organic growth sharp. I bring that creator perspective directly into how I brief, test, and iterate on paid creative." data-tr="Dashboard'ların ötesinde, sıfırdan 20.000'den fazla takipçiyle bir kişisel marka inşa ettim; bu deneyim hikaye anlatımı ve organik büyüme içgüdülerimi canlı tutuyor. Bu yaratıcı bakış açısını doğrudan ücretli kreatif briefing, test ve iterasyon süreçlerime yansıtıyorum.">Beyond the dashboards, I've built a personal brand of 20K+ followers from scratch, which keeps my instincts for storytelling and organic growth sharp. I bring that creator perspective directly into how I brief, test, and iterate on paid creative.</p>
        <p data-en="Based in Ankara, open to remote and global opportunities." data-tr="Ankara'da yaşıyorum, uzaktan ve global fırsatlara açığım.">Based in Ankara, open to remote and global opportunities.</p>
      </div>
      <div class="about-stats">
        <div class="stat">
          <div class="stat-number">4+</div>
          <div class="stat-label" data-en="Years in performance marketing" data-tr="Yıl performans pazarlama deneyimi">Years in performance marketing</div>
        </div>
        <div class="stat">
          <div class="stat-number">20K+</div>
          <div class="stat-label" data-en="Instagram followers built organically" data-tr="Organik büyütülen Instagram takipçisi">Instagram followers built organically</div>
        </div>
        <div class="stat">
          <div class="stat-number">4</div>
          <div class="stat-label" data-en="Paid channels managed (Meta, Google, LinkedIn, Microsoft)" data-tr="Yönetilen ücretli kanal (Meta, Google, LinkedIn, Microsoft)">Paid channels managed (Meta, Google, LinkedIn, Microsoft)</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- SKILLS -->
<section id="skills">
  <div class="section-inner">
    <p class="section-label" data-en="Core Competencies" data-tr="Temel Yetkinlikler">Core Competencies</p>
    <h2 data-en="What I bring to the table." data-tr="Masaya ne getiriyorum.">What I bring to the table.</h2>
    <div class="skills-grid">
      <div class="skill-tag" data-en="Paid Social &amp; Search" data-tr="Ücretli Sosyal &amp; Arama">Paid Social &amp; Search</div>
      <div class="skill-tag" data-en="User Acquisition" data-tr="Kullanıcı Kazanımı">User Acquisition</div>
      <div class="skill-tag" data-en="Demand Generation" data-tr="Talep Oluşturma">Demand Generation</div>
      <div class="skill-tag" data-en="Growth Marketing" data-tr="Büyüme Pazarlaması">Growth Marketing</div>
      <div class="skill-tag" data-en="Conversion Rate Optimisation" data-tr="Dönüşüm Oranı Optimizasyonu">Conversion Rate Optimisation</div>
      <div class="skill-tag" data-en="A/B Testing" data-tr="A/B Testi">A/B Testing</div>
      <div class="skill-tag" data-en="Funnel Analysis" data-tr="Huni Analizi">Funnel Analysis</div>
      <div class="skill-tag" data-en="Audience Development" data-tr="Kitle Geliştirme">Audience Development</div>
      <div class="skill-tag" data-en="Retargeting &amp; Remarketing" data-tr="Yeniden Hedefleme">Retargeting &amp; Remarketing</div>
      <div class="skill-tag" data-en="Campaign Scaling" data-tr="Kampanya Ölçeklendirme">Campaign Scaling</div>
      <div class="skill-tag" data-en="Performance Reporting" data-tr="Performans Raporlama">Performance Reporting</div>
      <div class="skill-tag" data-en="Creative Strategy" data-tr="Kreatif Strateji">Creative Strategy</div>
      <div class="skill-tag">Meta Ads</div>
      <div class="skill-tag">Google Ads</div>
      <div class="skill-tag">LinkedIn Ads</div>
      <div class="skill-tag">Microsoft Ads</div>
      <div class="skill-tag">SEO</div>
      <div class="skill-tag" data-en="AI-Assisted Workflows" data-tr="Yapay Zeka Destekli İş Akışları">AI-Assisted Workflows</div>
    </div>
  </div>
</section>

<!-- EXPERIENCE -->
<section id="experience">
  <div class="section-inner">
    <p class="section-label" data-en="Experience" data-tr="Deneyim">Experience</p>
    <h2 data-en="Where I've worked." data-tr="Çalıştığım yerler.">Where I've worked.</h2>
    <div class="timeline">

      <div class="job">
        <div class="job-meta">
          <div class="job-company">JotForm</div>
          <div class="job-dates" data-en="Jul 2024 – Present" data-tr="Tem 2024 – Günümüz">Jul 2024 – Present</div>
        </div>
        <div>
          <div class="job-title" data-en="Paid Acquisition Specialist" data-tr="Ücretli Kazanım Uzmanı">Paid Acquisition Specialist</div>
          <ul>
            <li data-en="Own paid acquisition across Google, Microsoft, LinkedIn, and Meta — aligned with pipeline growth and demand generation goals." data-tr="Google, Microsoft, LinkedIn ve Meta'da ücretli kazanım süreçlerini yönetiyorum; stratejiyi pipeline büyümesi ve talep oluşturma hedefleriyle hizalıyorum.">Own paid acquisition across Google, Microsoft, LinkedIn, and Meta — aligned with pipeline growth and demand generation goals.</li>
            <li data-en="Design and execute structured experimentation across creatives, audiences, and landing pages to improve acquisition efficiency and lead quality." data-tr="Kazanım verimliliğini ve potansiyel müşteri kalitesini artırmak için kreatifler, kitleler ve açılış sayfaları üzerinde yapılandırılmış deneyler tasarlıyor ve yürütüyorum.">Design and execute structured experimentation across creatives, audiences, and landing pages to improve acquisition efficiency and lead quality.</li>
            <li data-en="Leverage AI tools (ChatGPT, Claude, Perplexity) to accelerate hypothesis generation, creative briefing, and reporting." data-tr="Hipotez oluşturma, kreatif briefing ve raporlama süreçlerini hızlandırmak için yapay zeka araçlarından (ChatGPT, Claude, Perplexity) yararlanıyorum.">Leverage AI tools (ChatGPT, Claude, Perplexity) to accelerate hypothesis generation, creative briefing, and reporting.</li>
            <li data-en="Collaborate with sales, content, and marketing teams to keep acquisition strategy tightly aligned to business objectives." data-tr="Kazanım stratejisini iş hedefleriyle uyumlu tutmak için satış, içerik ve pazarlama ekipleriyle işbirliği yapıyorum.">Collaborate with sales, content, and marketing teams to keep acquisition strategy tightly aligned to business objectives.</li>
          </ul>
        </div>
      </div>

      <div class="job">
        <div class="job-meta">
          <div class="job-company">Uniqgene</div>
          <div class="job-dates" data-en="Oct 2022 – May 2024" data-tr="Eki 2022 – May 2024">Oct 2022 – May 2024</div>
        </div>
        <div>
          <div class="job-title" data-en="Digital Marketing Specialist" data-tr="Dijital Pazarlama Uzmanı">Digital Marketing Specialist</div>
          <ul>
            <li data-en="Led paid acquisition across B2B and B2C audiences with a strong focus on Meta advertising." data-tr="Meta reklamcılığına güçlü bir odakla B2B ve B2C kitleleri için ücretli kazanım süreçlerini yönettim.">Led paid acquisition across B2B and B2C audiences with a strong focus on Meta advertising.</li>
            <li data-en="Partnered with creative teams to develop performance-focused messaging and content strategies." data-tr="Performansa odaklı mesajlaşma ve içerik stratejileri geliştirmek için kreatif ekiplerle iş birliği yaptım.">Partnered with creative teams to develop performance-focused messaging and content strategies.</li>
            <li data-en="Conducted audience research and campaign analysis to sharpen targeting and lift conversion outcomes." data-tr="Hedeflemeyi keskinleştirmek ve dönüşüm sonuçlarını iyileştirmek için kitle araştırması ve kampanya analizi yürüttüm.">Conducted audience research and campaign analysis to sharpen targeting and lift conversion outcomes.</li>
          </ul>
        </div>
      </div>

      <div class="job">
        <div class="job-meta">
          <div class="job-company">Beforesunset AI</div>
          <div class="job-dates" data-en="Mar 2022 – Jun 2023" data-tr="Mar 2022 – Haz 2023">Mar 2022 – Jun 2023</div>
        </div>
        <div>
          <div class="job-title" data-en="Digital Marketing Specialist" data-tr="Dijital Pazarlama Uzmanı">Digital Marketing Specialist</div>
          <ul>
            <li data-en="Spearheaded SEO initiatives to improve organic visibility, traffic acquisition, and lead generation." data-tr="Organik görünürlüğü, trafik kazanımını ve potansiyel müşteri oluşturmayı iyileştirmek için SEO girişimlerine öncülük ettim.">Spearheaded SEO initiatives to improve organic visibility, traffic acquisition, and lead generation.</li>
            <li data-en="Supported growth marketing through content strategy, social media, and performance reporting." data-tr="İçerik stratejisi, sosyal medya ve performans raporlamasıyla büyüme pazarlamasını destekledim.">Supported growth marketing through content strategy, social media, and performance reporting.</li>
          </ul>
        </div>
      </div>

      <div class="job">
        <div class="job-meta">
          <div class="job-company">@nk.gizem (Instagram)</div>
          <div class="job-dates" data-en="Jul 2021 – Present" data-tr="Tem 2021 – Günümüz">Jul 2021 – Present</div>
        </div>
        <div>
          <div class="job-title" data-en="Content Creator &amp; Community Builder" data-tr="İçerik Üreticisi &amp; Topluluk Oluşturucu">Content Creator &amp; Community Builder</div>
          <ul>
            <li data-en="Built and scaled a personal brand around productivity, fitness, and self-development — growing an engaged audience of 20,000+ followers." data-tr="Verimlilik, fitness ve kişisel gelişim etrafında bir kişisel marka kurdum ve büyüttüm; 20.000'den fazla takipçiyle ilgili bir kitle oluşturdum.">Built and scaled a personal brand around productivity, fitness, and self-development — growing an engaged audience of 20,000+ followers.</li>
            <li data-en="Developed hands-on expertise in creative testing, storytelling, audience engagement, and organic growth." data-tr="Kreatif test, hikaye anlatımı, kitle etkileşimi ve organik büyüme konularında uygulamalı uzmanlık geliştirdim.">Developed hands-on expertise in creative testing, storytelling, audience engagement, and organic growth.</li>
          </ul>
        </div>
      </div>

    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="section-inner">
    <p class="section-label" data-en="Contact &amp; Education" data-tr="İletişim &amp; Eğitim">Contact &amp; Education</p>
    <div class="contact-grid">
      <div>
        <h2 data-en="Let's work together." data-tr="Birlikte çalışalım.">Let's work together.</h2>
        <div class="contact-line">
          <span class="contact-dot"></span>
          <a href="mailto:gizeemnurk@gmail.com">gizeemnurk@gmail.com</a>
        </div>
        <div class="contact-line">
          <span class="contact-dot"></span>
          <a href="tel:+905418633468">+90 541 863 3468</a>
        </div>
        <div class="contact-line">
          <span class="contact-dot"></span>
          <a href="https://instagram.com/nk.gizem" target="_blank" rel="noopener">@nk.gizem on Instagram</a>
        </div>
        <div class="contact-line">
          <span class="contact-dot"></span>
          <span style="color:var(--mid);font-size:.95rem;">Ankara, Türkiye</span>
        </div>
      </div>
      <div>
        <h2 style="font-size:1.4rem;" data-en="Education" data-tr="Eğitim">Education</h2>
        <div class="edu-block">
          <div class="school" data-en="Hacettepe University" data-tr="Hacettepe Üniversitesi">Hacettepe University</div>
          <div class="degree" data-en="B.A. English Language and Literature" data-tr="İngiliz Dili ve Edebiyatı Lisans">B.A. English Language and Literature</div>
          <div class="year">2018 – 2022</div>
        </div>
      </div>
    </div>
  </div>
</section>

<footer>
  <span>© 2026 Gizem Nur Keskin</span>
  <span data-en="Performance Marketing Specialist · Ankara, Türkiye" data-tr="Performans Pazarlama Uzmanı · Ankara, Türkiye">Performance Marketing Specialist · Ankara, Türkiye</span>
</footer>

<script>
  let currentLang = 'en';

  function setLang(lang) {
    currentLang = lang;

    // Update button states
    document.querySelectorAll('.lang-btn').forEach(btn => {
      btn.classList.toggle('active', btn.textContent.trim().toLowerCase() === lang);
    });

    // Update html lang attribute
    document.documentElement.lang = lang;

    // Update all elements with data-en / data-tr
    document.querySelectorAll('[data-en][data-tr]').forEach(el => {
      const text = el.getAttribute('data-' + lang);
      if (text !== null) {
        // Use innerHTML so tags like <em> and <br> render correctly
        el.innerHTML = text;
      }
    });

    // Update page title
    document.title = lang === 'tr'
      ? 'Gizem Nur Keskin — Performans Pazarlama Uzmanı'
      : 'Gizem Nur Keskin — Performance Marketing Specialist';
  }
</script>

</body>
</html>
