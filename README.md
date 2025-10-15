<!doctype html>
<html lang="en">

<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Eclipsera Hotel — Login</title>

  <!-- Google font -->
  <link rel="preconnect" href="https://fonts.gstatic.com">
  <link
    href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap"
    rel="stylesheet">

  <!-- Bootstrap -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/css/bootstrap.min.css" rel="stylesheet">

  <style>
    :root {
      --accent: #b98bff;
      --accent-dark: #6b3bbd;
      --gold: #d9b65a;
      --muted: #b3b3c6;
      --bg: #0b0a13;
      --card-bg: rgba(21, 18, 31, 0.95);
      --text: #e5e3f5;
    }

    body {
      font-family: 'Inter', system-ui, -apple-system, 'Segoe UI', Roboto, sans-serif;
      background: radial-gradient(circle at top, #1a1325 0%, #0b0a13 90%);
      color: var(--text);
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      overflow: hidden;
      position: relative;
    }

    /* พื้นหลังและเงาเรือง */
    .bg-glow {
      position: absolute;
      width: 700px;
      height: 700px;
      border-radius: 50%;
      background: radial-gradient(circle, rgba(185, 139, 255, 0.3), transparent 75%);
      filter: blur(80px);
      top: 45%;
      left: 50%;
      transform: translate(-50%, -50%);
      animation: pulse 8s infinite ease-in-out;
      z-index: 0;
    }

    @keyframes pulse {
      0%, 100% {
        opacity: 0.5;
        transform: translate(-50%, -50%) scale(1);
      }
      50% {
        opacity: 0.8;
        transform: translate(-50%, -50%) scale(1.1);
      }
    }

    /* กล่องล็อกอิน */
    .login-wrapper {
      position: relative;
      z-index: 2;
      width: 100%;
      max-width: 430px;
      background: var(--card-bg);
      border: 1px solid rgba(185, 139, 255, 0.25);
      border-radius: 20px;
      padding: 48px 42px;
      box-shadow: 0 0 50px rgba(185, 139, 255, 0.12);
      backdrop-filter: blur(14px);
      animation: fadeIn 1s ease forwards;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .login-logo {
      text-align: center;
      font-weight: 700;
      color: var(--gold);
      font-size: 1.8rem;
      letter-spacing: 0.5px;
      text-shadow: 0 0 10px rgba(217, 182, 90, 0.4);
      margin-bottom: 6px;
    }

    .login-subtitle {
      text-align: center;
      font-size: 0.95rem;
      color: var(--muted);
      margin-bottom: 28px;
      letter-spacing: 0.5px;
    }

    label {
      font-weight: 500;
    }

    .form-control {
      background-color: rgba(255, 255, 255, 0.07);
      border: 1px solid rgba(185, 139, 255, 0.25);
      color: var(--text);
      border-radius: 10px;
      padding: 10px 12px;
      transition: all 0.3s;
    }

    .form-control:focus {
      border-color: var(--accent);
      box-shadow: 0 0 12px rgba(185, 139, 255, 0.4);
      background-color: rgba(255, 255, 255, 0.1);
      color: #fff;
    }

    .btn-login {
      background: linear-gradient(90deg, var(--accent-dark), var(--accent));
      border: none;
      color: #fff;
      font-weight: 600;
      width: 100%;
      padding: 12px;
      border-radius: 10px;
      transition: 0.3s;
    }

    .btn-login:hover {
      box-shadow: 0 0 25px rgba(185, 139, 255, 0.45);
      transform: translateY(-2px);
    }

    .text-muted {
      color: var(--muted) !important;
    }

    .login-wrapper a {
      color: var(--accent);
      text-decoration: none;
      transition: color 0.3s;
    }

    .login-wrapper a:hover {
      color: var(--gold);
    }

    small {
      color: var(--muted);
    }
  </style>
</head>

<body>
  <div class="bg-glow"></div>

  <div class="login-wrapper shadow-lg">
    <div class="login-logo">Eclipsera Hotel</div>
    <div class="login-subtitle">Where elegance meets the night</div>

    <form>
      <div class="mb-3">
        <label for="email" class="form-label">Email address</label>
        <input type="email" class="form-control" id="email" placeholder="example@email.com">
      </div>

      <div class="mb-3">
        <label for="password" class="form-label">Password</label>
        <input type="password" class="form-control" id="password" placeholder="Enter your password">
      </div>

      <div class="d-flex justify-content-between align-items-center mb-3">
        <div class="form-check">
          <input class="form-check-input" type="checkbox" id="remember">
          <label class="form-check-label" for="remember">Remember me</label>
        </div>
        <a href="#">Forgot password?</a>
      </div>

      <button type="submit" class="btn-login">Sign in</button>

      <div class="text-center mt-4">
        <small>Don’t have an account? <a href="#">Register</a></small>
      </div>
    </form>
  </div>

  <audio id="bg-music" autoplay loop>
    <source src="./mp3/Dark Waltz Music - Vampire Masquerade collection.mp3" type="audio/mpeg">
  </audio>

  <script>
    // เริ่มเล่นเพลงหลังคลิกครั้งแรก
    document.addEventListener('click', function playMusic() {
      const audio = document.getElementById('bg-music');
      audio.play().catch(() => { });
      document.removeEventListener('click', playMusic);
    });

    document.getElementById('login-btn').addEventListener('click', function (e) {
    e.preventDefault(); // ป้องกันไม่ให้ form reload หน้า
    window.location.href = "Home.html"; // เปลี่ยนหน้าไป Home.html
    });
  </script>
</body>
</html>
