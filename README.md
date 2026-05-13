<html lang="sq">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Shqiperia e Mesme</title>
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400&family=Jost:wght@300;400;500;600&display=swap" rel="stylesheet"/>
  <style>
    :root {
      --cream: #f8f4ef;
      --warm-white: #fdfbf8;
      --charcoal: #1c1c1c;
      --muted: #6b6560;
      --accent: #8b3a3a;
      --accent-light: #c17070;
      --accent-pale: #f0e4e4;
      --gold: #b5924c;
      --gold-light: #e8d5b0;
      --border: #e2d9d0;
    }

    * { margin: 0; padding: 0; box-sizing: border-box; }

    body {
      font-family: 'Jost', sans-serif;
      background: var(--cream);
      color: var(--charcoal);
    }

    /* ── HEADER ── */
    header {
      background: var(--charcoal);
      color: var(--cream);
      text-align: center;
      padding: 64px 24px 52px;
      position: relative;
      overflow: hidden;
    }

    header::before {
      content: '';
      position: absolute;
      inset: 0;
      background: repeating-linear-gradient(
        -45deg,
        transparent,
        transparent 40px,
        rgba(255,255,255,0.015) 40px,
        rgba(255,255,255,0.015) 80px
      );
    }

    .flag-line {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 18px;
      margin-bottom: 20px;
    }

    .flag-line .rule {
      height: 1px;
      width: 60px;
      background: var(--gold);
      opacity: 0.6;
    }

    .flag-emoji { font-size: 2rem; }

    header h1 {
      font-family: 'Cormorant Garamond', serif;
      font-size: 3.2rem;
      font-weight: 300;
      letter-spacing: 4px;
      text-transform: uppercase;
      line-height: 1.1;
      position: relative;
    }

    header p {
      font-size: 0.78rem;
      font-weight: 500;
      letter-spacing: 3px;
      text-transform: uppercase;
      color: var(--gold-light);
      margin-top: 14px;
      position: relative;
    }

    /* ── NAV ── */
    nav {
      background: var(--warm-white);
      border-bottom: 1px solid var(--border);
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 0;
      padding: 0 10px;
    }

    nav a {
      color: var(--muted);
      text-decoration: none;
      font-size: 0.7rem;
      font-weight: 500;
      letter-spacing: 2px;
      text-transform: uppercase;
      padding: 14px 18px;
      border-bottom: 2px solid transparent;
      transition: color 0.2s, border-color 0.2s;
    }

    nav a:hover {
      color: var(--accent);
      border-bottom-color: var(--accent);
    }

    /* ── LAYOUT ── */
    .container { max-width: 900px; margin: 0 auto; padding: 48px 20px; }

    .section {
      background: var(--warm-white);
      border-radius: 2px;
      margin-bottom: 28px;
      padding: 40px 44px;
      border: 1px solid var(--border);
      position: relative;
    }

    .section::before {
      content: '';
      position: absolute;
      left: 0; top: 24px; bottom: 24px;
      width: 2px;
      background: linear-gradient(to bottom, var(--gold), var(--accent));
      border-radius: 0 2px 2px 0;
    }

    .section h2 {
      font-family: 'Cormorant Garamond', serif;
      font-size: 1.75rem;
      font-weight: 400;
      color: var(--charcoal);
      margin-bottom: 6px;
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .section-sub {
      font-size: 0.68rem;
      letter-spacing: 2.5px;
      text-transform: uppercase;
      color: var(--gold);
      font-weight: 600;
      margin-bottom: 22px;
      display: block;
    }

    .section p {
      font-size: 0.9rem;
      line-height: 1.9;
      color: #444;
      margin-bottom: 10px;
    }

    .section p:last-child { margin-bottom: 0; }

    /* ── STATS ── */
    .stats-row {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-top: 24px;
    }

    .stat-box {
      background: var(--cream);
      border: 1px solid var(--border);
      border-radius: 2px;
      padding: 16px 20px;
      text-align: center;
      flex: 1;
      min-width: 100px;
    }

    .stat-box .num {
      font-family: 'Cormorant Garamond', serif;
      font-size: 1.9rem;
      font-weight: 400;
      color: var(--accent);
      display: block;
      line-height: 1;
    }

    .stat-box .lbl {
      font-size: 0.65rem;
      letter-spacing: 1.5px;
      text-transform: uppercase;
      color: var(--muted);
      display: block;
      margin-top: 6px;
    }

    /* ── TIMELINE ── */
    .timeline { margin-top: 18px; }

    .t-item {
      display: flex;
      gap: 20px;
      margin-bottom: 26px;
      align-items: flex-start;
    }

    .t-year {
      background: transparent;
      color: var(--accent);
      font-size: 0.65rem;
      font-weight: 600;
      letter-spacing: 1.5px;
      text-transform: uppercase;
      padding: 5px 0;
      white-space: nowrap;
      min-width: 100px;
      text-align: right;
      border-right: 1px solid var(--gold-light);
      padding-right: 18px;
      margin-top: 2px;
    }

    .t-content { padding-left: 4px; }
    .t-content h4 {
      font-family: 'Cormorant Garamond', serif;
      font-size: 1.05rem;
      font-weight: 600;
      margin-bottom: 4px;
      color: var(--charcoal);
    }

    .t-content p {
      font-size: 0.83rem;
      color: var(--muted);
      line-height: 1.75;
      margin: 0;
    }

    /* ── CARDS ── */
    .cards-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(230px, 1fr));
      gap: 12px;
      margin-top: 20px;
    }

    .card {
      background: var(--cream);
      border: 1px solid var(--border);
      border-radius: 2px;
      padding: 20px;
      transition: border-color 0.25s, background 0.25s;
    }

    .card:hover {
      border-color: var(--gold);
      background: #fdf9f3;
    }

    .card-icon { font-size: 1.5rem; display: block; margin-bottom: 10px; }

    .card h3 {
      font-family: 'Cormorant Garamond', serif;
      font-size: 1.15rem;
      font-weight: 600;
      color: var(--charcoal);
      margin-bottom: 4px;
    }

    .card .badge {
      display: inline-block;
      font-size: 0.6rem;
      letter-spacing: 1.5px;
      text-transform: uppercase;
      color: var(--gold);
      border: 1px solid var(--gold-light);
      border-radius: 1px;
      padding: 2px 8px;
      font-weight: 600;
      margin-bottom: 10px;
    }

    .card p { font-size: 0.8rem; color: var(--muted); line-height: 1.7; margin: 0; }

    /* ── PLACE LIST ── */
    .place-list { list-style: none; margin-top: 14px; }

    .place-list li {
      display: flex;
      gap: 16px;
      align-items: flex-start;
      padding: 16px 0;
      border-bottom: 1px solid var(--border);
    }

    .place-list li:last-child { border-bottom: none; }
    .place-icon { font-size: 1.3rem; flex-shrink: 0; margin-top: 2px; }

    .place-list h4 {
      font-family: 'Cormorant Garamond', serif;
      font-size: 1.05rem;
      font-weight: 600;
      color: var(--charcoal);
      margin-bottom: 4px;
    }

    .place-list p { font-size: 0.81rem; color: var(--muted); margin: 0; line-height: 1.7; }

    /* ── TWO COL ── */
    .two-col {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 12px;
      margin-top: 18px;
    }

    .info-block {
      background: var(--cream);
      border: 1px solid var(--border);
      border-radius: 2px;
      padding: 16px 18px;
    }

    .info-block h4 {
      font-size: 0.68rem;
      letter-spacing: 2px;
      text-transform: uppercase;
      color: var(--gold);
      font-weight: 600;
      margin-bottom: 8px;
    }

    .info-block p { font-size: 0.81rem; color: var(--muted); line-height: 1.7; margin: 0; }

    /* ── PILLARS ── */
    .pillars {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(170px, 1fr));
      gap: 10px;
      margin-top: 20px;
    }

    .pillar {
      background: var(--cream);
      border: 1px solid var(--border);
      border-radius: 2px;
      padding: 18px 14px;
      text-align: center;
      transition: border-color 0.2s;
    }

    .pillar:hover { border-color: var(--gold); }
    .pillar .p-icon { font-size: 1.7rem; display: block; margin-bottom: 10px; }

    .pillar h4 {
      font-family: 'Cormorant Garamond', serif;
      font-size: 1rem;
      font-weight: 600;
      color: var(--charcoal);
      margin-bottom: 6px;
    }

    .pillar p { font-size: 0.76rem; color: var(--muted); line-height: 1.65; }

    /* ── POP BARS ── */
    .pop-bars { margin-top: 20px; display: flex; flex-direction: column; gap: 12px; }

    .pop-row { display: flex; align-items: center; gap: 12px; }

    .pop-city {
      width: 74px;
      font-size: 0.73rem;
      letter-spacing: 1px;
      text-transform: uppercase;
      font-weight: 600;
      color: var(--muted);
      flex-shrink: 0;
    }

    .pop-track {
      flex: 1;
      height: 3px;
      background: var(--border);
      border-radius: 2px;
      overflow: visible;
      position: relative;
    }

    .pop-fill {
      height: 100%;
      background: linear-gradient(90deg, var(--gold), var(--accent));
      border-radius: 2px;
      width: 0;
      transition: width 1.2s cubic-bezier(0.25, 1, 0.5, 1);
      position: relative;
    }

    .pop-val {
      font-family: 'Cormorant Garamond', serif;
      font-size: 0.9rem;
      font-weight: 400;
      color: var(--accent);
      width: 50px;
      text-align: right;
      flex-shrink: 0;
    }

    /* ── QUOTE ── */
    .quote-box {
      background: var(--charcoal);
      color: var(--cream);
      border-radius: 2px;
      padding: 32px 36px;
      margin: 20px 0;
      position: relative;
      overflow: hidden;
    }

    .quote-box::before {
      content: '"';
      font-family: 'Cormorant Garamond', serif;
      font-size: 8rem;
      color: var(--gold);
      opacity: 0.15;
      position: absolute;
      top: -20px;
      left: 16px;
      line-height: 1;
    }

    .quote-box p {
      font-family: 'Cormorant Garamond', serif;
      font-size: 1.4rem;
      font-style: italic;
      font-weight: 300;
      line-height: 1.6;
      color: var(--cream) !important;
      margin: 0 !important;
      position: relative;
    }

    .quote-box span {
      display: block;
      font-family: 'Jost', sans-serif;
      font-style: normal;
      font-size: 0.65rem;
      letter-spacing: 2.5px;
      text-transform: uppercase;
      color: var(--gold-light);
      margin-top: 14px;
      position: relative;
    }

    /* ── FOOTER ── */
    footer {
      background: var(--charcoal);
      color: var(--muted);
      text-align: center;
      padding: 32px 20px;
      font-size: 0.72rem;
      letter-spacing: 1.5px;
      text-transform: uppercase;
    }

    footer strong { color: var(--gold-light); font-weight: 400; }

    /* ── RESPONSIVE ── */
    @media (max-width: 600px) {
      header h1 { font-size: 2.2rem; }
      .section { padding: 28px 24px; }
      .two-col { grid-template-columns: 1fr; }
      .t-item { flex-direction: column; gap: 8px; }
      .t-year { text-align: left; border-right: none; border-left: 2px solid var(--gold-light); padding-right: 0; padding-left: 12px; }
    }
  </style>
