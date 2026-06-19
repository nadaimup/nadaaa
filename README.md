<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Biodata - Qotrunnada Salsabila</title>
    <style>
        :root {
            --bg: #fef9f3;
            --card-bg: #ffffff;
            --primary: #e88d7c;
            --primary-hover: #d47565;
            --accent: #f4c7b8;
            --text: #4a3f3b;
            --text-light: #7a6e68;
            --border: #f0e4db;
            --shadow: 0 8px 32px rgba(120, 80, 60, 0.08);
            --shadow-hover: 0 14px 40px rgba(120, 80, 60, 0.14);
            --radius: 22px;
            --radius-sm: 14px;
            --transition: 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', 'Inter', system-ui, -apple-system, sans-serif;
            background: linear-gradient(160deg, #fef5f0 0%, #fdf0e8 30%, #fef9f5 60%, #fff5f0 100%);
            background-attachment: fixed;
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 20px;
            position: relative;
            overflow-x: hidden;
        }

        /* Background decorations */
        body::before {
            content: '';
            position: fixed;
            top: -120px;
            right: -120px;
            width: 380px;
            height: 380px;
            background: radial-gradient(circle, rgba(232, 141, 124, 0.12) 0%, transparent 70%);
            border-radius: 50%;
            pointer-events: none;
            z-index: 0;
            animation: floatBubble1 12s ease-in-out infinite;
        }

        body::after {
            content: '';
            position: fixed;
            bottom: -100px;
            left: -100px;
            width: 340px;
            height: 340px;
            background: radial-gradient(circle, rgba(244, 199, 184, 0.14) 0%, transparent 70%);
            border-radius: 50%;
            pointer-events: none;
            z-index: 0;
            animation: floatBubble2 14s ease-in-out infinite;
        }

        @keyframes floatBubble1 {
            0%,
            100% {
                transform: translate(0, 0) scale(1);
            }
            25% {
                transform: translate(-30px, 25px) scale(1.08);
            }
            50% {
                transform: translate(10px, -15px) scale(0.94);
            }
            75% {
                transform: translate(20px, 30px) scale(1.05);
            }
        }

        @keyframes floatBubble2 {
            0%,
            100% {
                transform: translate(0, 0) scale(1);
            }
            30% {
                transform: translate(35px, -20px) scale(1.06);
            }
            60% {
                transform: translate(-15px, -30px) scale(0.93);
            }
            85% {
                transform: translate(-25px, 10px) scale(1.04);
            }
        }

        .card {
            position: relative;
            z-index: 1;
            background: var(--card-bg);
            border-radius: var(--radius);
            box-shadow: var(--shadow);
            padding: 44px 38px 36px;
            max-width: 470px;
            width: 100%;
            text-align: center;
            transition: box-shadow var(--transition), transform var(--transition);
            border: 1px solid var(--border);
        }

        .card:hover {
            box-shadow: var(--shadow-hover);
            transform: translateY(-4px);
        }

        /* Avatar */
        .avatar-wrapper {
            position: relative;
            display: inline-block;
            margin-bottom: 20px;
        }

        .avatar {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            background: linear-gradient(135deg, #fce4dc 0%, #f8cbbb 40%, #f0a996 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 52px;
            color: #ffffff;
            margin: 0 auto;
            box-shadow: 0 8px 28px rgba(232, 141, 124, 0.3);
            position: relative;
            z-index: 1;
            transition: transform var(--transition);
            user-select: none;
        }

        .avatar:hover {
            transform: scale(1.06);
        }

        .avatar-dot {
            position: absolute;
            bottom: 8px;
            right: 10px;
            width: 18px;
            height: 18px;
            background: #7ecb8a;
            border-radius: 50%;
            border: 3px solid #fff;
            z-index: 2;
            animation: pulse 2.2s ease-in-out infinite;
        }

        @keyframes pulse {
            0%,
            100% {
                box-shadow: 0 0 0 0 rgba(126, 203, 138, 0.55);
            }
            50% {
                box-shadow: 0 0 0 16px rgba(126, 203, 138, 0);
            }
        }

        /* Name */
        .name {
            font-size: 1.75rem;
            font-weight: 700;
            color: var(--text);
            margin-bottom: 4px;
            letter-spacing: -0.3px;
            line-height: 1.25;
        }

        .name-emoji {
            display: inline-block;
            animation: wave 2s ease-in-out infinite;
            transform-origin: 70% 70%;
            font-size: 1.5rem;
        }

        @keyframes wave {
            0%,
            100% {
                transform: rotate(0deg);
            }
            20% {
                transform: rotate(14deg);
            }
            40% {
                transform: rotate(-8deg);
            }
            60% {
                transform: rotate(10deg);
            }
            80% {
                transform: rotate(-4deg);
            }
        }

        /* Badge usia */
        .age-badge {
            display: inline-block;
            background: var(--accent);
            color: #8b4a3a;
            font-size: 0.8rem;
            font-weight: 600;
            padding: 5px 14px;
            border-radius: 20px;
            margin-top: 2px;
            letter-spacing: 0.3px;
        }

        /* Divider */
        .divider {
            width: 50px;
            height: 3px;
            background: var(--accent);
            border-radius: 3px;
            margin: 18px auto;
            opacity: 0.7;
        }

        /* Info grid */
        .info-grid {
            display: flex;
            flex-direction: column;
            gap: 13px;
            text-align: left;
            margin-bottom: 10px;
        }

        .info-row {
            display: flex;
            align-items: flex-start;
            gap: 14px;
            padding: 13px 16px;
            background: #fefbf9;
            border-radius: var(--radius-sm);
            transition: background var(--transition), transform var(--transition);
            border: 1px solid transparent;
        }

        .info-row:hover {
            background: #fffaf7;
            border-color: #fbe9e1;
            transform: translateX(3px);
        }

        .info-icon {
            flex-shrink: 0;
            width: 42px;
            height: 42px;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.3rem;
        }

        .icon-birth {
            background: #fef0ea;
        }
        .icon-hobby {
            background: #fdf3ef;
        }
        .icon-dream {
            background: #fff4ef;
        }
        .icon-motiv {
            background: #fff7f3;
        }

        .info-label {
            font-size: 0.72rem;
            text-transform: uppercase;
            letter-spacing: 0.8px;
            color: var(--text-light);
            font-weight: 600;
            margin-bottom: 2px;
        }

        .info-value {
            font-size: 0.98rem;
            color: var(--text);
            font-weight: 500;
            line-height: 1.4;
        }

        /* Motivasi highlight */
        .motivasi-highlight {
            background: linear-gradient(135deg, #fff8f5 0%, #fff3ed 100%);
            border-radius: var(--radius-sm);
            padding: 16px 20px;
            margin: 16px 0 10px;
            border: 1.5px dashed #f0cfbf;
            position: relative;
        }

        .motivasi-highlight .info-label {
            color: #c07a62;
        }
        .motivasi-highlight .info-value {
            font-style: italic;
            font-weight: 600;
            font-size: 1.05rem;
            color: #6b3d2e;
        }

        .sparkle {
            position: absolute;
            top: -8px;
            right: -6px;
            font-size: 1.4rem;
            animation: sparkleFloat 2.5s ease-in-out infinite;
        }

        @keyframes sparkleFloat {
            0%,
            100% {
                transform: translateY(0) scale(1);
                opacity: 0.7;
            }
            50% {
                transform: translateY(-10px) scale(1.25);
                opacity: 1;
            }
        }

        /* Button */
        .btn-project {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            background: var(--primary);
            color: #fff;
            font-weight: 600;
            font-size: 1rem;
            padding: 14px 30px;
            border-radius: 50px;
            text-decoration: none;
            letter-spacing: 0.3px;
            transition: all var(--transition);
            box-shadow: 0 6px 22px rgba(232, 141, 124, 0.35);
            border: none;
            cursor: pointer;
            margin-top: 12px;
            position: relative;
            overflow: hidden;
        }

        .btn-project::after {
            content: '';
            position: absolute;
            inset: 0;
            background: linear-gradient(135deg, rgba(255, 255, 255, 0.2) 0%, transparent 60%);
            border-radius: 50px;
            pointer-events: none;
        }

        .btn-project:hover {
            background: var(--primary-hover);
            box-shadow: 0 10px 30px rgba(212, 117, 101, 0.45);
            transform: translateY(-3px);
            gap: 14px;
        }

        .btn-project:active {
            transform: scale(0.96);
            box-shadow: 0 3px 12px rgba(212, 117, 101, 0.4);
            transition: 0.1s;
        }

        .btn-arrow {
            display: inline-block;
            transition: transform var(--transition);
            font-size: 1.15rem;
        }
        .btn-project:hover .btn-arrow {
            transform: translateX(5px);
        }

        /* Footer kecil */
        .footer-note {
            font-size: 0.7rem;
            color: #c5b5aa;
            margin-top: 20px;
            letter-spacing: 0.4px;
        }

        /* Responsive */
        @media (max-width: 480px) {
            .card {
                padding: 30px 20px 26px;
                border-radius: 18px;
            }
            .avatar {
                width: 96px;
                height: 96px;
                font-size: 42px;
            }
            .name {
                font-size: 1.45rem;
            }
            .info-row {
                gap: 10px;
                padding: 11px 12px;
            }
            .info-icon {
                width: 36px;
                height: 36px;
                font-size: 1.1rem;
                border-radius: 10px;
            }
            .btn-project {
                padding: 12px 24px;
                font-size: 0.9rem;
            }
        }
    </style>
</head>
<body>

    <div class="card">
        <!-- Avatar -->
        <div class="avatar-wrapper">
            <div class="avatar" aria-label="Avatar Qotrunnada Salsabila">🌸</div>
            <div class="avatar-dot" title="Online"></div>
        </div>

        <!-- Nama -->
        <h1 class="name">Qotrunnada Salsabila <span class="name-emoji">✨</span></h1>
        <span class="age-badge">🎂 23 Mei 2013</span>

        <div class="divider"></div>

        <!-- Info Grid -->
        <div class="info-grid">
            <!-- Tanggal Lahir -->
            <div class="info-row">
                <div class="info-icon icon-birth">🎀</div>
                <div>
                    <div class="info-label">Tanggal Lahir</div>
                    <div class="info-value">23 Mei 2013</div>
                </div>
            </div>

            <!-- Hobi -->
            <div class="info-row">
                <div class="info-icon icon-hobby">📚</div>
                <div>
                    <div class="info-label">Hobi</div>
                    <div class="info-value">Membaca Novel &amp; Menggambar</div>
                </div>
            </div>

            <!-- Cita-cita -->
            <div class="info-row">
                <div class="info-icon icon-dream">🧠</div>
                <div>
                    <div class="info-label">Cita-cita</div>
                    <div class="info-value">Psikolog</div>
                </div>
            </div>
        </div>

        <!-- Motivasi -->
        <div class="motivasi-highlight">
            <span class="sparkle">💤</span>
            <div class="info-label">✨ Motivasi Hidup</div>
            <div class="info-value">"Jangan Lupa Tidur"</div>
        </div>

        <!-- Tombol Projek -->
        <a href="https://nadaimup.github.io/Jualan-EsCendol/"
        class="btn-project"
        target="_blank"
        rel="noopener noreferrer"
        title="Kunjungi Projek Jualan Es Cendol">
        🍧 Lihat Projek Es Cendol
        <span class="btn-arrow">→</span>
    </a>

    <!-- Footer kecil -->
    <p class="footer-note">💖 dibuat dengan semangat &middot; 2024</p>
</div>

</body>
</html>
