<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Durairaj — Aspiring Ethical Hacker & Cybersecurity Enthusiast</title>
  <meta name="description" content="Durairaj — B.E. Cyber Security student. Portfolio showcasing skills, education and contact details." />
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&family=Roboto+Mono:wght@300;400;600&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg:#08090b;
      --card:#0f1113;
      --muted:#9aa6b2;
      --neon:#00ffd5;
      --neon-2:#36a3ff;
      --glass: rgba(255,255,255,0.03);
    }
    *{box-sizing:border-box}
    html,body{height:100%;}
    body{
      margin:0;
      font-family: 'Poppins', system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial;
      background: radial-gradient(1200px 600px at 10% 10%, rgba(54,163,255,0.04), transparent),
                  linear-gradient(180deg, #040405 0%, #07080a 100%);
      color:#dbe7ee;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      overflow-y:auto;
    }

    /* container */
    .container{max-width:1100px;margin:36px auto;padding:28px}
    header{display:flex;align-items:center;justify-content:space-between;gap:20px}
    .brand{display:flex;align-items:center;gap:14px}
    .logo{
      width:48px;height:48px;border-radius:10px;background:linear-gradient(135deg,var(--neon),var(--neon-2));
      display:flex;align-items:center;justify-content:center;font-weight:700;color:#041018;box-shadow:0 6px 25px rgba(54,163,255,0.06);
    }
    nav{display:flex;gap:12px;align-items:center}
    nav a{color:var(--muted);text-decoration:none;padding:8px 12px;border-radius:8px;font-weight:600;font-size:14px}
    nav a:hover{color:var(--neon-2);background:rgba(255,255,255,0.02)}

    .toggle{display:flex;align-items:center;gap:8px}
    .theme-btn{background:transparent;border:1px solid rgba(255,255,255,0.04);padding:8px;border-radius:10px;cursor:pointer;color:var(--muted)}

    /* hero */
    .hero{display:grid;grid-template-columns:1fr 340px;gap:28px;margin-top:30px;align-items:center}
    .intro{background:linear-gradient(180deg, rgba(255,255,255,0.02), transparent);padding:28px;border-radius:14px;box-shadow:0 10px 30px rgba(3,6,8,0.6)}
    h1{margin:0;font-size:28px;letter-spacing:0.4px}
    .title{color:var(--neon);font-family:'Roboto Mono',monospace;margin-top:8px}
    p.tag{color:var(--muted);margin-top:14px}
    .cta{margin-top:18px}
    .btn{background:linear-gradient(90deg,var(--neon),var(--neon-2));color:#041018;border:none;padding:10px 16px;border-radius:10px;font-weight:700;cursor:pointer;box-shadow:0 8px 25px rgba(54,163,255,0.12)}
    .ghost{background:transparent;border:1px solid rgba(255,255,255,0.06);color:var(--muted);padding:10px 14px;border-radius:10px;margin-left:12px}

    /* profile */
    .profile-card{background:linear-gradient(180deg,var(--card), rgba(255,255,255,0.02));padding:20px;border-radius:14px;text-align:center}
    .avatar{width:180px;height:180px;border-radius:14px;margin:0 auto;object-fit:cover;border:4px solid rgba(54,163,255,0.08);box-shadow:0 10px 40px rgba(54,163,255,0.05)}
    .name{margin-top:12px;font-weight:700}
    .meta{color:var(--muted);font-size:13px;margin-top:6px}

    /* sections */
    section{margin-top:22px}
    .card{background:var(--glass);padding:18px;border-radius:12px;border:1px solid rgba(255,255,255,0.02)}
    .section-title{display:flex;align-items:center;gap:12px}
    .section-title h3{margin:0}
    .skills{display:grid;grid-template-columns:repeat(2,1fr);gap:12px;margin-top:12px}
    .skill{background:transparent;padding:12px;border-radius:10px}
    .skill .label{display:flex;justify-content:space-between;color:var(--muted);font-weight:600}
    .bar{height:10px;background:rgba(255,255,255,0.04);border-radius:999px;margin-top:8px;overflow:hidden}
    .bar > i{display:block;height:100%;background:linear-gradient(90deg,var(--neon),var(--neon-2));border-radius:999px;transform-origin:left}

    .timeline{display:flex;flex-direction:column;gap:12px;margin-top:12px}
    .t-item{display:flex;gap:12px;align-items:flex-start}
    .dot{width:12px;height:12px;border-radius:50%;background:linear-gradient(90deg,var(--neon),var(--neon-2));margin-top:6px}
    .t-content{background:rgba(255,255,255,0.02);padding:10px;border-radius:10px}

    .portfolio-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:14px;margin-top:12px}
    .placeholder{display:flex;flex-direction:column;align-items:center;justify-content:center;padding:30px;border-radius:10px;border:1px dashed rgba(255,255,255,0.04);min-height:140px;color:var(--muted)}

    .contact-grid{display:grid;grid-template-columns:1fr 1fr;gap:14px;margin-top:12px}
    .contact-list{display:flex;flex-direction:column;gap:8px}
    .contact-item{display:flex;gap:12px;align-items:center;color:var(--muted)}
    .form{display:flex;flex-direction:column;gap:12px}
    .form input,.form textarea{background:transparent;border:1px solid rgba(255,255,255,0.04);padding:12px;border-radius:8px;color:inherit}
    .form textarea{min-height:120px}

    footer{margin-top:28px;text-align:center;color:var(--muted);font-size:13px;padding:20px}

    /* terminal effect */
    .terminal{background:#030407;padding:14px;border-radius:10px;font-family:'Roboto Mono',monospace;color:var(--muted);font-size:13px}
    .cursor{display:inline-block;width:8px;height:18px;background:var(--neon);margin-left:6px;animation:blink 1s infinite}
    @keyframes blink{0%,50%{opacity:1}51%,100%{opacity:0}}

    /* responsive */
    @media (max-width:900px){
      .hero{grid-template-columns:1fr;}
      .profile-card{order:-1}
      .skills{grid-template-columns:1fr}
      .portfolio-grid{grid-template-columns:1fr}
      .contact-grid{grid-template-columns:1fr}
      nav{display:none}
    }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="brand">
        <div class="logo">D</div>
        <div>
          <div style="font-weight:700">Durairaj</div>
          <div style="font-size:12px;color:var(--muted)">B.E. Cyber Security — Mahendra Engineering College</div>
        </div>
      </div>
      <nav aria-label="Main Navigation">
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#skills">Skills</a>
        <a href="#education">Education</a>
        <a href="#portfolio">Portfolio</a>
        <a href="#contact">Contact</a>
      </nav>
      <div class="toggle">
        <button class="theme-btn" id="toggleTheme" title="Toggle light/dark">Toggle</button>
      </div>
    </header>

    <main>
      <section id="home" class="hero">
        <div class="intro card">
          <h1>Durairaj — <span class="title">Aspiring Ethical Hacker & Cybersecurity Enthusiast</span></h1>
          <p class="tag">Exploring the world of cybersecurity, one tool at a time.</p>

          <div style="margin-top:18px" class="terminal">
            <div>&gt; echo "Learning: nmap, wireshark, burpsuite, metasploit"</div>
            <div>&gt; echo "Goal: Become a certified ethical hacker" <span class="cursor"></span></div>
          </div>

          <div class="cta">
            <button class="btn" onclick="document.getElementById('contact').scrollIntoView({behavior:'smooth'})">Contact Me</button>
            <button class="ghost" onclick="document.getElementById('about').scrollIntoView({behavior:'smooth'})">Learn More</button>
          </div>
        </div>

        
      </section>

      <section id="about">
        <div class="card">
          <div class="section-title">
            <h3>About</h3>
          </div>
          <p style="color:var(--muted);margin-top:8px">I'm currently a 2nd-year Cyber Security student at Mahendra Engineering College. I'm passionate about ethical hacking and exploring new tools and technologies in the field of cybersecurity. My goal is to become a certified ethical hacker and security professional.</p>
        </div>
      </section>

      <section id="skills">
        <div class="card">
          <div class="section-title"><h3>Skills</h3></div>
          <div class="skills">
            <div class="skill">
              <div class="label"><span>Python</span><span>85%</span></div>
              <div class="bar"><i style="width:85%"></i></div>
            </div>
            <div class="skill">
              <div class="label"><span>C++ / C</span><span>70%</span></div>
              <div class="bar"><i style="width:70%"></i></div>
            </div>
            <div class="skill">
              <div class="label"><span>Java / PHP / JS</span><span>60%</span></div>
              <div class="bar"><i style="width:60%"></i></div>
            </div>
            <div class="skill">
              <div class="label"><span>Web (HTML/CSS/Flutter/PHP)</span><span>65%</span></div>
              <div class="bar"><i style="width:65%"></i></div>
            </div>
            <div class="skill">
              <div class="label"><span>Networking (CCNA)</span><span>60%</span></div>
              <div class="bar"><i style="width:60%"></i></div>
            </div>
            <div class="skill">
              <div class="label"><span>Scripting (Bash/Shell)</span><span>55%</span></div>
              <div class="bar"><i style="width:55%"></i></div>
            </div>
          </div>
        </div>
      </section>

      

      <section id="portfolio">
        <div class="card">
          <div class="section-title"><h3>Portfolio (Projects)</h3></div>
          <div class="portfolio-grid">
            <div class="placeholder">
              <h4>Coming Soon</h4>
              <p style="max-width:260px;color:var(--muted)">Exciting projects are on the way as I continue learning and building my cybersecurity skills.</p>
            </div>
            <div class="placeholder">
              <h4>Stay Tuned</h4>
              <p style="max-width:260px;color:var(--muted)">Follow my GitHub to see projects as I publish them.</p>
            </div>
          </div>
        </div>
      </section>

      <section id="contact">
        <div class="card">
          <div class="section-title"><h3>Contact</h3></div>
          <div class="contact-grid">
            <div class="contact-list">
              <div class="contact-item"><strong>📧 Email:</strong>&nbsp;<span style="color:var(--muted)">jaasimbasha23@gmail.com</span></div>
              <div class="contact-item"><strong>📱 Phone:</strong>&nbsp;<span style="color:var(--muted)">9345069552</span></div>
              
              
              
            </div>
            <div>
              <form class="form" onsubmit="handleForm(event)">
                <input type="text" id="name" placeholder="Your name" required />
                <input type="email" id="email" placeholder="Your email" required />
                <input type="text" id="subject" placeholder="Subject" />
                <textarea id="message" placeholder="Message" required></textarea>
                <div style="display:flex;gap:8px">
                  <button class="btn" type="submit">Send Message</button>
                  <button type="button" class="ghost" onclick="mailtoFallback()">Email Me</button>
                </div>
              </form>
            </div>
          </div>
        </div>
      </section>

      <footer>
        © <span id="year"></span> Durairaj — Crafted with a passion for cybersecurity.
      </footer>
    </main>
  </div>

  <script>
    // set year
    document.getElementById('year').textContent = new Date().getFullYear();

    // simple theme toggle (keeps to session only)
    const toggle = document.getElementById('toggleTheme');
    toggle.addEventListener('click', ()=>{
      if(document.documentElement.style.getPropertyValue('--bg') === '#08090b'){
        // switch to light-ish
        document.documentElement.style.setProperty('--bg','#f6f7fb');
        document.body.style.background = '#f6f7fb';
        document.body.style.color = '#071019';
        document.querySelectorAll('.card').forEach(n=>n.style.border='1px solid rgba(7,16,25,0.04)');
      } else {
        document.documentElement.style.setProperty('--bg','#08090b');
        document.body.style.background = 'radial-gradient(1200px 600px at 10% 10%, rgba(54,163,255,0.04), transparent), linear-gradient(180deg, #040405 0%, #07080a 100%)';
        document.body.style.color = '#dbe7ee';
      }
    });

    // simple form handler: opens mailto with message; does not send server-side
    function handleForm(e){
      e.preventDefault();
      const name = document.getElementById('name').value.trim();
      const email = document.getElementById('email').value.trim();
      const subject = document.getElementById('subject').value.trim() || 'Contact from portfolio';
      const message = document.getElementById('message').value.trim();
      const body = encodeURIComponent(`Name: ${name}\nEmail: ${email}\n\n${message}`);
      const mail = `mailto:jaasimbasha23@gmail.com?subject=${encodeURIComponent(subject)}&body=${body}`;
      window.location.href = mail;
    }
    function mailtoFallback(){
      window.location.href = 'mailto:jaasimbasha23@gmail.com';
    }

    // small accessibility: follow hash links smoothly on load
    if(location.hash){
      const el = document.querySelector(location.hash);
      if(el) setTimeout(()=>el.scrollIntoView({behavior:'smooth'}),300);
    }
  </script>
</body>
</html>
