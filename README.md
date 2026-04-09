
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Weekend Workshops Hyderabad</title>
  <style>
    *, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }

    :root {
      --purple-50: #EEEDFE; --purple-100: #CECBF6; --purple-200: #AFA9EC;
      --purple-400: #7F77DD; --purple-600: #534AB7; --purple-800: #3C3489;
      --teal-50: #E1F5EE; --teal-200: #5DCAA5; --teal-600: #0F6E56;
      --coral-50: #FAECE7; --coral-600: #993C1D;
      --pink-50: #FBEAF0; --pink-600: #993556;
      --amber-50: #FAEEDA; --amber-600: #854F0B;
      --red-100: #F7C1C1; --red-700: #A32D2D;
      --bg: #ffffff; --bg-2: #f7f7f5; --bg-3: #f1efe8;
      --text: #1a1a1a; --text-2: #555550; --text-3: #88877f;
      --border: rgba(0,0,0,0.12); --border-2: rgba(0,0,0,0.22);
      --radius-md: 8px; --radius-lg: 12px; --radius-xl: 16px;
    }

    body {
      font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
      color: var(--text); background: var(--bg-3); line-height: 1.6;
    }

    .page-wrap { max-width: 900px; margin: 0 auto; padding: 1.5rem 1.25rem 3rem; }

    /* NAV */
    nav {
      display: flex; justify-content: space-between; align-items: center;
      padding: 1rem 0; margin-bottom: 1.5rem;
      border-bottom: 0.5px solid var(--border);
      flex-wrap: wrap; gap: 0.75rem;
    }
    .nav-brand { font-size: 1rem; font-weight: 600; color: var(--purple-600); }
    .nav-links { display: flex; gap: 1.25rem; }
    .nav-links a {
      font-size: 13px; color: var(--text-2); text-decoration: none;
      transition: color 0.15s;
    }
    .nav-links a:hover { color: var(--purple-600); }

    /* HERO */
    .hero {
      background: linear-gradient(135deg, var(--purple-50) 0%, var(--teal-50) 50%, var(--amber-50) 100%);
      padding: 3.5rem 2rem 3rem; text-align: center;
      border-radius: var(--radius-xl); margin-bottom: 2rem;
    }
    .badge {
      display: inline-block; background: var(--purple-600); color: var(--purple-50);
      font-size: 12px; padding: 4px 14px; border-radius: 20px; margin-bottom: 1rem;
    }
    .hero h1 {
      font-size: 2.4rem; font-weight: 600; color: var(--purple-800);
      line-height: 1.2; margin-bottom: 0.75rem;
    }
    .hero .tagline {
      font-size: 1.05rem; color: var(--purple-600);
      max-width: 500px; margin: 0 auto 1.5rem;
    }
    .hero-meta {
      display: flex; gap: 1rem; justify-content: center;
      flex-wrap: wrap; margin-bottom: 2rem;
    }
    .meta-pill {
      background: rgba(255,255,255,0.8); border: 0.5px solid var(--purple-200);
      border-radius: 20px; padding: 6px 16px;
      font-size: 13px; color: var(--purple-800);
    }
    .cta-btn {
      display: inline-block; background: var(--purple-600); color: var(--purple-50);
      border: none; padding: 14px 36px; border-radius: var(--radius-lg);
      font-size: 15px; font-weight: 500; cursor: pointer; text-decoration: none;
      transition: background 0.2s;
    }
    .cta-btn:hover { background: var(--purple-800); }

    /* STATS */
    .stats-row {
      display: grid; grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
      gap: 1rem; margin-bottom: 2.5rem;
    }
    .stat-card { background: var(--bg); border-radius: var(--radius-md); padding: 1rem; text-align: center; box-shadow: 0 1px 3px rgba(0,0,0,0.06); }
    .stat-num { font-size: 1.8rem; font-weight: 600; color: var(--purple-600); }
    .stat-label { font-size: 12px; color: var(--text-2); margin-top: 2px; }

    /* SECTIONS */
    .section { margin-bottom: 2.5rem; }
    .section-title {
      font-size: 1.3rem; font-weight: 600; color: var(--text);
      margin-bottom: 1.25rem; padding-bottom: 0.5rem;
      border-bottom: 0.5px solid var(--border);
    }

    /* WORKSHOP CARDS */
    .workshops-grid {
      display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 1rem;
    }
    .workshop-card {
      background: var(--bg); border: 0.5px solid var(--border);
      border-radius: var(--radius-lg); padding: 1.25rem;
      transition: border-color 0.2s, transform 0.15s;
      position: relative; overflow: hidden;
    }
    .workshop-card:hover { border-color: var(--purple-400); transform: translateY(-2px); }
    .workshop-card.featured { border: 1.5px solid var(--purple-400); }
    .card-icon { font-size: 28px; margin-bottom: 0.75rem; display: block; }
    .card-name { font-size: 15px; font-weight: 600; margin-bottom: 0.4rem; }
    .card-desc { font-size: 13px; color: var(--text-2); line-height: 1.5; margin-bottom: 0.75rem; }
    .card-tags { display: flex; flex-wrap: wrap; gap: 6px; }
    .tag { font-size: 11px; padding: 3px 10px; border-radius: 12px; font-weight: 500; }
    .tag-purple { background: var(--purple-50); color: var(--purple-600); }
    .tag-teal   { background: var(--teal-50);   color: var(--teal-600); }
    .tag-amber  { background: var(--amber-50);  color: var(--amber-600); }
    .tag-coral  { background: var(--coral-50);  color: var(--coral-600); }
    .tag-pink   { background: var(--pink-50);   color: var(--pink-600); }
    .soon-badge {
      position: absolute; top: 12px; right: 12px;
      background: var(--red-100); color: var(--red-700);
      font-size: 10px; padding: 2px 8px; border-radius: 10px;
    }

    /* HOW IT WORKS */
    .how-grid {
      display: grid; grid-template-columns: repeat(auto-fit, minmax(160px, 1fr)); gap: 1rem;
    }
    .how-step { background: var(--bg); border-radius: var(--radius-md); padding: 1.25rem; text-align: center; box-shadow: 0 1px 3px rgba(0,0,0,0.05); }
    .step-num {
      width: 32px; height: 32px; border-radius: 50%;
      background: var(--purple-50); color: var(--purple-600);
      font-size: 14px; font-weight: 600;
      display: flex; align-items: center; justify-content: center;
      margin: 0 auto 0.75rem;
    }
    .step-title { font-size: 14px; font-weight: 600; margin-bottom: 0.3rem; }
    .step-desc { font-size: 12px; color: var(--text-2); line-height: 1.5; }

    /* TESTIMONIALS */
    .testimonial-grid {
      display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 1rem;
    }
    .testimonial {
      background: var(--bg); border: 0.5px solid var(--border);
      border-left: 3px solid var(--purple-400);
      border-radius: 0 var(--radius-md) var(--radius-md) 0;
      padding: 1rem 1.25rem;
    }
    .testimonial p { font-size: 13px; color: var(--text-2); line-height: 1.6; margin-bottom: 0.75rem; font-style: italic; }
    .testimonial .author { font-size: 12px; font-weight: 600; color: var(--purple-600); }

    /* FAQ */
    .faq-item { border-bottom: 0.5px solid var(--border); padding: 1rem 0; cursor: pointer; }
    .faq-q { font-size: 14px; font-weight: 600; display: flex; justify-content: space-between; align-items: center; }
    .faq-a { font-size: 13px; color: var(--text-2); line-height: 1.6; margin-top: 0.5rem; display: none; }
    .faq-item.open .faq-a { display: block; }
    .faq-arrow { transition: transform 0.2s; color: var(--text-3); font-style: normal; }
    .faq-item.open .faq-arrow { transform: rotate(180deg); }

    /* BOOKING FORM */
    .booking-form {
      background: var(--bg); border: 0.5px solid var(--border);
      border-radius: var(--radius-lg); padding: 1.75rem;
    }
    .form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; margin-bottom: 1rem; }
    @media (max-width: 500px) { .form-row { grid-template-columns: 1fr; } }
    .form-group { display: flex; flex-direction: column; gap: 6px; margin-bottom: 0; }
    .form-label { font-size: 13px; color: var(--text-2); font-weight: 500; }
    .form-input {
      padding: 10px 12px; border: 0.5px solid var(--border-2);
      border-radius: var(--radius-md); font-size: 14px;
      background: var(--bg); color: var(--text);
      font-family: inherit; transition: border-color 0.15s;
    }
    .form-input:focus { outline: none; border-color: var(--purple-400); }
    textarea.form-input { resize: vertical; }
    .submit-btn {
      width: 100%; background: var(--purple-600); color: var(--purple-50);
      border: none; padding: 14px; border-radius: var(--radius-lg);
      font-size: 15px; font-weight: 600; cursor: pointer; margin-top: 0.75rem;
      font-family: inherit; transition: background 0.2s;
    }
    .submit-btn:hover { background: var(--purple-800); }
    .submit-btn:disabled { opacity: 0.5; cursor: default; }
    .success-msg {
      background: var(--teal-50); color: var(--teal-600);
      border: 0.5px solid var(--teal-200);
      border-radius: var(--radius-md); padding: 1rem;
      text-align: center; font-size: 14px; display: none; margin-top: 1rem;
    }

    /* FOOTER */
    footer {
      background: var(--bg-2); border-radius: var(--radius-lg);
      padding: 2rem; margin-top: 2rem; text-align: center;
    }
    footer .brand { font-size: 1rem; font-weight: 600; color: var(--text); margin-bottom: 0.4rem; }
    footer p { font-size: 13px; color: var(--text-2); margin-bottom: 0.3rem; }
    .contact-links { display: flex; gap: 1rem; justify-content: center; flex-wrap: wrap; margin-top: 1rem; }
    .contact-chip {
      background: var(--bg); border: 0.5px solid var(--border);
      border-radius: 20px; padding: 6px 16px;
      font-size: 13px; color: var(--text);
      text-decoration: none;
    }
    .contact-chip:hover { border-color: var(--purple-400); color: var(--purple-600); }
  </style>
