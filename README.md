<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Happy New Year 2026</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <!-- Confetti library (canvas-confetti) [web:15] -->
  <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.9.2/dist/confetti.browser.min.js"></script>

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: "Poppins", system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
    }

    body {
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      background: radial-gradient(circle at top, #1f3b73 0, #050816 55%, #000 100%);
      color: #fff;
      overflow: hidden;
    }

    .container {
      text-align: center;
      position: relative;
      z-index: 2;
      padding: 20px;
    }

    .small-text {
      letter-spacing: 4px;
      text-transform: uppercase;
      font-size: 14px;
      color: #facc15;
      animation: fadeInDown 1.2s ease-out forwards;
      opacity: 0;
    }

    .year {
      font-size: clamp(64px, 10vw, 120px);
      font-weight: 800;
      letter-spacing: 6px;
      margin: 10px 0;
      background: linear-gradient(120deg, #f97316, #facc15, #22c55e, #0ea5e9, #a855f7);
      -webkit-background-clip: text;
      color: transparent;
      animation: glow 2s ease-in-out infinite alternate, scaleIn 1.4s ease-out forwards;
      opacity: 0;
    }

    .message {
      font-size: 20px;
      max-width: 600px;
      margin: 10px auto 24px;
      line-height: 1.6;
      color: #e5e7eb;
      animation: fadeInUp 1.2s ease-out 0.3s forwards;
      opacity: 0;
    }

    .btn {
      margin-top: 10px;
      padding: 12px 30px;
      border-radius: 999px;
      border: 0;
      background: linear-gradient(135deg, #22c55e, #0ea5e9);
      color: #020617;
      font-size: 16px;
      font-weight: 600;
      cursor: pointer;
      box-shadow: 0 10px 30px rgba(34, 197, 94, 0.35);
      transition: transform 0.18s ease, box-shadow 0.18s ease, filter 0.18s ease;
      animation: fadeInUp 1.2s ease-out 0.6s forwards;
      opacity: 0;
    }

    .btn:hover {
      transform: translateY(-2px) scale(1.03);
      filter: brightness(1.05);
      box-shadow: 0 16px 40px rgba(34, 197, 94, 0.5);
    }

    .btn:active {
      transform: translateY(0) scale(0.98);
      box-shadow: 0 6px 20px rgba(15, 23, 42, 0.8);
    }

    /* Floating glowing circles background */
    .bubble {
      position: absolute;
      border-radius: 50%;
      background: radial-gradient(circle, rgba(248, 250, 252, 0.95), transparent 60%);
      opacity: 0.15;
      pointer-events: none;
      animation: floatUp 12s linear infinite;
      mix-blend-mode: screen;
    }

    .bubble:nth-child(1) { width: 160px; height: 160px; left: 10%; bottom: -160px; animation-delay: 0s; }
    .bubble:nth-child(2) { width: 220px; height: 220px; left: 55%; bottom: -220px; animation-delay: 3s; }
    .bubble:nth-child(3) { width: 120px; height: 120px; left: 80%; bottom: -140px; animation-delay: 5s; }
    .bubble:nth-child(4) { width: 190px; height: 190px; left: 30%; bottom: -190px; animation-delay: 7s; }

    /* Starry background */
    .stars::before,
    .stars::after {
      content: "";
      position: fixed;
      inset: 0;
      background-image:
        radial-gradient(1px 1px at 10% 20%, rgba(248, 250, 252, 0.9) 0, transparent 50%),
        radial-gradient(1px 1px at 80% 10%, rgba(248, 250, 252, 0.6) 0, transparent 50%),
        radial-gradient(1px 1px at 50% 80%, rgba(248, 250, 252, 0.75) 0, transparent 50%);
      opacity: 0.5;
      z-index: 0;
    }

    .stars::after {
      animation: twinkle 4s linear infinite;
      opacity: 0.3;
    }

    /* Keyframes */
    @keyframes glow {
      from {
        text-shadow:
          0 0 10px rgba(248, 250, 252, 0.7),
          0 0 30px rgba(250, 204, 21, 0.5),
          0 0 60px rgba(56, 189, 248, 0.5);
      }
      to {
        text-shadow:
          0 0 16px rgba(248, 250, 252, 0.9),
          0 0 50px rgba(250, 204, 21, 0.85),
          0 0 90px rgba(129, 140, 248, 0.95);
      }
    }

    @keyframes scaleIn {
      from {
        transform: scale(0.8);
        opacity: 0;
      }
      to {
        transform: scale(1);
        opacity: 1;
      }
    }

    @keyframes fadeInDown {
      from {
        transform: translateY(-20px);
        opacity: 0;
      }
      to {
        transform: translateY(0);
        opacity: 1;
      }
    }

    @keyframes fadeInUp {
      from {
        transform: translateY(20px);
        opacity: 0;
      }
      to {
        transform: translateY(0);
        opacity: 1;
      }
    }

    @keyframes floatUp {
      from {
        transform: translateY(0) translateX(0);
      }
      to {
        transform: translateY(-120vh) translateX(40px);
      }
    }

    @keyframes twinkle {
      0%, 100% { opacity: 0.3; }
      50% { opacity: 0.8; }
    }

    /* Responsive tweaks */
    @media (max-width: 600px) {
      .message {
        font-size: 16px;
        padding: 0 10px;
      }
      .small-text {
        font-size: 12px;
      }
    }
  </style>
</head>
<body class="stars">
  <!-- Glowing floating bubbles -->
  <div class="bubble"></div>
  <div class="bubble"></div>
  <div class="bubble"></div>
  <div class="bubble"></div>

  <div class="container">
    <div class="small-text">Cheers to a bright</div>
    <div class="year">2026</div>
    <p class="message">
      Wishing you a year full of joy, success, and endless possibilities. May all your dreams shine brighter than the fireworks in the sky!
    </p>
    <button class="btn" id="celebrateBtn">Celebrate 🎉</button>
  </div>

  <script>
    // Auto confetti burst on load
    function fireConfettiBurst() {
      confetti({
        particleCount: 160,
        spread: 70,
        origin: { y: 0.6 }
      });

      // Left and right side bursts
      confetti({
        particleCount: 80,
        angle: 60,
        spread: 55,
        origin: { x: 0, y: 0.8 }
      });

      confetti({
        particleCount: 80,
        angle: 120,
        spread: 55,
        origin: { x: 1, y: 0.8 }
      });
    }

    // Fireworks-style continuous confetti for a short time [web:15]
    function fireworksShow(duration = 3000) {
      const end = Date.now() + duration;

      (function frame() {
        // random bursts
        confetti({
          particleCount: 5,
          angle: 60,
          spread: 75,
          origin: { x: Math.random() * 0.3, y: Math.random() * 0.7 }
        });
        confetti({
          particleCount: 5,
          angle: 120,
          spread: 75,
          origin: { x: 0.7 + Math.random() * 0.3, y: Math.random() * 0.7 }
        });

        if (Date.now() < end) {
          requestAnimationFrame(frame);
        }
      })();
    }

    window.addEventListener("load", () => {
      // small delay so animations start nicely
      setTimeout(() => {
        fireConfettiBurst();
        fireworksShow(2500);
      }, 600);
    });

    document.getElementById("celebrateBtn").addEventListener("click", () => {
      fireConfettiBurst();
      fireworksShow(2500);
    });
  </script>
</body>
</html>
