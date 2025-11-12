# Web-Development-Part-3
Chris Brown Music Website 
This website was purposely created for music purposes
This website is viewed as an opportunity for chris brown fans to have access to concerts tours and listen to music 
Joyce Bila Music Website 
https://github.com/youngjbila1-pixel/Web-Development-Part-3.git
<img width="1330" height="630" alt="image" src="https://github.com/user-attachments/assets/0fb393e2-bf2f-462e-a8e0-0b183258589c" />
<img width="1323" height="628" alt="image" src="https://github.com/user-attachments/assets/d1efec53-f5b5-482c-be7f-30b5f3b511b9" />
<img width="1333" height="636" alt="image" src="https://github.com/user-attachments/assets/7283fa77-133a-48f9-8a70-6b498fd6ac91" />
<img width="1330" height="640" alt="image" src="https://github.com/user-attachments/assets/6e272e02-81f0-438c-9596-9ac1740150d2" />

<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Chris Brown — Official (Demo)</title>
  <meta name="description" content="Fan/demo site for Chris Brown — albums, videos, tour dates, contact." />
  <style>
    :root{
      --accent:#1db954;
      --dark:#0f1724;
      --muted:#94a3b8;
      --glass: rgba(255,255,255,0.06);
      font-family: Inter, system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial;
    }
    *{box-sizing:border-box}
    body{margin:0;background:linear-gradient(180deg,#05060a 0%, #0b1220 100%);color:#e6eef8;min-height:100vh}

    header{display:flex;align-items:center;justify-content:space-between;padding:18px 28px;background:transparent;position:sticky;top:0;z-index:40}
    .logo{display:flex;gap:12px;align-items:center}
    .logo img{width:46px;height:46px;border-radius:6px;object-fit:cover}
    nav{display:flex;gap:18px;align-items:center}
    nav a{color:var(--muted);text-decoration:none;font-weight:600}

    .burger{display:none;background:transparent;border:0;color:var(--muted)}

    .hero{display:grid;grid-template-columns:1fr 420px;gap:30px;padding:48px 6vw;align-items:center}
    .hero-left h1{font-size:clamp(28px,5vw,48px);margin:0 0 12px}
    .hero-left p{color:var(--muted);max-width:60ch}
    .cta{margin-top:18px}
    .btn{background:var(--accent);border:0;padding:10px 18px;border-radius:10px;color:#041018;font-weight:700;cursor:pointer}

    .card{background:linear-gradient(180deg, rgba(255,255,255,0.03), rgba(255,255,255,0.01));padding:16px;border-radius:14px;backdrop-filter: blur(6px)}

    /* Albums grid */
    .albums{padding:24px 6vw}
    .grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(210px,1fr));gap:18px}
    .album img{width:100%;height:220px;object-fit:cover;border-radius:12px}
    .album h4{margin:8px 0 4px}
    .album p{margin:0;color:var(--muted);font-size:14px}

    /* Gallery */
    .gallery{padding:24px 6vw}
    .gallery-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(160px,1fr));gap:12px}
    .gallery img{width:100%;height:160px;object-fit:cover;border-radius:10px}

    footer{padding:28px 6vw;border-top:1px solid rgba(255,255,255,0.03);display:flex;justify-content:space-between;align-items:center}

    /* Responsive */
    @media (max-width:920px){
      .hero{grid-template-columns:1fr;gap:20px;padding-top:20px}
      nav{display:none}
      .burger{display:inline-block}
    }

    /* simple modal/lightbox */
    .lightbox{position:fixed;inset:0;display:none;align-items:center;justify-content:center;background:rgba(0,0,0,0.7);z-index:80}
    .lightbox.open{display:flex}
    .lightbox img{max-width:92%;max-height:86%;border-radius:8px}

    /* small utility */
    .muted{color:var(--muted)}
    .row{display:flex;gap:12px;align-items:center}
  </style>
