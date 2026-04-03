<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>BAC PRO AMÉNAGEMENT ET FINITION</title>
<link href="https://fonts.googleapis.com/css2?family=OpenDyslexic&display=swap" rel="stylesheet">
<style>
  /* OpenDyslexic fallback via CDN */
  @font-face {
    font-family: 'OpenDyslexic';
    src: url('https://cdn.jsdelivr.net/npm/open-dyslexic@1.0.3/fonts/OpenDyslexic-Regular.otf') format('opentype');
    font-weight: normal;
  }
  @font-face {
    font-family: 'OpenDyslexic';
    src: url('https://cdn.jsdelivr.net/npm/open-dyslexic@1.0.3/fonts/OpenDyslexic-Bold.otf') format('opentype');
    font-weight: bold;
  }

  :root {
    --bg: #FFF8E7;
    --card: #FFFDF5;
    --accent1: #E8A020;
    --accent2: #2E7D6B;
    --accent3: #C0392B;
    --accent4: #2980B9;
    --text: #1A1A1A;
    --text-light: #444;
    --border: #D4A843;
    --tab-active: #E8A020;
    --tab-hover: #F5C842;
    --success: #27AE60;
    --error: #E74C3C;
    --warning: #F39C12;
    --shadow: 0 4px 15px rgba(0,0,0,0.12);
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    font-family: 'OpenDyslexic', 'Comic Sans MS', cursive;
    background: var(--bg);
    color: var(--text);
    font-size: 16px;
    line-height: 1.8;
  }

  /* HEADER */
  .site-header {
    background: linear-gradient(135deg, #1A3A2A 0%, #2E7D6B 50%, #1A3A2A 100%);
    padding: 20px 30px;
    text-align: center;
    box-shadow: 0 4px 20px rgba(0,0,0,0.3);
    position: sticky;
    top: 0;
    z-index: 1000;
  }
  .site-header h1 {
    color: #FFD700;
    font-size: 1.8em;
    font-weight: bold;
    text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
    letter-spacing: 2px;
  }
  .site-header .subtitle {
    color: #A8D8C8;
    font-size: 0.9em;
    margin-top: 5px;
  }
  .header-icons { font-size: 2em; margin-bottom: 8px; }

  /* NAVIGATION PRINCIPALE */
  .main-nav {
    background: #2E3A2A;
    overflow-x: auto;
    white-space: nowrap;
    padding: 0;
    border-bottom: 3px solid var(--accent1);
  }
  .main-nav::-webkit-scrollbar { height: 4px; }
  .main-nav::-webkit-scrollbar-track { background: #1a2a1a; }
  .main-nav::-webkit-scrollbar-thumb { background: var(--accent1); border-radius: 2px; }

  .main-nav button {
    display: inline-block;
    padding: 12px 16px;
    background: transparent;
    border: none;
    color: #A8D8C8;
    font-family: 'OpenDyslexic', 'Comic Sans MS', cursive;
    font-size: 0.8em;
    cursor: pointer;
    transition: all 0.3s;
    border-bottom: 3px solid transparent;
    white-space: nowrap;
  }
  .main-nav button:hover { background: rgba(232,160,32,0.2); color: #FFD700; }
  .main-nav button.active {
    background: rgba(232,160,32,0.3);
    color: #FFD700;
    border-bottom: 3px solid var(--accent1);
    font-weight: bold;
  }

  /* CONTENU */
  .content-area { padding: 20px; max-width: 1200px; margin: 0 auto; }

  .tab-content { display: none; }
  .tab-content.active { display: block; }

  /* SOUS-ONGLETS */
  .sub-tabs {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-bottom: 25px;
    background: white;
    padding: 12px;
    border-radius: 12px;
    box-shadow: var(--shadow);
    border-left: 5px solid var(--accent1);
  }
  .sub-tab-btn {
    padding: 8px 16px;
    border: 2px solid var(--accent1);
    background: white;
    color: var(--text);
    font-family: 'OpenDyslexic', 'Comic Sans MS', cursive;
    font-size: 0.85em;
    border-radius: 20px;
    cursor: pointer;
    transition: all 0.3s;
    font-weight: bold;
  }
  .sub-tab-btn:hover { background: var(--tab-hover); }
  .sub-tab-btn.active { background: var(--accent1); color: white; }

  .sub-content { display: none; }
  .sub-content.active { display: block; }

  /* CARDS ET SECTIONS */
  .section-card {
    background: var(--card);
    border-radius: 16px;
    padding: 25px;
    margin-bottom: 20px;
    box-shadow: var(--shadow);
    border-top: 4px solid var(--accent2);
    animation: fadeIn 0.4s ease;
  }
  @keyframes fadeIn { from { opacity:0; transform:translateY(10px); } to { opacity:1; transform:translateY(0); } }

  .section-card h2 {
    color: var(--accent2);
    font-size: 1.3em;
    margin-bottom: 15px;
    padding-bottom: 8px;
    border-bottom: 2px solid #E8F5F0;
    display: flex;
    align-items: center;
    gap: 10px;
  }
  .section-card h3 {
    color: var(--accent1);
    font-size: 1.1em;
    margin: 15px 0 8px 0;
  }
  .section-card p { margin-bottom: 10px; color: var(--text-light); }

  /* INFO BOXES */
  .info-box {
    border-radius: 10px;
    padding: 15px;
    margin: 12px 0;
    display: flex;
    align-items: flex-start;
    gap: 12px;
  }
  .info-box.blue { background: #EBF5FB; border-left: 4px solid #2980B9; }
  .info-box.green { background: #EAFAF1; border-left: 4px solid #27AE60; }
  .info-box.orange { background: #FEF9E7; border-left: 4px solid #F39C12; }
  .info-box.red { background: #FDEDEC; border-left: 4px solid #E74C3C; }
  .info-box .icon { font-size: 1.5em; flex-shrink: 0; }
  .info-box .content p { margin: 0; font-size: 0.95em; }

  /* TABLEAU */
  table {
    width: 100%;
    border-collapse: collapse;
    margin: 15px 0;
    font-size: 0.9em;
  }
  th {
    background: var(--accent2);
    color: white;
    padding: 10px 12px;
    text-align: left;
    font-weight: bold;
  }
  td { padding: 9px 12px; border-bottom: 1px solid #e0e0e0; }
  tr:nth-child(even) td { background: #F8FBF9; }
  tr:hover td { background: #EAF6F2; }

  /* LEXIQUE */
  .lexique-item {
    border-radius: 10px;
    padding: 12px 15px;
    margin-bottom: 10px;
    background: white;
    border-left: 4px solid var(--accent4);
    box-shadow: 0 2px 8px rgba(0,0,0,0.07);
  }
  .lexique-item strong { color: var(--accent4); font-size: 1.05em; }
  .lexique-item p { margin: 4px 0 0 0; color: var(--text-light); font-size: 0.92em; }

  /* CONTRÔLE TRAVAUX */
  .controle-phase {
    background: white;
    border-radius: 12px;
    padding: 18px;
    margin-bottom: 15px;
    border-top: 3px solid var(--accent1);
    box-shadow: 0 2px 10px rgba(0,0,0,0.08);
  }
  .controle-phase h3 { color: var(--accent1); margin-bottom: 12px; }
  .check-item {
    display: flex;
    align-items: center;
    gap: 10px;
    padding: 6px 0;
    border-bottom: 1px dashed #eee;
    font-size: 0.92em;
  }
  .check-item:last-child { border-bottom: none; }
  .check-icon { color: var(--accent2); font-size: 1.1em; }

  /* SÉCURITÉ */
  .securite-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
    gap: 15px;
  }
  .securite-card {
    background: linear-gradient(135deg, #FFF3CD, #FFEAA7);
    border: 2px solid #F39C12;
    border-radius: 12px;
    padding: 15px;
    text-align: center;
  }
  .securite-card .icon { font-size: 2em; display: block; margin-bottom: 8px; }
  .securite-card h4 { color: #E67E22; font-size: 0.95em; margin-bottom: 5px; }
  .securite-card p { font-size: 0.85em; color: var(--text-light); }

  /* QUESTIONNAIRE */
  .quiz-container { max-width: 800px; margin: 0 auto; }
  .quiz-question {
    background: white;
    border-radius: 14px;
    padding: 22px;
    margin-bottom: 20px;
    box-shadow: var(--shadow);
    border-left: 5px solid var(--accent2);
  }
  .quiz-question .q-header {
    display: flex;
    align-items: center;
    gap: 10px;
    margin-bottom: 15px;
  }
  .q-num {
    background: var(--accent2);
    color: white;
    width: 32px;
    height: 32px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: bold;
    font-size: 0.9em;
    flex-shrink: 0;
  }
  .q-text { font-weight: bold; color: var(--text); font-size: 1em; }
  .q-level {
    font-size: 0.75em;
    padding: 3px 8px;
    border-radius: 10px;
    margin-left: auto;
    flex-shrink: 0;
  }
  .q-level.easy { background: #EAFAF1; color: #27AE60; }
  .q-level.medium { background: #FEF9E7; color: #F39C12; }
  .q-level.hard { background: #FDEDEC; color: #E74C3C; }

  .quiz-options { list-style: none; padding: 0; }
  .quiz-options li {
    margin-bottom: 8px;
  }
  .quiz-options label {
    display: flex;
    align-items: center;
    gap: 10px;
    padding: 10px 14px;
    border: 2px solid #e0e0e0;
    border-radius: 10px;
    cursor: pointer;
    transition: all 0.2s;
    font-size: 0.92em;
  }
  .quiz-options label:hover { border-color: var(--accent2); background: #EAF6F2; }
  .quiz-options input[type="radio"],
  .quiz-options input[type="checkbox"] { cursor: pointer; width: 18px; height: 18px; }

  .open-answer {
    width: 100%;
    min-height: 80px;
    border: 2px solid #e0e0e0;
    border-radius: 10px;
    padding: 10px 14px;
    font-family: 'OpenDyslexic', 'Comic Sans MS', cursive;
    font-size: 0.92em;
    resize: vertical;
    color: var(--text);
  }
  .open-answer:focus { outline: none; border-color: var(--accent2); }

  .btn-check {
    background: var(--accent2);
    color: white;
    border: none;
    padding: 10px 20px;
    border-radius: 20px;
    cursor: pointer;
    font-family: 'OpenDyslexic', 'Comic Sans MS', cursive;
    font-size: 0.9em;
    font-weight: bold;
    transition: all 0.3s;
    margin-top: 10px;
  }
  .btn-check:hover { background: #1A5C4A; transform: translateY(-1px); }

  .answer-feedback {
    margin-top: 12px;
    padding: 12px 15px;
    border-radius: 10px;
    font-size: 0.9em;
    display: none;
  }
  .answer-feedback.correct { background: #EAFAF1; border-left: 4px solid #27AE60; color: #1E8449; }
  .answer-feedback.wrong { background: #FDEDEC; border-left: 4px solid #E74C3C; color: #922B21; }

  .quiz-footer {
    background: white;
    border-radius: 14px;
    padding: 22px;
    text-align: center;
    box-shadow: var(--shadow);
    margin-top: 20px;
  }
  .btn-submit {
    background: var(--accent1);
    color: white;
    border: none;
    padding: 15px 40px;
    border-radius: 25px;
    cursor: pointer;
    font-family: 'OpenDyslexic', 'Comic Sans MS', cursive;
    font-size: 1em;
    font-weight: bold;
    transition: all 0.3s;
    box-shadow: 0 4px 15px rgba(232,160,32,0.4);
  }
  .btn-submit:hover { transform: translateY(-2px); box-shadow: 0 6px 20px rgba(232,160,32,0.5); }

  .score-display {
    font-size: 2em;
    font-weight: bold;
    margin: 15px 0;
    display: none;
  }
  .score-display.show { display: block; }
  .score-message { font-size: 1.1em; margin-top: 10px; }

  /* IMAGE EXAMPLES */
  .img-example {
    border-radius: 12px;
    overflow: hidden;
    margin: 15px 0;
    box-shadow: var(--shadow);
    max-width: 100%;
  }
  .img-example img {
    width: 100%;
    max-height: 250px;
    object-fit: cover;
  }
  .img-example .caption {
    background: rgba(0,0,0,0.7);
    color: white;
    padding: 8px 12px;
    font-size: 0.85em;
    text-align: center;
  }
  .img-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    gap: 15px;
    margin: 15px 0;
  }

  /* BADGE */
  .badge {
    display: inline-block;
    padding: 3px 10px;
    border-radius: 12px;
    font-size: 0.8em;
    font-weight: bold;
    margin: 2px;
  }
  .badge.green { background: #EAFAF1; color: #27AE60; border: 1px solid #27AE60; }
  .badge.orange { background: #FEF9E7; color: #E67E22; border: 1px solid #E67E22; }
  .badge.red { background: #FDEDEC; color: #E74C3C; border: 1px solid #E74C3C; }
  .badge.blue { background: #EBF5FB; color: #2980B9; border: 1px solid #2980B9; }

  /* PROGRESS BAR */
  .progress-bar {
    background: #e0e0e0;
    border-radius: 10px;
    height: 10px;
    margin: 5px 0;
    overflow: hidden;
  }
  .progress-bar .fill {
    background: linear-gradient(90deg, var(--accent2), var(--accent1));
    height: 100%;
    border-radius: 10px;
    transition: width 0.5s ease;
  }

  /* SCROLLBAR */
  ::-webkit-scrollbar { width: 8px; }
  ::-webkit-scrollbar-track { background: #f0f0f0; }
  ::-webkit-scrollbar-thumb { background: var(--accent2); border-radius: 4px; }

  /* RESPONSIVE */
  @media (max-width: 768px) {
    .site-header h1 { font-size: 1.2em; }
    .content-area { padding: 12px; }
    .section-card { padding: 16px; }
    .sub-tabs { gap: 6px; }
    .sub-tab-btn { font-size: 0.78em; padding: 6px 12px; }
  }

  /* MISE EN SITUATION */
  .scenario-box {
    background: linear-gradient(135deg, #E8F4FD, #D6EAF8);
    border: 2px solid #2980B9;
    border-radius: 12px;
    padding: 18px;
    margin: 15px 0;
  }
  .scenario-box h4 { color: #1A5276; margin-bottom: 10px; }

  /* DÉSORDRES / PATHOLOGIES */
  .disorder-card {
    background: white;
    border-radius: 12px;
    padding: 18px;
    margin-bottom: 15px;
    border-left: 5px solid var(--accent3);
    box-shadow: 0 2px 10px rgba(0,0,0,0.08);
  }
  .disorder-card h4 { color: var(--accent3); margin-bottom: 8px; }
  .disorder-card .solution {
    background: #EAFAF1;
    border-radius: 8px;
    padding: 10px;
    margin-top: 10px;
    font-size: 0.9em;
    color: #1E8449;
  }
  .disorder-card .solution strong { color: #145A32; }

  /* NORME TAG */
  .norme-tag {
    display: inline-block;
    background: #2E3A2A;
    color: #FFD700;
    padding: 3px 10px;
    border-radius: 6px;
    font-size: 0.8em;
    font-weight: bold;
    margin: 2px;
  }

  ul.styled { padding-left: 20px; }
  ul.styled li { margin-bottom: 6px; color: var(--text-light); }
  ul.styled li::marker { color: var(--accent1); }
</style>
</head>
<body>

<header class="site-header">
  <div class="header-icons">🏗️ 🪣 🖌️ 🧱</div>
  <h1>BAC PRO AMÉNAGEMENT ET FINITION</h1>
  <div class="subtitle">📚 Support pédagogique complet — Révisions, Contrôles, Lexique, Quiz</div>
</header>

<nav class="main-nav" id="mainNav">
  <button class="active" onclick="showTab('carrelage', this)">🟫 Carrelage & Faïence</button>
  <button onclick="showTab('peinture', this)">🖌️ Peinture</button>
  <button onclick="showTab('papierpeint', this)">📜 Papier peint</button>
  <button onclick="showTab('solsouple', this)">🟨 Sol souple</button>
  <button onclick="showTab('carreauxplatre', this)">🧱 Carreaux de plâtre</button>
  <button onclick="showTab('cloison', this)">🏠 Cloison placo</button>
  <button onclick="showTab('doublage', this)">🧊 Doublage</button>
  <button onclick="showTab('plafondsuspendu', this)">⬜ Plafond suspendu</button>
  <button onclick="showTab('plafondautoportant', this)">🔲 Plafond autoportant</button>
  <button onclick="showTab('plafondmodulaire', this)">◻️ Plafond modulaire</button>
  <button onclick="showTab('ite', this)">🏘️ ITE</button>
  <button onclick="showTab('phonique', this)">🔇 Isolation phonique</button>
  <button onclick="showTab('thermique', this)">🌡️ Isolation thermique</button>
  <button onclick="showTab('incendie', this)">🔥 Protection incendie</button>
</nav>

<div class="content-area">

<!-- ================================================== -->
<!-- ONGLET 1 : CARRELAGE / FAÏENCE -->
<!-- ================================================== -->
<div id="carrelage" class="tab-content active">
  <div class="sub-tabs">
    <button class="sub-tab-btn active" onclick="showSub('carrelage', 'revision', this)">📖 Révision générale</button>
    <button class="sub-tab-btn" onclick="showSub('carrelage', 'controle', this)">✅ Contrôle travaux</button>
    <button class="sub-tab-btn" onclick="showSub('carrelage', 'lexique', this)">📝 Lexique</button>
    <button class="sub-tab-btn" onclick="showSub('carrelage', 'securite', this)">⛑️ Mémo sécurité</button>
    <button class="sub-tab-btn" onclick="showSub('carrelage', 'quiz', this)">🎯 Questionnaire d'acquis</button>
  </div>

  <!-- RÉVISION -->
  <div id="carrelage-revision" class="sub-content active">
    <div class="section-card">
      <h2>🟫 Carrelage & Faïence — Révision Générale</h2>
      <div class="img-grid">
        <div class="img-example"><img src="https://images.unsplash.com/photo-1556909114-f6e7ad7d3136?w=400&q=80" alt="Pose de carrelage mural"><div class="caption">📸 Pose de carrelage mural</div></div>
        <div class="img-example"><img src="https://images.unsplash.com/photo-1589939705384-5185137a7f0f?w=400&q=80" alt="Salle de bain carrelée"><div class="caption">📸 Salle de bain avec carrelage</div></div>
      </div>

      <h3>🔹 Terminologie essentielle (NF DTU 52.2)</h3>
      <table>
        <tr><th>Terme</th><th>Définition</th></tr>
        <tr><td><strong>Élément de revêtement</strong></td><td>Terme recouvrant l'ensemble des matériaux : carreaux, dalles, plaquettes de terre cuite, pâte de verre, pierres naturelles</td></tr>
        <tr><td><strong>Revêtement</strong></td><td>Association de plusieurs éléments de revêtement constituant l'ouvrage fini</td></tr>
        <tr><td><strong>Pose collée</strong></td><td>Méthode de fixation d'éléments de revêtement sur un support à l'aide d'un produit de collage</td></tr>
        <tr><td><strong>Marouflage</strong></td><td>Action d'appuyer sur un carreau avec un mouvement de glissement ou de rotation pour assurer le contact entre la colle et l'envers du carreau</td></tr>
        <tr><td><strong>Battage</strong></td><td>Action de taper sur un carreau avec un maillet pour l'enfoncer dans la colle et assurer le contact (sol)</td></tr>
        <tr><td><strong>Élancement (L/l)</strong></td><td>Rapport entre la longueur et la largeur d'un carreau. Si L/l ≥ 3 : carreau non visé par le calepin sol</td></tr>
        <tr><td><strong>DPU</strong></td><td>Durée Pratique d'Utilisation — temps pendant lequel le mortier-colle gâché peut être utilisé</td></tr>
      </table>

      <h3>🔹 Les types de carreaux et formats</h3>
      <table>
        <tr><th>Type</th><th>Utilisation</th><th>Absorption eau</th><th>Format max admis</th></tr>
        <tr><td>Faïence (BIa, BIIa)</td><td>Mur intérieur</td><td>Porosité élevée, émaillée</td><td>S ≤ 3 600 cm² (mur)</td></tr>
        <tr><td>Grès cérame vitrifié (BIa)</td><td>Sol et mur</td><td>≤ 0,5% — très résistant</td><td>Sol int. : S ≤ 3 600 cm² / L ≤ 90 cm</td></tr>
        <tr><td>Grès émaillé (BIb)</td><td>Sol intérieur</td><td>0,5% à 3%</td><td>Sol int. : S ≤ 3 600 cm² / L ≤ 90 cm</td></tr>
        <tr><td>Pierre naturelle</td><td>Sol et mur</td><td>Variable (porosité ≤ 2% ou &gt; 2%)</td><td>Sol int. : S ≤ 3 600 cm² / L ≤ 80 cm — Sol ext. : S ≤ 3 600 cm² / L ≤ 60 cm</td></tr>
        <tr><td>Mosaïque / Pâte de verre</td><td>Sol et mur</td><td>Variable</td><td>S ≤ 300 cm² (pâte de verre)</td></tr>
        <tr><td>Terre cuite / Carreaux étirés</td><td>Sol intérieur</td><td>Élevée</td><td>Joint mini 6 mm obligatoire</td></tr>
      </table>
      <div class="info-box orange"><div class="icon">📏</div><div class="content"><p><strong>Formats extérieurs :</strong> Carreaux céramiques S ≤ 2 200 cm² — longueur maxi 60 cm. Pierres naturelles S ≤ 3 600 cm² — longueur maxi 60 cm. Au-delà : vérification DTU nécessaire.</p></div></div>
      <div class="info-box blue"><div class="icon">💡</div><div class="content"><p><strong>Élancement L/l ≥ 3 :</strong> Un carreau de 70 cm × 15 cm a un élancement de 4,67. Il n'est <strong>pas visé</strong> par les calepins de chantier DTU 52.2 et nécessite une étude spécifique.</p></div></div>

      <h3>🔹 Conditions d'environnement (NF DTU 52.2)</h3>
      <div class="info-box red"><div class="icon">🌡️</div><div class="content"><p><strong>Température de pose :</strong> Support et air ambiant &gt; +5°C et &lt; 30°C. <strong>Support gelé = interdit</strong>. Ni sous forte chaleur ambiante ≥ 35°C. Local clos et hors d'eau obligatoire. <strong>Co-activité interdite</strong> : les autres corps d'état ne doivent pas travailler en même temps.</p></div></div>
      <div class="info-box orange"><div class="icon">⚠️</div><div class="content"><p><strong>Par temps chaud, sous l'action du soleil ou du vent, ou sur supports très poreux :</strong> le temps ouvert de la colle est réduit. Encoller de plus petites surfaces.</p></div></div>

      <h3>🔹 Classification UPEC</h3>
      <table>
        <tr><th>Lettre</th><th>Signification</th><th>Niveaux</th><th>Ce que ça mesure</th></tr>
        <tr><td><strong>U</strong></td><td>Usure</td><td>U2 à U4</td><td>Résistance à l'abrasion de surface</td></tr>
        <tr><td><strong>P</strong></td><td>Poinçonnement</td><td>P2 à P4</td><td>Résistance aux charges concentrées</td></tr>
        <tr><td><strong>E</strong></td><td>Eau</td><td>E0 à E3</td><td>Résistance à l'eau et à l'humidité</td></tr>
        <tr><td><strong>C</strong></td><td>Chimique</td><td>C0 à C2</td><td>Résistance aux agents chimiques (nettoyants)</td></tr>
      </table>

      <h3>🔹 Classement des locaux — Exposition à l'eau</h3>
      <table>
        <tr><th>Classement</th><th>Description</th><th>Exemples</th></tr>
        <tr><td><span class="badge blue">EA</span></td><td>Locaux secs</td><td>Chambre, couloir, bureau</td></tr>
        <tr><td><span class="badge blue">EB</span></td><td>Locaux moyennement humides</td><td>Cuisine habitation</td></tr>
        <tr><td><span class="badge orange">EB+ privatif</span></td><td>Exposition à l'eau beaucoup — salle de bain privative</td><td>SdB avec douche ou baignoire</td></tr>
        <tr><td><span class="badge red">EB+ collectif</span></td><td>Locaux collectifs humides</td><td>Vestiaires, salle de sport</td></tr>
        <tr><td><span class="badge red">EC</span></td><td>Exposition à l'eau continuelle</td><td>Douche collective, local technique, piscine</td></tr>
      </table>

      <h3>🔹 Délais avant pose selon le support (NF DTU 52.2)</h3>
      <table>
        <tr><th>Type de support</th><th>Délai avant pose (mortier-colle)</th><th>Délai avant pose (adhésif)</th></tr>
        <tr><td>Béton neuf (plancher)</td><td>2 mois après enlèvement étais</td><td>2 mois après enlèvement étais</td></tr>
        <tr><td>Dalle béton sur terre-plein</td><td>1 mois minimum</td><td>1 mois minimum</td></tr>
        <tr><td>Enduit base ciment</td><td>2 jours</td><td>3 semaines</td></tr>
        <tr><td>Support base plâtre (S4/S5)</td><td>Sans objet (voir humidité &lt;5%)</td><td>Humidité résiduelle ≤ 5%</td></tr>
        <tr><td>Carreaux de terre cuite (S12)</td><td>1 jour</td><td>1 jour</td></tr>
        <tr><td>Blocs béton cellulaire</td><td>1 jour</td><td>1 jour</td></tr>
        <tr><td>Chape/dalle désolidarisée</td><td>15 jours minimum</td><td>15 jours minimum</td></tr>
        <tr><td>Chape/dalle adhérente</td><td>1 mois minimum</td><td>1 mois minimum</td></tr>
        <tr><td>Protection d'étanchéité</td><td>15 jours minimum</td><td>15 jours minimum</td></tr>
      </table>
      <div class="info-box red"><div class="icon">⚠️</div><div class="content"><p><strong>Produit de cure :</strong> Si un produit de cure a été utilisé lors de la réalisation du support, la pose collée directe n'est applicable que si ce produit a été préalablement éliminé par <strong>grenaillage, sablage ou ponçage abrasif</strong>.</p></div></div>

      <h3>🔹 Tolérance du support (NF DTU 52.2)</h3>
      <table>
        <tr><th>Type de tolérance</th><th>Valeur sol</th><th>Valeur mur</th></tr>
        <tr><td>Planéité sous règle de 2m</td><td>≤ 5 mm</td><td>Courant ≤ 7 mm / Soigné ≤ 5 mm</td></tr>
        <tr><td>Planéité sous règle de 0,20m</td><td>≤ 2 mm</td><td>≤ 2 mm</td></tr>
        <tr><td>Faux aplomb (mur)</td><td>—</td><td>≤ 5 mm sur une hauteur d'étage (2,50m)</td></tr>
        <tr><td>Pente sol intérieur avec siphon</td><td>1% minimum</td><td>—</td></tr>
        <tr><td>Pente sol extérieur</td><td>1,5% minimum</td><td>—</td></tr>
      </table>

      <h3>🔹 La chape — types et délais</h3>
      <table>
        <tr><th>Type de chape</th><th>Description</th><th>Délai avant carrelage</th></tr>
        <tr><td>Chape adhérente base ciment</td><td>Collée au support béton</td><td>1 mois minimum</td></tr>
        <tr><td>Chape désolidarisée</td><td>Sur isolant ou couche désolidarisante</td><td>15 jours minimum</td></tr>
        <tr><td>Chape fluide (anhydrite)</td><td>Sulfate de calcium — plancher chauffant</td><td>Selon DTU 65.14 (14 jours + mise en chauffe)</td></tr>
        <tr><td>Chape sèche</td><td>Panneaux préfabriqués</td><td>Rénovation rapide — vérifier DTA</td></tr>
      </table>

      <h3>🔹 Plancher chauffant — procédure obligatoire</h3>
      <div class="controle-phase">
        <div class="check-item"><span class="check-icon">1️⃣</span> Pose isolant + tubes eau chaude + épreuve d'étanchéité</div>
        <div class="check-item"><span class="check-icon">2️⃣</span> Coulage couche d'enrobage (chape)</div>
        <div class="check-item"><span class="check-icon">3️⃣</span> Séchage naturel <strong>14 jours minimum</strong> (NF DTU 65.14)</div>
        <div class="check-item"><span class="check-icon">4️⃣</span> Mise en chauffe progressive : 3 jours à 20-25°C puis 4 jours à T° maxi de service</div>
        <div class="check-item"><span class="check-icon">5️⃣</span> Arrêt du chauffage <strong>2 jours minimum</strong> avant la pose du carrelage</div>
        <div class="check-item"><span class="check-icon">6️⃣</span> Utiliser obligatoirement mortier-colle <strong>C2 S1/S2</strong> (déformable)</div>
      </div>

      <h3>🔹 SPEC & SEL — Étanchéité en locaux humides</h3>
      <table>
        <tr><th></th><th>SPEC</th><th>SEL</th></tr>
        <tr><td><strong>Signification</strong></td><td>Système de Protection à l'Eau sous Carrelage</td><td>Système d'Étanchéité Liquide</td></tr>
        <tr><td><strong>Application</strong></td><td>Parois verticales (murs)</td><td>Sols horizontaux</td></tr>
        <tr><td><strong>Locaux</strong></td><td>EB+ (privatif et collectif) et EC</td><td>EB+ et EC</td></tr>
        <tr><td><strong>Forme</strong></td><td>Liquide ou solide (natte, film)</td><td>Uniquement liquide</td></tr>
        <tr><td><strong>Rôle</strong></td><td>Protège le support — NE garantit PAS l'étanchéité</td><td>Garantit l'étanchéité du plancher</td></tr>
        <tr><td><strong>Délai béton</strong></td><td>—</td><td>28 jours si dalle béton neuve</td></tr>
        <tr><td><strong>Assurance</strong></td><td>Couverte par qualif. 6312/6313</td><td>Souvent avenant nécessaire !</td></tr>
      </table>

      <h3>🔹 Classification des colles — NF EN 12004</h3>
      <table>
        <tr><th>Classe</th><th>Type</th><th>Usage typique</th></tr>
        <tr><td><span class="badge blue">C1</span></td><td>Mortier-colle normal</td><td>Travaux courants intérieur, petits formats</td></tr>
        <tr><td><span class="badge blue">C2</span></td><td>Mortier-colle amélioré</td><td>Grand format, extérieur, piscine, pierres</td></tr>
        <tr><td><span class="badge green">C2 S1</span></td><td>Mortier-colle amélioré déformable</td><td>Plancher chauffant, façades, grands formats</td></tr>
        <tr><td><span class="badge green">C2 S2</span></td><td>Mortier-colle très déformable</td><td>Très grands formats, conditions extrêmes</td></tr>
        <tr><td><span class="badge orange">D1</span></td><td>Adhésif en dispersion normal</td><td>Intérieur sec, carreaux plâtre (EA)</td></tr>
        <tr><td><span class="badge orange">D2</span></td><td>Adhésif en dispersion amélioré</td><td>Résistant à l'eau, carreaux plâtre (EB)</td></tr>
        <tr><td><span class="badge red">R1/R2</span></td><td>Colle réactive (époxy)</td><td>Zones à fortes sollicitations chimiques</td></tr>
      </table>
      <p><strong>Options de la colle :</strong> <span class="badge blue">E</span> Temps ouvert allongé (30 min) &nbsp; <span class="badge green">F</span> Prise rapide (10 min) &nbsp; <span class="badge orange">T</span> Résistance au glissement (mur) &nbsp; <span class="badge blue">G</span> Fluide (simple encollage universel)</p>
      <div class="info-box blue"><div class="icon">🎯</div><div class="content"><p><strong>Règle de choix rapide :</strong> Carreaux céramiques et pâtes de verre → C2 ou C2-S1/S2. Pierres naturelles → C2 ou C2-S1/S2. Extérieur → C2 minimum. Plancher chauffant → C2-S1/S2 obligatoire.</p></div></div>

      <h3>🔹 Préparation du mortier-colle</h3>
      <div class="controle-phase">
        <div class="check-item"><span class="check-icon">1️⃣</span> Gâchage au <strong>malaxeur lent (500 tr/min maximum)</strong> — gâchage manuel possible pour petites quantités</div>
        <div class="check-item"><span class="check-icon">2️⃣</span> Respecter la <strong>proportion de liquide de gâchage</strong> indiquée sur le sac</div>
        <div class="check-item"><span class="check-icon">3️⃣</span> Respecter le <strong>temps de repos</strong> de la pâte : environ 10 min pour mortier normal, puis mélanger brièvement</div>
        <div class="check-item"><span class="check-icon">4️⃣</span> Respecter la <strong>DPU (Durée Pratique d'Utilisation)</strong> indiquée sur le sac</div>
        <div class="check-item"><span class="check-icon">5️⃣</span> <strong>Adhésif (prêt à l'emploi) :</strong> Malaxer dans le seau avant emploi. Si pot ouvert &gt; 6h → peau en surface → enlever la peau + légère malaxation. Si ouvert &gt; 6h : produit à ne plus utiliser.</div>
      </div>

      <h3>🔹 Simple encollage vs Double encollage</h3>
      <table>
        <tr><th>Technique</th><th>Description</th><th>Usage</th></tr>
        <tr><td><strong>Simple encollage</strong></td><td>Colle appliquée sur le support uniquement, à la taloche puis peignée à la spatule crantée. Carreau posé avant formation d'une peau.</td><td>Petits et moyens formats selon tableau</td></tr>
        <tr><td><strong>Double encollage</strong></td><td>Colle sur le support (comme simple encollage) + beurrage sur la totalité de la face collée du carreau à la truelle. Mise en place immédiate.</td><td>Grands formats, pierres, extérieur</td></tr>
      </table>
      <div class="info-box green"><div class="icon">📊</div><div class="content"><p><strong>Règle simple encollage/double encollage (sol intérieur, mortier-colle) :</strong><br>
      → Carreaux absorption ≤ 0,5% ou porosité pierre ≤ 2% : Simple encollage si S ≤ 500 cm² / Double si 500 &lt; S ≤ 3 600 cm²<br>
      → Carreaux absorption &gt; 0,5% ou porosité pierre &gt; 2% : Simple si S ≤ 1 100 cm² / Double si 1 100 &lt; S ≤ 3 600 cm²</p></div></div>
      <div class="info-box blue"><div class="icon">🏗️</div><div class="content"><p><strong>Mur intérieur :</strong> Simple encollage si S ≤ 50 cm² (U3), S ≤ 500 cm² (U6). Double encollage si 500 &lt; S ≤ 3 600 cm² (U9).</p></div></div>

      <h3>🔹 Les spatules crantées — choix selon format</h3>
      <p>La spatule crantée est l'outil qui répartit la colle en cordons réguliers. Son choix conditionne la <strong>consommation minimale</strong> de mortier-colle et le bon contact colle/carreau.</p>
      <table>
        <tr><th>Désignation spatule</th><th>Format dents</th><th>Surface carreaux (cm²)</th><th>Consommation (kg/m²)</th></tr>
        <tr><td>U3</td><td>Petites dents</td><td>S ≤ 50 cm²</td><td>1,5 kg/m²</td></tr>
        <tr><td>U6</td><td>Dents moyennes</td><td>50 &lt; S ≤ 500 cm² (int.) / 50 &lt; S ≤ 300 cm² (ext.)</td><td>3,5 à 5 kg/m²</td></tr>
        <tr><td>U9</td><td>Grandes dents carrées</td><td>500 &lt; S ≤ 2 000 cm²</td><td>6 à 7 kg/m²</td></tr>
        <tr><td>Demi-lune Ø20 / 8×10×20</td><td>Très grandes dents</td><td>S &gt; 2 000 cm² (grands formats)</td><td>7 à 8 kg/m²</td></tr>
        <tr><td>V6 (dents triangulaires)</td><td>Dents triangulaires</td><td>Adhésif : S ≤ 500 cm²</td><td>3 kg/m²</td></tr>
      </table>
      <div class="info-box orange"><div class="icon">⚠️</div><div class="content"><p><strong>Important :</strong> Une consommation 15% inférieure aux valeurs minimales peut être acceptée sur des surfaces limitées. Au-delà de cette tolérance = non-conformité.</p></div></div>

      <h3>🔹 Temps ouvert — mise en place des carreaux</h3>
      <table>
        <tr><th>Type de mortier-colle</th><th>Temps ouvert</th><th>Surface à encoller</th></tr>
        <tr><td>Durcissement normal</td><td>15 à 20 min (mur) / 20 min (sol)</td><td>1 à 2 m²</td></tr>
        <tr><td>Durcissement rapide (F)</td><td>10 min</td><td>&lt; 1 m² (demi-sac de 25 kg)</td></tr>
        <tr><td>Temps ouvert allongé (E)</td><td>30 min</td><td>&gt; 2 m²</td></tr>
      </table>
      <div class="info-box red"><div class="icon">🚫</div><div class="content"><p><strong>Ne jamais dépasser le temps ouvert !</strong> Si une peau se forme en surface de la colle, ne pas poser le carreau. Gratter et remettre de la colle fraîche.</p></div></div>

      <h3>🔹 Marouflage et battage — contrôle du contact</h3>
      <p>La pression exercée sur le carreau doit permettre l'<strong>écrasement des sillons de la colle sur au moins 70% de la surface</strong>. En simple encollage, vérifier régulièrement le transfert de colle sur l'envers du carreau en le soulevant.</p>
      <table>
        <tr><th>Technique</th><th>Outil</th><th>Usage</th></tr>
        <tr><td><strong>Marouflage</strong></td><td>Main ou règle caoutchouc — mouvement glissement/rotation</td><td>Carreaux muraux, petits formats sol</td></tr>
        <tr><td><strong>Battage</strong></td><td>Maillet caoutchouc</td><td>Carreaux de sol, grands formats</td></tr>
        <tr><td><strong>Mortier fluide (G)</strong></td><td>Simple encollage uniquement</td><td>Carreaux de 120 cm² à 3 600 cm²</td></tr>
      </table>

      <h3>🔹 Les joints — largeurs et types (NF DTU 52.2)</h3>
      <div class="info-box red"><div class="icon">🚫</div><div class="content"><p><strong>La pose à joint nul n'est JAMAIS admise</strong> — ni en sol ni en mur. Largeur minimale : 2 mm partout.</p></div></div>
      <table>
        <tr><th>Type de carreau</th><th>Sol intérieur</th><th>Sol extérieur</th><th>Mur intérieur</th></tr>
        <tr><td>Carreaux pressés certifiés NF UPEC</td><td>≥ 2 mm (joint réduit)</td><td>≥ 5 mm</td><td>≥ 2 mm</td></tr>
        <tr><td>Carreaux pressés NF EN 14411</td><td>≥ 4 mm (joint normal)</td><td>≥ 5 mm</td><td>≥ 2 mm</td></tr>
        <tr><td>Carreaux de terre cuite / étirés</td><td>≥ 6 mm</td><td>—</td><td>—</td></tr>
        <tr><td>Pierres naturelles</td><td>≥ 2 mm</td><td>≥ 5 mm</td><td>≥ 2 mm</td></tr>
        <tr><td>Carreaux rectifiés (±0,25 mm)</td><td>≥ 2 mm possible</td><td>—</td><td>≥ 2 mm</td></tr>
      </table>
      <p><strong>Largeurs indicatives par format (grès sol) :</strong></p>
      <table>
        <tr><th>Format (cm × cm)</th><th>Largeur joint conseillée</th></tr>
        <tr><td>15 × 15</td><td>2 mm</td></tr>
        <tr><td>20 × 20 / 25 × 25</td><td>2 à 4 mm</td></tr>
        <tr><td>30 × 30 / 45 × 45</td><td>4 à 6 mm</td></tr>
      </table>
      <div class="info-box orange"><div class="icon">⏱️</div><div class="content"><p><strong>Délai avant jointoiement :</strong> Mortier-colle normal → le lendemain (15 à 20°C). Mortier rapide → 3 à 6h. Adhésif → le lendemain (carreaux AIIa, BIIa et pierres) ou après 3 jours (autres).</p></div></div>
      <p><strong>Étapes du jointoiement :</strong></p>
      <div class="controle-phase">
        <div class="check-item"><span class="check-icon">1️⃣</span> Enlever les cales et croisillons</div>
        <div class="check-item"><span class="check-icon">2️⃣</span> Faire les joints à la raclette caoutchouc</div>
        <div class="check-item"><span class="check-icon">3️⃣</span> Enlever les surplus de pâte de joint avant séchage</div>
        <div class="check-item"><span class="check-icon">4️⃣</span> Nettoyer avant le séchage complet des joints</div>
      </div>

      <h3>🔹 Joints de fractionnement et périphériques</h3>
      <table>
        <tr><th>Type de joint</th><th>Largeur</th><th>Rôle</th><th>Règle</th></tr>
        <tr><td>Joint de remplissage (coulis)</td><td>2 à 6 mm selon format</td><td>Combler l'espace entre carreaux</td><td>Pose à joint nul interdit</td></tr>
        <tr><td>Joint de fractionnement</td><td>≥ 5 mm</td><td>Absorber les mouvements du support</td><td>Reprend uniquement les joints du support — pas de fractionnement complémentaire</td></tr>
        <tr><td>Joint périphérique (pied de mur)</td><td>≥ 3 mm (normal) / ≥ 5 mm (plancher chauffant)</td><td>Désolidarise le carrelage des murs</td><td>Rempli de mastic souple (silicone)</td></tr>
        <tr><td>Joint de dilatation</td><td>Reprend joints bâtiment</td><td>Reprend les mouvements structurels</td><td>Jamais à couper ou boucher</td></tr>
      </table>

      <h3>🔹 Tolérances de l'ouvrage fini (NF DTU 52.2)</h3>
      <table>
        <tr><th>Critère</th><th>Tolérance admise</th></tr>
        <tr><td>Alignement des joints (sol)</td><td>≤ 2 mm sur 2 m</td></tr>
        <tr><td>Désaffleurement entre 2 carreaux adjacents</td><td>0,5 mm + 1/10e de la largeur du joint</td></tr>
        <tr><td>Alignement des joints (mur)</td><td>≤ 2 mm sur 2 m</td></tr>
        <tr><td>Désaffleurement mur</td><td>≤ 3 mm sur 2 m</td></tr>
      </table>
      <div class="info-box blue"><div class="icon">👁️</div><div class="content"><p><strong>Méthode d'observation :</strong> L'aspect final du revêtement s'évalue à une hauteur de <strong>1,65 m</strong> et à une distance de <strong>2 m</strong>, avec un éclairage non rasant (angle lumière/revêtement &gt; 45°). Un revêtement collé doit <strong>sonner plein</strong>.</p></div></div>

      <h3>🔹 Délais avant mise en service (sol)</h3>
      <table>
        <tr><th>Type de mortier-colle</th><th>Circulation pédestre sans protection</th><th>Mise en service normal</th></tr>
        <tr><td>Durcissement normal</td><td>12 heures</td><td>36 heures</td></tr>
        <tr><td>Durcissement rapide (F)</td><td>3 à 6 heures</td><td>12 heures</td></tr>
      </table>

      <h3>🔹 Diagnostic du support — 7 points clés</h3>
      <div class="controle-phase">
        <div class="check-item"><span class="check-icon">1️⃣</span> <strong>Planéité :</strong> Règle de 2m (≤ 5mm sol / ≤ 7mm mur courant / ≤ 5mm mur soigné) + réglet 20cm (≤ 2mm)</div>
        <div class="check-item"><span class="check-icon">2️⃣</span> <strong>Humidité :</strong> Mesure au carbure (CME) — max 5% pour supports plâtre (adhésif), voir délais selon support</div>
        <div class="check-item"><span class="check-icon">3️⃣</span> <strong>Résistance / cohésion :</strong> Test au couteau ou à la bille — Shore C ≥ 40 pour support plâtre</div>
        <div class="check-item"><span class="check-icon">4️⃣</span> <strong>Absence de parties creuses :</strong> Sondage au maillet ou à la bille</div>
        <div class="check-item"><span class="check-icon">5️⃣</span> <strong>Compatibilité support/colle :</strong> Choisir mortier-colle ou adhésif selon tableau support × local</div>
        <div class="check-item"><span class="check-icon">6️⃣</span> <strong>Propreté :</strong> Absence de graisse, huile, poussière, laitance, produit de cure</div>
        <div class="check-item"><span class="check-icon">7️⃣</span> <strong>Pente (sol) :</strong> ≥ 1% si local avec siphon / ≥ 1,5% en extérieur</div>
      </div>

      <h3>🔹 Stockage des matériaux (NF DTU 52.2)</h3>
      <div class="securite-grid" style="margin-top:10px;">
        <div class="securite-card"><span class="icon">🏗️</span><h4>Mortier-colle (sacs)</h4><p>Stocker sous abri dans un local sécurisé (auvent). Sur palette ou support sec — risque d'humidité.</p></div>
        <div class="securite-card"><span class="icon">🪨</span><h4>Pierres naturelles</h4><p>Stocker à l'intérieur (choc thermique et gel). Sur palette SANS emballage plastique.</p></div>
        <div class="securite-card"><span class="icon">📦</span><h4>Carreaux céramiques</h4><p>Sous abri, à l'abri du gel. Vérifier numéros de lots à la réception.</p></div>
      </div>
    </div>
  </div>

  <!-- CONTRÔLE TRAVAUX -->
  <div id="carrelage-controle" class="sub-content">
    <div class="section-card">
      <h2>✅ Contrôle des Travaux — Carrelage & Faïence</h2>
      <div class="controle-phase">
        <h3>🔵 AVANT LES TRAVAUX</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Vérifier la nature et la planéité du support (règle de 2m, écart ≤ 5mm)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Mesurer le taux d'humidité du support (≤ 4% pour béton)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Contrôler la résistance mécanique : sondage au maillet</div>
        <div class="check-item"><span class="check-icon">☑️</span> Vérifier l'absence de fissures actives (repérer, attendre stabilisation)</div>
        <div class="check-item"><span class="check-icon">☑️</span> S'assurer que le support est propre, sec, sain et sans poussière</div>
        <div class="check-item"><span class="check-icon">☑️</span> Vérifier la conformité du classement UPEC selon le local</div>
        <div class="check-item"><span class="check-icon">☑️</span> Prévoir le SPEC (mur) ou SEL (sol) si local humide EB+ ou EC</div>
        <div class="check-item"><span class="check-icon">☑️</span> Choisir la colle selon la norme NF EN 12004 (C1, C2, C2S1...)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Contrôler la conformité des carreaux (calibre, aspect, lot de fabrication)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Vérifier la traçabilité des produits (fiches techniques, DTA)</div>
      </div>
      <div class="controle-phase">
        <h3>🟡 PENDANT LES TRAVAUX</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Appliquer le primaire d'accrochage si nécessaire</div>
        <div class="check-item"><span class="check-icon">☑️</span> Appliquer SPEC sur parois verticales humides avant collage</div>
        <div class="check-item"><span class="check-icon">☑️</span> Appliquer SEL sur sol avant carrelage (zones EB+ / EC)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Respecter l'épaisseur de la colle (5 à 10mm selon carreau)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Vérifier le bon mouillage des carreaux (≥ 65% en intérieur, ≥ 80% en extérieur)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Respecter le temps ouvert de la colle (15 à 30 min selon produit)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Poser les croisillons ou espaceurs pour joints réguliers</div>
        <div class="check-item"><span class="check-icon">☑️</span> Contrôler la planéité au fur et à mesure (règle, niveau laser)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Préserver les joints périphériques (pied de mur, angle)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Ranger mélange des lots (même référence, même nuance)</div>
      </div>
      <div class="controle-phase">
        <h3>🟢 APRÈS LES TRAVAUX</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Attendre durcissement colle avant jointoiement (24h à 48h)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Nettoyer les joints avant séchage du coulis</div>
        <div class="check-item"><span class="check-icon">☑️</span> Vérifier la planéité finale (règle 2m, écart ≤ 5mm)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Vérifier qu'aucun carreau ne sonne creux (sondage)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Contrôler l'alignement, les diagonales, la régularité des joints</div>
        <div class="check-item"><span class="check-icon">☑️</span> Poser les joints souples silicone aux angles et périphérie</div>
        <div class="check-item"><span class="check-icon">☑️</span> Tester l'étanchéité (mise en eau 24h si douche à l'italienne)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Protéger le chantier pendant la période de cure</div>
        <div class="check-item"><span class="check-icon">☑️</span> Nettoyer les carreaux des résidus de colle et de coulis</div>
        <div class="check-item"><span class="check-icon">☑️</span> Rédiger le DOE (Dossier des Ouvrages Exécutés)</div>
      </div>
    </div>
  </div>

  <!-- LEXIQUE -->
  <div id="carrelage-lexique" class="sub-content">
    <div class="section-card">
      <h2>📝 Lexique — Carrelage & Faïence</h2>
      <div class="lexique-item"><strong>Absorption d'eau</strong><p>Quantité d'eau qu'un carreau peut absorber, exprimée en %. Grès cérame vitrifié : ≤ 0,5%. Conditionne le choix du mode d'encollage (simple ou double) et de la colle.</p></div>
      <div class="lexique-item"><strong>Adhérence</strong><p>Capacité d'un produit à se fixer solidement sur un support. Mesurée en N/mm². La colle C2 doit avoir une adhérence ≥ 1 N/mm².</p></div>
      <div class="lexique-item"><strong>Battage</strong><p>Technique de mise en place d'un carreau de sol en tapant avec un maillet caoutchouc pour l'enfoncer dans la colle et assurer un contact ≥ 70% de la surface.</p></div>
      <div class="lexique-item"><strong>Beurrage</strong><p>Opération du double encollage consistant à appliquer la colle sur la totalité de la face collée du carreau à l'aide d'une truelle, avant sa mise en place immédiate.</p></div>
      <div class="lexique-item"><strong>Calibre</strong><p>Dimension nominale d'un carreau. Les carreaux d'un même lot doivent avoir le même calibre pour obtenir des joints réguliers.</p></div>
      <div class="lexique-item"><strong>Chape adhérente</strong><p>Chape liée mécaniquement au support béton. Délai avant carrelage : 1 mois minimum.</p></div>
      <div class="lexique-item"><strong>Chape désolidarisée</strong><p>Chape posée sur une couche de désolidarisation (feutre, isolant) sans liaison avec le support. Délai : 15 jours minimum.</p></div>
      <div class="lexique-item"><strong>Chape fluide (anhydrite)</strong><p>Chape à base de sulfate de calcium, coulée en phase liquide. Utilisée sous plancher chauffant. Nécessite 14 jours de séchage + mise en chauffe progressive avant carrelage.</p></div>
      <div class="lexique-item"><strong>Classement UPEC</strong><p>Système français de classification des revêtements de sol selon leur résistance à l'Usure, au Poinçonnement, à l'Eau et aux agents Chimiques. Ex : U3P3E2C1.</p></div>
      <div class="lexique-item"><strong>Co-activité (interdite)</strong><p>Présence d'autres corps d'état pendant la pose du carrelage. Interdite selon le NF DTU 52.2 : risque de vibrations, chocs, projections compromettant l'accrochage.</p></div>
      <div class="lexique-item"><strong>Colle C2 S1 / C2 S2</strong><p>Mortier-colle amélioré déformable. Adhérence ≥ 1 N/mm². S1 = déformabilité 2,5 à 5mm. S2 = déformabilité &gt; 5mm. Obligatoire sur plancher chauffant, façades, grands formats.</p></div>
      <div class="lexique-item"><strong>Coulis de jointement</strong><p>Mortier fin (joint en sac prêt à l'emploi ou sable + ciment + eau) appliqué entre les carreaux après séchage de la colle pour remplir les joints.</p></div>
      <div class="lexique-item"><strong>Crossette</strong><p>Encoche pratiquée dans un carreau pour permettre son adaptation aux obstacles (tuyaux, gaines).</p></div>
      <div class="lexique-item"><strong>Désaffleurement</strong><p>Écart de niveau entre les rives de deux carreaux adjacents mesuré perpendiculairement au plan de collage. Maximum admis : 0,5 mm + 1/10e de la largeur du joint.</p></div>
      <div class="lexique-item"><strong>Double encollage</strong><p>Technique où la colle est appliquée à la fois sur le support ET sur l'envers du carreau (beurrage). Obligatoire pour les grands formats et en extérieur. Assure un contact colle/carreau ≥ 70%.</p></div>
      <div class="lexique-item"><strong>DPU (Durée Pratique d'Utilisation)</strong><p>Temps pendant lequel un mortier-colle gâché reste utilisable dans son seau après mélange. Indiqué sur le sac. Ne pas dépasser sous peine de perte d'adhérence.</p></div>
      <div class="lexique-item"><strong>DTA</strong><p>Document Technique d'Application. Document officiel autorisant l'emploi d'un procédé technique non traditionnel (ex : certains SPEC).</p></div>
      <div class="lexique-item"><strong>EB+</strong><p>Exposition à l'Eau Beaucoup. Salle de bain privative (EB+ privatif) ou collective (EB+ collectif). Détermine le choix du support et du système d'étanchéité.</p></div>
      <div class="lexique-item"><strong>EC</strong><p>Exposition à l'Eau Continuelle. Douche collective, local technique humide, piscine. Support et système d'étanchéité très stricts.</p></div>
      <div class="lexique-item"><strong>Élancement (L/l)</strong><p>Rapport longueur/largeur d'un carreau. Si L/l ≥ 3 (ex : 70 cm × 15 cm = 4,67) : carreau non visé par le calepin NF DTU 52.2, étude spécifique nécessaire.</p></div>
      <div class="lexique-item"><strong>Faïence</strong><p>Carreau en céramique poreuse émaillée (BIIb). Absorption d'eau élevée. Réservé aux murs intérieurs. Format max S ≤ 3 600 cm² en mural.</p></div>
      <div class="lexique-item"><strong>Grenaillage</strong><p>Technique de préparation de surface consistant à projeter des billes métalliques pour éliminer les produits de cure, les souillures, et créer une rugosité propice au collage.</p></div>
      <div class="lexique-item"><strong>Grès cérame</strong><p>Carreau à très faible porosité (≤ 0,5%), très résistant (BIa). Peut être poli, rectifié ou naturel. Utilisable sol et mur.</p></div>
      <div class="lexique-item"><strong>Joint de fractionnement</strong><p>Joint ≥ 5 mm traversant toute l'épaisseur mortier + carreau. Reprend uniquement les joints existants du support. Rempli de mastic souple (shore A ≥ 60).</p></div>
      <div class="lexique-item"><strong>Joint périphérique</strong><p>Joint souple (silicone) placé en pied de mur et aux angles. ≥ 3 mm (normal) ou ≥ 5 mm (plancher chauffant). Évite les soulèvements par contrainte thermique ou mouvement.</p></div>
      <div class="lexique-item"><strong>Malaxeur lent</strong><p>Outil électrique de gâchage à vitesse réduite (500 tr/min maximum). Indispensable pour préparer le mortier-colle sans incorporer d'air.</p></div>
      <div class="lexique-item"><strong>Marouflage</strong><p>Action d'appuyer sur un carreau mural avec un mouvement de glissement/rotation pour assurer le contact colle/carreau ≥ 70%. Pour les murs et petits formats sol.</p></div>
      <div class="lexique-item"><strong>NF DTU 52.2</strong><p>Norme française régissant la pose collée des revêtements céramiques et assimilés pierres naturelles (sol et mur, intérieur et extérieur). Constituée de 5 parties (3 CCT + 1 CGM + 1 CCS).</p></div>
      <div class="lexique-item"><strong>NF EN 12004</strong><p>Norme européenne de classification des mortiers-colles (C), adhésifs (D) et colles réactives (R) pour carrelage. Définit les classes C1, C2, S1, S2, E, F, T, G.</p></div>
      <div class="lexique-item"><strong>Peau (formation de peau)</strong><p>Croûte sèche qui se forme en surface de la colle lorsque le temps ouvert est dépassé. Carreau non admis sur la peau : risque de décollement immédiat.</p></div>
      <div class="lexique-item"><strong>Pente</strong><p>Inclinaison du sol pour l'écoulement des eaux. Minimum : 1% en intérieur avec siphon / 1,5% en extérieur. Réalisée dans la chape ou le mortier-colle.</p></div>
      <div class="lexique-item"><strong>Plancher chauffant</strong><p>Plancher intégrant des tubes à eau chaude pour le chauffage. Impose : colle C2-S1/S2, mise en chauffe préalable, arrêt 2 jours avant pose, joint périphérique ≥ 5 mm.</p></div>
      <div class="lexique-item"><strong>Pose à joint nul</strong><p>Pose sans espace entre carreaux — INTERDITE. Même pour les carreaux rectifiés, le joint minimum est de 2 mm.</p></div>
      <div class="lexique-item"><strong>Primaire d'accrochage</strong><p>Produit appliqué avant la colle pour améliorer l'adhérence sur support lisse ou peu absorbant (béton poli, carrelage ancien).</p></div>
      <div class="lexique-item"><strong>Produit de cure</strong><p>Produit appliqué sur le béton frais pour limiter l'évaporation de l'eau et favoriser le durcissement. Doit être éliminé par grenaillage/sablage avant collage direct.</p></div>
      <div class="lexique-item"><strong>Rectifié</strong><p>Carreau dont les bords ont été taillés mécaniquement avec une précision ±0,25 mm. Permet des joints réduits (≥ 2 mm).</p></div>
      <div class="lexique-item"><strong>SEL</strong><p>Système d'Étanchéité Liquide. Appliqué sur les sols des locaux humides EB+ et EC. Seule forme liquide. Garantit l'étanchéité. Nécessite souvent avenant d'assurance.</p></div>
      <div class="lexique-item"><strong>Simple encollage</strong><p>Colle appliquée uniquement sur le support à la taloche, puis peignée à la spatule crantée. Le carreau est posé avant formation d'une peau. Admis pour petits et moyens formats.</p></div>
      <div class="lexique-item"><strong>Spatule crantée</strong><p>Outil de répartition de la colle créant des cordons réguliers. Son format (U3, U6, U9, demi-lune) détermine la consommation minimale de mortier-colle selon le format du carreau.</p></div>
      <div class="lexique-item"><strong>SPEC</strong><p>Système de Protection à l'Eau sous Carrelage. Appliqué sur les parois verticales humides. NE garantit PAS l'étanchéité mais rend le support admissible à la pose collée.</p></div>
      <div class="lexique-item"><strong>Temps ouvert</strong><p>Durée pendant laquelle la colle reste collante après application : 20 min (normal), 10 min (F rapide), 30 min (E allongé). Par temps chaud ou sur support poreux : temps réduit.</p></div>
      <div class="lexique-item"><strong>Tuilage</strong><p>Défaut d'aspect du carreau prenant une forme concave ou convexe après pose, causé par des variations d'humidité ou un double encollage inadapté.</p></div>
      <div class="lexique-item"><strong>Ventouse</strong><p>Outil de manutention à aspiration utilisé pour manipuler les carreaux de grand format (S &gt; 2 000 cm²) sans contact avec la face émaillée.</p></div>
    </div>
  </div>

  <!-- SÉCURITÉ -->
  <div id="carrelage-securite" class="sub-content">
    <div class="section-card">
      <h2>⛑️ Mémo Prévention & Sécurité — Carrelage</h2>
      <div class="securite-grid">
        <div class="securite-card"><span class="icon">🥽</span><h4>Protection des yeux</h4><p>Port de lunettes de protection obligatoire lors de la découpe et du sondage.</p></div>
        <div class="securite-card"><span class="icon">🧤</span><h4>Protection des mains</h4><p>Gants résistants aux coupures pour la manipulation des carreaux et produits chimiques.</p></div>
        <div class="securite-card"><span class="icon">👂</span><h4>Protection auditive</h4><p>Bouchons ou casque antibruit lors de l'utilisation de la scie à carrelage.</p></div>
        <div class="securite-card"><span class="icon">😷</span><h4>Protection respiratoire</h4><p>Masque anti-poussière P2 lors des découpes (silice cristalline = cancérogène).</p></div>
        <div class="securite-card"><span class="icon">🦺</span><h4>Genouillères</h4><p>Protection des genoux lors de la pose au sol. Prévention des TMS (troubles musculo-squelettiques).</p></div>
        <div class="securite-card"><span class="icon">⚡</span><h4>Outils électriques</h4><p>Vérifier que la scie à eau est correctement mise à la terre. Éviter tout contact eau/électricité.</p></div>
        <div class="securite-card"><span class="icon">💊</span><h4>Risque chimique</h4><p>Les colles et ciments sont irritants et caustiques. Lire les FDS (Fiches de Données Sécurité).</p></div>
        <div class="securite-card"><span class="icon">🪨</span><h4>Charges lourdes</h4><p>Utiliser des aides à la manutention pour les grands formats. Poids max : 25 kg par personne.</p></div>
      </div>
      <div class="info-box red"><div class="icon">⚠️</div><div class="content"><p><strong>SILICE CRISTALLINE :</strong> La poussière de coupe des carreaux contient de la silice cristalline, substance classée cancérogène. Toujours couper avec de l'eau et porter un masque FFP2 ou FFP3.</p></div></div>
      <div class="info-box orange"><div class="icon">🏗️</div><div class="content"><p><strong>TRAVAIL EN HAUTEUR :</strong> Pour les revêtements muraux en hauteur, utiliser un échafaudage conforme. Ne jamais travailler sur un escabeau instable.</p></div></div>
    </div>
  </div>

  <!-- QUIZ -->
  <div id="carrelage-quiz" class="sub-content">
    <div class="section-card">
      <h2>🎯 Questionnaire d'Acquis — Carrelage & Faïence</h2>
      <p style="margin-bottom:20px;">Ce questionnaire mixte (simple → complexe) vérifie ta compréhension du carrelage. <strong>10 questions</strong> — Score final en %.</p>
    </div>
    <div class="quiz-container" id="quiz-carrelage">
      <!-- Q1 -->
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">1</div><div class="q-text">Qu'est-ce que la faïence ?</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="cq1" value="a"> a) Un carreau en grès cérame très résistant</label></li>
          <li><label><input type="radio" name="cq1" value="b"> b) Un carreau en céramique poreuse émaillée, utilisé principalement en mur</label></li>
          <li><label><input type="radio" name="cq1" value="c"> c) Une colle à carrelage</label></li>
          <li><label><input type="radio" name="cq1" value="d"> d) Un type de joint souple</label></li>
        </ul>
        <div class="answer-feedback" id="cq1-feedback"></div>
      </div>
      <!-- Q2 -->
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">2</div><div class="q-text">Que signifie le SPEC ?</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="cq2" value="a"> a) Système de Protection à l'Eau sous Carrelage</label></li>
          <li><label><input type="radio" name="cq2" value="b"> b) Système de Pose En Carrelage</label></li>
          <li><label><input type="radio" name="cq2" value="c"> c) Système d'Étanchéité Liquide pour Carreaux</label></li>
          <li><label><input type="radio" name="cq2" value="d"> d) Support Pour Encollage Carrelage</label></li>
        </ul>
        <div class="answer-feedback" id="cq2-feedback"></div>
      </div>
      <!-- Q3 -->
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">3</div><div class="q-text">Vrai ou Faux : Le SEL s'applique sur les parois verticales (murs) pour assurer l'étanchéité.</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="cq3" value="a"> ✅ Vrai</label></li>
          <li><label><input type="radio" name="cq3" value="b"> ❌ Faux</label></li>
        </ul>
        <div class="answer-feedback" id="cq3-feedback"></div>
      </div>
      <!-- Q4 -->
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">4</div><div class="q-text">Une colle C2 S1 est utilisée pour :</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="cq4" value="a"> a) Les travaux courants en intérieur sur béton</label></li>
          <li><label><input type="radio" name="cq4" value="b"> b) Les carreaux de grands formats, planchers chauffants et façades</label></li>
          <li><label><input type="radio" name="cq4" value="c"> c) Uniquement les zones sèches</label></li>
          <li><label><input type="radio" name="cq4" value="d"> d) La rénovation sur petites surfaces</label></li>
        </ul>
        <div class="answer-feedback" id="cq4-feedback"></div>
      </div>
      <!-- Q5 -->
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">5</div><div class="q-text">Quel écart de planéité est toléré sous la règle de 2 mètres lors d'un contrôle de carrelage ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="cq5" value="a"> a) 2 mm</label></li>
          <li><label><input type="radio" name="cq5" value="b"> b) 5 mm</label></li>
          <li><label><input type="radio" name="cq5" value="c"> c) 10 mm</label></li>
          <li><label><input type="radio" name="cq5" value="d"> d) 15 mm</label></li>
        </ul>
        <div class="answer-feedback" id="cq5-feedback"></div>
      </div>
      <!-- Q6 -->
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">6</div><div class="q-text">Dans la classification UPEC, que signifie la lettre "E" ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="cq6" value="a"> a) Entretien</label></li>
          <li><label><input type="radio" name="cq6" value="b"> b) Eau</label></li>
          <li><label><input type="radio" name="cq6" value="c"> c) Électricité</label></li>
          <li><label><input type="radio" name="cq6" value="d"> d) Extérieur</label></li>
        </ul>
        <div class="answer-feedback" id="cq6-feedback"></div>
      </div>
      <!-- Q7 -->
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">7</div><div class="q-text">Pourquoi le délai de 28 jours est-il important avant la pose d'un SEL sur dalle béton fraîche ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="cq7" value="a"> a) Pour que la dalle atteigne sa résistance maximale et un taux d'humidité acceptable</label></li>
          <li><label><input type="radio" name="cq7" value="b"> b) Pour des raisons administratives uniquement</label></li>
          <li><label><input type="radio" name="cq7" value="c"> c) Pour éviter la condensation en surface</label></li>
          <li><label><input type="radio" name="cq7" value="d"> d) C'est une règle de sécurité liée au travail en hauteur</label></li>
        </ul>
        <div class="answer-feedback" id="cq7-feedback"></div>
      </div>
      <!-- Q8 -->
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">8</div><div class="q-text">Vrai ou Faux : Les plaques de plâtre hydrofuges suffisent à elles seules à assurer l'étanchéité d'une douche.</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="cq8" value="a"> ✅ Vrai</label></li>
          <li><label><input type="radio" name="cq8" value="b"> ❌ Faux</label></li>
        </ul>
        <div class="answer-feedback" id="cq8-feedback"></div>
      </div>
      <!-- Q9 MISE EN SITUATION -->
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">9</div><div class="q-text">Mise en situation</div><span class="q-level hard">🔴 Difficile</span></div>
        <div class="scenario-box">
          <h4>🏗️ Scénario :</h4>
          <p>Tu dois poser du carrelage format 60x120 cm dans une douche à l'italienne (EB+) sur une dalle béton de 15 jours. Quels sont les 3 points critiques à vérifier AVANT de commencer ?</p>
        </div>
        <textarea class="open-answer" id="cq9-answer" placeholder="Écris ta réponse ici..."></textarea>
        <button class="btn-check" onclick="checkOpen('cq9')">Voir la correction 📋</button>
        <div class="answer-feedback" id="cq9-feedback"></div>
      </div>
      <!-- Q10 -->
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">10</div><div class="q-text">Quelle colle choisir pour poser du carrelage extérieur sur une terrasse exposée au gel ?</div><span class="q-level hard">🔴 Difficile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="cq10" value="a"> a) C1 (mortier-colle normal)</label></li>
          <li><label><input type="radio" name="cq10" value="b"> b) D1 (adhésif en dispersion)</label></li>
          <li><label><input type="radio" name="cq10" value="c"> c) C2 S1 ou C2 S2 (mortier-colle amélioré déformable)</label></li>
          <li><label><input type="radio" name="cq10" value="d"> d) D2 (adhésif amélioré)</label></li>
        </ul>
        <div class="answer-feedback" id="cq10-feedback"></div>
      </div>

      <div class="quiz-footer">
        <button class="btn-submit" onclick="submitQuiz('carrelage', 10)">🎯 Calculer mon score !</button>
        <div class="score-display" id="score-carrelage"></div>
      </div>
    </div>
  </div>
</div><!-- END CARRELAGE -->

<!-- ================================================== -->
<!-- ONGLET 2 : PEINTURE -->
<!-- ================================================== -->
<div id="peinture" class="tab-content">
  <div class="sub-tabs">
    <button class="sub-tab-btn active" onclick="showSub('peinture', 'revision', this)">📖 Révision générale</button>
    <button class="sub-tab-btn" onclick="showSub('peinture', 'controle', this)">✅ Contrôle travaux</button>
    <button class="sub-tab-btn" onclick="showSub('peinture', 'lexique', this)">📝 Lexique</button>
    <button class="sub-tab-btn" onclick="showSub('peinture', 'securite', this)">⛑️ Mémo sécurité</button>
    <button class="sub-tab-btn" onclick="showSub('peinture', 'quiz', this)">🎯 Questionnaire d'acquis</button>
  </div>
  <div id="peinture-revision" class="sub-content active">
    <div class="section-card">
      <h2>🖌️ Peinture — Révision Générale</h2>
      <div class="img-grid">
        <div class="img-example"><img src="https://images.unsplash.com/photo-1562259929-b4e1fd3aef09?w=400&q=80" alt="Peinture mur"><div class="caption">📸 Peinture intérieure au rouleau</div></div>
        <div class="img-example"><img src="https://images.unsplash.com/photo-1558618666-fcd25c85cd64?w=400&q=80" alt="Désordres peinture"><div class="caption">📸 Préparation du support</div></div>
      </div>
      <h3>🔹 Composition d'une peinture</h3>
      <table>
        <tr><th>Composant</th><th>Rôle</th><th>Exemple</th></tr>
        <tr><td>Liant</td><td>Fixe les pigments et charges au support, forme le film</td><td>Acrylique, alkyde, époxy</td></tr>
        <tr><td>Pigment</td><td>Donne la couleur et l'opacité</td><td>TiO₂ (blanc), oxydes de fer</td></tr>
        <tr><td>Charge (matière de charge)</td><td>Donne du corps, améliore la tenue, réduit le coût. N'apporte pas de couleur.</td><td>Carbonate de calcium (CaCO₃), talc, kaolin, baryte</td></tr>
        <tr><td>Solvant / diluant</td><td>Fluidifie la peinture pour l'application</td><td>Eau (acrylique), white-spirit (glycéro)</td></tr>
        <tr><td>Additifs</td><td>Améliore propriétés spécifiques</td><td>Siccatif (séchage), fongicide, anti-mousse, épaississant</td></tr>
      </table>
      <div class="info-box blue"><div class="icon">💡</div><div class="content"><p><strong>Charges vs Pigments :</strong> Les pigments colorent et opacifient. Les charges (ex : carbonate de calcium) donnent du corps à la peinture et en ajustent les propriétés mécaniques, sans apporter de couleur ni d'opacité.</p></div></div>

      <h3>🔹 Les types de peinture</h3>
      <table>
        <tr><th>Type</th><th>Base / Solvant</th><th>Domaine d'application</th><th>Propriétés clés</th><th>Séchage</th></tr>
        <tr><td><strong>Acrylique</strong></td><td>Émulsion aqueuse — résine acrylique</td><td>Tous supports intérieurs, toutes pièces</td><td>Faible odeur, séchage rapide, lavable, faibles COV</td><td>Toucher 1-2h / complet 6-8h</td></tr>
        <tr><td><strong>Glycérophtalique</strong></td><td>Solvant organique — résine alkyde</td><td>Tous supports int. et ext., finitions intérieures et extérieures, bois, métal</td><td>Durable, aspect lisse et brillant, excellent pouvoir couvrant, forte odeur</td><td>Toucher 6-8h / complet 24h</td></tr>
        <tr><td><strong>Alkyde</strong></td><td>Eau ou solvant — résine alkyde</td><td>Tous supports int. et ext.</td><td>Très résistante chocs, frottements, humidité. Aspect tendu régulier</td><td>Toucher 4-6h / complet 12-24h</td></tr>
        <tr><td><strong>Thixotrope</strong></td><td>Eau — acétate de vinyle + charges</td><td>Tous types de support poreux et farineux</td><td>Épaisse, ne coule pas. Fort pouvoir couvrant. Accrochage sur tous supports</td><td>Variable selon formulation</td></tr>
        <tr><td><strong>Vinylique</strong></td><td>Dispersion aqueuse — acétate de vinyle</td><td>Supports poreux et farineux</td><td>Résistance à l'eau, forte résistance aux fissures et craquelures, reste flexible</td><td>Rapide 1-2h toucher / 6-8h complet</td></tr>
        <tr><td><strong>Lasure</strong></td><td>Émulsion aqueuse</td><td>Bois extérieur (menuiseries, bardages, volets)</td><td>Semi-transparente, laisse respirer la surface, protection UV et intempéries</td><td>30 min à 4h selon formulation</td></tr>
        <tr><td><strong>Laque</strong></td><td>Émulsion ou dispersion aqueuse</td><td>Tous supports int., menuiseries, boiseries</td><td>Très résistante chocs, rayures, usure. Rendu très lisse et tendu. Brillant, satiné ou velouté</td><td>Moyen 4-6h toucher / 12-24h complet</td></tr>
        <tr><td><strong>Vernis</strong></td><td>Dispersion aqueuse</td><td>Tous supports</td><td>Protège la surface, ne s'imprègne pas dans le support. Brillant, satiné ou mat</td><td>Moyen 4-6h toucher / 12-24h complet</td></tr>
        <tr><td><strong>Époxy</strong></td><td>Résine époxy — 2 composants (durcisseur)</td><td>Sols industriels, garages, zones humides</td><td>Très résistante aux produits chimiques et à l'abrasion. Haute teneur en COV.</td><td>Variable selon formulation</td></tr>
        <tr><td><strong>Polyuréthane</strong></td><td>Résine PU + durcisseur + solvant chimique</td><td>Surfaces extérieures exposées, bois, métal</td><td>Flexible, très résistante à l'usure et aux intempéries</td><td>Variable</td></tr>
        <tr><td><strong>Anticorrosion</strong></td><td>Émulsion ou solvant + zinc</td><td>Surfaces métalliques</td><td>Protège contre la rouille et l'oxydation</td><td>Variable</td></tr>
        <tr><td><strong>Intumescente</strong></td><td>Émulsion aqueuse</td><td>Protection incendie des structures</td><td>Gonfle sous l'effet de la chaleur pour créer une barrière isolante</td><td>Variable</td></tr>
        <tr><td><strong>Microporeuse</strong></td><td>Émulsion aqueuse</td><td>Façades, supports extérieurs</td><td>Imperméable à l'eau liquide, perméable à la vapeur d'eau (support respire)</td><td>Variable</td></tr>
        <tr><td><strong>Hydrofuge</strong></td><td>Émulsion ou solvant</td><td>Façades, supports poreux extérieurs</td><td>Résiste à l'eau, protège contre l'humidité</td><td>Variable</td></tr>
        <tr><td><strong>Peintures décoratives</strong></td><td>Émulsion aqueuse</td><td>Décorations intérieures</td><td>Effets : sablé, béton, métallisé, nacré, tadelakt</td><td>Variable</td></tr>
      </table>

      <h3>🔹 Séchage d'une peinture — Les 3 étapes</h3>
      <div class="info-box blue"><div class="icon">⏱️</div><div class="content"><p>Le séchage correspond à la modification du liant qui passe d'un état pâteux à un état solide (formation d'un film dur). Il se déroule en 2 grandes phases : <strong>évaporation des produits volatils</strong> puis <strong>durcissement du film</strong>.</p></div></div>
      <div class="controle-phase">
        <div class="check-item"><span class="check-icon">1️⃣</span> <strong>Hors poussière :</strong> La poussière n'accroche plus sur le support (film encore mou mais non collant)</div>
        <div class="check-item"><span class="check-icon">2️⃣</span> <strong>Sec au toucher :</strong> On peut mettre la main sans risque de coller</div>
        <div class="check-item"><span class="check-icon">3️⃣</span> <strong>Sec recouvrable :</strong> On peut passer une autre couche sans détremper la couche précédente</div>
      </div>
      <div class="info-box orange"><div class="icon">⚠️</div><div class="content"><p><strong>Facteurs influençant le séchage :</strong> Temps froid → évaporation lente, risque de gel des peintures acryliques. Temps chaud → évaporation trop rapide, risque de mauvaise adhérence. Produits périmés et mauvaise préparation allongent également les temps de séchage.</p></div></div>

      <h3>🔹 Conditions d'intervention — Le subjectile</h3>
      <div class="info-box red"><div class="icon">🏗️</div><div class="content"><p><strong>Bâtiment hors d'eau, hors d'air obligatoire</strong> avant toute intervention du peintre. Température entre <strong>8°C et 35°C</strong>, hygrométrie inférieure à <strong>70%</strong>.</p></div></div>
      <p>Un support (subjectile) doit être : <span style="background:#FFF3CD;padding:3px 8px;border-radius:5px;font-weight:bold;">SAIN — SEC — PROPRE — PLAN — LISSE — COHÉSIF</span></p>
      <p style="margin-top:10px;">Le support doit être dépourvu de : taches d'humidité, moisissures, pulvérulence, efflorescence, salpêtre, bistre, huile, graisses, traces de bois ou métal, encre, crayon gras, graffiti.</p>
      <div class="info-box blue"><div class="icon">📐</div><div class="content"><p><strong>Tolérance de planéité (DTU 59.1 art. 5) :</strong> écart max <strong>1 mm</strong> sous règle de 20 cm et <strong>5 mm</strong> sous règle de 2 m.</p></div></div>

      <h3>🔹 Les documents de référence</h3>
      <table>
        <tr><th>Document</th><th>Rôle</th></tr>
        <tr><td><strong>NF DTU 59.1</strong></td><td>Norme des travaux de peinture (feuil mince, semi-épais, épais). Définit les conditions de mise en œuvre, finitions A/B/C et les 8 méthodes de vérification (art. 8).</td></tr>
        <tr><td><strong>Fiche technique</strong></td><td>Infos produit (composition, propriétés), instructions d'application (préparation, temps de séchage, dilution), sécurité (EPI/EPC), impact environnemental.</td></tr>
        <tr><td><strong>FDS (Fiche de Données de Sécurité)</strong></td><td>Document obligatoire donnant des informations sur les substances chimiques du produit et les précautions d'utilisation.</td></tr>
        <tr><td><strong>FDES (Fiche de Déclaration Environnementale et Sanitaire)</strong></td><td>Présente les résultats de l'analyse du cycle de vie (ACV) du produit et la quantité de CO₂ émise.</td></tr>
      </table>
      <div class="info-box green"><div class="icon">💡</div><div class="content"><p><strong>À savoir :</strong> En l'absence de précision dans les pièces du marché, l'état de finition <strong>B (courant)</strong> est retenu. L'aspect retenu par défaut est le <strong>satiné (BS compris entre 10 et 45)</strong>. La mesure du brillant spéculaire doit être faite au plus tard dans un délai de <strong>3 mois</strong> après l'application.</p></div></div>

      <h3>🔹 Les propriétés d'une peinture</h3>
      <table>
        <tr><th>Propriété</th><th>Description</th></tr>
        <tr><td>🎨 Qualité esthétique</td><td>Degré de brillant spéculaire, couleur stable, pouvoir couvrant suffisant</td></tr>
        <tr><td>💧 Bonne étanchéité</td><td>Propriétés hydrofuges, quantité suffisante de liant (satiné, brillant)</td></tr>
        <tr><td>🔗 Bonne adhérence</td><td>Peinture non périmée, support correctement préparé, bons outils</td></tr>
        <tr><td>⏳ Tenue dans le temps</td><td>Application correcte, usage adapté au local (humide/sec), absence de désordres (farinage, décollement)</td></tr>
        <tr><td>🛡️ Fonctions</td><td>Esthétisme (décorer), Protection (feuil imperméable), Assainissement (antifongique)</td></tr>
      </table>

      <h3>🔹 Les COV — Composés Organiques Volatils</h3>
      <div class="info-box red"><div class="icon">☠️</div><div class="content"><p>Les <strong>COV</strong> sont des solvants libérés lors du séchage de la peinture. En s'évaporant, ils participent à la formation de gaz à effet de serre (ozone). Une législation encadre leur teneur dans les produits pour préserver la santé et l'environnement. <strong>Les peintures aqueuses (acryliques) ont une faible teneur en COV</strong>, contrairement aux glycérophtaliques.</p></div></div>

      <h3>🔹 Le brillant spéculaire</h3>
      <p>Le <strong>brillant spéculaire</strong> est la mesure physique de la réflexion de la lumière sur un film peint, exprimée en <strong>unités de brillance (GU — Gloss Units)</strong> mesurées avec un glossmètre à 60°. On distingue :</p>
      <table>
        <tr><th>Aspect</th><th>Brillance (GU à 60°)</th><th>Usage courant</th></tr>
        <tr><td>Mat</td><td>&lt; 10 GU</td><td>Plafonds, murs de chambre</td></tr>
        <tr><td>Velours / Satiné mat</td><td>10 à 25 GU</td><td>Séjour, couloir</td></tr>
        <tr><td>Satiné</td><td>25 à 60 GU</td><td>Cuisine, salle de bain</td></tr>
        <tr><td>Brillant</td><td>60 à 85 GU</td><td>Boiseries, menuiseries</td></tr>
        <tr><td>Très brillant (laqué)</td><td>&gt; 85 GU</td><td>Mobilier, portes lacquées</td></tr>
      </table>
      <div class="info-box orange"><div class="icon">💡</div><div class="content"><p><strong>À retenir :</strong> Plus une peinture est brillante, plus elle est <strong>lavable et résistante</strong>, mais plus elle révèle les défauts du support. Une finition mate est plus couvrante en apparence mais masque les irrégularités.</p></div></div>

      <h3>🔹 Niveaux de finition (NF DTU 59.1)</h3>
      <div class="info-box red"><div class="icon">⚠️</div><div class="content"><p>La norme NF DTU 59.1 définit <strong>3 niveaux de finition</strong> uniquement : <strong>A (Soigné)</strong>, <strong>B (Courant)</strong> et <strong>C (Élémentaire)</strong>. Il n'existe pas de niveau P1/P2/P3/P4 dans cette norme.</p></div></div>
      <table>
        <tr><th>Niveau</th><th>Désignation</th><th>Description</th><th>Usage</th></tr>
        <tr><td><span class="badge green">Finition A</span></td><td>Soigné</td><td>Préparation soignée du support, enduits, ponçage inter-couches (égrenage), finition haut de gamme. Observation en lumière rasante admise.</td><td>Locaux haut de gamme, ERP, bâtiments représentatifs</td></tr>
        <tr><td><span class="badge blue">Finition B</span></td><td>Courant</td><td>Préparation correcte, enduits de rebouchage localisés, finition standard 2 couches. Observation en lumière normale.</td><td>Logements, bureaux standard</td></tr>
        <tr><td><span class="badge orange">Finition C</span></td><td>Élémentaire</td><td>Préparation minimale, application directe. Tolérances larges. Locaux à usage non résidentiel ou technique.</td><td>Caves, parkings, locaux techniques, chantiers temporaires</td></tr>
      </table>

      <h3>🔹 Les différents types d'enduits</h3>
      <table>
        <tr><th>Type d'enduit</th><th>Description</th><th>Usage</th></tr>
        <tr><td>Enduit de rebouchage</td><td>Pâte épaisse pour combler trous et fissures localisées</td><td>Réparations ponctuelles</td></tr>
        <tr><td>Enduit de lissage</td><td>Enduit fin appliqué en couche mince pour lisser une surface</td><td>Finition A sur murs/plafonds</td></tr>
        <tr><td>Enduit de garnissage</td><td>Enduit épais pour rattraper les irrégularités du support</td><td>Supports très irréguliers</td></tr>
        <tr><td>Enduit à la chaux</td><td>Enduit minéral naturel à base de chaux</td><td>Supports anciens, rénovation</td></tr>
        <tr><td>Enduit en poudre</td><td>Enduit à gâcher avec de l'eau</td><td>Usage général, chantier</td></tr>
        <tr><td>Enduit en pâte</td><td>Prêt à l'emploi, séchage par évaporation</td><td>Petits travaux, retouches</td></tr>
        <tr><td>Enduit de finition (micro-enduit)</td><td>Enduit très fin (< 1 mm), aspect béton ciré</td><td>Décoration, sols et murs</td></tr>
        <tr><td>Enduit armé</td><td>Enduit renforcé d'un treillis fibre de verre</td><td>Fissures, ITE, zones sollicitées</td></tr>
      </table>

      <h3>🔹 Travaux préparatoires</h3>
      <p>Les travaux préparatoires rendent le <strong>subjectile</strong> apte à recevoir les travaux d'apprêts ou de revêtement de finition : mur propre, sans aspérités ni désordres.</p>
      <table>
        <tr><th>🧹 SURFACES PROPRES</th><th>📏 SURFACES UNIES</th><th>🆕 SURFACES NOUVELLES</th></tr>
        <tr><td>Laver (eau)</td><td>Égrener</td><td>Décaper</td></tr>
        <tr><td>Lessiver (eau + savon)</td><td>Brosser</td><td>Arracher</td></tr>
        <tr><td>Épousseter</td><td>Gratter</td><td>Brûler</td></tr>
        <tr><td>Dégraisser</td><td>Ouvrir les fissures</td><td>Décoller</td></tr>
        <tr><td></td><td>Poncer</td><td>Entoiler</td></tr>
      </table>
      <h3>🔹 Les types de fissures</h3>
      <table>
        <tr><th>Type</th><th>Largeur</th><th>Causes</th><th>Solution</th></tr>
        <tr><td><span class="badge green">Microfissures</span></td><td>&lt; 0,2 mm</td><td>Mauvais dosage de l'eau, séchage trop rapide, épaisseur d'enduit trop importante</td><td>Grattage, ouverture, rebouchage + impression fixante + dégrossissage</td></tr>
        <tr><td><span class="badge orange">Fissures</span></td><td>0,2 à 2 mm</td><td>Mouvement du bâtiment, mauvaise préparation des points singuliers (joints plaques, jonctions)</td><td>Ouvrir les fissures, reboucher + poser bande de calicot</td></tr>
        <tr><td><span class="badge red">Lézardes</span></td><td>&gt; 2 mm</td><td>Mouvement du bâtiment, défauts de construction</td><td>Faire appel à un professionnel du gros œuvre — ne peut être traité par le peintre seul</td></tr>
        <tr><td><span class="badge orange">Faïençage</span></td><td>Petites mailles</td><td>Mauvais séchage des matériaux, produits périmés</td><td>Grattage, ouverture si nécessaire, rebouchage + impression fixante + dégrossissage</td></tr>
      </table>

      <h3>🔹 Travaux d'apprêts</h3>
      <div class="info-box orange"><div class="icon">⭐</div><div class="content"><p>Ce sont les travaux <strong>les plus difficiles et les plus importants</strong>. Ils révèlent les qualités techniques et professionnelles du peintre. De ces travaux dépendent la qualité et l'aspect final.</p></div></div>
      <table>
        <tr><th>🧱 SURFACES NON POREUSES / POREUSES</th><th>📏 SURFACES UNIES</th><th>✨ SURFACES LISSES</th></tr>
        <tr><td>Imprimer (spécifique ou non)</td><td>Reboucher</td><td>Entoiler</td></tr>
        <tr><td>Primaire d'accrochage</td><td>Ébaucher</td><td>Tapisser</td></tr>
        <tr><td></td><td>Dégrossis</td><td>Enduire (non repassé / repassé)</td></tr>
        <tr><td></td><td>Ratisser</td><td>Enduire au mixte</td></tr>
        <tr><td></td><td>Réviser</td><td></td></tr>
        <tr><td></td><td>Dégrossissage</td><td></td></tr>
      </table>
      <h3>🔹 Les différents travaux d'enduisage</h3>
      <table>
        <tr><th>Opération</th><th>Description</th></tr>
        <tr><td><strong>Rebouchage</strong></td><td>Rebouche les trous, aspérités et fissures</td></tr>
        <tr><td><strong>Dégrossissage</strong></td><td>Garnit les aspérités et imperfections du support en couche épaisse</td></tr>
        <tr><td><strong>Enduit mixte</strong></td><td>Préparation de fonds recevant un décor en peinture ou enduit décoratif. Principalement pour supports bois (enduit gras)</td></tr>
        <tr><td><strong>Ratissage</strong></td><td>Applique sur une surface imprimée ou peinte un enduit sans épaisseur. Permet de rendre la surface lisse</td></tr>
        <tr><td><strong>Enduit non repassé</strong></td><td>Enduit qui comporte une couche continue d'enduit garnissant, appliqué en une seule passe</td></tr>
        <tr><td><strong>Enduit repassé</strong></td><td>Enduisage en 2 passes avec ponçage entre les deux couches pour une surface lisse et bien plane</td></tr>
        <tr><td><strong>Entoilage</strong></td><td>Application d'une toile sur la surface avant enduisage. Renforce la surface et évite que les fissures ne se développent</td></tr>
      </table>
      <h3>🔹 L'impression (apprêt) — fonctions</h3>
      <table>
        <tr><th>Fonction</th><th>Description</th></tr>
        <tr><td>🛡️ <strong>Isolante</strong></td><td>Bloque les remontées de matières (bistre, bitume, taches)</td></tr>
        <tr><td>💧 <strong>Hydrofuge</strong></td><td>Imperméable, bloque la pénétration de l'humidité</td></tr>
        <tr><td>💪 <strong>Fixante</strong></td><td>Durcit le support poreux, pulvérulent ou sensible à l'eau</td></tr>
      </table>
      <div class="info-box blue"><div class="icon">💡</div><div class="content"><p><strong>Primaire d'accrochage :</strong> Fonction anticorrosive sur les métaux. Rôle d'accrochage sur les supports non poreux (carrelage, matières plastiques). Peut s'appliquer sur carrelage en cas de rénovation de salle de bain.</p></div></div>

      <h3>🔹 Travaux de finition</h3>
      <p>Les travaux de finition apportent la touche finale du décor après préparation et apprêtage. Ils s'exécutent en <strong>3 parties</strong> :</p>
      <div class="controle-phase">
        <div class="check-item"><span class="check-icon">1️⃣</span> <strong>Couche intermédiaire :</strong> Première couche de finition appliquée sur une surface prête à recevoir la finition</div>
        <div class="check-item"><span class="check-icon">2️⃣</span> <strong>Révision (Finition A uniquement) :</strong> Retouche la surface après l'impression ou la couche intermédiaire par application d'enduit localisé</div>
        <div class="check-item"><span class="check-icon">3️⃣</span> <strong>Couche de finition :</strong> Donne l'aspect final. Doit être identique à la couche intermédiaire</div>
      </div>
      <h3>🔹 Les finitions décoratives et enduits spéciaux</h3>
      <table>
        <tr><th>Produit</th><th>Composition</th><th>Propriétés / Usage</th></tr>
        <tr><td><strong>Stucco / Stuc</strong></td><td>Chaux ou plâtre + poudre de marbre, brique ou sable finement broyés</td><td>Effets décoratifs marbrés. Utilisation intérieure et extérieure</td></tr>
        <tr><td><strong>Tadelakt</strong></td><td>Chaux de Marrakech + eau de chaux + poudre de marbre + savon noir</td><td>Étanche et fongicide. Idéal pour pièces d'eau (douches, salles de bain)</td></tr>
        <tr><td><strong>Marmorino</strong></td><td>Chaux grasse + poudre de marbre (moins épais que le Tadelakt)</td><td>Bactéricide, hydrofugé et fongicide</td></tr>
        <tr><td><strong>Pâte Idéal / Comus</strong></td><td>Enduit décoratif à ferrage</td><td>Revêtements structurés ou aspect Stucco. Lisse et égalise les surfaces bois</td></tr>
        <tr><td><strong>Novastuc</strong></td><td>Résines acryliques + chaux</td><td>Effet marbré. Pièces sèches et humides sans projection d'eau</td></tr>
        <tr><td><strong>Micro-enduit / Béton ciré</strong></td><td>Ciment + résine (très fin, &lt;1mm)</td><td>Aspect béton ciré ou pierre. Sol et mur. Application à la taloche.</td></tr>
      </table>
      <h3>🔹 Essais et vérifications — Surface de référence</h3>
      <div class="info-box green"><div class="icon">🔍</div><div class="content"><p>La <strong>surface de référence</strong> est une zone représentative du bâtiment réalisée selon les spécifications contractuelles. Elle sert de modèle avant de poursuivre sur l'ensemble du projet. Elle est <strong>conservée par le maître d'ouvrage</strong> jusqu'à la réception. L'exécution totale des travaux ne peut se faire qu'après acceptation de cette surface. La vérification de conformité s'évalue selon <strong>8 méthodes (DTU 59.1 art. 8)</strong>.</p></div></div>
      <table>
        <tr><th>Outil</th><th>Usage</th><th>Avantage</th></tr>
        <tr><td>Pinceau plat</td><td>Découpes, angles, petites surfaces</td><td>Précision</td></tr>
        <tr><td>Rouleau laine</td><td>Grandes surfaces mates</td><td>Rapidité, aspect velouté</td></tr>
        <tr><td>Rouleau mousse</td><td>Surfaces lisses satinées ou brillantes</td><td>Finition lisse</td></tr>
        <tr><td>Pistolet airless</td><td>Grandes surfaces, boiseries en série</td><td>Rapidité, régularité</td></tr>
        <tr><td>Spalter</td><td>Laques, effets décoratifs</td><td>Finition très lisse</td></tr>
      </table>
      <h3>🔹 Désordres en peinture et solutions</h3>
      <div class="disorder-card">
        <h4>🔴 Cloquage / Bullage</h4>
        <p><strong>Cause :</strong> Humidité sous le film, peinture appliquée sur support trop humide ou en plein soleil.</p>
        <div class="solution"><strong>✅ Solution :</strong> Gratter les zones cloquées, traiter la cause d'humidité, laisser sécher, reprimer et repeindre. Éviter d'appliquer par T° > 30°C.</div>
      </div>
      <div class="disorder-card">
        <h4>🔴 Farinage</h4>
        <p><strong>Cause :</strong> Dégradation du liant en surface, peinture ancienne ou exposée aux UV. La peinture saupoudre à la surface.</p>
        <div class="solution"><strong>✅ Solution :</strong> Brosser énergiquement, appliquer un fixateur/primaire pénétrant, puis repeindre avec une peinture adaptée.</div>
      </div>
      <div class="disorder-card">
        <h4>🔴 Fissuration / craquelage</h4>
        <p><strong>Cause :</strong> Vieillissement, manque de flexibilité du film, support fissuré, sous-couche incompatible.</p>
        <div class="solution"><strong>✅ Solution :</strong> Décaper, enduire et poncer, appliquer un primaire adapté. Si fissure active : traiter avec bande à joint ou enduit armé.</div>
      </div>
      <div class="disorder-card">
        <h4>🔴 Décollement / pelage</h4>
        <p><strong>Cause :</strong> Support mal préparé (gras, poussiéreux), mauvais primaire, ou incompatibilité des couches.</p>
        <div class="solution"><strong>✅ Solution :</strong> Décaper entièrement les zones décollées, nettoyer et dégraisser le support, reprimer et peindre par couches compatibles.</div>
      </div>
      <div class="disorder-card">
        <h4>🔴 Coulures / traces de pinceau</h4>
        <p><strong>Cause :</strong> Peinture trop diluée, surcharge au pinceau ou rouleau, mauvaise technique d'application.</p>
        <div class="solution"><strong>✅ Solution :</strong> Poncer les coulures après séchage, repasser une couche en respectant le bon dosage de dilution et la technique croisée.</div>
      </div>
      <div class="disorder-card">
        <h4>🔴 Moisissures (champignons)</h4>
        <p><strong>Cause :</strong> Humidité chronique, condensation, pont thermique, manque de ventilation.</p>
        <div class="solution"><strong>✅ Solution :</strong> Traiter avec un fongicide/antifongique, laisser agir, rincer, puis appliquer une peinture antifongique. Traiter la cause : ventilation, isolation.</div>
      </div>
      <div class="disorder-card">
        <h4>🔴 Auréoles / taches de reprise</h4>
        <p><strong>Cause :</strong> Reprise de travail trop longue, peinture partiellement sèche, variations de température.</p>
        <div class="solution"><strong>✅ Solution :</strong> Reboucher la zone, poncer légèrement, repasser une couche uniforme sur toute la surface du pan de mur.</div>
      </div>
    </div>
  </div>
  <div id="peinture-controle" class="sub-content">
    <div class="section-card">
      <h2>✅ Contrôle des Travaux — Peinture</h2>
      <div class="controle-phase"><h3>🔵 AVANT</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Support propre, sec, sain (test de la bande adhésive pour vérifier l'adhérence)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Contrôler le taux d'humidité du support (≤ 5% en général)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Vérifier la planéité et reboucher les trous et fissures</div>
        <div class="check-item"><span class="check-icon">☑️</span> Choisir la peinture selon le niveau de finition demandé (P1 à P4)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Vérifier compatibilité sous-couche / peinture de finition</div>
        <div class="check-item"><span class="check-icon">☑️</span> Protéger les zones non peintes (plinthes, sols, vitrages) avec du scotch et des bâches</div>
      </div>
      <div class="controle-phase"><h3>🟡 PENDANT</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Respecter le temps de séchage entre les couches (2h acrylique, 24h glycéro)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Appliquer les couches croisées (vertical puis horizontal)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Contrôler l'épaisseur du film humide avec peigne calibreur</div>
        <div class="check-item"><span class="check-icon">☑️</span> Éviter les courants d'air et T° extrêmes (travail entre 5°C et 30°C)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Mélanger bien le pot avant emploi et respecter le taux de dilution</div>
      </div>
      <div class="controle-phase"><h3>🟢 APRÈS</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Vérifier l'aspect : uniformité, absence de coulures, traces, auréoles</div>
        <div class="check-item"><span class="check-icon">☑️</span> Contrôler l'adhérence : test au quadrillage ou à la bande adhésive</div>
        <div class="check-item"><span class="check-icon">☑️</span> Vérifier la couverture (opacité) : pas de transparence ni de zones mal couvertes</div>
        <div class="check-item"><span class="check-icon">☑️</span> Conserver les restes de peinture (étiquetés) pour les retouches futures</div>
      </div>
    </div>
  </div>
  <div id="peinture-lexique" class="sub-content">
    <div class="section-card">
      <h2>📝 Lexique — Peinture</h2>
      <div class="lexique-item"><strong>Acrylique</strong><p>Peinture à base aqueuse séchant par évaporation de l'eau puis coalescence. Odeur faible, séchage rapide (2h). Faibles COV. Reprise impossible car séchage trop rapide.</p></div>
      <div class="lexique-item"><strong>Amiante</strong><p>Fibre minérale cancérogène présente dans les bâtiments construits avant 1997 (plafonds, colles, enduits, joints). Toute intervention nécessite une formation spécifique SS3/SS4 et des EPI dédiés. Interdiction formelle de toucher sans être formé.</p></div>
      <div class="lexique-item"><strong>Bistre</strong><p>Tache sombre d'origine organique (suie, humins) pouvant traverser les couches de peinture par migration. Nécessite une sous-couche isolante avant repeinture.</p></div>
      <div class="lexique-item"><strong>Brillance spéculaire (BS)</strong><p>Mesure physique de la réflexion de la lumière sur un film peint, exprimée en unités GU (Gloss Units) avec un glossmètre à 60°. De mat (&lt;10 GU) à très brillant (&gt;85 GU). Par défaut (marché sans précision) : satiné, BS entre 10 et 45. Mesure à faire dans les 3 mois après application.</p></div>
      <div class="lexique-item"><strong>Calicot</strong><p>Bande de toile légère collée sur une fissure avant enduisage pour la stabiliser et éviter qu'elle ne réapparaisse en surface.</p></div>
      <div class="lexique-item"><strong>Charge (matière de charge)</strong><p>Constituant minéral inerte (carbonate de calcium, talc, kaolin) influant sur le brillant, la souplesse, la cohésion et la porosité. Contrairement aux pigments, les charges n'apportent ni teinte ni opacité. Prix inférieur aux pigments, très utilisées dans les peintures « amateur ».</p></div>
      <div class="lexique-item"><strong>Cloquage</strong><p>Formation de bulles ou cloques sous le film de peinture, souvent due à l'humidité ou à une application sur support trop humide / en plein soleil.</p></div>
      <div class="lexique-item"><strong>Coalescence</strong><p>Mécanisme de séchage des peintures aqueuses (acryliques). Les particules de liant dispersées dans l'eau se rapprochent puis fusionnent pour former un film continu et cohésif. Nécessite une température minimale d'environ 5°C.</p></div>
      <div class="lexique-item"><strong>Consignation électrique</strong><p>Procédure obligatoire de mise hors tension et de condamnation d'un circuit électrique avant toute intervention. Sans consignation, ne pas intervenir sur ou près d'un réseau.</p></div>
      <div class="lexique-item"><strong>COV (Composés Organiques Volatils)</strong><p>Solvants libérés lors du séchage de la peinture. Participent à la formation d'ozone. Une législation encadre leur teneur. Les peintures aqueuses ont de faibles COV, les glycérophtaliques en ont de forts.</p></div>
      <div class="lexique-item"><strong>CREP (Constat de Risque d'Exposition au Plomb)</strong><p>Diagnostic obligatoire avant travaux sur des bâtiments construits avant 1949 pour détecter la présence de peintures au plomb. Risque de saturnisme, notamment pour les enfants.</p></div>
      <div class="lexique-item"><strong>Dilution</strong><p>Action d'ajouter de l'eau ou du solvant pour fluidifier la peinture avant application. Taux indiqué sur la fiche technique (généralement 5 à 10%).</p></div>
      <div class="lexique-item"><strong>Durcisseur</strong><p>Composant chimique ajouté à certaines peintures (époxy, polyuréthane) pour provoquer la réticulation du liant et obtenir un film très dur et résistant.</p></div>
      <div class="lexique-item"><strong>Efflorescence / Salpêtre</strong><p>Dépôts blanchâtres en surface d'un mur causés par la migration et la cristallisation de sels solubles. Signe d'humidité. À éliminer avant toute peinture.</p></div>
      <div class="lexique-item"><strong>Égrenage</strong><p>Léger ponçage (papier 220-320) entre deux couches pour éliminer les aspérités et améliorer l'adhérence. Obligatoire en finition A.</p></div>
      <div class="lexique-item"><strong>Entoilage</strong><p>Application d'une toile (armature textile) sur une surface avant enduisage pour la renforcer et éviter que les fissures ne se développent.</p></div>
      <div class="lexique-item"><strong>EPC (Équipement de Protection Collectif)</strong><p>Dispositif protégeant l'ensemble des travailleurs d'un chantier : garde-corps, filets de sécurité, balisage, aspiration des poussières à la source. Prioritaire sur les EPI.</p></div>
      <div class="lexique-item"><strong>EPI (Équipement de Protection Individuelle)</strong><p>Équipement porté par le travailleur pour se protéger des risques résiduels : masque, lunettes, gants, casque, chaussures de sécurité, harnais, gilet. À vérifier avant chaque prise de poste.</p></div>
      <div class="lexique-item"><strong>Extrait sec</strong><p>Pourcentage en masse (ou volume) des matières non volatiles restant sur le support après séchage complet. Un extrait sec élevé = grande quantité de matière utile. Détermine directement le rendement.</p></div>
      <div class="lexique-item"><strong>Faïençage</strong><p>Réseau de petites fissures en mailles sur un film de peinture ou enduit, dû à un mauvais séchage ou à des produits périmés.</p></div>
      <div class="lexique-item"><strong>Farinage</strong><p>Dépôt poudreux en surface d'une peinture ancienne dû à la dégradation du liant. Traitement : brossage énergique + fixateur + repeinture.</p></div>
      <div class="lexique-item"><strong>FDS (Fiche de Données de Sécurité)</strong><p>Document obligatoire donnant des informations sur les substances chimiques d'un produit et les précautions d'utilisation. Contient notamment le point éclair, les EPI requis et les consignes en cas d'accident.</p></div>
      <div class="lexique-item"><strong>FDES (Fiche de Déclaration Environnementale et Sanitaire)</strong><p>Document technique présentant les résultats de l'Analyse du Cycle de Vie (ACV) d'un produit et la quantité de CO₂ émise lors de son cycle de vie.</p></div>
      <div class="lexique-item"><strong>Feuil</strong><p>Film mince de peinture formé sur le support après séchage. Feuil humide = peinture fraîchement appliquée. Feuil sec = après séchage complet. La NF DTU 59.1 régit les travaux en feuil mince, semi-épais et épais.</p></div>
      <div class="lexique-item"><strong>Film sec</strong><p>Épaisseur de la peinture après séchage complet, mesurée en microns (µm).</p></div>
      <div class="lexique-item"><strong>Finition A / B / C (NF DTU 59.1)</strong><p>Les 3 niveaux officiels. A = Soigné (enduits, égrenage, lumière rasante admise). B = Courant (défauts d'épiderme admis, aspect poché). C = Élémentaire (1 couche, usage technique). Par défaut : Finition B.</p></div>
      <div class="lexique-item"><strong>Fixateur</strong><p>Produit pénétrant appliqué sur un support poreux ou friable pour le consolider (durcir) avant peinture. Peut aussi bloquer les taches (bistre, bitume).</p></div>
      <div class="lexique-item"><strong>Glycérophtalique</strong><p>Peinture à base de résine alkyde et de solvant organique (white-spirit). Très résistante, aspect lisse et brillant, forte odeur, fort taux de COV, séchage lent (24h), jaunit avec le temps.</p></div>
      <div class="lexique-item"><strong>Habilitation électrique</strong><p>Reconnaissance par l'employeur de la capacité d'un travailleur à effectuer des opérations sur ou près des installations électriques. Sans habilitation : interdiction d'intervenir.</p></div>
      <div class="lexique-item"><strong>Hors d'eau / Hors d'air</strong><p>État d'un bâtiment dont la toiture est posée (hors d'eau) et dont les menuiseries extérieures sont installées (hors d'air). Condition préalable indispensable avant l'intervention du peintre.</p></div>
      <div class="lexique-item"><strong>Hygrométrie (HR)</strong><p>Taux d'humidité relative de l'air, exprimé en %. Condition de mise en œuvre des peintures : HR inférieure à 70%. Une hygrométrie trop élevée entraîne des désordres (cloquage, mauvaise adhérence).</p></div>
      <div class="lexique-item"><strong>Lézarde</strong><p>Fissure structurelle de plus de 2mm. Ne peut pas être traitée par le peintre seul — nécessite l'intervention d'un professionnel du gros œuvre.</p></div>
      <div class="lexique-item"><strong>Liant</strong><p>Matière filmogène essentielle liant les pigments et charges entre eux et au support. Détermine l'aspect (mat, brillant, satiné). Types : émulsion aqueuse (acrylique, vinylique) ou solution solvantée (glycéro, alkyde).</p></div>
      <div class="lexique-item"><strong>Marmorino</strong><p>Enduit décoratif à base de chaux grasse et poudre de marbre. Bactéricide, hydrofugé, fongicide. Moins épais que le Tadelakt.</p></div>
      <div class="lexique-item"><strong>Microfissures</strong><p>Fissures inférieures à 0,2mm. Dues à un mauvais dosage de l'eau, un séchage trop rapide ou une épaisseur d'enduit excessive.</p></div>
      <div class="lexique-item"><strong>Mise en teinte</strong><p>Opération consistant à obtenir une nuance de couleur précise par mélange de pigments ou de teintes selon une formule colorimétrique.</p></div>
      <div class="lexique-item"><strong>NF DTU 59.1</strong><p>Norme française régissant les travaux de peinture. Définit les finitions A/B/C, l'état des subjectiles (art. 5) et les 8 méthodes de vérification (art. 8).</p></div>
      <div class="lexique-item"><strong>OPPBTP (Organisme Professionnel de Prévention du BTP)</strong><p>Organisme national de prévention dédié au secteur du bâtiment et des travaux publics. Publie des mémos, guides et outils (application Check Chantier) pour améliorer la sécurité sur les chantiers.</p></div>
      <div class="lexique-item"><strong>Pigment</strong><p>Particule colorée insoluble apportant teinte et opacité. Types : minéraux/inorganiques (TiO₂ blanc, oxydes de fer), antirouille (zinc), aluminium/bronze, organiques.</p></div>
      <div class="lexique-item"><strong>Plomb (peintures au plomb)</strong><p>Ancienne peinture à base de céruse (carbonate de plomb) utilisée jusqu'aux années 1960-1980. Présence détectée par le CREP. Risque de saturnisme. EPI spécifiques et procédures encadrées obligatoires.</p></div>
      <div class="lexique-item"><strong>Point éclair</strong><p>Température minimale à laquelle les vapeurs d'un liquide inflammable s'enflamment au contact d'une flamme. Plus il est bas, plus le produit est dangereux. Ex : acétone = -18°C, white-spirit = +40°C. Indiqué sur la FDS.</p></div>
      <div class="lexique-item"><strong>Pouvoir couvrant</strong><p>Aptitude d'une peinture à masquer le support en une ou plusieurs couches. Exprimé en m²/L pour une opacité complète. Lié à la concentration en pigments (TiO₂ notamment).</p></div>
      <div class="lexique-item"><strong>Primaire d'accrochage</strong><p>Sous-couche appliquée sur les supports non poreux (carrelage, plastique, métal) pour assurer la liaison avec les couches suivantes et la fonction anticorrosive sur les métaux.</p></div>
      <div class="lexique-item"><strong>Pulvérulence</strong><p>État d'un support qui se désagrège en poudre au toucher. Doit être traité avec un fixateur ou durcisseur avant toute application de peinture.</p></div>
      <div class="lexique-item"><strong>Rechampissage</strong><p>Opération de finition consistant à peindre soigneusement au pinceau les arêtes, contours et boiseries pour obtenir une ligne nette entre deux couleurs. En finition A : aucune irrégularité admise.</p></div>
      <div class="lexique-item"><strong>Rendement</strong><p>Surface couverte par un litre de peinture (m²/L). Directement lié à l'extrait sec et à l'épaisseur de film souhaitée. Ex : extrait sec 50%, épaisseur humide 100µm → épaisseur sèche 50µm → rendement ≈ 10 m²/L.</p></div>
      <div class="lexique-item"><strong>Siccatif</strong><p>Additif catalyseur accélérant le séchage des peintures à base de solvants (glycéro, alkyde) par oxydation du liant.</p></div>
      <div class="lexique-item"><strong>Silice cristalline</strong><p>Substance minérale présente dans les poussières de coupe (béton, carrelage, enduit). Classée cancérogène (silicose). Porter masque FFP2 minimum, couper avec de l'eau.</p></div>
      <div class="lexique-item"><strong>SST (Sauveteur Secouriste du Travail)</strong><p>Travailleur formé aux gestes de premier secours sur le chantier. En cas d'urgence, alerter immédiatement le SST du chantier.</p></div>
      <div class="lexique-item"><strong>Stucco / Stuc</strong><p>Enduit décoratif à base de chaux ou plâtre mélangé à une charge finement broyée (poudre de marbre, brique, sable). Utilisé pour des effets décoratifs marbrés.</p></div>
      <div class="lexique-item"><strong>Subjectile</strong><p>Terme technique désignant le support sur lequel est appliqué un revêtement de peinture ou d'enduit. Un subjectile doit être : SAIN, SEC, PROPRE, PLAN, LISSE et COHÉSIF.</p></div>
      <div class="lexique-item"><strong>Surface de référence</strong><p>Zone représentative du bâtiment réalisée selon les spécifications contractuelles, servant de modèle validé avant la poursuite des travaux. Conservée par le maître d'ouvrage jusqu'à la réception.</p></div>
      <div class="lexique-item"><strong>Tadelakt</strong><p>Enduit stuc étanche à base de chaux de Marrakech, eau de chaux, poudre de marbre et savon noir. Étanche et fongicide. Idéal pour les pièces d'eau (douches, salles de bain).</p></div>
      <div class="lexique-item"><strong>Thixotropie</strong><p>Propriété d'une peinture épaisse (gélifiée au repos) qui redevient fluide lors de l'application par agitation. Ne coule pas. Caractéristique des peintures thixotropes.</p></div>
      <div class="lexique-item"><strong>TMS (Troubles Musculo-Squelettiques)</strong><p>Pathologies affectant les muscles, tendons et articulations, dues aux postures contraignantes répétées sur chantier (genoux, dos, épaules). Prévention : ergonomie, pauses, EPI (genouillères), aides à la manutention.</p></div>
      <div class="lexique-item"><strong>Viscosité</strong><p>Résistance d'un liquide à l'écoulement. La viscosité d'une peinture conditionne son aptitude à l'application (pinceau, rouleau, pistolet). On la règle par dilution selon la fiche technique.</p></div>
      <div class="lexique-item"><strong>Brillance spéculaire (BS)</strong><p>Mesure physique de la réflexion de la lumière sur un film peint, exprimée en unités GU (Gloss Units) avec un glossmètre à 60°. De mat (&lt;10 GU) à très brillant (&gt;85 GU). Par défaut (marché sans précision) : satiné, BS entre 10 et 45. Mesure à faire dans les 3 mois après application.</p></div>
      <div class="lexique-item"><strong>Calicot</strong><p>Bande de toile légère collée sur une fissure avant enduisage pour la stabiliser et éviter qu'elle ne réapparaisse en surface.</p></div>
      <div class="lexique-item"><strong>Charge (matière de charge)</strong><p>Constituant minéral inerte (carbonate de calcium, talc, kaolin) influant sur le brillant, la souplesse, la cohésion et la porosité. Contrairement aux pigments, les charges n'apportent ni teinte ni opacité. Prix inférieur aux pigments, très utilisées dans les peintures « amateur ».</p></div>
      <div class="lexique-item"><strong>Cloquage</strong><p>Formation de bulles ou cloques sous le film de peinture, souvent due à l'humidité ou à une application sur support trop humide / en plein soleil.</p></div>
      <div class="lexique-item"><strong>Coalescence</strong><p>Mécanisme de séchage des peintures aqueuses (acryliques). Les particules de liant dispersées dans l'eau se rapprochent puis fusionnent pour former un film continu et cohésif. Nécessite une température minimale d'environ 5°C.</p></div>
      <div class="lexique-item"><strong>COV (Composés Organiques Volatils)</strong><p>Solvants libérés lors du séchage de la peinture. Participent à la formation d'ozone. Une législation encadre leur teneur pour préserver la santé et l'environnement. Les peintures aqueuses (acryliques) ont de faibles COV, les glycérophtaliques en ont de forts.</p></div>
      <div class="lexique-item"><strong>Dilution</strong><p>Action d'ajouter de l'eau ou du solvant pour fluidifier la peinture avant application. Taux indiqué sur la fiche technique (généralement 5 à 10%).</p></div>
      <div class="lexique-item"><strong>Durcisseur</strong><p>Composant chimique ajouté à certaines peintures (époxy, polyuréthane) pour provoquer la réticulation du liant et obtenir un film très dur et résistant aux agressions chimiques.</p></div>
      <div class="lexique-item"><strong>Efflorescence / Salpêtre</strong><p>Dépôts blanchâtres en surface d'un mur causés par la migration et la cristallisation de sels solubles. Signe d'humidité. À éliminer avant toute peinture.</p></div>
      <div class="lexique-item"><strong>Égrenage</strong><p>Léger ponçage (papier 220-320) entre deux couches pour éliminer les aspérités et améliorer l'adhérence. Obligatoire en finition A.</p></div>
      <div class="lexique-item"><strong>Entoilage</strong><p>Application d'une toile (armature textile) sur une surface avant enduisage pour la renforcer et éviter que les fissures ne se développent.</p></div>
      <div class="lexique-item"><strong>Extrait sec</strong><p>Pourcentage en masse (ou volume) des matières non volatiles restant sur le support après séchage complet. Un extrait sec élevé = grande quantité de matière utile. Détermine directement le rendement.</p></div>
      <div class="lexique-item"><strong>Faïençage</strong><p>Réseau de petites fissures en mailles sur un film de peinture ou enduit, dû à un mauvais séchage ou à des produits périmés.</p></div>
      <div class="lexique-item"><strong>Farinage</strong><p>Dépôt poudreux en surface d'une peinture ancienne dû à la dégradation du liant. Traitement : brossage énergique + fixateur + repeinture.</p></div>
      <div class="lexique-item"><strong>FDES (Fiche de Déclaration Environnementale et Sanitaire)</strong><p>Document technique présentant les résultats de l'Analyse du Cycle de Vie (ACV) d'un produit et la quantité de CO₂ émise lors de son cycle de vie.</p></div>
      <div class="lexique-item"><strong>FDS (Fiche de Données de Sécurité)</strong><p>Document obligatoire donnant des informations sur les substances chimiques d'un produit et les précautions d'utilisation (stockage, EPI, premiers secours).</p></div>
      <div class="lexique-item"><strong>Feuil</strong><p>Film mince de peinture formé sur le support après séchage. Feuil humide = peinture fraîchement appliquée. Feuil sec = après séchage complet.</p></div>
      <div class="lexique-item"><strong>Film sec</strong><p>Épaisseur de la peinture après séchage complet, mesurée en microns (µm).</p></div>
      <div class="lexique-item"><strong>Finition A / B / C (NF DTU 59.1)</strong><p>Les 3 niveaux officiels. A = Soigné (enduits, égrenage, lumière rasante admise). B = Courant (défauts d'épiderme admis, aspect poché). C = Élémentaire (1 couche, usage technique). Par défaut : Finition B.</p></div>
      <div class="lexique-item"><strong>Fixateur</strong><p>Produit pénétrant appliqué sur un support poreux ou friable pour le consolider (durcir) avant peinture. Peut aussi bloquer les taches (bistre, bitume).</p></div>
      <div class="lexique-item"><strong>Glycérophtalique</strong><p>Peinture à base de résine alkyde et de solvant organique (white-spirit). Très résistante, aspect lisse et brillant, forte odeur, fort taux de COV, séchage lent (24h), jaunit avec le temps.</p></div>
      <div class="lexique-item"><strong>Lézarde</strong><p>Fissure structurelle de plus de 2mm. Ne peut pas être traitée par le peintre seul — nécessite l'intervention d'un professionnel du gros œuvre.</p></div>
      <div class="lexique-item"><strong>Liant</strong><p>Matière filmogène essentielle liant les pigments et charges entre eux et au support. Détermine l'aspect (mat, brillant, satiné). Types : émulsion aqueuse (acrylique, vinylique) ou solution solvantée (glycéro, alkyde).</p></div>
      <div class="lexique-item"><strong>Marmorino</strong><p>Enduit décoratif à base de chaux grasse et poudre de marbre. Bactéricide, hydrofugé, fongicide. Moins épais que le Tadelakt.</p></div>
      <div class="lexique-item"><strong>Microfissures</strong><p>Fissures inférieures à 0,2mm. Dues à un mauvais dosage de l'eau, un séchage trop rapide ou une épaisseur d'enduit excessive.</p></div>
      <div class="lexique-item"><strong>Mise en teinte</strong><p>Opération consistant à obtenir une nuance de couleur précise par mélange de pigments ou de teintes selon une formule colorimétrique.</p></div>
      <div class="lexique-item"><strong>NF DTU 59.1</strong><p>Norme française régissant les travaux de peinture. Définit les finitions A/B/C, l'état des subjectiles (art. 5) et les 8 méthodes de vérification (art. 8).</p></div>
      <div class="lexique-item"><strong>Pigment</strong><p>Particule colorée insoluble apportant teinte et opacité (pouvoir couvrant). Types : minéraux/inorganiques (TiO₂ blanc, oxydes de fer), antirouille (zinc), aluminium/bronze, organiques.</p></div>
      <div class="lexique-item"><strong>Point éclair</strong><p>Température minimale à laquelle les vapeurs d'un liquide inflammable s'enflamment au contact d'une flamme. Plus il est bas, plus le produit est dangereux. Ex : acétone = -18°C, white-spirit = +40°C. Indiqué sur la FDS. Essentiel pour le stockage et la sécurité.</p></div>
      <div class="lexique-item"><strong>Primaire d'accrochage</strong><p>Sous-couche appliquée sur les supports non poreux (carrelage, plastique, métal) pour assurer la liaison avec les couches suivantes et la fonction anticorrosive sur les métaux.</p></div>
      <div class="lexique-item"><strong>Pulvérulence</strong><p>État d'un support qui se désagrège en poudre au toucher. Doit être traité avec un fixateur ou durcisseur avant toute application de peinture.</p></div>
      <div class="lexique-item"><strong>Rechampissage</strong><p>Opération de finition consistant à peindre soigneusement au pinceau les arêtes, contours et boiseries pour obtenir une ligne nette entre deux couleurs. En finition A : aucune irrégularité admise.</p></div>
      <div class="lexique-item"><strong>Rendement</strong><p>Surface couverte par un litre de peinture (m²/L). Directement lié à l'extrait sec et à l'épaisseur de film souhaitée. Ex : extrait sec 50%, épaisseur humide 100µm → épaisseur sèche 50µm → rendement ≈ 10 m²/L. Indiqué sur la fiche technique.</p></div>
      <div class="lexique-item"><strong>Siccatif</strong><p>Additif catalyseur accélérant le séchage des peintures à base de solvants (glycéro, alkyde) par oxydation du liant.</p></div>
      <div class="lexique-item"><strong>Stucco / Stuc</strong><p>Enduit décoratif à base de chaux ou plâtre mélangé à une charge finement broyée (poudre de marbre, brique, sable). Utilisé pour des effets décoratifs marbrés, en intérieur et extérieur.</p></div>
      <div class="lexique-item"><strong>Subjectile</strong><p>Terme technique désignant le support sur lequel est appliqué un revêtement de peinture ou d'enduit (mur, plafond, boiserie, métal…). Un subjectile doit être : SAIN, SEC, PROPRE, PLAN, LISSE et COHÉSIF.</p></div>
      <div class="lexique-item"><strong>Tadelakt</strong><p>Enduit stuc étanche à base de chaux de Marrakech, eau de chaux, poudre de marbre et savon noir. Étanche et fongicide. Idéal pour les pièces d'eau (douches, salles de bain).</p></div>
      <div class="lexique-item"><strong>Thixotropie</strong><p>Propriété d'une peinture épaisse (gélifiée au repos) qui redevient fluide lors de l'application par agitation. Ne coule pas. Caractéristique des peintures thixotropes.</p></div>
      <div class="lexique-item"><strong>Rendement</strong><p>Surface couverte par un litre de peinture, exprimée en m²/L. Directement lié à l'extrait sec et à l'épaisseur de film souhaitée. Ex : peinture avec 50% extrait sec et film humide 100µm → film sec 50µm → rendement ≈ 10 m²/L. Indiqué sur la fiche technique.</p></div>
      <div class="lexique-item"><strong>Siccatif</strong><p>Additif catalyseur accélérant le séchage des peintures à base de solvants (glycéro, alkyde) par oxydation du liant.</p></div>
    </div>
  </div>
  <div id="peinture-securite" class="sub-content">
    <div class="section-card">
      <h2>⛑️ Mémo Prévention & Sécurité — Peinture (source OPPBTP)</h2>

      <div class="info-box red"><div class="icon">🔴</div><div class="content"><p><strong>Source : Mémo d'accueil OPPBTP — Peinture / Miroiterie / Vitrerie / Pose de revêtement</strong><br>Ces règles s'appliquent dès le premier jour sur le chantier.</p></div></div>

      <h3>🧹 Propreté du chantier & Hygiène</h3>
      <div class="securite-grid">
        <div class="securite-card"><span class="icon">🧹</span><h4>Poste de travail</h4><p>Au quotidien, garder son poste propre. Privilégier l'aspirateur au balai pour éviter la dispersion des poussières.</p></div>
        <div class="securite-card"><span class="icon">🧼</span><h4>Hygiène personnelle</h4><p>Porter des vêtements propres et secs. Se laver les mains régulièrement. Garder propres les installations d'hygiène.</p></div>
        <div class="securite-card"><span class="icon">📦</span><h4>Stockage</h4><p>Approvisionner uniquement les quantités nécessaires. Respecter les capacités de chargement des plateformes. Zones de circulation dégagées.</p></div>
        <div class="securite-card"><span class="icon">🚗</span><h4>Circulation routière</h4><p>Ranger et arrimer les charges avant de partir. Respecter le code de la route et rester vigilant pendant le trajet.</p></div>
      </div>

      <h3>🦺 EPI — Équipements de Protection Individuelle</h3>
      <div class="info-box orange"><div class="icon">⚠️</div><div class="content"><p><strong>Vérifiez les EPI à porter sur le chantier avant de commencer.</strong> Les EPI sont obligatoires et doivent être adaptés au poste de travail.</p></div></div>
      <div class="securite-grid">
        <div class="securite-card"><span class="icon">😷</span><h4>Protection respiratoire</h4><p>Masque FFP2 pour poussières (ponçage, décapage). Demi-masque avec cartouche vapeurs organiques pour peintures solvantées (glycéro, époxy, PU).</p></div>
        <div class="securite-card"><span class="icon">🥽</span><h4>Lunettes de sécurité</h4><p>Obligatoires lors de la projection (pistolet airless), du décapage, de la découpe et des travaux en plafond. Protection des éclats.</p></div>
        <div class="securite-card"><span class="icon">🧤</span><h4>Gants de protection</h4><p>Gants nitrile pour produits chimiques (solvants, décapants). Gants anticoupures pour outils coupants (cutter, grattoir). À renouveler régulièrement.</p></div>
        <div class="securite-card"><span class="icon">👷</span><h4>Casque & Harnais</h4><p>Casque de protection sur les chantiers avec risque de chute d'objets. Harnais anti-chute si travaux en hauteur sans garde-corps.</p></div>
        <div class="securite-card"><span class="icon">🥾</span><h4>Chaussures de sécurité</h4><p>Port obligatoire sur tous les chantiers BTP. Protection contre les chutes d'objets et les perforations.</p></div>
        <div class="securite-card"><span class="icon">🦺</span><h4>Gilet haute visibilité</h4><p>Obligatoire sur les chantiers avec circulation d'engins. Assure la visibilité du travailleur.</p></div>
        <div class="securite-card"><span class="icon">👂</span><h4>Protection auditive</h4><p>Casque antibruit ou bouchons d'oreilles lors de l'utilisation d'outils bruyants (ponceuse, compresseur). S'organiser pour réduire les nuisances sonores.</p></div>
        <div class="securite-card"><span class="icon">🦵</span><h4>Genouillères</h4><p>Protection des genoux lors des travaux au sol (pose de sols souples, carrelage). Prévention des TMS.</p></div>
      </div>

      <h3>☠️ Produits dangereux</h3>
      <div class="securite-grid">
        <div class="securite-card"><span class="icon">🧴</span><h4>EPI permanents</h4><p>Porter gants, lunettes et masque en permanence lors de la manipulation de produits chimiques. Ne jamais travailler sans protection.</p></div>
        <div class="securite-card"><span class="icon">🪣</span><h4>Stockage des produits</h4><p>Refermer les bidons après usage. Stocker dans des endroits spécifiques, ventilés, à l'abri de la chaleur et des flammes. Consulter la FDS.</p></div>
        <div class="securite-card"><span class="icon">🌬️</span><h4>Ventilation obligatoire</h4><p>Aérer le local en permanence lors de l'utilisation de peintures solvantées. Les COV sont toxiques et inflammables.</p></div>
        <div class="securite-card"><span class="icon">🔥</span><h4>Point éclair / Incendie</h4><p>Pas de flamme nue avec produits solvantés. Connaître le point éclair des produits utilisés (FDS). Extincteur disponible et accessible.</p></div>
      </div>
      <div class="info-box red"><div class="icon">⚠️</div><div class="content"><p><strong>COV :</strong> Les Composés Organiques Volatils des peintures solvantées sont nocifs pour les voies respiratoires et inflammables. Toujours ventiler et respecter les consignes de la FDS (Fiche de Données de Sécurité).</p></div></div>

      <h3>🏗️ Travaux en hauteur</h3>
      <div class="securite-grid">
        <div class="securite-card"><span class="icon">🚧</span><h4>Déplacement échafaudage</h4><p>Déplacer l'échafaudage SANS charge (ni matériel, ni personne). Faire attention aux obstacles au sol.</p></div>
        <div class="securite-card"><span class="icon">🔒</span><h4>Stabilisation</h4><p>Bloquer les roues et stabiliser l'échafaudage avant de monter. Vérifier l'échafaudage avec l'application <strong>Check Chantier</strong> (OPPBTP).</p></div>
        <div class="securite-card"><span class="icon">📐</span><h4>Plateforme de travail</h4><p>Utiliser une plateforme ou un échafaudage roulant homologué pour les travaux en plafond. Jamais sur escabeau instable.</p></div>
        <div class="securite-card"><span class="icon">🪜</span><h4>Règle d'or</h4><p>Ne jamais s'étirer ou se pencher hors du garde-corps. Se déplacer plutôt que de s'allonger dangereusement.</p></div>
      </div>

      <h3>⚡ Électricité & Réseaux</h3>
      <div class="securite-grid">
        <div class="securite-card"><span class="icon">⚡</span><h4>Habilitation électrique</h4><p>Vérifier son habilitation avant d'intervenir sur ou près des réseaux électriques. Sans habilitation = ne pas intervenir.</p></div>
        <div class="securite-card"><span class="icon">🚫</span><h4>Sans consignation</h4><p>Sans consignation ou protection préalable du réseau : ne pas intervenir ! Risque électrocution.</p></div>
        <div class="securite-card"><span class="icon">📏</span><h4>Zones de sécurité</h4><p>Respecter les distances de sécurité autour des lignes électriques : &lt;50 000V = 3m / ≥50 000V = 5m.</p></div>
        <div class="securite-card"><span class="icon">🔌</span><h4>Matériel électrique</h4><p>Utiliser du matériel en bon état (coffret, prolongateur, prises). Vérifier l'absence de dommages sur les câbles avant emploi.</p></div>
      </div>

      <h3>🔪 Outils coupants & Portatifs</h3>
      <div class="securite-grid">
        <div class="securite-card"><span class="icon">✂️</span><h4>Préparation du geste</h4><p>Prendre le temps de préparer son geste avant d'utiliser un outil coupant (cutter, grattoir, scie). Maîtriser la direction de coupe.</p></div>
        <div class="securite-card"><span class="icon">🧤</span><h4>EPI anticoupures</h4><p>Gants anticoupures + masque + lunettes lors de l'utilisation d'outils coupants. Se protéger des éclats.</p></div>
        <div class="securite-card"><span class="icon">🛡️</span><h4>Protections machines</h4><p>Ne jamais enlever les protections d'une machine (garde, capot). S'assurer de l'arrêt complet de l'outil avant de le poser.</p></div>
        <div class="securite-card"><span class="icon">🔧</span><h4>Utilisation conforme</h4><p>Utiliser l'outillage en respectant les consignes de sécurité du fabricant. Préférer les outils moins bruyants, vibrants et légers.</p></div>
      </div>

      <h3>🧱 Fibres dangereuses (Amiante / Plomb / Silice)</h3>
      <div class="info-box red"><div class="icon">☣️</div><div class="content"><p><strong>RÈGLE ABSOLUE : Sans être formé, ne pas toucher !</strong> L'amiante, le plomb et la silice cristalline sont des substances cancérogènes classées. Toute intervention nécessite une formation spécifique et des EPI dédiés (combinaison, masque TM3P...).</p></div></div>
      <div class="securite-grid">
        <div class="securite-card"><span class="icon">☣️</span><h4>Amiante</h4><p>Présent dans les bâtiments avant 1997 (plafonds, colles, joints, enduits). Formation SS3/SS4 obligatoire. EPI spécifiques. Déchets classés dangereux.</p></div>
        <div class="securite-card"><span class="icon">🔴</span><h4>Plomb (CREP)</h4><p>Présent dans les peintures anciennes (&lt;1949 principalement). Diagnostic CREP obligatoire avant travaux. Risque saturnisme (surtout enfants).</p></div>
        <div class="securite-card"><span class="icon">💨</span><h4>Silice cristalline</h4><p>Présente dans les poussières de coupe (carrelage, béton, enduit). Masque FFP2 minimum lors des découpes. Couper avec de l'eau si possible.</p></div>
        <div class="securite-card"><span class="icon">🧪</span><h4>EPI spécifiques fibres</h4><p>Combinaison de protection (type 5), masque TM3P (amiante), gants adaptés. Porter les équipements prévus pour le chantier.</p></div>
      </div>

      <h3>🚑 Urgence & Incendie</h3>
      <div class="securite-grid">
        <div class="securite-card"><span class="icon">🚑</span><h4>Urgence</h4><p>Alerter immédiatement le secouriste du chantier (SST). Soigner les petites blessures avec la trousse de secours. Numéros d'urgence : 15 (SAMU) / 18 (Pompiers) / 112.</p></div>
        <div class="securite-card"><span class="icon">🧯</span><h4>Incendie</h4><p>Alerter les secours (18). Utiliser l'extincteur mis à disposition. Ne pas prendre de risques inutiles. Évacuer si le feu dépasse les capacités de l'extincteur.</p></div>
        <div class="securite-card"><span class="icon">🚪</span><h4>Issues de secours</h4><p>Toujours dégagées. Ne jamais obstruer les sorties de secours avec du matériel ou des produits, même temporairement.</p></div>
        <div class="securite-card"><span class="icon">📞</span><h4>Affichage chantier</h4><p>Respecter les règles de sécurité affichées sur le chantier. Se déplacer dans les zones balisées (piétons séparés des engins).</p></div>
      </div>

      <h3>🏥 Manutention manuelle & TMS</h3>
      <div class="securite-grid">
        <div class="securite-card"><span class="icon">🦾</span><h4>Aides à la manutention</h4><p>Utiliser les aides à la manutention (diable, chariot, ventouses mécaniques pour vitrages). Ne jamais porter seul une charge trop lourde.</p></div>
        <div class="securite-card"><span class="icon">🧍</span><h4>Ergonomie</h4><p>Privilégier un poste de travail ergonomique et adapté. Alterner les postures contraignantes. Prendre des pauses régulières.</p></div>
        <div class="securite-card"><span class="icon">🔇</span><h4>Vibrations & bruit</h4><p>Utiliser des outils moins bruyants et vibrants. S'organiser pour limiter l'exposition aux nuisances sonores.</p></div>
      </div>

      <h3>🍺 Santé au travail</h3>
      <div class="info-box red"><div class="icon">🚫</div><div class="content"><p><strong>Alcool, drogues et médicaments :</strong> Ne pas consommer de boissons alcoolisées ni de substances interdites sur le chantier. Rester vigilant avec les médicaments qui peuvent altérer la vigilance (somnolence, réflexes).</p></div></div>
    </div>
  </div>
  <div id="peinture-quiz" class="sub-content">
    <div class="section-card"><h2>🎯 Questionnaire d'Acquis — Peinture</h2></div>
    <div class="quiz-container" id="quiz-peinture">
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">1</div><div class="q-text">Quelle est la fonction du liant dans une peinture ?</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="pq1" value="a"> a) Donner la couleur</label></li>
          <li><label><input type="radio" name="pq1" value="b"> b) Fixer les pigments au support et former le film dur</label></li>
          <li><label><input type="radio" name="pq1" value="c"> c) Fluidifier la peinture</label></li>
          <li><label><input type="radio" name="pq1" value="d"> d) Accélérer le séchage</label></li>
        </ul>
        <div class="answer-feedback" id="pq1-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">2</div><div class="q-text">Un mur présente des cloques sous la peinture. Quelle en est la cause probable ?</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="pq2" value="a"> a) Peinture trop épaisse</label></li>
          <li><label><input type="radio" name="pq2" value="b"> b) Humidité sous le film ou support trop humide lors de l'application</label></li>
          <li><label><input type="radio" name="pq2" value="c"> c) Trop de dilution</label></li>
          <li><label><input type="radio" name="pq2" value="d"> d) Peinture de mauvaise qualité</label></li>
        </ul>
        <div class="answer-feedback" id="pq2-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">3</div><div class="q-text">Vrai ou Faux : La peinture glycérophtalique est à base d'eau.</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="pq3" value="a"> ✅ Vrai</label></li>
          <li><label><input type="radio" name="pq3" value="b"> ❌ Faux</label></li>
        </ul>
        <div class="answer-feedback" id="pq3-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">4</div><div class="q-text">Quel niveau de finition (NF DTU 59.1) correspond à un travail soigné avec enduits, égrenage et observation en lumière rasante admise ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="pq4" value="a"> a) Finition C (Élémentaire)</label></li>
          <li><label><input type="radio" name="pq4" value="b"> b) Finition B (Courant)</label></li>
          <li><label><input type="radio" name="pq4" value="c"> c) Finition A (Soigné)</label></li>
          <li><label><input type="radio" name="pq4" value="d"> d) Finition D (Haut de gamme)</label></li>
        </ul>
        <div class="answer-feedback" id="pq4-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">5</div><div class="q-text">Des moisissures apparaissent sur un mur repeint il y a 6 mois. Quelle est la bonne démarche ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="pq5" value="a"> a) Peindre directement par-dessus avec une peinture antifongique</label></li>
          <li><label><input type="radio" name="pq5" value="b"> b) Traiter avec fongicide, traiter la cause d'humidité, puis repeindre</label></li>
          <li><label><input type="radio" name="pq5" value="c"> c) Gratter et reboucher uniquement</label></li>
          <li><label><input type="radio" name="pq5" value="d"> d) Changer la peinture de marque</label></li>
        </ul>
        <div class="answer-feedback" id="pq5-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">6</div><div class="q-text">Qu'est-ce que le "farinage" d'une peinture ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="pq6" value="a"> a) Des coulures visibles sur la peinture</label></li>
          <li><label><input type="radio" name="pq6" value="b"> b) Un dépôt poudreux en surface dû à la dégradation du liant</label></li>
          <li><label><input type="radio" name="pq6" value="c"> c) Des taches blanches dues à l'humidité</label></li>
          <li><label><input type="radio" name="pq6" value="d"> d) Un jaunissement de la peinture blanche</label></tr>
        </ul>
        <div class="answer-feedback" id="pq6-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">7</div><div class="q-text">Mise en situation — Décollement de peinture</div><span class="q-level hard">🔴 Difficile</span></div>
        <div class="scenario-box"><h4>🏗️ Scénario :</h4><p>En contrôlant une livraison de chantier, tu constates que la peinture se décolle par plaques sur un mur neuf. Le client est mécontent. Quelles sont les 3 causes possibles et comment vas-tu procéder pour la réparation ?</p></div>
        <textarea class="open-answer" id="pq7-answer" placeholder="Écris ta réponse ici..."></textarea>
        <button class="btn-check" onclick="checkOpen('pq7')">Voir la correction 📋</button>
        <div class="answer-feedback" id="pq7-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">8</div><div class="q-text">Pourquoi doit-on ventiler le local lors d'une application de peinture glycérophtalique ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="pq8" value="a"> a) Pour accélérer le séchage uniquement</label></li>
          <li><label><input type="radio" name="pq8" value="b"> b) Pour éliminer les COV toxiques et inflammables dégagés par les solvants</label></li>
          <li><label><input type="radio" name="pq8" value="c"> c) Pour éviter la condensation</label></li>
          <li><label><input type="radio" name="pq8" value="d"> d) Pour maintenir la couleur</label></li>
        </ul>
        <div class="answer-feedback" id="pq8-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">9</div><div class="q-text">Vrai ou Faux : Pour appliquer une peinture acrylique, il faut obligatoirement un primaire.</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="pq9" value="a"> ✅ Vrai</label></li>
          <li><label><input type="radio" name="pq9" value="b"> ❌ Faux</label></li>
        </ul>
        <div class="answer-feedback" id="pq9-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">10</div><div class="q-text">Pour peindre une salle de bain humide, quelle peinture est la plus adaptée ?</div><span class="q-level hard">🔴 Difficile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="pq10" value="a"> a) Peinture mate acrylique standard</label></li>
          <li><label><input type="radio" name="pq10" value="b"> b) Peinture acrylique satinée antifongique spéciale pièces humides</label></li>
          <li><label><input type="radio" name="pq10" value="c"> c) Lasure bois</label></li>
          <li><label><input type="radio" name="pq10" value="d"> d) Glycéro mat</label></li>
        </ul>
        <div class="answer-feedback" id="pq10-feedback"></div>
      </div>
      <div class="quiz-footer">
        <button class="btn-submit" onclick="submitQuiz('peinture', 10)">🎯 Calculer mon score !</button>
        <div class="score-display" id="score-peinture"></div>
      </div>
    </div>
  </div>
</div><!-- END PEINTURE -->

<!-- ================================================== -->
<!-- ONGLET 3 : PAPIER PEINT -->
<!-- ================================================== -->
<div id="papierpeint" class="tab-content">
  <div class="sub-tabs">
    <button class="sub-tab-btn active" onclick="showSub('papierpeint', 'revision', this)">📖 Révision générale</button>
    <button class="sub-tab-btn" onclick="showSub('papierpeint', 'controle', this)">✅ Contrôle travaux</button>
    <button class="sub-tab-btn" onclick="showSub('papierpeint', 'lexique', this)">📝 Lexique</button>
    <button class="sub-tab-btn" onclick="showSub('papierpeint', 'securite', this)">⛑️ Mémo sécurité</button>
    <button class="sub-tab-btn" onclick="showSub('papierpeint', 'quiz', this)">🎯 Questionnaire d'acquis</button>
  </div>
  <div id="papierpeint-revision" class="sub-content active">
    <div class="section-card">
      <h2>📜 Papier Peint & Revêtements Muraux — Révision Générale</h2>
      <div class="img-grid">
        <div class="img-example"><img src="https://images.unsplash.com/photo-1586023492125-27b2c045efd7?w=400&q=80" alt="Pose papier peint"><div class="caption">📸 Pose de papier peint</div></div>
        <div class="img-example"><img src="https://images.unsplash.com/photo-1615874959474-d609969a20ed?w=400&q=80" alt="Revêtements muraux"><div class="caption">📸 Revêtements muraux décoration</div></div>
      </div>

      <h3>🔹 Introduction — Bref historique</h3>
      <p>Le papier peint, véritable expression artistique, transcende le simple rôle de revêtement mural pour devenir une composante esthétique de nos espaces de vie. Depuis ses modestes débuts au <strong>XVIIe siècle</strong>, où il imitait des matériaux plus coûteux, il a évolué pour devenir une forme d'art décoratif à part entière, offrant motifs variés, textures subtiles et couleurs éclatantes.</p>

      <h3>🔹 La fabrication du papier peint</h3>
      <p>L'impression s'exécute à l'aide de <strong>cylindres gravés</strong> qui impriment un papier support enroulé en bobines de 800m de long. Un rouleau commercial mesure de <strong>0,53m à 0,78m de large × 10,05m de long</strong>, dans un grammage de <strong>60 à 280 g/m²</strong>.</p>
      <div class="controle-phase">
        <div class="check-item"><span class="check-icon">1️⃣</span> <strong>Fonçage :</strong> Application d'une couche de fond uniforme sur le papier brut (tambour + séchage + enroulage)</div>
        <div class="check-item"><span class="check-icon">2️⃣</span> <strong>Impression :</strong> Impression des motifs avec des cylindres — chaque cylindre dépose une couleur différente</div>
        <div class="check-item"><span class="check-icon">3️⃣</span> <strong>Gaufrage :</strong> Estampage entre deux cylindres (mâle et femelle) pour créer les reliefs et textures</div>
        <div class="check-item"><span class="check-icon">4️⃣</span> <strong>Séchage et bobinage :</strong> Séchage à 40°C puis enroulage sur bobines</div>
        <div class="check-item"><span class="check-icon">5️⃣</span> <strong>Enroulage commercial :</strong> Découpe automatique en rouleaux (200 rouleaux/heure)</div>
      </div>

      <h3>🔹 Les différents types de papier peint</h3>
      <table>
        <tr><th>Type</th><th>Composition</th><th>Avantages</th><th>Inconvénients</th></tr>
        <tr><td><strong>Simplex (traditionnel)</strong></td><td>1 couche de papier imprimé</td><td>Facile à poser</td><td>Difficile à entretenir, ne supporte pas l'humidité, faible opacité</td></tr>
        <tr><td><strong>Duplex (traditionnel)</strong></td><td>2 papiers entre-collés à la colle aqueuse</td><td>Plus résistant que le simplex</td><td>Coût plus élevé</td></tr>
        <tr><td><strong>Vinyle</strong></td><td>Support papier + couche PVC</td><td>Résistant, lavable, résistant UV, imperméable, masque les défauts, coût abordable</td><td>Non respirant</td></tr>
        <tr><td><strong>Intissé (non-tissé)</strong></td><td>Fibres synthétiques + vinyle/cellulose</td><td>Encollage au mur, épais, décollage facile sans produit, utilisable WC, grande résistance</td><td>Coût plus élevé</td></tr>
        <tr><td><strong>Expansé</strong></td><td>Support papier + PVC expansé</td><td>Épais, résistant, facile d'entretien, effets relief et gaufré</td><td>Contient du PVC</td></tr>
        <tr><td><strong>Panoramique</strong></td><td>Impression grand format</td><td>Décoration murale forte impact</td><td>Pose délicate, raccords complexes</td></tr>
      </table>

      <h3>🔹 Les revêtements muraux (au-delà du papier peint)</h3>
      <table>
        <tr><th>Type</th><th>Matière</th><th>Caractéristiques</th><th>Usage</th></tr>
        <tr><td><strong>Vinyle contrecollé (Vescom, Buflon...)</strong></td><td>PVC sur support textile</td><td>Résistant, lavable, large choix de motifs, durable</td><td>Hôtels, bureaux, hôpitaux — usage intensif</td></tr>
        <tr><td><strong>Naturels (paille japonaise, bambou, sisal)</strong></td><td>Fibres végétales</td><td>Chaleur, authenticité, respirant</td><td>Résidentiel décoratif — sensible humidité et lumière</td></tr>
        <tr><td><strong>Textiles (soie, lin, velours)</strong></td><td>Fibres naturelles ou synthétiques</td><td>Raffiné, confort acoustique, haut de gamme</td><td>Espaces secs, haut de gamme — entretien délicat</td></tr>
        <tr><td><strong>Toile de verre</strong></td><td>Fibres de verre tissées</td><td>Solidifie les murs fissurés, prêt à peindre</td><td>Rénovation, murs dégradés</td></tr>
        <tr><td><strong>Techniques</strong></td><td>Variable</td><td>Acoustiques, ignifuges, antibactériens</td><td>ERP, collectivités, hôpitaux</td></tr>
      </table>

      <h3>🔹 Les différents types de raccords</h3>
      <div class="info-box blue"><div class="icon">📋</div><div class="content"><p>Le type de raccord est <strong>indiqué sur l'étiquette du rouleau</strong>. Il détermine les chutes et la quantité nécessaire. Toujours vérifier avant de commander !</p></div></div>
      <table>
        <tr><th>Type de raccord</th><th>Symbole</th><th>Description</th><th>Impact sur les chutes</th></tr>
        <tr><td><strong>Raccord 0 / sans raccord</strong></td><td>— / ∞</td><td>Papier uni ou rayures verticales. Motifs non coupés sur les bords.</td><td>Aucune chute supplémentaire</td></tr>
        <tr><td><strong>Raccord droit</strong></td><td>↔</td><td>Le motif se reproduit tous les X cm sur une même ligne horizontale.</td><td>Chutes = hauteur du raccord</td></tr>
        <tr><td><strong>Raccord sauté (décalé)</strong></td><td>↕</td><td>Le motif se reproduit tous les X cm mais décalé tous les 2 lés. Travailler avec 2 rouleaux.</td><td>Chutes importantes — à prévoir !</td></tr>
      </table>

      <h3>🔹 Documents normatifs — DTU 59.4 (NF P74-204)</h3>
      <div class="info-box orange"><div class="icon">📗</div><div class="content"><p>Le <strong>DTU 59.4 (NF P74-204-1)</strong> régit la mise en œuvre des papiers peints et revêtements muraux à l'intérieur des bâtiments (neuf et rénovation). Le <strong>DTU 59.1</strong> régit la préparation des supports. <strong>En l'absence de précision, la finition B est retenue.</strong></p></div></div>
      <table>
        <tr><th>Document</th><th>Objet</th></tr>
        <tr><td><span class="norme-tag">DTU 59.4</span> NF P74-204-1</td><td>Cahier des clauses techniques — mise en œuvre des papiers peints et revêtements muraux</td></tr>
        <tr><td><span class="norme-tag">DTU 59.4</span> NF P74-204-2</td><td>Cahier des clauses spéciales — conditions administratives des marchés privés</td></tr>
        <tr><td><span class="norme-tag">DTU 59.1</span></td><td>Travaux de peinture — préparation des supports (subjectiles)</td></tr>
      </table>

      <h3>🔹 Conditions d'exécution (DTU 59.4)</h3>
      <div class="info-box red"><div class="icon">🏗️</div><div class="content"><p><strong>Conditions préalables indispensables (DTU 59.4 art. 4.1) :</strong> Le bâtiment doit être <strong>hors d'eau et vitré</strong>, les enduits de plâtre et ciment exécutés et secs, locaux clos mais ventilés, libres de tout autre corps d'état, éclairage équivalent à l'éclairage définitif.</p></div></div>
      <table>
        <tr><th>Paramètre</th><th>Exigence DTU 59.4</th></tr>
        <tr><td>Température ambiante</td><td>Entre ~10°C et ~25-30°C</td></tr>
        <tr><td>Hygrométrie</td><td>Conforme — pas d'humidité dans les murs</td></tr>
        <tr><td>Humidité support plâtre</td><td>≤ 5% d'humidité</td></tr>
        <tr><td>Humidité support bois</td><td>~12% ± 2%</td></tr>
        <tr><td>Planéité locale</td><td>Écart max 1mm sous règle 20cm / 5mm sous règle 2m</td></tr>
        <tr><td>Joints entre lés</td><td>Pas d'écart &gt; 1mm, pas de chevauchement</td></tr>
      </table>
      <div class="info-box green"><div class="icon">📋</div><div class="content"><p><strong>Avant de commencer (DTU 59.4 art. 4.2.1) :</strong> L'entrepreneur doit reconnaître les subjectiles, noter les défauts et non-conformités PAR ÉCRIT au maître d'ouvrage. Tout retard motivé par des conditions non conformes donne lieu à prorogation du délai d'exécution.</p></div></div>

      <h3>🔹 Préparation du support (subjectile)</h3>
      <p>Le support doit être posé sur tous supports usuels : <strong>plâtre et dérivés, liants hydrauliques, bois</strong>. Il doit être <strong>sain, plan, propre, sec et adapté</strong> au revêtement.</p>
      <div class="controle-phase">
        <div class="check-item"><span class="check-icon">☑️</span> Support nettoyé (époussetage, lessivage)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Fissures traitées et rebouchées</div>
        <div class="check-item"><span class="check-icon">☑️</span> Trous comblés à l'enduit de rebouchage</div>
        <div class="check-item"><span class="check-icon">☑️</span> Ponçage et dépoussiérage</div>
        <div class="check-item"><span class="check-icon">☑️</span> Application fixateur ou impression de fond si support absorbant ou neuf</div>
        <div class="check-item"><span class="check-icon">☑️</span> Dépose des radiateurs effectuée avant pose</div>
        <div class="check-item"><span class="check-icon">☑️</span> Vérification humidité conforme aux limites DTU</div>
      </div>

      <h3>🔹 Les colles à revêtements muraux</h3>
      <div class="info-box blue"><div class="icon">💡</div><div class="content"><p>De nos jours, toutes les colles à revêtements muraux sont en <strong>dispersion aqueuse</strong>, prêtes à l'emploi, formulées à base de <strong>résines vinyliques ou acryliques</strong>. Application à la spatule crantée ou au rouleau sur le support (ou exceptionnellement sur l'envers du revêtement selon le fabricant).</p></div></div>
      <table>
        <tr><th>Colle</th><th>Usage</th><th>Critères de choix</th></tr>
        <tr><td>Colle universelle (méthylcellulose)</td><td>Papier peint standard, simplex, duplex</td><td>Facilité de mise en œuvre</td></tr>
        <tr><td>Colle spéciale intissé</td><td>Revêtements intissés — s'applique sur le MUR</td><td>Tack élevé, temps ouvert long</td></tr>
        <tr><td>Colle vinyle / forte</td><td>Revêtements lourds, vinyle contrecollé, expansé</td><td>Bonne résistance, anti-moisissures</td></tr>
        <tr><td>Colle pour revêtements textiles</td><td>Soie, lin, paille japonaise, sisal</td><td>Absence d'odeur, bonne tenue en pièces humides</td></tr>
      </table>
      <p><strong>Critères de choix d'une colle (DTU 59.4) :</strong></p>
      <ul class="styled">
        <li>Facilité de mise en œuvre</li>
        <li>Bonne résistance au pourrissement (anti-moisissures, non virant)</li>
        <li>Tack élevé (adhérence immédiate)</li>
        <li>Temps ouvert très long (facilite la pose)</li>
        <li>Absence d'odeur</li>
        <li>Bonne tenue dans les pièces d'eau</li>
      </ul>

      <h3>🔹 Technique de pose pas à pas</h3>
      <div class="controle-phase">
        <div class="check-item"><span class="check-icon">1️⃣</span> <strong>Tracer le fil à plomb</strong> pour avoir une référence verticale absolue (retracer tous les 4-5 lés)</div>
        <div class="check-item"><span class="check-icon">2️⃣</span> <strong>Commencer côté opposé à la fenêtre</strong> (point lumineux) pour que les joints soient moins visibles</div>
        <div class="check-item"><span class="check-icon">3️⃣</span> <strong>Couper les lés</strong> en tenant compte du raccord (laisser 5 cm de surplus en haut et en bas)</div>
        <div class="check-item"><span class="check-icon">4️⃣</span> <strong>Encoller le papier ou le mur</strong> selon le type — intissé : coller le MUR uniquement</div>
        <div class="check-item"><span class="check-icon">5️⃣</span> <strong>Temps de trempage</strong> si papier classique (2 à 5 min selon grammage). Plier en accordéon.</div>
        <div class="check-item"><span class="check-icon">6️⃣</span> <strong>Poser et maroufler</strong> — lisser avec la spalter du centre vers les bords pour chasser bulles et colle</div>
        <div class="check-item"><span class="check-icon">7️⃣</span> <strong>Vérifier l'aplomb</strong> à chaque lé. Aligner le raccord.</div>
        <div class="check-item"><span class="check-icon">8️⃣</span> <strong>Arasement</strong> en haut et en bas — lame neuve obligatoire pour une coupe nette</div>
        <div class="check-item"><span class="check-icon">9️⃣</span> <strong>Éponger</strong> immédiatement les traces de colle sur le papier</div>
      </div>

      <h3>🔹 Technique de l'angle rentrant / sortant</h3>
      <div class="info-box orange"><div class="icon">📐</div><div class="content"><p>Angle rentrant : laisser <strong>dépasser 5 mm</strong> du lé dans l'angle. Découper le lé suivant à la largeur du pan de mur + 8mm à 1 cm. Ce lé chevauche les 5mm précédents.<br><strong>Angle sortant :</strong> même principe inversé. Chevaucher l'angle sortant, laisser dépasser 5mm. <strong>Conserver toujours les chutes</strong> pour compléter la pose !</p></div></div>

      <h3>🔹 Technique de la coupe double</h3>
      <div class="info-box red"><div class="icon">✂️</div><div class="content"><p>La <strong>coupe double est obligatoire dans les angles rentrants et sortants</strong> pour éviter les surplus de colle et les bulles d'air.</p></div></div>
      <div class="controle-phase">
        <div class="check-item"><span class="check-icon">1️⃣</span> Superposer les deux lés (chevauchement d'environ 5 cm)</div>
        <div class="check-item"><span class="check-icon">2️⃣</span> Réaliser les arasements haut et bas</div>
        <div class="check-item"><span class="check-icon">3️⃣</span> Placer la règle bombée sur l'axe de chevauchement (aplomb)</div>
        <div class="check-item"><span class="check-icon">4️⃣</span> Débuter la coupe avec un kicoup équipé d'une <strong>lame neuve</strong> — ne plus soulever le kicoup une fois la coupe commencée</div>
        <div class="check-item"><span class="check-icon">5️⃣</span> Faire coulisser la règle le long de la lame jusqu'en bas</div>
        <div class="check-item"><span class="check-icon">6️⃣</span> Retirer les deux bandes coupées</div>
        <div class="check-item"><span class="check-icon">7️⃣</span> Repasser de la colle à la brosse sur le joint, puis maroufler</div>
        <div class="check-item"><span class="check-icon">8️⃣</span> Éponger les traces de colle</div>
      </div>

      <h3>🔹 Désordres — Causes et solutions</h3>
      <div class="disorder-card"><h4>🔴 Décollements / bords soulevés</h4><p><strong>Causes :</strong> Colle insuffisante, support mal préparé (poussiéreux, humide), tack insuffisant.</p><div class="solution"><strong>✅ Solution :</strong> Injecter de la colle sous le papier, maroufler au rouleau à joints, traiter la cause d'humidité. Refaire si décollement important.</div></div>
      <div class="disorder-card"><h4>🔴 Raccords décalés</h4><p><strong>Causes :</strong> Mauvais traçage du fil à plomb, mur non vertical, dilatation du papier après encollage.</p><div class="solution"><strong>✅ Solution :</strong> Retracer le fil à plomb tous les 4-5 lés. Un léger décalage en angle est acceptable (DTU).</div></div>
      <div class="disorder-card"><h4>🔴 Bulles / boursouflures après séchage</h4><p><strong>Causes :</strong> Papier mal maroufle, colle trop épaisse, temps de trempage insuffisant, support trop absorbant.</p><div class="solution"><strong>✅ Solution :</strong> Dans les 24h : lisser à nouveau. Après séchage : percer et injecter de la colle, maroufler. Vérifier le primaire de fond.</div></div>
      <div class="disorder-card"><h4>🔴 Traces de colle visibles</h4><p><strong>Causes :</strong> Excès de colle, épongeage insuffisant pendant la pose.</p><div class="solution"><strong>✅ Solution :</strong> Éponger immédiatement pendant la pose. Après séchage, certaines colles s'effacent à l'eau tiède.</div></div>
      <div class="disorder-card"><h4>🔴 Joints visibles / écarts entre lés</h4><p><strong>Causes :</strong> Retrait du papier au séchage (excès de trempage), coupe imprécise, support non plan.</p><div class="solution"><strong>✅ Solution :</strong> Respecter le temps de trempage. Travailler sur support plan. Utiliser lame bien coupante pour arasement.</div></div>

      <h3>🔹 Surface de référence et réception (DTU 59.4 art. 7)</h3>
      <div class="info-box green"><div class="icon">🔍</div><div class="content"><p>L'entrepreneur informe le maître d'ouvrage <strong>au moins 15 jours à l'avance</strong> des dates d'exécution des surfaces de référence. La surface de référence ne peut être choisie dans l'appartement témoin de présentation commerciale.<br>La <strong>garantie</strong> des travaux de pose est de <strong>2 ans minimum</strong> (loi du 4 janvier 1978, article 1792-3 du Code Civil).</p></div></div>
    </div>
  </div>
  <div id="papierpeint-controle" class="sub-content">
    <div class="section-card">
      <h2>✅ Contrôle des Travaux — Papier Peint (DTU 59.4)</h2>
      <div class="controle-phase"><h3>🔵 AVANT LES TRAVAUX</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Bâtiment hors d'eau, vitré, étanchéité assurée</div>
        <div class="check-item"><span class="check-icon">☑️</span> Locaux clos mais ventilés — température entre 10°C et 30°C, hygrométrie conforme</div>
        <div class="check-item"><span class="check-icon">☑️</span> Humidité support plâtre ≤ 5% — bois ~12% ± 2% (mesure humidimètre)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Planéité support : écart ≤ 1mm/20cm et ≤ 5mm/2m (règle DTU)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Support propre, sec, sain, plan, cohésif (test bande adhésive)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Fissures et trous rebouchés et secs</div>
        <div class="check-item"><span class="check-icon">☑️</span> Impression de fond / fixateur appliqué si nécessaire</div>
        <div class="check-item"><span class="check-icon">☑️</span> Radiateurs déposés avant toute pose</div>
        <div class="check-item"><span class="check-icon">☑️</span> Tous les rouleaux proviennent du <strong>même lot de fabrication</strong></div>
        <div class="check-item"><span class="check-icon">☑️</span> Type de raccord vérifié sur l'étiquette</div>
        <div class="check-item"><span class="check-icon">☑️</span> Non-conformités notées PAR ÉCRIT au maître d'ouvrage (DTU 59.4 art. 4.2.1)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Éclairage du local équivalent à l'éclairage définitif</div>
      </div>
      <div class="controle-phase"><h3>🟡 PENDANT LES TRAVAUX</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Fil à plomb tracé — retracé tous les 4-5 lés</div>
        <div class="check-item"><span class="check-icon">☑️</span> Départ côté opposé à la fenêtre (source lumineuse principale)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Raccords de motif alignés entre chaque lé</div>
        <div class="check-item"><span class="check-icon">☑️</span> Marouflage soigné — pas de bulles ni de plis</div>
        <div class="check-item"><span class="check-icon">☑️</span> Joints jointifs — pas d'écart &gt; 1mm, pas de chevauchement visible</div>
        <div class="check-item"><span class="check-icon">☑️</span> Coupe double réalisée dans les angles rentrants et sortants</div>
        <div class="check-item"><span class="check-icon">☑️</span> Lame neuve pour tous les arasements</div>
        <div class="check-item"><span class="check-icon">☑️</span> Traces de colle éponge immédiatement</div>
        <div class="check-item"><span class="check-icon">☑️</span> Chutes conservées (angles, compléments)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Pose effectuée sur les angles adjacents (porte, fenêtre) selon technique</div>
      </div>
      <div class="controle-phase"><h3>🟢 APRÈS LES TRAVAUX</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Aucun décollement, aucun bord soulevé</div>
        <div class="check-item"><span class="check-icon">☑️</span> Raccords de motif corrects et alignés — vérification en lumière normale</div>
        <div class="check-item"><span class="check-icon">☑️</span> Surface plane, sans boursouflures après séchage complet (24-48h)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Pas de traces de colle visibles sur le revêtement</div>
        <div class="check-item"><span class="check-icon">☑️</span> Papier bien en bon état (se reporter DTU 59.4 page 25 — finition A ou B)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Nettoyage des salissures occasionnées par l'entreprise</div>
        <div class="check-item"><span class="check-icon">☑️</span> Enlèvement des déchets générés par l'entreprise</div>
        <div class="check-item"><span class="check-icon">☑️</span> Surface de référence présentée au maître d'ouvrage (préavis 15 jours)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Garantie 2 ans à compter de la réception (art. 1792-3 Code Civil)</div>
      </div>
      <div class="info-box blue"><div class="icon">📋</div><div class="content"><p><strong>Travaux après pose (DTU 59.4 art. 6) :</strong> Les autres corps d'état posent APRÈS la fin de la pose : poignées de porte, interrupteurs, prises, tringles à rideaux, mobiliers, robinetterie, chauffe-eau, remontage des radiateurs, ponçage des parquets.</p></div></div>
    </div>
  </div>

  <div id="papierpeint-lexique" class="sub-content">
    <div class="section-card">
      <h2>📝 Lexique — Papier Peint & Revêtements Muraux</h2>
      <div class="lexique-item"><strong>Arasement</strong><p>Coupe du surplus de papier peint en haut et en bas du lé, le long du plafond et de la plinthe. Nécessite une lame neuve pour une coupe nette.</p></div>
      <div class="lexique-item"><strong>Coupe double</strong><p>Technique obligatoire dans les angles. Deux lés superposés sont coupés simultanément à la règle bombée et au kicoup lame neuve, pour obtenir un joint parfait sans chevauchement ni écart.</p></div>
      <div class="lexique-item"><strong>DTU 59.4 (NF P74-204-1)</strong><p>Document Technique Unifié régissant la mise en œuvre des papiers peints et revêtements muraux à l'intérieur des bâtiments (neuf et rénovation). Définit les conditions d'exécution, la préparation des supports et les contrôles.</p></div>
      <div class="lexique-item"><strong>Duplex</strong><p>Papier peint constitué de deux papiers entre-collés avec une colle aqueuse. Plus résistant que le simplex, mais plus coûteux.</p></div>
      <div class="lexique-item"><strong>Expansé</strong><p>Papier peint avec couche de PVC expansé. Épais, résistant, effet de matière relief et gaufré, facile d'entretien.</p></div>
      <div class="lexique-item"><strong>Fil à plomb</strong><p>Outil ou tracé vertical servant de référence pour la pose du premier lé parfaitement droit. À retracer tous les 4-5 lés.</p></div>
      <div class="lexique-item"><strong>Fonçage</strong><p>Première étape de fabrication du papier peint : application d'une couche de fond uniforme sur le papier brut avant impression.</p></div>
      <div class="lexique-item"><strong>Gaufrage</strong><p>Opération de fabrication créant des reliefs dans le papier peint par estampage entre deux cylindres (mâle et femelle).</p></div>
      <div class="lexique-item"><strong>Grammage</strong><p>Masse du papier peint exprimée en g/m². Varie de 60 à 280 g/m² selon le type. Détermine le temps de trempage nécessaire.</p></div>
      <div class="lexique-item"><strong>Impression de fond (papier peint)</strong><p>Produit appliqué sur le support avant la pose, pour uniformiser l'absorption, éviter que la colle ne migre dans le mur et faciliter un éventuel décollage futur.</p></div>
      <div class="lexique-item"><strong>Intissé (non-tissé)</strong><p>Revêtement mural à base de fibres synthétiques et cellulose. La colle s'applique sur le MUR (pas sur le papier). Grande résistance, décollage facile sans produit, utilisable en pièces humides.</p></div>
      <div class="lexique-item"><strong>Kicoup</strong><p>Outil de coupe coulissant utilisé pour la coupe double. Doit impérativement être équipé d'une lame neuve. Ne jamais soulever l'outil une fois la coupe commencée.</p></div>
      <div class="lexique-item"><strong>Lé</strong><p>Bande de papier peint découpée à la hauteur de la pièce, augmentée d'un surplus de ~5 cm en haut et en bas pour les arasements et les raccords.</p></div>
      <div class="lexique-item"><strong>Lot de fabrication</strong><p>Ensemble de rouleaux produits en une même série. Il est impératif que tous les rouleaux d'une même pièce appartiennent au même lot pour éviter les différences de teinte.</p></div>
      <div class="lexique-item"><strong>Marouflage</strong><p>Action de lisser énergiquement le papier peint du centre vers les bords avec la spalter ou un rouleau, pour chasser les bulles d'air et assurer un contact parfait avec le mur.</p></div>
      <div class="lexique-item"><strong>NF P74-204</strong><p>Référence normative du DTU 59.4. Partie 1 = Cahier des clauses techniques. Partie 2 = Cahier des clauses spéciales (conditions administratives des marchés privés).</p></div>
      <div class="lexique-item"><strong>Raccord 0 (sans raccord)</strong><p>Papier uni ou à rayures verticales : les motifs ne sont pas coupés sur les bords. Aucune chute supplémentaire.</p></div>
      <div class="lexique-item"><strong>Raccord droit</strong><p>Le motif se reproduit tous les X cm sur une même ligne horizontale. Chutes = hauteur du raccord.</p></div>
      <div class="lexique-item"><strong>Raccord sauté (décalé)</strong><p>Le motif se reproduit décalé tous les 2 lés. Entraîne des chutes importantes. Travailler avec 2 rouleaux simultanément.</p></div>
      <div class="lexique-item"><strong>Règle bombée</strong><p>Règle à profil convexe utilisée lors de la coupe double. Placée sur l'axe de chevauchement pour guider le kicoup et obtenir une coupe nette.</p></div>
      <div class="lexique-item"><strong>Revêtement mural naturel</strong><p>Revêtement à base de fibres végétales (paille japonaise, bambou, sisal). Chaleureux et authentique mais sensible à l'humidité et aux UV. Usage décoratif résidentiel.</p></div>
      <div class="lexique-item"><strong>Revêtement vinyle contrecollé</strong><p>Revêtement mural professionnel (type Vescom, Buflon) constitué de PVC sur support textile. Résistant, lavable, grand choix de motifs. Utilisé dans les hôtels, bureaux, hôpitaux.</p></div>
      <div class="lexique-item"><strong>Simplex</strong><p>Papier peint traditionnel à une seule couche de papier imprimé. Facile à poser mais fragile, ne supporte pas l'humidité et opacité faible.</p></div>
      <div class="lexique-item"><strong>Spalter</strong><p>Brosse plate large utilisée pour maroufler le papier peint du centre vers les bords et chasser les bulles d'air.</p></div>
      <div class="lexique-item"><strong>Subjectile (papier peint)</strong><p>Support destiné à recevoir le revêtement mural : plâtre et dérivés, liants hydrauliques, bois. Doit être préparé selon DTU 59.1 et 59.4.</p></div>
      <div class="lexique-item"><strong>Surface de référence</strong><p>Zone représentative du chantier réalisée selon les spécifications du marché. L'entrepreneur informe le maître d'ouvrage 15 jours à l'avance. Conservée jusqu'à la réception des travaux.</p></div>
      <div class="lexique-item"><strong>Tack</strong><p>Adhérence initiale immédiate d'une colle au moment du contact. Un tack élevé est essentiel pour les revêtements lourds (vinyle épais, textiles).</p></div>
      <div class="lexique-item"><strong>Temps de trempage</strong><p>Durée pendant laquelle la colle est laissée à pénétrer le papier avant application. Varie de 2 à 5 min selon le grammage. Permet au papier de se ramollir pour s'étaler sans déchirures.</p></div>
      <div class="lexique-item"><strong>Toile de verre</strong><p>Revêtement mural en fibres de verre tissées, posé sur les murs fissurés pour les consolider, puis peint par-dessus.</p></div>
      <div class="lexique-item"><strong>Vinyle</strong><p>Papier peint constitué d'un support papier recouvert de PVC. Résistant aux frottements, UV, imperméable, lavable. Masque les défauts du support.</p></div>
    </div>
  </div>

  <div id="papierpeint-securite" class="sub-content">
    <div class="section-card">
      <h2>⛑️ Mémo Prévention & Sécurité — Papier Peint</h2>
      <div class="securite-grid">
        <div class="securite-card"><span class="icon">🏗️</span><h4>Travail en hauteur</h4><p>Échafaudage roulant ou plateau de travail obligatoire. Ne jamais travailler sur un escabeau instable. Bloquer les roues avant de monter. Vérifier avec l'app <strong>Check Chantier</strong> (OPPBTP).</p></div>
        <div class="securite-card"><span class="icon">✂️</span><h4>Outils coupants</h4><p>Kicoup et cutter = lames très tranchantes. EPI : gants anticoupures obligatoires. Changer les lames régulièrement. Préparer son geste avant de couper.</p></div>
        <div class="securite-card"><span class="icon">🔌</span><h4>Électricité</h4><p>Couper le courant avant de travailler autour des prises, interrupteurs et boîtiers électriques. Ne jamais appliquer de colle humide près d'une prise sous tension.</p></div>
        <div class="securite-card"><span class="icon">🌬️</span><h4>Ventilation</h4><p>Aérer le local pendant et après la pose. Les colles en dispersion aqueuse sont peu odorantes mais la ventilation est toujours obligatoire pour le séchage.</p></div>
        <div class="securite-card"><span class="icon">🦺</span><h4>TMS & Posture</h4><p>Alterner les postures (debout, bras levés). Prendre des pauses. Genouillères pour les travaux en bas de mur. Utiliser un table d'encollage à bonne hauteur.</p></div>
        <div class="securite-card"><span class="icon">💧</span><h4>Sol mouillé</h4><p>La colle renversée sur le sol crée des risques de glissade. Nettoyer immédiatement. Porter des chaussures de sécurité antidérapantes.</p></div>
        <div class="securite-card"><span class="icon">🧹</span><h4>Propreté chantier</h4><p>Garder le poste de travail propre. Éliminer les chutes de papier et les déchets de colle. Privilégier l'aspirateur au balai.</p></div>
        <div class="securite-card"><span class="icon">🧤</span><h4>Manipulation colles</h4><p>Gants de protection lors de la manipulation de colle. Certaines colles spéciales (résines) peuvent être irritantes. Consulter la FDS du produit.</p></div>
      </div>
      <div class="info-box orange"><div class="icon">⚠️</div><div class="content"><p><strong>Toile de verre :</strong> Les fibres de verre sont irritantes pour la peau, les yeux et les voies respiratoires. Masque FFP1, lunettes et manches longues obligatoires lors de la découpe et la pose.</p></div></div>
      <div class="info-box red"><div class="icon">🚫</div><div class="content"><p><strong>Avant d'intervenir sur un ancien revêtement :</strong> Vérifier l'absence d'amiante (bâtiments avant 1997) ou de plomb dans les peintures anciennes sous le papier peint. Sans formation, ne pas toucher !</p></div></div>
    </div>
  </div>
  <div id="papierpeint-quiz" class="sub-content">
    <div class="section-card"><h2>🎯 Questionnaire d'Acquis — Papier Peint & Revêtements Muraux</h2><p style="margin-bottom:20px;">Questions mixtes (simple → complexe) issues du cours et du DTU 59.4. <strong>10 questions</strong> — Score final en %.</p></div>
    <div class="quiz-container" id="quiz-papierpeint">
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">1</div><div class="q-text">Pour un revêtement intissé, où applique-t-on la colle ?</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="ppq1" value="a"> a) Sur le papier uniquement</label></li>
          <li><label><input type="radio" name="ppq1" value="b"> b) Sur le mur uniquement</label></li>
          <li><label><input type="radio" name="ppq1" value="c"> c) Sur le papier et le mur à la fois</label></li>
          <li><label><input type="radio" name="ppq1" value="d"> d) On n'utilise pas de colle pour l'intissé</label></li>
        </ul>
        <div class="answer-feedback" id="ppq1-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">2</div><div class="q-text">Selon le DTU 59.4, quelle est l'humidité maximale autorisée pour un support en plâtre avant pose de papier peint ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="ppq2" value="a"> a) 2%</label></li>
          <li><label><input type="radio" name="ppq2" value="b"> b) 5%</label></li>
          <li><label><input type="radio" name="ppq2" value="c"> c) 10%</label></li>
          <li><label><input type="radio" name="ppq2" value="d"> d) 15%</label></li>
        </ul>
        <div class="answer-feedback" id="ppq2-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">3</div><div class="q-text">Qu'est-ce que la "coupe double" et dans quel cas est-elle obligatoire ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="ppq3" value="a"> a) Couper le lé en deux avant de le poser — obligatoire sur les grands murs</label></li>
          <li><label><input type="radio" name="ppq3" value="b"> b) Technique de coupe de deux lés superposés simultanément — obligatoire dans les angles rentrants et sortants</label></li>
          <li><label><input type="radio" name="ppq3" value="c"> c) Couper le papier avec deux outils — pour les raccords droits</label></li>
          <li><label><input type="radio" name="ppq3" value="d"> d) Réaliser deux passages de cutter — pour les papiers épais</label></li>
        </ul>
        <div class="answer-feedback" id="ppq3-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">4</div><div class="q-text">Vrai ou Faux : Selon le DTU 59.4, en l'absence de précision dans le marché, la finition B est retenue.</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="ppq4" value="a"> ✅ Vrai</label></li>
          <li><label><input type="radio" name="ppq4" value="b"> ❌ Faux</label></li>
        </ul>
        <div class="answer-feedback" id="ppq4-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">5</div><div class="q-text">Mise en situation — Conditions non conformes</div><span class="q-level hard">🔴 Difficile</span></div>
        <div class="scenario-box"><h4>🏗️ Scénario :</h4><p>Tu arrives sur le chantier pour commencer la pose de papier peint. Tu constates que les murs en plâtre neuf présentent 8% d'humidité et la température du local est de 6°C. Que dois-tu faire selon le DTU 59.4 ?</p></div>
        <textarea class="open-answer" id="ppq5-answer" placeholder="Écris ta réponse ici..."></textarea>
        <button class="btn-check" onclick="checkOpen('ppq5')">Voir la correction 📋</button>
        <div class="answer-feedback" id="ppq5-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">6</div><div class="q-text">Quel type de raccord entraîne le plus de chutes et nécessite de travailler avec 2 rouleaux simultanément ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="ppq6" value="a"> a) Raccord 0 (sans raccord)</label></li>
          <li><label><input type="radio" name="ppq6" value="b"> b) Raccord droit</label></li>
          <li><label><input type="radio" name="ppq6" value="c"> c) Raccord sauté (décalé)</label></li>
          <li><label><input type="radio" name="ppq6" value="d"> d) Raccord panoramique</label></li>
        </ul>
        <div class="answer-feedback" id="ppq6-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">7</div><div class="q-text">Quelle est la durée de garantie minimale des travaux de pose de papier peint (loi du 4 janvier 1978) ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="ppq7" value="a"> a) 6 mois</label></li>
          <li><label><input type="radio" name="ppq7" value="b"> b) 1 an</label></li>
          <li><label><input type="radio" name="ppq7" value="c"> c) 2 ans</label></li>
          <li><label><input type="radio" name="ppq7" value="d"> d) 10 ans</label></li>
        </ul>
        <div class="answer-feedback" id="ppq7-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">8</div><div class="q-text">Selon le DTU 59.4, quel est l'écart maximal admis entre deux lés de papier peint ?</div><span class="q-level hard">🔴 Difficile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="ppq8" value="a"> a) 0 mm (joint parfaitement jointif)</label></li>
          <li><label><input type="radio" name="ppq8" value="b"> b) 1 mm maximum, sans chevauchement</label></li>
          <li><label><input type="radio" name="ppq8" value="c"> c) 3 mm</label></li>
          <li><label><input type="radio" name="ppq8" value="d"> d) 5 mm</label></li>
        </ul>
        <div class="answer-feedback" id="ppq8-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">9</div><div class="q-text">Parmi ces revêtements muraux, lequel est le plus adapté à un usage intensif en hôtel ou hôpital ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="ppq9" value="a"> a) Papier simplex</label></li>
          <li><label><input type="radio" name="ppq9" value="b"> b) Papier panoramique</label></li>
          <li><label><input type="radio" name="ppq9" value="c"> c) Revêtement vinyle contrecollé (type Vescom, Buflon)</label></li>
          <li><label><input type="radio" name="ppq9" value="d"> d) Revêtement naturel en paille japonaise</label></li>
        </ul>
        <div class="answer-feedback" id="ppq9-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">10</div><div class="q-text">Mise en situation — Non-conformités du support</div><span class="q-level hard">🔴 Difficile</span></div>
        <div class="scenario-box"><h4>🏗️ Scénario :</h4><p>Avant de commencer la pose, tu constates que les murs présentent des fissurations et que la planéité dépasse 7mm sous la règle de 2m. Quelle est la procédure à suivre selon le DTU 59.4 art. 4.2.1 ?</p></div>
        <textarea class="open-answer" id="ppq10-answer" placeholder="Décris la procédure réglementaire..."></textarea>
        <button class="btn-check" onclick="checkOpen('ppq10')">Voir la correction 📋</button>
        <div class="answer-feedback" id="ppq10-feedback"></div>
      </div>
      <div class="quiz-footer">
        <button class="btn-submit" onclick="submitQuiz('papierpeint', 10)">🎯 Calculer mon score !</button>
        <div class="score-display" id="score-papierpeint"></div>
      </div>
    </div>
  </div>
</div><!-- END PAPIER PEINT -->

<!-- ================================================== -->
<!-- ONGLET 4 : SOL SOUPLE -->
<!-- ================================================== -->
<div id="solsouple" class="tab-content">
  <div class="sub-tabs">
    <button class="sub-tab-btn active" onclick="showSub('solsouple', 'revision', this)">📖 Révision générale</button>
    <button class="sub-tab-btn" onclick="showSub('solsouple', 'controle', this)">✅ Contrôle travaux</button>
    <button class="sub-tab-btn" onclick="showSub('solsouple', 'lexique', this)">📝 Lexique</button>
    <button class="sub-tab-btn" onclick="showSub('solsouple', 'securite', this)">⛑️ Mémo sécurité</button>
    <button class="sub-tab-btn" onclick="showSub('solsouple', 'quiz', this)">🎯 Questionnaire d'acquis</button>
  </div>
  <div id="solsouple-revision" class="sub-content active">
    <div class="section-card">
      <h2>🟨 Sol Souple — Révision Générale</h2>
      <div class="img-grid">
        <div class="img-example"><img src="https://images.unsplash.com/photo-1600210492493-0946911123ea?w=400&q=80" alt="Sol vinyle"><div class="caption">📸 Lame vinyl LVT</div></div>
      </div>
      <h3>🔹 Les types de sols souples</h3>
      <table>
        <tr><th>Type</th><th>Matière</th><th>Usage</th></tr>
        <tr><td>PVC homogène</td><td>PVC massif</td><td>Hôpitaux, collectivités</td></tr>
        <tr><td>PVC hétérogène</td><td>PVC multicouche</td><td>Habitat, bureaux</td></tr>
        <tr><td>LVT (Luxury Vinyl Tile)</td><td>PVC rigide</td><td>Résidentiel haut de gamme</td></tr>
        <tr><td>Linoléum</td><td>Huile de lin, liège</td><td>Écologique, collectivités</td></tr>
        <tr><td>Moquette</td><td>Fibres textiles</td><td>Chambre, bureau</td></tr>
        <tr><td>Caoutchouc</td><td>Gomme naturelle/synthétique</td><td>Sport, industrie</td></tr>
      </table>
      <h3>🔹 Classement UPEC pour sols souples</h3>
      <p>Les sols souples ont également un classement UPEC. Il faut adapter le revêtement au local :</p>
      <table>
        <tr><th>Local</th><th>Classement minimum</th></tr>
        <tr><td>Chambre habitation</td><td>U2P2E0C0</td></tr>
        <tr><td>Couloir, séjour</td><td>U3P3E1C0</td></tr>
        <tr><td>Cuisine habitation</td><td>U3P3E2C1</td></tr>
        <tr><td>Salle de bain</td><td>U2P2E2C0</td></tr>
        <tr><td>Bureau collectif</td><td>U3P3E1C1</td></tr>
      </table>
      <h3>🔹 Préparation du support</h3>
      <div class="info-box orange"><div class="icon">⚠️</div><div class="content"><p>Le support doit être parfaitement <strong>plan, lisse, sec et propre</strong>. Toute irrégularité se verra à travers le revêtement souple (« télégraphie »). Utiliser un <strong>ragréage autolissant</strong> si nécessaire.</p></div></div>
      <h3>🔹 Désordres sols souples</h3>
      <div class="disorder-card"><h4>🔴 Décollements / remontées de bords</h4><p>Colle insuffisante, humidité remontante, mauvais dégraissage.</p><div class="solution"><strong>✅ Solution :</strong> Recoller avec colle adaptée, appliquer un lé de soudure si nécessaire, traiter l'humidité.</div></div>
      <div class="disorder-card"><h4>🔴 Télégraphie (marques visibles en surface)</h4><p>Support irrégulier sous le revêtement (relief, joints, etc.).</p><div class="solution"><strong>✅ Solution :</strong> Ragréage du support avant pose. Poncer si nécessaire.</div></div>
      <div class="disorder-card"><h4>🔴 Jaunissement / décoloration</h4><p>Migration de produits du support (plastifiant, bitume), UV.</p><div class="solution"><strong>✅ Solution :</strong> Utiliser une barrière anti-migration, choisir un revêtement adapté au support.</div></div>
    </div>
  </div>
  <div id="solsouple-controle" class="sub-content">
    <div class="section-card">
      <h2>✅ Contrôle des Travaux — Sol Souple</h2>
      <div class="controle-phase"><h3>🔵 AVANT</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Contrôler planéité : règle 2m, écart ≤ 3mm pour sols souples (plus exigeant que carrelage)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Taux d'humidité support ≤ 4% (CME carbure) pour PVC collé</div>
        <div class="check-item"><span class="check-icon">☑️</span> Support propre, dégraissé, sans aspérités ni saillies</div>
        <div class="check-item"><span class="check-icon">☑️</span> Ragréage si nécessaire (attendre durcissement complet)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Vérifier classement UPEC du revêtement vs usage du local</div>
      </div>
      <div class="controle-phase"><h3>🟡 PENDANT</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Temps de conditionnement du revêtement (24h à 20°C dans le local)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Appliquer la colle avec le bon peigne calibreur (dosage colle)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Respecter le temps d'ouverture de la colle avant pose</div>
        <div class="check-item"><span class="check-icon">☑️</span> Rouler avec le rouleau lourd (50 kg) juste après pose</div>
        <div class="check-item"><span class="check-icon">☑️</span> Réaliser les soudures à chaud des joints (PVC et linoléum)</div>
      </div>
      <div class="controle-phase"><h3>🟢 APRÈS</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Pas de décollements ni de bords soulevés</div>
        <div class="check-item"><span class="check-icon">☑️</span> Joints de soudure affleurants et de même teinte</div>
        <div class="check-item"><span class="check-icon">☑️</span> Absence de télégraphie (marques du support visible)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Plinthes ou barres de seuil proprement posées</div>
      </div>
    </div>
  </div>
  <div id="solsouple-lexique" class="sub-content">
    <div class="section-card">
      <h2>📝 Lexique — Sol Souple</h2>
      <div class="lexique-item"><strong>Autolissant (ragréage)</strong><p>Mortier fluide appliqué sur le sol pour corriger les irrégularités. Il s'étale seul par gravité.</p></div>
      <div class="lexique-item"><strong>CME (teneur en eau)</strong><p>Taux d'humidité d'un support mesuré au carbure de calcium. Limite : 4% pour pose de sol souple collé.</p></div>
      <div class="lexique-item"><strong>LVT (Luxury Vinyl Tile)</strong><p>Lame ou carreau en PVC rigide à haute résistance. Peut être cliqué ou collé.</p></div>
      <div class="lexique-item"><strong>Linoléum</strong><p>Revêtement naturel à base d'huile de lin, farines de bois et liège. Écologique et bactériostatique.</p></div>
      <div class="lexique-item"><strong>Plastifiant</strong><p>Additif incorporé au PVC pour lui conférer de la souplesse. Peut migrer et provoquer des taches.</p></div>
      <div class="lexique-item"><strong>Soudure à chaud</strong><p>Technique de jointoiement des lés de PVC à l'aide d'un cordon de soudure fondu par pistolet chaud.</p></div>
      <div class="lexique-item"><strong>Télégraphie</strong><p>Défaut où les irrégularités du support apparaissent en relief sous le revêtement souple.</p></div>
    </div>
  </div>
  <div id="solsouple-securite" class="sub-content">
    <div class="section-card">
      <h2>⛑️ Mémo Prévention & Sécurité — Sol Souple</h2>
      <div class="securite-grid">
        <div class="securite-card"><span class="icon">🌬️</span><h4>Ventilation</h4><p>Les colles de sols souples dégagent des solvants et COV. Ventiler obligatoirement.</p></div>
        <div class="securite-card"><span class="icon">🔥</span><h4>Risque incendie</h4><p>Colles solvantées inflammables. Pas de flamme nue, pas de cigarette.</p></div>
        <div class="securite-card"><span class="icon">🦺</span><h4>TMS genoux</h4><p>Genouillères obligatoires. Alterner les postures pour éviter les douleurs chroniques.</p></div>
        <div class="securite-card"><span class="icon">🧤</span><h4>Gants</h4><p>Gants nitrile pour manipulation des colles et solvants.</p></div>
        <div class="securite-card"><span class="icon">🌡️</span><h4>Pistolet soudure</h4><p>T° > 400°C. Ne jamais diriger la buse vers une personne. Attendre le refroidissement.</p></div>
      </div>
    </div>
  </div>
  <div id="solsouple-quiz" class="sub-content">
    <div class="section-card"><h2>🎯 Questionnaire d'Acquis — Sol Souple</h2></div>
    <div class="quiz-container" id="quiz-solsouple">
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">1</div><div class="q-text">Quel outil utilise-t-on pour mesurer le taux d'humidité d'un support avant pose de sol souple ?</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="ssq1" value="a"> a) Le niveau laser</label></li>
          <li><label><input type="radio" name="ssq1" value="b"> b) Le carbure de calcium (CME)</label></li>
          <li><label><input type="radio" name="ssq1" value="c"> c) La règle de 2 mètres</label></li>
          <li><label><input type="radio" name="ssq1" value="d"> d) Le manomètre</label></li>
        </ul>
        <div class="answer-feedback" id="ssq1-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">2</div><div class="q-text">Qu'est-ce que la "télégraphie" ?</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="ssq2" value="a"> a) Un type de sol souple</label></li>
          <li><label><input type="radio" name="ssq2" value="b"> b) Un défaut où les irrégularités du support apparaissent sous le revêtement</label></li>
          <li><label><input type="radio" name="ssq2" value="c"> c) Une technique de soudure</label></li>
          <li><label><input type="radio" name="ssq2" value="d"> d) Une norme de classement</label></li>
        </ul>
        <div class="answer-feedback" id="ssq2-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">3</div><div class="q-text">Vrai ou Faux : L'écart de planéité toléré pour un sol souple est de 5mm sous la règle de 2m (identique au carrelage).</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="ssq3" value="a"> ✅ Vrai</label></li>
          <li><label><input type="radio" name="ssq3" value="b"> ❌ Faux</label></li>
        </ul>
        <div class="answer-feedback" id="ssq3-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">4</div><div class="q-text">Quel est le rôle du rouleau lourd (50 kg) lors de la pose de sol souple ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="ssq4" value="a"> a) Couper le revêtement</label></li>
          <li><label><input type="radio" name="ssq4" value="b"> b) Bien mettre en contact le revêtement et la colle sur toute la surface</label></li>
          <li><label><input type="radio" name="ssq4" value="c"> c) Ragréer le support</label></li>
          <li><label><input type="radio" name="ssq4" value="d"> d) Souder les joints</label></li>
        </ul>
        <div class="answer-feedback" id="ssq4-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">5</div><div class="q-text">Le linoléum est un revêtement :</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="ssq5" value="a"> a) Synthétique à base de PVC</label></li>
          <li><label><input type="radio" name="ssq5" value="b"> b) Naturel à base d'huile de lin et de liège</label></li>
          <li><label><input type="radio" name="ssq5" value="c"> c) Minéral à base de ciment</label></li>
          <li><label><input type="radio" name="ssq5" value="d"> d) Textile à base de laine</label></li>
        </ul>
        <div class="answer-feedback" id="ssq5-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">6</div><div class="q-text">Pourquoi conditionne-t-on le revêtement souple 24h dans le local avant pose ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="ssq6" value="a"> a) Pour le laisser reposer après transport</label></li>
          <li><label><input type="radio" name="ssq6" value="b"> b) Pour qu'il s'adapte à la température et à l'humidité ambiante et évite les dilatations après pose</label></li>
          <li><label><input type="radio" name="ssq6" value="c"> c) Pour vérifier la couleur</label></li>
          <li><label><input type="radio" name="ssq6" value="d"> d) C'est une obligation réglementaire sans raison technique</label></li>
        </ul>
        <div class="answer-feedback" id="ssq6-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">7</div><div class="q-text">Mise en situation</div><span class="q-level hard">🔴 Difficile</span></div>
        <div class="scenario-box"><h4>🏗️ Scénario :</h4><p>Tu poses un PVC hétérogène dans un couloir de résidence (U3P3E1). 48h après, tu constates des bords qui se soulèvent. Donne les 3 causes possibles et la démarche de reprise.</p></div>
        <textarea class="open-answer" id="ssq7-answer" placeholder="Écris ta réponse ici..."></textarea>
        <button class="btn-check" onclick="checkOpen('ssq7')">Voir la correction 📋</button>
        <div class="answer-feedback" id="ssq7-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">8</div><div class="q-text">Quel est le taux d'humidité maximal autorisé d'un support béton pour poser un sol souple collé ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="ssq8" value="a"> a) 2%</label></li>
          <li><label><input type="radio" name="ssq8" value="b"> b) 4%</label></li>
          <li><label><input type="radio" name="ssq8" value="c"> c) 8%</label></li>
          <li><label><input type="radio" name="ssq8" value="d"> d) 10%</label></li>
        </ul>
        <div class="answer-feedback" id="ssq8-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">9</div><div class="q-text">Vrai ou Faux : La soudure à chaud des joints PVC est réalisée avec un pistolet thermique à environ 400°C.</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="ssq9" value="a"> ✅ Vrai</label></li>
          <li><label><input type="radio" name="ssq9" value="b"> ❌ Faux</label></li>
        </ul>
        <div class="answer-feedback" id="ssq9-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">10</div><div class="q-text">Pour une salle de sport avec roulage fréquent (chariots), quel classement UPEC minimum faut-il pour le sol ?</div><span class="q-level hard">🔴 Difficile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="ssq10" value="a"> a) U2P2E0C0</label></li>
          <li><label><input type="radio" name="ssq10" value="b"> b) U3P3E1C0</label></li>
          <li><label><input type="radio" name="ssq10" value="c"> c) U4P4E2C2</label></li>
          <li><label><input type="radio" name="ssq10" value="d"> d) U1P1E0C0</label></li>
        </ul>
        <div class="answer-feedback" id="ssq10-feedback"></div>
      </div>
      <div class="quiz-footer">
        <button class="btn-submit" onclick="submitQuiz('solsouple', 10)">🎯 Calculer mon score !</button>
        <div class="score-display" id="score-solsouple"></div>
      </div>
    </div>
  </div>
</div><!-- END SOL SOUPLE -->

<!-- ================================================== -->
<!-- ONGLETS 5-14 : VERSION CONDENSÉE MAIS COMPLÈTE -->
<!-- ================================================== -->

<!-- ONGLET 5 : CARREAUX DE PLÂTRE -->
<div id="carreauxplatre" class="tab-content">
  <div class="sub-tabs">
    <button class="sub-tab-btn active" onclick="showSub('carreauxplatre', 'revision', this)">📖 Révision générale</button>
    <button class="sub-tab-btn" onclick="showSub('carreauxplatre', 'controle', this)">✅ Contrôle travaux</button>
    <button class="sub-tab-btn" onclick="showSub('carreauxplatre', 'lexique', this)">📝 Lexique</button>
    <button class="sub-tab-btn" onclick="showSub('carreauxplatre', 'securite', this)">⛑️ Mémo sécurité</button>
    <button class="sub-tab-btn" onclick="showSub('carreauxplatre', 'quiz', this)">🎯 Questionnaire d'acquis</button>
  </div>
  <div id="carreauxplatre-revision" class="sub-content active">
    <div class="section-card">
      <h2>🧱 Carreaux de Plâtre — Révision Générale</h2>
      <div class="img-grid">
        <div class="img-example"><img src="https://images.unsplash.com/photo-1504307651254-35680f356dfd?w=400&q=80" alt="Construction cloison"><div class="caption">📸 Cloison en carreaux de plâtre</div></div>
      </div>
      <h3>🔹 Caractéristiques des carreaux de plâtre</h3>
      <p>Les carreaux de plâtre sont des éléments de construction préfabriqués en plâtre, utilisés pour réaliser des cloisons intérieures non porteuses.</p>
      <table>
        <tr><th>Type</th><th>Épaisseur</th><th>Usage</th></tr>
        <tr><td>Standard (S)</td><td>50 à 100 mm</td><td>Locaux secs (A0)</td></tr>
        <tr><td>Hydrofuge (H)</td><td>50 à 100 mm</td><td>Locaux humides (A2/A3)</td></tr>
        <tr><td>Alvéolaire</td><td>70 à 100 mm</td><td>Amélioration phonique</td></tr>
        <tr><td>Armé</td><td>50 à 100 mm</td><td>Résistance aux chocs renforcée</td></tr>
      </table>
      <h3>🔹 Dimensions courantes</h3>
      <p>Format standard : <strong>50 × 25 cm ou 66 × 50 cm</strong> (longueur × largeur). Épaisseur : 50, 60, 70 ou 100 mm selon isolation phonique souhaitée.</p>
      <h3>🔹 Mise en œuvre</h3>
      <div class="controle-phase">
        <div class="check-item"><span class="check-icon">1️⃣</span> Tracer l'implantation au sol et au plafond (fil à plomb, laser)</div>
        <div class="check-item"><span class="check-icon">2️⃣</span> Coller une bande mousse ou liège sur les profils périphériques (désolidarisation acoustique)</div>
        <div class="check-item"><span class="check-icon">3️⃣</span> Encoller les bords (plâtre gâché) et poser les carreaux en quinconce</div>
        <div class="check-item"><span class="check-icon">4️⃣</span> Maintenir les carreaux avec un coin en bois pendant la prise</div>
        <div class="check-item"><span class="check-icon">5️⃣</span> Enduire les joints à la barbotine de plâtre après prise</div>
        <div class="check-item"><span class="check-icon">6️⃣</span> Laisser sécher 48h minimum avant enduit ou peinture</div>
      </div>
      <h3>🔹 Avantages / Inconvénients</h3>
      <table>
        <tr><th>Avantages ✅</th><th>Inconvénients ❌</th></tr>
        <tr><td>Mise en œuvre rapide</td><td>Sensible à l'humidité (type S)</td></tr>
        <tr><td>Bonne résistance au feu</td><td>Masse importante (lourd)</td></tr>
        <tr><td>Bonne inertie thermique</td><td>Modifications difficiles</td></tr>
        <tr><td>Économique</td><td>Non démontable facilement</td></tr>
      </table>
    </div>
  </div>
  <div id="carreauxplatre-controle" class="sub-content">
    <div class="section-card">
      <h2>✅ Contrôle des Travaux — Carreaux de Plâtre</h2>
      <div class="controle-phase"><h3>🔵 AVANT</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Vérifier humidité locale ≤ 75% HR (carreaux standard)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Support sol propre, plan, résistant</div>
        <div class="check-item"><span class="check-icon">☑️</span> Tracer et reporter l'implantation avec précision</div>
        <div class="check-item"><span class="check-icon">☑️</span> Prévoir les passages de réseaux (câbles, tuyaux)</div>
      </div>
      <div class="controle-phase"><h3>🟡 PENDANT</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Pose en quinconce (joints décalés d'au moins 1/4 de carreau)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Aplomb et verticalité vérifiés au niveau</div>
        <div class="check-item"><span class="check-icon">☑️</span> Joints jointifs ou enduits de plâtre frais à chaque pose</div>
        <div class="check-item"><span class="check-icon">☑️</span> Bande de désolidarisation posée en périphérie</div>
      </div>
      <div class="controle-phase"><h3>🟢 APRÈS</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Planéité de la cloison (règle 2m, écart ≤ 5mm)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Verticalité (fil à plomb, écart ≤ 5mm sur 3m)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Pas de fissures aux joints</div>
        <div class="check-item"><span class="check-icon">☑️</span> Résistance à l'arrachement des fixations</div>
      </div>
    </div>
  </div>
  <div id="carreauxplatre-lexique" class="sub-content">
    <div class="section-card">
      <h2>📝 Lexique — Carreaux de Plâtre</h2>
      <div class="lexique-item"><strong>Barbotine</strong><p>Plâtre très fluide utilisé pour encoller les bords des carreaux.</p></div>
      <div class="lexique-item"><strong>Désolidarisation</strong><p>Isolation du mur des éléments de structure par bande mousse ou liège, pour éviter la transmission des vibrations.</p></div>
      <div class="lexique-item"><strong>HR (Humidité Relative)</strong><p>Taux d'humidité de l'air. Les carreaux standard ne doivent pas être posés si HR > 75%.</p></div>
      <div class="lexique-item"><strong>Quinconce</strong><p>Disposition en décalé des joints verticaux pour renforcer la résistance de la cloison.</p></div>
      <div class="lexique-item"><strong>Type H</strong><p>Carreau de plâtre hydrofugé. Résistant à l'humidité, utilisé en salles de bains et cuisines.</p></div>
    </div>
  </div>
  <div id="carreauxplatre-securite" class="sub-content">
    <div class="section-card">
      <h2>⛑️ Mémo Prévention & Sécurité — Carreaux de Plâtre</h2>
      <div class="securite-grid">
        <div class="securite-card"><span class="icon">😷</span><h4>Poussières de plâtre</h4><p>Masque FFP1 minimum lors des découpes et ponçages.</p></div>
        <div class="securite-card"><span class="icon">🦺</span><h4>Manutention</h4><p>Carreaux lourds (10-20 kg). Utiliser un diable et travailler à 2.</p></div>
        <div class="securite-card"><span class="icon">🥽</span><h4>Yeux</h4><p>Lunettes de protection pour les projections de plâtre.</p></div>
        <div class="securite-card"><span class="icon">🧤</span><h4>Mains</h4><p>Gants de protection : le plâtre est légèrement irritant.</p></div>
      </div>
    </div>
  </div>
  <div id="carreauxplatre-quiz" class="sub-content">
    <div class="section-card"><h2>🎯 Questionnaire d'Acquis — Carreaux de Plâtre</h2></div>
    <div class="quiz-container" id="quiz-carreauxplatre">
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">1</div><div class="q-text">Quel type de carreau de plâtre utilise-t-on dans une salle de bain ?</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="cpq1" value="a"> a) Type S (Standard)</label></li>
          <li><label><input type="radio" name="cpq1" value="b"> b) Type H (Hydrofugé)</label></li>
          <li><label><input type="radio" name="cpq1" value="c"> c) Type A (Alvéolaire)</label></li>
          <li><label><input type="radio" name="cpq1" value="d"> d) Type R (Armé)</label></li>
        </ul>
        <div class="answer-feedback" id="cpq1-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">2</div><div class="q-text">Qu'est-ce que la pose en quinconce ?</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="cpq2" value="a"> a) Une pose avec des joints tous alignés verticalement</label></li>
          <li><label><input type="radio" name="cpq2" value="b"> b) Une pose avec des joints décalés pour renforcer la cloison</label></li>
          <li><label><input type="radio" name="cpq2" value="c"> c) Une pose à l'horizontale</label></li>
          <li><label><input type="radio" name="cpq2" value="d"> d) Une pose sans joints</label></li>
        </ul>
        <div class="answer-feedback" id="cpq2-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">3</div><div class="q-text">Vrai ou Faux : Une cloison en carreaux de plâtre peut être porteuse.</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="cpq3" value="a"> ✅ Vrai</label></li>
          <li><label><input type="radio" name="cpq3" value="b"> ❌ Faux</label></li>
        </ul>
        <div class="answer-feedback" id="cpq3-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">4</div><div class="q-text">Quel est le rôle de la bande de désolidarisation placée en périphérie ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="cpq4" value="a"> a) Décorer les bords de la cloison</label></li>
          <li><label><input type="radio" name="cpq4" value="b"> b) Éviter la transmission des vibrations et améliorer l'isolation acoustique</label></li>
          <li><label><input type="radio" name="cpq4" value="c"> c) Renforcer la résistance au feu</label></li>
          <li><label><input type="radio" name="cpq4" value="d"> d) Imperméabiliser la jonction</label></li>
        </ul>
        <div class="answer-feedback" id="cpq4-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">5</div><div class="q-text">Combien de temps minimum faut-il attendre avant d'appliquer un enduit ou une peinture sur une cloison neuve en carreaux de plâtre ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="cpq5" value="a"> a) 2 heures</label></li>
          <li><label><input type="radio" name="cpq5" value="b"> b) 48 heures</label></li>
          <li><label><input type="radio" name="cpq5" value="c"> c) 28 jours</label></li>
          <li><label><input type="radio" name="cpq5" value="d"> d) 1 semaine</label></li>
        </ul>
        <div class="answer-feedback" id="cpq5-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">6</div><div class="q-text">Mise en situation</div><span class="q-level hard">🔴 Difficile</span></div>
        <div class="scenario-box"><h4>🏗️ Scénario :</h4><p>Tu dois créer une nouvelle salle de bain (local humide A3) avec des cloisons en carreaux de plâtre. Quelles précautions spécifiques dois-tu prendre pour ce type de local ?</p></div>
        <textarea class="open-answer" id="cpq6-answer" placeholder="Écris ta réponse ici..."></textarea>
        <button class="btn-check" onclick="checkOpen('cpq6')">Voir la correction 📋</button>
        <div class="answer-feedback" id="cpq6-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">7</div><div class="q-text">Quel est le format standard le plus courant d'un carreau de plâtre ?</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="cpq7" value="a"> a) 120 × 60 cm</label></li>
          <li><label><input type="radio" name="cpq7" value="b"> b) 50 × 25 cm ou 66 × 50 cm</label></li>
          <li><label><input type="radio" name="cpq7" value="c"> c) 30 × 30 cm</label></li>
          <li><label><input type="radio" name="cpq7" value="d"> d) 100 × 50 cm</label></li>
        </ul>
        <div class="answer-feedback" id="cpq7-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">8</div><div class="q-text">Quel avantage principal ont les carreaux de plâtre en matière de sécurité incendie ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="cpq8" value="a"> a) Ils sont ignifuges (ininflammables) grâce au plâtre</label></li>
          <li><label><input type="radio" name="cpq8" value="b"> b) Ils brûlent lentement</label></li>
          <li><label><input type="radio" name="cpq8" value="c"> c) Ils ne transmettent pas la fumée</label></li>
          <li><label><input type="radio" name="cpq8" value="d"> d) Ils résistent à l'explosion</label></li>
        </ul>
        <div class="answer-feedback" id="cpq8-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">9</div><div class="q-text">Vrai ou Faux : Les carreaux de plâtre standard (type S) peuvent être posés dans les douches sans traitement particulier.</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="cpq9" value="a"> ✅ Vrai</label></li>
          <li><label><input type="radio" name="cpq9" value="b"> ❌ Faux</label></li>
        </ul>
        <div class="answer-feedback" id="cpq9-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">10</div><div class="q-text">Qu'est-ce que la barbotine ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="cpq10" value="a"> a) Un type de carreau de plâtre alvéolaire</label></li>
          <li><label><input type="radio" name="cpq10" value="b"> b) Du plâtre très fluide utilisé pour encoller les bords des carreaux</label></li>
          <li><label><input type="radio" name="cpq10" value="c"> c) Un enduit de finition pour les joints</label></li>
          <li><label><input type="radio" name="cpq10" value="d"> d) Un outil de coupe du plâtre</label></li>
        </ul>
        <div class="answer-feedback" id="cpq10-feedback"></div>
      </div>
      <div class="quiz-footer">
        <button class="btn-submit" onclick="submitQuiz('carreauxplatre', 10)">🎯 Calculer mon score !</button>
        <div class="score-display" id="score-carreauxplatre"></div>
      </div>
    </div>
  </div>
</div><!-- END CARREAUX PLÂTRE -->

<!-- ONGLET 6 : CLOISON PLACO -->
<div id="cloison" class="tab-content">
  <div class="sub-tabs">
    <button class="sub-tab-btn active" onclick="showSub('cloison', 'revision', this)">📖 Révision générale</button>
    <button class="sub-tab-btn" onclick="showSub('cloison', 'controle', this)">✅ Contrôle travaux</button>
    <button class="sub-tab-btn" onclick="showSub('cloison', 'lexique', this)">📝 Lexique</button>
    <button class="sub-tab-btn" onclick="showSub('cloison', 'securite', this)">⛑️ Mémo sécurité</button>
    <button class="sub-tab-btn" onclick="showSub('cloison', 'quiz', this)">🎯 Questionnaire d'acquis</button>
  </div>
  <div id="cloison-revision" class="sub-content active">
    <div class="section-card">
      <h2>🏠 Cloison en Plaque de Plâtre — Révision Générale</h2>
      <div class="img-grid">
        <div class="img-example"><img src="https://images.unsplash.com/photo-1590490360182-c33d57733427?w=400&q=80" alt="Cloison placo"><div class="caption">📸 Montage ossature métallique cloison</div></div>
      </div>
      <h3>🔹 Principe de la cloison légère placo</h3>
      <p>La cloison en plaques de plâtre est composée d'une <strong>ossature métallique</strong> (rails + montants) habillée de chaque côté de <strong>plaques de plâtre</strong> (BA13, BA18…). Elle est légère, rapide à monter et démontable.</p>
      <h3>🔹 Les types de plaques</h3>
      <table>
        <tr><th>Plaque</th><th>Couleur bord</th><th>Usage</th></tr>
        <tr><td>BA13 standard</td><td>Gris</td><td>Cloisons, doublages intérieurs secs</td></tr>
        <tr><td>BA13 H (hydro)</td><td>Vert</td><td>Locaux humides (salle de bain, cuisine)</td></tr>
        <tr><td>BA13 F (feu)</td><td>Rose/Rouge</td><td>Protection incendie (EI)</td></tr>
        <tr><td>BA13 phonique</td><td>Bleu</td><td>Amélioration isolation acoustique</td></tr>
        <tr><td>BA18</td><td>Gris (18mm)</td><td>Résistance aux chocs renforcée</td></tr>
      </table>
      <h3>🔹 Composition d'une cloison type 72/48</h3>
      <div class="info-box blue"><div class="icon">🏗️</div><div class="content"><p>72/48 signifie : <strong>72 mm</strong> de largeur totale pour <strong>montant 48 mm</strong>. L'espace interne peut recevoir de la laine minérale pour l'isolation phonique.</p></div></div>
      <table>
        <tr><th>Désignation</th><th>Montant</th><th>Épaisseur totale</th></tr>
        <tr><td>48/36</td><td>36 mm</td><td>48 mm</td></tr>
        <tr><td>72/48</td><td>48 mm</td><td>72 mm</td></tr>
        <tr><td>98/70</td><td>70 mm</td><td>98 mm</td></tr>
        <tr><td>124/90</td><td>90 mm</td><td>124 mm</td></tr>
      </table>
      <h3>🔹 Étapes de mise en œuvre</h3>
      <div class="controle-phase">
        <div class="check-item"><span class="check-icon">1️⃣</span> Tracer l'implantation (sol, murs, plafond)</div>
        <div class="check-item"><span class="check-icon">2️⃣</span> Fixer les rails sol et plafond avec bande acoustique</div>
        <div class="check-item"><span class="check-icon">3️⃣</span> Poser les montants tous les 40 ou 60 cm</div>
        <div class="check-item"><span class="check-icon">4️⃣</span> Passer les réseaux avant fermeture</div>
        <div class="check-item"><span class="check-icon">5️⃣</span> Visser les plaques (vis TF 25 ou 35 mm)</div>
        <div class="check-item"><span class="check-icon">6️⃣</span> Enduire les joints (bande + enduit à joint)</div>
        <div class="check-item"><span class="check-icon">7️⃣</span> Poncer après séchage</div>
      </div>
    </div>
  </div>
  <div id="cloison-controle" class="sub-content">
    <div class="section-card">
      <h2>✅ Contrôle des Travaux — Cloison Placo</h2>
      <div class="controle-phase"><h3>🔵 AVANT</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Plans d'implantation validés</div>
        <div class="check-item"><span class="check-icon">☑️</span> Réseaux (électricité, plomberie) repérés</div>
        <div class="check-item"><span class="check-icon">☑️</span> Choix des plaques adapté au local (sèche, humide, feu, phonique)</div>
      </div>
      <div class="controle-phase"><h3>🟡 PENDANT</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Écartement des montants respecté (40 ou 60 cm entraxe)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Bande acoustique sous les rails</div>
        <div class="check-item"><span class="check-icon">☑️</span> Vis correctement enfoncées (tête affleurante, pas traversante)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Joints de plaques décalés entre les deux faces</div>
      </div>
      <div class="controle-phase"><h3>🟢 APRÈS</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Planéité : ≤ 5mm sous règle de 2m</div>
        <div class="check-item"><span class="check-icon">☑️</span> Verticalité (≤ 5mm sur 3m)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Joints invisibles, ponçage soigné</div>
        <div class="check-item"><span class="check-icon">☑️</span> Aucune vis apparente</div>
      </div>
    </div>
  </div>
  <div id="cloison-lexique" class="sub-content">
    <div class="section-card">
      <h2>📝 Lexique — Cloison Placo</h2>
      <div class="lexique-item"><strong>BA13</strong><p>Plaque de plâtre standard de 13mm. La désignation signifie Bord Aminci (BA) en millimètres d'épaisseur.</p></div>
      <div class="lexique-item"><strong>Rail</strong><p>Profilé métallique horizontal (U) fixé au sol et au plafond, dans lequel s'encastrent les montants.</p></div>
      <div class="lexique-item"><strong>Montant</strong><p>Profilé métallique vertical (C) inséré dans les rails, sur lesquels sont vissées les plaques.</p></div>
      <div class="lexique-item"><strong>Entraxe</strong><p>Distance entre les axes de deux montants consécutifs (40 ou 60 cm selon la configuration).</p></div>
      <div class="lexique-item"><strong>Bande acoustique</strong><p>Bande de mousse ou résilient posée sous les rails pour éviter la transmission des bruits d'impact.</p></div>
      <div class="lexique-item"><strong>Enduit à joint</strong><p>Produit utilisé pour masquer les joints entre plaques et les têtes de vis. Peut être en poudre ou en pâte.</p></div>
      <div class="lexique-item"><strong>Vis TF</strong><p>Vis à Tête Fraisée utilisée pour fixer les plaques sur l'ossature. TF25 (13mm), TF35 (double plaque).</p></div>
    </div>
  </div>
  <div id="cloison-securite" class="sub-content">
    <div class="section-card">
      <h2>⛑️ Mémo Prévention & Sécurité — Cloison Placo</h2>
      <div class="securite-grid">
        <div class="securite-card"><span class="icon">😷</span><h4>Poussières</h4><p>Masque FFP2 lors découpe des plaques (poussières de plâtre, fibres de verre si laine)</p></div>
        <div class="securite-card"><span class="icon">🥽</span><h4>Yeux</h4><p>Lunettes lors de la découpe à la scie ou à la rèpe.</p></div>
        <div class="securite-card"><span class="icon">🧤</span><h4>Mains</h4><p>Gants anti-coupures : les bords des profilés métalliques sont tranchants.</p></div>
        <div class="securite-card"><span class="icon">🦺</span><h4>Manutention</h4><p>Les plaques BA13 pèsent environ 10 kg/m². Travailler à deux pour les grandes dimensions.</p></div>
        <div class="securite-card"><span class="icon">🔌</span><h4>Électricité</h4><p>Repérer les câbles avant tout perçage dans cloison existante.</p></div>
      </div>
    </div>
  </div>
  <div id="cloison-quiz" class="sub-content">
    <div class="section-card"><h2>🎯 Questionnaire d'Acquis — Cloison Placo</h2></div>
    <div class="quiz-container" id="quiz-cloison">
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">1</div><div class="q-text">Que signifie "BA13" ?</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="clq1" value="a"> a) Bande Adhésive de 13 cm</label></li>
          <li><label><input type="radio" name="clq1" value="b"> b) Bord Aminci de 13 mm d'épaisseur</label></li>
          <li><label><input type="radio" name="clq1" value="c"> c) Béton Armé de 13 MPa</label></li>
          <li><label><input type="radio" name="clq1" value="d"> d) Bord Arrondi n°13</label></li>
        </ul>
        <div class="answer-feedback" id="clq1-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">2</div><div class="q-text">Quelle plaque choisir pour une cloison dans une salle de bain ?</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="clq2" value="a"> a) BA13 grise standard</label></li>
          <li><label><input type="radio" name="clq2" value="b"> b) BA13 verte hydrofugée</label></li>
          <li><label><input type="radio" name="clq2" value="c"> c) BA13 rose feu</label></li>
          <li><label><input type="radio" name="clq2" value="d"> d) BA18 bleue</label></li>
        </ul>
        <div class="answer-feedback" id="clq2-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">3</div><div class="q-text">Vrai ou Faux : L'entraxe standard des montants d'une cloison placo est 80 cm.</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="clq3" value="a"> ✅ Vrai</label></li>
          <li><label><input type="radio" name="clq3" value="b"> ❌ Faux (c'est 40 ou 60 cm)</label></li>
        </ul>
        <div class="answer-feedback" id="clq3-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">4</div><div class="q-text">Pourquoi faut-il décaler les joints des plaques entre les deux faces d'une cloison ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="clq4" value="a"> a) Pour faciliter le passage des câbles</label></li>
          <li><label><input type="radio" name="clq4" value="b"> b) Pour renforcer la rigidité de la cloison et éviter les fissures traversantes</label></li>
          <li><label><input type="radio" name="clq4" value="c"> c) Pour économiser du matériau</label></li>
          <li><label><input type="radio" name="clq4" value="d"> d) C'est une règle esthétique uniquement</label></li>
        </ul>
        <div class="answer-feedback" id="clq4-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">5</div><div class="q-text">Quel est le rôle de la bande acoustique placée sous les rails sol et plafond ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="clq5" value="a"> a) Coller le rail au sol</label></li>
          <li><label><input type="radio" name="clq5" value="b"> b) Empêcher la transmission des bruits d'impact structure à la cloison</label></li>
          <li><label><input type="radio" name="clq5" value="c"> c) Protéger le sol des rayures</label></li>
          <li><label><input type="radio" name="clq5" value="d"> d) Protéger contre l'humidité</label></li>
        </ul>
        <div class="answer-feedback" id="clq5-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">6</div><div class="q-text">Mise en situation</div><span class="q-level hard">🔴 Difficile</span></div>
        <div class="scenario-box"><h4>🏗️ Scénario :</h4><p>Un client veut améliorer l'isolation phonique entre sa chambre et le couloir. Tu vas refaire la cloison existante en placo. Quelles solutions techniques peux-tu lui proposer ?</p></div>
        <textarea class="open-answer" id="clq6-answer" placeholder="Écris ta réponse ici..."></textarea>
        <button class="btn-check" onclick="checkOpen('clq6')">Voir la correction 📋</button>
        <div class="answer-feedback" id="clq6-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">7</div><div class="q-text">Quel type de vis est utilisé pour fixer les plaques de plâtre sur l'ossature métallique ?</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="clq7" value="a"> a) Vis à bois TH</label></li>
          <li><label><input type="radio" name="clq7" value="b"> b) Vis à plâtre TF (Tête Fraisée)</label></li>
          <li><label><input type="radio" name="clq7" value="c"> c) Boulon M8</label></li>
          <li><label><input type="radio" name="clq7" value="d"> d) Clou de béton</label></li>
        </ul>
        <div class="answer-feedback" id="clq7-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">8</div><div class="q-text">Vrai ou Faux : Une cloison 72/48 a un montant de 72mm de large.</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="clq8" value="a"> ✅ Vrai</label></li>
          <li><label><input type="radio" name="clq8" value="b"> ❌ Faux (72mm = épaisseur totale, montant = 48mm)</label></li>
        </ul>
        <div class="answer-feedback" id="clq8-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">9</div><div class="q-text">Dans quel ordre doit-on réaliser les étapes d'une cloison placo ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="clq9" value="a"> a) Rails → plaques → montants → joints</label></li>
          <li><label><input type="radio" name="clq9" value="b"> b) Tracé → rails → montants → réseaux → plaques → joints</label></li>
          <li><label><input type="radio" name="clq9" value="c"> c) Plaques → montants → rails → tracé</label></li>
          <li><label><input type="radio" name="clq9" value="d"> d) Joints → plaques → réseaux → rails</label></li>
        </ul>
        <div class="answer-feedback" id="clq9-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">10</div><div class="q-text">Quelle est la tolérance de planéité d'une cloison placo finie ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="clq10" value="a"> a) 2mm sous règle de 2m</label></li>
          <li><label><input type="radio" name="clq10" value="b"> b) 5mm sous règle de 2m</label></li>
          <li><label><input type="radio" name="clq10" value="c"> c) 10mm sous règle de 2m</label></li>
          <li><label><input type="radio" name="clq10" value="d"> d) Aucune tolérance</label></li>
        </ul>
        <div class="answer-feedback" id="clq10-feedback"></div>
      </div>
      <div class="quiz-footer">
        <button class="btn-submit" onclick="submitQuiz('cloison', 10)">🎯 Calculer mon score !</button>
        <div class="score-display" id="score-cloison"></div>
      </div>
    </div>
  </div>
</div><!-- END CLOISON -->

<!-- ONGLET 7: DOUBLAGE -->
<div id="doublage" class="tab-content">
  <div class="sub-tabs">
    <button class="sub-tab-btn active" onclick="showSub('doublage', 'revision', this)">📖 Révision générale</button>
    <button class="sub-tab-btn" onclick="showSub('doublage', 'controle', this)">✅ Contrôle travaux</button>
    <button class="sub-tab-btn" onclick="showSub('doublage', 'lexique', this)">📝 Lexique</button>
    <button class="sub-tab-btn" onclick="showSub('doublage', 'securite', this)">⛑️ Mémo sécurité</button>
    <button class="sub-tab-btn" onclick="showSub('doublage', 'quiz', this)">🎯 Questionnaire d'acquis</button>
  </div>
  <div id="doublage-revision" class="sub-content active">
    <div class="section-card">
      <h2>🧊 Doublage — Révision Générale</h2>
      <h3>🔹 Définition</h3>
      <p>Le doublage est un revêtement intérieur appliqué contre un mur existant (façade ou refend) pour améliorer l'isolation thermique et/ou acoustique, sans modifier la structure.</p>
      <h3>🔹 Les systèmes de doublage</h3>
      <table>
        <tr><th>Système</th><th>Description</th><th>Avantage</th></tr>
        <tr><td>Complexe de doublage (plaque + isolant)</td><td>Plaque plâtre + PSE ou laine collée en usine</td><td>Rapide, précis, peu de place</td></tr>
        <tr><td>Doublage sur ossature</td><td>Rail + montants + isolant + plaque</td><td>Meilleure isolation phonique</td></tr>
        <tr><td>Doublage collé</td><td>Plaque collée au plot de plâtre ou colle</td><td>Économique, sans ossature</td></tr>
      </table>
      <h3>🔹 Isolation associée au doublage</h3>
      <table>
        <tr><th>Isolant</th><th>λ (conductivité)</th><th>Usage</th></tr>
        <tr><td>Laine de verre</td><td>0,032 à 0,04 W/m.K</td><td>Thermique et acoustique</td></tr>
        <tr><td>Laine de roche</td><td>0,034 à 0,04 W/m.K</td><td>Thermique, acoustique, feu</td></tr>
        <tr><td>PSE (polystyrène expansé)</td><td>0,030 à 0,038 W/m.K</td><td>Thermique principalement</td></tr>
        <tr><td>Polyuréthane</td><td>0,020 à 0,025 W/m.K</td><td>Haute performance thermique</td></tr>
      </table>
      <h3>🔹 Pont thermique</h3>
      <div class="info-box orange"><div class="icon">🌡️</div><div class="content"><p>Un <strong>pont thermique</strong> est une zone où l'isolation est interrompue (angle, plancher, refend), créant une déperdition de chaleur et un risque de condensation et moisissures. Le doublage doit couvrir les ponts thermiques.</p></div></div>
    </div>
  </div>
  <div id="doublage-controle" class="sub-content">
    <div class="section-card">
      <h2>✅ Contrôle des Travaux — Doublage</h2>
      <div class="controle-phase"><h3>🔵 AVANT</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Vérifier que le mur support est sain, sec, sans remontées capillaires</div>
        <div class="check-item"><span class="check-icon">☑️</span> Traiter les zones humides si nécessaire avant doublage</div>
        <div class="check-item"><span class="check-icon">☑️</span> Choisir le système adapté (acoustique, thermique, mixte)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Prendre en compte la résistance thermique R requise (RT2012/RE2020)</div>
      </div>
      <div class="controle-phase"><h3>🟡 PENDANT</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Ossature verticale bien d'aplomb</div>
        <div class="check-item"><span class="check-icon">☑️</span> Isolant sans ponts thermiques (joints décalés, isolant continu)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Pare-vapeur posé côté chaud (intérieur) si nécessaire</div>
        <div class="check-item"><span class="check-icon">☑️</span> Fixations aux plots ou rails bien réparties</div>
      </div>
      <div class="controle-phase"><h3>🟢 APRÈS</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Planéité et aplomb de la finition</div>
        <div class="check-item"><span class="check-icon">☑️</span> Jonctions angles et périphérie propres</div>
        <div class="check-item"><span class="check-icon">☑️</span> Perte de surface habitable conforme au plan</div>
      </div>
    </div>
  </div>
  <div id="doublage-lexique" class="sub-content">
    <div class="section-card">
      <h2>📝 Lexique — Doublage</h2>
      <div class="lexique-item"><strong>Complexe de doublage</strong><p>Produit industriel associant en usine une plaque de plâtre et un isolant (PSE, PU ou laine minérale).</p></div>
      <div class="lexique-item"><strong>Lambda (λ)</strong><p>Conductivité thermique d'un matériau en W/m.K. Plus λ est faible, meilleur est l'isolant.</p></div>
      <div class="lexique-item"><strong>Pare-vapeur</strong><p>Film plastique ou membrane placé du côté chaud de l'isolant pour empêcher la migration de vapeur d'eau vers l'isolant.</p></div>
      <div class="lexique-item"><strong>Pont thermique</strong><p>Zone de l'enveloppe où l'isolation est interrompue, provoquant une déperdition thermique localisée.</p></div>
      <div class="lexique-item"><strong>RE2020</strong><p>Réglementation Environnementale 2020. Remplace la RT2012, fixe les exigences de performance énergétique des bâtiments neufs.</p></div>
      <div class="lexique-item"><strong>Résistance thermique R</strong><p>Mesure de la capacité d'un matériau à s'opposer au flux de chaleur. R = e/λ (épaisseur/conductivité). Exprimée en m².K/W.</p></div>
    </div>
  </div>
  <div id="doublage-securite" class="sub-content">
    <div class="section-card">
      <h2>⛑️ Mémo Prévention & Sécurité — Doublage</h2>
      <div class="securite-grid">
        <div class="securite-card"><span class="icon">😷</span><h4>Fibres minérales</h4><p>Masque FFP1 minimum lors de la manipulation de laine de verre ou de roche.</p></div>
        <div class="securite-card"><span class="icon">🧤</span><h4>Laine minérale</h4><p>Gants + manches longues : les fibres provoquent des irritations cutanées.</p></div>
        <div class="securite-card"><span class="icon">🥽</span><h4>Protection visuelle</h4><p>Lunettes lors de la découpe et pose pour éviter les projections de fibres.</p></div>
        <div class="securite-card"><span class="icon">🌬️</span><h4>Ventilation</h4><p>Aérer lors de l'utilisation des colles et des mousses polyuréthane.</p></div>
      </div>
    </div>
  </div>
  <div id="doublage-quiz" class="sub-content">
    <div class="section-card"><h2>🎯 Questionnaire d'Acquis — Doublage</h2></div>
    <div class="quiz-container" id="quiz-doublage">
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">1</div><div class="q-text">Qu'est-ce qu'un "complexe de doublage" ?</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="dq1" value="a"> a) Un mélange de deux types de plaques</label></li>
          <li><label><input type="radio" name="dq1" value="b"> b) Une plaque de plâtre associée à un isolant fabriqué ensemble en usine</label></li>
          <li><label><input type="radio" name="dq1" value="c"> c) Un doublage réalisé en deux étapes</label></li>
          <li><label><input type="radio" name="dq1" value="d"> d) Un type d'ossature double</label></li>
        </ul>
        <div class="answer-feedback" id="dq1-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">2</div><div class="q-text">Quel isolant offre la meilleure performance thermique (λ le plus faible) ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="dq2" value="a"> a) Laine de verre (λ = 0,04)</label></li>
          <li><label><input type="radio" name="dq2" value="b"> b) Polyuréthane (λ = 0,022)</label></li>
          <li><label><input type="radio" name="dq2" value="c"> c) PSE (λ = 0,035)</label></li>
          <li><label><input type="radio" name="dq2" value="d"> d> Laine de roche (λ = 0,038)</label></li>
        </ul>
        <div class="answer-feedback" id="dq2-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">3</div><div class="q-text">Vrai ou Faux : Le pare-vapeur se pose du côté froid (extérieur) de l'isolant.</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="dq3" value="a"> ✅ Vrai</label></li>
          <li><label><input type="radio" name="dq3" value="b"> ❌ Faux (il se pose côté chaud = intérieur)</label></li>
        </ul>
        <div class="answer-feedback" id="dq3-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">4</div><div class="q-text">Qu'est-ce qu'un pont thermique ?</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="dq4" value="a"> a) Une zone bien isolée de la paroi</label></li>
          <li><label><input type="radio" name="dq4" value="b"> b) Une zone où l'isolation est interrompue, créant une déperdition de chaleur</label></li>
          <li><label><input type="radio" name="dq4" value="c"> c) Un pont de communication thermique entre pièces</label></li>
          <li><label><input type="radio" name="dq4" value="d"> d) Un matériau de chauffage intégré au mur</label></li>
        </ul>
        <div class="answer-feedback" id="dq4-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">5</div><div class="q-text">Mise en situation</div><span class="q-level hard">🔴 Difficile</span></div>
        <div class="scenario-box"><h4>🏗️ Scénario :</h4><p>Dans un appartement, des taches de moisissures apparaissent aux angles entre murs et plafond après un doublage. Quelle en est la cause probable et quelle solution proposer ?</p></div>
        <textarea class="open-answer" id="dq5-answer" placeholder="Écris ta réponse ici..."></textarea>
        <button class="btn-check" onclick="checkOpen('dq5')">Voir la correction 📋</button>
        <div class="answer-feedback" id="dq5-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">6</div><div class="q-text">Quelle réglementation encadre la performance thermique des bâtiments neufs depuis 2022 ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="dq6" value="a"> a) RT2012</label></li>
          <li><label><input type="radio" name="dq6" value="b"> b) RE2020</label></li>
          <li><label><input type="radio" name="dq6" value="c"> c) DTU 2020</label></li>
          <li><label><input type="radio" name="dq6" value="d"> d) NF EN 2020</label></li>
        </ul>
        <div class="answer-feedback" id="dq6-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">7</div><div class="q-text">Quel isolant est particulièrement adapté pour les exigences incendie en plus du thermique ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="dq7" value="a"> a) PSE (polystyrène expansé)</label></li>
          <li><label><input type="radio" name="dq7" value="b"> b) Polyuréthane</label></li>
          <li><label><input type="radio" name="dq7" value="c"> c) Laine de roche</label></li>
          <li><label><input type="radio" name="dq7" value="d"> d> Liège expansé</label></li>
        </ul>
        <div class="answer-feedback" id="dq7-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">8</div><div class="q-text">Vrai ou Faux : Le doublage réduit toujours légèrement la superficie de la pièce.</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="dq8" value="a"> ✅ Vrai</label></li>
          <li><label><input type="radio" name="dq8" value="b"> ❌ Faux</label></li>
        </ul>
        <div class="answer-feedback" id="dq8-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">9</div><div class="q-text">R = e/λ. Pour un isolant de 10 cm d'épaisseur avec λ = 0,04, quelle est la valeur de R ?</div><span class="q-level hard">🔴 Difficile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="dq9" value="a"> a) 0,4 m².K/W</label></li>
          <li><label><input type="radio" name="dq9" value="b"> b) 2,5 m².K/W</label></li>
          <li><label><input type="radio" name="dq9" value="c"> c) 25 m².K/W</label></li>
          <li><label><input type="radio" name="dq9" value="d"> d) 4 m².K/W</label></li>
        </ul>
        <div class="answer-feedback" id="dq9-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">10</div><div class="q-text">Dans le doublage collé, comment fixe-t-on le complexe sur le mur ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="dq10" value="a"> a) Par vissage sur chevilles</label></li>
          <li><label><input type="radio" name="dq10" value="b"> b) Par des plots de plâtre ou de colle disposés sur le mur</label></li>
          <li><label><input type="radio" name="dq10" value="c"> c) Par des agrafes métalliques</label></li>
          <li><label><input type="radio" name="dq10" value="d"> d) Par thermosoudure</label></li>
        </ul>
        <div class="answer-feedback" id="dq10-feedback"></div>
      </div>
      <div class="quiz-footer">
        <button class="btn-submit" onclick="submitQuiz('doublage', 10)">🎯 Calculer mon score !</button>
        <div class="score-display" id="score-doublage"></div>
      </div>
    </div>
  </div>
</div><!-- END DOUBLAGE -->

<!-- ONGLETS 8-14 : STRUCTURE GÉNÉRIQUE COMPLÈTE -->

<!-- ONGLET 8: PLAFOND SUSPENDU PLACO -->
<div id="plafondsuspendu" class="tab-content">
  <div class="sub-tabs">
    <button class="sub-tab-btn active" onclick="showSub('plafondsuspendu', 'revision', this)">📖 Révision générale</button>
    <button class="sub-tab-btn" onclick="showSub('plafondsuspendu', 'controle', this)">✅ Contrôle travaux</button>
    <button class="sub-tab-btn" onclick="showSub('plafondsuspendu', 'lexique', this)">📝 Lexique</button>
    <button class="sub-tab-btn" onclick="showSub('plafondsuspendu', 'securite', this)">⛑️ Mémo sécurité</button>
    <button class="sub-tab-btn" onclick="showSub('plafondsuspendu', 'quiz', this)">🎯 Questionnaire d'acquis</button>
  </div>
  <div id="plafondsuspendu-revision" class="sub-content active">
    <div class="section-card">
      <h2>⬜ Plafond Suspendu en Placo — Révision Générale</h2>
      <div class="img-grid">
        <div class="img-example"><img src="https://images.unsplash.com/photo-1497366216548-37526070297c?w=400&q=80" alt="Plafond suspendu"><div class="caption">📸 Plafond suspendu en plaques de plâtre</div></div>
      </div>
      <h3>🔹 Principe du plafond suspendu placo</h3>
      <p>Le plafond suspendu placo est une ossature métallique suspendue au plafond existant (dalle béton ou charpente), sur laquelle sont vissées des plaques de plâtre. Il permet de masquer les réseaux, d'améliorer isolation et acoustique, et de corriger les irrégularités.</p>
      <h3>🔹 Éléments constitutifs</h3>
      <table>
        <tr><th>Élément</th><th>Description</th></tr>
        <tr><td>Fourrure (F530)</td><td>Profilé métallique horizontal sur lequel sont vissées les plaques</td></tr>
        <tr><td>Suspente</td><td>Pince ou fil métallique reliant la fourrure au plafond</td></tr>
        <tr><td>Rail de rive (CD)</td><td>Profilé périphérique fixé aux murs</td></tr>
        <tr><td>Plaque BA13</td><td>Revêtement final vissé sur la fourrure</td></tr>
        <tr><td>Laine minérale</td><td>Isolant posé au-dessus des fourrures</td></tr>
      </table>
      <h3>🔹 Types de structures</h3>
      <table>
        <tr><th>Structure</th><th>Description</th><th>Usage</th></tr>
        <tr><td>Fourrures simples</td><td>Fourrures espacées de 60 cm</td><td>Pose simple (BA13)</td></tr>
        <tr><td>Fourrures croisées</td><td>Double réseau de fourrures</td><td>Amélioration acoustique</td></tr>
        <tr><td>Ossature de grande hauteur</td><td>Tiges filetées longues</td><td>Grande hauteur sous dalle</td></tr>
      </table>
      <h3>🔹 Niveaux et mise à hauteur</h3>
      <div class="info-box blue"><div class="icon">📐</div><div class="content"><p>Le niveau du plafond est défini par un <strong>repère laser</strong> ou niveau à bulle. Les suspentes sont réglées une à une. La tolérance de planéité est de <strong>±3mm sous règle de 2m</strong>.</p></div></div>
    </div>
  </div>
  <div id="plafondsuspendu-controle" class="sub-content">
    <div class="section-card">
      <h2>✅ Contrôle des Travaux — Plafond Suspendu Placo</h2>
      <div class="controle-phase"><h3>🔵 AVANT</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Résistance de la dalle vérifiée (supports de suspentes)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Réseaux (électricité, ventilation, plomberie) prévus et positionnés</div>
        <div class="check-item"><span class="check-icon">☑️</span> Hauteur finale définie (respect hauteur réglementaire min 2,20m)</div>
      </div>
      <div class="controle-phase"><h3>🟡 PENDANT</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Suspentes espacées correctement (entraxe ≤ 1,20m)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Fourrures posées perpendiculairement aux joints des plaques</div>
        <div class="check-item"><span class="check-icon">☑️</span> Niveau laser utilisé pour la mise à hauteur</div>
        <div class="check-item"><span class="check-icon">☑️</span> Bande de désolidarisation sur le rail de rive</div>
      </div>
      <div class="controle-phase"><h3>🟢 APRÈS</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Planéité ±3mm sous règle 2m</div>
        <div class="check-item"><span class="check-icon">☑️</span> Joints soignés, ponçage impeccable</div>
        <div class="check-item"><span class="check-icon">☑️</span> Réservations pour luminaires et bouches VMC correctes</div>
      </div>
    </div>
  </div>
  <div id="plafondsuspendu-lexique" class="sub-content">
    <div class="section-card">
      <h2>📝 Lexique — Plafond Suspendu Placo</h2>
      <div class="lexique-item"><strong>Fourrure (F530)</strong><p>Profilé métallique en U ou C fixé horizontalement sur les suspentes. Support de vissage des plaques.</p></div>
      <div class="lexique-item"><strong>Suspente</strong><p>Élément de liaison entre le plafond porteur (dalle) et la fourrure. Réglable en hauteur.</p></div>
      <div class="lexique-item"><strong>Rail de rive (CD)</strong><p>Profil en L fixé en périphérie sur les murs pour soutenir les extrémités des fourrures.</p></div>
      <div class="lexique-item"><strong>Entraxe des fourrures</strong><p>Distance entre axes de deux fourrures successives. Généralement 40 à 60 cm.</p></div>
      <div class="lexique-item"><strong>Hauteur sous plafond (HSP)</strong><p>Distance entre le sol fini et la face inférieure du plafond. Minimum réglementaire : 2,20 m en logement.</p></div>
    </div>
  </div>
  <div id="plafondsuspendu-securite" class="sub-content">
    <div class="section-card">
      <h2>⛑️ Mémo Prévention & Sécurité — Plafond Suspendu</h2>
      <div class="securite-grid">
        <div class="securite-card"><span class="icon">🏗️</span><h4>Travail en hauteur</h4><p>Échafaudage roulant ou plateau de travail obligatoire. Jamais sur escabeau instable.</p></div>
        <div class="securite-card"><span class="icon">😷</span><h4>Poussières / fibres</h4><p>Masque FFP2 lors manipulation laine minérale et découpe plaques.</p></div>
        <div class="securite-card"><span class="icon">🔌</span><h4>Électricité</h4><p>Vérifier l'absence de tension dans les réseaux avant tout travail dans le vide de plafond.</p></div>
        <div class="securite-card"><span class="icon">🥽</span><h4>Projections</h4><p>Lunettes obligatoires lors des travaux en plafond (chutes de poussières, copeaux).</p></div>
        <div class="securite-card"><span class="icon">🦺</span><h4>Port du casque</h4><p>Casque recommandé si risque de chute d'objets (fixations, éléments divers).</p></div>
      </div>
    </div>
  </div>
  <div id="plafondsuspendu-quiz" class="sub-content">
    <div class="section-card"><h2>🎯 Questionnaire d'Acquis — Plafond Suspendu Placo</h2></div>
    <div class="quiz-container" id="quiz-plafondsuspendu">
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">1</div><div class="q-text">Quel est le rôle de la suspente dans un plafond suspendu ?</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="psq1" value="a"> a) Maintenir les plaques entre elles</label></li>
          <li><label><input type="radio" name="psq1" value="b"> b) Relier la fourrure à la structure porteuse (dalle ou charpente)</label></li>
          <li><label><input type="radio" name="psq1" value="c"> c) Fixer les rails de rive aux murs</label></li>
          <li><label><input type="radio" name="psq1" value="d"> d) Soutenir l'isolant</label></li>
        </ul>
        <div class="answer-feedback" id="psq1-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">2</div><div class="q-text">Quelle est la hauteur minimale réglementaire sous plafond en logement ?</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="psq2" value="a"> a) 1,80 m</label></li>
          <li><label><input type="radio" name="psq2" value="b"> b) 2,20 m</label></li>
          <li><label><input type="radio" name="psq2" value="c"> c) 2,50 m</label></li>
          <li><label><input type="radio" name="psq2" value="d"> d) 3,00 m</label></li>
        </ul>
        <div class="answer-feedback" id="psq2-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">3</div><div class="q-text">Vrai ou Faux : La tolérance de planéité d'un plafond suspendu placo est de 5mm sous règle de 2m.</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="psq3" value="a"> ✅ Vrai</label></li>
          <li><label><input type="radio" name="psq3" value="b"> ❌ Faux (c'est ±3mm)</label></li>
        </ul>
        <div class="answer-feedback" id="psq3-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">4</div><div class="q-text">Pourquoi place-t-on une bande de désolidarisation sur le rail de rive ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="psq4" value="a"> a) Pour améliorer l'esthétique</label></li>
          <li><label><input type="radio" name="psq4" value="b"> b) Pour éviter la transmission des vibrations de la structure au plafond</label></li>
          <li><label><input type="radio" name="psq4" value="c"> c) Pour faciliter le démontage</label></li>
          <li><label><input type="radio" name="psq4" value="d"> d) Pour imperméabiliser le joint</label></li>
        </ul>
        <div class="answer-feedback" id="psq4-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">5</div><div class="q-text">Dans quel sens pose-t-on les fourrures par rapport aux joints de plaques ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="psq5" value="a"> a) Dans le même sens que les joints</label></li>
          <li><label><input type="radio" name="psq5" value="b"> b) Perpendiculairement aux joints</label></li>
          <li><label><input type="radio" name="psq5" value="c"> c) En diagonale</label></li>
          <li><label><input type="radio" name="psq5" value="d"> d) Le sens n'a pas d'importance</label></li>
        </ul>
        <div class="answer-feedback" id="psq5-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">6</div><div class="q-text">Mise en situation</div><span class="q-level hard">🔴 Difficile</span></div>
        <div class="scenario-box"><h4>🏗️ Scénario :</h4><p>Après la pose d'un plafond suspendu placo, tu constates des zones qui "flambent" (ondulent). Quelles en sont les causes et comment les prévenir ?</p></div>
        <textarea class="open-answer" id="psq6-answer" placeholder="Écris ta réponse ici..."></textarea>
        <button class="btn-check" onclick="checkOpen('psq6')">Voir la correction 📋</button>
        <div class="answer-feedback" id="psq6-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">7</div><div class="q-text">Quel outil utilise-t-on pour mettre les fourrures à la même hauteur ?</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="psq7" value="a"> a) Le mètre ruban</label></li>
          <li><label><input type="radio" name="psq7" value="b"> b) Le niveau laser</label></li>
          <li><label><input type="radio" name="psq7" value="c"> c) La règle de 2m</label></li>
          <li><label><input type="radio" name="psq7" value="d"> d) Le fil à plomb</label></li>
        </ul>
        <div class="answer-feedback" id="psq7-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">8</div><div class="q-text">Vrai ou Faux : On peut travailler à la pose d'un plafond suspendu sur un simple escabeau.</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="psq8" value="a"> ✅ Vrai</label></li>
          <li><label><input type="radio" name="psq8" value="b"> ❌ Faux (échafaudage obligatoire)</label></li>
        </ul>
        <div class="answer-feedback" id="psq8-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">9</div><div class="q-text">Dans un plafond suspendu avec isolation acoustique, que met-on au-dessus des fourrures ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="psq9" value="a"> a) Du sable</label></li>
          <li><label><input type="radio" name="psq9" value="b"> b) De la laine minérale</label></li>
          <li><label><input type="radio" name="psq9" value="c"> c) Un pare-vapeur uniquement</label></li>
          <li><label><input type="radio" name="psq9" value="d"> d) Du béton allégé</label></li>
        </ul>
        <div class="answer-feedback" id="psq9-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">10</div><div class="q-text">Quelle est la différence principale entre un plafond suspendu et un plafond autoportant ?</div><span class="q-level hard">🔴 Difficile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="psq10" value="a"> a) Le plafond suspendu ne nécessite pas de plaque</label></li>
          <li><label><input type="radio" name="psq10" value="b"> b) Le plafond autoportant repose sur les murs sans suspentes fixées à la dalle</label></li>
          <li><label><input type="radio" name="psq10" value="c"> c) Le plafond autoportant est uniquement pour l'extérieur</label></li>
          <li><label><input type="radio" name="psq10" value="d"> d> Il n'y a aucune différence</label></li>
        </ul>
        <div class="answer-feedback" id="psq10-feedback"></div>
      </div>
      <div class="quiz-footer">
        <button class="btn-submit" onclick="submitQuiz('plafondsuspendu', 10)">🎯 Calculer mon score !</button>
        <div class="score-display" id="score-plafondsuspendu"></div>
      </div>
    </div>
  </div>
</div><!-- END PLAFOND SUSPENDU -->

<!-- ONGLETS 9-14 CONDENSÉS MAIS COMPLETS -->
<!-- PLAFOND AUTOPORTANT -->
<div id="plafondautoportant" class="tab-content">
  <div class="sub-tabs">
    <button class="sub-tab-btn active" onclick="showSub('plafondautoportant', 'revision', this)">📖 Révision générale</button>
    <button class="sub-tab-btn" onclick="showSub('plafondautoportant', 'controle', this)">✅ Contrôle travaux</button>
    <button class="sub-tab-btn" onclick="showSub('plafondautoportant', 'lexique', this)">📝 Lexique</button>
    <button class="sub-tab-btn" onclick="showSub('plafondautoportant', 'securite', this)">⛑️ Mémo sécurité</button>
    <button class="sub-tab-btn" onclick="showSub('plafondautoportant', 'quiz', this)">🎯 Questionnaire d'acquis</button>
  </div>
  <div id="plafondautoportant-revision" class="sub-content active">
    <div class="section-card">
      <h2>🔲 Plafond Autoportant — Révision Générale</h2>
      <h3>🔹 Définition</h3>
      <p>Le plafond autoportant repose uniquement sur les murs périphériques de la pièce, sans suspentes fixées à la structure. L'ossature est portée par les murs via les rails de rive, sans liaison avec la dalle supérieure.</p>
      <h3>🔹 Avantages</h3>
      <div class="info-box green"><div class="icon">✅</div><div class="content"><p><strong>Isolation acoustique aux bruits aériens :</strong> En l'absence de liaison avec la dalle, les bruits d'impact du plancher supérieur ne se transmettent pas directement au plafond. Solution idéale pour les logements collectifs.</p></div></div>
      <h3>🔹 Principe de mise en œuvre</h3>
      <div class="controle-phase">
        <div class="check-item"><span class="check-icon">1️⃣</span> Tracer le niveau du plafond sur les 4 murs (niveau laser)</div>
        <div class="check-item"><span class="check-icon">2️⃣</span> Fixer les rails de rive sur les murs avec bande acoustique</div>
        <div class="check-item"><span class="check-icon">3️⃣</span> Poser les fourrures perpendiculairement aux joints des plaques</div>
        <div class="check-item"><span class="check-icon">4️⃣</span> Placer l'isolant entre les fourrures si nécessaire</div>
        <div class="check-item"><span class="check-icon">5️⃣</span> Visser les plaques BA13 ou BA15</div>
        <div class="check-item"><span class="check-icon">6️⃣</span> Réaliser les joints et finitions</div>
      </div>
      <h3>🔹 Limitations</h3>
      <table>
        <tr><th>Critère</th><th>Plafond suspendu</th><th>Plafond autoportant</th></tr>
        <tr><td>Appui</td><td>Dalle + murs</td><td>Murs uniquement</td></tr>
        <tr><td>Portée max</td><td>Grande portée possible</td><td>Limitée (max ~6m selon DTU)</td></tr>
        <tr><td>Bruit d'impact</td><td>Peut transmettre les impacts</td><td>Isole mieux des bruits d'impact</td></tr>
        <tr><td>Réseaux</td><td>Grande hauteur disponible</td><td>Hauteur limitée (fourrures seules)</td></tr>
      </table>
    </div>
  </div>
  <div id="plafondautoportant-controle" class="sub-content">
    <div class="section-card"><h2>✅ Contrôle — Plafond Autoportant</h2>
      <div class="controle-phase"><h3>🔵 AVANT</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Vérifier la portée (max ~6m) - au-delà prévoir renforts ou autre solution</div>
        <div class="check-item"><span class="check-icon">☑️</span> S'assurer que les murs peuvent reprendre la charge</div>
      </div>
      <div class="controle-phase"><h3>🟡 PENDANT</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Rails de rive à niveau (laser) et bien fixés</div>
        <div class="check-item"><span class="check-icon">☑️</span> Bande acoustique sous tous les rails</div>
        <div class="check-item"><span class="check-icon">☑️</span> Fourrures sans contact avec la dalle</div>
      </div>
      <div class="controle-phase"><h3>🟢 APRÈS</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Planéité ±3mm/2m</div>
        <div class="check-item"><span class="check-icon">☑️</span> Aucun contact entre ossature et dalle (risque de transmission acoustique)</div>
      </div>
    </div>
  </div>
  <div id="plafondautoportant-lexique" class="sub-content">
    <div class="section-card"><h2>📝 Lexique — Plafond Autoportant</h2>
      <div class="lexique-item"><strong>Autoportant</strong><p>Système dont la structure repose uniquement sur les murs périphériques, sans suspentes à la dalle.</p></div>
      <div class="lexique-item"><strong>Bruits d'impact</strong><p>Bruits transmis par la structure : pas, chutes d'objets. Le plafond autoportant limite leur transmission.</p></div>
      <div class="lexique-item"><strong>Portée</strong><p>Distance entre deux appuis. Pour un plafond autoportant, limitée à environ 6m selon le DTU 58.1.</p></div>
      <div class="lexique-item"><strong>DTU 58.1</strong><p>Document Technique Unifié régissant la mise en œuvre des plafonds en plaques de plâtre.</p></div>
    </div>
  </div>
  <div id="plafondautoportant-securite" class="sub-content">
    <div class="section-card"><h2>⛑️ Mémo Sécurité — Plafond Autoportant</h2>
      <div class="securite-grid">
        <div class="securite-card"><span class="icon">🏗️</span><h4>Travail en hauteur</h4><p>Plateau de travail ou échafaudage roulant. Jamais sur chaise ou tabouret.</p></div>
        <div class="securite-card"><span class="icon">😷</span><h4>Poussières</h4><p>Masque FFP2 découpe plaques et manipulation laine minérale.</p></div>
        <div class="securite-card"><span class="icon">🥽</span><h4>Yeux</h4><p>Lunettes pour les travaux en plafond (projections vers le bas).</p></div>
      </div>
    </div>
  </div>
  <div id="plafondautoportant-quiz" class="sub-content">
    <div class="section-card"><h2>🎯 Questionnaire d'Acquis — Plafond Autoportant</h2></div>
    <div class="quiz-container" id="quiz-plafondautoportant">
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">1</div><div class="q-text">Sur quoi repose un plafond autoportant ?</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="paq1" value="a"> a) Sur des suspentes fixées à la dalle</label></li>
          <li><label><input type="radio" name="paq1" value="b"> b) Uniquement sur les murs périphériques via les rails de rive</label></li>
          <li><label><input type="radio" name="paq1" value="c"> c) Sur des colonnes portantes</label></li>
          <li><label><input type="radio" name="paq1" value="d"> d) Sur le sol avec des supports réglables</label></li>
        </ul>
        <div class="answer-feedback" id="paq1-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">2</div><div class="q-text">Quel avantage principal a le plafond autoportant par rapport au plafond suspendu ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="paq2" value="a"> a) Il est moins cher</label></li>
          <li><label><input type="radio" name="paq2" value="b"> b) Il isole mieux des bruits d'impact provenant du plancher supérieur</label></li>
          <li><label><input type="radio" name="paq2" value="c"> c) Il s'installe plus rapidement</label></li>
          <li><label><input type="radio" name="paq2" value="d"> d) Il est plus facile à démonter</label></li>
        </ul>
        <div class="answer-feedback" id="paq2-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">3</div><div class="q-text">Vrai ou Faux : Un plafond autoportant peut avoir une portée illimitée.</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="paq3" value="a"> ✅ Vrai</label></li>
          <li><label><input type="radio" name="paq3" value="b"> ❌ Faux (portée limitée à environ 6m)</label></li>
        </ul>
        <div class="answer-feedback" id="paq3-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">4</div><div class="q-text">Pourquoi les fourrures d'un plafond autoportant ne doivent-elles PAS toucher la dalle ?</div><span class="q-level hard">🔴 Difficile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="paq4" value="a"> a) Pour éviter la corrosion des métaux</label></li>
          <li><label><input type="radio" name="paq4" value="b"> b"> Pour préserver le principe d'isolation acoustique (pas de pont phonique)</label></li>
          <li><label><input type="radio" name="paq4" value="c"> c) Pour faciliter le passage des câbles</label></li>
          <li><label><input type="radio" name="paq4" value="d"> d) C'est une règle esthétique</label></li>
        </ul>
        <div class="answer-feedback" id="paq4-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">5</div><div class="q-text">Mise en situation</div><span class="q-level hard">🔴 Difficile</span></div>
        <div class="scenario-box"><h4>🏗️ Scénario :</h4><p>Dans un immeuble collectif, les locataires du RDC entendent clairement les pas de leurs voisins du 1er. Quelle solution de plafond conseiller et pourquoi ?</p></div>
        <textarea class="open-answer" id="paq5-answer" placeholder="Écris ta réponse ici..."></textarea>
        <button class="btn-check" onclick="checkOpen('paq5')">Voir la correction 📋</button>
        <div class="answer-feedback" id="paq5-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">6</div><div class="q-text">Quel DTU régit la mise en œuvre des plafonds en plaques de plâtre ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="paq6" value="a"> a) DTU 25.41</label></li>
          <li><label><input type="radio" name="paq6" value="b"> b) DTU 58.1</label></li>
          <li><label><input type="radio" name="paq6" value="c"> c) DTU 45.2</label></li>
          <li><label><input type="radio" name="paq6" value="d"> d) DTU 13.3</label></li>
        </ul>
        <div class="answer-feedback" id="paq6-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">7</div><div class="q-text">Vrai ou Faux : La bande acoustique sous les rails est obligatoire pour un plafond autoportant.</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="paq7" value="a"> ✅ Vrai</label></li>
          <li><label><input type="radio" name="paq7" value="b"> ❌ Faux</label></li>
        </ul>
        <div class="answer-feedback" id="paq7-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">8</div><div class="q-text">Quelle est la tolérance de planéité d'un plafond autoportant en placo ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="paq8" value="a"> a) ±1mm sur 2m</label></li>
          <li><label><input type="radio" name="paq8" value="b"> b) ±3mm sur 2m</label></li>
          <li><label><input type="radio" name="paq8" value="c"> c) ±10mm sur 2m</label></li>
          <li><label><input type="radio" name="paq8" value="d"> d) ±5mm sur 1m</label></li>
        </ul>
        <div class="answer-feedback" id="paq8-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">9</div><div class="q-text">Dans quel type de logement le plafond autoportant est-il particulièrement adapté ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="paq9" value="a"> a) Maison individuelle de plain-pied</label></li>
          <li><label><input type="radio" name="paq9" value="b"> b) Immeuble collectif avec gêne sonore entre étages</label></li>
          <li><label><input type="radio" name="paq9" value="c"> c) Garage</label></li>
          <li><label><input type="radio" name="paq9" value="d"> d) Local commercial avec grande hauteur sous plafond</label></li>
        </ul>
        <div class="answer-feedback" id="paq9-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">10</div><div class="q-text">Quel outil est indispensable pour tracer le niveau du plafond autoportant sur les 4 murs ?</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="paq10" value="a"> a) Le mètre ruban</label></li>
          <li><label><input type="radio" name="paq10" value="b"> b) Le niveau laser</label></li>
          <li><label><input type="radio" name="paq10" value="c"> c) L'équerre de maçon</label></li>
          <li><label><input type="radio" name="paq10" value="d"> d) Le fil à plomb</label></li>
        </ul>
        <div class="answer-feedback" id="paq10-feedback"></div>
      </div>
      <div class="quiz-footer">
        <button class="btn-submit" onclick="submitQuiz('plafondautoportant', 10)">🎯 Calculer mon score !</button>
        <div class="score-display" id="score-plafondautoportant"></div>
      </div>
    </div>
  </div>
</div><!-- END PLAFOND AUTOPORTANT -->

<!-- PLAFOND MODULAIRE -->
<div id="plafondmodulaire" class="tab-content">
  <div class="sub-tabs">
    <button class="sub-tab-btn active" onclick="showSub('plafondmodulaire', 'revision', this)">📖 Révision générale</button>
    <button class="sub-tab-btn" onclick="showSub('plafondmodulaire', 'controle', this)">✅ Contrôle travaux</button>
    <button class="sub-tab-btn" onclick="showSub('plafondmodulaire', 'lexique', this)">📝 Lexique</button>
    <button class="sub-tab-btn" onclick="showSub('plafondmodulaire', 'securite', this)">⛑️ Mémo sécurité</button>
    <button class="sub-tab-btn" onclick="showSub('plafondmodulaire', 'quiz', this)">🎯 Questionnaire d'acquis</button>
  </div>
  <div id="plafondmodulaire-revision" class="sub-content active">
    <div class="section-card">
      <h2>◻️ Plafond Modulaire — Révision Générale</h2>
      <div class="img-grid">
        <div class="img-example"><img src="https://images.unsplash.com/photo-1497366811353-6870744d04b2?w=400&q=80" alt="Plafond modulaire bureau"><div class="caption">📸 Plafond modulaire en bureau</div></div>
      </div>
      <h3>🔹 Définition</h3>
      <p>Le plafond modulaire (ou plafond démontable) est constitué de dalles amovibles posées dans une ossature métallique apparente ou semi-encastrée. Très utilisé dans les bâtiments tertiaires, bureaux, commerces.</p>
      <h3>🔹 Types de dalles</h3>
      <table>
        <tr><th>Type de dalle</th><th>Matière</th><th>Performance</th></tr>
        <tr><td>Laine minérale</td><td>Fibres minérales</td><td>Acoustique, thermique</td></tr>
        <tr><td>Fibre de verre</td><td>Fibres de verre</td><td>Acoustique, légère</td></tr>
        <tr><td>Plâtre</td><td>Plâtre renforcé</td><td>Feu, acoustique</td></tr>
        <tr><td>Métal perforé</td><td>Aluminium ou acier</td><td>Lavable, esthétique</td></tr>
      </table>
      <h3>🔹 Formats courants</h3>
      <p>Formats standards : <strong>600×600 mm</strong>, 600×1200 mm, 300×1200 mm. L'ossature (T24) est dimensionnée selon le format des dalles.</p>
      <h3>🔹 Types d'ossature</h3>
      <table>
        <tr><th>Type</th><th>Description</th><th>Aspect</th></tr>
        <tr><td>Ossature apparente (T24)</td><td>T-bars visibles entre les dalles</td><td>Grille visible</td></tr>
        <tr><td>Semi-encastrée (T15)</td><td>T-bars partiellement visibles</td><td>Discret</td></tr>
        <tr><td>Encastrée (T0)</td><td>T-bars cachés dans les dalles</td><td>Plafond uni apparent</td></tr>
      </table>
      <h3>🔹 Avantages</h3>
      <div class="info-box green"><div class="icon">✅</div><div class="content"><p>Accès facile aux réseaux (câbles, VMC, sprinklers) en retirant les dalles. Remplacement de dalle individuelle possible. Rénovation rapide.</p></div></div>
    </div>
  </div>
  <div id="plafondmodulaire-controle" class="sub-content">
    <div class="section-card"><h2>✅ Contrôle — Plafond Modulaire</h2>
      <div class="controle-phase"><h3>🔵 AVANT</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Niveau du plafond défini et tracé (laser)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Grille de calepinage tracée (position des dalles par rapport aux murs)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Réseaux positionnés avant fermeture du plafond</div>
      </div>
      <div class="controle-phase"><h3>🟡 PENDANT</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Rails périphériques fixés à niveau</div>
        <div class="check-item"><span class="check-icon">☑️</span> T-bars suspendus à entraxe correct selon format de dalle</div>
        <div class="check-item"><span class="check-icon">☑️</span> Dalles de même lot (couleur, texture homogènes)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Coupes propres et dalles de bordure adaptées</div>
      </div>
      <div class="controle-phase"><h3>🟢 APRÈS</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Planéité du plafond (±3mm/2m)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Toutes les dalles bien posées, sans jours ni défauts</div>
        <div class="check-item"><span class="check-icon">☑️</span> Dalles de rives symétriques (calepinage centré)</div>
      </div>
    </div>
  </div>
  <div id="plafondmodulaire-lexique" class="sub-content">
    <div class="section-card"><h2>📝 Lexique — Plafond Modulaire</h2>
      <div class="lexique-item"><strong>Dalle amovible</strong><p>Élément de plafond posé dans l'ossature, non fixé, qu'on peut retirer facilement pour accéder aux réseaux.</p></div>
      <div class="lexique-item"><strong>T-bar (T24/T15)</strong><p>Profilé en T de l'ossature visible ou semi-encastrée. T24 = semelle de 24mm, T15 = semelle de 15mm.</p></div>
      <div class="lexique-item"><strong>Calepinage</strong><p>Plan de répartition des dalles sur le plafond. Permet de centrer la grille et d'optimiser les coupes en bordure.</p></div>
      <div class="lexique-item"><strong>Classe Absorption (αw)</strong><p>Mesure l'absorption acoustique d'une dalle. De A (meilleure) à E (moindre).</p></div>
      <div class="lexique-item"><strong>Sprinkler</strong><p>Tête de sprinkler (extincteur automatique à eau) intégrée dans le plafond. Doit être compatible avec les dalles.</p></div>
    </div>
  </div>
  <div id="plafondmodulaire-securite" class="sub-content">
    <div class="section-card"><h2>⛑️ Mémo Sécurité — Plafond Modulaire</h2>
      <div class="securite-grid">
        <div class="securite-card"><span class="icon">🏗️</span><h4>Travail en hauteur</h4><p>Nacelle ou échafaudage. Contrôler la stabilité du plateau.</p></div>
        <div class="securite-card"><span class="icon">😷</span><h4>Fibres minérales</h4><p>Masque FFP1 lors de la coupe et la manipulation des dalles laine minérale.</p></div>
        <div class="securite-card"><span class="icon">🔌</span><h4>Réseaux électriques</h4><p>Toujours vérifier qu'il n'y a pas de tension avant d'ouvrir le vide de plafond.</p></div>
        <div class="securite-card"><span class="icon">🥽</span><h4>Protection oculaire</h4><p>Lunettes lors de la découpe et lors des travaux en position plafond.</p></div>
      </div>
    </div>
  </div>
  <div id="plafondmodulaire-quiz" class="sub-content">
    <div class="section-card"><h2>🎯 Questionnaire d'Acquis — Plafond Modulaire</h2></div>
    <div class="quiz-container" id="quiz-plafondmodulaire">
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">1</div><div class="q-text">Quel est l'avantage principal du plafond modulaire par rapport au plafond placo ?</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="pmq1" value="a"> a) Il est moins cher</label></li>
          <li><label><input type="radio" name="pmq1" value="b"> b) L'accès aux réseaux est facile en retirant les dalles individuellement</label></li>
          <li><label><input type="radio" name="pmq1" value="c"> c) Il est plus résistant au feu</label></li>
          <li><label><input type="radio" name="pmq1" value="d"> d) Il est plus rapide à peindre</label></li>
        </ul>
        <div class="answer-feedback" id="pmq1-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">2</div><div class="q-text">Quel est le format standard le plus courant d'une dalle de plafond modulaire ?</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="pmq2" value="a"> a) 120×60 cm</label></li>
          <li><label><input type="radio" name="pmq2" value="b"> b) 60×60 cm</label></li>
          <li><label><input type="radio" name="pmq2" value="c"> c) 50×50 cm</label></li>
          <li><label><input type="radio" name="pmq2" value="d"> d) 100×100 cm</label></li>
        </ul>
        <div class="answer-feedback" id="pmq2-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">3</div><div class="q-text">Qu'est-ce que le calepinage ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="pmq3" value="a"> a) La fixation des dalles</label></li>
          <li><label><input type="radio" name="pmq3" value="b"> b) Le plan de répartition des dalles pour centrer la grille et optimiser les coupes</label></li>
          <li><label><input type="radio" name="pmq3" value="c"> c) Le nettoyage des dalles</label></li>
          <li><label><input type="radio" name="pmq3" value="d"> d> La découpe des T-bars</label></li>
        </ul>
        <div class="answer-feedback" id="pmq3-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">4</div><div class="q-text">Dans quel secteur utilise-t-on principalement les plafonds modulaires ?</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="pmq4" value="a"> a) Maisons individuelles</label></li>
          <li><label><input type="radio" name="pmq4" value="b"> b) Bâtiments tertiaires (bureaux, commerces, hôpitaux)</label></li>
          <li><label><input type="radio" name="pmq4" value="c"> c) Parkings</label></li>
          <li><label><input type="radio" name="pmq4" value="d"> d> Piscines</label></li>
        </ul>
        <div class="answer-feedback" id="pmq4-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">5</div><div class="q-text">Vrai ou Faux : Toutes les dalles d'un même chantier peuvent provenir de lots différents sans problème esthétique.</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="pmq5" value="a"> ✅ Vrai</label></li>
          <li><label><input type="radio" name="pmq5" value="b"> ❌ Faux (les lots différents peuvent avoir des teintes légèrement différentes)</label></li>
        </ul>
        <div class="answer-feedback" id="pmq5-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">6</div><div class="q-text">Mise en situation</div><span class="q-level hard">🔴 Difficile</span></div>
        <div class="scenario-box"><h4>🏗️ Scénario :</h4><p>Un client remarque que les dalles de bordure d'un plafond modulaire sont très petites (< 5 cm) d'un côté. Qu'aurais-tu dû faire pour éviter ce problème ? Explique la démarche correcte.</p></div>
        <textarea class="open-answer" id="pmq6-answer" placeholder="Écris ta réponse ici..."></textarea>
        <button class="btn-check" onclick="checkOpen('pmq6')">Voir la correction 📋</button>
        <div class="answer-feedback" id="pmq6-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">7</div><div class="q-text">Quel type de dalle est recommandé pour une salle de réunion avec beaucoup de bruit ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="pmq7" value="a"> a) Dalle métallique perforée (décorative)</label></li>
          <li><label><input type="radio" name="pmq7" value="b"> b) Dalle en laine minérale haute absorption acoustique</label></li>
          <li><label><input type="radio" name="pmq7" value="c"> c) Dalle en plâtre standard</label></li>
          <li><label><input type="radio" name="pmq7" value="d"> d) Dalle PVC lisse</label></li>
        </ul>
        <div class="answer-feedback" id="pmq7-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">8</div><div class="q-text">Vrai ou Faux : Les T-bars T24 (24mm de semelle) ont un aspect plus discret que les T0.</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="pmq8" value="a"> ✅ Vrai</label></li>
          <li><label><input type="radio" name="pmq8" value="b"> ❌ Faux (T0 sont encastrés = plus discrets)</label></li>
        </ul>
        <div class="answer-feedback" id="pmq8-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">9</div><div class="q-text">Qu'est-ce qu'un sprinkler et pourquoi est-il important dans un plafond modulaire ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="pmq9" value="a"> a) Un système d'éclairage LED</label></li>
          <li><label><input type="radio" name="pmq9" value="b"> b> Une tête d'extincteur automatique à eau intégrée dans le plafond (sécurité incendie)</label></li>
          <li><label><input type="radio" name="pmq9" value="c"> c) Un dispositif de ventilation</label></li>
          <li><label><input type="radio" name="pmq9" value="d"> d> Un capteur d'humidité</label></li>
        </ul>
        <div class="answer-feedback" id="pmq9-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">10</div><div class="q-text">Quelle est la tolérance de planéité d'un plafond modulaire ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="pmq10" value="a"> a) ±1mm/2m</label></li>
          <li><label><input type="radio" name="pmq10" value="b"> b) ±3mm/2m</label></li>
          <li><label><input type="radio" name="pmq10" value="c"> c) ±10mm/2m</label></li>
          <li><label><input type="radio" name="pmq10" value="d"> d> ±15mm/2m</label></li>
        </ul>
        <div class="answer-feedback" id="pmq10-feedback"></div>
      </div>
      <div class="quiz-footer">
        <button class="btn-submit" onclick="submitQuiz('plafondmodulaire', 10)">🎯 Calculer mon score !</button>
        <div class="score-display" id="score-plafondmodulaire"></div>
      </div>
    </div>
  </div>
</div><!-- END PLAFOND MODULAIRE -->

<!-- ITE -->
<div id="ite" class="tab-content">
  <div class="sub-tabs">
    <button class="sub-tab-btn active" onclick="showSub('ite', 'revision', this)">📖 Révision générale</button>
    <button class="sub-tab-btn" onclick="showSub('ite', 'controle', this)">✅ Contrôle travaux</button>
    <button class="sub-tab-btn" onclick="showSub('ite', 'lexique', this)">📝 Lexique</button>
    <button class="sub-tab-btn" onclick="showSub('ite', 'securite', this)">⛑️ Mémo sécurité</button>
    <button class="sub-tab-btn" onclick="showSub('ite', 'quiz', this)">🎯 Questionnaire d'acquis</button>
  </div>
  <div id="ite-revision" class="sub-content active">
    <div class="section-card">
      <h2>🏘️ ITE — Isolation Thermique par l'Extérieur</h2>
      <div class="img-grid">
        <div class="img-example"><img src="https://images.unsplash.com/photo-1580587771525-78b9dba3b914?w=400&q=80" alt="ITE facade"><div class="caption">📸 Isolation thermique par l'extérieur</div></div>
      </div>
      <h3>🔹 Principe de l'ITE</h3>
      <p>L'ITE consiste à envelopper le bâtiment d'une couche isolante fixée sur les façades extérieures, puis à la recouvrir d'une finition (enduit, bardage...). Elle supprime les ponts thermiques et conserve l'inertie thermique des murs.</p>
      <h3>🔹 Les 2 principaux systèmes ITE</h3>
      <table>
        <tr><th>Système</th><th>Description</th><th>Finition</th></tr>
        <tr><td>ETICS (Enduit sur Isolant)</td><td>Isolant collé/chevillé + enduit armé</td><td>Enduit minéral ou organique</td></tr>
        <tr><td>Bardage rapporté avec lame d'air</td><td>Isolant + ossature + bardage</td><td>Bois, composite, métal, HPL</td></tr>
      </table>
      <h3>🔹 Isolants utilisés en ITE</h3>
      <table>
        <tr><th>Isolant</th><th>λ</th><th>Avantages</th></tr>
        <tr><td>PSE (polystyrène expansé)</td><td>0,031-0,038</td><td>Léger, économique</td></tr>
        <tr><td>Laine de roche</td><td>0,034-0,040</td><td>Incombustible, acoustique</td></tr>
        <tr><td>Panneau polyuréthane</td><td>0,020-0,025</td><td>Haute performance, faible épaisseur</td></tr>
      </table>
      <h3>🔹 Mise en œuvre ETICS (système le plus courant)</h3>
      <div class="controle-phase">
        <div class="check-item"><span class="check-icon">1️⃣</span> Pose du profil de départ (larmier) en pied de façade</div>
        <div class="check-item"><span class="check-icon">2️⃣</span> Collage des panneaux isolants (colle + chevillage)</div>
        <div class="check-item"><span class="check-icon">3️⃣</span> Chevilles d'ancrage (≥ 6/m² selon vent)</div>
        <div class="check-item"><span class="check-icon">4️⃣</span> Application du sous-enduit armé + treillis de fibre de verre</div>
        <div class="check-item"><span class="check-icon">5️⃣</span> Application de la couche primaire</div>
        <div class="check-item"><span class="check-icon">6️⃣</span> Application de l'enduit de finition</div>
      </div>
      <h3>🔹 Avantages de l'ITE</h3>
      <ul class="styled">
        <li>Suppression des ponts thermiques (liaisons façade-plancher)</li>
        <li>Conservation de la surface habitable intérieure</li>
        <li>Rénovation de l'aspect extérieur en même temps</li>
        <li>Économies d'énergie importantes (jusqu'à 30%)</li>
        <li>Protection des murs contre les intempéries</li>
      </ul>
    </div>
  </div>
  <div id="ite-controle" class="sub-content">
    <div class="section-card"><h2>✅ Contrôle — ITE</h2>
      <div class="controle-phase"><h3>🔵 AVANT</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Diagnostic façade : fissures, humidité, ancienne peinture</div>
        <div class="check-item"><span class="check-icon">☑️</span> Validation du système (ETAG ou ATec)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Déclaration de travaux ou permis si nécessaire</div>
        <div class="check-item"><span class="check-icon">☑️</span> Protection des abords (toitures, baies, etc.)</div>
      </div>
      <div class="controle-phase"><h3>🟡 PENDANT</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Planéité du collage (règle de 2m)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Panneaux bien joints (pas de ponts thermiques entre panneaux)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Nombre et implantation des chevilles conformes</div>
        <div class="check-item"><span class="check-icon">☑️</span> Treillis de renfort aux angles et baies</div>
      </div>
      <div class="controle-phase"><h3>🟢 APRÈS</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Aspect homogène de l'enduit</div>
        <div class="check-item"><span class="check-icon">☑️</span> Joints de dilatation correctement exécutés</div>
        <div class="check-item"><span class="check-icon">☑️</span> Rejingots et larmiers en place</div>
      </div>
    </div>
  </div>
  <div id="ite-lexique" class="sub-content">
    <div class="section-card"><h2>📝 Lexique — ITE</h2>
      <div class="lexique-item"><strong>ATec / DTA</strong><p>Avis Technique / Document Technique d'Application : document officiel validant un procédé de construction non traditionnel.</p></div>
      <div class="lexique-item"><strong>Cheville de fixation</strong><p>Dispositif mécanique en plastique ou acier assurant l'ancrage de l'isolant dans le mur support.</p></div>
      <div class="lexique-item"><strong>ETICS</strong><p>External Thermal Insulation Composite System : système d'ITE avec enduit armé sur isolant. Le système le plus répandu.</p></div>
      <div class="lexique-item"><strong>Larmier</strong><p>Profilé de départ en aluminium ou PVC fixé en bas de façade pour soutenir les premiers panneaux.</p></div>
      <div class="lexique-item"><strong>Pont thermique</strong><p>Liaison entre un élément de structure (plancher, refend) et la façade créant une déperdition thermique.</p></div>
      <div class="lexique-item"><strong>Treillis de renfort</strong><p>Grille en fibre de verre noyée dans le sous-enduit pour renforcer la résistance aux chocs et à la fissuration.</p></div>
    </div>
  </div>
  <div id="ite-securite" class="sub-content">
    <div class="section-card"><h2>⛑️ Mémo Sécurité — ITE</h2>
      <div class="securite-grid">
        <div class="securite-card"><span class="icon">🏗️</span><h4>Travail en hauteur</h4><p>Échafaudage de façade conforme. Vérification quotidienne des amarrages.</p></div>
        <div class="securite-card"><span class="icon">😷</span><h4>Fibres / poussières</h4><p>Masque FFP2 pour la laine de roche. Masque vapeurs pour les enduits solvantés.</p></div>
        <div class="securite-card"><span class="icon">🥽</span><h4>Yeux</h4><p>Lunettes lors des opérations de chevillage et projection d'enduit.</p></div>
        <div class="securite-card"><span class="icon">🌬️</span><h4>Conditions météo</h4><p>Pas d'application d'enduit si T° < 5°C ou > 30°C, vent fort ou pluie.</p></div>
        <div class="securite-card"><span class="icon">🦺</span><h4>EPI complets</h4><p>Casque, harnais si nécessaire, chaussures de sécurité, gants sur l'échafaudage.</p></div>
      </div>
    </div>
  </div>
  <div id="ite-quiz" class="sub-content">
    <div class="section-card"><h2>🎯 Questionnaire d'Acquis — ITE</h2></div>
    <div class="quiz-container" id="quiz-ite">
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">1</div><div class="q-text">Que signifie ITE ?</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="iteq1" value="a"> a) Isolation Thermique Extérieure</label></li>
          <li><label><input type="radio" name="iteq1" value="b"> b) Isolation Thermique par l'Extérieur</label></li>
          <li><label><input type="radio" name="iteq1" value="c"> c) Isolation Totale et Économique</label></li>
          <li><label><input type="radio" name="iteq1" value="d"> d) Inspection Technique des Enduits</label></li>
        </ul>
        <div class="answer-feedback" id="iteq1-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">2</div><div class="q-text">Quel est l'avantage principal de l'ITE par rapport à l'isolation intérieure ?</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="iteq2" value="a"> a) Elle est moins chère</label></li>
          <li><label><input type="radio" name="iteq2" value="b"> b) Elle supprime les ponts thermiques et préserve la surface habitable</label></li>
          <li><label><input type="radio" name="iteq2" value="c"> c) Elle est plus rapide à poser</label></li>
          <li><label><input type="radio" name="iteq2" value="d"> d> Elle ne nécessite pas de permis</label></li>
        </ul>
        <div class="answer-feedback" id="iteq2-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">3</div><div class="q-text">Que signifie ETICS ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="iteq3" value="a"> a) Système ITE avec bardage bois</label></li>
          <li><label><input type="radio" name="iteq3" value="b"> b) Système ITE avec enduit armé sur isolant (External Thermal Insulation Composite System)</label></li>
          <li><label><input type="radio" name="iteq3" value="c"> c) Norme européenne des enduits</label></li>
          <li><label><input type="radio" name="iteq3" value="d"> d> Certification des entreprises ITE</label></li>
        </ul>
        <div class="answer-feedback" id="iteq3-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">4</div><div class="q-text">Vrai ou Faux : On peut appliquer un enduit d'ITE par temps de pluie ou forte chaleur (> 30°C).</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="iteq4" value="a"> ✅ Vrai</label></li>
          <li><label><input type="radio" name="iteq4" value="b"> ❌ Faux</label></li>
        </ul>
        <div class="answer-feedback" id="iteq4-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">5</div><div class="q-text">Quel isolant est incombustible et donc préférable pour les bâtiments à risque incendie ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="iteq5" value="a"> a) PSE (polystyrène expansé)</label></li>
          <li><label><input type="radio" name="iteq5" value="b"> b) Laine de roche</label></li>
          <li><label><input type="radio" name="iteq5" value="c"> c) Polyuréthane</label></li>
          <li><label><input type="radio" name="iteq5" value="d"> d> Liège</label></li>
        </ul>
        <div class="answer-feedback" id="iteq5-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">6</div><div class="q-text">Mise en situation</div><span class="q-level hard">🔴 Difficile</span></div>
        <div class="scenario-box"><h4>🏗️ Scénario :</h4><p>Sur un chantier ITE, tu remarques des fissures diagonales dans l'enduit au niveau des angles des baies (fenêtres) après 3 mois. Quelle est la cause probable et comment aurais-tu pu l'éviter ?</p></div>
        <textarea class="open-answer" id="iteq6-answer" placeholder="Écris ta réponse ici..."></textarea>
        <button class="btn-check" onclick="checkOpen('iteq6')">Voir la correction 📋</button>
        <div class="answer-feedback" id="iteq6-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">7</div><div class="q-text">Quel est le rôle du larmier de départ en ITE ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="iteq7" value="a"> a) Décorer le bas de façade</label></li>
          <li><label><input type="radio" name="iteq7" value="b"> b> Soutenir les premiers panneaux isolants et rejeter l'eau loin de la fondation</label></li>
          <li><label><input type="radio" name="iteq7" value="c"> c) Fixer le treillis de renfort</label></li>
          <li><label><input type="radio" name="iteq7" value="d"> d> Protéger l'enduit des rayons UV</label></li>
        </ul>
        <div class="answer-feedback" id="iteq7-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">8</div><div class="q-text">Pourquoi chevillage-t-on les panneaux isolants en plus du collage ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="iteq8" value="a"> a) Pour réduire les coûts</label></li>
          <li><label><input type="radio" name="iteq8" value="b"> b) Pour assurer la résistance aux efforts du vent (décollement possible)</label></li>
          <li><label><input type="radio" name="iteq8" value="c"> c> Pour améliorer l'aspect esthétique</label></li>
          <li><label><input type="radio" name="iteq8" value="d"> d) Pour accélérer le séchage</label></li>
        </ul>
        <div class="answer-feedback" id="iteq8-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">9</div><div class="q-text">Vrai ou Faux : Une ITE ne nécessite jamais de permis de construire.</div><span class="q-level hard">🔴 Difficile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="iteq9" value="a"> ✅ Vrai</label></li>
          <li><label><input type="radio" name="iteq9" value="b"> ❌ Faux (selon la commune et zone protégée, une autorisation peut être requise)</label></li>
        </ul>
        <div class="answer-feedback" id="iteq9-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">10</div><div class="q-text">Quel isolant a la meilleure performance thermique (λ le plus faible) pour une épaisseur minimale ?</div><span class="q-level hard">🔴 Difficile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="iteq10" value="a"> a) PSE (λ = 0,035)</label></li>
          <li><label><input type="radio" name="iteq10" value="b"> b) Laine de roche (λ = 0,038)</label></li>
          <li><label><input type="radio" name="iteq10" value="c"> c) Polyuréthane (λ = 0,022)</label></li>
          <li><label><input type="radio" name="iteq10" value="d"> d) Liège (λ = 0,040)</label></li>
        </ul>
        <div class="answer-feedback" id="iteq10-feedback"></div>
      </div>
      <div class="quiz-footer">
        <button class="btn-submit" onclick="submitQuiz('ite', 10)">🎯 Calculer mon score !</button>
        <div class="score-display" id="score-ite"></div>
      </div>
    </div>
  </div>
</div><!-- END ITE -->

<!-- ISOLATION PHONIQUE -->
<div id="phonique" class="tab-content">
  <div class="sub-tabs">
    <button class="sub-tab-btn active" onclick="showSub('phonique', 'revision', this)">📖 Révision générale</button>
    <button class="sub-tab-btn" onclick="showSub('phonique', 'controle', this)">✅ Contrôle travaux</button>
    <button class="sub-tab-btn" onclick="showSub('phonique', 'lexique', this)">📝 Lexique</button>
    <button class="sub-tab-btn" onclick="showSub('phonique', 'securite', this)">⛑️ Mémo sécurité</button>
    <button class="sub-tab-btn" onclick="showSub('phonique', 'quiz', this)">🎯 Questionnaire d'acquis</button>
  </div>
  <div id="phonique-revision" class="sub-content active">
    <div class="section-card">
      <h2>🔇 Isolation Phonique et Acoustique — Révision Générale</h2>
      <h3>🔹 Types de bruit</h3>
      <table>
        <tr><th>Type de bruit</th><th>Description</th><th>Source</th></tr>
        <tr><td>Bruits aériens</td><td>Se propagent dans l'air (voix, musique, TV)</td><td>Voisins, rue</td></tr>
        <tr><td>Bruits d'impact</td><td>Transmis par la structure (chocs)</td><td>Pas, chutes, travaux</td></tr>
        <tr><td>Bruits d'équipements</td><td>Vibrations d'installations</td><td>VMC, ascenseur, tuyaux</td></tr>
      </table>
      <h3>🔹 Grandeurs acoustiques</h3>
      <table>
        <tr><th>Symbole</th><th>Nom</th><th>Description</th></tr>
        <tr><td><strong>Rw</strong></td><td>Indice d'affaiblissement pondéré</td><td>Isolation aux bruits aériens (en dB)</td></tr>
        <tr><td><strong>Lw</strong></td><td>Niveau de pression</td><td>Intensité d'un bruit en dB</td></tr>
        <tr><td><strong>Ln,w</strong></td><td>Niveau de bruit d'impact</td><td>Transmission des bruits d'impact</td></tr>
        <tr><td><strong>αw</strong></td><td>Coefficient d'absorption</td><td>Absorption du son dans un local</td></tr>
      </table>
      <h3>🔹 Solutions d'isolation phonique</h3>
      <table>
        <tr><th>Solution</th><th>Efficacité</th><th>Usage</th></tr>
        <tr><td>Cloison double plaque</td><td>Bonne aux bruits aériens</td><td>Entre pièces</td></tr>
        <tr><td>Désolidarisation ossature</td><td>Bruits d'impact et aériens</td><td>Cloisons, plafonds</td></tr>
        <tr><td>Laine de roche entre plaques</td><td>Amélioration acoustique</td><td>Cloisons et plafonds</td></tr>
        <tr><td>Sol flottant</td><td>Bruits d'impact</td><td>Planchers</td></tr>
        <tr><td>Sous-couche acoustique</td><td>Bruits d'impact</td><td>Sous parquet/carrelage</td></tr>
      </table>
      <h3>🔹 Réglementation NRA (Nouvelle Réglementation Acoustique)</h3>
      <div class="info-box blue"><div class="icon">📋</div><div class="content"><p>La NRA fixe les exigences acoustiques des bâtiments d'habitation neufs. Exemple : isolement entre logements ≥ <strong>53 dB</strong> DnT,A pour les bruits aériens.</p></div></div>
      <h3>🔹 Ponts phoniques</h3>
      <p>Comme les ponts thermiques, les ponts phoniques sont des continuités structurelles qui transmettent les vibrations sonores d'une pièce à l'autre. Les éviter en <strong>désolidarisant systématiquement</strong> les ossatures des structures.</p>
    </div>
  </div>
  <div id="phonique-controle" class="sub-content">
    <div class="section-card"><h2>✅ Contrôle — Isolation Phonique</h2>
      <div class="controle-phase"><h3>🔵 AVANT</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Identifier les sources de bruit (voisins, rue, équipements)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Choisir la solution adaptée au type de bruit</div>
        <div class="check-item"><span class="check-icon">☑️</span> Planifier la désolidarisation des ossatures</div>
      </div>
      <div class="controle-phase"><h3>🟡 PENDANT</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Bandes acoustiques sous tous les rails et supports</div>
        <div class="check-item"><span class="check-icon">☑️</span> Laine minérale bien mise en place sans interstices</div>
        <div class="check-item"><span class="check-icon">☑️</span> Calfeutrement des traversées (câbles, tuyaux) avec mastics acoustiques</div>
      </div>
      <div class="controle-phase"><h3>🟢 APRÈS</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Mesures acoustiques in situ si exigences réglementaires</div>
        <div class="check-item"><span class="check-icon">☑️</span> Aucun pont phonique (tuyaux, câbles, fixations directes)</div>
      </div>
    </div>
  </div>
  <div id="phonique-lexique" class="sub-content">
    <div class="section-card"><h2>📝 Lexique — Isolation Phonique</h2>
      <div class="lexique-item"><strong>Décibel (dB)</strong><p>Unité de mesure de l'intensité sonore. +10dB = son perçu deux fois plus fort.</p></div>
      <div class="lexique-item"><strong>Désolidarisation</strong><p>Séparation mécanique d'un élément de la structure par bande résiliente pour éviter la transmission des vibrations.</p></div>
      <div class="lexique-item"><strong>DnT,A</strong><p>Isolement acoustique normalisé aux bruits aériens entre pièces, mesuré in situ en dB.</p></div>
      <div class="lexique-item"><strong>Ln,w</strong><p>Niveau de bruit d'impact pondéré. Plus il est faible, meilleure est l'isolation aux impacts.</p></div>
      <div class="lexique-item"><strong>NRA</strong><p>Nouvelle Réglementation Acoustique (arrêté du 30/06/1999). Fixe les exigences pour les bâtiments d'habitation neufs.</p></div>
      <div class="lexique-item"><strong>Sol flottant</strong><p>Sol posé sur une sous-couche résiliente sans contact rigide avec les murs. Réduit les bruits d'impact.</p></div>
    </div>
  </div>
  <div id="phonique-securite" class="sub-content">
    <div class="section-card"><h2>⛑️ Mémo Sécurité — Isolation Phonique</h2>
      <div class="securite-grid">
        <div class="securite-card"><span class="icon">😷</span><h4>Laine minérale</h4><p>Masque FFP1 + vêtements couvrants pour manipulation de la laine de roche ou verre.</p></div>
        <div class="securite-card"><span class="icon">👂</span><h4>Bruits de chantier</h4><p>Protections auditives si utilisation d'outils bruyants (perceuse, scie).</p></div>
        <div class="securite-card"><span class="icon">🔌</span><h4>Électricité</h4><p>Couper les circuits avant d'intervenir dans cloisons ou plafonds.</p></div>
      </div>
    </div>
  </div>
  <div id="phonique-quiz" class="sub-content">
    <div class="section-card"><h2>🎯 Questionnaire d'Acquis — Isolation Phonique</h2></div>
    <div class="quiz-container" id="quiz-phonique">
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">1</div><div class="q-text">Quels sont les bruits d'impact ?</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="phq1" value="a"> a) La voix d'un voisin</label></li>
          <li><label><input type="radio" name="phq1" value="b"> b) Les pas, les chutes d'objets transmis par la structure</label></li>
          <li><label><input type="radio" name="phq1" value="c"> c) Le bruit de la rue</label></li>
          <li><label><input type="radio" name="phq1" value="d"> d> La musique de voisins</label></li>
        </ul>
        <div class="answer-feedback" id="phq1-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">2</div><div class="q-text">Un Rw élevé signifie que la paroi :</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="phq2" value="a"> a) Est mauvaise isolante phoniquement</label></li>
          <li><label><input type="radio" name="phq2" value="b"> b) Isole bien les bruits aériens (forte résistance)</label></li>
          <li><label><input type="radio" name="phq2" value="c"> c) Absorbe bien le son</label></li>
          <li><label><input type="radio" name="phq2" value="d"> d> Est fine</label></li>
        </ul>
        <div class="answer-feedback" id="phq2-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">3</div><div class="q-text">Vrai ou Faux : Un sol flottant améliore principalement l'isolation aux bruits aériens.</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="phq3" value="a"> ✅ Vrai</label></li>
          <li><label><input type="radio" name="phq3" value="b"> ❌ Faux (il améliore principalement les bruits d'impact)</label></li>
        </ul>
        <div class="answer-feedback" id="phq3-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">4</div><div class="q-text">Pourquoi calfeutre-t-on les traversées de câbles et tuyaux dans une cloison phonique ?</div><span class="q-level hard">🔴 Difficile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="phq4" value="a"> a) Pour éviter les infiltrations d'eau</label></li>
          <li><label><input type="radio" name="phq4" value="b"> b) Pour éviter les ponts phoniques et la transmission du son par les trous</label></li>
          <li><label><input type="radio" name="phq4" value="c"> c) Pour des raisons esthétiques</label></li>
          <li><label><input type="radio" name="phq4" value="d"> d> Pour respecter la norme incendie</label></li>
        </ul>
        <div class="answer-feedback" id="phq4-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">5</div><div class="q-text">Quel isolant est le plus efficace en acoustique entre laine de roche et PSE ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="phq5" value="a"> a) PSE (polystyrène expansé)</label></li>
          <li><label><input type="radio" name="phq5" value="b"> b) Laine de roche</label></li>
          <li><label><input type="radio" name="phq5" value="c"> c) Ils sont équivalents</label></li>
          <li><label><input type="radio" name="phq5" value="d"> d) Cela dépend de la couleur</label></li>
        </ul>
        <div class="answer-feedback" id="phq5-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">6</div><div class="q-text">Mise en situation</div><span class="q-level hard">🔴 Difficile</span></div>
        <div class="scenario-box"><h4>🏗️ Scénario :</h4><p>Dans un immeuble, un locataire se plaint d'entendre les conversations de ses voisins à travers la cloison. Quelle solution de rénovation phonique propose-t-on et quels sont les points critiques à respecter ?</p></div>
        <textarea class="open-answer" id="phq6-answer" placeholder="Écris ta réponse ici..."></textarea>
        <button class="btn-check" onclick="checkOpen('phq6')">Voir la correction 📋</button>
        <div class="answer-feedback" id="phq6-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">7</div><div class="q-text">Que mesure l'indice Ln,w ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="phq7" value="a"> a) L'absorption sonore d'un plafond</label></li>
          <li><label><input type="radio" name="phq7" value="b"> b) Le niveau de bruit d'impact pondéré</label></li>
          <li><label><input type="radio" name="phq7" value="c"> c) L'isolement aux bruits aériens entre pièces</label></li>
          <li><label><input type="radio" name="phq7" value="d"> d) Le bruit généré par les équipements</label></li>
        </ul>
        <div class="answer-feedback" id="phq7-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">8</div><div class="q-text">Vrai ou Faux : Plus le Ln,w est élevé, meilleure est l'isolation aux bruits d'impact.</div><span class="q-level hard">🔴 Difficile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="phq8" value="a"> ✅ Vrai</label></li>
          <li><label><input type="radio" name="phq8" value="b"> ❌ Faux (plus Ln,w est faible, meilleure est l'isolation)</label></li>
        </ul>
        <div class="answer-feedback" id="phq8-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">9</div><div class="q-text">Quel est l'isolement acoustique minimum entre logements selon la NRA ?</div><span class="q-level hard">🔴 Difficile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="phq9" value="a"> a) 40 dB</label></li>
          <li><label><input type="radio" name="phq9" value="b"> b) 53 dB</label></li>
          <li><label><input type="radio" name="phq9" value="c"> c) 30 dB</label></li>
          <li><label><input type="radio" name="phq9" value="d"> d> 70 dB</label></li>
        </ul>
        <div class="answer-feedback" id="phq9-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">10</div><div class="q-text">Quelle est l'unité de mesure du son ?</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="phq10" value="a"> a) Watt (W)</label></li>
          <li><label><input type="radio" name="phq10" value="b"> b) Décibel (dB)</label></li>
          <li><label><input type="radio" name="phq10" value="c"> c) Hertz (Hz)</label></li>
          <li><label><input type="radio" name="phq10" value="d"> d> Newton (N)</label></li>
        </ul>
        <div class="answer-feedback" id="phq10-feedback"></div>
      </div>
      <div class="quiz-footer">
        <button class="btn-submit" onclick="submitQuiz('phonique', 10)">🎯 Calculer mon score !</button>
        <div class="score-display" id="score-phonique"></div>
      </div>
    </div>
  </div>
</div><!-- END PHONIQUE -->

<!-- ISOLATION THERMIQUE -->
<div id="thermique" class="tab-content">
  <div class="sub-tabs">
    <button class="sub-tab-btn active" onclick="showSub('thermique', 'revision', this)">📖 Révision générale</button>
    <button class="sub-tab-btn" onclick="showSub('thermique', 'controle', this)">✅ Contrôle travaux</button>
    <button class="sub-tab-btn" onclick="showSub('thermique', 'lexique', this)">📝 Lexique</button>
    <button class="sub-tab-btn" onclick="showSub('thermique', 'securite', this)">⛑️ Mémo sécurité</button>
    <button class="sub-tab-btn" onclick="showSub('thermique', 'quiz', this)">🎯 Questionnaire d'acquis</button>
  </div>
  <div id="thermique-revision" class="sub-content active">
    <div class="section-card">
      <h2>🌡️ Isolation Thermique — Révision Générale</h2>
      <h3>🔹 Mécanismes de transfert de chaleur</h3>
      <table>
        <tr><th>Mécanisme</th><th>Description</th><th>Solution</th></tr>
        <tr><td>Conduction</td><td>Chaleur traversant un matériau solide</td><td>Isolant (λ faible)</td></tr>
        <tr><td>Convection</td><td>Déplacement de l'air chaud</td><td>Calfeutrement des défauts</td></tr>
        <tr><td>Rayonnement</td><td>Rayonnement infrarouge</td><td>Films réfléchissants</td></tr>
      </table>
      <h3>🔹 Principales grandeurs thermiques</h3>
      <table>
        <tr><th>Grandeur</th><th>Symbole</th><th>Unité</th><th>Description</th></tr>
        <tr><td>Conductivité thermique</td><td>λ</td><td>W/m.K</td><td>Facilité à conduire la chaleur (bas = bon isolant)</td></tr>
        <tr><td>Résistance thermique</td><td>R</td><td>m².K/W</td><td>R = e/λ (épais + λ faible = meilleure R)</td></tr>
        <tr><td>Coefficient U</td><td>U</td><td>W/m².K</td><td>Déperdition totale d'une paroi (bas = bien isolé)</td></tr>
      </table>
      <h3>🔹 Comparatif des isolants courants</h3>
      <table>
        <tr><th>Isolant</th><th>λ (W/m.K)</th><th>Type</th><th>Usage courant</th></tr>
        <tr><td>Laine de verre</td><td>0,032-0,040</td><td>Minéral</td><td>Combles, murs, plafonds</td></tr>
        <tr><td>Laine de roche</td><td>0,034-0,040</td><td>Minéral</td><td>Acoustique + thermique</td></tr>
        <tr><td>PSE</td><td>0,030-0,038</td><td>Synthétique</td><td>ITE, sol, murs</td></tr>
        <tr><td>Polyuréthane</td><td>0,020-0,025</td><td>Synthétique</td><td>Haute perf. faible épaisseur</td></tr>
        <tr><td>Ouate de cellulose</td><td>0,035-0,040</td><td>Naturel</td><td>Combles insufflés</td></tr>
        <tr><td>Liège</td><td>0,038-0,045</td><td>Naturel</td><td>Acoustique, écologique</td></tr>
      </table>
      <h3>🔹 RE2020</h3>
      <div class="info-box blue"><div class="icon">🏠</div><div class="content"><p>La RE2020 (Réglementation Environnementale 2020) remplace la RT2012. Elle fixe des seuils de <strong>consommation d'énergie primaire</strong>, d'émissions de CO₂ et de confort d'été (IC). Elle favorise les matériaux biosourcés.</p></div></div>
    </div>
  </div>
  <div id="thermique-controle" class="sub-content">
    <div class="section-card"><h2>✅ Contrôle — Isolation Thermique</h2>
      <div class="controle-phase"><h3>🔵 AVANT</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Calcul de la valeur R requise selon RT/RE et usage</div>
        <div class="check-item"><span class="check-icon">☑️</span> Vérification de la compatibilité isolant/support</div>
        <div class="check-item"><span class="check-icon">☑️</span> Identification et traitement des ponts thermiques</div>
      </div>
      <div class="controle-phase"><h3>🟡 PENDANT</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Isolation sans interstices ni ponts thermiques</div>
        <div class="check-item"><span class="check-icon">☑️</span> Pare-vapeur bien positionné côté chaud</div>
        <div class="check-item"><span class="check-icon">☑️</span> Épaisseur conforme aux plans</div>
      </div>
      <div class="controle-phase"><h3>🟢 APRÈS</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Test thermographique si possible (caméra infrarouge)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Test d'infiltrométrie (Blower Door) si exigé</div>
      </div>
    </div>
  </div>
  <div id="thermique-lexique" class="sub-content">
    <div class="section-card"><h2>📝 Lexique — Isolation Thermique</h2>
      <div class="lexique-item"><strong>Biosourcé</strong><p>Matériau fabriqué à partir de matières premières renouvelables biologiques (bois, chanvre, paille, ouate de cellulose).</p></div>
      <div class="lexique-item"><strong>Blower Door</strong><p>Test d'étanchéité à l'air d'un bâtiment. Mesure les infiltrations d'air parasites.</p></div>
      <div class="lexique-item"><strong>Coefficient U</strong><p>Coefficient de transmission thermique d'une paroi (W/m².K). Plus U est faible, moins il y a de déperditions.</p></div>
      <div class="lexique-item"><strong>Conduction thermique</strong><p>Transfert de chaleur d'une molécule à l'autre dans un matériau solide.</p></div>
      <div class="lexique-item"><strong>RE2020</strong><p>Réglementation Environnementale 2020. Encadre la performance thermique et carbone des bâtiments neufs depuis janvier 2022.</p></div>
      <div class="lexique-item"><strong>Résistance thermique R</strong><p>Capacité d'un matériau à s'opposer aux transferts de chaleur. R = épaisseur (m) / λ. Exprimée en m².K/W.</p></div>
      <div class="lexique-item"><strong>Thermographie infrarouge</strong><p>Technique de diagnostic qui visualise les déperditions thermiques d'un bâtiment par caméra infrarouge.</p></div>
    </div>
  </div>
  <div id="thermique-securite" class="sub-content">
    <div class="section-card"><h2>⛑️ Mémo Sécurité — Isolation Thermique</h2>
      <div class="securite-grid">
        <div class="securite-card"><span class="icon">😷</span><h4>Fibres</h4><p>Masque FFP1 à FFP2 selon les matériaux. Obligatoire pour laines minérales.</p></div>
        <div class="securite-card"><span class="icon">🧤</span><h4>Peau</h4><p>Manches longues et gants : les fibres sont irritantes pour la peau et les yeux.</p></div>
        <div class="securite-card"><span class="icon">🌬️</span><h4>COV</h4><p>Isolants synthétiques (polyuréthane en mousse) : ventiler lors de l'application en mousse.</p></div>
        <div class="securite-card"><span class="icon">🔥</span><h4>Incendie</h4><p>PSE et PU sont combustibles. Stocker à l'écart des sources de chaleur et de flammes.</p></div>
      </div>
    </div>
  </div>
  <div id="thermique-quiz" class="sub-content">
    <div class="section-card"><h2>🎯 Questionnaire d'Acquis — Isolation Thermique</h2></div>
    <div class="quiz-container" id="quiz-thermique">
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">1</div><div class="q-text">La résistance thermique R se calcule avec la formule :</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="thq1" value="a"> a) R = λ × e</label></li>
          <li><label><input type="radio" name="thq1" value="b"> b) R = e / λ</label></li>
          <li><label><input type="radio" name="thq1" value="c"> c) R = λ / e</label></li>
          <li><label><input type="radio" name="thq1" value="d"> d> R = e + λ</label></li>
        </ul>
        <div class="answer-feedback" id="thq1-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">2</div><div class="q-text">Quel isolant naturel est utilisé en insufflation dans les combles perdus ?</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="thq2" value="a"> a) Laine de verre</label></li>
          <li><label><input type="radio" name="thq2" value="b"> b) Ouate de cellulose</label></li>
          <li><label><input type="radio" name="thq2" value="c"> c) Polyuréthane</label></li>
          <li><label><input type="radio" name="thq2" value="d"> d> PSE</label></li>
        </ul>
        <div class="answer-feedback" id="thq2-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">3</div><div class="q-text">Un coefficient U élevé signifie que la paroi :</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="thq3" value="a"> a) Isole bien (faibles déperditions)</label></li>
          <li><label><input type="radio" name="thq3" value="b"> b) Laisse passer beaucoup de chaleur (mauvaise isolation)</label></li>
          <li><label><input type="radio" name="thq3" value="c"> c) Est très résistante mécaniquement</label></li>
          <li><label><input type="radio" name="thq3" value="d"> d> Est épaisse</label></li>
        </ul>
        <div class="answer-feedback" id="thq3-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">4</div><div class="q-text">Vrai ou Faux : La RE2020 a remplacé la RT2012 pour les bâtiments neufs.</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="thq4" value="a"> ✅ Vrai</label></li>
          <li><label><input type="radio" name="thq4" value="b"> ❌ Faux</label></li>
        </ul>
        <div class="answer-feedback" id="thq4-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">5</div><div class="q-text">Mise en situation</div><span class="q-level hard">🔴 Difficile</span></div>
        <div class="scenario-box"><h4>🏗️ Scénario :</h4><p>Un client veut isoler ses murs intérieurs (ITI). Pour 10 cm d'isolant avec λ = 0,04 W/m.K, quelle est la résistance thermique R obtenue ? Est-ce suffisant pour la RE2020 (exigence mur : R ≥ 3,7 m².K/W) ? Que conseilles-tu ?</p></div>
        <textarea class="open-answer" id="thq5-answer" placeholder="Calcule R et donne ton conseil..."></textarea>
        <button class="btn-check" onclick="checkOpen('thq5')">Voir la correction 📋</button>
        <div class="answer-feedback" id="thq5-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">6</div><div class="q-text">Du côté de quel côté doit-on impérativement placer le pare-vapeur ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="thq6" value="a"> a) Côté froid (extérieur)</label></li>
          <li><label><input type="radio" name="thq6" value="b"> b) Côté chaud (intérieur)</label></li>
          <li><label><input type="radio" name="thq6" value="c"> c) Au milieu de l'isolant</label></li>
          <li><label><input type="radio" name="thq6" value="d"> d> Cela n'a pas d'importance</label></li>
        </ul>
        <div class="answer-feedback" id="thq6-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">7</div><div class="q-text">Quel outil permet de visualiser les déperditions thermiques d'un bâtiment ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="thq7" value="a"> a) L'humidimètre</label></li>
          <li><label><input type="radio" name="thq7" value="b"> b) La caméra thermique infrarouge</label></li>
          <li><label><input type="radio" name="thq7" value="c"> c) Le niveau laser</label></li>
          <li><label><input type="radio" name="thq7" value="d"> d> Le débitmètre</label></li>
        </ul>
        <div class="answer-feedback" id="thq7-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">8</div><div class="q-text">Vrai ou Faux : Le polystyrène expansé (PSE) est incombustible.</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="thq8" value="a"> ✅ Vrai</label></li>
          <li><label><input type="radio" name="thq8" value="b"> ❌ Faux (le PSE est combustible, contrairement à la laine de roche)</label></li>
        </ul>
        <div class="answer-feedback" id="thq8-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">9</div><div class="q-text">Quel est le λ du polyuréthane (approximatif) ?</div><span class="q-level hard">🔴 Difficile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="thq9" value="a"> a) 0,040 W/m.K</label></li>
          <li><label><input type="radio" name="thq9" value="b"> b) 0,022 W/m.K</label></li>
          <li><label><input type="radio" name="thq9" value="c"> c) 0,055 W/m.K</label></li>
          <li><label><input type="radio" name="thq9" value="d"> d> 0,010 W/m.K</label></li>
        </ul>
        <div class="answer-feedback" id="thq9-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">10</div><div class="q-text">Quel phénomène de transfert de chaleur est combattu par le calfeutrement des défauts d'étanchéité ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="thq10" value="a"> a) La conduction</label></li>
          <li><label><input type="radio" name="thq10" value="b"> b) La convection (déplacement d'air)</label></li>
          <li><label><input type="radio" name="thq10" value="c"> c) Le rayonnement</label></li>
          <li><label><input type="radio" name="thq10" value="d"> d> L'osmose</label></li>
        </ul>
        <div class="answer-feedback" id="thq10-feedback"></div>
      </div>
      <div class="quiz-footer">
        <button class="btn-submit" onclick="submitQuiz('thermique', 10)">🎯 Calculer mon score !</button>
        <div class="score-display" id="score-thermique"></div>
      </div>
    </div>
  </div>
</div><!-- END THERMIQUE -->

<!-- PROTECTION INCENDIE -->
<div id="incendie" class="tab-content">
  <div class="sub-tabs">
    <button class="sub-tab-btn active" onclick="showSub('incendie', 'revision', this)">📖 Révision générale</button>
    <button class="sub-tab-btn" onclick="showSub('incendie', 'controle', this)">✅ Contrôle travaux</button>
    <button class="sub-tab-btn" onclick="showSub('incendie', 'lexique', this)">📝 Lexique</button>
    <button class="sub-tab-btn" onclick="showSub('incendie', 'securite', this)">⛑️ Mémo sécurité</button>
    <button class="sub-tab-btn" onclick="showSub('incendie', 'quiz', this)">🎯 Questionnaire d'acquis</button>
  </div>
  <div id="incendie-revision" class="sub-content active">
    <div class="section-card">
      <h2>🔥 Protection Incendie — Révision Générale</h2>
      <h3>🔹 Le triangle du feu</h3>
      <div class="info-box red"><div class="icon">🔥</div><div class="content"><p>Un feu nécessite <strong>3 éléments</strong> : un combustible (ce qui brûle), un comburant (oxygène), et une énergie d'activation (chaleur). Supprimer l'un des trois éteint le feu.</p></div></div>
      <h3>🔹 Classement au feu des matériaux (Euroclasses)</h3>
      <table>
        <tr><th>Euroclass</th><th>Comportement au feu</th></tr>
        <tr><td><span class="badge green">A1</span></td><td>Ininflammable (béton, acier, verre)</td></tr>
        <tr><td><span class="badge green">A2</span></td><td>Non combustible avec contribution au feu négligeable</td></tr>
        <tr><td><span class="badge blue">B</span></td><td>Combustible très difficilement inflammable</td></tr>
        <tr><td><span class="badge blue">C</span></td><td>Combustible difficilement inflammable</td></tr>
        <tr><td><span class="badge orange">D</span></td><td>Combustible moyennement inflammable</td></tr>
        <tr><td><span class="badge orange">E</span></td><td>Combustible facilement inflammable</td></tr>
        <tr><td><span class="badge red">F</span></td><td>Non classé (le plus dangereux)</td></tr>
      </table>
      <p>Lettres complémentaires : <strong>s1, s2, s3</strong> (fumée) et <strong>d0, d1, d2</strong> (gouttelettes enflammées)</p>
      <h3>🔹 Classement des ERP (Établissements Recevant du Public)</h3>
      <table>
        <tr><th>Type</th><th>Nature</th><th>Exemples</th></tr>
        <tr><td>Type J</td><td>Structures d'accueil handicapés</td><td>EHPAD, IME</td></tr>
        <tr><td>Type L</td><td>Spectacles, conférences</td><td>Cinéma, théâtre</td></tr>
        <tr><td>Type M</td><td>Magasins</td><td>Supermarchés</td></tr>
        <tr><td>Type N</td><td>Restaurants</td><td>Cafés, bars</td></tr>
        <tr><td>Type O</td><td>Hôtels</td><td>Résidences</td></tr>
        <tr><td>Type W</td><td>Bureaux</td><td>Open-space</td></tr>
      </table>
      <h3>🔹 Résistance au feu des éléments de construction</h3>
      <table>
        <tr><th>Symbole</th><th>Signification</th><th>Durée</th></tr>
        <tr><td><strong>REI 30</strong></td><td>Résistance + Étanchéité + Isolation 30 min</td><td>30 minutes</td></tr>
        <tr><td><strong>REI 60</strong></td><td>Résistance + Étanchéité + Isolation 60 min</td><td>60 minutes</td></tr>
        <tr><td><strong>EI 30/60/90/120</strong></td><td>Étanchéité + Isolation (cloison)</td><td>30/60/90/120 min</td></tr>
        <tr><td><strong>R 60</strong></td><td>Résistance structurelle seule</td><td>60 minutes</td></tr>
      </table>
      <h3>🔹 Solutions de protection passive incendie</h3>
      <table>
        <tr><th>Solution</th><th>Rôle</th></tr>
        <tr><td>Plaques BA13 feu (roses)</td><td>Résistance au feu des cloisons et plafonds</td></tr>
        <tr><td>Laine de roche</td><td>Incombustible, renforce REI</td></tr>
        <tr><td>Enduit intumescent</td><td>Gonfle au contact du feu, protège la structure</td></tr>
        <tr><td>Coupe-feu (joint/mastic)</td><td>Colmate les traversées de câbles et tuyaux</td></tr>
        <tr><td>Porte coupe-feu (EI 30/60)</td><td>Compartimentage</td></tr>
      </table>
      <h3>🔹 Compartimentage</h3>
      <div class="info-box orange"><div class="icon">🧱</div><div class="content"><p>Le <strong>compartimentage</strong> divise un bâtiment en zones étanches au feu pour limiter la propagation des flammes et des fumées. Les cloisons, plafonds et portes doivent avoir la résistance au feu requise (EI ou REI selon la réglementation).</p></div></div>
    </div>
  </div>
  <div id="incendie-controle" class="sub-content">
    <div class="section-card"><h2>✅ Contrôle — Protection Incendie</h2>
      <div class="controle-phase"><h3>🔵 AVANT</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Identifier le type ERP ou IGH (immeuble de grande hauteur)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Vérifier les exigences REI des parois selon le règlement</div>
        <div class="check-item"><span class="check-icon">☑️</span> Sélectionner les matériaux avec les bonnes Euroclasses</div>
        <div class="check-item"><span class="check-icon">☑️</span> Prévoir les trappes de désenfumage</div>
      </div>
      <div class="controle-phase"><h3>🟡 PENDANT</h3>
        <div class="check-item"><span class="check-icon">☑️</span> Traitement de toutes les traversées de parois coupe-feu</div>
        <div class="check-item"><span class="check-icon">☑️</span> Plaques feu correctement vissées (pas de manque)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Jonctions et raccords en pied de cloison traités</div>
      </div>
      <div class="controle-phase"><h3>🟢 APRÈS</h3>
        <div class="check-item"><span class="check-icon">☑️</span> PV d'essai au feu si exigé</div>
        <div class="check-item"><span class="check-icon">☑️</span> Notice de sécurité mise à jour (DOE)</div>
        <div class="check-item"><span class="check-icon">☑️</span> Signalisation incendie en place</div>
      </div>
    </div>
  </div>
  <div id="incendie-lexique" class="sub-content">
    <div class="section-card"><h2>📝 Lexique — Protection Incendie</h2>
      <div class="lexique-item"><strong>Compartimentage</strong><p>Division du bâtiment en zones séparées par des parois résistantes au feu pour limiter la propagation de l'incendie.</p></div>
      <div class="lexique-item"><strong>Coupe-feu</strong><p>Élément (cloison, porte, joint) résistant au feu pour une durée déterminée (30, 60, 120 min).</p></div>
      <div class="lexique-item"><strong>EI</strong><p>Étanchéité aux flammes + Isolation thermique. Critères de résistance au feu d'une cloison ou plafond.</p></div>
      <div class="lexique-item"><strong>Enduit intumescent</strong><p>Produit qui gonfle à la chaleur pour protéger les structures métalliques ou bois contre le feu.</p></div>
      <div class="lexique-item"><strong>ERP</strong><p>Établissement Recevant du Public. Soumis à des règles strictes de sécurité incendie.</p></div>
      <div class="lexique-item"><strong>Euroclasse</strong><p>Système européen de classification du comportement au feu des matériaux de construction (A1 à F).</p></div>
      <div class="lexique-item"><strong>IGH</strong><p>Immeuble de Grande Hauteur (> 28m pour habitation, > 28m pour bureaux). Réglementation incendie très stricte.</p></div>
      <div class="lexique-item"><strong>REI</strong><p>Résistance mécanique + Étanchéité + Isolation thermique. Critères pour les parois porteuses.</p></div>
    </div>
  </div>
  <div id="incendie-securite" class="sub-content">
    <div class="section-card"><h2>⛑️ Mémo Prévention & Sécurité — Incendie Chantier</h2>
      <div class="info-box red"><div class="icon">🔥</div><div class="content"><p><strong>Le chantier lui-même est une zone à risque incendie !</strong> Matériaux combustibles (bois, isolant PSE), sources d'ignition (meuleuses, soudures, électricité).</p></div></div>
      <div class="securite-grid">
        <div class="securite-card"><span class="icon">🧯</span><h4>Extincteur</h4><p>Obligatoire sur le chantier. Vérifier la date de contrôle et l'accessibilité.</p></div>
        <div class="securite-card"><span class="icon">🚭</span><h4>Interdiction de fumer</h4><p>Interdit de fumer dans les zones avec matériaux combustibles.</p></div>
        <div class="securite-card"><span class="icon">⚡</span><h4>Installations électriques</h4><p>Tableaux protégés, câbles sans dommage, pas de multiprises surchargées.</p></div>
        <div class="securite-card"><span class="icon">🔥</span><h4>Travaux par points chauds</h4><p>Permis de feu obligatoire. Présence d'un extincteur. Surveillance après travaux 1h min.</p></div>
        <div class="securite-card"><span class="icon">🚪</span><h4>Issues de secours</h4><p>Toujours dégagées, jamais obstruées par des matériaux ou équipements.</p></div>
        <div class="securite-card"><span class="icon">📞</span><h4>Numéros d'urgence</h4><p>18 (Pompiers) - 15 (SAMU) - 17 (Police) - 112 (Urgences européen)</p></div>
      </div>
    </div>
  </div>
  <div id="incendie-quiz" class="sub-content">
    <div class="section-card"><h2>🎯 Questionnaire d'Acquis — Protection Incendie</h2></div>
    <div class="quiz-container" id="quiz-incendie">
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">1</div><div class="q-text">Quels sont les 3 éléments du triangle du feu ?</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="inq1" value="a"> a) Eau, air, terre</label></li>
          <li><label><input type="radio" name="inq1" value="b"> b) Combustible, comburant (oxygène), énergie d'activation</label></li>
          <li><label><input type="radio" name="inq1" value="c"> c) Bois, plastique, métal</label></li>
          <li><label><input type="radio" name="inq1" value="d"> d> Flamme, fumée, chaleur</label></li>
        </ul>
        <div class="answer-feedback" id="inq1-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">2</div><div class="q-text">Quelle Euroclass correspond à un matériau ININFLAMMABLE (béton, acier) ?</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="inq2" value="a"> a) Classe F</label></li>
          <li><label><input type="radio" name="inq2" value="b"> b) Classe A1</label></li>
          <li><label><input type="radio" name="inq2" value="c"> c) Classe C</label></li>
          <li><label><input type="radio" name="inq2" value="d"> d> Classe D</label></li>
        </ul>
        <div class="answer-feedback" id="inq2-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">3</div><div class="q-text">Que signifie "EI 60" pour une cloison ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="inq3" value="a"> a) Épaisseur Isolante de 60 mm</label></li>
          <li><label><input type="radio" name="inq3" value="b"> b) Étanchéité et Isolation thermique pendant 60 minutes</label></li>
          <li><label><input type="radio" name="inq3" value="c"> c) Efficacité Incendie niveau 60</label></li>
          <li><label><input type="radio" name="inq3" value="d"> d> Euroclass Incendie 60 dB</label></li>
        </ul>
        <div class="answer-feedback" id="inq3-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">4</div><div class="q-text">Qu'est-ce que le compartimentage ?</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="inq4" value="a"> a) L'organisation des stocks sur le chantier</label></li>
          <li><label><input type="radio" name="inq4" value="b"> b) La division d'un bâtiment en zones séparées pour limiter la propagation du feu</label></li>
          <li><label><input type="radio" name="inq4" value="c"> c) L'installation des extincteurs</label></li>
          <li><label><input type="radio" name="inq4" value="d"> d> Le balisage des issues de secours</label></li>
        </ul>
        <div class="answer-feedback" id="inq4-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">5</div><div class="q-text">Vrai ou Faux : Une plaque BA13 standard (grise) offre la même résistance au feu qu'une BA13 rose (feu).</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="inq5" value="a"> ✅ Vrai</label></li>
          <li><label><input type="radio" name="inq5" value="b"> ❌ Faux (la BA13 rose contient des additifs spéciaux pour résister plus longtemps au feu)</label></li>
        </ul>
        <div class="answer-feedback" id="inq5-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">6</div><div class="q-text">Mise en situation</div><span class="q-level hard">🔴 Difficile</span></div>
        <div class="scenario-box"><h4>🏗️ Scénario :</h4><p>Tu réalises une cloison séparant deux appartements dans un immeuble. Le règlement exige EI 60. Quelle est la configuration minimale de la cloison placo pour atteindre cet objectif ? Justifie.</p></div>
        <textarea class="open-answer" id="inq6-answer" placeholder="Décris la configuration (montants, plaques, isolant)..."></textarea>
        <button class="btn-check" onclick="checkOpen('inq6')">Voir la correction 📋</button>
        <div class="answer-feedback" id="inq6-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">7</div><div class="q-text">Quel produit gonfle au contact de la chaleur pour protéger une structure ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="inq7" value="a"> a) L'enduit de lissage</label></li>
          <li><label><input type="radio" name="inq7" value="b"> b) L'enduit intumescent</label></li>
          <li><label><input type="radio" name="inq7" value="c"> c) La mousse polyuréthane</label></li>
          <li><label><input type="radio" name="inq7" value="d"> d> Le ciment réfractaire</label></li>
        </ul>
        <div class="answer-feedback" id="inq7-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">8</div><div class="q-text">Qu'est-ce qu'un "permis de feu" ?</div><span class="q-level medium">🟡 Moyen</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="inq8" value="a"> a) Une autorisation de construire</label></li>
          <li><label><input type="radio" name="inq8" value="b"> b"> Un document autorisant des travaux à risque (soudure, meulage) sur un chantier</label></li>
          <li><label><input type="radio" name="inq8" value="c"> c) Un brevet de pompier</label></li>
          <li><label><input type="radio" name="inq8" value="d"> d> Une certification de matériau ignifuge</label></li>
        </ul>
        <div class="answer-feedback" id="inq8-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">9</div><div class="q-text">Pourquoi doit-on traiter les traversées de câbles et tuyaux dans une paroi coupe-feu ?</div><span class="q-level hard">🔴 Difficile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="inq9" value="a"> a) Pour l'isolation phonique uniquement</label></li>
          <li><label><input type="radio" name="inq9" value="b"> b"> Pour éviter que le feu se propage d'un compartiment à l'autre par les ouvertures</label></li>
          <li><label><input type="radio" name="inq9" value="c"> c) Pour des raisons esthétiques</label></li>
          <li><label><input type="radio" name="inq9" value="d"> d> Pour protéger les câbles de l'humidité</label></li>
        </ul>
        <div class="answer-feedback" id="inq9-feedback"></div>
      </div>
      <div class="quiz-question">
        <div class="q-header"><div class="q-num">10</div><div class="q-text">Vrai ou Faux : Une issue de secours peut être temporairement obstruée par des matériaux de chantier.</div><span class="q-level easy">🟢 Facile</span></div>
        <ul class="quiz-options">
          <li><label><input type="radio" name="inq10" value="a"> ✅ Vrai</label></li>
          <li><label><input type="radio" name="inq10" value="b"> ❌ Faux (jamais obstruée : risque vital en cas d'évacuation)</label></li>
        </ul>
        <div class="answer-feedback" id="inq10-feedback"></div>
      </div>
      <div class="quiz-footer">
        <button class="btn-submit" onclick="submitQuiz('incendie', 10)">🎯 Calculer mon score !</button>
        <div class="score-display" id="score-incendie"></div>
      </div>
    </div>
  </div>
</div><!-- END INCENDIE -->

</div><!-- END CONTENT-AREA -->

<script>
// ================================================
// NAVIGATION
// ================================================
function showTab(tabId, btn) {
  document.querySelectorAll('.tab-content').forEach(t => t.classList.remove('active'));
  document.querySelectorAll('.main-nav button').forEach(b => b.classList.remove('active'));
  document.getElementById(tabId).classList.add('active');
  btn.classList.add('active');
  window.scrollTo(0, 0);
}

function showSub(tabId, subId, btn) {
  const parentTab = document.getElementById(tabId);
  parentTab.querySelectorAll('.sub-content').forEach(s => s.classList.remove('active'));
  parentTab.querySelectorAll('.sub-tab-btn').forEach(b => b.classList.remove('active'));
  document.getElementById(tabId + '-' + subId).classList.add('active');
  btn.classList.add('active');
}

// ================================================
// QUIZ ANSWERS
// ================================================
const answers = {
  // CARRELAGE
  cq1: 'b', cq2: 'a', cq3: 'b', cq4: 'b', cq5: 'b',
  cq6: 'b', cq7: 'a', cq8: 'b', cq10: 'c',
  // PEINTURE
  pq1: 'b', pq2: 'b', pq3: 'b', pq4: 'c', pq5: 'b',
  pq6: 'b', pq8: 'b', pq9: 'b', pq10: 'b',
  // PAPIER PEINT
  ppq1: 'b', ppq2: 'b', ppq3: 'b', ppq4: 'a',
  ppq6: 'c', ppq7: 'c', ppq8: 'b', ppq9: 'c',
  // SOL SOUPLE
  ssq1: 'b', ssq2: 'b', ssq3: 'b', ssq4: 'b', ssq5: 'b',
  ssq6: 'b', ssq8: 'b', ssq9: 'a', ssq10: 'c',
  // CARREAUX PLATRE
  cpq1: 'b', cpq2: 'b', cpq3: 'b', cpq4: 'b', cpq5: 'b',
  cpq7: 'b', cpq8: 'a', cpq9: 'b', cpq10: 'b',
  // CLOISON
  clq1: 'b', clq2: 'b', clq3: 'b', clq4: 'b', clq5: 'b',
  clq7: 'b', clq8: 'b', clq9: 'b', clq10: 'b',
  // DOUBLAGE
  dq1: 'b', dq2: 'b', dq3: 'b', dq4: 'b',
  dq6: 'b', dq7: 'c', dq8: 'a', dq9: 'b', dq10: 'b',
  // PLAFOND SUSPENDU
  psq1: 'b', psq2: 'b', psq3: 'b', psq4: 'b', psq5: 'b',
  psq7: 'b', psq8: 'b', psq9: 'b', psq10: 'b',
  // PLAFOND AUTOPORTANT
  paq1: 'b', paq2: 'b', paq3: 'b', paq4: 'b',
  paq6: 'b', paq7: 'a', paq8: 'b', paq9: 'b', paq10: 'b',
  // PLAFOND MODULAIRE
  pmq1: 'b', pmq2: 'b', pmq3: 'b', pmq4: 'b', pmq5: 'b',
  pmq7: 'b', pmq8: 'b', pmq9: 'b', pmq10: 'b',
  // ITE
  iteq1: 'b', iteq2: 'b', iteq3: 'b', iteq4: 'b', iteq5: 'b',
  iteq7: 'b', iteq8: 'b', iteq9: 'b', iteq10: 'c',
  // PHONIQUE
  phq1: 'b', phq2: 'b', phq3: 'b', phq4: 'b', phq5: 'b',
  phq7: 'b', phq8: 'b', phq9: 'b', phq10: 'b',
  // THERMIQUE
  thq1: 'b', thq2: 'b', thq3: 'b', thq4: 'a',
  thq6: 'b', thq7: 'b', thq8: 'b', thq9: 'b', thq10: 'b',
  // INCENDIE
  inq1: 'b', inq2: 'b', inq3: 'b', inq4: 'b', inq5: 'b',
  inq7: 'b', inq8: 'b', inq9: 'b', inq10: 'b'
};

const explanations = {
  cq1: "La faïence est un carreau céramique poreuse et émaillée, principalement utilisé sur les murs intérieurs.",
  cq2: "SPEC = Système de Protection à l'Eau sous Carrelage.",
  cq3: "FAUX : Le SEL (Système d'Étanchéité Liquide) s'applique sur les SOLS horizontaux. Le SPEC s'applique sur les parois verticales.",
  cq4: "La colle C2 S1 est déformable et améliorée, idéale pour les grands formats, planchers chauffants et façades.",
  cq5: "La tolérance est de 5mm sous la règle de 2m pour le carrelage.",
  cq6: "Le 'E' de UPEC signifie Eau (résistance à l'eau et aux liquides).",
  cq7: "28 jours de séchage permet à la dalle d'atteindre sa résistance et son taux d'humidité acceptable (≤4%) avant l'application du SEL.",
  cq8: "FAUX : Les plaques hydrofuges ne suffisent pas. Il faut impérativement appliquer un SPEC sur les parois et un SEL sur le sol.",
  cq9: "Points critiques : 1) Dalle trop jeune (< 28j), appliquer SEL uniquement après 28j. 2) Colle C2S1 obligatoire (grand format + conditions). 3) SPEC sur les murs + SEL sol zone EB+.",
  cq10: "En extérieur exposé au gel, utiliser une colle C2 S1 ou C2 S2 (déformable, résistant aux cycles gel/dégel).",
  pq1: "Le liant est le composant qui fixe les pigments au support et forme le film dur et adhérent.",
  pq2: "Le cloquage est causé par l'humidité sous le film (support trop humide lors de l'application).",
  pq3: "FAUX : La peinture glycérophtalique est à base de solvant (white-spirit), pas d'eau.",
  pq4: "La Finition A (Soigné) est le niveau haut de gamme de la norme NF DTU 59.1 : préparation soignée, enduits, égrenage inter-couches, observation en lumière rasante admise.",
  pq5: "Il faut traiter le problème à la source : traiter avec fongicide, traiter l'humidité (ventilation, isolation), puis repeindre avec une peinture antifongique.",
  pq6: "Le farinage est un dépôt poudreux résultant de la dégradation du liant en surface.",
  pq7: "Causes possibles : support non préparé/gras, mauvais primaire, incompatibilité des couches. Reprise : décaper entièrement, nettoyer, reprimer et peindre par couches compatibles.",
  pq8: "Les COV des peintures solvantées sont toxiques pour les voies respiratoires et inflammables. La ventilation est obligatoire.",
  pq9: "FAUX : Un primaire n'est pas toujours obligatoire pour la peinture acrylique. Il est recommandé sur support absorbant ou neuf.",
  pq10: "Salle de bain = humidité : choisir une peinture acrylique satinée antifongique spécialement formulée pour les pièces humides.",
  ppq1: "Pour l'intissé, la colle s'applique sur le MUR (pas sur le papier). Caractéristique fondamentale de l'intissé.",
  ppq2: "Selon le DTU 59.4, l'humidité maximale d'un support plâtre est de 5% avant pose de papier peint.",
  ppq3: "La coupe double superpose deux lés et les coupe simultanément à la règle bombée avec un kicoup lame neuve. OBLIGATOIRE dans les angles rentrants et sortants.",
  ppq4: "VRAI : Selon le DTU 59.4 art. 3.1, en l'absence de précision dans les pièces du marché, la finition B est retenue.",
  ppq5: "DTU 59.4 art. 4.2.2 : Conditions non conformes → Aviser PAR ÉCRIT le maître d'ouvrage. Celui-ci décidera d'ajourner les travaux (avec prorogation de délai) ou de mettre en place un chauffage progressif. Les frais de chauffage font l'objet d'un accord préalable.",
  ppq6: "Le raccord sauté entraîne les chutes les plus importantes car le motif est décalé tous les 2 lés. Travailler avec 2 rouleaux simultanément.",
  ppq7: "La garantie minimale est de 2 ans à compter de la réception (loi du 4 janvier 1978, art. 1792-3 Code Civil — garantie de bon fonctionnement).",
  ppq8: "Selon le DTU 59.4, l'écart maximal admis entre deux lés est de 1mm. Aucun chevauchement n'est admis.",
  ppq9: "Le revêtement vinyle contrecollé (Vescom, Buflon) est le plus adapté aux usages intensifs : résistant, lavable, durable. Idéal pour les collectivités.",
  ppq10: "DTU 59.4 art. 4.2.1 : L'entrepreneur doit reconnaître les subjectiles et noter les défauts PAR ÉCRIT au maître d'ouvrage. Avant tout début d'exécution, le maître d'ouvrage décide de la suite (examen contradictoire). La mise en conformité fait l'objet d'un ordre de service qui prolonge le délai.",
  ssq1: "Le CME (Carbure Mètre d'Eau) mesure l'humidité du support par réaction chimique.",
  ssq2: "La télégraphie est l'apparition des irrégularités du support à travers le revêtement souple.",
  ssq3: "FAUX : Pour le sol souple, la tolérance est plus stricte : ≤ 3mm sous règle de 2m (vs 5mm pour carrelage).",
  ssq4: "Le rouleau lourd assure un contact uniforme sur toute la surface entre le revêtement et la colle.",
  ssq5: "Le linoléum est un matériau naturel à base d'huile de lin, farines de bois et liège.",
  ssq6: "Le conditionnement permet l'adaptation aux conditions hygrométriques et thermiques, évitant les dilatations post-pose.",
  ssq7: "Causes : humidité support, colle mal dosée, mauvais temps ouvert, roulage insuffisant. Reprise : recoller avec colle adaptée, utiliser rouleau lourd, traiter l'humidité.",
  ssq8: "4% est le taux maximal d'humidité (CME) autorisé pour un sol souple collé.",
  ssq9: "VRAI : La soudure à chaud utilise un pistolet thermique réglé à environ 400°C.",
  ssq10: "Salle de sport avec chariots = U4P4E2C2 minimum (très haute résistance).",
  cpq1: "En salle de bain (local humide), utiliser les carreaux type H (Hydrofugés).",
  cpq2: "La pose en quinconce décale les joints verticaux d'au moins 1/4 de carreau pour renforcer la cloison.",
  cpq3: "FAUX : Les carreaux de plâtre ne sont PAS porteurs. Ils servent uniquement à créer des cloisons de séparation non-structurelles.",
  cpq4: "La bande de désolidarisation évite la transmission des vibrations (bruits) de la structure vers la cloison.",
  cpq5: "48h minimum sont nécessaires avant d'appliquer enduit ou peinture sur une cloison neuve en carreaux de plâtre.",
  cpq6: "Utiliser des carreaux type H (hydrofugés), appliquer un SPEC sur les parois avant carrelage, assurer ventilation correcte.",
  cpq7: "Format standard courant : 50×25 cm ou 66×50 cm.",
  cpq8: "Le plâtre contient de l'eau chimiquement liée qui se libère sous l'effet de la chaleur (calcination), ralentissant la propagation du feu.",
  cpq9: "FAUX : Les carreaux type S ne sont pas adaptés aux zones humides comme les douches. Utiliser type H.",
  cpq10: "La barbotine est du plâtre très fluide utilisé pour encoller les bords des carreaux lors de la pose.",
  clq1: "BA13 = Bord Aminci, 13mm d'épaisseur.",
  clq2: "BA13 verte hydrofugée pour les locaux humides (salle de bain, cuisine).",
  clq3: "FAUX : L'entraxe standard est de 40 ou 60 cm selon la configuration.",
  clq4: "Les joints décalés entre les deux faces renforcent la rigidité de la cloison et évitent les fissures traversantes.",
  clq5: "La bande acoustique empêche la transmission des bruits d'impact entre la structure et la cloison.",
  clq6: "Solutions : double ossature désolidarisée, double plaque, laine de roche entre plaques, bandes acoustiques sur tous les rails.",
  clq7: "Les vis TF (Tête Fraisée) s'enfoncent dans la plaque sans la transpercer ni dépasser.",
  clq8: "FAUX : 72mm = épaisseur totale de la cloison. Le montant mesure 48mm de large.",
  clq9: "Ordre correct : Tracé → Rails → Montants → Réseaux → Plaques → Joints.",
  clq10: "Tolérance de planéité cloison placo : ≤ 5mm sous règle de 2m.",
  dq1: "Le complexe de doublage associe en usine une plaque de plâtre et un isolant (PSE, PU ou laine).",
  dq2: "Le polyuréthane a le λ le plus faible (≈ 0,022 W/m.K), meilleure performance thermique.",
  dq3: "FAUX : Le pare-vapeur se place côté CHAUD (intérieur) pour empêcher la vapeur d'eau de migrer vers l'isolant et de condenser.",
  dq4: "Un pont thermique est une zone où l'isolation est interrompue, créant une déperdition thermique localisée.",
  dq5: "Cause : ponts thermiques en périphérie (angles murs/plafond mal traités), condensation s'y développe. Solution : traiter les angles avec isolation continue et améliorer la ventilation.",
  dq6: "La RE2020 est la réglementation pour les bâtiments neufs depuis 2022.",
  dq7: "La laine de roche est incombustible (classe A1) = meilleure résistance incendie.",
  dq8: "VRAI : Le doublage occupe toujours une épaisseur sur l'un ou plusieurs murs.",
  dq9: "R = 0,10 / 0,04 = 2,5 m².K/W.",
  dq10: "Le doublage collé est fixé par des plots de plâtre ou de colle disposés sur le mur.",
  psq1: "La suspente relie la fourrure à la structure porteuse (dalle ou charpente) et permet le réglage de hauteur.",
  psq2: "Hauteur minimale réglementaire sous plafond en logement : 2,20m.",
  psq3: "FAUX : La tolérance est ±3mm (plus stricte que les 5mm du carrelage).",
  psq4: "La bande acoustique évite les bruits d'impact transmis de la structure au plafond suspendu.",
  psq5: "Les fourrures se posent perpendiculairement aux joints des plaques pour les soutenir correctement.",
  psq6: "Causes : suspentes mal réglées (hauteurs inégales), fourrures insuffisamment fixées, jointoiement humide, mauvais entraxe. Prévention : utiliser niveau laser, vérifier chaque suspente.",
  psq7: "Le niveau laser permet de mettre les fourrures à la même hauteur avec précision.",
  psq8: "FAUX : Il faut un plateau de travail ou un échafaudage roulant pour travailler en sécurité au plafond.",
  psq9: "De la laine minérale est placée au-dessus des fourrures pour l'isolation acoustique et thermique.",
  psq10: "Le plafond autoportant repose uniquement sur les murs (sans suspentes à la dalle), contrairement au plafond suspendu.",
  paq1: "Le plafond autoportant repose uniquement sur les murs via les rails de rive.",
  paq2: "Sans lien avec la dalle, les bruits d'impact (pas, chocs) ne se transmettent pas directement au plafond.",
  paq3: "FAUX : La portée est limitée à environ 6m selon le DTU 58.1.",
  paq4: "Si les fourrures touchent la dalle, le principe acoustique est rompu (pont phonique) : les bruits d'impact se transmettent directement.",
  paq5: "Solution plafond autoportant : ossature non liée à la dalle. Les bruits d'impact du plancher ne se transmettent plus directement.",
  paq6: "DTU 58.1 régit les plafonds en plaques de plâtre.",
  paq7: "VRAI : La bande acoustique est obligatoire sous tous les rails d'un plafond autoportant.",
  paq8: "Tolérance ±3mm sur 2m pour les plafonds placo.",
  paq9: "L'immeuble collectif avec gêne sonore entre étages est le cas d'usage principal du plafond autoportant.",
  paq10: "Le niveau laser trace le niveau sur les 4 murs avec précision.",
  pmq1: "L'accès facile aux réseaux (en retirant les dalles) est le principal avantage du plafond modulaire.",
  pmq2: "60×60 cm est le format standard le plus courant des dalles de plafond modulaire.",
  pmq3: "Le calepinage est le plan de répartition des dalles pour centrer la grille et optimiser les coupes de bordure.",
  pmq4: "Bureaux, commerces, hôpitaux = bâtiments tertiaires = usage principal des plafonds modulaires.",
  pmq5: "FAUX : Des lots différents peuvent avoir des teintes légèrement différentes → utiliser un seul lot.",
  pmq6: "Il fallait réaliser un calepinage au préalable : mesurer la pièce, centrer la grille et s'assurer que les dalles de bordure mesurent au moins la moitié d'une dalle complète.",
  pmq7: "Laine minérale haute absorption acoustique (classe A) pour réduire la réverbération.",
  pmq8: "FAUX : T24 est apparent (grille visible), T0 est encastré (plus discret).",
  pmq9: "Le sprinkler est une tête d'extincteur automatique à eau intégrée dans le plafond pour la sécurité incendie.",
  pmq10: "Tolérance ±3mm sur 2m pour les plafonds modulaires.",
  iteq1: "ITE = Isolation Thermique par l'Extérieur.",
  iteq2: "L'ITE supprime les ponts thermiques et préserve toute la surface habitable intérieure.",
  iteq3: "ETICS = External Thermal Insulation Composite System = système ITE avec enduit armé sur isolant.",
  iteq4: "FAUX : Conditions d'application : 5°C < T° < 30°C, sans pluie, ni vent fort.",
  iteq5: "La laine de roche est incombustible (classe A1) = sécurité incendie maximale.",
  iteq6: "Cause : absence de renforts diagonaux aux angles des baies. Solution : poser des morceaux de treillis en diagonale (45°) à tous les angles de fenêtres.",
  iteq7: "Le larmier soutient les premiers panneaux et rejette l'eau loin de la façade et des fondations.",
  iteq8: "Le chevillage assure la résistance au vent (dépression) qui pourrait décoller les panneaux collés.",
  iteq9: "FAUX : Dans certaines zones (site classé, ABF), une déclaration préalable ou un permis peut être requis.",
  iteq10: "Le polyuréthane a λ ≈ 0,022 W/m.K, le meilleur parmi les options proposées.",
  phq1: "Les bruits d'impact sont transmis par la structure : pas, chutes, travaux sur plancher.",
  phq2: "Un Rw élevé = paroi très résistante aux bruits aériens = bonne isolation phonique.",
  phq3: "FAUX : Un sol flottant améliore principalement les bruits d'impact (transmission structurelle).",
  phq4: "Les traversées créent des ponts phoniques : la vibration passe par le câble ou tuyau d'une pièce à l'autre.",
  phq5: "La laine de roche est bien meilleure acoustiquement que le PSE, grâce à sa structure fibreuse absorbante.",
  phq6: "Solution : doublage placo avec double plaque + laine de roche + désolidarisation complète. Points critiques : traitement des traversées, bandes acoustiques, joints périphériques.",
  phq7: "Ln,w = Niveau normalisé de bruit d'impact pondéré. Mesure la transmission des bruits d'impact.",
  phq8: "FAUX : Un Ln,w faible = meilleure isolation aux bruits d'impact (moins de bruit transmis).",
  phq9: "NRA : isolement minimum DnT,A ≥ 53 dB entre logements.",
  phq10: "Le décibel (dB) est l'unité de mesure de l'intensité sonore.",
  thq1: "R = e (épaisseur en m) / λ (conductivité en W/m.K).",
  thq2: "La ouate de cellulose (papier recyclé) est l'isolant naturel le plus utilisé en insufflation dans les combles.",
  thq3: "U élevé = paroi très conductrice = mauvaise isolation thermique (beaucoup de chaleur perdue).",
  thq4: "VRAI : La RE2020 remplace la RT2012 pour les bâtiments neufs depuis le 1er janvier 2022.",
  thq5: "R = 0,10/0,04 = 2,5 m².K/W. Non suffisant (< 3,7). Conseiller d'augmenter à au moins 15 cm (R=3,75).",
  thq6: "Le pare-vapeur se place côté CHAUD (intérieur) pour éviter la condensation dans l'isolant.",
  thq7: "La caméra thermique infrarouge visualise les déperditions et ponts thermiques.",
  thq8: "FAUX : Le PSE est combustible (s'enflamme et dégage des gaz toxiques). La laine de roche est incombustible.",
  thq9: "λ polyuréthane ≈ 0,022 W/m.K = meilleure performance thermique pour faible épaisseur.",
  thq10: "La convection est le déplacement d'air chaud par les défauts d'étanchéité (fissures, jonctions mal traitées).",
  inq1: "Triangle du feu : combustible (matière) + comburant (oxygène) + énergie d'activation (chaleur).",
  inq2: "Classe A1 = ininflammable : béton, acier, verre, laine de roche.",
  inq3: "EI 60 = Étanchéité + Isolation thermique pendant 60 minutes.",
  inq4: "Le compartimentage divise le bâtiment en zones séparées par des parois résistantes au feu.",
  inq5: "FAUX : BA13 rose contient des additifs ignifuges qui augmentent sa résistance au feu.",
  inq6: "Pour EI 60 : ossature 48mm + laine de roche 45mm + 2×BA13 feu (rose) de chaque côté = système homologué EI 60.",
  inq7: "L'enduit intumescent gonfle au contact de la chaleur pour isoler et protéger la structure.",
  inq8: "Le permis de feu est un document obligatoire pour les travaux à risque (soudure, meulage) sur un chantier.",
  inq9: "Les traversées créent des ouvertures dans les parois coupe-feu, permettant la propagation du feu et des fumées.",
  inq10: "FAUX : Les issues de secours ne doivent JAMAIS être obstruées, même temporairement."
};

function checkMultipleChoice(name, qId) {
  const selected = document.querySelector(`input[name="${name}"]:checked`);
  const feedback = document.getElementById(`${qId}-feedback`);
  if (!selected) {
    feedback.style.display = 'block';
    feedback.className = 'answer-feedback wrong';
    feedback.innerHTML = '⚠️ Sélectionne une réponse !';
    return false;
  }
  const isCorrect = selected.value === answers[name];
  feedback.style.display = 'block';
  if (isCorrect) {
    feedback.className = 'answer-feedback correct';
    feedback.innerHTML = `✅ Bonne réponse ! ${explanations[name] ? '💡 ' + explanations[name] : ''}`;
  } else {
    const correctAnswer = answers[name];
    const correctLabel = document.querySelector(`input[name="${name}"][value="${correctAnswer}"]`)?.parentElement?.textContent.trim() || '';
    feedback.className = 'answer-feedback wrong';
    feedback.innerHTML = `❌ Mauvaise réponse. La bonne réponse est : <strong>${correctLabel}</strong><br>💡 ${explanations[name] || ''}`;
  }
  return isCorrect;
}

function checkOpen(qId) {
  const feedback = document.getElementById(`${qId}-feedback`);
  const answer = document.getElementById(`${qId}-answer`)?.value.trim();
  if (!answer || answer.length < 10) {
    feedback.style.display = 'block';
    feedback.className = 'answer-feedback wrong';
    feedback.innerHTML = '⚠️ Écris une réponse avant de voir la correction !';
    return;
  }
  feedback.style.display = 'block';
  feedback.className = 'answer-feedback correct';
  feedback.innerHTML = `📋 <strong>Correction :</strong> ${explanations[qId] || 'Consultez le cours pour la correction détaillée.'}`;
}

// QUIZ SUBMIT
function submitQuiz(prefix, total) {
  const quizMap = {
    carrelage: ['cq1','cq2','cq3','cq4','cq5','cq6','cq7','cq8','cq10'],
    peinture: ['pq1','pq2','pq3','pq4','pq5','pq6','pq8','pq9','pq10'],
    papierpeint: ['ppq1','ppq2','ppq3','ppq4','ppq6','ppq7','ppq8','ppq9'],
    solsouple: ['ssq1','ssq2','ssq3','ssq4','ssq5','ssq6','ssq8','ssq9','ssq10'],
    carreauxplatre: ['cpq1','cpq2','cpq3','cpq4','cpq5','cpq7','cpq8','cpq9','cpq10'],
    cloison: ['clq1','clq2','clq3','clq4','clq5','clq7','clq8','clq9','clq10'],
    doublage: ['dq1','dq2','dq3','dq4','dq6','dq7','dq8','dq9','dq10'],
    plafondsuspendu: ['psq1','psq2','psq3','psq4','psq5','psq7','psq8','psq9','psq10'],
    plafondautoportant: ['paq1','paq2','paq3','paq4','paq6','paq7','paq8','paq9','paq10'],
    plafondmodulaire: ['pmq1','pmq2','pmq3','pmq4','pmq5','pmq7','pmq8','pmq9','pmq10'],
    ite: ['iteq1','iteq2','iteq3','iteq4','iteq5','iteq7','iteq8','iteq9','iteq10'],
    phonique: ['phq1','phq2','phq3','phq4','phq5','phq7','phq8','phq9','phq10'],
    thermique: ['thq1','thq2','thq3','thq4','thq6','thq7','thq8','thq9','thq10'],
    incendie: ['inq1','inq2','inq3','inq4','inq5','inq7','inq8','inq9','inq10']
  };

  const questions = quizMap[prefix] || [];
  let score = 0;
  let answered = 0;

  questions.forEach(name => {
    const sel = document.querySelector(`input[name="${name}"]:checked`);
    if (sel) {
      answered++;
      const feedback = document.getElementById(`${name}-feedback`);
      const isCorrect = sel.value === answers[name];
      if (isCorrect) {
        score++;
      }
      if (!feedback.style.display || feedback.style.display === 'none') {
        feedback.style.display = 'block';
        if (isCorrect) {
          feedback.className = 'answer-feedback correct';
          feedback.innerHTML = `✅ Bonne réponse ! ${explanations[name] ? '💡 ' + explanations[name] : ''}`;
        } else {
          const correctAnswer = answers[name];
          const correctLabel = document.querySelector(`input[name="${name}"][value="${correctAnswer}"]`)?.parentElement?.textContent.trim() || '';
          feedback.className = 'answer-feedback wrong';
          feedback.innerHTML = `❌ Mauvaise réponse. La bonne : <strong>${correctLabel}</strong><br>💡 ${explanations[name] || ''}`;
        }
      }
    }
  });

  const percent = Math.round((score / questions.length) * 100);
  const scoreDiv = document.getElementById(`score-${prefix}`);
  scoreDiv.classList.add('show');

  let emoji = '😔';
  let msg = 'Continue tes révisions !';
  if (percent >= 90) { emoji = '🏆'; msg = 'Excellent ! Tu maîtrises très bien ce cours !'; }
  else if (percent >= 75) { emoji = '🌟'; msg = 'Très bien ! Quelques petites révisions et tu seras parfait !'; }
  else if (percent >= 60) { emoji = '👍'; msg = 'Bien ! Tu as les bases, continue tes révisions.'; }
  else if (percent >= 40) { emoji = '📚'; msg = 'Des lacunes à combler. Relis le cours et retente !'; }

  scoreDiv.innerHTML = `
    <div style="font-size:3em; margin-bottom:10px;">${emoji}</div>
    <div style="color:${percent >= 60 ? 'var(--accent2)' : 'var(--accent3)'}; font-size:2.5em; font-weight:bold;">${percent}%</div>
    <div style="font-size:1em; color:var(--text-light);">Score : ${score} / ${questions.length} bonnes réponses</div>
    <div class="score-message">${msg}</div>
    <div class="progress-bar" style="max-width:400px;margin:15px auto;">
      <div class="fill" style="width:${percent}%"></div>
    </div>
  `;
  scoreDiv.scrollIntoView({behavior:'smooth'});
}
</script>
</body>
</html>
