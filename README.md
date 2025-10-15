<!doctype html>
<html lang="en">

<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Hotel — Home</title>

  <!-- Google font -->
  <link rel="preconnect" href="https://fonts.gstatic.com">
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">

  <!-- Bootstrap CSS -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/css/bootstrap.min.css" rel="stylesheet">

  <style>
    :root {
      --accent: #b98bff;
      --accent-dark: #6b3bbd;
      --gold: #d9b65a;
      --muted: #b3b3c6;
      --bg: #0b0a13;
      --card-bg: #15121f;
      --text: #e5e3f5;
    }

    body {
      font-family: 'Inter', system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial;
      background: radial-gradient(circle at top, #1c1529 0%, #0b0a13 90%);
      color: var(--text);
      scroll-behavior: smooth;
    }

    /* NAVBAR */
    .navbar {
      background: rgba(10, 8, 20, 0.8);
      backdrop-filter: blur(8px);
      border-bottom: 1px solid rgba(185, 139, 255, 0.25);
    }

    .navbar-brand {
      font-weight: 700;
      letter-spacing: -0.4px;
      color: var(--gold) !important;
      text-shadow: 0 0 6px rgba(217, 182, 90, 0.4);
    }

    .nav-link {
      color: var(--muted) !important;
      transition: color .3s;
    }

    .nav-link:hover {
      color: var(--accent) !important;
    }

    .btn-outline-primary {
      border-color: var(--accent);
      color: var(--accent);
    }

    .btn-outline-primary:hover {
      background: var(--accent);
      color: #fff;
    }

    /* HERO / CAROUSEL */
    .hero-carousel {
      position: relative;
      overflow: hidden;
      border-bottom-left-radius: 18px;
      border-bottom-right-radius: 18px;
      box-shadow: 0 8px 30px rgba(185, 139, 255, 0.1);
      margin-bottom: 40px;
    }

    .hero-carousel .carousel-item {
      height: 500px;
    }

    .hero-carousel .carousel-item img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      filter: brightness(0.45) saturate(1.1);
    }

    .carousel-caption h5 {
      color: var(--gold);
      text-shadow: 0 0 8px rgba(217, 182, 90, 0.4);
      font-size: 1.8rem;
      font-weight: 700;
    }

    .carousel-caption p {
      color: var(--muted);
      font-size: 1rem;
    }

    /* CATEGORIES / CARDS */
    .cards-grid {
      margin-top: 36px;
    }

    .category-card {
      border: 1px solid rgba(185, 139, 255, 0.2);
      border-radius: 12px;
      overflow: hidden;
      background: var(--card-bg);
      transition: transform .28s ease, box-shadow .28s ease, border-color .3s;
      color: var(--text);
      display: flex;
      flex-direction: column;
      justify-content: space-between;
    }

    .category-card:hover {
      transform: translateY(-6px);
      border-color: var(--accent);
      box-shadow: 0 0 25px rgba(185, 139, 255, 0.25);
    }

    .category-card .row.g-0 {
      flex: 1;
    }

    .category-card img {
      width: 140px;
      height: 100%;
      object-fit: cover;
      border-radius: 10px;
    }

    .card-title {
      color: var(--gold);
      font-weight: 600;
    }

    .text-muted {
      color: var(--muted) !important;
      font-size: 0.9rem;
    }

    .fw-bold {
      color: var(--accent);
    }

    .d-flex.justify-content-between {
      margin-top: auto;
    }

    /* POPULAR STAYS */
    .popular-card {
      background: var(--card-bg);
      border: 1px solid rgba(185, 139, 255, 0.2);
      border-radius: 12px;
      transition: transform .28s ease, box-shadow .28s ease, border-color .3s;
    }

    .popular-card:hover {
      transform: translateY(-6px);
      border-color: var(--accent);
      box-shadow: 0 0 25px rgba(185, 139, 255, 0.25);
    }

    .popular-card img {
      border-radius: 12px 12px 0 0;
      height: 180px;
      object-fit: cover;
    }

    .popular-card .card-body {
      color: var(--text);
    }

    footer {
      margin-top: 48px;
      padding: 32px 0;
      background: #0a0912;
      color: var(--muted);
      border-top: 1px solid rgba(185, 139, 255, 0.15);
    }

    footer p {
      color: var(--accent);
    }

    footer small {
      color: var(--muted);
    }

    @media (max-width: 767px) {
      .hero-carousel .carousel-item {
        height: 320px;
      }

      .category-card {
        flex-direction: row;
      }

      .category-card img {
        width: 100px;
        height: 100%;
      }
    }
  </style>
</head>

