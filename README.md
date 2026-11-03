<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Old Fairway Club</title>
  <meta name="description" content="Golf clothing from a club that never existed. Reserve the first drop from Old Fairway Club.">
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Federo&family=Reenie+Beanie&family=Spectral:wght@400;600&display=swap" rel="stylesheet">

  <style>
    :root {
      --pine: #0f3d2e;
      --deep: #092a20;
      --butter: #f3dc7b;
      --sage: #dde7d3;
      --oxblood: #7a2230;
      --ink: #13261e;
      --display: "Federo", Georgia, serif;
      --body: "Spectral", Georgia, serif;
      --pencil: "Reenie Beanie", "Comic Sans MS", cursive;
    }

    *, *::before, *::after { box-sizing: border-box; }

    html { scroll-behavior: smooth; }

    body {
      margin: 0;
      background: var(--pine);
      color: var(--sage);
      font-family: var(--body);
      font-size: 1.125rem;
      line-height: 1.6;
    }

    h1, h2, h3, p { margin: 0; }

    h1, h2, h3 {
      font-family: var(--display);
      font-weight: 400;
      line-height: 1.05;
    }

    a { color: inherit; }

    :focus-visible {
      outline: 3px solid var(--oxblood);
      outline-offset: 3px;
    }

    .hero :focus-visible,
    .story :focus-visible,
    footer :focus-visible {
      outline-color: var(--butter);
    }

    .wrap {
      width: min(1120px, 100%);
      margin: 0 auto;
      padding: 0 24px;
    }

    /* Hero */
    .hero {
      min-height: 100svh;
      display: flex;
      align-items: center;
      padding: 48px 0;
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1.35fr 1fr;
      align-items: center;
      gap: 40px;
    }

    .hero h1 {
      color: var(--butter);
      font-size: clamp(4rem, 12vw, 9.5rem);
      line-height: .92;
    }

    .hero h1 span { display: block; }

    .hero p {
      max-width: 30ch;
      margin-top: 28px;
      font-size: clamp(1.25rem, 2.4vw, 1.6rem);
      line-height: 1.35;
    }

    .button {
      display: inline-block;
      margin-top: 32px;
      padding: 14px 24px;
      border: 2px solid var(--butter);
      background: var(--butter);
      color: var(--ink);
      font-family: var(--display);
      font-size: 1.15rem;
      text-decoration: none;
      cursor: pointer;
    }

    .button:hover {
      background: transparent;
      color: var(--butter);
    }

    .crest {
      display: block;
      width: 100%;
      max-width: 400px;
      margin-left: auto;
      animation: settle 900ms cubic-bezier(.2, .8, .2, 1) both;
    }

    @keyframes settle {
      from { opacity: 0; transform: rotate(-14deg) scale(.9); }
      to { opacity: 1; transform: rotate(0) scale(1); }
    }

    /* Scorecard */
    .card-section {
      background: var(--sage);
      color: var(--ink);
      padding: 80px 0;
    }

    .card-section h2 {
      font-size: clamp(2.5rem, 6vw, 4.25rem);
      color: var(--pine);
    }

    .intro {
      max-width: 54ch;
      margin-top: 14px;
    }

    .scorecard {
      margin: 36px 0 0;
      padding: 0;
      list-style: none;
      border: 3px solid var(--pine);
    }

    .row {
      display: grid;
      grid-template-columns: 72px 130px minmax(0, 1fr) 90px 110px 170px;
      align-items: stretch;
      border-top: 1px solid var(--pine);
    }

    .row:first-child { border-top: 0; }

    .row > * {
      display: flex;
      align-items: center;
      min-width: 0;
      padding: 12px 14px;
      border-left: 1px solid var(--pine);
    }

    .row > *:first-child { border-left: 0; }

    .head {
      background: var(--pine);
      color: var(--butter);
      font-family: var(--display);
    }

    .hole {
      justify-content: center;
      font-family: var(--display);
      font-size: 2rem;
      color: var(--oxblood);
    }

    .picture svg {
      display: block;
      width: 100%;
      height: auto;
    }

    .piece {
      flex-direction: column;
      align-items: flex-start !important;
      justify-content: center;
    }

    .piece h3 { font-size: 1.5rem; }

    .piece p {
      font-size: 1rem;
      line-height: 1.4;
      margin-top: 4px;
    }

    select {
      width: 100%;
      padding: 7px 4px;
      border: 1px solid var(--pine);
      border-radius: 0;
      background: transparent;
      color: var(--ink);
      font: inherit;
    }

    .one-size { font-size: 1rem; }

    .mark {
      justify-content: space-between;
      gap: 6px;
    }

    .stepper {
      flex: none;
      width: 42px;
      height: 42px;
      border: 1px solid var(--pine);
      background: transparent;
      color: var(--pine);
      font-family: var(--display);
      font-size: 1.4rem;
      line-height: 1;
      cursor: pointer;
    }

    .stepper:hover {
      background: var(--pine);
      color: var(--butter);
    }

    .count {
      min-width: 2ch;
      color: var(--oxblood);
      font-family: var(--pencil);
      font-size: 2.6rem;
      line-height: 1;
      text-align: center;
    }

    .count.bump { animation: bump 180ms ease-out; }

    @keyframes bump {
      from { transform: rotate(-8deg) scale(1.4); }
      to { transform: none; }
    }

    .total-row {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 16px;
      padding: 14px;
      border-top: 3px solid var(--pine);
      font-family: var(--display);
      font-size: 1.4rem;
    }

    .total {
      color: var(--oxblood);
      font-family: var(--pencil);
      font-size: 2.8rem;
      line-height: 1;
    }

    /* Reservation form */
    form {
      display: grid;
      grid-template-columns: 1fr 1fr auto;
      align-items: end;
      gap: 16px;
      margin-top: 36px;
    }

    label {
      display: block;
      font-family: var(--display);
      font-size: 1.05rem;
    }

    input {
      display: block;
      width: 100%;
      margin-top: 6px;
      padding: 12px;
      border: 2px solid var(--pine);
      border-radius: 0;
      background: #fff;
      color: var(--ink);
      font: inherit;
    }

    form .button {
      margin: 0;
      border-color: var(--pine);
      background: var(--pine);
      color: var(--butter);
    }

    form .button:hover {
      background: transparent;
      color: var(--pine);
    }

    .form-note {
      margin-top: 14px;
      font-size: 1rem;
    }

    .status {
      min-height: 1.6em;
      margin-top: 8px;
      color: var(--oxblood);
      font-weight: 600;
    }

    /* Story */
    .story { padding: 88px 0; }

    .story-grid {
      display: grid;
      grid-template-columns: 1fr 1.2fr;
      gap: 48px;
    }

    .story h2 {
      color: var(--butter);
      font-size: clamp(2.5rem, 6vw, 4.25rem);
    }

    .story p {
      max-width: 58ch;
      margin-bottom: 18px;
    }

    /* Footer */
    footer {
      background: var(--deep);
      padding: 32px 0;
      font-size: 1rem;
    }

    @media (max-width: 860px) {
      .hero-grid,
      .story-grid {
        grid-template-columns: 1fr;
      }

      .crest {
        grid-row: 1;
        width: 190px;
        margin: 0;
      }

      .hero { min-height: auto; }

      .head { display: none; }

      .scorecard { border-width: 2px; }

      .row {
        grid-template-columns: 64px minmax(0, 1fr) 96px;
        border-top: 3px solid var(--pine);
      }

      .row:nth-child(2) { border-top: 0; }

      .row > * { border-left: 0; padding: 10px 12px; }

      .hole { grid-column: 1; grid-row: 1; }
      .piece { grid-column: 2; grid-row: 1; }
      .picture { grid-column: 3; grid-row: 1; padding: 8px; }

      .price, .size, .mark {
        grid-column: 1 / -1;
        justify-content: space-between;
        border-top: 1px solid var(--pine);
      }

      .price::before { content: "Price"; font-family: var(--display); }
      .size::before { content: "Size"; font-family: var(--display); margin-right: 16px; }
      .size select { width: 130px; }

      form { grid-template-columns: 1fr; }

      form .button { width: 100%; }
    }

    @media (prefers-reduced-motion: reduce) {
      html { scroll-behavior: auto; }

      .crest, .count.bump { animation: none; }
    }
  </style>
