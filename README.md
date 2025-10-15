<!doctype html>
<html lang="th">

<head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Eclipsera Hotel — Login</title>
    <link rel="preconnect" href="https://fonts.gstatic.com">
    <link
        href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;600;700&family=Inter:wght@300;400;600&display=swap"
        rel="stylesheet">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/css/bootstrap.min.css" rel="stylesheet">
    <style>
        :root {
            --accent: #b98bff;
            --gold: #d9b65a;
            --bg: #0b0a13;
            --text: #e5e3f5;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: #000;
            overflow: hidden;
            color: var(--text);
        }

        .bg-video {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
            z-index: -3;
            filter: brightness(0.35) saturate(1.2);
        }

        .overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at center, rgba(0, 0, 0, 0.3), rgba(5, 3, 10, 0.95));
            z-index: -2;
        }

        .warning-screen,
        .intro-screen,
        .login-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: column;
            text-align: center;
            padding: 40px;
            transition: opacity 2s ease;
        }

        .warning-screen {
            background: #0b0a13;
            z-index: 15;
            opacity: 0;
        }

        .warning-box {
            max-width: 700px;
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 255, 255, 0.15);
            border-radius: 16px;
            padding: 30px 40px;
            box-shadow: 0 0 20px rgba(255, 255, 255, 0.08);
        }

        .warning-box h2 {
            color: #ff8080;
            font-size: 1.5rem;
            margin-bottom: 15px;
            text-shadow: 0 0 8px rgba(255, 128, 128, 0.5);
        }

        .warning-box p {
            font-size: 1rem;
            line-height: 1.7;
            color: #ddd;
        }

        .intro-screen {
            background: #0b0a13;
            z-index: 10;
            opacity: 0;
        }

        .intro-title {
            font-family: 'Cinzel', serif;
            font-size: 3rem;
            color: var(--gold);
            letter-spacing: 2px;
            text-shadow: 0 0 15px rgba(217, 182, 90, 0.5);
            opacity: 0;
            transform: scale(0.8);
            transition: opacity 2s ease, transform 2s ease;
        }

        .login-container {
            opacity: 0;
            z-index: 5;
        }

        .login-box {
            background: rgba(20, 15, 30, 0.85);
            padding: 40px;
            border-radius: 16px;
            border: 1px solid rgba(185, 139, 255, 0.2);
            box-shadow: 0 0 30px rgba(185, 139, 255, 0.2);
            width: 100%;
            max-width: 420px;
            text-align: center;
        }

        .login-box h2 {
            font-family: 'Cinzel', serif;
            color: var(--gold);
            margin-bottom: 20px;
            text-shadow: 0 0 8px rgba(217, 182, 90, 0.4);
        }

        .form-control {
            background: rgba(255, 255, 255, 0.08);
            border: 1px solid rgba(185, 139, 255, 0.3);
            color: #fff;
        }

        .form-control:focus {
            border-color: var(--accent);
            box-shadow: 0 0 10px rgba(185, 139, 255, 0.4);
            background: rgba(255, 255, 255, 0.12);
            color: #fff;
        }

        .btn-login {
            width: 100%;
            background: var(--accent);
            border: none;
            padding: 10px;
            color: #fff;
            font-weight: 600;
            border-radius: 8px;
            transition: background 0.3s ease;
        }

        .btn-login:hover {
            background: #6b3bbd;
        }

        .text-muted {
            color: #b3b3c6 !important;
        }

        #music-toggle {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: rgba(255, 255, 255, 0.1);
            border: 1px solid rgba(185, 139, 255, 0.4);
            color: var(--accent);
            border-radius: 50%;
            width: 50px;
            height: 50px;
            font-size: 1.4rem;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        #music-toggle:hover {
            background: rgba(185, 139, 255, 0.3);
            color: #fff;
        }
    </style>
</head>