<body>
  <!-- NAVBAR -->
  <nav class="navbar navbar-expand-lg navbar-dark">
    <div class="container">
      <a class="navbar-brand" href="#">Eclipsera Hotel</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navMenu"
        aria-controls="navMenu" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navMenu">
        <ul class="navbar-nav ms-auto align-items-lg-center">
          <li class="nav-item me-2"><a class="nav-link" href="./Home.html">Home</a></li>
          <li class="nav-item me-2"><a class="nav-link" href="./Role.html">Role</a></li>
          <li class="nav-item me-2"><a class="nav-link" href="./About_Hotel.html">About Hotel</a></li>
          <li class="nav-item me-2"><a class="nav-link" href="./About_Tag.html">About Tag</a></li>
          <li class="nav-item me-2"><button id="music-toggle" class="btn btn-outline-primary btn-sm">🔈 Music</button>
          </li>
        </ul>
      </div>
    </div>
  </nav>

  <!-- HERO / CAROUSEL -->
  <div id="carouselExampleCaptions" class="carousel slide hero-carousel">
    <div class="carousel-indicators">
      <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="0" class="active"
        aria-current="true" aria-label="Slide 1"></button>
      <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="1"
        aria-label="Slide 2"></button>
      <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="2"
        aria-label="Slide 3"></button>
    </div>
    <div class="carousel-inner">
      <div class="carousel-item active">
        <img src="./image/hotel2.gif" class="d-block w-100" alt="...">
        <div class="carousel-caption d-none d-md-block">
          <h5>Welcome to Eclipsera Hotel</h5>
          <p>ยินดีต้อนรับเหล่ามนุษย์อัญมณีทุกท่าน สู่โรงแรมแห่งแสงจันทร์และอัญมณี ที่ซ่อนความลับและมนตราในทุกมุมมอง</p>
        </div>
      </div>
      <div class="carousel-item">
        <img src="./image/auction.gif" class="d-block w-100" alt="...">
        <div class="carousel-caption d-none d-md-block">
          <h5>Special auction event</h5>
          <p>เตรียมพบกับค่ำคืนแห่งการประมูลสุดหรู สมบัติและอัญมณีล้ำค่า รอให้คุณคว้ามาเป็นของตัวเอง</p>
        </div>
      </div>
      <div class="carousel-item">
        <img src="./image/ball2.gif" class="d-block w-100" alt="...">
        <div class="carousel-caption d-none d-md-block">
          <h5>Moonlit Gem Masquerade</h5>
          <p>ราตรีแห่งหน้ากากและอัญมณี ภายใต้แสงจันทร์ เต้นรำไปกับมนตราและเสน่ห์ของค่ำคืนอันลึกลับ</p>
        </div>
      </div>
    </div>
    <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide="prev">
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Previous</span>
    </button>
    <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide="next">
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Next</span>
    </button>
  </div>

  <!-- CONTENT: CATEGORIES GRID -->
  <main class="container cards-grid">
    <div class="d-flex align-items-center justify-content-between mb-3">
      <h4 class="m-0" style="color:var(--gold)">All stays in hotel</h4>
      <a href="#" class="text-decoration-none" style="color:var(--accent)">See all</a>
    </div>

    <div class="row gy-3">
      <!-- Repeat card columns -->
      <div class="col-lg-6">
        <div class="card category-card p-2">
          <div class="row g-0 align-items-center">
            <div class="col-auto">
              <img src="./image/ตราโลภะ.png" class="card-img-left rounded" alt="img">
            </div>
            <div class="col">
              <div class="card-body">
                <h5 class="card-title mb-1">Greed Hall</h5>
                <p class="card-text small text-muted">ชั้นที่เต็มไปด้วยความหรูหราเกินจำเป็น
                  ทุกอย่างประดับด้วยทองคำและอัญมณีล้ำค่า แขกทุกคนถูกล่อลวงให้ไขว่คว้าสิ่งที่เกินพอดี
                </p>
                <div class="d-flex justify-content-between align-items-center mt-2">
                  <div class="fw-bold">€2,400 / night</div>
                  <a href="./โลภะ.html" class="btn btn-sm btn-outline-primary">Book</a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="col-lg-6">
        <div class="card category-card p-2">
          <div class="row g-0 align-items-center">
            <div class="col-auto">
              <img src="./image/ตราราคะ.png" class="card-img-left rounded" alt="img">
            </div>
            <div class="col">
              <div class="card-body">
                <h5 class="card-title mb-1">Lust Chamber</h5>
                <p class="card-text small text-muted">ห้องชุดบรรยากาศเย้ายวนด้วยกลิ่นหอมชวนหลง
                  และเสียงดนตรีแผ่วเบาปลุกเร้าความปรารถนาในใจผู้เข้าพัก</p>
                <div class="d-flex justify-content-between align-items-center mt-2">
                  <div class="fw-bold">€2,400 / night</div>
                  <a href="./ราคะ.html" class="btn btn-sm btn-outline-primary">Book</a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="col-lg-6">
        <div class="card category-card p-2">
          <div class="row g-0 align-items-center">
            <div class="col-auto">
              <img src="./image/ตราโทสะ.png" class="card-img-left rounded" alt="img">
            </div>
            <div class="col">
              <div class="card-body">
                <h5 class="card-title mb-1">Wrath Wing</h5>
                <p class="card-text small text-muted">การตกแต่งด้วยเฉดแดงดำและเปลวไฟจำลองสะท้อนความโกรธเกรี้ยว
                  ทุกอย่างที่นี่เหมือนกำลังสั่นสะเทือนด้วยพลังของความเดือดดาล</p>
                <div class="d-flex justify-content-between align-items-center mt-2">
                  <div class="fw-bold">€2,400 / night</div>
                  <a href="./โทสะ.html" class="btn btn-sm btn-outline-primary">Book</a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="col-lg-6">
        <div class="card category-card p-2">
          <div class="row g-0 align-items-center">
            <div class="col-auto">
              <img src="./image/ตราเกียจคร้าน.png" class="card-img-left rounded" alt="img">
            </div>
            <div class="col">
              <div class="card-body">
                <h5 class="card-title mb-1">Sloth Garden</h5>
                <p class="card-text small text-muted">เต็มไปด้วยหมอกสีเทาอ่อนและเสียงน้ำไหลช้า ๆ
                  ทุกอย่างถูกออกแบบให้ขยับช้าเหมือนเวลาแทบหยุดนิ่ง แขกสามารถลืมโลกภายนอกได้อย่างสมบูรณ์</p>
                <div class="d-flex justify-content-between align-items-center mt-2">
                  <div class="fw-bold">€2,400 / night</div>
                  <a href="./เกียจคร้าน.html" class="btn btn-sm btn-outline-primary">Book</a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="col-lg-6">
        <div class="card category-card p-2">
          <div class="row g-0 align-items-center">
            <div class="col-auto">
              <img src="./image/ตราริษยา.png" class="card-img-left rounded" alt="img">
            </div>
            <div class="col">
              <div class="card-body">
                <h5 class="card-title mb-1">Envy Lounge</h5>
                <p class="card-text small text-muted">กระจกทุกบานสะท้อนภาพของ “สิ่งที่คุณอยากเป็น” แทนที่จะเป็นตัวคุณเอง
                  ที่นี่คือสถานที่ที่ความอิจฉาแผ่วเบาแต่กัดกินหัวใจอย่างช้า ๆ</p>
                <div class="d-flex justify-content-between align-items-center mt-2">
                  <div class="fw-bold">€2,400 / night</div>
                  <a href="./ริษยา.html" class="btn btn-sm btn-outline-primary">Book</a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="col-lg-6">
        <div class="card category-card p-2">
          <div class="row g-0 align-items-center">
            <div class="col-auto">
              <img src="./image/ตราตะกละ.png" class="card-img-left rounded" alt="img">
            </div>
            <div class="col">
              <div class="card-body">
                <h5 class="card-title mb-1">Gluttony Hall</h5>
                <p class="card-text small text-muted">ห้องอาหารหรูไร้กาลเวลา เสิร์ฟอาหารรสเลิศไม่สิ้นสุด
                  แต่ไม่ว่าอิ่มเท่าไร ก็รู้สึกเหมือนขาดบางอย่างอยู่เสมอ</p>
                <div class="d-flex justify-content-between align-items-center mt-2">
                  <div class="fw-bold">€2,400 / night</div>
                  <a href="./ตะกละ.html" class="btn btn-sm btn-outline-primary">Book</a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="col-lg-6">
        <div class="card category-card p-2">
          <div class="row g-0 align-items-center">
            <div class="col-auto">
              <img src="./image/ตราอัตตา.png" class="card-img-left rounded" alt="img">
            </div>
            <div class="col">
              <div class="card-body">
                <h5 class="card-title mb-1">Pride Throne</h5>
                <p class="card-text small text-muted">ชั้นสูงสุดของโรงแรม
                  ประดับด้วยกระจกเงินและแสงส่องเหนือบัลลังก์กลางห้อง แขกทุกคนถูกทดสอบว่าจะ “ภาคภูมิใจ” หรือ “หลงตนเอง”
                </p>
                <div class="d-flex justify-content-between align-items-center mt-2">
                  <div class="fw-bold">€2,400 / night</div>
                  <a href="./อัตตา.html" class="btn btn-sm btn-outline-primary">Book</a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- <div class="col-lg-6">
        <div class="card category-card p-2">
          <div class="row g-0 align-items-center">
            <div class="col-auto">
              <img src="./image/ตัวอย่างรูปตึงๆ.jpg" class="card-img-left rounded" alt="img">
            </div>
            <div class="col">
              <div class="card-body">
                <h5 class="card-title mb-1">Sin Reverie</h5>
                <p class="card-text small text-muted">ชั้นต้องห้ามที่ไม่อยู่ในแผนผังโรงแรมอย่างเป็นทางการ
                  ผู้ที่ขึ้นมาถึงได้ ถือว่า “ยอมรับบาปทั้งหมดในใจตนเองแล้ว” ที่นี่คือสถานที่ที่
                  เจ็ดบาปหลอมรวมกันเป็นหนึ่งเดียว ทั้งความงาม ความมืด และความปรารถนาไม่มีที่สิ้นสุด</p>
                <div class="d-flex justify-content-between align-items-center mt-2">
                  <div class="fw-bold">฿2,400 / night</div>
                  <a href="#" class="btn btn-sm btn-outline-primary">Book</a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div> -->

    </div>

    <!-- Rules -->
    <div class="mt-5">
      <div class="d-flex align-items-center justify-content-between mb-3">
        <h4 class="m-0" style="color:var(--gold)">Rules</h4>
        <!-- <a href="#" class="text-decoration-none" style="color:var(--accent)">See all</a> -->
      </div>

      <div class="row gy-4 justify-content-center">
        <div class="col-md-3 col-sm-6">
          <div class="card popular-card h-100 d-flex flex-column">
            <img src="./image/กรร.gif" class="card-img-top" alt="...">
            <div class="card-body d-flex flex-column">
              <h5 class="card-title">กฎของโรงแรม</h5>
              <p class="card-text text-muted small flex-grow-1">
                กรุณาปฏิบัติตามกฎของโรงแรม เพื่อให้ทุกการเข้าพักของเหล่ามนุษย์อัญมณีงดงาม น่าจดจำ และปราศจากความวุ่นวาย
              </p>
              <a href="./กฎโรงแรม.html" class="btn btn-sm btn-outline-primary mt-2">See all</a>
            </div>
          </div>
        </div>

        <div class="col-md-3 col-sm-6">
          <div class="card popular-card h-100 d-flex flex-column">
            <img src="./image/กทวร.gif" class="card-img-top" alt="...">
            <div class="card-body d-flex flex-column">
              <h5 class="card-title">กฎแท็กวาดรูปและการโรล</h5>
              <p class="card-text text-muted small flex-grow-1">
                ใช้แท็กอย่างเหมาะสม และผู้อื่น
              </p>
              <a href="./กฎแท็กวาดรูปและโรลเพล์.html" class="btn btn-sm btn-outline-primary mt-2">See all</a>
            </div>
          </div>
        </div>

        <div class="col-md-3 col-sm-6">
          <div class="card popular-card h-100 d-flex flex-column">
            <img src="./image/กสตลค.gif" class="card-img-top" alt="...">
            <div class="card-body d-flex flex-column">
              <h5 class="card-title">กฎการสร้างตัวละคร</h5>
              <p class="card-text text-muted small flex-grow-1">
                ทุกอัญมณีมีเรื่องราวเป็นของตัวเอง โปรดสร้างตัวละครด้วยความใส่ใจ ให้สอดคล้องกับธีมของโรงแรม ทั้งยศ ชั้น
                และบาปประจำตน
              </p>
              <a href="./กฎการสร้างตัวละคร.html" class="btn btn-sm btn-outline-primary mt-2">See all</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </main>

  <footer class="text-center">
    <div class="container">
      <p class="mb-1">© 2025 Eclipsera Hotel — Designed with ❤️</p>
      <small class="text-white">Replace placeholder images with your own (folder: /image) for production.</small>
    </div>
  </footer>

  <audio id="bg-music" autoplay loop>
    <source src="./mp3/Dark Waltz Music - Vampire Masquerade collection.mp3" type="audio/mpeg">
    Your browser does not support the audio element.
  </audio>

  <!-- Bootstrap JS -->
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/js/bootstrap.bundle.min.js"></script>

  <script>
    document.addEventListener('DOMContentLoaded', () => {
      const audio = document.getElementById('bg-music');

      // รอให้ผู้ใช้คลิกก่อนถึงจะเล่น
      const playMusic = () => {
        audio.play().catch(() => { });
        document.removeEventListener('click', playMusic);
      };

      document.addEventListener('click', playMusic);
    });

    const audio = document.getElementById('bg-music');
    const btn = document.getElementById('music-toggle');
    let playing = false;

    btn.addEventListener('click', () => {
      if (!playing) {
        audio.play();
        btn.textContent = '🔊 Playing';
      } else {
        audio.pause();
        btn.textContent = '🔈 Music';
      }
      playing = !playing;
    });
  </script>
</body>

</html>
