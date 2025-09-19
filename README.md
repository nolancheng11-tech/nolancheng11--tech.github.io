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
      --accent-glow: 0 0 18px rgba(0,240,255,0.06), 0 0 6px rgba(0,255,136,0.04);
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
      box-shadow: 0 8px 40px rgba(0,0,0,0.7), var(--accent-glow);
      border: 1px solid rgba(0,255,255,0.03);
      backdrop-filter: blur(6px);
    }

    header{
      display:flex;
      flex-direction:column;
      gap:10px;
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
      gap:8px;
      align-items:center;
    }

    .subtitle{
      color:var(--neon-cyan);
      font-weight:400;
      font-size:14px;
      margin-top:4px;
      opacity:0.9;
    }

    nav{
      margin:18px 0;
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
      background: linear-gradient(180deg, rgba(255,255,255,0.01), rgba(255,255,255,0.005));
      border:1px solid rgba(255,255,255,0.02);
    }

    .lead{
      color:var(--muted);
      font-size:15px;
      margin-bottom:10px;
    }

    .glow-title{
      color:var(--neon-cyan);
      font-weight:700;
      text-shadow: 0 0 8px rgba(0,240,255,0.08);
      margin-bottom:8px;
    }

    .row{
      display:grid;
      grid-template-columns: 1fr 320px;
      gap:20px;
      align-items:start;
    }

    .card{
      background:var(--glass);
      padding:12px;
      border-radius:8px;
      border:1px solid rgba(255,255,255,0.02);
    }

    .image-grid{
      display:grid;
      gap:12px;
    }

    figure{
      margin:0;
      border-radius:8px;
      overflow:hidden;
      border:1px solid rgba(255,255,255,0.02);
      background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
    }

    figure img{
      width:100%;
      display:block;
      height:190px;
      object-fit:cover;
      filter: contrast(1.05) saturate(1.08);
    }

    figcaption{
      padding:8px;
      font-size:12px;
      color:var(--muted);
    }

    .countries-list{
      display:grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap:12px;
      margin-top:12px;
    }

    .country{
      background: linear-gradient(180deg, rgba(0,0,0,0.25), rgba(255,255,255,0.01));
      padding:12px;
      border-radius:8px;
      border:1px solid rgba(255,255,255,0.02);
    }
    .country h4{
      margin:0 0 6px 0;
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

    /* responsive */
    @media (max-width:880px){
      .row{ grid-template-columns:1fr; }
      figure img { height:140px; }
    }

    /* small code-like badges */
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
  </style>
</head>

<body id="top">
  <div class="container">
    <header>
      <h1>Internet Censorship</h1>
      <div class="byline">
        <div>By <strong style="color:var(--neon-cyan);">Nolan Cheng</strong></div>
        <div class="subtitle">A concise, neutral, educational overview of how censorship interacts with online systems, data, and policy.</div>
      </div>

      <nav aria-label="Main navigation">
        <a href="#how-it-works">How the Internet Works</a>
        <a href="#censorship">Censorship & Free Speech</a>
        <a href="#countries">Countries with Restrictions</a>
        <a href="#closing">Closing Notes</a>
      </nav>
    </header>

    <!-- HOW IT WORKS -->
    <section id="how-it-works">
      <div class="glow-title">How the Internet Works — a short technical primer</div>
      <p class="lead">
        The internet connects many computing devices across networks. Information flows as digital signals — composed of <span class="vocab">bits</span> and <span class="vocab">bytes</span> — which are grouped into <strong>packets</strong> and routed through routers and servers using standards such as <span class="vocab">IP</span> and <span class="vocab">TCP</span>. The maximum amount of data that can be moved per second is called <span class="vocab">bandwidth</span>, and each piece of data often carries <span class="vocab">metadata</span> that helps systems identify the sender, the receiver, or the type of content.
      </p>

      <div class="row">
        <div>
          <div class="card">
            <h3 style="margin-top:0;color:var(--neon-green)">Paths, protocols, and redundancy</h3>
            <p>
              A message typically splits into many packets that may take different <strong>paths</strong> across the network. Protocols (agreed sets of rules) like <span class="vocab">HTTP</span> and <span class="vocab">TCP</span> define how data is requested, transported, and reassembled. Because the internet contains multiple physical connections, redundancy and fault tolerance let traffic reroute when parts of the network fail — making the system <span class="vocab">fault tolerant</span> and scalable.
            </p>

            <p class="note">
              Example: a 1000-byte file is 8,000 bits; a router divides it into packets and forwards them — packets may arrive out-of-order and be reassembled by the receiver.
            </p>
          </div>

          <div style="height:12px"></div>

          <div class="card">
            <h3 style="color:var(--neon-cyan)">Analog versus digital data, and limits</h3>
            <p>
              The world includes <span class="vocab">analog data</span> (smoothly varying signals like audio). To send that over the internet it must be sampled and encoded digitally. Finite digital representations cause potential <span class="vocab">roundoff</span> or precision limits when the number of bits is insufficient. Compression can be <span class="vocab">lossless</span> (full recovery possible) or <span class="vocab">lossy</span> (some information discarded for smaller size).
            </p>
          </div>
        </div>

        <aside class="card">
          <div style="font-size:14px;color:var(--neon-green);font-weight:700;margin-bottom:8px">Quick glossary (inline)</div>
          <div style="font-size:13px;color:var(--muted)">
            <div><span class="vocab">bit</span> — binary digit (0 or 1)</div>
            <div><span class="vocab">byte</span> — 8 bits</div>
            <div><span class="vocab">bandwidth</span> — bit rate capacity</div>
            <div><span class="vocab">metadata</span> — data about data</div>
          </div>
        </aside>
      </div>
    </section>

    <!-- CENSORSHIP & FREE SPEECH -->
    <section id="censorship">
      <div class="glow-title">Censorship and Free Speech Online — mechanics and examples</div>

      <p class="lead">
        Censorship online can happen in many technical ways: blocking URLs, filtering packets, throttling bandwidth, disconnecting entire networks, or legally requiring platforms to remove content. Systems can inspect <span class="vocab">metadata</span>, throttle particular protocols, or remove access to specific <span class="vocab">URLs</span> — all actions that affect how information flows on the web.
      </p>

      <div class="row">
        <div>
          <p>
            Platforms and governments use a mix of legal and technical tools. For example, some states implement full internet shutdowns (disconnecting paths so packets cannot be routed), while others require platform-level moderation rules that result in removal of content. These measures interact with the underlying computer network architecture: DNS can be manipulated to hide names, routers may be ordered to block IP addresses, and deep packet inspection can filter traffic based on content or protocol signatures.
          </p>

          <p>
            When content is compressed and shared, the difference between <span class="vocab">lossless</span> and <span class="vocab">lossy</span> matters — for archiving journalism or evidence, lossless formats preserve original information, but lossy formats may be chosen for faster delivery over constrained <span class="vocab">bandwidth</span>.
          </p>

          <p class="note">
            This page is educational and aims to describe common technical mechanisms and policy patterns without advocating for particular policies.
          </p>
        </div>

        <aside class="card">
          <h4 style="color:var(--neon-cyan);margin:0 0 8px 0">Technical levers of censorship</h4>
          <ul style="margin:0;padding-left:18px;color:var(--muted);font-size:13px">
            <li>DNS blocking or poisoning</li>
            <li>IP address blocking</li>
            <li>URL / keyword filtering</li>
            <li>Bandwidth throttling or traffic shaping</li>
            <li>Platform takedowns and legal orders</li>
            <li>Complete network shutdowns</li>
          </ul>
        </aside>
      </div>
    </section>

    <!-- COUNTRIES -->
    <section id="countries">
      <div class="glow-title">Countries with notable restrictions (selection)</div>
      <p class="lead">Below is a longer list of countries that have been reported to impose significant restrictions on online speech or access. Each blurb briefly summarizes common forms of censorship observed or reported in public sources.</p>

      <div class="countries-list">
        <!-- Country entries: image links point to Wikimedia Commons pages (click through for full image & attribution) -->
        <div class="country">
          <h4>China</h4>
          <p class="note">Extensive content filtering and platform-level controls (the "Great Firewall"), blocking many international services, strong legal oversight of platforms and metadata collection; nationwide monitoring and removal of content is common. <a href="https://commons.wikimedia.org/wiki/File:China_Censorship22.jpg" target="_blank" rel="noopener">Image (Commons)</a></p>
        </div>

        <div class="country">
          <h4>Iran</h4>
          <p class="note">Frequent internet shutdowns in times of unrest, filtering of social platforms, and legal penalties for online speech; network-level blocking and throttles have been widely used. <a href="https://commons.wikimedia.org/wiki/File:Internet_censorship_in_Iran_-_censorship_in_Iran_-_Internet_shutdown_in_Iran_-_2019_Iranian_protests_-_%D8%B3%D8%A7%D9%86%D8%B3%D9%88%D8%B1_%D8%A7%DB%8C%D9%86%D8%AA%D8%B1%D9%86%D8%AA_.jpg" target="_blank" rel="noopener">Image (Commons)</a></p>
        </div>

        <div class="country">
          <h4>North Korea</h4>
          <p class="note">Very limited public internet access; tightly controlled national intranet with only regime-approved content; independent online communication is effectively blocked for most people. <a href="https://commons.wikimedia.org/wiki/File:North_Korea_-_Computer_(5381234656).jpg" target="_blank" rel="noopener">Image (Commons)</a></p>
        </div>

        <div class="country">
          <h4>Russia</h4>
          <p class="note">Blocking and fines for platforms and media that refuse to remove content; laws requiring local data and content removal; measures to block or throttle services during political events. <a href="https://commons.wikimedia.org/wiki/Category:Internet_censorship_in_Russia" target="_blank" rel="noopener">Image category (Commons)</a></p>
        </div>

        <div class="country">
          <h4>Saudi Arabia</h4>
          <p class="note">Website filtering, social media monitoring, and legal penalties for content deemed to violate local laws or morality codes; platforms are required to comply with takedown requests. <a href="https://commons.wikimedia.org/wiki/Category:Censorship_in_Saudi_Arabia" target="_blank" rel="noopener">Image category (Commons)</a></p>
        </div>

        <div class="country">
          <h4>Vietnam</h4>
          <p class="note">Legal restrictions on political content, platform regulation, and takedowns; some international services intermittently blocked or restricted. <a href="https://en.wikipedia.org/wiki/Internet_censorship_in_Vietnam" target="_blank" rel="noopener">Country overview (Wikipedia)</a></p>
        </div>

        <div class="country">
          <h4>Myanmar</h4>
          <p class="note">Internet shutdowns and social platform blocks used during political crises; access reduced to control information flows and public organization online. <a href="https://rsf.org/" target="_blank" rel="noopener">Reports (RSF)</a></p>
        </div>

        <div class="country">
          <h4>Belarus</h4>
          <p class="note">Blocking of independent media sites and social platforms during protests; legal pressure on platforms and journalists. <a href="https://rsf.org/" target="_blank" rel="noopener">Reports (RSF)</a></p>
        </div>

        <div class="country">
          <h4>Cuba</h4>
          <p class="note">Limited and expensive connectivity historically, with monitoring and restrictions on political content; occasional shutdowns and platform controls. <a href="https://freedomhouse.org/report/freedom-net" target="_blank" rel="noopener">Freedom on the Net</a></p>
        </div>

        <div class="country">
          <h4>Turkmenistan</h4>
          <p class="note">Very limited public internet and heavy filtering; most independent outlets are blocked and access is constrained by the state. <a href="https://freedomhouse.org/report/freedom-net" target="_blank" rel="noopener">Freedom on the Net</a></p>
        </div>

        <div class="country">
          <h4>Uzbekistan</h4>
          <p class="note">State controls and content filtering, together with pressure on independent media and online platforms; reforms occasionally shift levels of restriction. <a href="https://freedomhouse.org/report/freedom-net" target="_blank" rel="noopener">Freedom on the Net</a></p>
        </div>

        <div class="country">
          <h4>Eritrea</h4>
          <p class="note">Extremely limited press and internet freedom; state control of available content and blocking of independent sites. <a href="https://rsf.org/" target="_blank" rel="noopener">Reports (RSF)</a></p>
        </div>

        <div class="country">
          <h4>United Arab Emirates (UAE)</h4>
          <p class="note">Legal and technical restrictions on political speech and some online content; regulation of messaging apps and platform compliance. <a href="https://freedomhouse.org/report/freedom-net" target="_blank" rel="noopener">Freedom on the Net</a></p>
        </div>

        <div class="country">
          <h4>Ethiopia</h4>
          <p class="note">Occasional social media blocks and network disruptions during unrest; laws and actions that affect press and online expression. <a href="https://apnews.com/article/e111d7de4ac8223088159182c664d1f2" target="_blank" rel="noopener">Recent reporting</a></p>
        </div>

        <div class="country">
          <h4>Nepal & selected regional examples</h4>
          <p class="note">Several countries may impose platform restrictions or registration rules for social media, sometimes temporarily blocking services; such measures can affect commerce, education, and emergency communications. <a href="https://apnews.com/article/e111d7de4ac8223088159182c664d1f2" target="_blank" rel="noopener">Recent reporting (AP)</a></p>
        </div>

      </div>

      <p class="note" style="margin-top:12px">
        This list is illustrative rather than exhaustive. Levels and types of restrictions change over time — the research community (e.g., Freedom on the Net, RSF) monitors these developments and publishes periodic updates.
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

      <p class="note">
        If you'd like, Nolan, I can:
        <ul>
          <li>Replace the Commons links with specific direct image file URLs so images render inline (no clicks needed).</li>
          <li>Trim or expand the country list to your preferred length (shorter or still longer).</li>
          <li>Add printable/print-friendly CSS or a lightweight PDF export.</li>
        </ul>
      </p>
    </section>

    <footer>
      <div>Created by <strong style="color:var(--neon-cyan)">Nolan Cheng</strong></div>
      <div style="color:var(--muted)">Sources: Freedom on the Net, Reporters Without Borders, news reporting; image links to Wikimedia Commons and public reporting.</div>
    </footer>

    <a class="top-btn" href="#top">↑ Back to Top</a>
  </div>
</body>
</html>
