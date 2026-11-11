# gakere-consultation-company
a ecommerce website
html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Gakere Consultation Company | IT Solutions in Kenya</title>
<meta name="description" content="Gakere Consultation Company: software development, networking, hardware & software upgrades, electrical maintenance, computer tutoring, diagnostics and IT consultation.">
<style>
  :root{
    --navy:#0b1f3a;
    --blue:#1565d8;
    --cyan:#18c1d8;
    --light:#f4f7fb;
    --text:#1d2733;
    --muted:#5b6b7c;
    --white:#fff;
  }
  *{box-sizing:border-box;margin:0;padding:0}
  html{scroll-behavior:smooth}
  body{font-family:"Segoe UI",Roboto,Arial,sans-serif;color:var(--text);line-height:1.6;background:var(--white)}
  a{text-decoration:none;color:inherit}
  .container{width:min(1120px,92%);margin:0 auto}

  /* Header */
  header{position:sticky;top:0;z-index:50;background:var(--navy);color:var(--white);box-shadow:0 2px 12px rgba(0,0,0,.25)}
  .nav{display:flex;align-items:center;justify-content:space-between;padding:14px 0}
  .logo{font-weight:800;font-size:1.2rem;letter-spacing:.5px}
  .logo span{color:var(--cyan)}
  nav ul{display:flex;gap:24px;list-style:none}
  nav a{font-size:.95rem;opacity:.9;transition:.2s}
  nav a:hover{color:var(--cyan);opacity:1}
  .menu-btn{display:none;background:none;border:0;color:#fff;font-size:1.8rem;cursor:pointer}

  /* Hero */
  .hero{background:linear-gradient(135deg,var(--navy) 0%,#123a73 60%,var(--blue) 100%);color:var(--white);padding:110px 0 100px;text-align:center}
  .hero h1{font-size:clamp(2rem,5vw,3.4rem);line-height:1.15;margin-bottom:16px}
  .hero h1 span{color:var(--cyan)}
  .hero p{max-width:680px;margin:0 auto 32px;font-size:1.1rem;opacity:.92}
  .btn{display:inline-block;padding:13px 28px;border-radius:8px;font-weight:600;transition:.2s;border:2px solid transparent;cursor:pointer;font-size:1rem}
  .btn-primary{background:var(--cyan);color:var(--navy)}
  .btn-primary:hover{background:#4fd8ea}
  .btn-outline{border-color:var(--white);color:var(--white);margin-left:10px}
  .btn-outline:hover{background:var(--white);color:var(--navy)}

  /* Sections */
  section{padding:80px 0}
  .section-title{text-align:center;margin-bottom:50px}
  .section-title h2{font-size:2rem;color:var(--navy)}
  .section-title p{color:var(--muted);margin-top:8px}
  .section-title .bar{width:60px;height:4px;background:var(--cyan);margin:14px auto 0;border-radius:2px}
  .alt{background:var(--light)}

  /* About */
  .about{display:grid;grid-template-columns:1.2fr 1fr;gap:40px;align-items:center}
  .about p{margin-bottom:14px;color:var(--muted)}
  .stats{display:grid;grid-template-columns:1fr 1fr;gap:16px}
  .stat{background:var(--navy);color:var(--white);padding:26px;border-radius:12px;text-align:center}
  .stat strong{display:block;font-size:1.8rem;color:var(--cyan)}
  .stat span{font-size:.9rem;opacity:.85}

  /* Services */
  .grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:24px}
  .card{background:var(--white);border-radius:14px;padding:30px 26px;box-shadow:0 4px 18px rgba(11,31,58,.08);transition:.25s;border-top:4px solid var(--cyan)}
  .card:hover{transform:translateY(-6px);box-shadow:0 10px 26px rgba(11,31,58,.15)}
  .card .icon{font-size:2.2rem;margin-bottom:12px}
  .card h3{color:var(--navy);margin-bottom:8px;font-size:1.1rem}
  .card p{color:var(--muted);font-size:.95rem}

  /* Why us */
  .why{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:22px}
  .why div{text-align:center;padding:20px}
  .why .num{width:54px;height:54px;line-height:54px;border-radius:50%;background:var(--blue);color:#fff;font-weight:700;font-size:1.2rem;margin:0 auto 12px}
  .why h4{color:var(--navy);margin-bottom:6px}
  .why p{color:var(--muted);font-size:.93rem}

  /* Contact */
  .contact{display:grid;grid-template-columns:1fr 1.2fr;gap:40px}
  .info-box{background:var(--navy);color:var(--white);padding:36px;border-radius:14px}
  .info-box h3{margin-bottom:18px;color:var(--cyan)}
  .info-item{margin-bottom:18px}
  .info-item small{display:block;opacity:.65;text-transform:uppercase;letter-spacing:1px;font-size:.72rem}
  .info-item a:hover{color:var(--cyan)}
  form{background:var(--white);padding:32px;border-radius:14px;box-shadow:0 4px 18px rgba(11,31,58,.1)}
  label{display:block;font-weight:600;font-size:.9rem;margin-bottom:5px;color:var(--navy)}
  input,select,textarea{width:100%;padding:12px 14px;border:1px solid #cdd6e0;border-radius:8px;font-size:1rem;font-family:inherit;margin-bottom:16px}
  input:focus,select:focus,textarea:focus{outline:2px solid var(--cyan);border-color:var(--cyan)}
  textarea{min-height:110px;resize:vertical}
  form .btn{width:100%;border:0;background:var(--blue);color:#fff}
  form .btn:hover{background:#0f4fb0}
  .note{font-size:.8rem;color:var(--muted);margin-top:10px;text-align:center}

  /* Footer */
  footer{background:var(--navy);color:rgba(255,255,255,.8);text-align:center;padding:26px 0;font-size:.9rem}

  /* WhatsApp float */
  .wa{position:fixed;right:20px;bottom:20px;background:#25d366;color:#fff;width:58px;height:58px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:1.7rem;box-shadow:0 4px 14px rgba(0,0,0,.3);z-index:60}

  @media(max-width:820px){
    .menu-btn{display:block}
    nav ul{display:none;position:absolute;top:100%;left:0;right:0;background:var(--navy);flex-direction:column;gap:0;padding:10px 4%}
    nav ul.open{display:flex}
    nav li{padding:12px 0;border-bottom:1px solid rgba(255,255,255,.08)}
    .about,.contact{grid-template-columns:1fr}
    .btn-outline{margin:12px 0 0}
    section{padding:60px 0}
  }
</style>
</head>
<body>

<header>
  <div class="container nav">
    <a href="#home" class="logo">GAKERE <span>CONSULTATION</span></a>
    <button class="menu-btn" id="menuBtn" aria-label="Toggle menu">&#9776;</button>
    <nav>
      <ul id="menu">
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#services">Services</a></li>
        <li><a href="#why">Why Us</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </div>
</header>

<section class="hero" id="home">
  <div class="container">
    <h1>Smart IT Solutions for <span>Every Need</span></h1>
    <p>From software development and networking to hardware upgrades, electrical maintenance and computer training, Gakere Consultation Company is your one-stop partner for all IT-related queries.</p>
    <a href="#contact" class="btn btn-primary">Get a Free Consultation</a>
    <a href="#services" class="btn btn-outline">Our Services</a>
  </div>
</section>

<section id="about">
  <div class="container">
    <div class="section-title">
      <h2>About Us</h2>
      <div class="bar"></div>
    </div>
    <div class="about">
      <div>
        <p>Gakere Consultation Company handles every kind of IT-related query for individuals, schools, small businesses and organisations. Whether your network is acting up, your computer is slow, or you want to learn to code, we deliver practical, reliable and affordable solutions.</p>
        <p>We combine technical skill with clear communication, so you always understand what is being done and why.</p>
      </div>
      <div class="stats">
        <div class="stat"><strong>9+</strong><span>IT Services</span></div>
        <div class="stat"><strong>100%</strong><span>Client Focus</span></div>
        <div class="stat"><strong>Fast</strong><span>Response Time</span></div>
        <div class="stat"><strong>Quality</strong><span>Guaranteed Work</span></div>
      </div>
    </div>
  </div>
</section>

<section id="services" class="alt">
  <div class="container">
    <div class="section-title">
      <h2>Our Services</h2>
      <p>Everything IT, under one roof</p>
      <div class="bar"></div>
    </div>
    <div class="grid">
      <div class="card"><div class="icon">&#128187;</div><h3>Software Development</h3><p>Custom websites, apps and business software built to fit your exact needs.</p></div>
      <div class="card"><div class="icon">&#127760;</div><h3>Networking &amp; Troubleshooting</h3><p>Setup, repair and troubleshooting of wired and wireless networks, Wi-Fi and internet connectivity.</p></div>
      <div class="card"><div class="icon">&#128295;</div><h3>Hardware &amp; Software Upgrades</h3><p>Boost your computer's speed and lifespan with RAM, SSD, OS and software upgrades.</p></div>
      <div class="card"><div class="icon">&#9889;</div><h3>Basic Electrical Maintenance</h3><p>Safe basic electrical repairs, wiring checks and maintenance for homes and offices.</p></div>
      <div class="card"><div class="icon">&#127891;</div><h3>Computer Tutoring</h3><p>Hands-on lessons in computer basics, Microsoft Office, internet use and digital skills.</p></div>
      <div class="card"><div class="icon">&#128214;</div><h3>Programming Tutoring</h3><p>Learn Python, JavaScript, HTML/CSS, Java, C++ and more, from beginner to advanced.</p></div>
      <div class="card"><div class="icon">&#128269;</div><h3>System Diagnostics</h3><p>Thorough computer diagnostics to find and fix hardware, software and performance faults.</p></div>
      <div class="card"><div class="icon">&#128736;</div><h3>System Support</h3><p>Ongoing technical support, updates, virus removal and maintenance to keep you running.</p></div>
      <div class="card"><div class="icon">&#128172;</div><h3>IT Consultation</h3><p>Expert advice on technology choices, infrastructure and digital strategy for your needs.</p></div>
    </div>
  </div>
</section>

<section id="why">
  <div class="container">
    <div class="section-title">
      <h2>Why Choose Us</h2>
      <div class="bar"></div>
    </div>
    <div class="why">
      <div><div class="num">1</div><h4>Skilled &amp; Versatile</h4><p>One team covering software, hardware, networks and training.</p></div>
      <div><div class="num">2</div><h4>Affordable Pricing</h4><p>Fair, transparent rates with no hidden charges.</p></div>
      <div><div class="num">3</div><h4>Quick Turnaround</h4><p>Prompt response and efficient fixes that save you downtime.</p></div>
      <div><div class="num">4</div><h4>Friendly Support</h4><p>Clear explanations in plain language, before and after the job.</p></div>
    </div>
  </div>
</section>

<section id="contact" class="alt">
  <div class="container">
    <div class="section-title">
      <h2>Contact Us</h2>
      <p>Tell us what you need and we'll get back to you</p>
      <div class="bar"></div>
    </div>
    <div class="contact">
      <div class="info-box">
        <h3>Get In Touch</h3>
        <div class="info-item"><small>Contact Person</small>Gakere John</div>
        <div class="info-item"><small>Phone / WhatsApp</small><a href="tel:+254717375573">0717 375 573</a></div>
        <div class="info-item"><small>Email</small><a href="mailto:gakerejohn933@gmail.com">gakerejohn933@gmail.com</a></div>
        <a class="btn btn-primary" href="https://wa.me/254717375573?text=Hello%20Gakere%20Consultation%20Company%2C%20I%20need%20IT%20help." target="_blank" rel="noopener">Chat on WhatsApp</a>
      </div>

      <form id="contactForm">
        <label for="name">Your Name</label>
        <input type="text" id="name" required placeholder="Full name">

        <label for="phone">Phone Number</label>
        <input type="tel" id="phone" required placeholder="e.g. 07XX XXX XXX">

        <label for="service">Service Needed</label>
        <select id="service">
          <option>Software Development</option>
          <option>Networking Troubleshooting</option>
          <option>Hardware / Software Upgrade</option>
          <option>Electrical Maintenance &amp; Repair</option>
          <option>Computer Tutoring</option>
          <option>Programming Tutoring</option>
          <option>System Diagnostics</option>
          <option>System Support</option>
          <option>IT Consultation</option>
        </select>

        <label for="message">Message</label>
        <textarea id="message" required placeholder="Describe your problem or request..."></textarea>

        <button type="submit" class="btn">Send via WhatsApp</button>
        <p class="note">Your message opens in WhatsApp, ready to send to us.</p>
      </form>
    </div>
  </div>
</section>

<footer>
  <div class="container">
    &copy; <span id="year"></span> Gakere Consultation Company. All rights reserved.
  </div>
</footer>

<a class="wa" href="https://wa.me/254717375573" target="_blank" rel="noopener" aria-label="WhatsApp">&#128172;</a>

<script>
  document.getElementById('year').textContent = new Date().getFullYear();

  var menu = document.getElementById('menu');
  document.getElementById('menuBtn').addEventListener('click', function(){ menu.classList.toggle('open'); });
  menu.querySelectorAll('a').forEach(function(a){ a.addEventListener('click', function(){ menu.classList.remove('open'); }); });

  document.getElementById('contactForm').addEventListener('submit', function(e){
    e.preventDefault();
    var text = 'Hello Gakere Consultation Company,%0A' +
      'Name: ' + encodeURIComponent(document.getElementById('name').value) + '%0A' +
      'Phone: ' + encodeURIComponent(document.getElementById('phone').value) + '%0A' +
      'Service: ' + encodeURIComponent(document.getElementById('service').value) + '%0A' +
      'Message: ' + encodeURIComponent(document.getElementById('message').value);
    window.open('https://wa.me/254717375573?text=' + text, '_blank');
  });
</script>
</body>
</html>

Double-click the saved file and it opens as your website. To put it online, upload it to Netlify Drop (app.netlify.com/drop) and you get a live link right away.

de bug your code

I went through the code and found three bugs, and I’ve fixed them all in the updated index.html.

Numbered circles in “Why Choose Us” were misshapen. My CSS rule .why div also hit the number circles, adding extra padding that squashed the numbers. It is now .why > div.
Menu links scrolled too far. The sticky header covered the top of each section when you clicked a menu link. I added scroll-margin-top:60px to the section style.
The WhatsApp message was built in a fragile way. It mixed encoded and unencoded text, so some characters could break the message. It now builds the plain text first and encodes it once, so names with & or other symbols come through correctly.

If you’re pasting the code by hand instead of using the file, make these three replacements:

1. Find:

css
.why div{text-align:center;padding:20px}

Replace with:

css
.why > div{text-align:center;padding:20px}

2. Find:

css
section{padding:80px 0}

Replace with:

css
section{padding:80px 0;scroll-margin-top:60px}

3. Replace the whole contactForm submit script with:

js
document.getElementById('contactForm').addEventListener('submit', function(e){
  e.preventDefault();
  var text = 'Hello Gakere Consultation Company,\n' +
    'Name: ' + document.getElementById('name').value + '\n' +
    'Phone: ' + document.getElementById('phone').value + '\n' +
    'Service: ' + document.getElementById('service').value + '\n' +
    'Message: ' + document.getElementById('message').value;
  window.open('https://wa.me/254717375573?text=' + encodeURIComponent(text), '_blank');
});

If something specific is going wrong on your side, such as the page not opening, the menu not working, or the form not sending, tell me what you see and I’ll fix that too.

Index
Code
·HTML

write the code it one clen doc

Here is the complete, corrected code in one piece. Copy it all, paste it into Notepad, and save it as index.html (set “Save as type” to “All files”). Then double-click the file to open your website.

html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Gakere Consultation Company | IT Solutions in Kenya</title>
<meta name="description" content="Gakere Consultation Company: software development, networking, hardware & software upgrades, electrical maintenance, computer tutoring, diagnostics and IT consultation.">
<style>
  :root{
    --navy:#0b1f3a;
    --blue:#1565d8;
    --cyan:#18c1d8;
    --light:#f4f7fb;
    --text:#1d2733;
    --muted:#5b6b7c;
    --white:#fff;
  }
  *{box-sizing:border-box;margin:0;padding:0}
  html{scroll-behavior:smooth}
  body{font-family:"Segoe UI",Roboto,Arial,sans-serif;color:var(--text);line-height:1.6;background:var(--white)}
  a{text-decoration:none;color:inherit}
  .container{width:min(1120px,92%);margin:0 auto}

  /* Header */
  header{position:sticky;top:0;z-index:50;background:var(--navy);color:var(--white);box-shadow:0 2px 12px rgba(0,0,0,.25)}
  .nav{display:flex;align-items:center;justify-content:space-between;padding:14px 0}
  .logo{font-weight:800;font-size:1.2rem;letter-spacing:.5px}
  .logo span{color:var(--cyan)}
  nav ul{display:flex;gap:24px;list-style:none}
  nav a{font-size:.95rem;opacity:.9;transition:.2s}
  nav a:hover{color:var(--cyan);opacity:1}
  .menu-btn{display:none;background:none;border:0;color:#fff;font-size:1.8rem;cursor:pointer}

  /* Hero */
  .hero{background:linear-gradient(135deg,var(--navy) 0%,#123a73 60%,var(--blue) 100%);color:var(--white);padding:110px 0 100px;text-align:center}
  .hero h1{font-size:clamp(2rem,5vw,3.4rem);line-height:1.15;margin-bottom:16px}
  .hero h1 span{color:var(--cyan)}
  .hero p{max-width:680px;margin:0 auto 32px;font-size:1.1rem;opacity:.92}
  .btn{display:inline-block;padding:13px 28px;border-radius:8px;font-weight:600;transition:.2s;border:2px solid transparent;cursor:pointer;font-size:1rem}
  .btn-primary{background:var(--cyan);color:var(--navy)}
  .btn-primary:hover{background:#4fd8ea}
  .btn-outline{border-color:var(--white);color:var(--white);margin-left:10px}
  .btn-outline:hover{background:var(--white);color:var(--navy)}

  /* Sections */
  section{padding:80px 0;scroll-margin-top:60px}
  .section-title{text-align:center;margin-bottom:50px}
  .section-title h2{font-size:2rem;color:var(--navy)}
  .section-title p{color:var(--muted);margin-top:8px}
  .section-title .bar{width:60px;height:4px;background:var(--cyan);margin:14px auto 0;border-radius:2px}
  .alt{background:var(--light)}

  /* About */
  .about{display:grid;grid-template-columns:1.2fr 1fr;gap:40px;align-items:center}
  .about p{margin-bottom:14px;color:var(--muted)}
  .stats{display:grid;grid-template-columns:1fr 1fr;gap:16px}
  .stat{background:var(--navy);color:var(--white);padding:26px;border-radius:12px;text-align:center}
  .stat strong{display:block;font-size:1.8rem;color:var(--cyan)}
  .stat span{font-size:.9rem;opacity:.85}

  /* Services */
  .grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:24px}
  .card{background:var(--white);border-radius:14px;padding:30px 26px;box-shadow:0 4px 18px rgba(11,31,58,.08);transition:.25s;border-top:4px solid var(--cyan)}
  .card:hover{transform:translateY(-6px);box-shadow:0 10px 26px rgba(11,31,58,.15)}
  .card .icon{font-size:2.2rem;margin-bottom:12px}
  .card h3{color:var(--navy);margin-bottom:8px;font-size:1.1rem}
  .card p{color:var(--muted);font-size:.95rem}

  /* Why us */
  .why{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:22px}
  .why > div{text-align:center;padding:20px}
  .why .num{width:54px;height:54px;line-height:54px;border-radius:50%;background:var(--blue);color:#fff;font-weight:700;font-size:1.2rem;margin:0 auto 12px}
  .why h4{color:var(--navy);margin-bottom:6px}
  .why p{color:var(--muted);font-size:.93rem}

  /* Contact */
  .contact{display:grid;grid-template-columns:1fr 1.2fr;gap:40px}
  .info-box{background:var(--navy);color:var(--white);padding:36px;border-radius:14px}
  .info-box h3{margin-bottom:18px;color:var(--cyan)}
  .info-item{margin-bottom:18px}
  .info-item small{display:block;opacity:.65;text-transform:uppercase;letter-spacing:1px;font-size:.72rem}
  .info-item a:hover{color:var(--cyan)}
  form{background:var(--white);padding:32px;border-radius:14px;box-shadow:0 4px 18px rgba(11,31,58,.1)}
  label{display:block;font-weight:600;font-size:.9rem;margin-bottom:5px;color:var(--navy)}
  input,select,textarea{width:100%;padding:12px 14px;border:1px solid #cdd6e0;border-radius:8px;font-size:1rem;font-family:inherit;margin-bottom:16px}
  input:focus,select:focus,textarea:focus{outline:2px solid var(--cyan);border-color:var(--cyan)}
  textarea{min-height:110px;resize:vertical}
  form .btn{width:100%;border:0;background:var(--blue);color:#fff}
  form .btn:hover{background:#0f4fb0}
  .note{font-size:.8rem;color:var(--muted);margin-top:10px;text-align:center}

  /* Footer */
  footer{background:var(--navy);color:rgba(255,255,255,.8);text-align:center;padding:26px 0;font-size:.9rem}

  /* WhatsApp floating button */
  .wa{position:fixed;right:20px;bottom:20px;background:#25d366;color:#fff;width:58px;height:58px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:1.7rem;box-shadow:0 4px 14px rgba(0,0,0,.3);z-index:60}

  /* Mobile */
  @media(max-width:820px){
    .menu-btn{display:block}
    nav ul{display:none;position:absolute;top:100%;left:0;right:0;background:var(--navy);flex-direction:column;gap:0;padding:10px 4%}
    nav ul.open{display:flex}
    nav li{padding:12px 0;border-bottom:1px solid rgba(255,255,255,.08)}
    .about,.contact{grid-template-columns:1fr}
    .btn-outline{margin:12px 0 0}
    section{padding:60px 0}
  }
</style>
</head>
<body>

<!-- HEADER -->
<header>
  <div class="container nav">
    <a href="#home" class="logo">GAKERE <span>CONSULTATION</span></a>
    <button class="menu-btn" id="menuBtn" aria-label="Toggle menu">&#9776;</button>
    <nav>
      <ul id="menu">
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#services">Services</a></li>
        <li><a href="#why">Why Us</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </div>
</header>

<!-- HERO -->
<section class="hero" id="home">
  <div class="container">
    <h1>Smart IT Solutions for <span>Every Need</span></h1>
    <p>From software development and networking to hardware upgrades, electrical maintenance and computer training, Gakere Consultation Company is your one-stop partner for all IT-related queries.</p>
    <a href="#contact" class="btn btn-primary">Get a Free Consultation</a>
    <a href="#services" class="btn btn-outline">Our Services</a>
  </div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="container">
    <div class="section-title">
      <h2>About Us</h2>
      <div class="bar"></div>
    </div>
    <div class="about">
      <div>
        <p>Gakere Consultation Company handles every kind of IT-related query for individuals, schools, small businesses and organisations. Whether your network is acting up, your computer is slow, or you want to learn to code, we deliver practical, reliable and affordable solutions.</p>
        <p>We combine technical skill with clear communication, so you always understand what is being done and why.</p>
      </div>
      <div class="stats">
        <div class="stat"><strong>9+</strong><span>IT Services</span></div>
        <div class="stat"><strong>100%</strong><span>Client Focus</span></div>
        <div class="stat"><strong>Fast</strong><span>Response Time</span></div>
        <div class="stat"><strong>Quality</strong><span>Guaranteed Work</span></div>
      </div>
    </div>
  </div>
</section>

<!-- SERVICES -->
<section id="services" class="alt">
  <div class="container">
    <div class="section-title">
      <h2>Our Services</h2>
      <p>Everything IT, under one roof</p>
      <div class="bar"></div>
    </div>
    <div class="grid">
      <div class="card"><div class="icon">&#128187;</div><h3>Software Development</h3><p>Custom websites, apps and business software built to fit your exact needs.</p></div>
      <div class="card"><div class="icon">&#127760;</div><h3>Networking &amp; Troubleshooting</h3><p>Setup, repair and troubleshooting of wired and wireless networks, Wi-Fi and internet connectivity.</p></div>
      <div class="card"><div class="icon">&#128295;</div><h3>Hardware &amp; Software Upgrades</h3><p>Boost your computer's speed and lifespan with RAM, SSD, OS and software upgrades.</p></div>
      <div class="card"><div class="icon">&#9889;</div><h3>Basic Electrical Maintenance</h3><p>Safe basic electrical repairs, wiring checks and maintenance for homes and offices.</p></div>
      <div class="card"><div class="icon">&#127891;</div><h3>Computer Tutoring</h3><p>Hands-on lessons in computer basics, Microsoft Office, internet use and digital skills.</p></div>
      <div class="card"><div class="icon">&#128214;</div><h3>Programming Tutoring</h3><p>Learn Python, JavaScript, HTML/CSS, Java, C++ and more, from beginner to advanced.</p></div>
      <div class="card"><div class="icon">&#128269;</div><h3>System Diagnostics</h3><p>Thorough computer diagnostics to find and fix hardware, software and performance faults.</p></div>
      <div class="card"><div class="icon">&#128736;</div><h3>System Support</h3><p>Ongoing technical support, updates, virus removal and maintenance to keep you running.</p></div>
      <div class="card"><div class="icon">&#128172;</div><h3>IT Consultation</h3><p>Expert advice on technology choices, infrastructure and digital strategy for your needs.</p></div>
    </div>
  </div>
</section>

<!-- WHY US -->
<section id="why">
  <div class="container">
    <div class="section-title">
      <h2>Why Choose Us</h2>
      <div class="bar"></div>
    </div>
    <div class="why">
      <div><div class="num">1</div><h4>Skilled &amp; Versatile</h4><p>One team covering software, hardware, networks and training.</p></div>
      <div><div class="num">2</div><h4>Affordable Pricing</h4><p>Fair, transparent rates with no hidden charges.</p></div>
      <div><div class="num">3</div><h4>Quick Turnaround</h4><p>Prompt response and efficient fixes that save you downtime.</p></div>
      <div><div class="num">4</div><h4>Friendly Support</h4><p>Clear explanations in plain language, before and after the job.</p></div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact" class="alt">
  <div class="container">
    <div class="section-title">
      <h2>Contact Us</h2>
      <p>Tell us what you need and we'll get back to you</p>
      <div class="bar"></div>
    </div>
    <div class="contact">
      <div class="info-box">
        <h3>Get In Touch</h3>
        <div class="info-item"><small>Contact Person</small>Gakere John</div>
        <div class="info-item"><small>Phone / WhatsApp</small><a href="tel:+254717375573">0717 375 573</a></div>
        <div class="info-item"><small>Email</small><a href="mailto:gakerejohn933@gmail.com">gakerejohn933@gmail.com</a></div>
        <a class="btn btn-primary" href="https://wa.me/254717375573?text=Hello%20Gakere%20Consultation%20Company%2C%20I%20need%20IT%20help." target="_blank" rel="noopener">Chat on WhatsApp</a>
      </div>

      <form id="contactForm">
        <label for="name">Your Name</label>
        <input type="text" id="name" required placeholder="Full name">

        <label for="phone">Phone Number</label>
        <input type="tel" id="phone" required placeholder="e.g. 07XX XXX XXX">

        <label for="service">Service Needed</label>
        <select id="service">
          <option>Software Development</option>
          <option>Networking Troubleshooting</option>
          <option>Hardware / Software Upgrade</option>
          <option>Electrical Maintenance &amp; Repair</option>
          <option>Computer Tutoring</option>
          <option>Programming Tutoring</option>
          <option>System Diagnostics</option>
          <option>System Support</option>
          <option>IT Consultation</option>
        </select>

        <label for="message">Message</label>
        <textarea id="message" required placeholder="Describe your problem or request..."></textarea>

        <button type="submit" class="btn">Send via WhatsApp</button>
        <p class="note">Your message opens in WhatsApp, ready to send to us.</p>
      </form>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="container">
    &copy; <span id="year"></span> Gakere Consultation Company. All rights reserved.
  </div>
</footer>

<!-- FLOATING WHATSAPP BUTTON -->
<a class="wa" href="https://wa.me/254717375573" target="_blank" rel="noopener" aria-label="WhatsApp">&#128172;</a>

<script>
  // Footer year
  document.getElementById('year').textContent = new Date().getFullYear();

  // Mobile menu
  var menu = document.getElementById('menu');
  document.getElementById('menuBtn').addEventListener('click', function(){
    menu.classList.toggle('open');
  });
  menu.querySelectorAll('a').forEach(function(a){
    a.addEventListener('click', function(){ menu.classList.remove('open'); });
  });

  // Contact form -> WhatsApp
  document.getElementById('contactForm').addEventListener('submit', function(e){
    e.preventDefault();
    var text = 'Hello Gakere Consultation Company,\n' +
      'Name: ' + document.getElementById('name').value + '\n' +
      'Phone: ' + document.getElementById('phone').value + '\n' +
      'Service: ' + document.getElementById('service').value + '\n' +
      'Message: ' + document.getElementById('message').value;
    window.open('https://wa.me/254717375573?text=' + encodeURIComponent(text), '_blank');
  });
</script>
</body>
</html>
