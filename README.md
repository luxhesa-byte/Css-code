# Css-code
<style>
@import url('https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,500;1,400&family=Quicksand:wght@400;600;700&display=swap');
div[class*="badge"], div[class*="pronoun"], span[class*="pronoun"] { display: none !important; }
body, p, span, div, a { font-family: 'Quicksand', sans-serif !important; color: #ff80ab !important; text-shadow: 0 0 3px rgba(255, 255, 255, 0.8), 0 0 8px rgba(186, 225, 255, 0.5) !important; }
h1, h2, h3, .profile-name, .luna-title { font-family: 'Playfair Display', serif !important; font-style: italic !important; color: #ff80ab !important; text-shadow: 0 0 5px rgba(255, 255, 255, 0.9), 0 0 12px rgba(255, 182, 193, 0.6) !important; }
@keyframes bubbleFloat { 0%, 100% { transform: translateY(0px) scale(1); } 50% { transform: translateY(-14px) scale(1.03); } }
@keyframes wingFlutter { 0%, 100% { transform: perspective(300px) rotateY(0deg) rotate(15deg) scale(1); } 50% { transform: perspective(300px) rotateY(60deg) rotate(15deg) scale(0.9); } }
@keyframes bubbleBurst {
  0% { transform: scale(0.2) translateY(0); opacity: 0; }
  50% { opacity: 1; }
  100% { transform: scale(1) translateY(-25px); opacity: 0; }
}
@keyframes contentPop {
  0% { opacity: 0; transform: scale(0.7) translateY(15px); }
  70% { transform: scale(1.02) translateY(-3px); }
  100% { opacity: 1; transform: scale(1) translateY(0); }
}
div:has(> img[src*="avatars"]), div:has(> img[src*="user"]), div[class*="profile"], div[class*="Profile"] { display: flex !important; flex-direction: column !important; align-items: center !important; justify-content: center !important; text-align: center !important; width: 100% !important; }
div:has(> img[src*="avatars"]) ~ *, div:has(> img[src*="user"]) ~ * { text-align: center !important; margin-left: auto !important; margin-right: auto !important; }
div:has(> img[src*="avatars"]), div:has(> img[src*="user"]), div[class*="avatar"], a[href*="/characters/"] div:has(> img) { margin: 0 auto 18px auto !important; position: relative !important; border-radius: 50% !important; border: 2px solid rgba(255, 255, 255, 0.8) !important; box-shadow: 0 12px 32px rgba(255, 182, 193, 0.4) !important; animation: bubbleFloat 3.8s ease-in-out infinite !important; display: flex !important; align-items: center !important; justify-content: center !important; overflow: visible !important; }
div:has(> img[src*="avatars"]), div:has(> img[src*="user"]), div[class*="avatar"] { width: 160px !important; height: 160px !important; }
img[src*="avatars"], img[src*="user"], img[alt*="avatar"], div[class*="avatar"] img, div[class*="Profile"] img:first-of-type, a[href*="/characters/"] img { width: 100% !important; height: 100% !important; border-radius: 50% !important; object-fit: cover !important; z-index: 1 !important; }
div:has(> img[src*="avatars"])::before, div:has(> img[src*="user"])::before, div[class*="avatar"]::before { content: '' !important; display: block !important; position: absolute !important; top: -4px !important; right: -4px !important; width: 44px !important; height: 44px !important; background-image: url("https://img.icons8.com/ios-filled/100/ffffff/butterfly.png") !important; background-size: contain !important; background-position: center !important; background-repeat: no-repeat !important; filter: drop-shadow(0 0 6px rgba(255, 255, 255, 1)) drop-shadow(0 4px 6px rgba(255, 182, 193, 0.6)) !important; z-index: 999 !important; pointer-events: none !important; animation: wingFlutter 0.35s ease-in-out infinite alternate !important; transform-origin: center center !important; }
div:has(> img[src*="avatars"])::after, div:has(> img[src*="user"])::after, div[class*="avatar"]::after, a[href*="/characters/"] div:has(> img)::after { content: '' !important; position: absolute !important; top: 0 !important; left: 0 !important; width: 100% !important; height: 100% !important; border-radius: 50% !important; background: radial-gradient(circle at 30% 30%, rgba(255, 255, 255, 0.85) 0%, rgba(255, 255, 255, 0.2) 25%, rgba(255, 255, 255, 0) 50%, rgba(255, 182, 193, 0.25) 80%, rgba(255, 255, 255, 0.6) 100%) !important; box-shadow: inset 0 6px 18px rgba(255, 255, 255, 0.9), inset 0 -8px 22px rgba(255, 182, 193, 0.7) !important; pointer-events: none !important; z-index: 5 !important; }
button, a[role="button"] { background: linear-gradient(135deg, #ffccd5 0%, #ffb3c1 100%) !important; color: #ffffff !important; text-shadow: 0 0 4px rgba(255, 255, 255, 0.8) !important; border-radius: 35px !important; border: 1.5px solid #ffffff !important; box-shadow: 0 4px 12px rgba(255, 158, 187, 0.35) !important; font-weight: 600 !important; }
[role="tablist"], .chakra-tabs__tablist, div:has(> [role="tablist"]) { background: transparent !important; border: none !important; box-shadow: none !important; }
.chakra-tabs__tab-indicator { display: none !important; background: transparent !important; height: 0 !important; }
[role="tab"], button[role="tab"] { border: none !important; border-bottom: none !important; }
[role="tab"][aria-selected="true"], button[aria-selected="true"] { box-shadow: 0 4px 12px rgba(255, 158, 187, 0.35) !important; border: none !important; background: rgba(255, 255, 255, 0.15) !important; border-radius: 35px !important; outline: none !important; }
.luna-container { max-width: 800px; margin: 20px auto; text-align: center; padding: 10px; }
.luna-title { font-size: 2.5rem; margin-bottom: 25px; }
.luna-bubbles-wrapper { display: flex; flex-wrap: wrap; justify-content: center; gap: 20px; margin-bottom: 30px; }

/* Main Circle Bubble */
.luna-card {
  box-sizing: border-box;
  width: 140px;
  height: 140px;
  max-height: 140px;
  padding: 0;
  position: relative;
  background: radial-gradient(circle at 25% 15%, rgba(255, 255, 255, 0.95) 0%, rgba(255, 255, 255, 0.4) 40%, rgba(255, 182, 193, 0.15) 100%) !important;
  backdrop-filter: blur(12px) !important;
  -webkit-backdrop-filter: blur(12px) !important;
  border-radius: 50% !important;
  border: 2px solid rgba(255, 255, 255, 0.9) !important;
  box-shadow: 0 10px 25px rgba(255, 140, 175, 0.25), inset 0 10px 20px rgba(255, 255, 255, 0.9), inset 0 -8px 20px rgba(255, 182, 193, 0.5) !important;
  transition: all 0.5s cubic-bezier(0.25, 1, 0.5, 1);
  overflow: visible;
}

.luna-card:hover {
  transform: translateY(-5px) scale(1.03);
  box-shadow: 0 15px 35px rgba(255, 140, 175, 0.4), inset 0 12px 25px rgba(255, 255, 255, 1), inset 0 -8px 25px rgba(255, 182, 193, 0.6) !important;
}

.luna-card details { width: 100%; height: 100%; display: flex; flex-direction: column; position: relative; }
.luna-card details summary { cursor: pointer; font-weight: 700; font-size: 1.1rem; list-style: none; outline: none; display: flex; justify-content: center; align-items: center; text-align: center; width: 100%; height: 100%; padding: 10px; box-sizing: border-box; color: #ff6699 !important; text-shadow: 0 0 6px rgba(255, 255, 255, 0.9), 0 0 12px rgba(255, 105, 180, 0.5) !important; transition: all 0.4s ease; }
.luna-card details summary::-webkit-details-marker { display: none; }
.luna-card details summary::after { content: '✨'; font-size: 1.2rem; display: none; transition: transform 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275); }

/* LITTLE POPPING MINI-BUBBLES WHEN OPENING */
.luna-card:has(details[open]) {
  width: 100%;
  max-height: 800px;
  height: auto;
  border-radius: 35px !important;
  padding: 22px 30px;
  overflow: hidden;
}

.luna-card:has(details[open]) details summary { justify-content: space-between; height: auto; font-size: 1.3rem; text-align: left; padding: 0; }
.luna-card:has(details[open]) details summary::after { display: block; }
.luna-card details[open] summary::after { transform: rotate(180deg) scale(1.3); }

/* Mini bubbles spawning effect */
.luna-card details[open]::before {
  content: '';
  position: absolute;
  top: 20px;
  left: 50%;
  width: 10px;
  height: 10px;
  background: radial-gradient(circle, #fff 0%, rgba(255,182,193,0.6) 100%);
  border-radius: 50%;
  box-shadow: 
    -40px -20px 0 4px rgba(255,255,255,0.8),
    45px -30px 0 7px rgba(255,255,255,0.7),
    -20px -50px 0 3px rgba(255,182,193,0.8),
    30px -45px 0 5px rgba(255,255,255,0.9),
    0px -60px 0 6px rgba(255,182,193,0.7);
  animation: bubbleBurst 0.6s ease-out forwards;
  pointer-events: none;
  z-index: 10;
}

.luna-content { margin-top: 15px; padding-top: 15px; border-top: 2px dashed rgba(255, 255, 255, 0.8); line-height: 1.7; font-size: 1.05rem; text-align: left; transform-origin: top center; animation: contentPop 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275) forwards; }
.luna-tag-group { display: flex; flex-wrap: wrap; gap: 10px; justify-content: center; margin-top: 10px; }
.luna-tag { background: linear-gradient(180deg, rgba(255, 255, 255, 0.8) 0%, rgba(255, 182, 193, 0.4) 100%) !important; padding: 6px 18px; border-radius: 30px; font-weight: 600; border: 1.5px solid rgba(255, 255, 255, 0.95); box-shadow: inset 0 2px 6px rgba(255, 255, 255, 0.8), 0 4px 10px rgba(255, 158, 187, 0.25); }
.banner-img { width: 100%; max-width: 90%; border-radius: 35px; border: 3px solid rgba(255, 255, 255, 0.9); box-shadow: 0 10px 30px rgba(255, 140, 175, 0.3); margin: 20px auto; display: block; animation: bubbleFloat 4.5s ease-in-out infinite; }
.butterfly-wrapper { position: fixed; top: 0; left: 0; width: 100vw; height: 100vh; pointer-events: none; z-index: 99999; overflow: hidden; will-change: transform; }
.float-up { position: absolute; bottom: -60px; animation: simpleFloatUp 9s infinite linear; will-change: transform, opacity; }
.flutter-wing { width: 100%; height: 100%; object-fit: contain; filter: drop-shadow(0 0 6px rgba(255, 255, 255, 1)) drop-shadow(0 3px 6px rgba(255, 182, 193, 0.6)); animation: wingFlutter 0.35s ease-in-out infinite alternate; transform-origin: center center; }
.b-1 { left: 10%; width: 28px; height: 28px; animation-duration: 8s; animation-delay: 0s; }
.b-2 { left: 25%; width: 36px; height: 36px; animation-duration: 11s; animation-delay: 2s; }
.b-3 { left: 40%; width: 22px; height: 22px; animation-duration: 7s; animation-delay: 4s; }
.b-4 { left: 55%; width: 32px; height: 32px; animation-duration: 10s; animation-delay: 1s; }
.b-5 { left: 70%; width: 26px; height: 26px; animation-duration: 8.5s; animation-delay: 3s; }
.b-6 { left: 85%; width: 34px; height: 34px; animation-duration: 9.5s; animation-delay: 5s; }
.b-7 { left: 18%; width: 28px; height: 28px; animation-duration: 10.5s; animation-delay: 6s; }
.b-8 { left: 75%; width: 24px; height: 24px; animation-duration: 7.5s; animation-delay: 2.5s; }
@keyframes simpleFloatUp { 0% { transform: translateY(0) translateX(0); opacity: 0; } 15% { opacity: 0.85; } 85% { opacity: 0.85; } 100% { transform: translateY(-110vh) translateX(25px); opacity: 0; } }
.chakra-portal div:has(> img[src*="avatars"]), nav div:has(> img[src*="avatars"]), header div:has(> img[src*="avatars"]) { width: auto !important; height: auto !important; border: none !important; box-shadow: none !important; animation: none !important; margin: 0 !important; display: block !important; }
.chakra-portal img[src*="avatars"], nav img[src*="avatars"], header img[src*="avatars"] { width: 40px !important; height: 40px !important; border-radius: 50% !important; object-fit: cover !important; }
.chakra-portal div:has(> img[src*="avatars"])::before, nav div:has(> img[src*="avatars"])::before, header div:has(> img[src*="avatars"])::before, .chakra-portal div:has(> img[src*="avatars"])::after, nav div:has(> img[src*="avatars"])::after, header div:has(> img[src*="avatars"])::after { display: none !important; content: none !important; }
.chakra-portal div:has(> img[src*="avatars"]) ~ *, nav div:has(> img[src*="avatars"]) ~ *, header div:has(> img[src*="avatars"]) ~ * { text-align: left !important; margin: 0 !important; }
</style>
<div class="butterfly-wrapper">
<div class="float-up b-1"><img src="https://img.icons8.com/ios-filled/100/ffffff/butterfly.png" class="flutter-wing" alt="butterfly"></div>
<div class="float-up b-2"><img src="https://img.icons8.com/ios-filled/100/ffffff/butterfly.png" class="flutter-wing" alt="butterfly"></div>
<div class="float-up b-3"><img src="https://img.icons8.com/ios-filled/100/ffffff/butterfly.png" class="flutter-wing" alt="butterfly"></div>
<div class="float-up b-4"><img src="https://img.icons8.com/ios-filled/100/ffffff/butterfly.png" class="flutter-wing" alt="butterfly"></div>
<div class="float-up b-5"><img src="https://img.icons8.com/ios-filled/100/ffffff/butterfly.png" class="flutter-wing" alt="butterfly"></div>
<div class="float-up b-6"><img src="https://img.icons8.com/ios-filled/100/ffffff/butterfly.png" class="flutter-wing" alt="butterfly"></div>
<div class="float-up b-7"><img src="https://img.icons8.com/ios-filled/100/ffffff/butterfly.png" class="flutter-wing" alt="butterfly"></div>
<div class="float-up b-8"><img src="https://img.icons8.com/ios-filled/100/ffffff/butterfly.png" class="flutter-wing" alt="butterfly"></div>
</div>
<div class="luna-container">
<div class="luna-title">✨ Welcome to Luna's Corner ✨</div>
<div class="luna-bubbles-wrapper">
<div class="luna-card">
<details>
<summary>About Me</summary>
<div class="luna-content">
Lowkey giving up on CSS for now; that shit is tiring, not gonna lie! 🌸<br><br>
• <b>Name:</b> Luna (you can also call me <b>Lole</b>!)<br>
• <b>Age:</b> 19 year old student<br>
• <b>Orientation:</b> Bisexual 💖💜💙<br>
• <b>Language:</b> English is my third language, so I have a little trouble with it sometimes!<br>
• <b>Pet:</b> I have a fat orange cat named <b>Chubby</b> 🐾 (and I swear I don't give her that much food!)
</div>
</details>
</div>
<div class="luna-card">
<details>
<summary>My Bots & Writing</summary>
<div class="luna-content">
I mostly make <b>FemPOV</b> and <b>AnyPOV</b> bots! I write them based on books I read, taking inspiration from the stories and adding my own spin to them.<br><br>
I'm always making bots, but I mostly just like playing them! I'll still keep posting bots even when school starts. 💕
</div>
</details>
</div>
<div class="luna-card">
<details>
<summary>Tools & Free Assets</summary>
<div class="luna-content">
I mostly use <b>Tensor Art</b> and <b>Gemini</b> for my images.<br><br>
<i>Fun fact:</i> You can all use my side character images if you want since I don't plan on making standalone bots for them! Just please credit me, loves! 🎨
</div>
</details>
</div>
<div class="luna-card">
<details>
<summary>Socials</summary>
<div class="luna-content">
I will add my socials here once I fix them up! 🛠️
</div>
</details>
</div>
<div class="luna-card">
<details>
<summary>Favorite Tags</summary>
<div class="luna-content">
<div class="luna-tag-group">
<span class="luna-tag">FemPOV</span>
<span class="luna-tag">AnyPOV</span>
<span class="luna-tag">Romance</span>
<span class="luna-tag">Angst</span>
<span class="luna-tag">Fluff</span>
<span class="luna-tag">WLW</span>
<span class="luna-tag">MLW</span>
</div>
</div>
</details>
</div>
</div>
<img src="https://ella.janitorai.com/media-approved/aJtRtqLXyEY7m2PKV4n6o.webp" class="banner-img" alt="Profile Banner">
</div>