</head>
<body>

<header>
  <div class="flag-line">
    <span class="rule"></span>
    <span class="flag-emoji">🇦🇱</span>
    <span class="rule"></span>
  </div>
  <h1>Shqipëria e Mesme</h1>
  <p>Historia · Qytetet · Turizmi · Kultura</p>
</header>

<nav>
  <a href="#hyrje">Hyrje</a>
  <a href="#historia">Historia</a>
  <a href="#qytetet">Qytetet</a>
  <a href="#turizmi">Turizmi</a>
  <a href="#kultura">Kultura</a>
  <a href="#popullsia">Popullsia</a>
  <a href="#ekonomia">Ekonomia</a>
</nav>

<div class="container">

  <div class="section" id="hyrje">
    <h2>🏔️ Çfarë është Shqipëria e Mesme?</h2>
    <span class="section-sub">Rajoni Qendror</span>
    <p>Shqipëria e Mesme është rajoni qendror i vendit tonë dhe mund të thuhet se është "zemra" e Shqipërisë. Këtu gjendet kryeqyteti Tirana, porti i Durrësit, qyteti historik i Elbasanit dhe shumë vende tjera interesante.</p>
    <p>Gjeografikisht kufizohet me Shqipërinë Veriore në veri, Shqipërinë Jugore në jug, Adriatikun në perëndim dhe Maqedoninë e Veriut e Kosovën në lindje. Terreni varion nga fusha bregdetare deri te male të larta si Dajti.</p>
    <div class="stats-row">
      <div class="stat-box"><span class="num">~1.5M</span><span class="lbl">Banorë</span></div>
      <div class="stat-box"><span class="num">~5,000</span><span class="lbl">km² Sipërfaqe</span></div>
      <div class="stat-box"><span class="num">3</span><span class="lbl">Qarqe Kryesore</span></div>
      <div class="stat-box"><span class="num">11</span><span class="lbl">Bashki</span></div>
      <div class="stat-box"><span class="num">65%</span><span class="lbl">e GDP Kombëtare</span></div>
    </div>
  </div>

  <div class="section" id="historia">
    <h2>📜 Historia</h2>
    <span class="section-sub">Nga Ilirët deri sot</span>
    <p>Kjo zonë ka një histori shumë të gjatë dhe të pasur — nga ilirët e lashtë deri te shteti modern shqiptar.</p>
    <div class="timeline">
      <div class="t-item">
        <span class="t-year">Shek. IV p.Kr.</span>
        <div class="t-content">
          <h4>🛡️ Ilirët</h4>
          <p>Fisi i Taulantëve, ilirët më të fuqishëm, kishin qendrën kryesore aty ku sot është Durrësi. Linin pas fortifikime, varreza dhe sende artistike shumë të bukura.</p>
        </div>
      </div>
      <div class="t-item">
        <span class="t-year">229 p.Kr. – 395</span>
        <div class="t-content">
          <h4>🏛️ Romakët</h4>
          <p>Durrësi (Dyrrachium) u bë nyja e Via Egnatia — rruga romake që lidhte Romën me Konstantinopolin. Ndërtuan amfiteatra, rrugë dhe koloni të tëra.</p>
        </div>
      </div>
      <div class="t-item">
        <span class="t-year">Shek. IX – XIII</span>
        <div class="t-content">
          <h4>⚜️ Perandoria Bizantine</h4>
          <p>Zona kaloi nën sundimin bizantin. U formuan principata vendase si ajo e Muzakajve dhe Topiajve, duke i dhënë formë identitetit shqiptar.</p>
        </div>
      </div>
      <div class="t-item">
        <span class="t-year">1443 – 1468</span>
        <div class="t-content">
          <h4>⚔️ Gjergj Kastrioti Skënderbeu</h4>
          <p>Heroi ynë kombëtar! Mbajti Krujën dhe luftoi osmanët për 25 vjet. Beteja e Torviollit (1444) u bë legjendë ushtarake e të gjithë Europës. Pas tij, Shqipëria ra nën osmanët.</p>
        </div>
      </div>
      <div class="t-item">
        <span class="t-year">1468 – 1912</span>
        <div class="t-content">
          <h4>🕌 Periudha Osmane</h4>
          <p>500 vjet nën Perandorinë Osmane. Xhamitë, pazaret, hamamet dhe arkitektura osmane e kësaj kohe shihet ende sot nëpër qytetet tona.</p>
        </div>
      </div>
      <div class="t-item">
        <span class="t-year">28 Nëntor 1912</span>
        <div class="t-content">
          <h4>🚩 Pavarësia!</h4>
          <p>Ismail Qemali ngriti flamurin e kuq me shqiponjën dykrenare në Vlorë. Tirana u bë kryeqytet në 1920. Kjo është dita jonë më e shenjtë kombëtare!</p>
        </div>
      </div>
      <div class="t-item">
        <span class="t-year">1944 – 1990</span>
        <div class="t-content">
          <h4>🔒 Komunizmi</h4>
          <p>Shqipëria u mbyll plotësisht nga bota nën regjimin e Enver Hoxhës. U ndërtuan mbi 170,000 bunkerë nëpër vend. Pas rënies, filloi emigrimi masiv.</p>
        </div>
      </div>
      <div class="t-item">
        <span class="t-year">1990 – Sot</span>
        <div class="t-content">
          <h4>🌍 Shqipëria Moderne</h4>
          <p>Demokracia, ekonomia e tregut dhe integrimi europian. Tirana sot është ndër kryeqytetet më dinamike të Ballkanit dhe Shqipëria është kandidate zyrtare për BE.</p>
        </div>
      </div>
    </div>
  </div>

  <div class="section" id="qytetet">
    <h2>🏙️ Qytetet & Rajonet</h2>
    <span class="section-sub">Zemrat Urbane</span>
    <p>Shqipëria e Mesme ka disa qytete të rëndësishme, secili me karakterin e vet:</p>
    <div class="cards-grid">
      <div class="card">
        <span class="card-icon">🏛️</span>
        <h3>Tirana</h3>
        <span class="badge">Kryeqytet</span>
        <p>Qyteti më i madh i Shqipërisë me mbi 900,000 banorë. Sheshi Skënderbej, Bunkart, muzete, restaurantet dhe jeta e natës e bëjnë Tiranën qytetin ku dëshiron të jetosh.</p>
      </div>
      <div class="card">
        <span class="card-icon">⚓</span>
        <h3>Durrësi</h3>
        <span class="badge">Port Adriatik</span>
        <p>Qyteti i dytë i vendit. Amfiteatri romak 2000-vjeçar, plazhet e gjata dhe porti që të lidh me Italinë. Vera shqiptare fillon dhe mbaron këtu!</p>
      </div>
      <div class="card">
        <span class="card-icon">🏰</span>
        <h3>Elbasani</h3>
        <span class="badge">Qytet Historik</span>
        <p>I ndërtuar brenda mureve osmane të shekullit XV. Kalaja, xhamia e Mbretit dhe pazari i vjetër me rrugët e kalldrëmosura të çojnë direkt në mesjetë.</p>
      </div>
      <div class="card">
        <span class="card-icon">⚔️</span>
        <h3>Kruja</h3>
        <span class="badge">Kala Skënderbeu</span>
        <p>Qyteti-simbol i rezistencës shqiptare! Kalaja historike, Muzeu Kombëtar Skënderbeu dhe Tekke e Bektashive janë must-see absolute.</p>
      </div>
      <div class="card">
        <span class="card-icon">🌾</span>
        <h3>Kavaja</h3>
        <span class="badge">Bujqësi & Traditë</span>
        <p>E famshme për vajin e ullirit dhe pemët frutore. Kavaja ka tradita të pasura artizanale dhe festa tradicionale që ruhen me shumë dashuri.</p>
      </div>
      <div class="card">
        <span class="card-icon">🌊</span>
        <h3>Peqini</h3>
        <span class="badge">Lumi Shkumbin</span>
        <p>Ndahet nga lumi Shkumbin — kufiri historik mes dialektit gegë dhe toskë. Eko-turizmi dhe natyra e pastër e bëjnë të veçantë.</p>
      </div>
    </div>
  </div>

  <div class="section" id="turizmi">
    <h2>🗺️ Turizmi — Ku të shkosh?</h2>
    <span class="section-sub">Destinacionet e Zgjedhura</span>
    <p>Ka shumë vende të bukura për të vizituar në Shqipërinë e Mesme. Ja disa nga më të mirat:</p>
    <ul class="place-list">
      <li>
        <span class="place-icon">🏛️</span>
        <div>
          <h4>Amfiteatri Romak — Durrës</h4>
          <p>Amfiteatri më i madh i Ballkanit (shekulli II pas Kr.), me kapacitet 15,000 spektatorësh. Mozaikët e ruajtur brenda janë vërtet të mahnitshëm. Hyrja kushton pak dhe ia vlen çdo cent.</p>
        </div>
      </li>
      <li>
        <span class="place-icon">⚔️</span>
        <div>
          <h4>Kalaja e Krujës + Muzeu Skënderbeu</h4>
          <p>Kala mbi shkëmb ku Skënderbeu kundërvuri osmanët 25 vjet. Brenda ka muzeu dhe bazar të vjetër osmane. Pamja nga lart është spektakolare — mund të shihet deri Tirana.</p>
        </div>
      </li>
      <li>
        <span class="place-icon">🌿</span>
        <div>
          <h4>Mali i Dajtit + Teleferiku</h4>
          <p>Vetëm 25 km nga Tirana! Teleferiku të çon lart në 1613m. Pyje pishe, kafene me pamje gjigante mbi kryeqytet dhe ajër i pastër — perfekt për fundjavë.</p>
        </div>
      </li>
      <li>
        <span class="place-icon">🏖️</span>
        <div>
          <h4>Plazhet e Durrësit</h4>
          <p>30 km plazh adriatik. Me makinë 40 minuta nga Tirana dhe je te deti. Vera është super e nxehtë dhe çmimet janë akoma të arsyeshme.</p>
        </div>
      </li>
      <li>
        <span class="place-icon">🕌</span>
        <div>
          <h4>Et'hem Bej Xhamia — Tirana</h4>
          <p>Ndërtuar 1793, është mes pikave turistike kryesore të Tiranës. Pikturimi i mureve të brendshme me lule dhe pemë (jo figura njerëzore) është unik për arkitekturën osmane.</p>
        </div>
      </li>
      <li>
        <span class="place-icon">🏰</span>
        <div>
          <h4>Pazari i Vjetër — Elbasan</h4>
          <p>Brenda mureve osmane me rrugë kalldrëm dhe dyqane zejtarësh. Mund të blesh çizme lëkure, enë bakri dhe ëmbëlsira tradicionale. Shumë autentik!</p>
        </div>
      </li>
      <li>
        <span class="place-icon">🌄</span>
        <div>
          <h4>Kanioni i Erzenit</h4>
          <p>I fshehur midis Tiranës dhe Elbasanit — kanione të bukura me ujë të pastër. Ideal për ecje dhe piknik me familjen.</p>
        </div>
      </li>
      <li>
        <span class="place-icon">🏛️</span>
        <div>
          <h4>Muzeu Historik Kombëtar — Tirana</h4>
          <p>Muzeu me mozaikun e famshëm gjigant mbi fasadë. Brenda gjen çdo gjë nga epoka ilire deri te shpallja e pavarësisë. Hyrje me çmim simbolik.</p>
        </div>
      </li>
    </ul>
  </div>

  <div class="section" id="kultura">
    <h2>🎭 Kultura & Traditat</h2>
    <span class="section-sub">Shpirti i Vendit</span>
    <p>Shqipëria e Mesme ka një kulturë shumë të pasur — mix i traditave të vjetra dhe jetës moderne:</p>
    <div class="quote-box">
      <p>"Ku është shqiptari, atje është Shqipëria."</p>
      <span>— Shprehje Popullore</span>
    </div>
    <div class="two-col">
      <div class="info-block">
        <h4>🎵 Muzika & Vallet</h4>
        <p>Valle si "Valle e Gegërisë" dhe muzika me lahutë janë tipike për zonat veriore-qendrore. Çdo dasmë shqiptare ka njerëz që vallëzojnë deri në mëngjes — kjo nuk ndryshon kurrë!</p>
      </div>
      <div class="info-block">
        <h4>🍽️ Ushqimi</h4>
        <p>Tavë kosi, byrek me mish, fërgësa tiranase, qofte, korrica dhe rakia tradicionale. Çdo zonë ka specialitetin e vet. Mos ik nga Tirana pa ngrënë fërgës!</p>
      </div>
      <div class="info-block">
        <h4>📚 Letërsia & Arti</h4>
        <p>Ismail Kadare, Fan Noli dhe Faik Konica lidhen me këtë rajon. Teatri Kombëtar dhe Galeria Kombëtare e Arteve janë qendra kryesore kulturore.</p>
      </div>
      <div class="info-block">
        <h4>🕊️ Feja & Toleranca</h4>
        <p>Shqiptarët janë muslimanë, ortodoksë, katolikë dhe bektashinj — dhe bashkëjetojnë shumë mirë. Selia Botërore e Bektashizmit është pikërisht në Tiranë!</p>
      </div>
      <div class="info-block">
        <h4>🏗️ Arkitektura</h4>
        <p>Ndërtesa osmane, vila të vjetra, godina socialiste gjigante dhe ndërtesa moderne. Ky miks çuditërisht funksionon dhe i jep karakter unik Tiranës.</p>
      </div>
      <div class="info-block">
        <h4>🎉 Festat</h4>
        <p>28 Nëntorit, 29 Nëntorit, Novruz, Kurban Bajrami, Krishtlindja — të gjitha festohen. Shqipëria është vend festash!</p>
      </div>
    </div>
  </div>

  <div class="section" id="popullsia">
    <h2>👥 Popullsia</h2>
    <span class="section-sub">Shpërndarja Demografike</span>
    <p>Shqipëria e Mesme është rajoni më i densuar i vendit. Ja si ndahet popullsia nëpër qytete kryesore:</p>
    <div class="pop-bars" id="popBars">
      <div class="pop-row">
        <span class="pop-city">Tirana</span>
        <div class="pop-track"><div class="pop-fill" data-w="85"></div></div>
        <span class="pop-val">~930K</span>
      </div>
      <div class="pop-row">
        <span class="pop-city">Durrësi</span>
        <div class="pop-track"><div class="pop-fill" data-w="55"></div></div>
        <span class="pop-val">~175K</span>
      </div>
      <div class="pop-row">
        <span class="pop-city">Elbasani</span>
        <div class="pop-track"><div class="pop-fill" data-w="40"></div></div>
        <span class="pop-val">~140K</span>
      </div>
      <div class="pop-row">
        <span class="pop-city">Kavaja</span>
        <div class="pop-track"><div class="pop-fill" data-w="18"></div></div>
        <span class="pop-val">~45K</span>
      </div>
      <div class="pop-row">
        <span class="pop-city">Kruja</span>
        <div class="pop-track"><div class="pop-fill" data-w="12"></div></div>
        <span class="pop-val">~30K</span>
      </div>
      <div class="pop-row">
        <span class="pop-city">Peqini</span>
        <div class="pop-track"><div class="pop-fill" data-w="7"></div></div>
        <span class="pop-val">~20K</span>
      </div>
    </div>
    <div class="two-col" style="margin-top:22px">
      <div class="info-block">
        <h4>🌍 Diaspora</h4>
        <p>Vlerësohet se 1–1.5 milion shqiptarë nga ky rajon jetojnë jashtë, kryesisht në Itali, Greqi, Gjermani dhe SHBA. Rimeset e tyre mbajnë ekonominë familjare!</p>
      </div>
      <div class="info-block">
        <h4>📈 Urbanizimi</h4>
        <p>Pas 1990-ës, Tirana u trefishua. Sot 65% e popullatës totale të Shqipërisë jeton brenda 50km nga kryeqyteti. Fenomeni i "larg Tiranës" nuk ekziston më.</p>
      </div>
      <div class="info-block">
        <h4>🎓 Arsimi</h4>
        <p>Universiteti i Tiranës (1957) dhe dhjetëra universitete private bëjnë Tiranën qendrën arsimore. Mbi 60% e të rinjve 18–25 vjeç ndjekin universitet.</p>
      </div>
      <div class="info-block">
        <h4>⛪ Feja</h4>
        <p>Muslimanët ~57%, Ortodoksët ~20%, Katolikët ~10%, Bektashinjtë ~7%. Shqipëria është ndër vendet me tolerancë fetare më të lartë në botë.</p>
      </div>
    </div>
  </div>

  <div class="section" id="ekonomia">
    <h2>💼 Ekonomia</h2>
    <span class="section-sub">Motori i Vendit</span>
    <p>Rajoni qendror gjeneron mbi 65% të GDP-së kombëtare. Ekonomia mbështetet kryesisht në 4 shtylla:</p>
    <div class="pillars">
      <div class="pillar">
        <span class="p-icon">💼</span>
        <h4>Shërbimet</h4>
        <p>Bankat, sigurimet, tregtia dhe IT. Tirana është qendra financiare e rajonit ballkanik perëndimor.</p>
      </div>
      <div class="pillar">
        <span class="p-icon">🏗️</span>
        <h4>Ndërtimi</h4>
        <p>Boom i pasurive të paluajtshme. Autostrada Tiranë–Durrës–Elbasan ka ndryshuar gjithçka.</p>
      </div>
      <div class="pillar">
        <span class="p-icon">🌾</span>
        <h4>Bujqësia</h4>
        <p>Fusha e Myzeqesë prodhon grurë, misër e perime. Ulliri i Kavajës është i famshëm.</p>
      </div>
      <div class="pillar">
        <span class="p-icon">⚡</span>
        <h4>Energjia</h4>
        <p>Hidrocentralet dhe panelet diellore. Shqipëria synon 100% energji të rinovueshme deri 2030.</p>
      </div>
      <div class="pillar">
        <span class="p-icon">✈️</span>
        <h4>Turizmi</h4>
        <p>Aeroporti Nënë Tereza rekorde çdo vit. Turizmi po rritet me 15–20% në vit.</p>
      </div>
      <div class="pillar">
        <span class="p-icon">👕</span>
        <h4>Industria</h4>
        <p>Tekstilet, konfeksionet dhe materialet e ndërtimit janë sektorë tradicionale të rajonit.</p>
      </div>
    </div>
    <p style="margin-top:20px; font-size:0.8rem; color:var(--muted); border-left: 2px solid var(--gold-light); padding-left:14px;">
      <strong style="color:var(--gold); font-weight:600;">Fakt:</strong> GDP e Tiranës e vetme do të ishte ekonomia e dytë ose e tretë më e madhe në Ballkanin Perëndimor nëse do të ishte shtet i veçantë.
    </p>
  </div>

</div>

<footer>
  <p>🇦🇱 &nbsp;<strong>Shqipëria e Mesme</strong> &nbsp;·&nbsp; Zemra e Kombit</p>
  <p style="margin-top:8px; opacity:0.5;">Bërë me dashuri për vendin tonë &nbsp;❤️</p>
</footer>

<script>
  const bars = document.querySelectorAll('.pop-fill');
  const obs = new IntersectionObserver(entries => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        bars.forEach(b => {
          b.style.width = b.getAttribute('data-w') + '%';
        });
        obs.disconnect();
      }
    });
  }, { threshold: 0.3 });

  const popSection = document.getElementById('popBars');
  if (popSection) obs.observe(popSection);

  document.querySelectorAll('a[href^="#"]').forEach(a => {
    a.addEventListener('click', e => {
      e.preventDefault();
      const t = document.querySelector(a.getAttribute('href'));
      if (t) t.scrollIntoView({ behavior: 'smooth' });
    });
  });
</script>

</body>
</html>

      