</head>
<body>
  <header>
    <div class="logo">
      <!-- Replace the src with a portrait image of Chris Brown or your chosen artwork -->
      <img src="https://images.unsplash.com/photo-1511671782779-c97d3d27a1d4?auto=format&fit=crop&w=600&q=60" alt="Artist Logo">
      <div>
        <div style="font-weight:800">Chris Brown</div>
        <div class="muted" style="font-size:12px">Official (demo)</div>
      </div>
    </div>

    <nav>
      <a href="#albums">Albums</a>
      <a href="#videos">Media</a>
      <a href="#tour">Tour</a>
      <a href="#contact">Contact</a>
    </nav>

    <button class="burger" aria-label="open menu" id="openMenu">☰</button>
  </header>

  <main>
    <section class="hero">
      <div class="hero-left">
        <h1>Chris Brown — Music, videos & tour</h1>
        <p>Welcome to the demo fan site. Stream the latest singles, explore albums, watch videos, and find upcoming tour dates. Replace the placeholder images and audio links with official assets you have permission to use.</p>
        <div class="cta row">
          <button class="btn" id="playSingle">Play Featured Single</button>
          <a href="#albums" class="muted" style="align-self:center">Browse albums ↓</a>
        </div>

        <div style="margin-top:18px" class="card">
          <strong>Featured single: "Demo Groove"</strong>
          <div class="muted">Released: 2025</div>
          <!-- audio: replace src with your audio file or streaming link -->
          <audio id="audioPlayer" controls preload="none" style="width:100%;margin-top:10px">
            <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
            Your browser does not support the audio element.
          </audio>
        </div>
      </div>

      <aside class="card" style="padding:12px;display:flex;flex-direction:column;gap:12px;align-items:center">
        <img src="https://images.unsplash.com/photo-1517841905240-472988babdf9?auto=format&fit=crop&w=800&q=60" alt="cover art" style="width:100%;border-radius:10px;max-width:360px;height:420px;object-fit:cover">
        <div style="text-align:center">
          <div style="font-weight:700">New Album — "Midnight Vibes"</div>
          <div class="muted">Available everywhere • 12 tracks</div>
        </div>
      </aside>
    </section>

    <section id="albums" class="albums">
      <h2 style="margin:0 0 12px 0;padding-left:6vw">Albums</h2>
      <div class="grid">
        <!-- Album cards: swap images with album art files -->
        <article class="album card">
          <img src="https://images.unsplash.com/photo-1526178610405-1c2a6f1e8b5b?auto=format&fit=crop&w=800&q=60" alt="Album 1">
          <h4>Midnight Vibes</h4>
          <p class="muted">2025 • 12 tracks</p>
        </article>

        <article class="album card">
          <img src="https://images.unsplash.com/photo-1508214751196-bcfd4ca60f91?auto=format&fit=crop&w=800&q=60" alt="Album 2">
          <h4>Rhythm & Motion</h4>
          <p class="muted">2023 • 10 tracks</p>
        </article>

        <article class="album card">
          <img src="https://images.unsplash.com/photo-1485579149621-3123dd979885?auto=format&fit=crop&w=800&q=60" alt="Album 3">
          <h4>Sunset Echoes</h4>
          <p class="muted">2021 • 11 tracks</p>
        </article>

        <article class="album card">
          <img src="https://images.unsplash.com/photo-1511671782779-c97d3d27a1d4?auto=format&fit=crop&w=800&q=60" alt="Album 4">
          <h4>Back To The Beat</h4>
          <p class="muted">2019 • 14 tracks</p>
        </article>
      </div>
    </section>

    <section id="videos" class="gallery">
      <h2 style="margin:0 0 12px 0;padding-left:6vw">Media & Videos</h2>
      <div class="gallery-grid">
        <!-- Replace images with video thumbnail images and link to YouTube or mp4 files -->
        <div class="card"><img src="https://images.unsplash.com/photo-1492684223066-81342ee5ff30?auto=format&fit=crop&w=800&q=60" alt="video 1" data-large="https://images.unsplash.com/photo-1492684223066-81342ee5ff30?auto=format&fit=crop&w=1600&q=60"></div>
        <div class="card"><img src="https://images.unsplash.com/photo-1485579149621-3123dd979885?auto=format&fit=crop&w=800&q=60" alt="video 2" data-large="https://images.unsplash.com/photo-1485579149621-3123dd979885?auto=format&fit=crop&w=1600&q=60"></div>
        <div class="card"><img src="https://images.unsplash.com/photo-1517841905240-472988babdf9?auto=format&fit=crop&w=800&q=60" alt="video 3" data-large="https://images.unsplash.com/photo-1517841905240-472988babdf9?auto=format&fit=crop&w=1600&q=60"></div>
        <div class="card"><img src="https://images.unsplash.com/photo-1526178610405-1c2a6f1e8b5b?auto=format&fit=crop&w=800&q=60" alt="video 4" data-large="https://images.unsplash.com/photo-1526178610405-1c2a6f1e8b5b?auto=format&fit=crop&w=1600&q=60"></div>
      </div>
    </section>

    <section id="tour" class="albums" style="padding-top:6px">
      <h2 style="margin:0 0 12px 0;padding-left:6vw">Tour Dates</h2>
      <div class="card" style="padding:14px;margin:0 6vw;display:flex;flex-direction:column;gap:8px">
        <div class="row"><strong>Dec 05, 2025</strong> — The Forum, Los Angeles • <span class="muted">Tickets: Sold Out</span></div>
        <div class="row"><strong>Dec 14, 2025</strong> — O2 Arena, London • <span class="muted">Tickets Available</span></div>
        <div class="row"><strong>Jan 10, 2026</strong> — Accor Arena, Paris • <span class="muted">Pre-sale</span></div>
        <div style="margin-top:10px" class="muted">Note: These dates in this demo are illustrative. Replace with official tour data from the artist's management.</div>
      </div>
    </section>

    <section id="contact" style="padding:28px 6vw">
      <h2 style="margin:0 0 12px 0">Contact & Press</h2>
      <div class="card" style="display:grid;grid-template-columns:1fr 320px;gap:18px;padding:18px">
        <form id="contactForm">
          <label style="display:block;margin-bottom:8px">Name<br><input required name="name" placeholder="Your name" style="width:100%;padding:8px;margin-top:6px;border-radius:8px;border:0" /></label>
          <label style="display:block;margin-bottom:8px">Email<br><input required name="email" type="email" placeholder="you@example.com" style="width:100%;padding:8px;margin-top:6px;border-radius:8px;border:0" /></label>
          <label style="display:block;margin-bottom:8px">Message<br><textarea required name="message" placeholder="Press / booking enquiry" rows="5" style="width:100%;padding:8px;margin-top:6px;border-radius:8px;border:0"></textarea></label>
          <div style="margin-top:8px"><button class="btn" type="submit">Send message</button></div>
        </form>

        <div>
          <h4>Management</h4>
          <p class="muted">Email: management@example.com</p>
          <h4>Social</h4>
          <div class="row" style="margin-top:8px">
            <a class="muted" href="#">YouTube</a>
            <a class="muted" href="#">Instagram</a>
            <a class="muted" href="#">Twitter/X</a>
          </div>
        </div>
      </div>
    </section>

  </main>

  <footer>
    <div class="muted">© 2025 Chris Brown — demo site. All rights reserved (demo)</div>
    <div class="row"><a class="muted" href="#">Privacy</a><a class="muted" href="#">Credits</a></div>
  </footer>

  <!-- Lightbox -->
  <div id="lightbox" class="lightbox" role="dialog" aria-hidden="true">
    <img src="" alt="preview">
  </div>

  <script>
    // Basic interactions: open image lightbox, play audio on featured button, simple mobile menu
    document.querySelectorAll('.gallery img, .album img').forEach(img => {
      img.addEventListener('click', e => {
        const lb = document.getElementById('lightbox');
        const preview = lb.querySelector('img');
        preview.src = e.currentTarget.dataset.large || e.currentTarget.src;
        lb.classList.add('open');
        lb.setAttribute('aria-hidden','false');
      });
    });
    document.getElementById('lightbox').addEventListener('click', e => {
      if(e.target === e.currentTarget){
        e.currentTarget.classList.remove('open');
        e.currentTarget.setAttribute('aria-hidden','true');
      }
    });

    const audio = document.getElementById('audioPlayer');
    document.getElementById('playSingle').addEventListener('click', ()=>{
      if(audio.paused){audio.play();}else{audio.pause();}
    });

    // contact form: demo submit
    document.getElementById('contactForm').addEventListener('submit', e=>{
      e.preventDefault();
      alert('Thanks! This is a demo: the form would be sent to your server or email service.');
      e.target.reset();
    });

    // mobile menu (very small demo)
    document.getElementById('openMenu').addEventListener('click', ()=>{
      alert('Mobile menu: add a slide-out or off-canvas nav here.');
    });
  </script>
