<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Deniz İskenderhan | Resmi Web Sitesi</title>
    <style>
        /* Temel Stil Ayarları */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #0b0b0b;
            color: #ffffff;
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Navigasyon Menüsü */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            background-color: rgba(11, 11, 11, 0.95);
            padding: 20px 50px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            z-index: 1000;
            border-bottom: 1px solid #1a1a1a;
        }

        .logo {
            font-size: 24px;
            font-weight: bold;
            letter-spacing: 2px;
            color: #fff;
            text-transform: uppercase;
        }

        nav a {
            color: #a0a0a0;
            text-decoration: none;
            margin-left: 30px;
            font-size: 16px;
            transition: color 0.3s;
            cursor: pointer;
        }

        nav a:hover, nav a.active {
            color: #ffffff;
        }

        /* Sayfa Bölümleri */
        section {
            padding: 120px 50px 80px 50px;
            min-height: 100vh;
            display: none; /* Sayfalar varsayılan olarak gizli */
        }

        section.active-section {
            display: block; /* Sadece aktif sayfa görünür */
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        h2 {
            font-size: 36px;
            margin-bottom: 40px;
            text-transform: uppercase;
            letter-spacing: 2px;
            border-bottom: 2px solid #1a1a1a;
            padding-bottom: 10px;
        }

        /* 1. Ana Sayfa (Home) */
        #home {
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            background: linear-gradient(rgba(11,11,11,0.7), rgba(11,11,11,1)), url('arka-plan.jpg') no-repeat center center/cover;
        }

        .hero-content h1 {
            font-size: 64px;
            letter-spacing: 4px;
            margin-bottom: 20px;
            text-transform: uppercase;
        }

        .hero-content p {
            font-size: 18px;
            color: #a0a0a0;
            margin-bottom: 40px;
        }

        .btn {
            display: inline-block;
            padding: 15px 40px;
            background-color: #ffffff;
            color: #0b0b0b;
            text-decoration: none;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: background 0.3s;
        }

        .btn:hover {
            background-color: #cccccc;
        }

        /* 2. Diskografi (Müzik) */
        .music-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 300px 40px;
        }

        .release-card {
            background-color: #111111;
            border: 1px solid #1a1a1a;
            padding: 20px;
            text-align: center;
        }

        .release-card img {
            width: 100%;
            height: auto;
            margin-bottom: 20px;
        }

        .release-card h3 {
            font-size: 20px;
            margin-bottom: 10px;
        }

        .listen-links a {
            color: #ffffff;
            margin: 0 10px;
            text-decoration: underline;
            font-size: 14px;
        }

        /* 3. Biyografi (Hakkında) */
        .bio-text {
            font-size: 18px;
            color: #cccccc;
            max-width: 800px;
            margin-bottom: 30px;
        }

        /* 4. Topluluk (Telegram & İletişim) */
        .community-box {
            background-color: #111111;
            border: 1px solid #1a1a1a;
            padding: 40px;
            border-radius: 4px;
            text-align: center;
            max-width: 600px;
            margin: 0 auto;
        }

        .telegram-btn {
            background-color: #0088cc;
            color: white;
            padding: 12px 30px;
            border-radius: 20px;
            text-navigation: none;
            display: inline-block;
            margin-top: 20px;
            font-weight: bold;
            text-decoration: none;
        }
    </style>
</head>
<body>

    <!-- Navigasyon -->
    <header>
        <div class="logo">Deniz İskenderhan</div>
        <nav>
            <a onclick="showSection('home')" id="nav-home" class="active">Ana Sayfa</a>
            <a onclick="showSection('music')" id="nav-music">Müzik</a>
            <a onclick="showSection('bio')" id="nav-bio">Biyografi</a>
            <a onclick="showSection('community')" id="nav-community">Topluluk</a>
        </nav>
    </header>

    <!-- 1. Ana Sayfa -->
    <section id="home" class="active-section">
        <div class="hero-content">
            <h1>Deniz İskenderhan</h1>
            <p>Resmi Web Sitesine Hoş Geldiniz</p>
            <a onclick="showSection('music')" class="btn">Son Çalışmayı Dinle</a>
        </div>
    </section>

    <!-- 2. Müzik / Diskografi -->
    <section id="music">
        <div class="container">
            <h2>Müzik</h2>
            <div class="music-grid">
                <!-- Örnek Şarkı Kartı -->
                <div class="release-card">
                    <img src="recete-cover.jpg" alt="Reçete Cover">
                    <h3>Reçete</h3>
                    <p style="color: #a0a0a0; margin-bottom: 15px;">Single (2026)</p>
                    <div class="listen-links">
                        <a href="#" target="_blank">Spotify</a>
                        <a href="#" target="_blank">Apple Music</a>
                        <a href="#" target="_blank">YouTube</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 3. Biyografi -->
    <section id="bio">
        <div class="container">
            <h2>Biyografi</h2>
            <div class="bio-text">
                <p>Müziğin ve sözlerin derinliğine odaklanan, bağımsız bir sanatsal vizyonla şekillenen dinamik melodiler.</p>
                <br>
                <p>Kendi kurallarını koyan ve hikayesini doğrudan dinleyicisine aktaran özgün müzikal yolculuk.</p>
            </div>
        </div>
    </section>

    <!-- 4. Topluluk / Telegram -->
    <section id="community">
        <div class="container">
            <h2>Topluluk</h2>
            <div class="community-box">
                <h3>Resmi Telegram Kanalı</h3>
                <p style="margin-top: 15px; color: #a0a0a0;">Yeni şarkılardan, yayınlanmamış demolardan ve en güncel gelişmelerden anında haberdar olmak için topluluğumuza katılın.</p>
                <a href="#" target="_blank" class="telegram-btn">Kanalımıza Katıl</a>
            </div>
        </div>
    </section>

    <!-- Sayfa Geçiş JavaScript Kodu -->
    <script>
        function showSection(sectionId) {
            // Tüm bölümleri gizle
            const sections = document.querySelectorAll('section');
            sections.forEach(sec => sec.classList.remove('active-section'));

            // Tüm menü linklerinin aktifliğini kaldır
            const links = document.querySelectorAll('nav a');
            links.forEach(link => link.classList.remove('active'));

            // Seçilen bölümü göster ve menü linkini aktif yap
            document.getElementById(sectionId).classList.add('active-section');
            document.getElementById('nav-' + sectionId).classList.add('active');

            // Sayfayı yukarı kaydır
            window.scrollTo(0, 0);
        }
    </script>
</body>
</html>
