<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Krishna Chetan Portfolio</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
  <style>
    /* ========== VARIABLES ========== */
    :root{
      --bg-1: #0f2027;
      --bg-2: #203a43;
      --bg-3: #2c5364;
      --glass: rgba(255,255,255,0.06);
      --glass-2: rgba(255,255,255,0.03);
      --neon-green: #00e676;
      --neon-purple: #8e44ff;
      --neon-cyan: #00e5ff;
      --neon-gold: #ffd166;
      --accent-glow: 0 10px 40px rgba(0,230,118,0.07);
      --radius: 14px;
      --maxw: 1100px;
      --ease: cubic-bezier(.2,.9,.2,1);
    }

    /* ========== BASE ========== */
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      padding-top:72px;
      font-family:'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      color:#fff;
      background: linear-gradient(90deg,var(--bg-1),var(--bg-2),var(--bg-3));
      -webkit-font-smoothing:antialiased;
      overflow-x:hidden;
    }

    /* ========== NAV ========== */
    nav{
      position:fixed;
      top:0;left:0;width:100%;
      z-index:1200;
      display:flex;justify-content:center;align-items:center;
      padding:12px 20px;
      backdrop-filter: blur(8px);
      background: linear-gradient(90deg, rgba(0,0,0,0.55), rgba(0,0,0,0.25));
      border-bottom: 1px solid rgba(255,255,255,0.03);
    }
    nav a{
      color:#e6f7ef; text-decoration:none; margin:0 14px; font-weight:700; position:relative;
      padding:6px 2px;
      transition: transform .28s var(--ease), color .28s var(--ease);
      -webkit-tap-highlight-color: transparent;
    }
    /* underline animation */
    nav a::after{
      content:'';
      position:absolute;left:0;right:0;bottom:-6px;height:3px;border-radius:6px;
      background:linear-gradient(90deg,var(--neon-green),var(--neon-cyan));
      transform:scaleX(0); transform-origin:left;
      transition:transform .28s var(--ease), opacity .28s var(--ease);
      opacity:0;
    }
    nav a:hover{ color:var(--neon-green); transform:translateY(-2px) }
    nav a:hover::after{ transform:scaleX(1); opacity:1 }

    /* ========== FLOATING BG ELEMENTS ========== */
    .bg-shape{
      position:fixed; pointer-events:none; z-index:0; filter: blur(36px); opacity:.45;
      mix-blend-mode: screen;
      animation: floaty 12s infinite ease-in-out;
      border-radius:50%;
    }
    .bg-shape.x1{ width:320px; height:320px; left:-80px; top:20%; background: radial-gradient(circle at 30% 30%, rgba(0,230,118,0.18), transparent 45%); animation-duration:18s;}
    .bg-shape.x2{ width:260px; height:260px; right:-60px; top:5%; background: radial-gradient(circle at 60% 40%, rgba(142,68,255,0.12), transparent 45%); animation-duration:16s; animation-delay:2s}
    .bg-shape.x3{ width:180px; height:180px; right:10%; bottom:-30px; background: radial-gradient(circle at 50% 50%, rgba(0,229,255,0.12), transparent 45%); animation-duration:20s; animation-delay:3s}

    @keyframes floaty{
      0%{ transform: translateY(0px) translateX(0px) }
      50%{ transform: translateY(-18px) translateX(6px) }
      100%{ transform: translateY(0px) translateX(0px) }
    }

    /* ========== CONTAINER / SECTIONS ========== */
    .container{ max-width:var(--maxw); margin:0 auto; padding:0 20px; position:relative; z-index:10; }
    section{ padding:48px 0; }

    /* ========== HERO / PROFILE ========== */
    header{
      text-align:center; padding:48px 20px 36px; position:relative;
      display:flex;flex-direction:column;align-items:center;justify-content:center;
      gap:12px;
    }

    /* rotating gradient border */
    .avatar-wrap{
      --size:150px;
      width:var(--size); height:var(--size);
      display:grid; place-items:center;
      border-radius:999px;
      padding:6px;
      background: conic-gradient(from 0deg, var(--neon-green), var(--neon-cyan), var(--neon-purple), var(--neon-gold), var(--neon-green));
      animation: rotate-border 6s linear infinite;
      box-shadow: 0 6px 28px rgba(0,0,0,0.45), 0 6px 40px rgba(0,230,118,0.06);
    }
    @keyframes rotate-border{
      to { transform: rotate(360deg) }
    }

    .profile-image{
      width: calc(var(--size) - 16px);
      height: calc(var(--size) - 16px);
      border-radius:50%;
      object-fit:cover;
      background:linear-gradient(180deg, rgba(255,255,255,0.03), rgba(255,255,255,0.01));
      border-radius:50%;
      display:block;
      box-shadow: 0 8px 30px rgba(0,0,0,0.4);
      transition: transform .5s var(--ease), box-shadow .3s;
      transform-origin:center;
      outline: 2px solid rgba(255,255,255,0.02);
    }
    .profile-image:hover{ transform:translateY(-6px) scale(1.03); box-shadow: 0 22px 60px rgba(0,0,0,0.6) }

    header h1{
      font-size:2.4rem; margin:6px 0 0;
      background: linear-gradient(90deg, var(--neon-green), var(--neon-cyan), var(--neon-purple));
      -webkit-background-clip:text; background-clip:text; color:transparent;
      letter-spacing:0.6px;
    }
    header p{ margin:6px 0 6px; opacity:0.95; font-size:1rem; }

    /* ========== CARDS: GLASS ========== */
    .card{
      background: linear-gradient(180deg, rgba(255,255,255,0.03), rgba(255,255,255,0.02));
      border: 1px solid rgba(255,255,255,0.04);
      backdrop-filter: blur(8px) saturate(120%);
      border-radius: var(--radius);
      padding:20px;
      box-shadow: 0 8px 30px rgba(2,8,12,0.6);
      transition: transform .36s var(--ease), box-shadow .36s;
    }
    .card:hover{ transform: translateY(-8px); box-shadow: 0 18px 60px rgba(0,0,0,0.65); }

    .social-icons{ margin-top:12px; display:flex; align-items:center; gap:12px; justify-content:center }
    .social-icons a{
      display:inline-grid; place-items:center;
      width:44px;height:44px;border-radius:10px;
      background: linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
      border:1px solid rgba(255,255,255,0.03);
      box-shadow: 0 6px 20px rgba(0,0,0,0.5);
      transition: transform .28s var(--ease), box-shadow .28s, filter .28s;
      color:#fff; text-decoration:none; font-size:18px;
    }
    .social-icons a:hover{ transform:translateY(-6px) scale(1.08); box-shadow: 0 20px 40px rgba(0,230,118,0.12); filter: drop-shadow(0 8px 18px rgba(0,230,118,0.12)) }

    /* neon glows per icon */
    .social-icons a.linkedin:hover{ box-shadow: 0 12px 30px rgba(10,102,194,0.14) }
    .social-icons a.youtube:hover{ box-shadow: 0 12px 30px rgba(255,0,0,0.12) }
    .social-icons a.instagram:hover{ box-shadow: 0 12px 30px rgba(142,68,255,0.12) }
    .social-icons a.github:hover{ box-shadow: 0 12px 30px rgba(200,200,200,0.09) }

    /* ========== SECTION HEADINGS ========== */
    .section-header{
      display:flex; align-items:center; gap:12px; justify-content:space-between; margin-bottom:14px;
    }
    .section-header h2{
      margin:0; font-size:1.4rem; letter-spacing:0.3px;
      background: linear-gradient(90deg, rgba(255,255,255,0.92), rgba(255,255,255,0.7));
      -webkit-background-clip:text; background-clip:text; color:transparent;
    }

    /* ========== EDUCATION TIMELINE ========== */
    .edu-wrap{ display:grid; gap:12px }
    .edu-card{
      display:flex; gap:14px; align-items:flex-start;
      border-left: 4px solid transparent; padding:14px; transition: transform .36s var(--ease);
      background: linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
      border-radius:12px;
      transform-origin:left center;
    }
    .edu-card:hover{ transform: translateX(8px); background: linear-gradient(180deg, rgba(255,255,255,0.035), rgba(255,255,255,0.015)); }
    .edu-icon{
      min-width:44px; height:44px; border-radius:10px; display:grid; place-items:center;
      background: linear-gradient(135deg,var(--neon-cyan), var(--neon-purple));
      box-shadow: 0 8px 30px rgba(142,68,255,0.08);
      font-weight:700;
    }

    /* ========== ACHIEVEMENTS ========== */
    .award-grid{ display:grid; grid-template-columns: repeat(auto-fit,minmax(240px,1fr)); gap:12px; margin-top:8px }
    .award-card{
      padding:16px; border-radius:12px;
      background: linear-gradient(135deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
      border:1px solid rgba(255,255,255,0.03);
      transform-origin:center;
      animation: bounceIn .6s var(--ease);
    }
    @keyframes bounceIn{
      0%{ transform: translateY(18px) scale(.98); opacity:0 }
      60%{ transform: translateY(-6px) scale(1.01); opacity:1 }
      100%{ transform: translateY(0px) scale(1) }
    }

    /* shimmer effect */
    .shimmer{
      position:relative; overflow:hidden;
    }
    .shimmer::after{
      content:''; position:absolute; left:-120%; top:0; width:40%; height:100%;
      background: linear-gradient(90deg, transparent, rgba(255,255,255,0.04), transparent);
      transform: skewX(-18deg);
      animation: shimmer 2.2s infinite;
    }
    @keyframes shimmer{ to { left:120% } }

    /* ========== YOUTUBE CARD ========== */
    .youtube-wrap{ display:grid; gap:12px }
    .yt-embed{
      border-radius:12px; overflow:hidden; border:1px solid rgba(255,255,255,0.04);
      box-shadow: 0 10px 40px rgba(0,0,0,0.6);
      background: linear-gradient(180deg, rgba(0,0,0,0.5), rgba(0,0,0,0.45));
      transition: box-shadow .28s;
    }
    .yt-embed:hover{ box-shadow: 0 20px 60px rgba(0,230,118,0.08) }

    /* glowing outline */
    .yt-embed .glow{
      border-top: 4px solid transparent;
      background: linear-gradient(90deg, rgba(0,230,118,0.12), rgba(0,229,255,0.08), rgba(142,68,255,0.08));
    }

    /* ========== CONTACT FORM ========== */
    form label{ display:block; font-weight:600; margin-top:10px; opacity:.95 }
    input, textarea{
      background: linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
      border:1px solid rgba(255,255,255,0.03); color:#fff; outline:none;
      transition: box-shadow .22s, transform .22s;
    }
    input:focus, textarea:focus{
      box-shadow: 0 8px 36px rgba(0,230,118,0.08);
      transform: translateY(-3px);
    }
    .btn{
      display:inline-block; padding:10px 18px; margin-top:12px; cursor:pointer;
      border-radius:10px; border: none; font-weight:700;
      background: linear-gradient(90deg, var(--neon-green), var(--neon-cyan));
      color:#001; letter-spacing:0.3px;
      transition: transform .22s var(--ease), box-shadow .22s;
      box-shadow: 0 8px 30px rgba(0,230,118,0.12);
    }
    .btn:hover{ transform: translateY(-6px) scale(1.02); box-shadow: 0 22px 60px rgba(0,230,118,0.16); }

    /* success animation */
    .success-message{
      display:none; margin-top:10px; padding:10px; border-radius:8px; color:#08341b;
      background: linear-gradient(90deg, rgba(210,245,210,0.95), rgba(200,240,200,0.9));
      border:1px solid rgba(0,120,60,0.12);
    }

    /* ========== RESPONSIVE ========== */
    @media (max-width:820px){
      header h1{ font-size:1.8rem }
      .avatar-wrap{ --size:120px }
      .container{ padding:0 14px }
      .award-grid{ grid-template-columns: 1fr }
    }

    /* small utility */
    .muted{ color: rgba(255,255,255,0.72); font-size:0.95rem }
    a.ghost{ color:inherit; text-decoration:underline; opacity:.95 }
  </style>
</head>
<body>
  <!-- floating background shapes -->
  <div class="bg-shape x1"></div>
  <div class="bg-shape x2"></div>
  <div class="bg-shape x3"></div>

  <nav>
    <div class="container" style="display:flex;align-items:center;justify-content:center">
      <a href="#about">About</a>
      <a href="#education">Education</a>
      <a href="#awards">Achievements</a>
      <a href="#youtube">YouTube</a>
      <a href="#contact">Contact</a>
    </div>
  </nav>

  <header>
    <div class="avatar-wrap" aria-hidden="true">
      <!-- Replace the src filename if your service uses a different path -->
      <img src="https://res.cloudinary.com/dzfqapzbg/image/upload/v1754827179/WhatsApp_Image_2025-08-10_at_17.28.15_7d8e06c0_fgihvz.jpg" alt="Krishna Chetan" class="profile-image">
    </div>
    <h1>Krishna Chetan Paidimarri</h1>
    <p class="muted">ICT Student | Developer | Content Creator</p>

    <div style="margin-top:8px" class="social-icons">
      <a class="linkedin" href="https://www.linkedin.com/in/paidimarri-krishna-chetan" target="_blank" rel="noopener noreferrer" aria-label="LinkedIn"><i class="fab fa-linkedin"></i></a>
      <a class="youtube" href="https://www.youtube.com/@sastravibes" target="_blank" rel="noopener noreferrer" aria-label="YouTube"><i class="fab fa-youtube"></i></a>
      <a class="instagram" href="https://www.instagram.com/paidimarri_krishna_chetan" target="_blank" rel="noopener noreferrer" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
      <a class="github" href="https://github.com/chetan2007-k" target="_blank" rel="noopener noreferrer" aria-label="GitHub"><i class="fab fa-github"></i></a>
    </div>
  </header>

  <main class="container">
    <!-- ABOUT -->
    <section id="about">
      <div class="card">
        <div class="section-header">
          <h2>About Me</h2>
          <div class="muted">Passionate about building, teaching, and creating.</div>
        </div>
        <p>Hello! I am <strong>Krishna Chetan</strong>, an ICT student at SASTRA University. I enjoy exploring new technologies, building web solutions, and sharing knowledge through my YouTube channel <a href="https://www.youtube.com/@sastravibes" class="ghost" target="_blank" rel="noopener noreferrer">Sastra Vibes</a>.</p>
      </div>
    </section>

    <!-- EDUCATION -->
    <section id="education">
      <div class="card">
        <div class="section-header">
          <h2>Education</h2>
          <div class="muted">Academic timeline & skills</div>
        </div>
        <div class="edu-wrap">
          <div class="edu-card shimmer">
            <div class="edu-icon">S</div>
            <div>
              <h3 style="margin:0;color:var(--neon-green)">SASTRA University, Thanjavur</h3>
              <p class="muted" style="margin:6px 0"><strong>Degree:</strong> B.Tech in Information and Communication Technology (2024 – 2028)</p>
              <p style="margin:0"><strong>CGPA:</strong> 9.025 &nbsp; • &nbsp; <strong>Skills:</strong> C, C++</p>
            </div>
          </div>

          <div class="edu-card">
            <div class="edu-icon" style="background: linear-gradient(135deg,var(--neon-gold), var(--neon-green))">J</div>
            <div>
              <h3 style="margin:0;color:var(--neon-cyan)">Jaggaiahpet Residential College (JRC)</h3>
              <p class="muted" style="margin:6px 0"><strong>Course:</strong> Intermediate, MPC (2022 – 2024)</p>
              <p style="margin:0"><strong>Grade:</strong> 98.4%</p>
            </div>
          </div>

          <div class="edu-card">
            <div class="edu-icon" style="background: linear-gradient(135deg,var(--neon-purple), var(--neon-cyan))">C</div>
            <div>
              <h3 style="margin:0;color:var(--neon-purple)">CHEGU VIDYALAYAM EM HIGH SCHOOL</h3>
              <p class="muted" style="margin:6px 0"><strong>SSC</strong> – March 2022</p>
              <p style="margin:0"><strong>Grade:</strong> 95.83%</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- ACHIEVEMENTS -->
    <section id="awards">
      <div class="card">
        <div class="section-header">
          <h2>Achievements & Awards</h2>
          <div class="muted">Honors, scholarships & leadership</div>
        </div>

        <div class="award-grid">
          <div class="award-card shimmer">
            <h3 style="margin:0;color:var(--neon-gold)">Bharati Airtel Scholarship</h3>
            <p class="muted" style="margin-top:6px">Awarded for outstanding academic performance and leadership potential.</p>
          </div>

          <div class="award-card" style="background:linear-gradient(135deg, rgba(0,0,0,0.45), rgba(255,255,255,0.01));">
            <h3 style="margin:0;color:var(--neon-cyan)">Social Wellbeing Committee</h3>
            <p class="muted" style="margin-top:6px">Selected as a member to promote mental wellness and community engagement.</p>
          </div>

          <div class="award-card shimmer">
            <h3 style="margin:0;color:var(--neon-green)">Top Performer in Projects</h3>
            <p class="muted" style="margin-top:6px">Recognized for excellence in multiple technical and creative projects.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- YOUTUBE -->
    <section id="youtube">
      <div class="card">
        <div class="section-header">
          <h2>YouTube Channel</h2>
          <div class="muted">Latest upload (auto-updating)</div>
        </div>

        <div style="display:flex;gap:18px;flex-wrap:wrap;align-items:flex-start">
          <div style="min-width:140px;display:flex;flex-direction:column;align-items:center;gap:8px">
            <img src="https://yt3.ggpht.com/U-bb7zeG8MWXBo-4Qv30idLscgiSNGBgd2tS2NHhwNlD2ZJTix9PczKz0SvYAJp5g4ndh4Pj=s600-c-k-c0x00ffffff-no-rj-rp-mo" alt="Sastra Vibes" class="channel-image" style="width:100px;height:100px;border-radius:14px;border:3px solid rgba(255,0,0,0.08);box-shadow:0 12px 36px rgba(255,0,0,0.04)">
            <a href="https://www.youtube.com/@sastravibes" target="_blank" rel="noopener noreferrer" class="btn" style="padding:8px 14px;font-size:14px">Visit Channel</a>
            <div class="muted" style="margin-top:6px">Subscribers: <strong>1.50K </strong></div>
          </div>

          <div style="flex:1;min-width:280px" class="youtube-wrap">
            <div id="youtube-video" class="yt-embed glow" aria-live="polite">
              <!-- JS will insert iframe here -->
              <div style="padding:28px;text-align:center;color:rgba(255,255,255,0.6)">Loading latest video…</div>
            </div>
            <div style="margin-top:8px" class="stars muted" aria-hidden="true">
              <i class="fas fa-star" style="color:var(--neon-gold)"></i>
              <i class="fas fa-star" style="color:var(--neon-gold)"></i>
              <i class="fas fa-star" style="color:var(--neon-gold)"></i>
              <i class="fas fa-star" style="color:var(--neon-gold)"></i>
              <i class="fas fa-star-half-alt" style="color:var(--neon-gold)"></i>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact">
      <div class="card">
        <div class="section-header">
          <h2>Contact Me</h2>
          <div class="muted">Get in touch — I respond to students & collaborators</div>
        </div>

        <form id="contactForm" action="https://formsubmit.co/128014029@sastra.ac.in" method="POST" onsubmit="handleContactSubmit(event)">
          <input type="hidden" name="_captcha" value="false">
          <input type="hidden" name="_next" value="https://thankyou-page-link.com">
          <label for="name">Name:</label>
          <input id="name" name="name" required placeholder="Your full name">

          <label for="email">Email:</label>
          <input id="email" name="email" type="email" required placeholder="you@example.com">

          <label for="message">Message:</label>
          <textarea id="message" name="message" rows="5" required placeholder="How can I help?"></textarea>

          <button type="submit" class="btn">Send Message</button>
        </form>

        <div id="successMessage" class="success-message" role="status" aria-live="polite">
          ✅ Thank you! Your message has been sent.
        </div>
      </div>
    </section>

    <footer style="margin:36px 0 80px;text-align:center;color:rgba(255,255,255,0.78)">
      <small>&copy; 2025 Krishna Chetan Paidimarri. All rights reserved.</small>
    </footer>
  </main>

  <!-- ========== SCRIPTS ========== -->
  <script>
    /***********************************************
     *  Auto-updating latest YouTube video section
     *  - Replace 'YOUR_YOUTUBE_API_KEY' with your API key
     *  - CHANNEL_ID is your channel: UC33NV7XOrUtzLCcxLliy6Ug
     ***********************************************/
    (function(){
      const API_KEY = "YOUR_YOUTUBE_API_KEY"; // <-- PUT YOUR API KEY HERE
      const CHANNEL_ID = "UC33NV7XOrUtzLCcxLliy6Ug";
      const target = document.getElementById('youtube-video');

      // If no API key provided, show helpful fallback and keep current static video
      if(!API_KEY || API_KEY === "YOUR_YOUTUBE_API_KEY"){
        target.innerHTML = `
          <iframe width="100%" height="315" src="https://www.youtube.com/embed/NAuExe3UKGQ" frameborder="0" allowfullscreen style="display:block"></iframe>
          <div style="margin-top:8px;color:rgba(255,255,255,0.6);font-size:0.95rem">Tip: Add your YouTube API key in the script for auto-updating videos.</div>
        `;
        return;
      }

      // fetch latest video
      const url = \`https://www.googleapis.com/youtube/v3/search?key=\${API_KEY}&channelId=\${CHANNEL_ID}&part=snippet,id&order=date&maxResults=1&type=video\`;

      fetch(url)
        .then(r => r.json())
        .then(data => {
          if(!data || !data.items || data.items.length === 0){
            target.innerHTML = '<div style="padding:22px;text-align:center;color:rgba(255,255,255,0.6)">No videos found.</div>';
            return;
          }
          const videoId = data.items[0].id.videoId;
          const title = data.items[0].snippet.title || 'Latest video';
          // embed
          target.innerHTML = \`
            <iframe width="100%" height="360" src="https://www.youtube.com/embed/\${videoId}" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen title="\${escapeHtml(title)}" style="display:block"></iframe>
          \`;
        })
        .catch(err => {
          console.error('YouTube API error', err);
          target.innerHTML = '<div style="padding:22px;text-align:center;color:rgba(255,255,255,0.6)">Error loading latest video. Check API key & quota in Google Cloud Console.</div>';
        });

      function escapeHtml(str){ return String(str).replace(/[&<>"]/g, s => ({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;'}[s])); }
    })();

    /***********************************************
     * Contact form UX: show success message but still submit
     ***********************************************/
    function handleContactSubmit(e){
      // allow formsubmit.co to process normally, but show a local success message
      const msg = document.getElementById('successMessage');
      msg.style.display = 'block';
      // small animation
      msg.animate([{ opacity: 0 }, { opacity: 1 }], { duration: 420, easing: 'ease-out' });
      // allow normal form submission to continue (no preventDefault)
      // but we can scroll to the message
      setTimeout(()=>{ msg.scrollIntoView({behavior:'smooth', block:'center'}); }, 200);
    }

    /* Optional: small lazy animation for shimmering cards */
    document.addEventListener('DOMContentLoaded', ()=>{
      const shimmers = document.querySelectorAll('.shimmer');
      shimmers.forEach((el,i)=> el.style.animationDelay = (i*120)+'ms');
    });
  </script>
</body>
</html>