</body>
</html>

📋 Pages Overview
🏠 Homepage (index.html)
Hero section with responsive background images
👤 About (about.html)
Biography section with statistics
🎪 Tour (tour.html)
Upcoming concert dates
🖼️ Gallery (gallery.html)
Responsive image grid
📞 Contact (contact.html)
Contact form with validation
💼 Enquiries (enquiry.html)
Business enquiry form
🎨 Customization
Colors
:root {
    --primary-color: #ff6b6b;
    --secondary-color: #4a235a;
    --background-dark: #2c3e50;
    --text-light: #ffffff;
    --text-dark: #333333;
}
⚙️ Technologies Used
HTML5 - Semantic markup and structure

CSS3 - Modern styling with Flexbox/Grid

JavaScript - Interactive functionality

Responsive Design - Mobile-first approach

SEO Optimization - Meta tags and schema

Web Accessibility - ARIA labels and keyboard navigation
Different enquiry types
📱 Browser Support
Browser	Version	Support
Chrome	60+	✅ Full
Firefox	55+	✅ Full
Safari	12+	✅ Full
Edge	79+	✅ Full
Opera	50+	✅ Full
🚀 Performance Features
Lazy Loading - Images load as needed
🔧 JavaScript Features
Main Functionality (js/main.js)
- Smooth scrolling navigation
- Mobile menu toggle
- Accordion functionality
- News content loading
- Search functionality
- Music Player (js/music-player.js)
- - Audio playback controls
- Track switching
- Progress tracking
- Volume control
- Gallery (js/gallery.js)
- - Lightbox implementation
- Image lazy loading
- Keyboard navigation
- Forms (js/forms.js)
- - Form validation
- Real-time error messages
- AJAX form submission
- Success/error handling
- Touch gestures for mobile
- 📈 SEO Implementation
On-Page SEO
Proper title tags and meta descriptions

