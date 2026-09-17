<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>बालाजी ग्रुप ऑफ सर्विसेज | मुख्य पृष्ठ</title>
    <style>
        /* प्राकृतिक कलर थीम और रीसेट */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --primary-color: #2c5e3b; /* गहरा प्राकृतिक हरा */
            --secondary-color: #8fbc8f; /* हल्का हरा (Sage Green) */
            --accent-color: #d2b48c; /* मिट्टी जैसा रंग (Tan/Gold) */
            --bg-light: #f4f7f4; /* ऑफ-व्हाइट प्राकृतिक बैकग्राउंड */
            --text-dark: #2f4f4f; /* गहरा स्लेटी/डार्क टेक्स्ट */
            --water-blue: #4a90e2; /* आरओ वाटर के लिए नीला */
        }

        body {
            background-color: var(--bg-light);
            color: var(--text-dark);
            line-height: 1.6;
        }

        /* हेडर और नेविगेशन */
        header {
            background-color: #ffffff;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
            padding: 15px 20px;
        }

        .logo-area img {
            height: 60px; /* आपके लोगो का आकार */
            vertical-align: middle;
        }

        nav a {
            text-decoration: none;
            color: var(--primary-color);
            margin: 0 15px;
            font-weight: bold;
            transition: color 0.3s;
        }

        nav a:hover {
            color: var(--accent-color);
        }

        .cta-btn {
            background-color: var(--primary-color);
            color: white;
            padding: 10px 20px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
        }

        /* मुख्य बैनर (Hero Section) */
        .hero {
            background: linear-gradient(rgba(44, 94, 59, 0.8), rgba(44, 94, 59, 0.6)), url('https://unsplash.com') no-repeat center center/cover;
            color: white;
            text-align: center;
            padding: 100px 20px;
        }

        .hero h1 {
            font-size: 2.5rem;
            margin-bottom: 20px;
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
        }

        .hero-btns .btn {
            background-color: var(--accent-color);
            color: var(--text-dark);
            padding: 12px 25px;
            margin: 10px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
            display: inline-block;
        }

        .hero-btns .btn-alt {
            background-color: transparent;
            color: white;
            border: 2px solid white;
        }

        /* ऑफर पट्टी (Discount Bar) */
        .promo-bar {
            background-color: #e67e22;
            color: white;
            text-align: center;
            padding: 12px;
            font-weight: bold;
            font-size: 1.1rem;
        }

        /* सेवाएँ (Services Grid) */
        .section-title {
            text-align: center;
            margin: 50px 0 30px;
            color: var(--primary-color);
            position: relative;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
            max-width: 1200px;
            margin: 0 auto 50px;
            padding: 0 20px;
        }

        .service-card {
            background: white;
            border-radius: 8px;
            padding: 25px;
            text-align: center;
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
            border-top: 5px solid var(--primary-color);
            transition: transform 0.3s;
        }

        .service-card:hover {
            transform: translateY(-5px);
        }

        .service-card.ro { border-top-color: var(--water-blue); }
        .service-card h3 { margin: 15px 0 10px; color: #111; }
        .service-card p { font-size: 0.95rem; color: #666; margin-bottom: 20px; }
        
        .card-btn {
            background-color: var(--primary-color);
            color: white;
            padding: 8px 15px;
            text-decoration: none;
            border-radius: 4px;
            font-size: 0.9rem;
            display: inline-block;
        }

        /* समीक्षाएँ (Testimonials) */
        .testimonials {
            background-color: #eaefe9;
            padding: 50px 20px;
        }

        .testimonial-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .testimonial-card {
            background: white;
            padding: 20px;
            border-radius: 8px;
            width: 300px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.05);
        }

        .stars { color: #f39c12; margin-bottom: 10px; }

        /* फुटर / संपर्क */
        footer {
            background-color: var(--primary-color);
            color: white;
            padding: 40px 20px 20px;
            text-align: center;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            text-align: left;
            padding-bottom: 30px;
            border-bottom: 1px solid rgba(255,255,255,0.2);
        }

        .footer-col h4 { margin-bottom: 15px; color: var(--accent-color); }
        .footer-col p, .footer-col a { color: #ddd; text-decoration: none; }
        .footer-bottom { text-align: center; padding-top: 20px; font-size: 0.9rem; color: #bbb; }

        /* रिस्पॉन्सिव मोबाइल व्यू */
        @media (max-width: 768px) {
            .nav-container { flex-direction: column; gap: 15px; text-align: center; }
            .hero h1 { font-size: 2rem; }
            .footer-col { text-align: center; }
        }
    </style>
</head>
<body>

    <!-- 1. हेडर और नेविगेशन -->
    <header>
        <div class="nav-container">
            <div class="logo-area">
                <!-- अपनी लोगो फ़ाइल का नाम यहाँ डालें (जैसे logo.png) -->
                <img src="logo.png" alt="बालाजी ग्रुप लोगो"> 
            </div>
            <nav>
                <a href="#home">होम</a>
                <a href="#services">हमारी सेवाएँ</a>
                <a href="#reviews">ग्राहक समीक्षा</a>
                <a href="#contact">संपर्क करें</a>
            </nav>
            <a href="tel:+91XXXXXXXXXX" class="cta-btn">📞 अभी कॉल करें</a>
        </div>
    </header>

    <!-- 2. विशेष डिस्काउंट ऑफर पट्टी -->
    <div class="promo-bar">
        🎉 शुभ शुरुआत ऑफर: हमारी किसी भी सर्विस की पहली बुकिंग पर पाएं फ्लैट 10% की छूट!
    </div>

    <!-- 3. मुख्य बैनर (Hero Section) -->
    <section class="hero" id="home">
        <h1>बालाजी ग्रुप ऑफ सर्विसेज</h1>
        <p>एक छत के नीचे, प्रकृति के भरोसे के साथ आपकी हर दैनिक जरूरत का विश्वसनीय समाधान। शुद्ध पानी से लेकर होम सर्विसेस तक—हमेशा आपके साथ।</p>
        <div class="hero-btns">
            <a href="#services" class="btn">हमारी सेवाएँ देखें</a>
            <a href="https://wa.me" class="btn btn-alt" target="_blank">WhatsApp बुकिंग</a>
        </div>
    </section>

    <!-- 4. हमारी सेवाएँ (Services) -->
    <section id="services">
        <h2 class="section-title">हमारी मुख्य सेवाएँ</h2>
        <div class="services-grid">
            
            <!-- आरओ वाटर -->
            <div class="service-card ro">
                <h2>💧</h2>
                <h3>बालाजी आरओ वाटर</h3>
                <p>शुद्ध जल, स्वस्थ कल। नए आरओ की बिक्री, फिल्टर बदलना और मंथली वाटर जार सप्लाई की उत्तम व्यवस्था।</p>
                <a href="tel:+91XXXXXXXXXX" class="card-btn">पानी ऑर्डर करें</a>
            </div>

            <!-- एसी सर्विस -->
            <div class="service-card">
                <h2>❄️</h2>
                <h3>बालाजी एसी सर्विस</h3>
                <p>गर्मी को कहें अलविदा। स्प्लिट और विंडो एसी इंस्टॉलेशन, गैस रिफिलिंग और डीप क्लीनिंग एक्सपर्ट्स द्वारा।</p>
                <a href="tel:+91XXXXXXXXXX" class="card-btn">मैकेनिक बुलाएँ</a>
            </div>

            <!-- स्टूडियो -->
            <div class="service-card">
                <h2>📸</h2>
                <h3>बालाजी स्टूडियो</h3>
                <p>आपकी खूबसूरत यादों को जीवंत बनाते हैं। वेडिंग फोटोग्राफी, प्री-वेडिंग शूट और बेहतरीन वीडियो एडिटिंग।</p>
                <a href="tel:+91XXXXXXXXXX" class="card-btn">तारीख बुक करें</a>
            </div>

            <!-- जनरल स्टोर -->
            <div class="service-card">
                <h2>🛒</h2>
                <h3>बालाजी जनरल स्टोर</h3>
                <p>रोजमर्रा का सामान, सबसे किफायती दाम। किराना सामान, कॉस्मेटिक्स और दैनिक जरूरत की सभी वस्तुएं उपलब्ध।</p>
                <a href="https://wa.me" class="card-btn" style="background-color: #25D366;">लिस्ट भेजें (WhatsApp)</a>
            </div>

        </div>
    </section>

    <!-- 5. ग्राहक समीक्षाएँ (Testimonials Section) -->
    <section class="testimonials" id="reviews">
        <h2 class="section-title">हमारे खुश ग्राहक क्या कहते हैं</h2>
        <div class="testimonial-container">
            
            <div class="testimonial-card">
                <div class="stars">★★★★★</div>
                <p>"बालाजी आरओ वाटर की सर्विस बहुत तेज है। पानी की क्वालिटी और जार की साफ-सफाई एकदम बढ़िया रहती है।"</p>
