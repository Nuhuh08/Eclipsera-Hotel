<!doctype html>
<html lang="en">

<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Eclipsera Hotel — Login</title>

  <!-- Google font -->
  <link rel="preconnect" href="https://fonts.gstatic.com">
  <link
    href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap"
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
      --card-bg: #15121f;
      --text: #e5e3f5;
    }

    body {
      font-family: 'Inter', system-ui, -apple-system, 'Segoe UI', Roboto, sans-serif;
      background: radial-gradient(circle at top, #1c1529 0%, #0b0a13 90%);
      color: var(--text);
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      overflow: hidden;
    }

    .login-wrapper {
      position: relative;
      z-index: 2;
      width: 100%;
      max-width: 420px;
      background: rgba(21, 18, 31, 0.9);
      border: 1px solid rgba(185, 139, 255, 0.3);
      border-radius: 18px;
      padding: 40px 36px;
      box-shadow: 0 0 40px rgba(185, 139, 255, 0.15);
      backdrop-filter: blur(12px);
    }

    .login-wrapper h2 {
      color: var(--gold);
      font-weight: 700;
      text-align: center;
      margin-bottom: 20px;
      text-shadow: 0 0 8px rgba(217, 182, 90, 0.4);
    }

    .form-control {
      background-color: rgba(255, 255, 255, 0.07);
      border: 1px solid rgba(185, 139, 255, 0.25);
      color: var(--text);
      border-radius: 10px;
    }

    .form-control:focus {
      border-color: var(--accent);
      box-shadow: 0 0 8px rgba(185, 139, 255, 0.4);
      background-color: rgba(255, 255, 255, 0.1);
      color: #fff;
    }

    .btn-login {
      background: linear-gradient(90deg, var(--accent-dark), var(--accent));
      border: none;
      color: #fff;
      font-weight: 600;
      width: 100%;
      padding: 10px;
      border-radius: 10px;
      transition: 0.3s;
    }

    .btn-login:hover {
      box-shadow: 0 0 20px rgba(185, 139, 255, 0.4);
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

    /* แสงตกแต่งพื้นหลัง */
    .bg-glow {
      position: absolute;
      width: 600px;
      height: 600px;
      border-radius: 50%;
      background: radial-gradient(circle, rgba(185, 139, 255, 0.25), transparent 70%);
      filter: blur(60px);
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      z-index: 1;
      animation: pulse 6s infinite ease-in-out;
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

    small {
      color: var(--muted);
    }

  </style>
</head>

<body>

  <div class="bg-glow"></div>

  <div class="login-wrapper">
    <h2>Welcome back</h2>
    <form>
      <div class="mb-3">
        <label for="email" class="form-label">Email address</label>
        <input type="email" class="form-control" id="email" placeholder="Enter your email">
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

      <button type="submit" class="btn-login">Login</button>

      <div class="text-center mt-4">
        <small>Don’t have an account? <a href="#">Register</a></small>
      </div>
    </form>
  </div>

  <audio id="bg-music" autoplay loop>
    <source src="./mp3/Dark Waltz Music - Vampire Masquerade collection.mp3" type="audio/mpeg">
  </audio>

  <script>
    // กดคลิกถึงจะเริ่มเล่นเพลง
    document.addEventListener('click', function playMusic() {
      const audio = document.getElementById('bg-music');
      audio.play().catch(() => { });
      document.removeEventListener('click', playMusic);
    });
  </script>

</body>
</html>