</head>

<body>
  <!-- Reusable crest. Edit the words or colors here and they update everywhere. -->
  <svg width="0" height="0" style="position:absolute" aria-hidden="true">
    <symbol id="mini-crest" viewBox="0 0 40 46">
      <path d="M3 3h34v22c0 10-8 15-17 19C11 40 3 35 3 25z" fill="#f3dc7b"/>
      <path d="M14 34 26 10M26 34 14 10" stroke="#0f3d2e" stroke-width="3"/>
    </symbol>
  </svg>

  <main>
    <section class="hero">
      <div class="wrap hero-grid">
        <div>
          <h1><span>Old</span> <span>Fairway</span> <span>Club</span></h1>
          <p>A golf club that never existed. The clothes are real.</p>
          <a class="button" href="#first-drop">Mark your card</a>
        </div>

        <svg class="crest" viewBox="0 0 400 400" role="img" aria-label="Old Fairway Club crest with crossed golf clubs and the year 1926">
          <defs>
            <path id="ring-top" d="M64 200a136 136 0 0 1 272 0"/>
            <path id="ring-bottom" d="M44 200a156 156 0 0 0 312 0"/>
          </defs>
          <circle cx="200" cy="200" r="194" fill="#f3dc7b"/>
          <circle cx="200" cy="200" r="182" fill="none" stroke="#0f3d2e" stroke-width="3"/>
          <circle cx="200" cy="200" r="122" fill="#0f3d2e"/>
          <text font-family="Federo, Georgia, serif" font-size="39" fill="#0f3d2e" letter-spacing="4">
            <textPath href="#ring-top" startOffset="50%" text-anchor="middle">OLD FAIRWAY CLUB</textPath>
          </text>
          <text font-family="Federo, Georgia, serif" font-size="30" fill="#7a2230" letter-spacing="6">
            <textPath href="#ring-bottom" startOffset="50%" text-anchor="middle">FOUNDED IN FICTION</textPath>
          </text>
          <g stroke="#f3dc7b" stroke-width="9" stroke-linecap="round" fill="none">
            <path d="M138 128 248 268q6 10 22 2"/>
            <path d="M262 128 152 268q-6 10-22 2"/>
          </g>
          <circle cx="200" cy="130" r="17" fill="#dde7d3"/>
          <text x="200" y="311" font-family="Federo, Georgia, serif" font-size="27" fill="#f3dc7b" text-anchor="middle" letter-spacing="3">1926</text>
        </svg>
      </div>
    </section>

    <section class="card-section" id="first-drop">
      <div class="wrap">
        <h2>The first drop</h2>
        <p class="intro">Three pieces, made in small numbers. Mark what you want on the card and reserve it. You won't pay anything yet.</p>

        <ul class="scorecard">
          <li class="row head" aria-hidden="true">
            <span>Hole</span><span>Piece</span><span></span><span>Price</span><span>Size</span><span>Your mark</span>
          </li>

          <li class="row" data-name="The Crest Cap" data-price="38">
            <span class="hole" aria-hidden="true">1</span>
            <span class="picture">
              <svg viewBox="0 0 120 90" aria-hidden="true">
                <path d="M22 62c0-30 16-46 38-46s36 18 36 46z" fill="#0f3d2e"/>
                <path d="M20 62h82c8 0 14 4 15 10-24-4-68-4-97-2z" fill="#092a20"/>
                <use href="#mini-crest" x="46" y="28" width="22" height="25"/>
              </svg>
            </span>
            <div class="piece">
              <h3>The Crest Cap</h3>
              <p>Six-panel cotton cap with an embroidered crest.</p>
            </div>
            <span class="price">$38</span>
            <span class="size"><span class="one-size">One size</span></span>
            <div class="mark" role="group" aria-label="Quantity of The Crest Cap">
              <button class="stepper" type="button" data-step="-1" aria-label="Remove one Crest Cap">&minus;</button>
              <span class="count" aria-live="polite">&ndash;</span>
              <button class="stepper" type="button" data-step="1" aria-label="Add one Crest Cap">+</button>
            </div>
          </li>

          <li class="row" data-name="The Clubhouse Crewneck" data-price="68">
            <span class="hole" aria-hidden="true">2</span>
            <span class="picture">
              <svg viewBox="0 0 120 100" aria-hidden="true">
                <path d="M40 10 14 24 4 66l17 4 7-24v48h64V46l7 24 17-4-10-42-26-14c-6 8-34 8-40 0z" fill="#7a2230"/>
                <path d="M40 10c6 10 34 10 40 0" fill="none" stroke="#f3dc7b" stroke-width="3"/>
                <use href="#mini-crest" x="49" y="32" width="22" height="25"/>
              </svg>
            </span>
            <div class="piece">
              <h3>The Clubhouse Crewneck</h3>
              <p>Heavyweight fleece with a faded club crest.</p>
            </div>
            <span class="price">$68</span>
            <span class="size">
              <select aria-label="Size for The Clubhouse Crewneck">
                <option>S</option><option selected>M</option><option>L</option><option>XL</option><option>XXL</option>
              </select>
            </span>
            <div class="mark" role="group" aria-label="Quantity of The Clubhouse Crewneck">
              <button class="stepper" type="button" data-step="-1" aria-label="Remove one Clubhouse Crewneck">&minus;</button>
              <span class="count" aria-live="polite">&ndash;</span>
              <button class="stepper" type="button" data-step="1" aria-label="Add one Clubhouse Crewneck">+</button>
            </div>
          </li>

          <li class="row" data-name="The Members' Polo" data-price="58">
            <span class="hole" aria-hidden="true">3</span>
            <span class="picture">
              <svg viewBox="0 0 120 100" aria-hidden="true">
                <path d="M42 10 16 22 4 56l17 6 7-16v48h64V46l7 16 17-6-12-34L78 10l-18 12z" fill="#f3dc7b" stroke="#0f3d2e" stroke-width="2"/>
                <path d="M42 10l18 12-10 12zM78 10 60 22l10 12z" fill="#0f3d2e"/>
                <path d="M60 22v26" stroke="#0f3d2e" stroke-width="2"/>
                <circle cx="82" cy="44" r="5" fill="#7a2230"/>
              </svg>
            </span>
            <div class="piece">
              <h3>The Members' Polo</h3>
              <p>Soft cotton piqu&eacute; with an embroidered chest crest.</p>
            </div>
            <span class="price">$58</span>
            <span class="size">
              <select aria-label="Size for The Members' Polo">
                <option>S</option><option selected>M</option><option>L</option><option>XL</option><option>XXL</option>
              </select>
            </span>
            <div class="mark" role="group" aria-label="Quantity of The Members' Polo">
              <button class="stepper" type="button" data-step="-1" aria-label="Remove one Members' Polo">&minus;</button>
              <span class="count" aria-live="polite">&ndash;</span>
              <button class="stepper" type="button" data-step="1" aria-label="Add one Members' Polo">+</button>
            </div>
          </li>

          <li class="total-row">
            <span>Card total</span>
            <span class="total" id="total" aria-live="polite">$0</span>
          </li>
        </ul>

        <form id="reserve" novalidate>
          <label>Your name
            <input type="text" name="name" autocomplete="name" required>
          </label>
          <label>Your email
            <input type="email" name="email" autocomplete="email" required>
          </label>
          <button class="button" type="submit">Reserve my card</button>
        </form>
        <p class="form-note">This opens your email app with your card filled in. Send that email to finish reserving.</p>
        <p class="status" id="status" role="alert"></p>
      </div>
    </section>

    <section class="story">
      <div class="wrap story-grid">
        <h2>The club we made up</h2>
        <div>
          <p>Picture a private course that opened in 1926, with a crooked clubhouse, a strict dress code and members who took their Sunday rounds far too seriously.</p>
          <p>None of it is real. We invented Old Fairway Club so we could make the clothes it would have sold in its pro shop: old-fashioned golf style you can wear on the course or anywhere else.</p>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="wrap">
      <p>&copy; 2026 Old Fairway Club. We're a clothing brand. The club and its history are fictional.</p>
    </div>
  </footer>

  <script>
    // Change this to the email address where you want to receive reservations.
    const CLUB_EMAIL = "your-email@example.com";

    const rows = [...document.querySelectorAll(".row[data-name]")];
    const totalEl = document.getElementById("total");
    const statusEl = document.getElementById("status");
    const form = document.getElementById("reserve");
    const quantities = new Map(rows.map((row) => [row, 0]));

    function updateTotal() {
      let total = 0;
      rows.forEach((row) => {
        total += quantities.get(row) * Number(row.dataset.price);
      });
      totalEl.textContent = `$${total}`;
      return total;
    }

    rows.forEach((row) => {
      const count = row.querySelector(".count");

      row.querySelectorAll(".stepper").forEach((button) => {
        button.addEventListener("click", () => {
          const next = Math.min(9, Math.max(0, quantities.get(row) + Number(button.dataset.step)));
          quantities.set(row, next);
          count.textContent = next === 0 ? "\u2013" : next;
          count.classList.remove("bump");
          void count.offsetWidth;
          count.classList.add("bump");
          statusEl.textContent = "";
          updateTotal();
        });
      });
    });

    form.addEventListener("submit", (event) => {
      event.preventDefault();

      const picks = rows
        .filter((row) => quantities.get(row) > 0)
        .map((row) => {
          const size = row.querySelector("select")?.value || "One size";
          return `${quantities.get(row)} x ${row.dataset.name} (${size})`;
        });

      if (picks.length === 0) {
        statusEl.textContent = "Mark at least one piece on your card.";
        return;
      }

      if (!form.checkValidity()) {
        statusEl.textContent = "Enter your name and a valid email address.";
        return;
      }

      const data = new FormData(form);
      const subject = `Card reservation from ${data.get("name")}`;
      const body = [
        `Name: ${data.get("name")}`,
        `Email: ${data.get("email")}`,
        "",
        ...picks,
        "",
        `Card total: $${updateTotal()}`
      ].join("\n");

      window.location.href = `mailto:${CLUB_EMAIL}?subject=${encodeURIComponent(subject)}&body=${encodeURIComponent(body)}`;
      statusEl.textContent = "Your email is ready. Send it to finish reserving.";
    });
  </script>
</body>
</html>
