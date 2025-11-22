# bamboo
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>BambooCo — Bamboo Solutions</title>
  <!-- ====== Custom font: change --root --font-family to use your preferred font (Google Fonts link in head if needed) ====== -->
  <style>
    :root{
      --accent:#2e8b57;          /* bamboo green */
      --accent-2:#185c3d;
      --bg:#f7f7f6;
      --text:#111;
      --muted:#555;
      --font-family: "Inter", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
      --nav-height:64px;
    }
    /* Basic Reset */
    *{box-sizing:border-box}
    html,body{height:100%;margin:0;font-family:var(--font-family);color:var(--text);background:var(--bg);-webkit-font-smoothing:antialiased}
    a{color:inherit;text-decoration:none}
    /* Header / Navbar */
    header{
      position:sticky;top:0;z-index:50;background:rgba(255,255,255,0.9);backdrop-filter: blur(4px);
      border-bottom:1px solid #eee;
    }
    .nav{
      max-width:1100px;margin:0 auto;height:var(--nav-height);display:flex;align-items:center;justify-content:space-between;padding:0 18px;
    }
    .brand{display:flex;align-items:center;gap:12px}
    .brand .logo{
      width:42px;height:42px;border-radius:8px;background:linear-gradient(135deg,var(--accent),var(--accent-2));display:flex;align-items:center;justify-content:center;color:white;font-weight:700;
      font-family:monospace;
    }
    nav ul{display:flex;gap:16px;align-items:center;margin:0;padding:0;list-style:none}
    nav button.lang{background:transparent;border:1px solid #ddd;padding:6px 10px;border-radius:8px;cursor:pointer}
    .hero{
      max-width:1100px;margin:28px auto;padding:0 18px;display:grid;grid-template-columns:1fr 420px;gap:28px;align-items:center;
    }
    .hero .left{padding:18px;background:white;border-radius:12px;box-shadow:0 6px 20px rgba(10,10,10,0.05)}
    .hero h1{margin:0 0 10px 0;font-size:28px}
    .hero p.lead{margin:0 0 16px;color:var(--muted)}
    .hero .cta{display:flex;gap:10px}
    .btn{padding:10px 14px;border-radius:10px;border:0;cursor:pointer;font-weight:600}
    .btn.primary{background:var(--accent);color:white}
    .btn.ghost{background:transparent;border:1px solid #ddd}
    .hero .right img{width:100%;height:100%;min-height:250px;object-fit:cover;border-radius:12px}
    /* Services */
    .section{max-width:1100px;margin:28px auto;padding:0 18px}
    .services{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:18px}
    .card{background:white;border-radius:10px;padding:18px;box-shadow:0 6px 18px rgba(10,10,10,0.04)}
    .card h3{margin:0 0 8px 0}
    .muted{color:var(--muted)}
    /* Contact + Map */
    .contact-grid{display:grid;grid-template-columns:1fr 360px;gap:18px;align-items:start}
    .contact-form label{display:block;margin:8px 0 6px;font-weight:600}
    .contact-form input, .contact-form textarea{width:100%;padding:10px;border-radius:8px;border:1px solid #e6e6e6}
    iframe.map{width:100%;height:360px;border-radius:10px;border:0}
    /* Footer */
    footer{max-width:1100px;margin:28px auto;padding:18px;text-align:center;color:var(--muted)}
    /* Responsive */
    @media (max-width:900px){
      .hero{grid-template-columns:1fr}
      .contact-grid{grid-template-columns:1fr}
    }
  </style>
</head>
<body>
  <header>
    <div class="nav">
      <div class="brand">
        <div class="logo">B</div>
        <div>
          <div style="font-weight:700">BambooCo</div>
          <div style="font-size:12px;color:var(--muted)">Sustainable bamboo solutions</div>
        </div>
      </div>

      <nav>
        <ul>
          <li><a href="#services" data-i18n="nav_services">Services</a></li>
          <li><a href="#about" data-i18n="nav_about">About</a></li>
          <li><a href="#contact" data-i18n="nav_contact">Contact</a></li>
          <li><button class="lang" id="langToggle">Kurdî</button></li>
        </ul>
      </nav>
    </div>
  </header>

  <main>
    <section class="hero" aria-label="hero">
      <div class="left">
        <h1 data-i18n="hero_title">Premium Bamboo Products & Services</h1>
        <p class="lead" data-i18n="hero_sub">We supply sustainable bamboo materials and design services for construction, furniture and landscaping.</p>
        <div class="cta">
          <a class="btn primary" href="#contact" data-i18n="hero_cta">Get in touch</a>
          <a class="btn ghost" href="#services" data-i18n="hero_cta2">Our services</a>
        </div>

        <div style="margin-top:16px;">
          <strong data-i18n="hero_loc_label">Location:</strong>
          <div class="muted" id="companyLocation">Erbil, Kurdistan Region (replace with your address)</div>
        </div>

        <div style="margin-top:14px;">
          <strong data-i18n="hero_contact_label">Contact:</strong>
          <div class="muted">Phone: <span id="phone">+964-770-000-0000</span> • Email: <span id="email">info@bambooco.example</span></div>
        </div>
      </div>

      <div class="right">
        <!-- Unsplash image (copyable link below) -->
        <img src="https://images.unsplash.com/photo-1493655167920-6b5f6a4b7f3f?q=80&w=1600&auto=format&fit=crop&ixlib=rb-4.0.3&s=placeholder" alt="bamboo hero image">
      </div>
    </section>

    <section id="services" class="section">
      <h2 data-i18n="services_title">Our Services</h2>
      <div class="services" aria-hidden="false">
        <div class="card">
          <h3 data-i18n="svc_supply">Bamboo Supply</h3>
          <p class="muted" data-i18n="svc_supply_p">High-quality bamboo poles, treated and graded for construction and manufacturing.</p>
        </div>
        <div class="card">
          <h3 data-i18n="svc_design">Design & Fabrication</h3>
          <p class="muted" data-i18n="svc_design_p">Custom bamboo furniture, panels and structures designed to your specifications.</p>
        </div>
        <div class="card">
          <h3 data-i18n="svc_landscape">Landscaping</h3>
          <p class="muted" data-i18n="svc_landscape_p">Bamboo-based fencing, screening and garden features for sustainable landscaping.</p>
        </div>
        <div class="card">
          <h3 data-i18n="svc_consult">Consultation & Installation</h3>
          <p class="muted" data-i18n="svc_consult_p">Project consulting, installation supervision and maintenance guidance.</p>
        </div>
      </div>
    </section>

    <section id="about" class="section">
      <h2 data-i18n="about_title">About BambooCo</h2>
      <div class="card" style="padding:18px;margin-top:12px">
        <p data-i18n="about_p">We are committed to sustainable sourcing and craftsmanship. Our team works with architects, contractors and homeowners to create durable, beautiful bamboo products.</p>
      </div>
    </section>

    <section id="contact" class="section" aria-label="contact">
      <h2 data-i18n="contact_title">Contact & Location</h2>
      <div class="contact-grid" style="margin-top:12px">
        <div class="card contact-form">
          <form onsubmit="event.preventDefault(); alert(i18n[currentLang].thanks_contact)">
            <label for="name" data-i18n="form_name">Name</label>
            <input id="name" placeholder="" required />
            <label for="email" data-i18n="form_email">Email</label>
            <input id="email_in" type="email" placeholder="" required />
            <label for="message" data-i18n="form_message">Message</label>
            <textarea id="message" rows="5" placeholder="" required></textarea>
            <div style="margin-top:12px;">
              <button class="btn primary" type="submit" data-i18n="form_send">Send Message</button>
            </div>
          </form>
        </div>

        <div>
          <div class="card" style="padding:10px;">
            <div style="display:flex;justify-content:space-between;align-items:center">
              <div>
                <strong data-i18n="contact_info">Contact Info</strong>
                <div class="muted" style="margin-top:8px"><span id="phone_copy">+964-770-000-0000</span><br><span id="email_copy">info@bambooco.example</span></div>
              </div>
            </div>
            <div style="margin-top:10px">
              <small class="muted" data-i18n="map_note">Our approximate location (replace coordinates below in the iframe with your exact location)</small>
            </div>
          </div>

          <!-- Map iframe: replace src coords with your exact coordinates or Google Maps share link -->
          <div style="margin-top:12px">
            <iframe
              class="map"
              title="Company location"
              src="https://www.google.com/maps/embed?pb=!1m14!1m12!1m3!1d80565.123456789!2d44.0094!3d36.1911!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!5e0!3m2!1sen!2s!4v0000000000000"
              allowfullscreen=""
              loading="lazy"
            ></iframe>
          </div>
        </div>
      </div>
    </section>

    <footer>
      <div>© <span id="year"></span> BambooCo — Sustainable Bamboo Solutions</div>
      <div class="muted" style="margin-top:6px">Designed for quick customization. Ask me to change fonts, colors, or the navigator.</div>
    </footer>
  </main>

  <script>
    // Simple bilingual dictionary (English + Kurdish Kurmanji)
    const i18n = {
      en: {
        nav_services: "Services",
        nav_about: "About",
        nav_contact: "Contact",
        hero_title: "Premium Bamboo Products & Services",
        hero_sub: "We supply sustainable bamboo materials and design services for construction, furniture and landscaping.",
        hero_cta: "Get in touch",
        hero_cta2: "Our services",
        hero_loc_label: "Location:",
        hero_contact_label: "Contact:",
        services_title: "Our Services",
        svc_supply: "Bamboo Supply",
        svc_supply_p: "High-quality bamboo poles, treated and graded for construction and manufacturing.",
        svc_design: "Design & Fabrication",
        svc_design_p: "Custom bamboo furniture, panels and structures designed to your specifications.",
        svc_landscape: "Landscaping",
        svc_landscape_p: "Bamboo-based fencing, screening and garden features for sustainable landscaping.",
        svc_consult: "Consultation & Installation",
        svc_consult_p: "Project consulting, installation supervision and maintenance guidance.",
        about_title: "About BambooCo",
        about_p: "We are committed to sustainable sourcing and craftsmanship. Our team works with architects, contractors and homeowners to create durable, beautiful bamboo products.",
        contact_title: "Contact & Location",
        form_name: "Name",
        form_email: "Email",
        form_message: "Message",
        form_send: "Send Message",
        contact_info: "Contact Info",
        map_note: "Our approximate location (replace coordinates in the iframe with your exact location)",
        thanks_contact: "Thank you — we'll contact you soon!"
      },
      ku: {
        nav_services: "Xizmetî",
        nav_about: "Di derbarê de",
        nav_contact: "Têkilî",
        hero_title: "Berhem û Xizmetên Bambuya Bilind",
        hero_sub: "Em materyalên bambûyê yên bæstanê û xizmetên dizaynê bo avahî, mobîlya û bakûrê daynin.",
        hero_cta: "Têkilî dan",
        hero_cta2: "Xizmetên me",
        hero_loc_label: "Cîh:",
        hero_contact_label: "Têkilî:",
        services_title: "Xizmetên Me",
        svc_supply: "Pêşkêşkirina Bambû",
        svc_supply_p: "Bambûyên baldar, muavenî û ji bo avahî û çêkirinê amade.",
        svc_design: "Dizayn û Çêkirin",
        svc_design_p: "Mobîlya û strûktûrên bambûyê yên xweşik û taybet.",
        svc_landscape: "Xizmeta Baxçeyê",
        svc_landscape_p: "Sînor, ekran û taybetmendiyên baxçeyê ji bambû.",
        svc_consult: "Rêkeftin û Sazkirin",
        svc_consult_p: "Rêkeftin bo proje, kontrola sazkirinê û rêjeyên parastinê.",
        about_title: "Di derbarê BambooCo de",
        about_p: "Em bi berdestkirina dirêj û hunerê xebitîn. Tîma me bi mîmaran, kontraktoran û xwedî malan re dixebite da ku berhemên bambûyê bidefîne.",
        contact_title: "Têkilî & Cîh",
        form_name: "Nav",
        form_email: "Email",
        form_message: "Peyam",
        form_send: "Bişîne",
        contact_info: "Agahdariya Têkilî",
        map_note: "Cîhiya me (coords-ên iframeê biguherîne bi cîhê rast)",
        thanks_contact: "Spas — em ê zû têkilîdaynin!"
      }
    };

    // default language
    let currentLang = 'en';

    function updateText(lang){
      currentLang = lang;
      document.querySelectorAll('[data-i18n]').forEach(el=>{
        const key = el.getAttribute('data-i18n');
        if(i18n[lang] && i18n[lang][key]) el.textContent = i18n[lang][key];
      });
      // change lang button label
      document.getElementById('langToggle').textContent = lang === 'en' ? 'Kurdî' : 'EN';
      // accessibility: update document lang attribute
      document.documentElement.lang = (lang === 'en') ? 'en' : 'ku';
    }

    // initial render
    updateText('en');

    // lang toggle
    document.getElementById('langToggle').addEventListener('click',()=>{
      updateText(currentLang === 'en' ? 'ku' : 'en');
    });

    // footer year
    document.getElementById('year').textContent = new Date().getFullYear();

    // TODO: replace the image src with a real Unsplash link if you want a specific photo.
  </script>
</body>
</html>

its my company website for showing our services
