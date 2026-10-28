# Padew-Cubing-League-PCLindex.html
<!doctype html>
<html lang="pl">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <meta name="theme-color" content="#101317">
  <meta name="description" content="Padew Cubing League — informacje o lokalnej społeczności układającej kostkę Rubika w Padwi Narodowej.">
  <title>Padew Cubing League | PCL</title>
  <style>
    :root {
      color-scheme: dark;
      --bg: #101317;
      --surface: #171c22;
      --surface-2: #1d242c;
      --line: #2a333d;
      --text: #f3f6f9;
      --muted: #a6b0bb;
      --blue: #65a9ff;
      --blue-strong: #3185ef;
      --radius: 18px;
      --width: 1120px;
      font-family: Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
    }
    * { box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body { margin: 0; min-width: 320px; background: var(--bg); color: var(--text); line-height: 1.6; }
    button, input, textarea, select { font: inherit; }
    button, a { -webkit-tap-highlight-color: transparent; }
    a { color: var(--blue); text-decoration: none; }
    a:hover { color: #a1ceff; }
    button { color: inherit; }
    .wrap { width: min(var(--width), calc(100% - 40px)); margin-inline: auto; }
    .topbar { position: sticky; z-index: 10; top: 0; border-bottom: 1px solid rgba(255,255,255,.07); background: rgba(16,19,23,.92); backdrop-filter: blur(16px); }
    .topbar-inner { min-height: 76px; display: flex; align-items: center; justify-content: space-between; gap: 22px; }
    .brand { display: inline-flex; align-items: center; gap: 12px; color: var(--text); font-weight: 750; letter-spacing: -.03em; white-space: nowrap; }
    .brand-mark { display: grid; width: 38px; height: 38px; place-items: center; border-radius: 12px; background: var(--blue-strong); color: #fff; font-size: 15px; letter-spacing: -.04em; }
    .brand-copy { line-height: 1.15; }
    .brand-copy small { display: block; margin-top: 4px; color: var(--muted); font-size: 10px; font-weight: 600; letter-spacing: .13em; text-transform: uppercase; }
    .nav { display: flex; align-items: center; gap: 4px; overflow-x: auto; scrollbar-width: none; }
    .nav::-webkit-scrollbar { display: none; }
    .nav-link { flex: 0 0 auto; border: 0; border-radius: 10px; padding: 9px 11px; background: transparent; color: var(--muted); font-size: 13px; font-weight: 650; cursor: pointer; transition: .18s ease; }
    .nav-link:hover, .nav-link[aria-current="page"] { background: var(--surface-2); color: var(--text); }
    .nav-link[aria-current="page"] { box-shadow: inset 0 -2px var(--blue); }
    .admin-trigger, .button { display: inline-flex; min-height: 42px; align-items: center; justify-content: center; gap: 8px; border: 1px solid var(--line); border-radius: 11px; padding: 9px 14px; background: var(--surface); color: var(--text); font-size: 13px; font-weight: 700; cursor: pointer; transition: .18s ease; }
    .admin-trigger:hover, .button:hover { border-color: #4c5967; background: var(--surface-2); }
    .button.primary { border-color: var(--blue-strong); background: var(--blue-strong); color: #fff; }
    .button.primary:hover { background: #1c70d8; }
    .button.quiet { background: transparent; }
    .button.danger { border-color: #62383b; background: #291b1d; color: #ffb1b5; }
    .button.small { min-height: 34px; padding: 6px 10px; font-size: 12px; }
    main { min-height: calc(100vh - 150px); }
    .view { display: none; padding: 46px 0 80px; animation: appear .22s ease both; }
    .view.active { display: block; }
    @keyframes appear { from { opacity: 0; transform: translateY(5px); } to { opacity: 1; transform: translateY(0); } }
    .eyebrow { margin: 0 0 12px; color: var(--blue); font-size: 11px; font-weight: 800; letter-spacing: .16em; text-transform: uppercase; }
    h1, h2, h3, p { margin-top: 0; }
    h1 { max-width: 800px; margin-bottom: 18px; font-size: clamp(38px, 6vw, 66px); line-height: 1.02; letter-spacing: -.055em; }
    h2 { margin-bottom: 10px; font-size: clamp(25px, 3.8vw, 38px); line-height: 1.12; letter-spacing: -.04em; }
    h3 { margin-bottom: 9px; font-size: 18px; line-height: 1.3; letter-spacing: -.02em; }
    .lead { max-width: 690px; color: var(--muted); font-size: clamp(16px, 2vw, 19px); }
    .hero { position: relative; overflow: hidden; min-height: 400px; display: flex; align-items: center; border: 1px solid var(--line); border-radius: 26px; padding: clamp(30px, 7vw, 76px); background: radial-gradient(ellipse at 93% 15%, rgba(49,133,239,.19), transparent 38%), linear-gradient(135deg, #191f26 0%, #14191f 65%, #11151a 100%); }
    .hero:after { position: absolute; right: 7%; bottom: -92px; width: 280px; height: 280px; border: 1px solid rgba(101,169,255,.16); border-radius: 36px; content: ""; transform: rotate(25deg); box-shadow: 0 0 0 24px rgba(101,169,255,.025), 0 0 0 48px rgba(101,169,255,.02); pointer-events: none; }
    .hero-content { position: relative; z-index: 1; max-width: 750px; }
    .hero .lead { max-width: 600px; }
    .actions { display: flex; flex-wrap: wrap; gap: 10px; margin-top: 26px; }
    .intro-grid { display: grid; grid-template-columns: minmax(0, 1.2fr) minmax(250px, .8fr); gap: 18px; margin-top: 20px; }
    .panel, .card { border: 1px solid var(--line); border-radius: var(--radius); background: var(--surface); }
    .panel { padding: 24px; }
    .panel p:last-child, .card p:last-child { margin-bottom: 0; }
    .section-heading { display: flex; align-items: end; justify-content: space-between; gap: 20px; margin-bottom: 24px; }
    .section-heading p { max-width: 650px; margin-bottom: 0; color: var(--muted); }
    .stat-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 14px; margin-top: 30px; }
    .stat-card { min-height: 150px; padding: 22px; }
    .stat-value { margin: 12px 0 2px; color: var(--text); font-size: clamp(36px, 5vw, 52px); font-weight: 780; line-height: 1; letter-spacing: -.06em; }
    .stat-label { color: var(--muted); font-size: 13px; }
    .card-grid { display: grid; grid-template-columns: repeat(3, minmax(0,1fr)); gap: 14px; }
    .card { display: flex; min-height: 178px; flex-direction: column; padding: 21px; }
    .card p { color: var(--muted); white-space: pre-wrap; }
    .card-meta { margin: 0 0 11px; color: var(--blue); font-size: 11px; font-weight: 750; letter-spacing: .1em; text-transform: uppercase; }
    .card-link { margin-top: auto; padding-top: 12px; font-weight: 700; }
    .empty { grid-column: 1 / -1; border: 1px dashed #36414d; border-radius: var(--radius); padding: 25px; color: var(--muted); }
    .contact-grid { display: grid; grid-template-columns: repeat(2, minmax(0,1fr)); gap: 14px; margin-top: 25px; }
    .contact-row { padding: 18px; border: 1px solid var(--line); border-radius: 14px; background: var(--surface); }
    .contact-row small { display: block; margin-bottom: 6px; color: var(--muted); font-size: 11px; font-weight: 750; letter-spacing: .1em; text-transform: uppercase; }
    .note { margin-top: 18px; color: var(--muted); font-size: 13px; }
    .footer { border-top: 1px solid rgba(255,255,255,.07); padding: 22px 0; color: var(--muted); font-size: 12px; }
    .footer-inner { display: flex; justify-content: space-between; gap: 16px; }
    .connection-note { display: none; margin: 0 0 18px; border: 1px solid #5b4c2d; border-radius: 12px; padding: 11px 14px; background: #211e17; color: #e9d6aa; font-size: 13px; }
    .connection-note.show { display: block; }
    dialog { width: min(760px, calc(100% - 24px)); max-height: min(90vh, 900px); border: 1px solid #36414d; border-radius: 20px; padding: 0; background: #14191f; color: var(--text); box-shadow: 0 24px 100px rgba(0,0,0,.65); }
    dialog::backdrop { background: rgba(4,7,10,.78); backdrop-filter: blur(5px); }
    .dialog-head { display: flex; align-items: center; justify-content: space-between; gap: 15px; border-bottom: 1px solid var(--line); padding: 19px 22px; }
    .dialog-head h2 { margin: 0; font-size: 21px; }
    .dialog-body { max-height: calc(90vh - 72px); overflow-y: auto; padding: 22px; }
    .close-button { width: 36px; height: 36px; border: 1px solid var(--line); border-radius: 10px; background: var(--surface); cursor: pointer; font-size: 19px; }
    .form-grid { display: grid; grid-template-columns: repeat(2, minmax(0,1fr)); gap: 14px; }
    .field { display: flex; flex-direction: column; gap: 6px; margin-bottom: 14px; }
    .field.full { grid-column: 1 / -1; }
    .field label { color: #d7dee5; font-size: 12px; font-weight: 700; }
    .field input, .field textarea, .field select { width: 100%; border: 1px solid #35414d; border-radius: 10px; outline: 0; padding: 11px 12px; background: #0f1317; color: var(--text); }
    .field input:focus, .field textarea:focus, .field select:focus { border-color: var(--blue); box-shadow: 0 0 0 3px rgba(101,169,255,.12); }
    .field textarea { min-height: 104px; resize: vertical; }
    .help { color: var(--muted); font-size: 11px; font-weight: 450; }
    .admin-status { min-height: 22px; margin: 0 0 12px; color: var(--muted); font-size: 13px; }
    .admin-status.error { color: #ff9da4; }
    .admin-status.success { color: #9ce0b1; }
    .admin-toolbar { display: flex; flex-wrap: wrap; justify-content: space-between; gap: 10px; margin-bottom: 20px; }
    .admin-tabs { display: flex; gap: 7px; }
    .admin-tab { border: 1px solid var(--line); border-radius: 9px; padding: 8px 12px; background: transparent; color: var(--muted); cursor: pointer; }
    .admin-tab.active { border-color: #365c84; background: #172536; color: #c8e2ff; }
    .admin-view { display: none; }
    .admin-view.active { display: block; }
    .admin-item { display: flex; align-items: center; justify-content: space-between; gap: 12px; margin-top: 9px; border: 1px solid var(--line); border-radius: 11px; padding: 12px; background: var(--surface); }
    .admin-item-info { min-width: 0; }
    .admin-item-info strong { display: block; overflow: hidden; text-overflow: ellipsis; white-space: nowrap; }
    .admin-item-info small { color: var(--muted); }
    .admin-item-actions { display: flex; flex: 0 0 auto; gap: 6px; }
    .checkline { display: flex; align-items: center; gap: 9px; margin-bottom: 14px; color: var(--muted); font-size: 13px; }
    .checkline input { accent-color: var(--blue-strong); }
    @media (max-width: 900px) {
      .topbar-inner { flex-wrap: wrap; padding: 12px 0; }
      .nav { order: 3; width: 100%; }
      .admin-trigger { margin-left: auto; }
      .card-grid { grid-template-columns: repeat(2, minmax(0,1fr)); }
    }
    @media (max-width: 620px) {
      .wrap { width: min(var(--width), calc(100% - 28px)); }
      .topbar-inner { gap: 10px; }
      .brand-copy { font-size: 14px; }
      .nav-link { padding: 8px 10px; }
      .view { padding: 28px 0 54px; }
      .hero { min-height: 365px; padding: 27px; }
      .hero:after { right: -120px; }
      .intro-grid, .contact-grid, .form-grid { grid-template-columns: 1fr; }
      .field.full { grid-column: auto; }
      .stat-grid { grid-template-columns: 1fr; gap: 10px; }
      .stat-card { min-height: 120px; }
      .card-grid { grid-template-columns: 1fr; }
      .section-heading { align-items: start; flex-direction: column; }
      .footer-inner { flex-direction: column; }
      .admin-item { align-items: start; flex-direction: column; }
      .admin-item-actions { width: 100%; }
    }
    @media (prefers-reduced-motion: reduce) { *, *::before, *::after { scroll-behavior: auto !important; animation-duration: .01ms !important; transition-duration: .01ms !important; } }
  </style>
</head>
<body>
  <header class="topbar">
    <div class="wrap topbar-inner">
      <a class="brand" href="#onas" aria-label="Padew Cubing League — strona główna">
        <span class="brand-mark">PCL</span>
        <span class="brand-copy">Padew Cubing League<small>Padew Narodowa</small></span>
      </a>
      <nav class="nav" aria-label="Główna nawigacja">
        <button class="nav-link" type="button" data-view="onas">O nas</button>
        <button class="nav-link" type="button" data-view="statystyki">Statystyki</button>
        <button class="nav-link" type="button" data-view="aktualnosci">Aktualności</button>
        <button class="nav-link" type="button" data-view="zajecia">Zajęcia</button>
        <button class="nav-link" type="button" data-view="partnerzy">Partnerzy</button>
        <button class="nav-link" type="button" data-view="kontakt">Kontakt</button>
        <a class="nav-link" href="https://www.worldcubeassociation.org/" target="_blank" rel="noopener noreferrer">WCA ↗</a>
      </nav>
      <button class="admin-trigger" id="admin-open" type="button">Panel administratora</button>
    </div>
  </header>

  <main class="wrap">
    <p class="connection-note" id="connection-note" role="status"></p>

    <section class="view" id="view-onas" data-page="onas">
      <div class="hero">
        <div class="hero-content">
          <p class="eyebrow">Padew Cubing League · PCL</p>
          <h1 id="hero-title">Układamy. Uczymy się. Działamy razem.</h1>
          <p class="lead" id="hero-description">Lokalna społeczność miłośników kostki Rubika w Padwi Narodowej.</p>
          <div class="actions">
            <button class="button primary" type="button" data-go="zajecia">Informacje o zajęciach</button>
            <button class="button quiet" type="button" data-go="kontakt">Skontaktuj się</button>
          </div>
        </div>
      </div>
      <div class="intro-grid">
        <article class="panel">
          <p class="eyebrow">O nas</p>
          <h2>Padew Cubing League</h2>
          <p id="about-copy">Informacje o społeczności i jej działalności można uzupełnić w panelu administratora.</p>
        </article>
        <article class="panel">
          <p class="eyebrow">Więcej o układaniu</p>
          <h3>World Cube Association</h3>
          <p>Oficjalne informacje o speedcubingu i zawodach znajdziesz na stronie WCA.</p>
          <a class="card-link" href="https://www.worldcubeassociation.org/" target="_blank" rel="noopener noreferrer">Otwórz worldcubeassociation.org ↗</a>
        </article>
      </div>
    </section>

    <section class="view" id="view-statystyki" data-page="statystyki">
      <div class="section-heading">
        <div><p class="eyebrow">PCL w liczbach</p><h2>Statystyki</h2></div>
        <p>Aktualne wartości możesz zmienić w panelu administratora.</p>
      </div>
      <div class="stat-grid">
        <article class="panel stat-card"><p class="eyebrow">Uczestnicy</p><div class="stat-value" id="stat-students">9</div><div class="stat-label">uczniów</div></article>
        <article class="panel stat-card"><p class="eyebrow">Zajęcia</p><div class="stat-value" id="stat-groups">1</div><div class="stat-label">grupa</div></article>
        <article class="panel stat-card"><p class="eyebrow">Lokalizacja</p><div class="stat-value" id="stat-location">Padew</div><div class="stat-label" id="stat-location-label">Padew Narodowa</div></article>
      </div>
    </section>

    <section class="view" id="view-aktualnosci" data-page="aktualnosci">
      <div class="section-heading">
        <div><p class="eyebrow">Co u nas słychać</p><h2>Aktualności</h2></div>
        <p>Wiadomości i ogłoszenia dodaje administrator.</p>
      </div>
      <div class="card-grid" id="news-list"></div>
    </section>

    <section class="view" id="view-zajecia" data-page="zajecia">
      <div class="section-heading">
        <div><p class="eyebrow">Spotkania PCL</p><h2>Zajęcia</h2></div>
        <p id="classes-intro">Informacje o terminach i organizacji zajęć można uzupełnić w panelu administratora.</p>
      </div>
      <div class="card-grid" id="classes-list"></div>
    </section>

    <section class="view" id="view-partnerzy" data-page="partnerzy">
      <div class="section-heading">
        <div><p class="eyebrow">Współpraca</p><h2>Partnerzy</h2></div>
        <p>Lista jest uzupełniana po potwierdzeniu współpracy.</p>
      </div>
      <div class="card-grid" id="partners-list"></div>
    </section>

    <section class="view" id="view-kontakt" data-page="kontakt">
      <div class="section-heading">
        <div><p class="eyebrow">Napisz do nas</p><h2>Kontakt</h2></div>
        <p id="contact-intro">Wybierz dostępny sposób kontaktu. Dane można uzupełnić w panelu administratora.</p>
      </div>
      <div class="contact-grid" id="contact-list"></div>
      <p class="note">Nie podano jeszcze publicznych danych kontaktowych.</p>
    </section>
  </main>

  <footer class="footer">
    <div class="wrap footer-inner"><span>© <span id="year"></span> Padew Cubing League</span><span>PCL · Padew Narodowa</span></div>
  </footer>

  <dialog id="admin-dialog" aria-labelledby="admin-heading">
    <div class="dialog-head">
      <h2 id="admin-heading">Panel administratora</h2>
      <button class="close-button" id="admin-close" type="button" aria-label="Zamknij">×</button>
    </div>
    <div class="dialog-body">
      <p class="admin-status" id="admin-status" role="status"></p>
      <form id="login-form">
        <p>Zaloguj się kontem administratora. Konta dodaje się w Supabase; nie ma publicznej rejestracji.</p>
        <div class="field"><label for="login-email">Adres e-mail</label><input id="login-email" name="email" type="email" autocomplete="username" required></div>
        <div class="field"><label for="login-password">Hasło</label><input id="login-password" name="password" type="password" autocomplete="current-password" required></div>
        <button class="button primary" type="submit">Zaloguj się</button>
      </form>
      <div id="admin-editor" hidden>
        <div class="admin-toolbar">
          <div class="admin-tabs">
            <button class="admin-tab active" data-admin-view="settings" type="button">Dane i kontakt</button>
            <button class="admin-tab" data-admin-view="items" type="button">Treści strony</button>
          </div>
          <button class="button small quiet" id="logout-button" type="button">Wyloguj</button>
        </div>

        <section class="admin-view active" id="admin-view-settings">
          <form id="settings-form">
            <div class="form-grid">
              <div class="field full"><label for="setting-title">Nagłówek strony</label><input id="setting-title" name="title" maxlength="100" required></div>
              <div class="field full"><label for="setting-description">Krótki opis na stronie głównej</label><textarea id="setting-description" name="description" maxlength="500"></textarea></div>
              <div class="field full"><label for="setting-about">Opis „O nas”</label><textarea id="setting-about" name="about" maxlength="2000"></textarea></div>
              <div class="field"><label for="setting-students">Liczba uczniów</label><input id="setting-students" name="students" type="number" min="0" max="9999"></div>
              <div class="field"><label for="setting-groups">Liczba grup</label><input id="setting-groups" name="groups" type="number" min="0" max="999"></div>
              <div class="field full"><label for="setting-location">Lokalizacja</label><input id="setting-location" name="location" maxlength="120"></div>
              <div class="field full"><label for="setting-classes-intro">Wstęp do sekcji „Zajęcia”</label><textarea id="setting-classes-intro" name="classesIntro" maxlength="500"></textarea></div>
              <div class="field full"><label for="setting-contact-intro">Wstęp do sekcji „Kontakt”</label><textarea id="setting-contact-intro" name="contactIntro" maxlength="500"></textarea></div>
              <div class="field"><label for="setting-email">Publiczny e-mail <span class="help">(opcjonalnie)</span></label><input id="setting-email" name="email" type="email" maxlength="200"></div>
              <div class="field"><label for="setting-phone">Publiczny telefon <span class="help">(opcjonalnie)</span></label><input id="setting-phone" name="phone" type="tel" maxlength="50"></div>
            </div>
            <button class="button primary" type="submit">Zapisz dane</button>
          </form>
        </section>

        <section class="admin-view" id="admin-view-items">
          <div class="field">
            <label for="item-category">Wybierz sekcję</label>
            <select id="item-category">
              <option value="news">Aktualności</option>
              <option value="classes">Zajęcia</option>
              <option value="partners">Partnerzy</option>
            </select>
          </div>
          <form id="item-form">
            <input type="hidden" name="id" id="item-id">
            <div class="form-grid">
              <div class="field full"><label for="item-title">Tytuł</label><input id="item-title" name="title" maxlength="150" required></div>
              <div class="field full"><label for="item-body">Treść</label><textarea id="item-body" name="body" maxlength="3000"></textarea></div>
              <div class="field"><label for="item-details">Dodatkowa informacja <span class="help">(np. data albo miejsce)</span></label><input id="item-details" name="details" maxlength="200"></div>
              <div class="field"><label for="item-url">Link <span class="help">(opcjonalnie, https://...)</span></label><input id="item-url" name="url" type="url" maxlength="500"></div>
            </div>
            <label class="checkline"><input id="item-published" name="published" type="checkbox" checked> Pokaż wpis na stronie</label>
            <div class="actions" style="margin-top:0">
              <button class="button primary" type="submit" id="item-save">Dodaj wpis</button>
              <button class="button quiet" type="button" id="item-cancel" hidden>Anuluj edycję</button>
            </div>
          </form>
          <div style="height:1px;background:var(--line);margin:22px 0"></div>
          <h3>Wpisy w tej sekcji</h3>
          <div id="admin-item-list"></div>
        </section>
      </div>
    </div>
  </dialog>

  <script type="module">
    // Public project settings can be placed here. Never put a service_role or secret key in this file.
    const SUPABASE_URL = "";
    const SUPABASE_PUBLISHABLE_KEY = "";

    const DEFAULT_SETTINGS = {
      title: "Układamy. Uczymy się. Działamy razem.",
      description: "Lokalna społeczność miłośników kostki Rubika w Padwi Narodowej.",
      about: "Informacje o społeczności i jej działalności można uzupełnić w panelu administratora.",
      students: 9,
      groups: 1,
      location: "Padew Narodowa",
      classesIntro: "Informacje o terminach i organizacji zajęć można uzupełnić w panelu administratora.",
      contactIntro: "Wybierz dostępny sposób kontaktu. Dane można uzupełnić w panelu administratora.",
      email: "",
      phone: ""
    };

    const state = { settings: Object.assign({}, DEFAULT_SETTINGS), items: [], client: null, adminId: null };
    const $ = (selector, root) => (root || document).querySelector(selector);
    const $$ = (selector, root) => Array.from((root || document).querySelectorAll(selector));
    const hasSupabaseConfig = Boolean(SUPABASE_URL.trim() && SUPABASE_PUBLISHABLE_KEY.trim());

    function setStatus(message, type) {
      const node = $("#admin-status");
      node.textContent = message || "";
      node.className = "admin-status" + (type ? " " + type : "");
    }

    function setConnectionNote(message) {
      const node = $("#connection-note");
      node.textContent = message || "";
      node.classList.toggle("show", Boolean(message));
    }

    function safeText(value) {
      return value === null || value === undefined ? "" : String(value);
    }

    function safeExternalUrl(value) {
      try {
        const parsed = new URL(String(value || ""));
        return parsed.protocol === "https:" || parsed.protocol === "http:" ? parsed.href : "";
      } catch (error) {
        return "";
      }
    }

    function setView(viewName, updateHash) {
      const known = ["onas", "statystyki", "aktualnosci", "zajecia", "partnerzy", "kontakt"];
      const chosen = known.includes(viewName) ? viewName : "onas";
      $$(".view").forEach((view) => view.classList.toggle("active", view.dataset.page === chosen));
      $$(".nav-link[data-view]").forEach((link) => {
        if (link.dataset.view === chosen) link.setAttribute("aria-current", "page");
        else link.removeAttribute("aria-current");
      });
      if (updateHash !== false && window.location.hash !== "#" + chosen) history.pushState(null, "", "#" + chosen);
      window.scrollTo({ top: 0, behavior: "smooth" });
    }

    function makeEmpty(message) {
      const node = document.createElement("div");
      node.className = "empty";
      node.textContent = message;
      return node;
    }

    function renderCards(category, targetId, emptyText) {
      const target = $("#" + targetId);
      target.replaceChildren();
      const rows = state.items.filter((item) => item.category === category && item.published !== false);
      if (!rows.length) {
        target.append(makeEmpty(emptyText));
        return;
      }
      rows.forEach((item) => {
        const card = document.createElement("article");
        card.className = "card";
        if (item.details) {
          const meta = document.createElement("p");
          meta.className = "card-meta";
          meta.textContent = safeText(item.details);
          card.append(meta);
        }
        const title = document.createElement("h3");
        title.textContent = safeText(item.title);
        card.append(title);
        if (item.body) {
          const body = document.createElement("p");
          body.textContent = safeText(item.body);
          card.append(body);
        }
        const externalUrl = safeExternalUrl(item.url);
        if (externalUrl) {
          const link = document.createElement("a");
          link.className = "card-link";
          link.href = externalUrl;
          link.target = "_blank";
          link.rel = "noopener noreferrer";
          link.textContent = "Więcej ↗";
          card.append(link);
        }
        target.append(card);
      });
    }

    function renderContact() {
      const target = $("#contact-list");
      target.replaceChildren();
      const pairs = [
        { label: "E-mail", value: state.settings.email, href: state.settings.email ? "mailto:" + state.settings.email : "" },
        { label: "Telefon", value: state.settings.phone, href: state.settings.phone ? "tel:" + state.settings.phone.replace(/[^\d+]/g, "") : "" },
        { label: "Lokalizacja", value: state.settings.location, href: "" }
      ];
      let visible = 0;
      pairs.forEach((pair) => {
        if (!pair.value) return;
        visible += 1;
        const row = document.createElement("div");
        row.className = "contact-row";
        const label = document.createElement("small");
        label.textContent = pair.label;
        row.append(label);
        if (pair.href) {
          const link = document.createElement("a");
          link.href = pair.href;
          link.textContent = pair.value;
          row.append(link);
        } else {
          const value = document.createElement("strong");
          value.textContent = pair.value;
          row.append(value);
        }
        target.append(row);
      });
      $(".note", $("#view-kontakt")).hidden = visible > 0;
    }

    function render() {
      $("#hero-title").textContent = safeText(state.settings.title || DEFAULT_SETTINGS.title);
      $("#hero-description").textContent = safeText(state.settings.description || "");
      $("#about-copy").textContent = safeText(state.settings.about || "");
      $("#stat-students").textContent = safeText(state.settings.students);
      $("#stat-groups").textContent = safeText(state.settings.groups);
      const location = safeText(state.settings.location || "—");
      $("#stat-location").textContent = location.length > 18 ? location.slice(0, 17) + "…" : location;
      $("#stat-location-label").textContent = location;
      $("#classes-intro").textContent = safeText(state.settings.classesIntro || "");
      $("#contact-intro").textContent = safeText(state.settings.contactIntro || "");
      renderCards("news", "news-list", "Nie ma jeszcze aktualności. Wróć tu później.");
      renderCards("classes", "classes-list", "Informacje o zajęciach pojawią się tutaj po ich dodaniu.");
      renderCards("partners", "partners-list", "Lista partnerów zostanie uzupełniona po potwierdzeniu współpracy.");
      renderContact();
    }

    async function loadPublicContent() {
      if (!hasSupabaseConfig) {
        setConnectionNote("Wspólne edytowanie treści w panelu administratora wymaga podłączenia projektu Supabase. Strona pokazuje dane początkowe zapisane w pliku.");
        render();
        return;
      }
      try {
        const supabaseModule = await import("https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2/+esm");
        const createClient = supabaseModule.createClient;
        state.client = createClient(SUPABASE_URL, SUPABASE_PUBLISHABLE_KEY);
        const settingsResult = await state.client.from("pcl_settings").select("data").eq("id", "main").maybeSingle();
        if (settingsResult.error) throw settingsResult.error;
        if (settingsResult.data && settingsResult.data.data) state.settings = Object.assign({}, DEFAULT_SETTINGS, settingsResult.data.data);
        const itemsResult = await state.client.from("pcl_items").select("id,category,title,body,details,url,sort_order,published,created_at").order("sort_order", { ascending: true }).order("created_at", { ascending: false });
        if (itemsResult.error) throw itemsResult.error;
        state.items = itemsResult.data || [];
        setConnectionNote("");
      } catch (error) {
        console.error(error);
        setConnectionNote("Nie udało się pobrać wspólnych danych. Sprawdź konfigurację Supabase i zasady dostępu opisane w instrukcji.");
      }
      render();
    }

    function populateSettingsForm() {
      const form = $("#settings-form");
      Object.keys(DEFAULT_SETTINGS).forEach((key) => {
        if (form.elements[key]) form.elements[key].value = state.settings[key] === null || state.settings[key] === undefined ? "" : state.settings[key];
      });
    }

    function readSettingsForm() {
      const form = $("#settings-form");
      return {
        title: form.elements.title.value.trim(),
        description: form.elements.description.value.trim(),
        about: form.elements.about.value.trim(),
        students: Number(form.elements.students.value || 0),
        groups: Number(form.elements.groups.value || 0),
        location: form.elements.location.value.trim(),
        classesIntro: form.elements.classesIntro.value.trim(),
        contactIntro: form.elements.contactIntro.value.trim(),
        email: form.elements.email.value.trim(),
        phone: form.elements.phone.value.trim()
      };
    }

    async function checkAdministrator() {
      const sessionResult = await state.client.auth.getSession();
      if (sessionResult.error) throw sessionResult.error;
      const session = sessionResult.data.session;
      if (!session) {
        showLogin();
        setStatus("Zaloguj się kontem administratora.");
        return false;
      }
      const userId = session.user.id;
      const adminResult = await state.client.from("pcl_admins").select("user_id").eq("user_id", userId).maybeSingle();
      if (adminResult.error) throw adminResult.error;
      if (!adminResult.data) {
        await state.client.auth.signOut();
        state.adminId = null;
        showLogin();
        setStatus("To konto nie ma uprawnień administratora. Poproś o dodanie go do listy administratorów w Supabase.", "error");
        return false;
      }
      state.adminId = userId;
      $("#login-form").hidden = true;
      $("#admin-editor").hidden = false;
      setStatus("Zalogowano. Zmiany zapisują się we wspólnej bazie.", "success");
      populateSettingsForm();
      await loadAdminItems();
      return true;
    }

    function showLogin() {
      $("#login-form").hidden = false;
      $("#admin-editor").hidden = true;
    }

    async function openAdmin() {
      if (!hasSupabaseConfig) {
        setConnectionNote("Aby używać panelu administratora, wpisz w kodzie adres projektu Supabase i jego klucz publishable, a następnie skonfiguruj bazę według instrukcji TXT.");
        return;
      }
      $("#admin-dialog").showModal();
      setStatus("Sprawdzam dostęp…");
      showLogin();
      try {
        await checkAdministrator();
      } catch (error) {
        console.error(error);
        setStatus("Nie udało się sprawdzić konta. Sprawdź połączenie i ustawienia Supabase.", "error");
      }
    }

    async function loadAdminItems() {
      const result = await state.client.from("pcl_items").select("id,category,title,body,details,url,published,sort_order,created_at").order("sort_order", { ascending: true }).order("created_at", { ascending: false });
      if (result.error) throw result.error;
      state.items = result.data || [];
      render();
      renderAdminItemList();
    }

    function renderAdminItemList() {
      const target = $("#admin-item-list");
      target.replaceChildren();
      const category = $("#item-category").value;
      const rows = state.items.filter((item) => item.category === category);
      if (!rows.length) {
        target.append(makeEmpty("Brak wpisów w tej sekcji. Formularz powyżej pozwala dodać pierwszy."));
        return;
      }
      rows.forEach((item) => {
        const row = document.createElement("div");
        row.className = "admin-item";
        const info = document.createElement("div");
        info.className = "admin-item-info";
        const title = document.createElement("strong");
        title.textContent = safeText(item.title || "(bez tytułu)");
        const meta = document.createElement("small");
        meta.textContent = (item.published ? "Widoczny" : "Ukryty") + (item.details ? " · " + item.details : "");
        info.append(title, meta);
        const actions = document.createElement("div");
        actions.className = "admin-item-actions";
        const edit = document.createElement("button");
        edit.type = "button";
        edit.className = "button small";
        edit.textContent = "Edytuj";
        edit.addEventListener("click", () => editItem(item));
        const remove = document.createElement("button");
        remove.type = "button";
        remove.className = "button small danger";
        remove.textContent = "Usuń";
        remove.addEventListener("click", () => deleteItem(item));
        actions.append(edit, remove);
        row.append(info, actions);
        target.append(row);
      });
    }

    function editItem(item) {
      const form = $("#item-form");
      form.elements.id.value = item.id;
      form.elements.title.value = item.title || "";
      form.elements.body.value = item.body || "";
      form.elements.details.value = item.details || "";
      form.elements.url.value = item.url || "";
      form.elements.published.checked = item.published !== false;
      $("#item-save").textContent = "Zapisz zmiany";
      $("#item-cancel").hidden = false;
      form.elements.title.focus();
    }

    function clearItemForm() {
      $("#item-form").reset();
      $("#item-id").value = "";
      $("#item-published").checked = true;
      $("#item-save").textContent = "Dodaj wpis";
      $("#item-cancel").hidden = true;
    }

    async function deleteItem(item) {
      if (!window.confirm("Usunąć wpis „" + safeText(item.title) + "”?")) return;
      const result = await state.client.from("pcl_items").delete().eq("id", item.id);
      if (result.error) {
        setStatus("Nie udało się usunąć wpisu. Sprawdź uprawnienia Supabase.", "error");
        return;
      }
      setStatus("Wpis został usunięty.", "success");
      await loadAdminItems();
    }

    $$(".nav-link[data-view]").forEach((link) => link.addEventListener("click", () => setView(link.dataset.view, true)));
    $$("[data-go]").forEach((button) => button.addEventListener("click", () => setView(button.dataset.go, true)));
    window.addEventListener("hashchange", () => setView(window.location.hash.slice(1), false));
    $("#year").textContent = String(new Date().getFullYear());
    setView(window.location.hash.slice(1), false);

    $("#admin-open").addEventListener("click", openAdmin);
    $("#admin-close").addEventListener("click", () => $("#admin-dialog").close());
    $("#admin-dialog").addEventListener("click", (event) => {
      if (event.target === $("#admin-dialog")) $("#admin-dialog").close();
    });

    $("#login-form").addEventListener("submit", async (event) => {
      event.preventDefault();
      setStatus("Logowanie…");
      const email = $("#login-email").value.trim();
      const password = $("#login-password").value;
      try {
        const result = await state.client.auth.signInWithPassword({ email: email, password: password });
        if (result.error) {
          setStatus("Nie udało się zalogować. Sprawdź e-mail i hasło.", "error");
          return;
        }
        const authorized = await checkAdministrator();
        if (!authorized) return;
      } catch (error) {
        console.error(error);
        setStatus("Logowanie powiodło się, ale nie udało się sprawdzić uprawnień. Sprawdź tabelę administratorów.", "error");
      }
    });

    $("#logout-button").addEventListener("click", async () => {
      await state.client.auth.signOut();
      state.adminId = null;
      showLogin();
      setStatus("Wylogowano.", "success");
    });

    $$(".admin-tab").forEach((button) => button.addEventListener("click", () => {
      $$(".admin-tab").forEach((tab) => tab.classList.toggle("active", tab === button));
      $$(".admin-view").forEach((view) => view.classList.toggle("active", view.id === "admin-view-" + button.dataset.adminView));
    }));

    $("#settings-form").addEventListener("submit", async (event) => {
      event.preventDefault();
      const data = readSettingsForm();
      setStatus("Zapisuję dane…");
      const result = await state.client.from("pcl_settings").upsert({ id: "main", data: data }, { onConflict: "id" });
      if (result.error) {
        console.error(result.error);
        setStatus("Nie udało się zapisać. Sprawdź, czy konto ma uprawnienia administratora i czy uruchomiono SQL z instrukcji.", "error");
        return;
      }
      state.settings = Object.assign({}, DEFAULT_SETTINGS, data);
      render();
      setStatus("Zapisano. Zmiany są widoczne dla wszystkich odwiedzających stronę.", "success");
    });

    $("#item-category").addEventListener("change", () => {
      clearItemForm();
      renderAdminItemList();
    });
    $("#item-cancel").addEventListener("click", clearItemForm);
    $("#item-form").addEventListener("submit", async (event) => {
      event.preventDefault();
      const form = event.currentTarget;
      const record = {
        category: $("#item-category").value,
        title: form.elements.title.value.trim(),
        body: form.elements.body.value.trim(),
        details: form.elements.details.value.trim(),
        url: safeExternalUrl(form.elements.url.value.trim()) || null,
        published: form.elements.published.checked
      };
      if (form.elements.url.value.trim() && !record.url) {
        setStatus("Link musi zaczynać się od http:// lub https://.", "error");
        return;
      }
      const id = form.elements.id.value;
      setStatus("Zapisuję wpis…");
      const result = id
        ? await state.client.from("pcl_items").update(record).eq("id", id)
        : await state.client.from("pcl_items").insert(record);
      if (result.error) {
        console.error(result.error);
        setStatus("Nie udało się zapisać wpisu. Sprawdź uprawnienia Supabase.", "error");
        return;
      }
      clearItemForm();
      setStatus("Wpis został zapisany.", "success");
      await loadAdminItems();
    });

    async function start() {
      render();
      if (hasSupabaseConfig) await loadPublicContent();
    }
    start();
  </script>
</body>
</html>
