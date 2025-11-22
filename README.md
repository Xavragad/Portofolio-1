<!DOCTYPE html>

<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Angelo Roneil C. Paa — Fantasy Grimoire</title>

  <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;700&family=Merriweather:wght@300;700&display=swap" rel="stylesheet">

  <style>
    :root{
      --bg-deep:#07040b;
      --gold:#d9a441;
      --muted:#d9d6cf;
      --accent:#b64b4b;
      --max-width:1000px;
      --radius:14px;
    }
    *{box-sizing:border-box;margin:0;padding:0}
    html,body{height:100%}
    body{
      font-family:'Merriweather',serif;
      background:
        radial-gradient(1200px 600px at 10% 10%, rgba(120,40,160,0.12), transparent 6%),
        radial-gradient(900px 500px at 90% 80%, rgba(10,10,30,0.18), transparent 12%),
        linear-gradient(180deg, rgba(0,0,0,0.6), rgba(0,0,0,0.85)),
        url('../Homepage_files/480301141_9279944875455896_5586049436356959454_n.jpg') center/cover fixed;
      color:var(--muted);
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      padding-bottom:60px;
      position:relative;
      overflow-x:hidden;
    }

    .motes{position:fixed;inset:0;pointer-events:none;z-index:5;mix-blend-mode:screen}
    .motes i{position:absolute;width:6px;height:6px;border-radius:50%;background:linear-gradient(135deg,var(--gold),rgba(255,200,120,0.9));box-shadow:0 0 12px rgba(217,164,65,0.6);animation:float 8s linear infinite;opacity:0.85;filter:blur(.6px)}
    .motes i.alt{background:linear-gradient(135deg,var(--accent),#ff9aa0);box-shadow:0 0 10px rgba(182,75,75,0.45)}
    @keyframes float{0%{transform:translateY(0) translateX(0) scale(.7)}50%{transform:translateY(-140vh) translateX(60vw) scale(1)}100%{transform:translateY(-280vh) translateX(0) scale(.7)}}

    header{max-width:var(--max-width);margin:36px auto;padding:28px;display:flex;gap:18px;align-items:center;background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(0,0,0,0.12));border-radius:var(--radius);border:1px solid rgba(255,255,255,0.04);box-shadow:0 10px 60px rgba(2,0,10,0.6);position:relative;z-index:10}
    .crest{width:124px;height:124px;flex:0 0 124px;display:flex;align-items:center;justify-content:center;border-radius:12px;background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(0,0,0,0.25));border:2px solid rgba(217,164,65,0.06);box-shadow:inset 0 2px 12px rgba(0,0,0,0.6)}
    .crest svg{width:86px;height:86px;filter:drop-shadow(0 6px 18px rgba(0,0,0,0.6))}
    .hero-meta{flex:1}
    .hero-meta h1{font-family:'Cinzel',serif;font-weight:700;color:var(--gold);letter-spacing:1px;font-size:2rem;margin-bottom:6px;text-shadow:0 2px 8px rgba(0,0,0,0.7)}
    .hero-meta p{color:var(--muted);font-size:0.98rem;max-width:70ch;line-height:1.6}

    main.container{max-width:var(--max-width);margin:24px auto;padding:0 18px;z-index:8;position:relative}
    .section{margin:22px 0;background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(0,0,0,0.14));border-radius:12px;padding:20px;border:1px solid rgba(255,255,255,0.03);box-shadow:0 12px 40px rgba(2,0,10,0.5);position:relative;overflow:hidden}
    .section:before{content:"";position:absolute;inset:0;background:linear-gradient(135deg, rgba(217,164,65,0.02), transparent 20%), url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="400" height="400"><defs><linearGradient id="g" x1="0" x2="1"><stop offset="0" stop-color="%23fff" stop-opacity="0.02"/><stop offset="1" stop-color="%23fff" stop-opacity="0"/></linearGradient></defs><rect width="100%" height="100%" fill="url(%23g)"/></svg>');pointer-events:none;mix-blend-mode:overlay;opacity:0.6}
    .section h2{font-family:'Cinzel',serif;color:var(--gold);font-size:1.25rem;margin-bottom:8px;letter-spacing:0.6px;display:inline-block;padding-right:12px;position:relative;z-index:2}
    .ornament{display:inline-block;vertical-align:middle;margin-left:10px;color:var(--accent);opacity:0.95}
    p, li{color:var(--muted);font-size:0.98rem;line-height:1.7}
    ul{margin-left:18px}

    .grid{display:grid;grid-template-columns:repeat(3,1fr);gap:18px;margin-top:12px}
    .card{
      display:flex;
      flex-direction:column;
      gap:10px;
      background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(0,0,0,0.18));
      padding:16px;border-radius:10px;border:1px solid rgba(255,255,255,0.03);transform:translateZ(0);
      transition:transform .28s ease,box-shadow .28s ease;
      text-decoration:none;
      color:inherit;
      cursor:pointer;
    }
    .card:focus{outline:3px solid rgba(217,164,65,0.18);outline-offset:4px}
    .card:hover{transform:translateY(-8px) scale(1.01);box-shadow:0 18px 60px rgba(10,0,30,0.55),0 0 18px rgba(217,164,65,0.06)}
    .thumb{width:100%;height:160px;overflow:hidden;border-radius:8px;background:#0b0b0b;border:1px solid rgba(255,255,255,0.02);display:flex;align-items:center;justify-content:center}
    .thumb img{width:100%;height:100%;object-fit:cover;display:block;transition:transform .6s ease}
    .card:hover .thumb img{ transform: scale(1.06) }
    .card h4{font-family:'Cinzel',serif;color:var(--gold);margin-bottom:6px;font-size:1rem}
    .card p{color:var(--muted);font-size:.92rem}

    .skills{display:flex;flex-wrap:wrap;gap:10px;margin-top:12px}
    .rune{padding:8px 12px;background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(10,6,8,0.18));border-radius:999px;border:1px solid rgba(255,255,255,0.04);color:var(--muted);font-weight:700;font-size:.9rem;box-shadow:0 6px 18px rgba(0,0,0,0.45);letter-spacing:.6px;position:relative;transition:transform .22s ease,box-shadow .22s ease}
    .rune:before{content:"✦";color:var(--gold);margin-right:8px;opacity:0.9;display:inline-block;transform:translateY(-1px)}
    .rune:hover{transform:translateY(-6px) scale(1.03);box-shadow:0 20px 40px rgba(0,0,0,0.6)}

    .contact-row{display:flex;gap:12px;align-items:center;margin-top:12px;flex-wrap:wrap}
    .btn{padding:10px 14px;border-radius:10px;background:linear-gradient(180deg,var(--gold),#b8862b);color:#0b0710;font-weight:700;text-decoration:none;box-shadow:0 8px 26px rgba(181,134,59,0.12);border:1px solid rgba(255,255,255,0.04)}
    .btn.secondary{background:transparent;color:var(--muted);border:1px dashed rgba(255,255,255,0.04)}

    footer{max-width:var(--max-width);margin:36px auto 80px;text-align:center;color:rgba(217,210,195,0.85);font-size:0.95rem}

    /* modal styles */
    .modal{position:fixed;inset:0;display:none;z-index:60;align-items:center;justify-content:center;padding:28px}
    .modal.open{display:flex}
    .modal-overlay{position:absolute;inset:0;background:linear-gradient(180deg, rgba(0,0,0,0.6), rgba(0,0,0,0.75));backdrop-filter:blur(3px)}
    .modal-panel{position:relative;max-width:1000px;width:100%;background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(0,0,0,0.12));border-radius:12px;padding:18px;border:1px solid rgba(255,255,255,0.04);box-shadow:0 30px 80px rgba(0,0,0,0.7);z-index:61}
    .modal-close{position:absolute;right:12px;top:12px;background:transparent;border:0;color:var(--muted);font-size:18px;cursor:pointer}
    .modal-body{display:grid;grid-template-columns:1fr 380px;gap:18px;align-items:start}
    .modal-media{background:#0b0b0b;padding:8px;border-radius:8px;border:1px solid rgba(255,255,255,0.03);display:flex;align-items:center;justify-content:center;flex-direction:column}
    .modal-media img{width:100%;height:100%;max-height:520px;object-fit:contain;border-radius:6px;cursor:zoom-in}
    .modal-gallery{display:grid;grid-template-columns:repeat(4,1fr);gap:8px;margin-top:12px;width:100%}
    .modal-thumb{height:68px;border-radius:6px;overflow:hidden;border:2px solid transparent;cursor:pointer;display:block}
    .modal-thumb img{width:100%;height:100%;object-fit:cover;display:block}
    .modal-thumb[aria-selected="true"]{outline:2px solid var(--gold)}
    .modal-info h2{font-family:'Cinzel',serif;color:var(--gold);margin:0 0 8px 0}
    .modal-info .muted{color:var(--muted);margin:0 0 8px 0}
    .modal-info .meta{color:var(--muted);font-size:.93rem;margin-bottom:10px}
    .modal-info .desc{line-height:1.6;color:var(--muted)}

    /* lightbox (enlarged image) */
    .lightbox{position:fixed;inset:0;display:none;align-items:center;justify-content:center;background:rgba(0,0,0,0.92);z-index:200;padding:24px}
    .lightbox.open{display:flex}
    .lightbox img{max-width:95%;max-height:95%;object-fit:contain;border-radius:6px;box-shadow:0 20px 80px rgba(0,0,0,0.8);cursor:zoom-out;transition:transform .28s ease}
    .lightbox .close-hint{position:fixed;top:18px;right:20px;color:var(--muted);font-size:14px;opacity:0.9}

    /* --- Sword cursor styles --- */
    /* hide native cursor; show sword sprite */
    body { cursor: none; }
    /* interactive elements keep native pointer for UX */
    a, button, input, textarea, .card { cursor: pointer; }

    .sword {
      position: fixed;
      left: 0;
      top: 0;
      width: 64px;
      height: 64px;
      pointer-events: none;
      z-index: 9999;
      transform-origin: 50% 78%;
      will-change: transform, left, top;
      transition: transform .06s linear;
      opacity: 0.98;
      display: block;
      mix-blend-mode: normal;
    }
    .sword svg { width: 100%; height: 100%; display: block; }
    .sword.swing { animation: sword-swing 420ms cubic-bezier(.2,.8,.2,1) forwards; }
    @keyframes sword-swing {
      0%   { transform: rotate(0deg) translate(0,0); }
      30%  { transform: rotate(-85deg) translate(18px,-6px) scale(1.04); }
      65%  { transform: rotate(-30deg) translate(6px,-3px); }
      100% { transform: rotate(0deg) translate(0,0); }
    }

    @media(max-width:900px){.modal-body{grid-template-columns:1fr}.modal-media img{max-height:320px}}
    @media (max-width:980px){.grid{grid-template-columns:repeat(2,1fr)}header{flex-direction:column;align-items:center;text-align:center}.hero-meta p{max-width:100%}}
    @media (max-width:640px){.grid{grid-template-columns:1fr}.crest{width:96px;height:96px;flex:0 0 96px}.hero-meta h1{font-size:1.5rem}}
  </style>
</head>
<body>

  <div class="motes" aria-hidden="true">
    <i style="left:4%; bottom:-10%; width:6px;height:6px; animation-duration:10s"></i>
    <i class="alt" style="left:16%; bottom:-20%; width:8px;height:8px; animation-duration:12s"></i>
    <i style="left:36%; bottom:-5%; width:5px;height:5px; animation-duration:9s"></i>
    <i class="alt" style="left:64%; bottom:-30%; width:7px;height:7px; animation-duration:11s"></i>
    <i style="left:82%; bottom:-15%; width:6px;height:6px; animation-duration:13s"></i>
  </div>

  <!-- sword cursor element (aria-hidden) -->
  <div class="sword" aria-hidden="true">
    <svg viewBox="0 0 64 64" xmlns="http://www.w3.org/2000/svg" aria-hidden="true" focusable="false">
      <g stroke="#111" stroke-width="1">
        <path d="M32 2 L38 12 L46 20 L38 28 L32 26 L26 28 L18 20 L26 12 Z" fill="#eef2f6"/>
        <rect x="30" y="28" width="4" height="16" rx="1" fill="#dfe6ea"/>
        <path d="M32 30 L33 40" stroke="#bfc8cd" stroke-width="1.2" stroke-linecap="round"/>
        <rect x="16" y="44" width="32" height="4" rx="2" fill="#8b6b47" stroke="#6b4f33"/>
        <rect x="28" y="48" width="8" height="10" rx="2" fill="#3b2b20" stroke="#231815"/>
        <circle cx="32" cy="60" r="3.5" fill="#8b6b47" stroke="#6b4f33"/>
      </g>
    </svg>
  </div>

  <header role="banner" aria-label="Intro crest">
    <div class="crest" aria-hidden="true">
      <svg viewBox="0 0 64 64" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
        <defs><linearGradient id="g" x1="0" x2="1"><stop offset="0" stop-color="#ffd98b"/><stop offset="1" stop-color="#cf8a3a"/></linearGradient></defs>
        <circle cx="32" cy="32" r="30" fill="url(#g)" opacity="0.12"/>
        <path d="M32 12c6 6 12 8 12 18s-6 20-12 22c-6-2-12-12-12-22s6-12 12-18z" fill="#b64b4b" opacity="0.95"/>
        <path d="M32 20c3 3 6 4 6 9s-3 11-6 12c-3-1-6-7-6-12s3-6 6-9z" fill="#fff" opacity="0.06"/>
      </svg>
    </div>

    <div class="hero-meta">
      <h1>Angelo Roneil C. Paa</h1>
      <p>Game Artist & Developer — Weaver of worlds, sculptor of light and shadow. Environments, models and gameplay — forged with Blender, Unity and a restless imagination.</p>
    </div>
  </header>

  <main class="container" role="main">
    <section class="section" id="about" aria-labelledby="about-title">
      <h2 id="about-title">About the Traveler <span class="ornament">✦</span></h2>
      <p>I craft atmospheric worlds and characters with an eye for silhouette and mood. My tools include Blender for modelling, Unity for interactivity, and a range of paint & texture tools for the final flourish. I enjoy blending technical systems with artistic direction to make playable stories feel alive.</p>
      <div class="contact-row" style="margin-top:14px">
        <a class="btn" href="#projects">View Grimoire (Projects)</a>
        <a class="btn secondary" href="../resume.pdf" download>Download Tome (Resume)</a>
      </div>
    </section>

    <section class="section" id="projects" aria-labelledby="projects-title">
      <h2 id="projects-title">Grimoire of Works <span class="ornament">✦</span></h2>

      <div class="grid" role="list">
        <div class="card" role="listitem" tabindex="0" data-id="darkons" aria-label="Open Darkon's Madness project">
          <div class="thumb"><img src="assets/darkons-1.png" alt="Darkon's Madness — preview"></div>
          <h4>Darkon's Madness — Guest Artist (2019)</h4>
          <p>Environment props and textures; contributed mood pieces and banners used during the event.</p>
        </div>

        <div class="card" role="listitem" tabindex="0" data-id="tomato-works" aria-label="Open Tomato Works project">
          <div class="thumb"><img src="assets/tomato-works-1.png" alt="Tomato Works — preview"></div>
          <h4>Tomato Works — Lead Artist (2023)</h4>
          <p>Led art direction, asset pipeline and level visuals. Focus on readable silhouette and color language.</p>
        </div>

        <div class="card" role="listitem" tabindex="0" data-id="pixel-canopy" aria-label="Open Pixel Canopy project">
          <div class="thumb"><img src="assets/pixel-canopy-1.png" alt="Pixel Canopy — preview"></div>
          <h4>Pixel Canopy — Back End Dev (2025)</h4>
          <p>Server-side tooling and content pipelines to support live services and asset distribution.</p>
        </div>

        <div class="card" role="listitem" tabindex="0" data-id="pixel-z" aria-label="Open Pixel Z project">
          <div class="thumb"><img src="assets/pixel-z-1.png" alt="Pixel Z — preview"></div>
          <h4>Pixel Z — Full Stack (2025)</h4>
          <p>Web portal for analytics and content management with dashboard visualizations.</p>
        </div>

        <div class="card" role="listitem" tabindex="0" data-id="asset-pack" aria-label="Open 3D Asset Pack project">
          <div class="thumb"><img src="assets/asset-pack-1.png" alt="3D Asset Pack — preview"></div>
          <h4>3D Asset Pack (2024)</h4>
          <p>Collection of rigs, PBR textures and props for environment kits and quick prototyping.</p>
        </div>

        <div class="card" role="listitem" tabindex="0" data-id="personal-demos" aria-label="Open Personal Demos project">
          <div class="thumb"><img src="assets/personal-demos-1.png" alt="Personal demos — preview"></div>
          <h4>Personal Demos</h4>
          <p>Small Unity prototypes exploring narrative tools, lighting setups and locomotion mechanics.</p>
        </div>
      </div>
    </section>

    <section class="section" id="skills" aria-labelledby="skills-title">
      <h2 id="skills-title">Runes & Tools <span class="ornament">✦</span></h2>
      <div class="skills" role="list">
        <span class="rune">Unity (C#)</span>
        <span class="rune">Blender</span>
        <span class="rune">Maya</span>
        <span class="rune">Substance Painter</span>
        <span class="rune">Photoshop</span>
        <span class="rune">Krita</span>
        <span class="rune">C#, C++</span>
        <span class="rune">3D Modeling</span>
        <span class="rune">Rigging & Animation</span>
        <span class="rune">Game Design</span>
      </div>
    </section>

    <section class="section" id="contact" aria-labelledby="contact-title">
      <h2 id="contact-title">Summon & Contact <span class="ornament">✦</span></h2>
      <p>To request work, collaborations, or to trade stories, send a raven (or email): <a href="mailto:202210124@feualabang.edu.ph" style="color:var(--gold);text-decoration:underline">202210124@feualabang.edu.ph</a></p>
      <p style="margin-top:10px">Phone: <strong>09608138619</strong> — Location: San Pedro, Laguna</p>
    </section>
  </main>

  <!-- static single-page modal viewer with gallery (4 images per project) -->
  <div id="project-modal" class="modal" aria-hidden="true" role="dialog" aria-modal="true" aria-labelledby="modal-title">
    <div class="modal-overlay" data-close></div>
    <div class="modal-panel" role="document">
      <button class="modal-close" aria-label="Close project (Esc)">✕</button>
      <div class="modal-body">
        <div class="modal-media" aria-live="polite">
          <img id="modal-image" src="assets/darkons-1.png" alt="">
          <div class="modal-gallery" id="modal-gallery" role="listbox" aria-label="Project gallery"></div>
        </div>
        <div class="modal-info">
          <h2 id="modal-title">Project title</h2>
          <p id="modal-role" class="muted">Role</p>
          <div class="meta"><strong>Year:</strong> <span id="modal-year">—</span> · <strong>Tools:</strong> <span id="modal-tools">—</span></div>
          <div id="modal-desc" class="desc">Description</div>
          <div id="modal-links" style="margin-top:12px"></div>
        </div>
      </div>
    </div>
  </div>

  <!-- lightbox element (enlarged image) -->
  <div id="lightbox" class="lightbox" role="dialog" aria-hidden="true" aria-label="Enlarged image">
    <span class="close-hint">Esc or click to close</span>
    <img id="lightbox-img" src="" alt="">
  </div>

  <footer role="contentinfo">
    <p>&copy; 2025 Angelo Roneil C. Paa — Crafted with care. Member: Junior Philippine Computer Society</p>
  </footer>

  <script>
    (function(){
      // static projects map — each has up to 4 images (placeholders named accordingly)
      const projects = {
        "darkons": {
          title: "Darkon's Madness",
          role: "Guest Artist",
          year: "2019",
          tools: "Blender, Substance, Photoshop",
          gallery: [
            "assets/darkons-1.png",
            "assets/darkons-2.png",
            "assets/darkons-3.png",
            "assets/darkons-4.png"
          ],
          description: "Environment props and textures; contributed mood pieces and banners used during the event."
        },
        "tomato-works": {
          title: "Tomato Works",
          role: "Lead Artist",
          year: "2023",
          tools: "Blender, Unity, Substance",
          gallery: [
            "assets/tomato-works-1.png",
            "assets/tomato-works-2.png",
            "assets/tomato-works-3.png",
            "assets/tomato-works-4.png"
          ],
          description: "Led art direction, asset pipeline and level visuals. Focus on readable silhouette and color language."
        },
        "pixel-canopy": {
          title: "Pixel Canopy",
          role: "Back End Dev",
          year: "2025",
          tools: "Node, C#, Docker",
          gallery: [
            "assets/pixel-canopy-1.png",
            "assets/pixel-canopy-2.png",
            "assets/pixel-canopy-3.png",
            "assets/pixel-canopy-4.png"
          ],
          description: "Server-side tooling and content pipelines to support live services and asset distribution."
        },
        "pixel-z": {
          title: "Pixel Z",
          role: "Full Stack",
          year: "2025",
          tools: "React, Node, SQL",
          gallery: [
            "assets/pixel-z-1.png",
            "assets/pixel-z-2.png",
            "assets/pixel-z-3.png",
            "assets/pixel-z-4.png"
          ],
          description: "Web portal for analytics and content management with dashboard visualizations."
        },
        "asset-pack": {
          title: "3D Asset Pack",
          role: "Creator",
          year: "2024",
          tools: "Blender, Substance",
          gallery: [
            "assets/asset-pack-1.png",
            "assets/asset-pack-2.png",
            "assets/asset-pack-3.png",
            "assets/asset-pack-4.png"
          ],
          description: "Collection of rigs, PBR textures and props for environment kits and quick prototyping."
        },
        "personal-demos": {
          title: "Personal Demos",
          role: "Solo Prototypes",
          year: "Ongoing",
          tools: "Unity, C#",
          gallery: [
            "assets/personal-demos-1.png",
            "assets/personal-demos-2.png",
            "assets/personal-demos-3.png",
            "assets/personal-demos-4.png"
          ],
          description: "Small Unity prototypes exploring narrative tools, lighting setups and locomotion mechanics."
        }
      };

      const modal = document.getElementById('project-modal');
      const modalImage = document.getElementById('modal-image');
      const modalTitle = document.getElementById('modal-title');
      const modalRole = document.getElementById('modal-role');
      const modalYear = document.getElementById('modal-year');
      const modalTools = document.getElementById('modal-tools');
      const modalDesc = document.getElementById('modal-desc');
      const modalGallery = document.getElementById('modal-gallery');

      const lightbox = document.getElementById('lightbox');
      const lightboxImg = document.getElementById('lightbox-img');

      let lastFocused = null;
      let currentIndex = 0;
      let currentGallery = [];

      function buildGallery(gallery, initialIndex = 0){
        modalGallery.innerHTML = '';
        currentGallery = (gallery || []).slice();
        currentIndex = Math.max(0, Math.min(initialIndex, currentGallery.length - 1));
        currentGallery.forEach((src, i) => {
          const btn = document.createElement('button');
          btn.className = 'modal-thumb';
          btn.type = 'button';
          btn.setAttribute('aria-label', 'Image ' + (i+1));
          btn.setAttribute('data-idx', i);
          if(i === currentIndex) btn.setAttribute('aria-selected', 'true');
          const im = document.createElement('img');
          im.src = src;
          im.alt = (modalTitle.textContent || '') + ' image ' + (i+1);
          btn.appendChild(im);
          btn.addEventListener('click', ()=> {
            setMainImage(i);
            btn.focus();
          });
          // double-click or Ctrl+Enter opens lightbox from thumbnail
          btn.addEventListener('dblclick', ()=> openLightbox(src, modalTitle.textContent + ' image ' + (i+1)));
          btn.addEventListener('keydown', (e)=> {
            if((e.key === 'Enter' && e.ctrlKey) || e.key === ' '){
              e.preventDefault();
              openLightbox(src, modalTitle.textContent + ' image ' + (i+1));
            }
          });
          modalGallery.appendChild(btn);
        });
        setMainImage(currentIndex);
      }

      function setMainImage(index){
        if(!currentGallery.length) return;
        index = Math.max(0, Math.min(index, currentGallery.length - 1));
        currentIndex = index;
        modalImage.src = currentGallery[index];
        modalImage.alt = (modalTitle.textContent || '') + ' preview ' + (index+1);
        modalGallery.querySelectorAll('.modal-thumb').forEach((t)=>{
          t.setAttribute('aria-selected', t.dataset.idx === String(index) ? 'true' : 'false');
        });
      }

      function openModal(id){
        const data = projects[id];
        if(!data) return;
        modalTitle.textContent = data.title;
        modalRole.textContent = data.role;
        modalYear.textContent = data.year;
        modalTools.textContent = data.tools;
        modalDesc.textContent = data.description;
        buildGallery(data.gallery || [data.image || 'assets/placeholder.png'], 0);
        modal.classList.add('open');
        modal.setAttribute('aria-hidden','false');
        lastFocused = document.activeElement;
        const closeBtn = modal.querySelector('.modal-close');
        if(closeBtn) closeBtn.focus();
        document.body.style.overflow = 'hidden';
        document.addEventListener('keydown', onKeyDown);
      }

      function closeModal(){
        modal.classList.remove('open');
        modal.setAttribute('aria-hidden','true');
        document.body.style.overflow = '';
        if(lastFocused && lastFocused.focus) lastFocused.focus();
        document.removeEventListener('keydown', onKeyDown);
        closeLightbox();
      }

      function onKeyDown(e){
        if(e.key === 'Escape') return closeModal();
        if(e.key === 'ArrowRight') { setMainImage(currentIndex + 1); }
        if(e.key === 'ArrowLeft') { setMainImage(currentIndex - 1); }
        if(e.key === 'Tab'){
          const focusables = modal.querySelectorAll('button, a[href], input, textarea, [tabindex]:not([tabindex="-1"])');
          if(!focusables.length) return;
          const first = focusables[0], last = focusables[focusables.length-1];
          if(e.shiftKey && document.activeElement === first){ e.preventDefault(); last.focus(); }
          else if(!e.shiftKey && document.activeElement === last){ e.preventDefault(); first.focus(); }
        }
      }

      // attach handlers to cards
      document.querySelectorAll('.grid .card').forEach(card=>{
        card.addEventListener('click', function(e){
          e.preventDefault();
          const id = card.dataset.id;
          if(id) openModal(id);
        });
        card.addEventListener('keydown', function(e){
          if(e.key === 'Enter' || e.key === ' ') { e.preventDefault(); const id = card.dataset.id; if(id) openModal(id); }
        });
      });

      // close actions
      modal.querySelector('[data-close]')?.addEventListener('click', closeModal);
      modal.querySelector('.modal-close')?.addEventListener('click', closeModal);
      modal.addEventListener('click', (e)=>{ if(e.target === modal) closeModal(); });

      /* LIGHTBOX (enlarged image) */
      function openLightbox(src, alt = ''){
        if(!src) return;
        lightboxImg.src = src;
        lightboxImg.alt = alt || '';
        lightbox.classList.add('open');
        lightbox.setAttribute('aria-hidden','false');
        document.addEventListener('keydown', onLightboxKey);
      }
      function closeLightbox(){
        if(!lightbox.classList.contains('open')) return;
        lightbox.classList.remove('open');
        lightbox.setAttribute('aria-hidden','true');
        lightboxImg.src = '';
        document.removeEventListener('keydown', onLightboxKey);
      }
      function onLightboxKey(e){
        if(e.key === 'Escape') return closeLightbox();
        if(e.key === 'ArrowRight'){ setMainImage(currentIndex + 1); lightboxImg.src = currentGallery[currentIndex]; }
        if(e.key === 'ArrowLeft'){ setMainImage(currentIndex - 1); lightboxImg.src = currentGallery[currentIndex]; }
      }

      // click main modal image opens lightbox
      modalImage.addEventListener('click', ()=> {
        if(modal.classList.contains('open')) openLightbox(modalImage.src, modalImage.alt);
      });

      // clicking a thumbnail sets main image (dblclick opens lightbox handled in buildGallery)
      modalGallery.addEventListener('click', (e)=> {
        const btn = e.target.closest('.modal-thumb');
        if(!btn) return;
        const idx = Number(btn.dataset.idx || 0);
        setMainImage(idx);
      });

      // close lightbox on click overlay or image
      lightbox.addEventListener('click', (e)=> {
        if(e.target === lightbox || e.target === lightboxImg) closeLightbox();
      });

      // ensure lightbox closes when modal closes
      modal.querySelector('.modal-close')?.addEventListener('click', ()=>{ closeLightbox(); closeModal(); });
      modal.querySelector('[data-close]')?.addEventListener('click', ()=>{ closeLightbox(); closeModal(); });

    })();
  </script>

  <!-- Sword cursor behavior: follow pointer + dblclick swing -->
  <script>
    (function(){
      const sword = document.querySelector('.sword');
      if(!sword) return;
      const W = 64, H = 64;

      // track pointer; offset so blade tip aligns to pointer
      function onMove(e){
        const left = (e.clientX || (e.touches && e.touches[0].clientX) || 0) - W/2;
        const top  = (e.clientY || (e.touches && e.touches[0].clientY) || 0) - H*0.14;
        sword.style.left = left + 'px';
        sword.style.top  = top  + 'px';
      }

      // enable on mouse move
      window.addEventListener('mousemove', onMove, { passive: true });

      // double click or double tap to swing
      let lastTap = 0;
      function triggerSwing(){
        sword.classList.remove('swing');
        void sword.offsetWidth;
        sword.classList.add('swing');
      }

      document.addEventListener('dblclick', (e) => {
        triggerSwing();
      });

      // simple double-tap detection for touch devices (also prevents permanent hiding)
      document.addEventListener('touchend', function(e){
        const now = Date.now();
        const dt = now - lastTap;
        if(dt < 300 && dt > 30){
          triggerSwing();
        }
        lastTap = now;
      }, { passive: true });

      sword.addEventListener('animationend', ()=> sword.classList.remove('swing'));

      // on first touch, hide sword and restore native cursor for touch UX
      function onFirstTouch(){
        sword.style.display = 'none';
        document.body.style.cursor = '';
        window.removeEventListener('mousemove', onMove);
      }
      window.addEventListener('touchstart', onFirstTouch, { once: true });
    })();
  </script>

