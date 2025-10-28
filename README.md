<!DOCTYPE html>
<html lang="bn">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Health Friend BD — বাংলা স্বাস্থ্য সহকারী</title>
  <meta name="description" content="বাংলা ভাষায় সাধারণ স্বাস্থ্য পরামর্শ — বিনামূল্যে, সহজ ও ভদ্র টোনে। জরুরি হলে ৯৯৯ বা ১৬২৬৩-এ যোগাযোগ করুন।" />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+Bengali:wght@400;600;700&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg: #0f172a;          /* slate-900 */
      --card: #111827;        /* gray-900 */
      --muted: #94a3b8;       /* slate-400 */
      --text: #e5e7eb;        /* gray-200 */
      --accent: #22d3ee;      /* cyan-400 */
      --accent-2: #a78bfa;    /* violet-400 */
      --success: #34d399;     /* emerald-400 */
      --warn: #fbbf24;        /* amber-400 */
      --danger: #fb7185;      /* rose-400 */
    }
    * { box-sizing: border-box; }
    html, body { margin:0; padding:0; font-family: "Noto Sans Bengali", system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, sans-serif; background: var(--bg); color: var(--text); }
    a { color: var(--accent); text-decoration: none; }
    .container { max-width: 1100px; margin: 0 auto; padding: 24px; }
    header { display:flex; align-items:center; justify-content:space-between; gap:16px; padding: 16px 0; }
    .brand { display:flex; align-items:center; gap:12px; font-weight:700; font-size: clamp(20px, 3vw, 28px); }
    .brand .dot { width:10px; height:10px; border-radius:999px; background: linear-gradient(135deg, var(--accent), var(--accent-2)); display:inline-block; }
    .cta { display:inline-flex; align-items:center; gap:8px; background: linear-gradient(135deg, var(--accent), var(--accent-2)); color:#001016; font-weight:700; border:none; padding:10px 14px; border-radius:14px; cursor:pointer; }
    .hero { display:grid; grid-template-columns: 1.2fr 1fr; gap:24px; align-items:center; padding: 20px 0 8px; }
    @media (max-width: 900px){ .hero{ grid-template-columns: 1fr; } }
    .card { background: linear-gradient(180deg, #0b1220, #0a0f1a); border:1px solid #1f2937; border-radius: 16px; padding: 20px; box-shadow: 0 10px 30px rgba(0,0,0,.35); }
    .pill { display:inline-block; background:#0b2a32; color:#8af3ff; padding:6px 10px; border-radius:999px; border:1px solid #164e63; font-size:12px; letter-spacing:.2px; }
    h1 { margin:.2em 0 .4em; font-size: clamp(28px, 5vw, 44px); line-height:1.15; }
    p.lead { color: var(--muted); font-size: clamp(15px, 2.5vw, 18px); }
    .grid { display:grid; grid-template-columns: repeat(3, 1fr); gap:16px; }
    @media (max-width: 900px){ .grid{ grid-template-columns: 1fr; } }
    .feature { background: #0b1020; border:1px solid #1e293b; padding:16px; border-radius:14px; }
    .feature h3{ margin:4px 0 8px; font-size:18px; }
    .badge { font-size: 12px; color:#0b1220; background: var(--success); padding:3px 8px; border-radius:999px; font-weight:700; }
    .notice { display:flex; gap:12px; align-items:flex-start; background:#20140f; border:1px solid #4a1d09; color:#ffd7ae; padding:12px 14px; border-radius:12px; margin-top:12px; }
    .notice strong{ color:#ffb86b; }
    footer{ margin: 32px 0 80px; color: var(--muted); font-size:14px; }
    .footer-grid{ display:grid; grid-template-columns: 1fr 1fr; gap:16px; }
    @media (max-width: 700px){ .footer-grid{ grid-template-columns: 1fr; } }
    .kbd { font-family: ui-monospace, SFMono-Regular, Menlo, monospace; font-size: 12px; background:#0b1020; border:1px solid #233044; padding:2px 6px; border-radius:6px; }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="brand"><span class="dot"></span> Health Friend BD</div>
      <button class="cta" onclick="window.botpress && window.botpress.open()">চ্যাট শুরু করুন</button>
    </header>

    <section class="hero">
      <div>
        <span class="pill">বাংলা স্বাস্থ্য সহকারী · ফ্রি</span>
        <h1>প্রতিদিনের ছোটখাটো অসুখে দ্রুত, সহজ ও ভদ্র পরামর্শ।</h1>
        <p class="lead">আমি ডাক্তার নই — আমি শুধু সাধারণ তথ্য দিই। আপনার উপসর্গ গুরুতর হলে বা ভালো না হলে অবশ্যই কাছের চিকিৎসকের পরামর্শ নিন। জরুরি অবস্থায় ৯৯৯ অথবা স্বাস্থ্য বাতায়ন ১৬২৬৩-এ কল করুন।</p>
        <div class="grid" style="margin-top:16px;">
          <div class="feature">
            <h3>🤧 ঠান্ডা/কাশি</h3>
            <p class="lead">গরম পানি, ভাপ, বিশ্রাম — আর শ্বাসকষ্ট হলে চিকিৎসক।</p>
          </div>
          <div class="feature">
            <h3>🌡️ জ্বর</h3>
            <p class="lead">পানি/ORS, বিশ্রাম, ৩ দিনের বেশি হলে পরীক্ষা ও পরামর্শ।</p>
          </div>
          <div class="feature">
            <h3>🍲 পেটের সমস্যা</h3>
            <p class="lead">পরিষ্কার পানি, হালকা খাবার; শিশুদের ডায়রিয়ায় দ্রুত পদক্ষেপ।</p>
          </div>
        </div>
        <div class="notice">
          <div>⚠️</div>
          <div>
            <strong>দ্রষ্টব্য:</strong> এই সাইট থেকে কোনো ওষুধ, ডোজ বা রোগ নির্ণয় জানানো হয় না। এটি শুধু সাধারণ স্বাস্থ্য সচেতনতার সহায়ক।
          </div>
        </div>
      </div>

      <div class="card">
        <h3 style="margin-top:0">কীভাবে ব্যবহার করবেন?</h3>
        <ol>
          <li>ডান–নিচের <span class="kbd">চ্যাট</span> বোতাম চাপুন।</li>
          <li>বাংলায় প্রশ্ন লিখুন — যেমন “আমার ঠান্ডা লেগেছে, কী করব?”</li>
          <li>পরামর্শ পড়ে দেখুন; গুরুতর হলে চিকিৎসকের শরণাপন্ন হোন।</li>
        </ol>
        <p style="color:var(--muted);margin-top:8px">হোমস্ক্রিনে যুক্ত করতে ব্রাউজারের মেনু থেকে <span class="kbd">Add to Home Screen</span> বেছে নিন — অ্যাপের মতো ব্যবহার করুন।</p>
      </div>
    </section>

    <footer>
      <div class="footer-grid">
        <div>
          <strong>প্রাইভেসি</strong><br />
          এই সাইট ব্যক্তিগত তথ্য সংগ্রহ করে না। আপনি যা লিখবেন, তা শুধুই AI-কে উত্তরের জন্য পাঠানো হয়।
        </div>
        <div>
          <strong>যোগাযোগ</strong><br />
          শাফি ফান টিভি — ইমেইল: <a href="mailto:shafifuntv@gmail.com">shafifuntv@gmail.com</a>
        </div>
      </div>
    </footer>
  </div>

  <!-- Botpress Cloud Webchat Embed -->
  <!-- ❶ এই দুইটি স্ক্রিপ্ট অপরিবর্তিত রাখুন -->
  <script src="https://cdn.botpress.cloud/webchat/v2.2/inject.js"></script>
  <!-- ❷ নিচের লিঙ্কে <BOT_ID> অংশটি আপনার Botpress বট আইডি দিয়ে বদলান -->
  <script src="https://mediafiles.botpress.cloud/<BOT_ID>/webchat/v2.2/config.js"></script>

  <script>
    // ঐচ্ছিক: ওয়েবচ্যাট ওপেন করার সহজ API
    window.botpress = {
      open: function(){
        if (window.botpressWebChat) {
          window.botpressWebChat.sendEvent({ type: 'show' });
          window.botpressWebChat.sendEvent({ type: 'open' });
        }
      }
    };
  </script>
</body>
</html>
