# Recreate minimal deliverables for direct upload without unzipping a big package.
from pathlib import Path
from textwrap import dedent
from PIL import Image, ImageDraw, ImageFont
import zipfile

out_root = Path("/mnt/data/hbd_ready")
assets = out_root / "assets"
assets.mkdir(parents=True, exist_ok=True)

index_html = dedent("""
<!DOCTYPE html>
<html lang="bn">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Health Information BD</title>
  <link rel="icon" href="assets/favicon.png" />
  <meta property="og:image" content="assets/og-image.png" />
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gray-50 text-gray-800">
  <header class="bg-blue-700 text-white p-4 text-center text-2xl font-bold">Health Information BD</header>
  <main class="max-w-6xl mx-auto p-6">
    <h1 class="text-4xl font-bold text-center text-blue-800">স্বাগতম!</h1>
    <p class="text-center mt-2 text-gray-600">বাংলায় একটি পূর্ণ স্বাস্থ্য তথ্য ওয়েবসাইট</p>
    <section class="my-12 text-center">
      <h2 class="text-3xl font-semibold text-blue-700 mb-4">AI চ্যাট</h2>
      <iframe id="aiFrame" src="about:blank" class="w-full max-w-3xl h-[600px] mx-auto border rounded-xl shadow"></iframe>
      <p class="text-sm text-gray-500 mt-2">AI URL বসাতে index.html-এ const AI_URL আপডেট করুন।</p>
    </section>
  </main>
  <footer class="bg-white border-t text-center py-6">
    <p class="text-gray-600 text-lg">© <span id="year"></span> Health Information BD</p>
    <h2 class="mt-2 text-2xl md:text-3xl font-extrabold text-blue-900">এই AI তৈরি করেছেন — শাহারিয়ার হক শাফি</h2>
  </footer>
  <script>
    const AI_URL = 'https://your-ai-url.example.com'; // এখানে তোমার Botpress/AI লিংক বসাও
    const f=document.getElementById('aiFrame'); if(f) f.src = AI_URL;
    document.getElementById('year').innerText = new Date().getFullYear();
  </script>
</body>
</html>
""")

(out_root / "index.html").write_text(index_html, encoding="utf-8")

# Create simple placeholder images for assets
def make_png(path, text, size=(512, 320)):
    from PIL import Image, ImageDraw, ImageFont
    img = Image.new("RGB", size, (240,248,255))
    d = ImageDraw.Draw(img)
    try:
        font = ImageFont.truetype("DejaVuSans.ttf", 28)
    except:
        font = ImageFont.load_default()
    w,h = d.textsize(text, font=font)
    d.rectangle([(0,0),(size[0]-1,size[1]-1)], outline=(59,130,246), width=3)
    d.text(((size[0]-w)//2,(size[1]-h)//2), text, fill=(29,78,216), font=font)
    img.save(path)

make_png(assets / "og-image.png", "Health Information BD")
make_png(assets / "favicon.png", "H", size=(128,128))

# Also create a small zip with just the assets for uploading as a folder
assets_zip = Path("/mnt/data/hbd_assets.zip")
with zipfile.ZipFile(assets_zip, "w", zipfile.ZIP_DEFLATED) as z:
    for p in assets.rglob("*"):
        z.write(p, p.relative_to(out_root))  # keep folder name 'assets'

str(out_root / "index.html"), str(assets_zip)
