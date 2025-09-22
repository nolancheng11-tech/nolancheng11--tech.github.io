# nolancheng11--tech.github.io
AP Computer Science Principles Project
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Internet Censorship — Nolan Cheng</title>

  <!-- Roboto font -->
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&display=swap" rel="stylesheet">

  <style>
    :root{
      --bg:#040406;
      --panel:#07070a;
      --neon-cyan: #00f0ff;
      --neon-green:#00ff88;
      --muted:#9aa3ad;
      --glass: rgba(255,255,255,0.03);
      --max-width:1000px;
    }
    html,body{
      height:100%;
      margin:0;
      background: linear-gradient(180deg, #020203 0%, #060609 100%);
      color: #dfe9f2;
      font-family: "Roboto", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.45;
    }
    a { color: var(--neon-cyan); text-decoration: none; }
    a:hover { text-decoration: underline; }
    .container{
      max-width: var(--max-width);
      margin: 48px auto;
      padding: 28px;
      background: linear-gradient(180deg, rgba(255,255,255,0.015), rgba(255,255,255,0.008));
      border-radius: 14px;
      box-shadow: 0 8px 40px rgba(0,0,0,0.7), 0 0 26px rgba(0,255,136,0.04);
      border: 1px solid rgba(0,255,255,0.03);
      backdrop-filter: blur(6px);
    }
    header{
      display:flex;
      flex-direction:column;
      gap:8px;
      align-items:flex-start;
      margin-bottom:18px;
    }
    h1{
      margin:0;
      font-size: clamp(28px, 4vw, 44px);
      letter-spacing: 0.6px;
      color: var(--neon-green);
      text-shadow: 0 0 10px rgba(0,255,136,0.12), 0 0 26px rgba(0,255,136,0.06);
    }
    .byline{
      color: var(--muted);
      font-size:14px;
      display:flex;
      gap:4px;
      flex-direction:column;
      align-items:flex-start;
    }
    .bio {
      color: var(--neon-cyan);
      font-weight:500;
      font-size:13px;
    }
    .subtitle{
      color:var(--neon-cyan);
      font-weight:400;
      font-size:14px;
      margin-top:4px;
      opacity:0.9;
    }
    nav{
      margin:14px 0;
      display:flex;
      gap:12px;
      flex-wrap:wrap;
    }
    nav a{
      padding:8px 12px;
      border-radius:8px;
      background: linear-gradient(90deg, rgba(0,255,136,0.02), rgba(0,240,255,0.01));
      color:var(--neon-cyan);
      font-weight:500;
      border:1px solid rgba(0,255,136,0.03);
      font-size:13px;
    }
    section{
      margin:28px 0;
      padding:20px;
      border-radius:10px;
      background: linear-gradient(180deg, rgba(255,255,255,0.01), rgba(255,255,white: 0.005));
      border:1px solid rgba(255,255,255,0.02);
    }
    .glow-title{
      color:var(--neon-cyan);
      font-weight:700;
      text-shadow: 0 0 8px rgba(0,240,255,0.08);
      margin-bottom:8px;
    }
    .lead{
      color:var(--muted);
      font-size:15px;
      margin-bottom:10px;
    }
    .row{
      display:grid;
      grid-template-columns: 1fr 320px;
      gap:20px;
      align-items:start;
    }
    .card{
      background:rgba(255,255,255,0.02);
      padding:12px;
      border-radius:8px;
      border:1px solid rgba(255,255,255,0.02);
    }
    figure {
      margin:12px 0;
    }
    figure img {
      width:100%;
      max-width:480px;
      height:auto;
      display:block;
      border-radius:8px;
      border:1px solid rgba(255,255,255,0.02);
    }
    .attribution {
      font-size:11px;
      color:var(--muted);
      margin-top:4px;
    }
    .countries-list{
      display:grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap:20px;
      margin-top:12px;
    }
    .country{
      background: linear-gradient(180deg, rgba(0,0,0,0.25), rgba(255,255,255,0.01));
      padding:12px;
      border-radius:8px;
      border:1px solid rgba(255,255,255,0.02);
    }
    .country img {
      width:100%;
      height:auto;
      border-radius:6px;
      border:1px solid rgba(255,255,255,0.02);
    }
    .country h4{
      margin:12px 0 6px 0;
      color:var(--neon-green);
    }
    .country p{
      margin:0;
      color:var(--muted);
      font-size:13px;
    }
    footer{
      margin-top:18px;
      color:var(--muted);
      font-size:13px;
      display:flex;
      justify-content:space-between;
      align-items:center;
      gap:8px;
      flex-wrap:wrap;
    }
    .top-btn{
      position: fixed;
      right: 22px;
      bottom: 22px;
      background: linear-gradient(180deg, rgba(0,255,136,0.12), rgba(0,240,255,0.06));
      color: var(--neon-cyan);
      border-radius: 999px;
      padding: 12px 14px;
      font-weight:700;
      border:1px solid rgba(0,255,136,0.06);
      text-decoration:none;
      box-shadow: 0 6px 30px rgba(0,255,136,0.03);
      backdrop-filter: blur(6px);
      transform: translateZ(0);
    }
    .vocab{
      display:inline-block;
      font-family: monospace;
      background:rgba(0,255,136,0.04);
      padding:2px 6px;
      border-radius:6px;
      border:1px solid rgba(0,255,136,0.03);
      color: var(--neon-green);
      font-size:12px;
      margin-left:6px;
    }
    .note{
      color:var(--muted);
      font-size:13px;
      margin-top:10px;
    }
    @media (max-width:880px){
      .row{ grid-template-columns:1fr; }
      figure img { max-width:100%; height:auto; }
    }
  </style>
</head>

<body id="top">
  <div class="container">
    <header>
      <h1>Internet Censorship</h1>
      <div class="byline">
        <div>By <strong style="color:var(--neon-cyan);">Nolan Cheng</strong></div>
        <div class="bio">Future Electrical Engineer</div>
        <div class="subtitle">A concise, neutral, educational overview of how censorship interacts with online systems, data, and policy.</div>
      </div>

      <nav aria-label="Main navigation">
        <a href="#how-it-works">How the Internet Works</a>
        <a href="#censorship">Censorship & Free Speech</a>
        <a href="#countries">Countries with Restrictions</a>
        <a href="#closing">Closing Notes</a>
        <a href="#unit1">Unit 1 Vocabulary</a>
        <a href="#unit2">Unit 2 Vocabulary</a>
      </nav>
    </header>

    <!-- HOW IT WORKS -->
    <section id="how-it-works">
      <div class="glow-title">How the Internet Works — a short technical primer</div>
      <p class="lead">
        The internet connects many computing devices across networks. Information flows as digital signals — composed of <span class="vocab">bits</span> and <span class="vocab">bytes</span> — which are grouped into <strong>packets</strong> and routed through routers and servers using standards such as <span class="vocab">IP</span> and <span class="vocab">TCP</span>. The maximum amount of data that can be moved per second is called <span class="vocab">bandwidth</span>, and each piece of data often carries <span class="vocab">metadata</span> that helps systems identify the sender, the receiver, or the type of content.
      </p>
    </section>

    <!-- CENSORSHIP -->
    <section id="censorship">
      <div class="glow-title">Censorship and Free Speech Online — mechanics and examples</div>
      <p class="lead">
        Censorship online can happen in many technical ways: blocking URLs, filtering packets, throttling bandwidth, disconnecting entire networks, or legally requiring platforms to remove content. Systems can inspect <span class="vocab">metadata</span>, throttle particular protocols, or remove access to specific <span class="vocab">URLs</span> — all actions that affect how information flows on the web.
      </p>
    </section>

    <!-- COUNTRIES WITH PHOTOS -->
    <section id="countries">
      <div class="glow-title">Countries with notable restrictions (selection)</div>
      <p class="lead">Here are several countries with documented restrictions on internet speech, each illustrated with a photo and a short description.</p>

      <div class="countries-list">
        <!-- China with photo -->
        <div class="country">
          <img src="https://upload.wikimedia.org/wikipedia/commons/6/67/China_Censorship22.jpg" alt="Internet censorship illustration in China">
          <h4>China</h4>
          <p>Extensive content filtering and platform-level controls (the “Great Firewall”), blocking many international services and monitoring metadata; nationwide filtering and takedowns are common.</p>
          <div class="attribution">Photo: mikemacmarketing via Flickr / CC BY 2.0 :contentReference[oaicite:0]{index=0}</div>
        </div>

        <!-- Iran with placeholder photo or from Commons if available -->
        <div class="country">
          <img src="https://upload.wikimedia.org/wikipedia/commons/a/a0/Internet_censorship_in_Iran_-_censorship_in_Iran_-_Internet_shutdown_in_Iran_%282019%29.jpg" alt="Internet shutdown in Iran">
          <h4>Iran</h4>
          <p>Frequent social platform filtering and periodic internet shutdowns during unrest; state controls and throttles limit access to some services.</p>
          <div class="attribution">Photo: Wikimedia Commons / CC BY-SA (Photographer unknown) *</div>
        </div>

        <!-- Vietnam example photo -->
        <div class="country">
          <img src="https://upload.wikimedia.org/wikipedia/commons/3/3d/Ho_Chi_Minh_City_Traffic.jpg" alt="Cityscape Vietnam">
          <h4>Vietnam</h4>
          <p>Legal restrictions on political content, platform regulation, and periodic blocking of international services.</p>
          <div class="attribution">Photo: Wikimedia Commons / Public Domain *</div>
        </div>

        <!-- Additional country entries with placeholder photos or later replacement -->
        <div class="country">
          <img src="https://upload.wikimedia.org/wikipedia/commons/e/e6/Flag_of_Russia.svg" alt="Flag of Russia">
          <h4>Russia</h4>
          <p>Blocking and legal pressure on platforms and independent media; measures to block or throttle services have been used during political events.</p>
          <div class="attribution">Image: Flag via Wikimedia Commons / Public Domain *</div>
        </div>

        <div class="country">
          <img src="https://upload.wikimedia.org/wikipedia/commons/4/4f/Flag_of_Saudi_Arabia.svg" alt="Flag of Saudi Arabia">
          <h4>Saudi Arabia</h4>
          <p>Website filtering, monitoring of social media, and takedown requests to platforms for content deemed to violate local laws or morality rules.</p>
          <div class="attribution">Image: Flag via Wikimedia Commons / Public Domain *</div>
        </div>

        <!-- More countries as before... -->
      </div>

      <p class="note" style="margin-top:12px">
        * Attribution for some images: photographer/license not fully known or placeholder; replacements can be done. This list is illustrative rather than exhaustive.
      </p>
    </section>

    <!-- CLOSING NOTES -->
    <section id="closing">
      <div class="glow-title">Closing notes — neutral, educational summary</div>
      <p>
        Online censorship can be implemented using technical network controls (blocking, filtering, throttling), platform moderation, legal orders, or full network shutdowns. Understanding the technical building blocks — bits and bytes, packets, protocols, bandwidth, and metadata — helps clarify how such controls are implemented and why they affect people differently depending on the local infrastructure and laws.
      </p>

      <p>
        For educators and students: when studying this topic, consider both the network-level mechanisms (how packets and routing work) and the social/political context (laws, platform policies, and public goods like safety and privacy). Accurate technical vocabulary — like <span class="vocab">packet</span>, <span class="vocab">bandwidth</span>, <span class="vocab">lossy</span> / <span class="vocab">lossless</span> — helps make nuanced, factual descriptions possible.
      </p>
    </section>

    <!-- UNIT 1 VOCAB -->
    <section id="unit1">
      <div class="glow-title">Unit 1: Data — short vocabulary resources</div>
      <p class="lead">Short definitions and mixed diagrams / images illustrating key data concepts.</p>

      <div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:12px;">
        <div class="card">
          <h4 style="margin:0 0 8px 0;color:var(--neon-green)">bit</h4>
          <p style="color:var(--muted);margin:0 0 10px 0">A binary digit, either 0 or 1, that is the smallest unit of digital data.</p>
          <figure>
            <img src="https://upload.wikimedia.org/wikipedia/commons/8/80/Binary_Clock_Display.jpg" alt="Binary clock display showing bits">
            <div class="attribution">Photo: Wikimedia Commons / CC BY-SA *</div>
          </figure>
        </div>

        <div class="card">
          <h4 style="margin:0 0 8px 0;color:var(--neon-green)">byte</h4>
          <p style="color:var(--muted);margin:0 0 10px 0">A sequence of 8 bits commonly used as a single unit for representing data.</p>
          <figure>
            <img src="https://upload.wikimedia.org/wikipedia/commons/2/23/Hexdump_sample.png" alt="Hex dump sample showing bytes">
            <div class="attribution">Photo: Wikimedia Commons / CC BY-SA *</div>
          </figure>
        </div>

        <div class="card">
          <h4 style="margin:0 0 8px 0;color:var(--neon-green)">metadata</h4>
          <p style="color:var(--muted);margin:0 0 10px 0">Data about data, such as file type, timestamps, sender or receiver labels.</p>
          <figure>
            <img src="https://upload.wikimedia.org/wikipedia/commons/a/a4/Exif_example.jpg" alt="EXIF metadata example in photo file">
            <div class="attribution">Photo: Wikimedia Commons / CC BY-SA *</div>
          </figure>
        </div>

      </div>
    </section>

    <!-- UNIT 2 VOCAB -->
    <section id="unit2">
      <div class="glow-title">Unit 2: Computer Systems & Networks — short vocabulary resources</div>
      <p class="lead">Definitions and diagrams illustrating network and system concepts.</p>

      <div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:12px;">
        <div class="card">
          <h4 style="margin:0 0 8px 0;color:var(--neon-green)">DNS / URL</h4>
          <p style="color:var(--muted);margin:0 0 10px 0">DNS translates human-friendly URLs into IP addresses that routers use to forward packets.</p>
          <figure>
            <img src="https://upload.wikimedia.org/wikipedia/commons/8/8d/DomainNameSystem.png" alt="Diagram of the Domain Name System">
            <div class="attribution">Diagram: Sakari A. Maaranen / CC BY 3.0 :contentReference[oaicite:1]{index=1}</div>
          </figure>
        </div>

        <div class="card">
          <h4 style="margin:0 0 8px 0;color:var(--neon-green)">Path / Router / IP</h4>
          <p style="color:var(--muted);margin:0 0 10px 0">A path is the route packets take; routers forward packets and IP addresses identify devices on that path.</p>
          <figure>
            <img src="https://upload.wikimedia.org/wikipedia/commons/0/0c/Internet_blackholes.svg" alt="Map of internet obstacles to flow of information">
            <div class="attribution">Diagram: “Internet Blackholes” map, Wikimedia Commons / Public Domain :contentReference[oaicite:2]{index=2}</div>
          </figure>
        </div>

      </div>
    </section>

    <footer>
      <div>Created by <strong style="color:var(--neon-cyan)">Nolan Cheng</strong></div>
      <div style="color:var(--muted)">Sources: Freedom on the Net, Reporters Without Borders, Wikimedia Commons photo/diagram licenses.</div>
    </footer>

    <a class="top-btn" href="#top">↑ Back to Top</a>
  </div>
</body>
</html>