Semantic HTML structure

Image alt text optimization

Clean URL structure

Internal linking
Technical SEO
robots.txt file

sitemap.xml generation

Mobile-friendly design

Fast loading times

SSL/HTTPS ready
🌐 Social Media Integration
Open Graph meta tags

Twitter Card support

Social sharing buttons

Social media icons
📧 Form Handling
Contact Form
Name, email, message type, and message fields

HTML5 validation

JavaScript enhancement

Success/error feedback
Enquiry Form
Business-focused fields

Phone number validation

Enquiry type categorization

Professional response system
🎵 Music Integration
Audio Features
HTML5 audio player

Custom controls

Track listing

Progress bars

Volume controls
Music Data
const discography = [
    {
        title: "Breezy",
        year: 2022,
        type: "album",
        tracks: 23,
        streams: "2.5B"
    }
    // ... more albums
];
🖼️ Image Gallery Features
Responsive grid layout

Lightbox modal

Image captions

Navigation controls

Mobile-optimized touch gestures
🔒 Security Features
Form validation

XSS protection

Secure form handling

Input sanitization
📊 Analytics Ready
Google Analytics integration ready:
<!-- Add to head section -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
LICENSE
MIT License

Copyright (c) 2024 Chris Brown Official Website

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
Image Optimization - Responsive images with WebP fallbacks

Minified CSS/JS - Optimized file sizes

Fast Loading - Optimized hero images

Caching - Proper cache headers
Professional response system
Message type selection

Success/error handling
Lightbox functionality

Performance and studio photos
Interactive map integration

Ticket booking information
Interactive accordion for career timeline

Achievement highlights
Latest news section

Featured music player

Album releases grid
