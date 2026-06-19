<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Biodata - Kamelia Rusdiyanto</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet" />
    <style>
        /* ----- RESET & GLOBAL ----- */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(145deg, #fce4ec, #f3e5f5);
            padding: 20px;
        }

        /* ----- CARD UTAMA ----- */
        .card {
            max-width: 520px;
            width: 100%;
            background: rgba(255, 255, 255, 0.85);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border-radius: 48px 48px 48px 48px;
            padding: 40px 32px 36px;
            box-shadow:
                0 30px 50px rgba(0, 0, 0, 0.12),
                0 10px 25px rgba(0, 0, 0, 0.05),
                inset 0 1px 2px rgba(255, 255, 255, 0.6);
            border: 1px solid rgba(255, 255, 255, 0.5);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            text-align: center;
        }

        .card:hover {
            transform: translateY(-6px);
            box-shadow: 0 40px 65px rgba(0, 0, 0, 0.15);
        }

        /* ----- AVATAR / BADGE ----- */
        .avatar {
            width: 110px;
            height: 110px;
            border-radius: 50%;
            background: linear-gradient(135deg, #f48fb1, #ce93d8);
            margin: 0 auto 18px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 48px;
            color: #fff;
            box-shadow: 0 12px 28px rgba(206, 147, 216, 0.35);
            border: 4px solid rgba(255, 255, 255, 0.6);
            transition: transform 0.25s ease;
            user-select: none;
        }

        .avatar:hover {
            transform: scale(1.04) rotate(-2deg);
        }

        /* ----- NAMA & SUBTITLE ----- */
        .name {
            font-size: 28px;
            font-weight: 700;
            color: #4a1a4b;
            letter-spacing: -0.2px;
            margin-bottom: 2px;
        }

        .subhead {
            font-size: 15px;
            font-weight: 400;
            color: #7b4b7c;
            background: rgba(206, 147, 216, 0.18);
            display: inline-block;
            padding: 2px 18px;
            border-radius: 40px;
            margin-bottom: 22px;
            backdrop-filter: blur(4px);
            border: 1px solid rgba(255, 255, 255, 0.3);
        }

        /* ----- INFO LIST ----- */
        .info-grid {
            display: flex;
            flex-direction: column;
            gap: 14px;
            margin: 24px 0 28px;
            text-align: left;
        }

        .info-item {
            display: flex;
            align-items: center;
            gap: 14px;
            background: rgba(255, 255, 255, 0.5);
            backdrop-filter: blur(4px);
            -webkit-backdrop-filter: blur(4px);
            padding: 14px 20px;
            border-radius: 28px;
            border: 1px solid rgba(255, 255, 255, 0.5);
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.02);
            transition: background 0.2s ease, transform 0.2s ease;
        }

        .info-item:hover {
            background: rgba(255, 255, 255, 0.75);
            transform: scale(1.01);
        }

        .info-icon {
            font-size: 22px;
            width: 40px;
            height: 40px;
            background: linear-gradient(135deg, #f8bbd0, #e1bee7);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-shrink: 0;
            color: #4a1a4b;
            box-shadow: 0 4px 8px rgba(206, 147, 216, 0.2);
        }

        .info-label {
            font-weight: 600;
            font-size: 14px;
            color: #4a1a4b;
            min-width: 70px;
        }

        .info-value {
            font-weight: 400;
            font-size: 15px;
            color: #2d1a2e;
            word-break: break-word;
        }

        .info-value.motivation {
            font-style: italic;
            color: #6a3b6b;
            background: rgba(206, 147, 216, 0.12);
            padding: 2px 14px;
            border-radius: 30px;
            display: inline-block;
            border-left: 3px solid #ce93d8;
        }

        /* ----- TOMBOL PROYEK ----- */
        .btn-wrapper {
            margin-top: 8px;
            display: flex;
            justify-content: center;
        }

        .btn-proyek {
            display: inline-flex;
            align-items: center;
            gap: 12px;
            background: linear-gradient(145deg, #7b1fa2, #6a1b9a);
            color: #fff;
            font-weight: 600;
            font-size: 18px;
            padding: 16px 42px;
            border-radius: 60px;
            text-decoration: none;
            border: none;
            cursor: pointer;
            box-shadow: 0 12px 28px rgba(106, 27, 154, 0.35);
            transition: all 0.25s ease;
            letter-spacing: 0.3px;
            border: 1px solid rgba(255, 255, 255, 0.15);
            backdrop-filter: blur(4px);
        }

        .btn-proyek:hover {
            transform: translateY(-4px) scale(1.02);
            box-shadow: 0 18px 40px rgba(106, 27, 154, 0.45);
            background: linear-gradient(145deg, #8e24aa, #7b1fa2);
        }

        .btn-proyek:active {
            transform: scale(0.96);
            box-shadow: 0 6px 16px rgba(106, 27, 154, 0.3);
        }

        .btn-proyek .icon-arrow {
            font-size: 22px;
            transition: transform 0.25s ease;
        }

        .btn-proyek:hover .icon-arrow {
            transform: translateX(4px) rotate(-6deg);
        }

        /* ----- FOOTER KECIL ----- */
        .footer-note {
            margin-top: 22px;
            font-size: 12px;
            color: #9b7b9c;
            letter-spacing: 0.3px;
            opacity: 0.7;
            border-top: 1px solid rgba(206, 147, 216, 0.2);
            padding-top: 18px;
        }

        /* ----- RESPONSIVE ----- */
        @media (max-width: 480px) {
            .card {
                padding: 30px 18px 28px;
                border-radius: 32px;
            }

            .name {
                font-size: 22px;
            }

            .info-item {
                padding: 12px 14px;
                gap: 10px;
            }

            .info-label {
                min-width: 56px;
                font-size: 12px;
            }

            .info-value {
                font-size: 13px;
            }

            .btn-proyek {
                font-size: 16px;
                padding: 14px 30px;
            }

            .avatar {
                width: 85px;
                height: 85px;
                font-size: 36px;
            }
        }

        @media (max-width: 380px) {
            .info-item {
                flex-wrap: wrap;
                gap: 4px 10px;
            }

            .info-label {
                min-width: 100%;
            }
        }
    </style>
</head>
<body>

    <div class="card" role="main" aria-label="Kartu biodata Kamelia Rusdiyanto">

        <!-- Avatar -->
        <div class="avatar" aria-hidden="true">🌸</div>

        <!-- Nama & sub -->
        <h1 class="name">Kamelia Rusdiyanto</h1>
        <span class="subhead">✨ #Semangat ✨</span>

        <!-- Info Biodata -->
        <div class="info-grid">

            <!-- Tanggal Lahir -->
            <div class="info-item">
                <span class="info-icon" aria-hidden="true">📅</span>
                <span class="info-label">Lahir</span>
                <span class="info-value"><strong>19 / 01 / 2011</strong></span>
            </div>

            <!-- Hobi -->
            <div class="info-item">
                <span class="info-icon" aria-hidden="true">🎬</span>
                <span class="info-label">Hobi</span>
                <span class="info-value">Menonton</span>
            </div>

            <!-- Cita-cita -->
            <div class="info-item">
                <span class="info-icon" aria-hidden="true">💐</span>
                <span class="info-label">Cita-cita</span>
                <span class="info-value">Tukang Bunga</span>
            </div>

            <!-- Motivasi -->
            <div class="info-item">
                <span class="info-icon" aria-hidden="true">🔥</span>
                <span class="info-label">Motivasi</span>
                <span class="info-value motivation">“Jangan pernah menyerah melewati rintangan”</span>
            </div>

        </div>

        <!-- Tombol Proyek -->
        <div class="btn-wrapper">
            <a href="https://github.com/amel150/Aqua-blast.git"
            target="_blank"
            rel="noopener noreferrer"
            class="btn-proyek"
            aria-label="Buka proyek Aqua-blast di GitHub">
            <span>📂 Proyek</span>
            <span class="icon-arrow" aria-hidden="true">➜</span>
        </a>
    </div>

    <!-- Footer kecil -->
    <div class="footer-note">
        🌱  jangan pernah menyerah  🌱
    </div>

</div>

</body>
</html>