<body>
    <video class="bg-video" autoplay muted loop playsinline>
        <source src="./image/hotel2.gif" type="video/mp4">
    </video>
    <div class="overlay"></div>

    <div class="warning-screen" id="warning">
        <div class="warning-box">
            <h2>⚠️ คำเตือนก่อนเข้าสู่เว็บไซต์ ⚠️</h2>
            <p> เว็บไซต์ <strong>Eclipsera Hotel</strong> เป็นส่วนหนึ่งของแท็กวาดรูปและโรลเพลย์ในโลกสมมติ
                ซึ่งรายละเอียดของฉาก สถานที่ ตัวละคร หรือเหตุการณ์ทั้งหมดที่ปรากฏในเว็บไซต์นี้
                <strong>ไม่มีส่วนเกี่ยวข้องกับโลกความเป็นจริง</strong>
                และจัดทำขึ้นเพื่อวัตถุประสงค์ด้านบันเทิงและสร้างสรรค์เท่านั้น<br><br>
                ข้อมูลหรือเนื้อหาภายในเว็บไซต์นี้อาจมีลักษณะลึกลับหรือเหนือธรรมชาติ เหยียดชนชั้น
                โปรดใช้วิจารณญาณในการเข้าชม<br><br> เพื่อเพิ่มอรรถรสในการเข้าชม
                <strong>กรุณากดปุ่มเปิดเพลงด้านล่างขวาของหน้า</strong> 🎶<br><br> Log in หน้านี้เป็นแบบจำลอง
                <strong>คุณสามารถใส่ข้อมูลเข้าสู่ระบบได้ตามต้องการ (ไม่ต้องกรอกจริง)</strong> </p>
        </div>
    </div>

    <div class="intro-screen" id="intro">
        <h1 class="intro-title" id="hotel-title">Eclipsera Hotel</h1>
    </div>

    <div class="login-container" id="login">
        <div class="login-box">
            <h2>Sign In</h2>
            <form action="Choice.html">
                <div class="mb-3">
                    <input type="text" class="form-control" placeholder="Username" required>
                </div>
                <div class="mb-3">
                    <input type="password" class="form-control" placeholder="Password" required>
                </div>
                <button type="submit" class="btn-login">Log In</button>
            </form>
            <p class="mt-3 text-muted">© 2025 Eclipsera Hotel</p>
        </div>
    </div>

    <button id="music-toggle">🔈</button>

    <audio id="bg-music" loop>
        <source src="./mp3/Dark Waltz Music - Vampire Masquerade collection.mp3" type="audio/mpeg">
    </audio>

    <script>
        const audio = document.getElementById('bg-music');
        const btn = document.getElementById('music-toggle');
        let playing = false;
        btn.addEventListener('click', () => {
            if (!playing) {
                audio.play();
                btn.textContent = '🔊';
            } else {
                audio.pause();
                btn.textContent = '🔈';
            }
            playing = !playing;
        });

        const warning = document.getElementById('warning');
        const intro = document.getElementById('intro');
        const login = document.getElementById('login');
        const hotelTitle = document.getElementById('hotel-title');

        window.addEventListener('load', () => {
            // ค่อยๆ แสดงคำเตือน
            warning.style.opacity = 1;
            setTimeout(() => {
                // ค่อยๆ หายไป
                warning.style.opacity = 0;
                setTimeout(() => {
                    warning.style.display = 'none';
                    // แสดงชื่อโรงแรม
                    intro.style.opacity = 1;
                    hotelTitle.style.opacity = 1;
                    hotelTitle.style.transform = 'scale(1)';
                    audio.play(); // เล่นเพลงตอนชื่อโรงแรมขึ้น
                    setTimeout(() => {
                        // ค่อยๆ หายไป intro
                        intro.style.opacity = 0;
                        hotelTitle.style.opacity = 0;
                        setTimeout(() => {
                            intro.style.display = 'none';
                            // แสดงฟอร์ม login
                            login.style.opacity = 1;
                        }, 2000);
                    }, 4000); // เวลาแสดงชื่อโรงแรม
                }, 2000);
            }, 5500); // เวลาแสดงคำเตือน
        });
    </script>
</body>

</html>
