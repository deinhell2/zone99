
<html lang="tr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Zone99 | Motor Aksesuarları</title>
  <meta name="description" content="Zone99 motor aksesuar mağazası - kaliteli kasklar, eldivenler, LED farlar ve daha fazlası. Hız tutkunları için özel ürünler burada!">
  <meta name="keywords" content="motor aksesuar, kask, eldiven, led far, motosiklet ekipmanları, Zone99">
  <meta name="author" content="Zone99 Garage">
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body { font-family: 'Roboto', sans-serif; background-color: #111; color: #fff; overflow-x: hidden; }
    header { background-color: #000; padding: 20px; text-align: center; border-bottom: 3px solid red; }
    header h1 { color: red; font-size: 2.5rem; }
    nav { background-color: #1a1a1a; display: flex; justify-content: center; gap: 30px; padding: 10px; }
    nav a { color: #ccc; text-decoration: none; font-weight: bold; }
    nav a:hover { color: red; }.hero { background: url('https://images.unsplash.com/photo-1603721729420-8b33c45f4f49') center/cover no-repeat; height: 400px; display: flex; align-items: center; justify-content: center; text-shadow: 2px 2px 8px #000; }
.hero h2 { font-size: 3rem; color: #fff; background: rgba(0,0,0,0.6); padding: 20px; }

.products { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 20px; padding: 40px; background-color: #1a1a1a; }
.product { background-color: #222; padding: 20px; border: 1px solid #333; border-radius: 10px; text-align: center; }
.product img { max-width: 100%; height: 150px; object-fit: cover; border-radius: 5px; }
.product h3 { margin: 15px 0 10px; }
.product p { font-size: 14px; color: #aaa; }
.product button { margin-top: 10px; background-color: red; border: none; padding: 10px 20px; color: white; border-radius: 5px; cursor: pointer; }
.product button:hover { background-color: darkred; }

.cart {
  background-color: #222; padding: 20px; margin: 20px; border-radius: 10px;
}
.cart h3 { color: red; }

footer { background-color: #000; text-align: center; padding: 20px; color: #888; position: relative; }

.whatsapp-button {
  position: fixed; bottom: 20px; right: 20px; background-color: #25d366;
  color: white; border-radius: 50%; width: 60px; height: 60px;
  display: flex; align-items: center; justify-content: center;
  font-size: 30px; box-shadow: 0 0 10px rgba(0,0,0,0.5); z-index: 999;
}

/* Açılış animasyonu */
#intro {
  position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: #000; color: red;
  display: flex; flex-direction: column; align-items: center; justify-content: center;
  z-index: 1000; animation: fadeOut 2.5s ease 2s forwards;
}
@keyframes fadeOut {
  to { opacity: 0; visibility: hidden; }
}
.motor-icon {
  font-size: 80px; animation: slide 2s ease forwards;
}
@keyframes slide {
  0% { transform: translateX(-100%); opacity: 0; }
  50% { transform: translateX(0); opacity: 1; }
  100% { transform: translateX(100%); opacity: 0; }
}

  </style>
</head>
<body>
  <div id="intro">
    <div class="motor-icon">🏍️</div>
    <h1>ZONE99</h1>
  </div>  <header>
    <h1>ZONE99 MOTOR AKSESUAR</h1>
  </header>  <nav>
    <a href="#">Anasayfa</a>
    <a href="#urunler">Ürünler</a>
    <a href="#iletisim">İletişim</a>
    <a href="/admin-panel/login.html">Admin Panel</a>
  </nav>  <section class="hero">
    <h2>Hız Tutkunları İçin Özel Aksesuarlar</h2>
  </section>  <section class="products" id="urunler">
    <div class="product">
      <img src="https://images.unsplash.com/photo-1583341381263-e4f3a7b6c121" alt="Kask">
      <h3>Racing Kask</h3>
      <p>Yüksek koruma, agresif tasarım.</p>
      <button onclick="addToCart('Racing Kask', 1500)">Sepete Ekle</button>
    </div>
    <div class="product">
      <img src="https://images.unsplash.com/photo-1608719509638-445e6c179f0f" alt="Eldiven">
      <h3>Koruyucu Eldiven</h3>
      <p>Dayanıklı, rahat ve güvenli.</p>
      <button onclick="addToCart('Koruyucu Eldiven', 500)">Sepete Ekle</button>
    </div>
    <div class="product">
      <img src="https://images.unsplash.com/photo-1580247819530-9c117f6a3535" alt="Far">
      <h3>LED Far Seti</h3>
      <p>Gece sürüşlerinde maksimum görüş.</p>
      <button onclick="addToCart('LED Far Seti', 800)">Sepete Ekle</button>
    </div>
  </section>  <div class="cart">
    <h3>Sepet</h3>
    <ul id="cart-items"></ul>
    <p><strong>Toplam:</strong> <span id="total">0</span> TL</p>
    <button onclick="checkout()">Ödeme Yap</button>
  </div>  <footer id="iletisim">
    <p>© 2025 Zone99 Motor Aksesuar | WhatsApp: 0 5xx xxx xx xx | Instagram: @zone99garage</p>
  </footer><a class="whatsapp-button" href="https://wa.me/905xxxxxxxxx" target="_blank" title="Bize WhatsApp'tan ulaşın">🟢</a>

  <script>
    let cart = [];
    function addToCart(product, price) {
      cart.push({ product, price });
      updateCart();
    }
    function updateCart() {
      const items = document.getElementById('cart-items');
      items.innerHTML = '';
      let total = 0;
      cart.forEach(item => {
        items.innerHTML += `<li>${item.product} - ${item.price} TL</li>`;
        total += item.price;
      });
      document.getElementById('total').innerText = total;
    }
    function checkout() {
      alert("Sipariş alındı. Teşekkürler!");
      cart = [];
      updateCart();
    }
  </script></body>
