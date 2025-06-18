<html lang="tr">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1" />
<meta name="description" content="ZZONE99 PUBG Mobile Klanı - Since 2018. Kaliteli ve rekabetçi PUBG Mobile topluluğu." />
<title>ZZONE99</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;600&display=swap');
  * {
    box-sizing: border-box;
  }
  body {
    margin:0; padding:0;
    font-family: 'Poppins', sans-serif;
    background: linear-gradient(135deg, #0b1424, #1c2a46);
    color:#d0e7ff;
    overflow-x: hidden;
  }
  /* Arkaplan animasyon (hafif ışık ve renk geçişleri) */
  body::before {
    content: "";
    position: fixed;
    inset: 0;
    background: radial-gradient(circle at top left, #0b1424, #1c2a46, #001122);
    animation: bgpulse 15s ease-in-out infinite alternate;
    z-index: -1;
  }
  @keyframes bgpulse {
    0% {background-position: 0% 50%;}
    50% {background-position: 100% 50%;}
    100% {background-position: 0% 50%;}
  }

  header, main, footer {
    max-width: 1000px;
    margin: 0 auto;
    padding: 15px 20px;
  }

  /* --- Loading Screen --- */
  #loading-screen {
    position: fixed;
    inset: 0;
    background: #0b1424;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    z-index: 9999;
    animation: fadeOut 0.5s ease forwards;
    animation-delay: 2s;
  }
  #loading-screen.hidden {
    display: none;
  }
  #loading-logo {
    width: 120px;
    height: 120px;
    background: url('logo.png') no-repeat center / contain;
    filter: drop-shadow(0 0 10px #0ff);
    animation: glowPulse 2s ease-in-out infinite alternate;
  }
  #loading-text {
    margin-top: 10px;
    font-weight: 700;
    font-size: 2.4rem;
    letter-spacing: 0.15em;
    color: #0ff;
    text-shadow: 0 0 8px #0ff;
    animation: glowPulse 2s ease-in-out infinite alternate;
  }

  @keyframes glowPulse {
    0% {filter: drop-shadow(0 0 5px #0ff);}
    100% {filter: drop-shadow(0 0 20px #0ff);}
  }
  @keyframes fadeOut {
    to {opacity: 0; visibility: hidden;}
  }

  /* --- Navbar --- */
  nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: rgba(0,30,50,0.7);
    padding: 10px 15px;
    border-radius: 10px;
    margin-bottom: 20px;
    box-shadow: 0 0 20px #0ff5;
  }
  nav .logo {
    display: flex;
    align-items: center;
  }
  nav .logo img {
    width: 60px;
    height: 60px;
    filter: drop-shadow(0 0 10px #0ff);
    margin-right: 10px;
    animation: glowPulse 3s ease-in-out infinite alternate;
  }
  nav .logo span {
    font-size: 1.8rem;
    font-weight: 700;
    color: #0ff;
    letter-spacing: 0.2em;
    text-shadow: 0 0 10px #0ff;
  }
  nav ul {
    list-style: none;
    display: flex;
    gap: 25px;
  }
  nav ul li {
    cursor: pointer;
    font-weight: 600;
    color: #d0e7ff;
    padding: 8px 15px;
    border-radius: 8px;
    transition: all 0.3s ease;
    position: relative;
  }
  nav ul li:hover {
    background: #0ff5;
    color: #001a33;
    box-shadow: 0 0 15px #0ff;
  }
  nav ul li.active {
    background: #0ff;
    color: #001a33;
    box-shadow: 0 0 15px #0ff;
  }

  /* Hamburger menu - mobile */
  #hamburger {
    display: none;
    flex-direction: column;
    cursor: pointer;
    gap: 6px;
  }
  #hamburger div {
    width: 28px;
    height: 3px;
    background: #0ff;
    border-radius: 2px;
    transition: all 0.3s ease;
  }
  @media (max-width: 768px) {
    nav ul {
      position: fixed;
      top: 65px;
      right: -100%;
      flex-direction: column;
      background: rgba(0,30,50,0.95);
      width: 180px;
      padding: 15px;
      border-radius: 0 0 0 10px;
      transition: right 0.3s ease;
      height: calc(100vh - 65px);
      z-index: 999;
    }
    nav ul.open {
      right: 0;
    }
    #hamburger {
      display: flex;
    }
  }

  /* --- Section Styling --- */
  section {
    margin-bottom: 40px;
  }
  h2 {
    font-size: 2rem;
    font-weight: 700;
    margin-bottom: 15px;
    color: #0ff;
    letter-spacing: 0.1em;
    text-shadow: 0 0 8px #0ff8;
  }
  p {
    line-height: 1.5;
    font-weight: 300;
    font-size: 1.1rem;
    color: #bbdff9;
  }

  /* --- Tanıtım --- */
  #tanitim p {
    font-size: 1.15rem;
  }

  /* --- Üyeler Bölümü --- */
  #uyeler {
    display: flex;
    justify-content: center;
    gap: 35px;
    flex-wrap: wrap;
  }
  .member-card {
    background: rgba(0,30,50,0.6);
    border-radius: 15px;
    width: 180px;
    padding: 15px;
    box-shadow: 0 0 15px #0ff8;
    text-align: center;
    transition: transform 0.3s ease;
    cursor: default;
    filter: drop-shadow(0 0 6px #0ff8);
  }
  .member-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 0 20px #0ff;
  }
  .member-card img {
    width: 130px;
    height: 130px;
    object-fit: contain;
    margin-bottom: 10px;
    filter: drop-shadow(0 0 10px #0ff);
  }
  .member-card h3 {
    font-size: 1.3rem;
    font-weight: 700;
    color: #0ff;
    letter-spacing: 0.05em;
    text-shadow: 0 0 7px #0ff;
  }

  /* --- Başvuru Butonu ve Popup --- */
  #basvuru-btn {
    display: block;
    margin: 0 auto 40px auto;
    padding: 14px 35px;
    font-size: 1.3rem;
    font-weight: 700;
    background: linear-gradient(45deg, #00ffff, #00aacc);
    border: none;
    border-radius: 35px;
    color: #001a33;
    cursor: pointer;
    box-shadow: 0 0 20px #0ff8;
    transition: all 0.3s ease;
  }
  #basvuru-btn:hover {
    background: linear-gradient(45deg, #00aacc, #007788);
    color: #d0e7ff;
    box-shadow: 0 0 30px #0ff;
  }

  #basvuru-popup-bg {
    position: fixed;
    inset: 0;
    background: rgba(0,0,0,0.7);
    display: none;
    justify-content: center;
    align-items: center;
    z-index: 10000;
  }
  #basvuru-popup {
    background: #122f4f;
    border-radius: 15px;
    padding: 30px 25px;
    width: 95%;
    max-width: 440px;
    box-shadow: 0 0 20px #0ff8;
    position: relative;
    color: #d0e7ff;
  }
  #basvuru-popup h3 {
    margin-top: 0;
    text-align: center;
    font-size: 1.7rem;
    margin-bottom: 20px;
    color: #00ffff;
  }
  #basvuru-popup label {
    font-weight: 600;
    display: block;
    margin: 10px 0 5px 0;
  }
  #basvuru-popup input, #basvuru-popup select, #basvuru-popup textarea {
    width: 100%;
    padding: 10px;
    border-radius: 8px;
    border: none;
    font-size: 1rem;
    margin-bottom: 15px;
    outline: none;
  }
  #basvuru-popup button.submit-btn {
    width: 100%;
    background: linear-gradient(45deg, #00ffff, #00aacc);
    border: none;
    padding: 12px;
    font-weight: 700;
    font-size: 1.2rem;
    border-radius: 30px;
    cursor: pointer;
    color: #001a33;
    box-shadow: 0 0 20px #0ff8;
    transition: all 0.3s ease;
  }
  #basvuru-popup button.submit-btn:hover {
    background: linear-gradient(45deg, #00aacc, #007788);
    color: #d0e7ff;
  }
  #basvuru-popup .close-btn {
    position: absolute;
    top: 12px;
    right: 15px;
    background: none;
    border: none;
    font-size: 1.6rem;
    font-weight: 700;
    color: #00ffff;
    cursor: pointer;
  }

  /* Başvuru geri bildirim */
  #form-feedback {
    text-align: center;
    margin-top: 10px;
    font-weight: 600;
    font-size: 1.1rem;
  }
  #form-feedback.success {
    color: #00ffb3;
  }
  #form-feedback.error {
    color: #ff6161;
  }

  /* --- Tiktok Popup --- */
  #tiktok-popup-bg {
    position: fixed;
    inset: 0;
    background: rgba(0,0,0,0.7);
    display: none;
    justify-content: center;
    align-items: center;
    z-index: 9999;
  }
  #tiktok-popup {
    background: #12345d;
    padding: 25px 30px;
    border-radius: 15px;
    max-width: 300px;
    box-shadow: 0 0 20px #0ff8;
    color: #d0e7ff;
    text-align: center;
  }
  #tiktok-popup h3 {
    margin: 0 0 15px 0;
    color: #00ffff;
  }
  #tiktok-popup a {
    color: #0ff;
    text-decoration: none;
    font-weight: 600;
    word-break: break-word;
  }
  #tiktok-popup button.close-tiktok {
    margin-top: 15px;
    background: #007788;
    border: none;
    padding: 8px 20px;
    border-radius: 25px;
    color: #d0e7ff;
    font-weight: 600;
    cursor: pointer;
    transition: background 0.3s ease;
  }
  #tiktok-popup button.close-tiktok:hover {
    background: #005566;
  }

  /* --- Buttons to open tiktok popup */
  #tiktok-buttons {
    display: flex;
    justify-content: center;
    gap: 25px;
    margin-bottom: 30px;
  }
  #tiktok-buttons button {
    background: linear-gradient(45deg, #00ffff, #00aacc);
    border: none;
    padding: 12px 22px;
    border-radius: 35px;
    cursor: pointer;
    font-weight: 700;
    color: #001a33;
    box-shadow: 0 0 15px #0ff8;
    transition: all 0.3s ease;
    letter-spacing: 0.04em;
  }
  #tiktok-buttons button:hover {
    background: linear-gradient(45deg, #00aacc, #007788);
    color: #d0e7ff;
    box-shadow: 0 0 25px #0ff;
  }

  /* --- Zzone99 Parlak İsim Efekti --- */
  #site-title {
    font-weight: 900;
    font-size: 3.5rem;
    letter-spacing: 0.15em;
    text-align: center;
    margin-bottom: 25px;
    color: #0ff;
    text-shadow:
      0 0 8px #0ff,
      0 0 15px #00ffff,
      0 0 22px #00ffff,
      0 0 40px #0ff,
      0 0 50px #0ff;
    animation: shimmer 4s linear infinite;
  }
  @keyframes shimmer {
    0% {text-shadow:
      0 0 8px #0ff,
      0 0 15px #00ffff,
      0 0 22px #00ffff,
      0 0 40px #0ff,
      0 0 50px #0ff;}
    50% {text-shadow:
      0 0 10px #0ff,
      0 0 20px #00ffff,
      0 0 28px #00ffff,
      0 0 50px #0ff,
      0 0 70px #0ff;}
    100% {text-shadow:
      0 0 8px #0ff,
      0 0 15px #00ffff,
      0 0 22px #00ffff,
      0 0 40px #0ff,
      0 0 50px #0ff;}
  }

  /* --- Ziyaretçi Sayacı --- */
  #visitor-counter {
    text-align: center;
    font-weight: 600;
    font-size: 1.1rem;
    margin-bottom: 40px;
    color: #66e4ff;
    text-shadow: 0 0 10px #0ff9;
  }

  /* --- Oyun içi iletişim --- */
  #oyun-ici-iletisim {
    background: rgba(0, 30, 50, 0.6);
    padding: 18px 25px;
    border-radius: 15px;
    box-shadow: 0 0 20px #00ffff80;
    font-weight: 700;
    font-size: 1.3rem;
    color: #00ffff;
    margin-bottom: 40px;
    text-align: center;
    letter-spacing: 0.05em;
  }

  /* Sayfa geçiş animasyonu */
  .page {
    opacity: 0;
    transform: translateY(15px);
    transition: opacity 0.5s ease, transform 0.5s ease;
    display: none;
  }
  .page.active {
    opacity: 1;
    transform: translateY(0);
    display: block;
  }

</style>
</head>
<body>

<!-- Loading Screen -->
<div id="loading-screen">
  <div id="loading-logo"></div>
  <div id="loading-text">ZZONE99</div>
</div>

<!-- Navbar -->
<nav>
  <div class="logo">
    <img src="logo.png" alt="ZZONE99 Logo" />
    <span>ZZONE99</span>
  </div>
  <div id="hamburger">
    <div></div><div></div><div></div>
  </div>
  <ul id="nav-links">
    <li class="nav-item active" data-target="tanitim">Tanıtım</li>
    <li class="nav-item" data-target="uyeler">Üyeler</li>
    <li class="nav-item" data-target="basvuru">Klana Katıl</li>
    <li class="nav-item" data-target="oyunici">Oyun İçi</li>
    <li class="nav-item" data-target="iletisim">İletişim</li>
  </ul>
</nav>

<main>
  <h1 id="site-title">ZZONE99</h1>

  <div id="visitor-counter">Ziyaretçi Sayısı: <span id="visitor-count">0</span></div>

  <section id="tanitim" class="page active">
    <h2>ZZONE99 PUBG Mobile Klanı</h2>
    <p>2018 yılında kurulmuş olan ZZONE99, PUBG Mobile dünyasında kaliteli, rekabetçi ve samimi bir topluluk oluşturmayı amaçlayan bir klandır. Oyuncuların birlikte gelişebileceği, turnuvalara katılabileceği ve eğlenceli vakit geçirebileceği bir ortam sunar.</p>
  </section>

  <section id="uyeler" class="page">
    <h2>Önemli Üyelerimiz</h2>
    <div class="member-card">
      <img src="mazz.png" alt="mAzz99" />
      <h3>mAzz99</h3>
      <p>Kurucu & Lider</p>
    </div>
    <div class="member-card">
      <img src="yazz.png" alt="yAzz99" />
      <h3>yAzz99</h3>
      <p>Yönetici</p>
    </div>
  </section>

  <section id="basvuru" class="page">
    <button id="basvuru-btn">Klana Katıl</button>
  </section>

  <section id="oyunici" class="page">
    <div id="oyun-ici-iletisim">
      <p>Oyuncu İsimleri:</p>
      <p style="font-size: 1.5rem; font-weight: 900; letter-spacing: 0.1em; color:#0ff; margin-top:10px;">
        mAzz99 &nbsp;|&nbsp; yAzz99 &nbsp;|&nbsp; babavizyondapm
      </p>
    </div>
  </section>

  <section id="iletisim" class="page">
    <h2>İletişim</h2>
    <p>Bizi TikTok üzerinden takip edebilirsiniz:</p>
    <div id="tiktok-buttons">
      <button data-user="@mazz99theboss">mAzz99 TikTok</button>
      <button data-user="@babavizyondapm">babaVizyon TikTok</button>
    </div>
  </section>
</main>

<footer>
  <p style="text-align:center; margin-top:40px; font-weight:700; color:#0ff;">
    Für die Famiilla &nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp; SINCE 2018
  </p>
</footer>

<!-- Başvuru Popup -->
<div id="basvuru-popup-bg">
  <div id="basvuru-popup">
    <button class="close-btn" title="Kapat">&times;</button>
    <h3>Klana Katıl Başvurusu</h3>
    <form id="basvuru-form" action="https://formspree.io/f/xldnljve" method="POST">
      <label for="uid">UID (Oyuncu ID):</label>
      <input type="text" name="uid" id="uid" required placeholder="UID numaranız" />
      <label for="oyunIsmi">Oyun İsmi:</label>
      <input type="text" name="oyunIsmi" id="oyunIsmi" required placeholder="Oyun içi isminiz" />
      <label for="isim">İsim (Gerçek):</label>
      <input type="text" name="isim" id="isim" required placeholder="Gerçek adınız" />
      <label for="yas">Yaş:</label>
      <input type="number" name="yas" id="yas" required min="12" max="100" />
      <label for="cihaz">Cihaz:</label>
      <select name="cihaz" id="cihaz" required>
        <option value="">Seçiniz</option>
        <option value="Android">Android</option>
        <option value="iOS">iOS</option>
        <option value="PC">PC</option>
      </select>
      <label for="aktiflik">Aktiflik Durumu:</label>
      <select name="aktiflik" id="aktiflik" required>
        <option value="">Seçiniz</option>
        <option value="Sık Oynar">Sık Oynar</option>
        <option value="Bazen Oynar">Bazen Oynar</option>
        <option value="Nadiren Oynar">Nadiren Oynar</option>
      </select>
      <button class="submit-btn" type="submit">Başvuruyu Gönder</button>
      <div id="form-feedback"></div>
    </form>
  </div>
</div>

<!-- TikTok Popup -->
<div id="tiktok-popup-bg">
  <div id="tiktok-popup">
    <h3>TikTok Profili</h3>
    <p id="tiktok-username">@mazz99theboss</p>
    <button class="close-tiktok">Kapat</button>
  </div>
</div>

<script>
  // Loading screen gizleme (2 saniyede)
  window.addEventListener('load', () => {
    setTimeout(() => {
      const loading = document.getElementById('loading-screen');
      loading.classList.add('hidden');
    }, 2000);
  });

  // Navbar hamburger toggle
  const hamburger = document.getElementById('hamburger');
  const navLinks = document.getElementById('nav-links');
  hamburger.addEventListener('click', () => {
    navLinks.classList.toggle('open');
  });

  // Sayfa geçişleri ve aktif menu kontrolü
  const navItems = document.querySelectorAll('.nav-item');
  const pages = document.querySelectorAll('.page');

  function setActivePage(targetId) {
    pages.forEach(p => {
      p.classList.remove('active');
      if(p.id === targetId) p.classList.add('active');
    });
    navItems.forEach(item => {
      item.classList.remove('active');
      if(item.dataset.target === targetId) item.classList.add('active');
    });
    // URL hash güncelle
    history.replaceState(null, '', `#${targetId}`);
    // Menü kapat (mobilde)
    navLinks.classList.remove('open');
  }

  navItems.forEach(item => {
    item.addEventListener('click', () => {
      setActivePage(item.dataset.target);
    });
  });

  // URL hash ile sayfa açma
  window.addEventListener('DOMContentLoaded', () => {
    const hash = location.hash.replace('#','');
    if(hash && [...pages].some(p => p.id === hash)) {
      setActivePage(hash);
    }
  });

  // Başvuru popup aç/kapat
  const basvuruBtn = document.getElementById('basvuru-btn');
  const basvuruPopupBg = document.getElementById('basvuru-popup-bg');
  const basvuruCloseBtn = basvuruPopupBg.querySelector('.close-btn');

  basvuruBtn.addEventListener('click', () => {
    basvuruPopupBg.style.display = 'flex';
  });
  basvuruCloseBtn.addEventListener('click', () => {
    basvuruPopupBg.style.display = 'none';
  });
  basvuruPopupBg.addEventListener('click', (e) => {
    if(e.target === basvuruPopupBg) basvuruPopupBg.style.display = 'none';
  });

  // Formspree AJAX gönderim
  const basvuruForm = document.getElementById('basvuru-form');
  const formFeedback = document.getElementById('form-feedback');

  basvuruForm.addEventListener('submit', async (e) => {
    e.preventDefault();
    formFeedback.textContent = '';
    const formData = new FormData(basvuruForm);
    try {
      const response = await fetch(basvuruForm.action, {
        method: 'POST',
        body: formData,
        headers: {
          'Accept': 'application/json'
        }
      });
      if (response.ok) {
        formFeedback.textContent = "Başvurunuz başarıyla gönderildi. En kısa sürede dönüş yapılacaktır.";
        formFeedback.className = 'success';
        basvuruForm.reset();
      } else {
        const data = await response.json();
        formFeedback.textContent = data.errors ? data.errors.map(e=>e.message).join(', ') : "Gönderimde hata oluştu.";
        formFeedback.className = 'error';
      }
    } catch {
      formFeedback.textContent = "Bağlantı hatası, lütfen tekrar deneyiniz.";
      formFeedback.className = 'error';
    }
  });

  // TikTok popup yönetimi
  const tiktokButtons = document.querySelectorAll('#tiktok-buttons button');
  const tiktokPopupBg = document.getElementById('tiktok-popup-bg');
  const tiktokPopupUsername = document.getElementById('tiktok-username');
  const tiktokCloseBtn = document.querySelector('.close-tiktok');

  tiktokButtons.forEach(btn => {
    btn.addEventListener('click', () => {
      tiktokPopupUsername.textContent = btn.dataset.user;
      tiktokPopupBg.style.display = 'flex';
    });
  });
  tiktokCloseBtn.addEventListener('click', () => {
    tiktokPopupBg.style.display = 'none';
  });
  tiktokPopupBg.addEventListener('click', (e) => {
    if(e.target === tiktokPopupBg) tiktokPopupBg.style.display = 'none';
  });

  // Ziyaretçi sayacı (localStorage)
  const visitorCountEl = document.getElementById('visitor-count');
  function updateVisitorCount() {
    const key = 'zzone99_visitor_count';
    let count = parseInt(localStorage.getItem(key)) || 0;
    count++;
    localStorage.setItem(key, count);
    visitorCountEl.textContent = count;
  }
  updateVisitorCount();

  // Push Notification örneği (isteğe bağlı)
  if('Notification' in window){
    if(Notification.permission === 'default') {
      Notification.requestPermission();
    }
  }

</script>
</body>