</head>
<body>
<div class="page-wrap">

  <nav>
    <span class="nav-brand">🌸 Weekend Workshops Hyderabad</span>
    <div class="nav-links">
      <a href="#workshops">Workshops</a>
      <a href="#about">About</a>
      <a href="#book">Book a spot</a>
    </div>
  </nav>

  <div class="hero">
    <span class="badge">Hyderabad · Every weekend · Summer 2025</span>
    <h1>Make something beautiful.<br>Feel something good.</h1>
    <p class="tagline">Intimate weekend workshops where creativity meets calm. Small groups, big feelings, zero pressure.</p>
    <div class="hero-meta">
      <span class="meta-pill">🌿 15–30 people per session</span>
      <span class="meta-pill">⏱ 2–3 hours</span>
      <span class="meta-pill">📍 Hyderabad</span>
    </div>
    <a href="#book" class="cta-btn">Reserve your spot →</a>
  </div>

  <div class="stats-row">
    <div class="stat-card"><div class="stat-num">6+</div><div class="stat-label">Workshop types</div></div>
    <div class="stat-card"><div class="stat-num">30</div><div class="stat-label">Max per session</div></div>
    <div class="stat-card"><div class="stat-num">2–3h</div><div class="stat-label">Per workshop</div></div>
    <div class="stat-card"><div class="stat-num">Every<br>weekend</div><div class="stat-label">All summer</div></div>
  </div>

  <div class="section" id="workshops">
    <p class="section-title">Our workshops</p>
    <div class="workshops-grid">

      <div class="workshop-card featured">
        <span class="card-icon">💐</span>
        <div class="card-name">Bouquet making</div>
        <div class="card-desc">Arrange fresh seasonal blooms into a bouquet you'll take home. Meditative, fragrant, and deeply satisfying.</div>
        <div class="card-tags"><span class="tag tag-purple">Beginner friendly</span><span class="tag tag-teal">Take-home piece</span></div>
      </div>

      <div class="workshop-card">
        <span class="card-icon">👜</span>
        <div class="card-name">Tote bag painting</div>
        <div class="card-desc">Paint your own tote with fabric colours. From botanicals to abstract — no art experience needed.</div>
        <div class="card-tags"><span class="tag tag-amber">Expressive</span><span class="tag tag-teal">Take-home piece</span></div>
      </div>

      <div class="workshop-card">
        <span class="card-icon">🎂</span>
        <div class="card-name">Cake decoration</div>
        <div class="card-desc">Learn fondant work, piping, and edible florals. You bake your feelings and eat them too.</div>
        <div class="card-tags"><span class="tag tag-pink">Therapeutic</span><span class="tag tag-coral">Snack included</span></div>
      </div>

      <div class="workshop-card">
        <span class="card-icon">🕯️</span>
        <div class="card-name">Candle making</div>
        <div class="card-desc">Blend wax, fragrance, and colour to pour your own soy candle. Calming and sensory.</div>
        <div class="card-tags"><span class="tag tag-amber">Sensory</span><span class="tag tag-teal">Take-home piece</span></div>
      </div>

      <div class="workshop-card">
        <span class="card-icon">🪴</span>
        <div class="card-name">Terrarium building</div>
        <div class="card-desc">Layer soil, moss, and tiny plants into a glass world. Grounding and gently mindful.</div>
        <div class="card-tags"><span class="tag tag-teal">Mindful</span><span class="tag tag-purple">Beginner friendly</span></div>
      </div>

      <div class="workshop-card">
        <span class="soon-badge">Coming soon</span>
        <span class="card-icon">🎨</span>
        <div class="card-name">Pour painting</div>
        <div class="card-desc">Fluid acrylic art — pour, tilt, and watch colours bloom. Messy, joyful, and freeing.</div>
        <div class="card-tags"><span class="tag tag-coral">Joyful</span><span class="tag tag-teal">Take-home piece</span></div>
      </div>

    </div>
  </div>

  <div class="section" id="about">
    <p class="section-title">What makes this different</p>
    <div class="how-grid">
      <div class="how-step">
        <div class="step-num">1</div>
        <div class="step-title">Small groups only</div>
        <div class="step-desc">15–30 people per session so you get real guidance, space, and good conversation.</div>
      </div>
      <div class="how-step">
        <div class="step-num">2</div>
        <div class="step-title">Therapy-inspired</div>
        <div class="step-desc">Each session is designed to feel restorative — not a class, more like a slow Saturday with friends.</div>
      </div>
      <div class="how-step">
        <div class="step-num">3</div>
        <div class="step-title">You create, you keep</div>
        <div class="step-desc">Every workshop ends with a handmade piece that's yours to take home.</div>
      </div>
      <div class="how-step">
        <div class="step-num">4</div>
        <div class="step-title">No experience needed</div>
        <div class="step-desc">These workshops are for curious humans, not trained artists.</div>
      </div>
    </div>
  </div>

  <div class="section">
    <p class="section-title">What people say</p>
    <div class="testimonial-grid">
      <div class="testimonial">
        <p>"I came for the bouquet class and stayed for the vibe. It felt like actual decompression — not just a hobby class."</p>
        <span class="author">— Meera, Banjara Hills</span>
      </div>
      <div class="testimonial">
        <p>"The tote bag session was the most fun I've had on a Saturday in months. I didn't expect to feel so proud of something I made."</p>
        <span class="author">— Rahul, Kondapur</span>
      </div>
      <div class="testimonial">
        <p>"Came with my sister for cake decorating. We laughed the whole time and cried a little too. Highly recommend."</p>
        <span class="author">— Ananya, Jubilee Hills</span>
      </div>
    </div>
  </div>

  <div class="section">
    <p class="section-title">Frequently asked questions</p>

    <div class="faq-item" onclick="this.classList.toggle('open')">
      <div class="faq-q">Do I need to bring anything? <i class="faq-arrow">▾</i></div>
      <div class="faq-a">Nope! All materials, tools, and supplies are included. Just bring yourself (and maybe a friend).</div>
    </div>
    <div class="faq-item" onclick="this.classList.toggle('open')">
      <div class="faq-q">Can I come alone? <i class="faq-arrow">▾</i></div>
      <div class="faq-a">Absolutely! Solo attendees are always welcome. The small group format makes it easy to connect with others naturally.</div>
    </div>
    <div class="faq-item" onclick="this.classList.toggle('open')">
      <div class="faq-q">Where exactly are the workshops held? <i class="faq-arrow">▾</i></div>
      <div class="faq-a">Our studio is in central Hyderabad. The exact address is shared upon booking confirmation via WhatsApp.</div>
    </div>
    <div class="faq-item" onclick="this.classList.toggle('open')">
      <div class="faq-q">What is the cancellation policy? <i class="faq-arrow">▾</i></div>
      <div class="faq-a">Full refund if cancelled 48+ hours before the session. Within 48 hours, your spot can be transferred to someone else or moved to a future date.</div>
    </div>
    <div class="faq-item" onclick="this.classList.toggle('open')">
      <div class="faq-q">Can I book for a group or birthday? <i class="faq-arrow">▾</i></div>
      <div class="faq-a">Yes! We love group bookings and private sessions. Message us on WhatsApp at 7995276651 and we'll arrange something special.</div>
    </div>
  </div>

  <div class="section" id="book">
    <p class="section-title">Reserve your spot</p>
    <div class="booking-form">
      <div class="form-row">
        <div class="form-group">
          <label class="form-label">Your name</label>
          <input class="form-input" id="fname" type="text" placeholder="e.g. Priya Sharma" />
        </div>
        <div class="form-group">
          <label class="form-label">WhatsApp number</label>
          <input class="form-input" id="fphone" type="tel" placeholder="+91 98765 43210" />
        </div>
      </div>
      <div class="form-row">
        <div class="form-group">
          <label class="form-label">Workshop</label>
          <select class="form-input" id="fworkshop">
            <option value="">Choose a workshop</option>
            <option>Bouquet making</option>
            <option>Tote bag painting</option>
            <option>Cake decoration</option>
            <option>Candle making</option>
            <option>Terrarium building</option>
          </select>
        </div>
        <div class="form-group">
          <label class="form-label">Number of spots</label>
          <select class="form-input" id="fspots">
            <option>1 spot (just me)</option>
            <option>2 spots</option>
            <option>3 spots</option>
            <option>4+ spots (group)</option>
          </select>
        </div>
      </div>
      <div class="form-group" style="margin-bottom:0;">
        <label class="form-label">Anything you'd like us to know? (optional)</label>
        <textarea class="form-input" id="fnote" rows="2" placeholder="e.g. celebrating a birthday, first time doing anything creative..."></textarea>
      </div>
      <button class="submit-btn" id="submit-btn" onclick="submitBooking()">Send booking request →</button>
      <div class="success-msg" id="success-msg">
        🎉 Woohoo! We've got your request. You'll hear from us on WhatsApp within 24 hours. See you soon!
      </div>
    </div>
  </div>

  <footer>
    <p class="brand">🌸 Weekend Workshops Hyderabad</p>
    <p>Creative weekend workshops · Hyderabad · Summer 2025</p>
    <p style="margin-top:0.25rem; font-size:12px; color:#88877f;">Made with love for curious, creative humans who need a slow, joyful Saturday.</p>
    <div class="contact-links">
      <a href="https://wa.me/917995276651" class="contact-chip" target="_blank">📱 WhatsApp: 7995276651</a>
      <span class="contact-chip">✉️ Email coming soon</span>
      <span class="contact-chip">📍 Hyderabad</span>
    </div>
  </footer>

</div>

<script>
  function submitBooking() {
    const name = document.getElementById('fname').value.trim();
    const phone = document.getElementById('fphone').value.trim();
    const workshop = document.getElementById('fworkshop').value;
    if (!name || !phone || !workshop) {
      alert('Please fill in your name, phone number, and choose a workshop.');
      return;
    }
    document.getElementById('success-msg').style.display = 'block';
    const btn = document.getElementById('submit-btn');
    btn.disabled = true;
    btn.style.opacity = '0.5';
    btn.textContent = 'Request sent!';
  }
</script>
</body>
</html>
