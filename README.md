<!DOCTYPE html>
<html lang="bn">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover" />
  <title>Health Friend BD — বাংলা স্বাস্থ্য সহকারী</title>
  <meta name="description" content="বাংলা ভাষায় সাধারণ স্বাস্থ্য পরামর্শ — বিনামূল্যে, সহজ ও ভদ্র টোনে। জরুরি হলে ৯৯৯ বা ১৬২৬৩-এ যোগাযোগ করুন।" />

  <!-- Font -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+Bengali:wght@400;600;700&display=swap" rel="stylesheet">

  <style>
    :root{
      --bg:#0f172a;       /* slate-900 */
      --card:#111827;     /* gray-900 */
      --muted:#94a3b8;    /* slate-400 */
      --text:#e5e7eb;     /* gray-200 */
      --accent:#22d3ee;   /* cyan-400 */
      --accent-2:#a78bfa; /* violet-400 */
      --success:#34d399;  /* emerald-400 */
    }
    *{box-sizing:border-box}
    html,body{
      margin:0; padding:0;
      font-family:"Noto Sans Bengali",system-ui,-apple-system,Segoe UI,Roboto,Helvetica,Arial,sans-serif;
      background:var(--bg); color:var(--text);
      -webkit-text-size-adjust:100%; /* iOS zoom glitch fix */
    }

    a{color:var(--accent); text-decoration:none}

    .container{max-width:1100px; margin:0 auto; padding:clamp(12px,3vw,24px)}
    header{
      display:flex; align-items:center; justify-content:space-between; gap:16px;
      padding:12px 0;
    }
    .brand{display:flex; align-items:center; gap:10px; font-weight:700;
      font-size:clamp(18px,3.2vw,28px)}
    .brand .dot{width:10px;height:10px;border-radius:999px;
      background:linear-gradient(135deg,var(--accent),var(--accent-2))}

    .hero{
      display:grid; grid-template-columns:1.2fr 1fr; gap:clamp(14px,2.8vw,24px);
      align-items:center; padding: 12px 0 8px;
    }
    @media (max-width: 900px){
      .hero{grid-template-columns:1fr}
    }

    .card{
      background:linear-gradient(180deg,#0b1220,#0a0f1a);
      border:1px solid #1f2937; border-radius:16px; padding:clamp(14px,3vw,20px);
      box-shadow:0 10px 30px rgba(0,0,0,.35)
    }
    .pill{display:inline-block;background:#0b2a32;color:#8af3ff;
      padding:6px 10px;border-radius:999px;border:1px solid #164e63;font-size:12px;letter-spacing:.2px}
    h1{margin:.2em 0 .4em; font-size:clamp(26px,5vw,44px); line-height:1.15}
    p.lead{color:var(--muted); font-size:clamp(15px,2.5vw,18px)}

    .grid{display:grid; grid-template-columns:repeat(3,1fr); gap:clamp(10px,2vw,16px)}
    @media (max-width:900px){ .grid{grid-template-columns:1fr} }

    .feature{background:#0b1020; border:1px solid #1e293b; padding:16px; border-radius:14px}
    .feature h3{margin:4px 0 8px; font-size:18px}

    .notice{display:flex; gap:12px; align-items:flex-start;
      background:#20140f; border:1px solid #4a1d09; color:#ffd7ae;
      padding:12px 14px; border-radius:12px; margin-top:12px}
    .notice strong{color:#ffb86b}

    footer{margin:32px 0 80px; color:var(--muted); font-size:14px}
    .footer-grid{display:grid; grid-template-columns:1fr 1fr; gap:16px}
    @media (max-width:700px){ .footer-grid{grid-template-columns:1fr} }

    /* Safe-area for notches (iPhone etc.) */
    .safe{padding-left:env(safe-area-inset-left); padding-right:env(safe-area-inset-right)}
  </style>

  <!-- ✅ Chatbase embed (তোমার আইডি আছে—এটাই রাখো) -->
  <script>
  (function(){
    if(!window.chatbase || window.chatbase("getState")!=="initialized"){
      window.chatbase=(...args)=>{(window.chatbase.q=window.chatbase.q||[]).push(args)};
      window.chatbase=new Proxy(window.chatbase,{get(t,p){if(p==="q")return t.q; return(...a)=>t(p,...a)}});
    }
    const onLoad=function(){
      const s=document.createElement("script");
      s.src="https://www.chatbase.co/embed.min.js";
      s.id="qh-QBSpTeK3Yu7CCsAA6D";   /* ← তোমার দেওয়া আইডি */
      s.domain="www.chatbase.co";
      document.body.appendChild(s);
    };
    if(document.readyState==="complete"){onLoad()} else {window.addEventListener("load",onLoad)}
  })();
  </script>

  <!-- (ঐচ্ছিক) Botpress embed – ভবিষ্যতে চাইলে ব্যবহার করো
  <script src="https://cdn.botpress.cloud/webchat/v2.2/inject.js"></script>
  <script src="https://mediafiles.botpress.cloud/<BOT_ID>/webchat/v2.2/config.js"></script>
  -->
</head>

<body>
  <div class="container safe">
    <header>
      <div class="brand"><span class="dot"></span> Health Friend BD</div>
      <!-- আগের 'চ্যাট শুরু করুন' বাটনটি ইচ্ছাকৃতভাবে সরানো হলো ।
           এখন শুধু Chatbase-এর কালো ফ্লোটিং বাটন থাকবে। -->
    </header>

    <section class="hero">
      <div>
        <span class="pill">বাংলা স্বাস্থ্য সহকারী · ফ্রি</span>
        <h1>প্রতিদিনের ছোটখাটো অসুখে দ্রুত, সহজ ও ভদ্র পরামর্শ।</h1>
        <p class="lead">
          আমি ডাক্তার নই—আমি শুধু সাধারণ তথ্য দিই। উপসর্গ গুরুতর হলে অবশ্যই চিকিৎসকের পরামর্শ নিন।
          জরুরি অবস্থায় ৯৯৯ অথবা স্বাস্থ্য বাতায়ন ১৬২৬৩-এ কল করুন।
        </p>

        <div class="grid" style="margin-top:16px">
          <div class="feature"><h3>🤧 ঠান্ডা/কাশি</h3><p class="lead">গরম পানি, ভাপ; শ্বাসকষ্টে দ্রুত চিকিৎসক।</p></div>
          <div class="feature"><h3>🌡️ জ্বর</h3><p class="lead">ORS/পানি; ৩ দিনের বেশি হলে পরীক্ষা করুন।</p></div>
          <div class="feature"><h3>🍲 পেটের সমস্যা</h3><p class="lead">পরিষ্কার পানি, হালকা খাবার; শিশুতে সতর্কতা।</p></div>
        </div>

        <div class="notice">
          <div>⚠️</div>
          <div><strong>দ্রষ্টব্য:</strong> এখানে কোনো ওষুধ/ডোজ দেওয়া হয় না—এটি কেবল সচেতনতার সহায়ক।</div>
        </div>
      </div>

      <div class="card">
        <h3 style="margin-top:0">কীভাবে ব্যবহার করবেন?</h3>
        <ol>
          <li>ডান–নিচে যে <b>কালো চ্যাট বাটন</b> দেখা যাবে, সেটি চাপুন।</li>
          <li>বাংলায় প্রশ্ন লিখুন — যেমন “আমার ঠান্ডা লেগেছে, কী করব?”</li>
          <li>পরামর্শ পড়ে দেখুন; গুরুতর হলে চিকিৎসকের শরণাপন্ন হোন।</li>
        </ol>
        <p style="color:var(--muted);margin-top:8px">
          হোমস্ক্রিনে যুক্ত করতে ব্রাউজারের মেনু → <span style="font-family:ui-monospace">Add to Home Screen</span>.
        </p>
      </div>
    </section>

    <footer>
      <div class="footer-grid">
        <div><strong>প্রাইভেসি</strong><br>এই সাইট ব্যক্তিগত তথ্য সংরক্ষণ করে না; লেখা কনটেন্ট Chatbase-এ পাঠানো হয় উত্তরের জন্য।</div>
        <div><strong>যোগাযোগ</strong><br>শাফি ফান টিভি — <a href="mailto:shafifuntv@gmail.com">shafifuntv@gmail.com</a></div>
      </div>
    </footer>
  </div>

  <script>
    // (ঐচ্ছিক) যদি হেডারে ভবিষ্যতে কোনো কাস্টম বাটন যোগ করে Chatbase খুলতে চাও,
    // এই ফাংশনটা কল করলেই বেশিরভাগ ক্ষেত্রে কাজ করবে:
    window.openChatbase = function(){
      // কিছু থিমে Chatbase ওপেন API না থাকলে লঞ্চার বাটনে কৃত্রিম ক্লিক পাঠাই
      const possible = [
        '[class*="chatbase"] button',
        'button[id*="chatbase"]',
        'iframe[src*="chatbase"]'
      ];
      for (const sel of possible){
        const el = document.querySelector(sel);
        if (el){ el.click(); break; }
      }
      if (window.chatbase) { try { window.chatbase('open'); } catch(e){} }
    };

    // Mobile polish
    // 1) iOS Safari address bar shrink glitch fallback
    document.documentElement.style.setProperty('--vh', window.innerHeight * 0.01 + 'px');
    window.addEventListener('resize', () => {
      document.documentElement.style.setProperty('--vh', window.innerHeight * 0.01 + 'px');
    });
  </script>
</body>
</html>

