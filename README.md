<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EliteMotors  | Ultimate Car Platform</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700&family=Oswald:wght@500;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #d40000;
            --primary-dark: #a30000;
            --secondary: #1a1a1a;
            --accent: #0077cc;
            --light: #f5f5f5;
            --gray: #e0e0e0;
            --dark-gray: #666;
            --shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            --transition: all 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Montserrat', sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f9f9f9;
        }

        h1, h2, h3, h4, h5 {
            font-family: 'Oswald', sans-serif;
            font-weight: 600;
            margin-bottom: 1rem;
            color: var(--secondary);
        }

        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header & Navigation */
        header {
            background-color: var(--secondary);
            color: white;
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: var(--shadow);
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: white;
            display: flex;
            align-items: center;
        }

        .logo i {
            color: var(--primary);
            margin-right: 10px;
        }

        .logo span {
            color: var(--primary);
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav ul li {
            margin-left: 1.5rem;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: var(--transition);
            padding: 5px 0;
            position: relative;
        }

        nav ul li a:hover {
            color: var(--primary);
        }

        nav ul li a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--primary);
            transition: var(--transition);
        }

        nav ul li a:hover::after {
            width: 100%;
        }

        .user-actions {
            display: flex;
            align-items: center;
        }

        .user-actions a {
            color: white;
            margin-left: 1rem;
            font-size: 1.2rem;
            transition: var(--transition);
        }

        .user-actions a:hover {
            color: var(--primary);
        }

        .search-box {
            display: flex;
            align-items: center;
            background: white;
            border-radius: 30px;
            padding: 8px 15px;
            margin-left: 1rem;
        }

        .search-box input {
            border: none;
            outline: none;
            width: 200px;
            padding: 5px;
        }

        .search-box button {
            background: none;
            border: none;
            color: var(--secondary);
            cursor: pointer;
        }

        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://i.pinimg.com/originals/65/b2/d0/65b2d094463069b3cea8242a38d6d64c.jpg');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 6rem 0;
            text-align: center;
        }

        .hero h1 {
            font-size: 3.5rem;
            color: white;
            margin-bottom: 1.5rem;
            text-transform: uppercase;
        }

        .hero p {
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto 2rem;
        }

        .cta-buttons {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-top: 2rem;
        }

        .btn {
            display: inline-block;
            padding: 12px 30px;
            background-color: var(--primary);
            color: white;
            text-decoration: none;
            border-radius: 30px;
            font-weight: 600;
            transition: var(--transition);
            border: none;
            cursor: pointer;
            font-size: 1rem;
        }

        .btn:hover {
            background-color: var(--primary-dark);
            transform: translateY(-3px);
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.2);
        }

        .btn-outline {
            background-color: transparent;
            border: 2px solid white;
        }

        .btn-outline:hover {
            background-color: white;
            color: var(--secondary);
        }

        /* Sections */
        section {
            padding: 5rem 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            position: relative;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background-color: var(--primary);
        }

        /* Car Grid */
        .car-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
        }

        .car-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
        }

        .car-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
        }

        .car-image {
            height: 200px;
            width: 100%;
            object-fit: cover;
        }

        .car-info {
            padding: 1.5rem;
        }

        .car-info h3 {
            margin-bottom: 0.5rem;
        }

        .car-price {
            color: var(--primary);
            font-weight: 700;
            font-size: 1.2rem;
            margin-bottom: 1rem;
        }

        .car-features {
            display: flex;
            justify-content: space-between;
            margin-bottom: 1rem;
            font-size: 0.9rem;
            color: var(--dark-gray);
        }

        /* Search Section */
        .search-container {
            background-color: white;
            padding: 3rem;
            border-radius: 10px;
            box-shadow: var(--shadow);
            margin-top: 2rem;
        }

        .search-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 2rem;
        }

        .knowledge-results {
            margin-top: 2rem;
        }

        .knowledge-item {
            background-color: var(--light);
            padding: 1.5rem;
            border-radius: 8px;
            margin-bottom: 1rem;
            border-left: 4px solid var(--accent);
        }

        /* Community Section */
        .forum-container {
            display: grid;
            grid-template-columns: 2fr 1fr;
            gap: 2rem;
        }

        .post-form {
            background-color: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: var(--shadow);
            margin-bottom: 2rem;
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
        }

        .form-group input,
        .form-group textarea,
        .form-group select {
            width: 100%;
            padding: 12px;
            border: 1px solid var(--gray);
            border-radius: 5px;
            font-family: 'Montserrat', sans-serif;
        }

        .community-posts {
            background-color: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: var(--shadow);
        }

        .post {
            border-bottom: 1px solid var(--gray);
            padding: 1.5rem 0;
        }

        .post:last-child {
            border-bottom: none;
        }

        .post-header {
            display: flex;
            justify-content: space-between;
            margin-bottom: 1rem;
        }

        .post-user {
            display: flex;
            align-items: center;
        }

        .user-avatar {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background-color: var(--primary);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: 600;
            margin-right: 10px;
        }

        .expert-badge {
            background-color: var(--accent);
            color: white;
            padding: 3px 8px;
            border-radius: 20px;
            font-size: 0.8rem;
            margin-left: 10px;
        }

        /* Car Customizer */
        .customizer-container {
            display: grid;
            grid-template-columns: 1fr 2fr;
            gap: 2rem;
        }

        .customizer-controls {
            background-color: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: var(--shadow);
        }

        .customizer-preview {
            background-color: var(--secondary);
            border-radius: 10px;
            padding: 2rem;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 500px;
        }

        .car-visualization {
            width: 100%;
            height: 300px;
            background-color: #333;
            border-radius: 10px;
            margin-bottom: 2rem;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            position: relative;
        }

        .car-part {
            position: absolute;
            background-color: rgba(255, 255, 255, 0.1);
            border: 1px dashed rgba(255, 255, 255, 0.3);
            padding: 10px;
            border-radius: 5px;
            cursor: pointer;
            transition: var(--transition);
        }

        .car-part:hover {
            background-color: rgba(255, 255, 255, 0.2);
        }

        .engine { top: 50%; left: 20%; width: 60px; height: 40px; }
        .spoiler { top: 10%; left: 40%; width: 80px; height: 20px; }
        .wheel-front { bottom: 10%; left: 25%; width: 40px; height: 40px; border-radius: 50%; }
        .wheel-back { bottom: 10%; right: 25%; width: 40px; height: 40px; border-radius: 50%; }

        /* Merchandise */
        .merch-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 2rem;
        }

        .merch-item {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
        }

        .merch-item:hover {
            transform: translateY(-5px);
        }

        .merch-image {
            height: 200px;
            width: 100%;
            object-fit: cover;
        }

        .merch-info {
            padding: 1.5rem;
        }

        /* Footer */
        footer {
            background-color: var(--secondary);
            color: white;
            padding: 4rem 0 2rem;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 3rem;
        }

        .footer-column h3 {
            color: white;
            margin-bottom: 1.5rem;
            font-size: 1.3rem;
        }

        .footer-column ul {
            list-style: none;
        }

        .footer-column ul li {
            margin-bottom: 0.8rem;
        }

        .footer-column ul li a {
            color: #ccc;
            text-decoration: none;
            transition: var(--transition);
        }

        .footer-column ul li a:hover {
            color: var(--primary);
            padding-left: 5px;
        }

        .copyright {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid #444;
            color: #aaa;
            font-size: 0.9rem;
        }

        /* Responsive Design */
        @media (max-width: 992px) {
            .customizer-container,
            .forum-container {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 768px) {
            .mobile-menu-btn {
                display: block;
            }

            nav {
                position: fixed;
                top: 70px;
                left: 0;
                width: 100%;
                background-color: var(--secondary);
                padding: 1rem;
                transform: translateY(-100%);
                opacity: 0;
                visibility: hidden;
                transition: var(--transition);
                box-shadow: var(--shadow);
            }

            nav.active {
                transform: translateY(0);
                opacity: 1;
                visibility: visible;
            }

            nav ul {
                flex-direction: column;
            }

            nav ul li {
                margin: 0 0 1rem 0;
            }

            .hero h1 {
                font-size: 2.5rem;
            }

            .cta-buttons {
                flex-direction: column;
                align-items: center;
            }

            .search-box input {
                width: 150px;
            }
        }

        /* Tabs for car types */
        .tabs {
            display: flex;
            justify-content: center;
            margin-bottom: 3rem;
            flex-wrap: wrap;
        }

        .tab-btn {
            padding: 10px 20px;
            background-color: white;
            border: none;
            border-radius: 30px;
            margin: 0 5px 10px;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
            box-shadow: var(--shadow);
        }

        .tab-btn.active {
            background-color: var(--primary);
            color: white;
        }

        .tab-content {
            display: none;
        }

        .tab-content.active {
            display: block;
            animation: fadeIn 0.5s;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-container">
            <div class="logo">
                <i class="fas fa-car"></i>
                Elite<span>Motors</span>
            </div>
            
            <button class="mobile-menu-btn" id="mobileMenuBtn">
                <i class="fas fa-bars"></i>
            </button>
            
            <nav id="mainNav">
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#cars">Buy Cars</a></li>
                    <li><a href="#knowledge">Car Knowledge</a></li>
                    <li><a href="#community">Community</a></li>
                    <li><a href="#customizer">Car Customizer</a></li>
                    <li><a href="#merchandise">Merchandise</a></li>
                </ul>
            </nav>
            
            <div class="user-actions">
                <div class="search-box">
                    <input type="text" placeholder="Search cars, parts, info...">
                    <button><i class="fas fa-search"></i></button>
                </div>
                <a href="#"><i class="fas fa-shopping-cart"></i></a>
                <a href="#"><i class="fas fa-user-circle"></i></a>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <h1>Your Ultimate Car Experience Awaits</h1>
            <p>Explore, customize, and purchase your dream car. Connect with a global community of car enthusiasts. Find answers to all your car-related questions from verified experts.</p>
            <div class="cta-buttons">
                <a href="#cars" class="btn">Browse Cars</a>
                <a href="#customizer" class="btn btn-outline">Build Your Dream Car</a>
            </div>
        </div>
    </section>

    <!-- Car Marketplace -->
    <section id="cars" class="cars-section">
        <div class="container">
            <h2 class="section-title">Browse & Buy Cars</h2>
            
            <div class="tabs">
                <button class="tab-btn active" data-tab="all">All Cars</button>
                <button class="tab-btn" data-tab="sports">Sports Cars</button>
                <button class="tab-btn" data-tab="suv">SUVs</button>
                <button class="tab-btn" data-tab="luxury">Luxury</button>
                <button class="tab-btn" data-tab="f1">Formula 1</button>
                <button class="tab-btn" data-tab="electric">Electric</button>
            </div>
            
            <!-- All Cars Tab -->
            <div id="all" class="tab-content active">
                <div class="car-grid">
                    <!-- Koenigsegg -->
                    <div class="car-card">
                        <img src="https://spots.ag/2024/08/15/koenigsegg-jesko-attack-nur-edition-31664-c447215082024133901_1.jpg?" alt="Koenigsegg Jesko" class="car-image">
                        <div class="car-info">
                            <h3>Koenigsegg Jesko</h3>
                            <div class="car-price">$3,000,000</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 1600 HP</span>
                                <span><i class="fas fa-bolt"></i> 2.5s 0-60</span>
                                <span><i class="fas fa-gas-pump"></i> 12 MPG</span>
                            </div>
                            <p>Swedish hypercar with revolutionary aerodynamic design and mind-bending performance.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Inquire to Buy</button>
                        </div>
                    </div>
                    
                    <!-- Lamborghini -->
                    <div class="car-card">
                        <img src="https://i.ytimg.com/vi/T_QALZC-6io/maxresdefault.jpg" alt="Lamborghini Aventador" class="car-image">
                        <div class="car-info">
                            <h3>Lamborghini Aventador SVJ</h3>
                            <div class="car-price">$517,770</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 759 HP</span>
                                <span><i class="fas fa-bolt"></i> 2.8s 0-60</span>
                                <span><i class="fas fa-gas-pump"></i> 10 MPG</span>
                            </div>
                            <p>V12 masterpiece with aggressive styling and track-focused performance.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Buy Now</button>
                        </div>
                    </div>
                    
                    <!-- McLaren -->
                    <div class="car-card">
                        <img src="https://libertywalk.co.jp/wp-content/uploads/2024/07/LB-WORKS-Mclaren-720S-Spider00015.jpg" alt="McLaren 720S" class="car-image">
                        <div class="car-info">
                            <h3>McLaren 720S</h3>
                            <div class="car-price">$299,000</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 710 HP</span>
                                <span><i class="fas fa-bolt"></i> 2.8s 0-60</span>
                                <span><i class="fas fa-gas-pump"></i> 18 MPG</span>
                            </div>
                            <p>British supercar combining breathtaking performance with daily usability.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Buy Now</button>
                        </div>
                    </div>
                    
                    <!-- Porsche -->
                    <div class="car-card">
                        <img src="https://www.europeanprestige.co.uk/blobs/stock/284/images/fde33432-2d3e-4c30-ba21-0d0de188e819/hi4a3191.jpg?width=2000&height=1333" alt="Porsche 911 Turbo S" class="car-image">
                        <div class="car-info">
                            <h3>Porsche 911 Turbo S</h3>
                            <div class="car-price">$205,000</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 640 HP</span>
                                <span><i class="fas fa-bolt"></i> 2.7s 0-60</span>
                                <span><i class="fas fa-gas-pump"></i> 20 MPG</span>
                            </div>
                            <p>The pinnacle of sports car engineering with blistering acceleration and precision handling.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Buy Now</button>
                        </div>
                    </div>
                    
                    <!-- Audi -->
                    <div class="car-card">
                        <img src="https://www.turbo.fr/sites/default/files/styles/header_image/public/2023-11/ABT%20XGT%2001.jpg?itok=RCxxx1YJ" alt="Audi R8" class="car-image">
                        <div class="car-info">
                            <h3>Audi R8 V10 Plus</h3>
                            <div class="car-price">$197,000</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 602 HP</span>
                                <span><i class="fas fa-bolt"></i> 3.2s 0-60</span>
                                <span><i class="fas fa-gas-pump"></i> 17 MPG</span>
                            </div>
                            <p>German engineering excellence with a screaming V10 and quattro all-wheel drive.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Buy Now</button>
                        </div>
                    </div>
                    
                    <!-- BMW -->
                    <div class="car-card">
                        <img src="https://images.hgmsites.net/hug/2018-bmw-m8-gte-race-car_100636412_h.jpg" alt="BMW M8" class="car-image">
                        <div class="car-info">
                            <h3>BMW M8 Competition</h3>
                            <div class="car-price">$146,000</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 617 HP</span>
                                <span><i class="fas fa-bolt"></i> 3.0s 0-60</span>
                                <span><i class="fas fa-gas-pump"></i> 19 MPG</span>
                            </div>
                            <p>Luxury grand tourer with racetrack capabilities and executive comfort.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Buy Now</button>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Sports Cars Tab -->
            <div id="sports" class="tab-content">
                <div class="car-grid">
                    <div class="car-card">
                        <img src="https://www.topgear.com/sites/default/files/news-listicle/image/huracan_performante_green_140.jpg" alt="Lamborghini" class="car-image">
                        <div class="car-info">
                            <h3>Lamborghini Huracán EVO</h3>
                            <div class="car-price">$261,274</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 631 HP</span>
                                <span><i class="fas fa-bolt"></i> 2.9s 0-60</span>
                                <span><i class="fas fa-gas-pump"></i> 15 MPG</span>
                            </div>
                            <p>V10-powered Italian supercar with razor-sharp handling and explosive acceleration.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Buy Now</button>
                        </div>
                    </div>
                    
                    <div class="car-card">
                        <img src="https://mclaren.scene7.com/is/image/mclaren/Pure-McLaren-About-Us-1200x1200?wid=1024&hei=1024" alt="McLaren" class="car-image">
                        <div class="car-info">
                            <h3>McLaren 765LT</h3>
                            <div class="car-price">$358,000</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 755 HP</span>
                                <span><i class="fas fa-bolt"></i> 2.7s 0-60</span>
                                <span><i class="fas fa-gas-pump"></i> 18 MPG</span>
                            </div>
                            <p>Longtail version with enhanced aerodynamics and track-focused performance.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Buy Now</button>
                        </div>
                    </div>
                    
                    <div class="car-card">
                        <img src="data:image/jpeg;base64,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" alt="Audi R8" class="car-image">
                        <div class="car-info">
                            <h3>Audi R8 Performance</h3>
                            <div class="car-price">$197,000</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 602 HP</span>
                                <span><i class="fas fa-bolt"></i> 3.2s 0-60</span>
                                <span><i class="fas fa-gas-pump"></i> 17 MPG</span>
                            </div>
                            <p>Everyday supercar with legendary V10 engine and quattro all-wheel drive.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Buy Now</button>
                        </div>
                    </div>
                    
                    <div class="car-card">
                        <img src="https://media.ed.edmunds-media.com/chevrolet/corvette/2023/ns/2023_chevrolet_corvette_actf34_ns_930222_717.jpg" alt="Chevrolet Corvette" class="car-image">
                        <div class="car-info">
                            <h3>Chevrolet Corvette Z06</h3>
                            <div class="car-price">$106,395</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 670 HP</span>
                                <span><i class="fas fa-bolt"></i> 2.6s 0-60</span>
                                <span><i class="fas fa-gas-pump"></i> 16 MPG</span>
                            </div>
                            <p>American supercar with mid-engine layout and track-proven performance.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Buy Now</button>
                        </div>
                    </div>
                    
                    <div class="car-card">
                        <img src="https://www.mustangspecs.com/wp-content/uploads/2021/07/2021-Ford-Mustang-Shelby-GT500-6.jpg" alt="Ford Mustang" class="car-image">
                        <div class="car-info">
                            <h3>Ford Mustang Shelby GT500</h3>
                            <div class="car-price">$73,995</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 760 HP</span>
                                <span><i class="fas fa-bolt"></i> 3.3s 0-60</span>
                                <span><i class="fas fa-gas-pump"></i> 14 MPG</span>
                            </div>
                            <p>American muscle car icon with supercharged V8 and track capabilities.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Buy Now</button>
                        </div>
                    </div>
                    
                    <div class="car-card">
                        <img src="https://www.shutterstock.com/image-photo/des-moines-ia-july-03-600nw-2242748665.jpg" alt="Dodge" class="car-image">
                        <div class="car-info">
                            <h3>Dodge Challenger SRT Hellcat</h3>
                            <div class="car-price">$71,895</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 717 HP</span>
                                <span><i class="fas fa-bolt"></i> 3.6s 0-60</span>
                                <span><i class="fas fa-gas-pump"></i> 13 MPG</span>
                            </div>
                            <p>Modern muscle car with supercharged Hemi V8 and retro styling.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Buy Now</button>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- SUVs Tab -->
            <div id="suv" class="tab-content">
                <div class="car-grid">
                    <div class="car-card">
                        <img src="https://cms-assets.autoscout24.com/uaddx06iwzdz/7Ljkfe9cpCOZNMyyxIh91O/19503cb6de146c03bd8d2d939dacd412/land-rover-range-rover-front.jpg?w=1100" alt="Range Rover" class="car-image">
                        <div class="car-info">
                            <h3>Range Rover Autobiography</h3>
                            <div class="car-price">$145,000</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 518 HP</span>
                                <span><i class="fas fa-couch"></i> Luxury Interior</span>
                                <span><i class="fas fa-snowflake"></i> All-Terrain</span>
                            </div>
                            <p>Ultimate luxury SUV with unparalleled comfort and off-road capabilities.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Buy Now</button>
                        </div>
                    </div>
                    
                    <div class="car-card">
                        <img src="https://i.ytimg.com/vi/Se6Ht3fK06E/hqdefault.jpg" alt="Mercedes G-Class" class="car-image">
                        <div class="car-info">
                            <h3>Mercedes-Benz G63 AMG 
                                Modified by MANSORY
                            </h3>
                            <div class="car-price">$156,450</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 577 HP</span>
                                <span><i class="fas fa-bolt"></i> 4.5s 0-60</span>
                                <span><i class="fas fa-gas-pump"></i> 15 MPG</span>
                            </div>
                            <p>Iconic off-road vehicle with AMG performance and luxury amenities.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Buy Now</button>
                        </div>
                    </div>
                    
                    <div class="car-card">
                        <img src="https://img.olx.com.br/thumbs700x500/14/148596331662681.webp" alt="Cadillac Escalade" class="car-image">
                        <div class="car-info">
                            <h3>Cadillac Escalade-V</h3>
                            <div class="car-price">$149,990</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 682 HP</span>
                                <span><i class="fas fa-bolt"></i> 4.4s 0-60</span>
                                <span><i class="fas fa-gas-pump"></i> 15 MPG</span>
                            </div>
                            <p>American luxury SUV with supercharged V8 and premium technology.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Buy Now</button>
                        </div>
                    </div>
                    
                    <div class="car-card">
                        <img src="https://i.gaw.to/vehicles/photos/40/31/403101-2023-bmw-x7.jpg?640x400" alt="BMW X7" class="car-image">
                        <div class="car-info">
                            <h3>BMW X7 M60i</h3>
                            <div class="car-price">$104,095</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 523 HP</span>
                                <span><i class="fas fa-bolt"></i> 4.5s 0-60</span>
                                <span><i class="fas fa-gas-pump"></i> 20 MPG</span>
                            </div>
                            <p>Full-size luxury SUV with M performance and three rows of seating.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Buy Now</button>
                        </div>
                    </div>
                    
                    <div class="car-card">
                        <img src="https://images.overdrive.in/wp-content/uploads/2023/08/Audi-Q8-e-tron-and-Audi-Q8-Sportback-e-tron-1-900x506.jpg" alt="Audi Q8" class="car-image">
                        <div class="car-info">
                            <h3>Audi Q8 Sportback e-tron</h3>
                            <div class="car-price">$74,400</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 402 HP</span>
                                <span><i class="fas fa-bolt"></i> 5.6s 0-60</span>
                                <span><i class="fas fa-charging-station"></i> Electric</span>
                            </div>
                            <p>Electric luxury SUV coupe with advanced technology and quattro all-wheel drive.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Buy Now</button>
                        </div>
                    </div>
                    
                    <div class="car-card">
                        <img src="https://torquecafe.b-cdn.net/wp-content/uploads/2023/05/656628.jpg" alt="Volkswagen Touareg" class="car-image">
                        <div class="car-info">
                            <h3>Volkswagen Touareg R-Line</h3>
                            <div class="car-price">$67,345</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 335 HP</span>
                                <span><i class="fas fa-bolt"></i> 5.5s 0-60</span>
                                <span><i class="fas fa-gas-pump"></i> 22 MPG</span>
                            </div>
                            <p>Premium German SUV with sophisticated design and advanced technology.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Buy Now</button>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Luxury Tab -->
            <div id="luxury" class="tab-content">
                <div class="car-grid">
                    <div class="car-card">
                        <img src="https://i.ytimg.com/vi/KW_OOY0PxSc/maxresdefault.jpg" alt="Rolls Royce" class="car-image">
                        <div class="car-info">
                            <h3>Rolls-Royce Phantom 
                                Modified by MANSORY
                            </h3>
                            <div class="car-price">$455,000</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 563 HP</span>
                                <span><i class="fas fa-crown"></i> Ultimate Luxury</span>
                                <span><i class="fas fa-gas-pump"></i> 18 MPG</span>
                            </div>
                            <p>The pinnacle of automotive luxury with whisper-quiet ride and bespoke customization.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Inquire to Buy</button>
                        </div>
                    </div>
                    
                    <div class="car-card">
                        <img src="https://i.ytimg.com/vi/iuRNqlRiQyI/maxresdefault.jpg" alt="Mercedes S-Class" class="car-image">
                        <div class="car-info">
                            <h3>Mercedes-Maybach S680</h3>
                            <div class="car-price">$205,650</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 621 HP</span>
                                <span><i class="fas fa-crown"></i> Chauffeur Package</span>
                                <span><i class="fas fa-gas-pump"></i> 17 MPG</span>
                            </div>
                            <p>Ultra-luxury sedan with rear executive seating and advanced comfort systems.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Buy Now</button>
                        </div>
                    </div>
                    
                    <div class="car-card">
                        <img src="https://vehicle-images.dealerinspire.com/fee5-110004916/WBA33EJ00SCU37804/06d82b9142721008c985394406dd2cf7.jpg" alt="BMW 7 Series" class="car-image">
                        <div class="car-info">
                            <h3>BMW 760i xDrive</h3>
                            <div class="car-price">$113,600</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 536 HP</span>
                                <span><i class="fas fa-crown"></i> Executive Lounge</span>
                                <span><i class="fas fa-gas-pump"></i> 22 MPG</span>
                            </div>
                            <p>Flagship luxury sedan with V8 power and cutting-edge technology.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Buy Now</button>
                        </div>
                    </div>
                    
                    <div class="car-card">
                        <img src="https://www.joemacari.com/blobs/stock/10005064/images/f56eafb0-9c43-445b-b145-a2bd8dc80a14.jpg?width=2000&height=1333" alt="Aston Martin" class="car-image">
                        <div class="car-info">
                            <h3>Aston Martin DB11</h3>
                            <div class="car-price">$205,600</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 630 HP</span>
                                <span><i class="fas fa-crown"></i> Handcrafted Interior</span>
                                <span><i class="fas fa-gas-pump"></i> 20 MPG</span>
                            </div>
                            <p>British grand tourer with exquisite craftsmanship and thrilling performance.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Buy Now</button>
                        </div>
                    </div>
                    
                    <div class="car-card">
                        <img src="https://imgcdn.oto.com/large/gallery/exterior/22/180/lexus-ls-front-angle-low-view-554991.jpg" alt="Lexus" class="car-image">
                        <div class="car-info">
                            <h3>Lexus LS 500h</h3>
                            <div class="car-price">$81,010</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 354 HP</span>
                                <span><i class="fas fa-leaf"></i> Hybrid</span>
                                <span><i class="fas fa-gas-pump"></i> 28 MPG</span>
                            </div>
                            <p>Japanese luxury sedan with hybrid efficiency and impeccable reliability.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Buy Now</button>
                        </div>
                    </div>
                    
                    <div class="car-card">
                        <img src="https://i.gaw.to/vehicles/photos/08/39/083916_2018_cadillac_CT6.jpg?640x400" alt="Cadillac" class="car-image">
                        <div class="car-info">
                            <h3>Cadillac CT6 Platinum</h3>
                            <div class="car-price">$88,790</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 404 HP</span>
                                <span><i class="fas fa-crown"></i> Super Cruise</span>
                                <span><i class="fas fa-gas-pump"></i> 22 MPG</span>
                            </div>
                            <p>American luxury flagship with hands-free driving technology.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Buy Now</button>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Formula 1 Tab -->
            <div id="f1" class="tab-content">
                <div class="car-grid">
                    <div class="car-card">
                        <img src="https://e0.365dm.com/21/02/2048x1152/skysports-lewis-hamilton-mercedes_5258685.jpg?20210202114007" alt="F1 Car" class="car-image">
                        <div class="car-info">
                            <h3>Mercedes-AMG F1 W12</h3>
                            <div class="car-price">$12,500,000</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 1000+ HP</span>
                                <span><i class="fas fa-bolt"></i> 2.5s 0-60</span>
                                <span><i class="fas fa-trophy"></i> Championship</span>
                            </div>
                            <p>Race-winning Formula 1 car with hybrid power unit and cutting-edge aerodynamics.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Inquire to Buy</button>
                        </div>
                    </div>
                    
                    <div class="car-card">
                        <img src="https://cdn-2.motorsport.com/images/amp/YW7JPpkY/s6/red-bull-racing-rb18-1.jpg" alt="F1 Car" class="car-image">
                        <div class="car-info">
                            <h3>Red Bull Racing RB18</h3>
                            <div class="car-price">$15,000,000</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 1050 HP</span>
                                <span><i class="fas fa-bolt"></i> 2.4s 0-60</span>
                                <span><i class="fas fa-trophy"></i> World Champion</span>
                            </div>
                            <p>Championship-winning F1 car with ground-effect aerodynamics and Honda power unit.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Inquire to Buy</button>
                        </div>
                    </div>
                    
                    <div class="car-card">
                        <img src="https://formu1a.uno/wp-content/uploads/2023/05/gmhbsrth3kza1-scaled.jpg" alt="F1 Car" class="car-image">
                        <div class="car-info">
                            <h3>Ferrari SF-23</h3>
                            <div class="car-price">$13,750,000</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 1020 HP</span>
                                <span><i class="fas fa-bolt"></i> 2.6s 0-60</span>
                                <span><i class="fas fa-trophy"></i> Scuderia Ferrari</span>
                            </div>
                            <p>Italian racing masterpiece with screaming V6 turbo hybrid and prancing horse heritage.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Inquire to Buy</button>
                        </div>
                    </div>
                    
                    <div class="car-card">
                        <img src="https://cdn-2.motorsport.com/images/amp/YBeAWnK2/s1000/lando-norris-mclaren-mcl60-1.jpg" alt="F1 Car" class="car-image">
                        <div class="car-info">
                            <h3>McLaren MCL60</h3>
                            <div class="car-price">$11,800,000</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 1010 HP</span>
                                <span><i class="fas fa-bolt"></i> 2.5s 0-60</span>
                                <span><i class="fas fa-trophy"></i> British Racing</span>
                            </div>
                            <p>Papaya orange racing car with Mercedes power unit and carbon fiber monocoque.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Inquire to Buy</button>
                        </div>
                    </div>
                    
                    <div class="car-card">
                        <img src="https://cdn-8.motorsport.com/images/amp/0L1DGQP2/s1000/esteban-ocon-alpine-a523-1.jpg" alt="F1 Car" class="car-image">
                        <div class="car-info">
                            <h3>Alpine A523</h3>
                            <div class="car-price">$10,500,000</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 1000 HP</span>
                                <span><i class="fas fa-bolt"></i> 2.6s 0-60</span>
                                <span><i class="fas fa-trophy"></i> French Engineering</span>
                            </div>
                            <p>Renault-powered F1 car with French blue livery and advanced aerodynamic package.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Inquire to Buy</button>
                        </div>
                    </div>
                    
                    <div class="car-card">
                        <img src="https://www.autohebdo.fr/app/uploads/2024/02/AMR24_16x9_Image_2-753x494.jpg" alt="F1 Car" class="car-image">
                        <div class="car-info">
                            <h3>Aston Martin AMR23</h3>
                            <div class="car-price">$12,200,000</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 1015 HP</span>
                                <span><i class="fas fa-bolt"></i> 2.5s 0-60</span>
                                <span><i class="fas fa-trophy"></i> British Racing Green</span>
                            </div>
                            <p>British racing car with Mercedes power unit and iconic green livery.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Inquire to Buy</button>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Electric Tab -->
            <div id="electric" class="tab-content">
                <div class="car-grid">
                    <div class="car-card">
                        <img src="https://octane.rent/wp-content/uploads/2024/11/tesla_model_s_black_01.jpg"" alt="Tesla" class="car-image">
                        <div class="car-info">
                            <h3>Tesla Model S Plaid</h3>
                            <div class="car-price">$135,990</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 1020 HP</span>
                                <span><i class="fas fa-bolt"></i> 1.99s 0-60</span>
                                <span><i class="fas fa-charging-station"></i> 396 mi</span>
                            </div>
                            <p>Fastest production car in the world with tri-motor setup and futuristic technology.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Buy Now</button>
                        </div>
                    </div>
                    
                    <div class="car-card">
                        <img src="https://image-cdn.hypb.st/https%3A%2F%2Fhypebeast.com%2Fimage%2F2024%2F09%2F20%2Faudi-rs-e-tron-gt-performance-release-info-001.jpg?q=75&w=800&cbr=1&fit=max" alt="Audi e-tron" class="car-image">
                        <div class="car-info">
                            <h3>Audi e-tron GT</h3>
                            <div class="car-price">$105,945</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 590 HP</span>
                                <span><i class="fas fa-bolt"></i> 3.9s 0-60</span>
                                <span><i class="fas fa-charging-station"></i> 238 mi</span>
                            </div>
                            <p>Electric grand tourer with Porsche Taycan platform and quattro all-wheel drive.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Buy Now</button>
                        </div>
                    </div>
                    
                    <div class="car-card">
                        <img src="https://ev-database.org/img/auto/Porsche_Taycan_Turbo_S/Porsche_Taycan_Turbo_S-01@2x.jpg" alt="Porsche Taycan" class="car-image">
                        <div class="car-info">
                            <h3>Porsche Taycan Turbo S</h3>
                            <div class="car-price">$190,900</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 750 HP</span>
                                <span><i class="fas fa-bolt"></i> 2.6s 0-60</span>
                                <span><i class="fas fa-charging-station"></i> 212 mi</span>
                            </div>
                            <p>Electric sports sedan with Porsche performance DNA and 800-volt architecture.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Buy Now</button>
                        </div>
                    </div>
                    
                    <div class="car-card">
                        <img src="https://billeder.bilbasen.dk/bilinfo/a954d1e0-6eb6-4b02-9688-cdd1cbcab233.jpeg?class=S960X960" alt="BMW i7" class="car-image">
                        <div class="car-info">
                            <h3>BMW i7 xDrive60</h3>
                            <div class="car-price">$120,295</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 536 HP</span>
                                <span><i class="fas fa-bolt"></i> 4.5s 0-60</span>
                                <span><i class="fas fa-charging-station"></i> 318 mi</span>
                            </div>
                            <p>Electric luxury flagship with 31-inch theater screen and crystal interior elements.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Buy Now</button>
                        </div>
                    </div>
                    
                    <div class="car-card">
                        <img src="https://www.topgear.com/sites/default/files/2021/10/Cyber_Orange_019.jpg" alt="Ford Mustang Mach-E" class="car-image">
                        <div class="car-info">
                            <h3>Ford Mustang Mach-E GT</h3>
                            <div class="car-price">$70,995</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 480 HP</span>
                                <span><i class="fas fa-bolt"></i> 3.8s 0-60</span>
                                <span><i class="fas fa-charging-station"></i> 270 mi</span>
                            </div>
                            <p>Electric SUV with Mustang styling and performance-oriented driving dynamics.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Buy Now</button>
                        </div>
                    </div>
                    
                    <div class="car-card">
                        <img src="https://www.cnet.com/a/img/resize/d49500c0c0e47a3fb9a96946ac9de8ab8f38aefb/hub/2021/11/01/177d8fc4-fd4d-4b46-8313-6368f678ecf7/id4-promo.jpg?auto=webp&width=768" alt="Volkswagen ID.4" class="car-image">
                        <div class="car-info">
                            <h3>Volkswagen ID.4 Pro</h3>
                            <div class="car-price">$42,495</div>
                            <div class="car-features">
                                <span><i class="fas fa-tachometer-alt"></i> 295 HP</span>
                                <span><i class="fas fa-bolt"></i> 5.7s 0-60</span>
                                <span><i class="fas fa-charging-station"></i> 275 mi</span>
                            </div>
                            <p>Affordable electric SUV with spacious interior and practical everyday usability.</p>
                            <button class="btn" style="width: 100%; margin-top: 15px;">Buy Now</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Car Knowledge Hub -->
    <section id="knowledge" class="knowledge-section" style="background-color: var(--light);">
        <div class="container">
            <h2 class="section-title">Car Knowledge Hub</h2>
            <p style="text-align: center; max-width: 800px; margin: 0 auto 2rem;">Get answers to all your car-related questions from verified experts, official brand representatives, and trusted knowledge sources.</p>
            
            <div class="search-container">
                <div class="search-header">
                    <h3>What would you like to know about cars?</h3>
                    <button class="btn">Ask an Expert</button>
                </div>
                
                <div class="form-group">
                    <input type="text" placeholder="Type your question here (e.g., 'What's the difference between turbocharging and supercharging?')" style="padding: 15px; font-size: 1rem;">
                </div>
                
                <div class="knowledge-results">
                    <h4>Popular Questions & Answers</h4>
                    
                    <div class="knowledge-item">
                        <h5>What maintenance does an electric car need compared to a gasoline car?</h5>
                        <p><strong>Answered by:</strong> Tesla Engineering Team</p>
                        <p>Electric vehicles require less maintenance than gasoline cars because they have fewer moving parts. No oil changes, spark plugs, fuel filters, or exhaust systems. However, they still need tire rotations, brake fluid checks, and battery cooling system maintenance.</p>
                        <div style="margin-top: 10px; color: var(--accent); font-size: 0.9rem;">
                            <i class="fas fa-check-circle"></i> Verified Answer • From Official Source
                        </div>
                    </div>
                    
                    <div class="knowledge-item">
                        <h5>How often should I replace my car's timing belt?</h5>
                        <p><strong>Answered by:</strong> Mike Johnson, Master Mechanic</p>
                        <p>Most manufacturers recommend replacing the timing belt every 60,000 to 100,000 miles. However, check your owner's manual for the specific interval for your vehicle. Failure to replace a worn timing belt can cause serious engine damage.</p>
                        <div style="margin-top: 10px; color: var(--accent); font-size: 0.9rem;">
                            <i class="fas fa-check-circle"></i> Verified Answer • From Certified Expert
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Community Forum -->
    <section id="community" class="community-section">
        <div class="container">
            <h2 class="section-title">Car Community Forum</h2>
            <p style="text-align: center; max-width: 800px; margin: 0 auto 3rem;">Share your car problems, get solutions from experts and fellow enthusiasts, and join discussions about everything automotive.</p>
            
            <div class="forum-container">
                <div>
                    <div class="post-form">
                        <h3>Post Your Car Problem</h3>
                        <form id="problemForm">
                            <div class="form-group">
                                <label for="problemTitle">Problem Title</label>
                                <input type="text" id="problemTitle" placeholder="E.g., 'My car makes a knocking sound when accelerating'">
                            </div>
                            <div class="form-group">
                                <label for="problemDescription">Description</label>
                                <textarea id="problemDescription" rows="4" placeholder="Describe the problem in detail..."></textarea>
                            </div>
                            <div class="form-group">
                                <label for="carModel">Car Model & Year</label>
                                <input type="text" id="carModel" placeholder="E.g., Honda Civic 2018">
                            </div>
                            <button type="submit" class="btn">Submit Problem</button>
                        </form>
                    </div>
                    
                    <div class="community-posts">
                        <h3>Recent Community Problems</h3>
                        
                        <div class="post">
                            <div class="post-header">
                                <div class="post-user">
                                    <div class="user-avatar">JS</div>
                                    <div>
                                        <strong>John Smith</strong>
                                        <div style="font-size: 0.9rem; color: var(--dark-gray);">Toyota Camry 2015</div>
                                    </div>
                                </div>
                                <div style="font-size: 0.9rem; color: var(--dark-gray);">2 hours ago</div>
                            </div>
                            <h4>Brake pedal feels spongy and car pulls to the right when braking</h4>
                            <p>I noticed this issue last week. The brake pedal goes almost to the floor before the car starts slowing down. Also, when I brake at higher speeds, the car pulls to the right side. I checked the brake fluid level and it's fine. What could be the issue?</p>
                            
                            <div class="post-comments" style="margin-top: 15px; padding-top: 15px; border-top: 1px dashed var(--gray);">
                                <div style="display: flex; margin-bottom: 10px;">
                                    <div class="user-avatar" style="width: 30px; height: 30px; font-size: 0.8rem;">MT</div>
                                    <div style="margin-left: 10px;">
                                        <div><strong>Mike Taylor <span class="expert-badge">Expert Mechanic</span></strong></div>
                                        <p>Sounds like you have air in the brake lines (causing spongy pedal) and a stuck caliper or contaminated brake pad on the left side (causing pull to the right). You should bleed the brakes and inspect the calipers.</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                        
                        <div class="post">
                            <div class="post-header">
                                <div class="post-user">
                                    <div class="user-avatar">SR</div>
                                    <div>
                                        <strong>Sarah Rodriguez</strong>
                                        <div style="font-size: 0.9rem; color: var(--dark-gray);">Ford Mustang 2020</div>
                                    </div>
                                </div>
                                <div style="font-size: 0.9rem; color: var(--dark-gray);">1 day ago</div>
                            </div>
                            <h4>Engine overheating only when AC is turned on</h4>
                            <p>My Mustang runs at normal temperature until I turn on the AC. After about 10 minutes with AC on, the temperature gauge starts climbing. If I turn off the AC, it slowly returns to normal. Coolant level is good. Any ideas?</p>
                            
                            <div class="post-comments" style="margin-top: 15px; padding-top: 15px; border-top: 1px dashed var(--gray);">
                                <div style="display: flex; margin-bottom: 10px;">
                                    <div class="user-avatar" style="width: 30px; height: 30px; font-size: 0.8rem;">RC</div>
                                    <div style="margin-left: 10px;">
                                        <div><strong>Robert Chen <span class="expert-badge">Ford Technician</span></strong></div>
                                        <p>This is likely a failing radiator fan or fan clutch. When AC is on, the AC condenser adds more heat to the radiator, requiring more cooling. If the fan isn't working properly, the engine will overheat. Check if the fan engages when AC is turned on.</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div>
                    <div class="community-posts">
                        <h3>Top Experts This Month</h3>
                        <div style="margin-top: 20px;">
                            <div style="display: flex; align-items: center; margin-bottom: 20px; padding-bottom: 15px; border-bottom: 1px solid var(--gray);">
                                <div class="user-avatar" style="background-color: var(--accent);">MT</div>
                                <div style="margin-left: 10px;">
                                    <div><strong>Mike Taylor</strong></div>
                                    <div style="font-size: 0.9rem; color: var(--dark-gray);">Master Mechanic • 342 solutions</div>
                                </div>
                            </div>
                            
                            <div style="display: flex; align-items: center; margin-bottom: 20px; padding-bottom: 15px; border-bottom: 1px solid var(--gray);">
                                <div class="user-avatar" style="background-color: var(--primary);">AE</div>
                                <div style="margin-left: 10px;">
                                    <div><strong>Amanda Evans</strong></div>
                                    <div style="font-size: 0.9rem; color: var(--dark-gray);">Porsche Engineer • 287 solutions</div>
                                </div>
                            </div>
                            
                            <div style="display: flex; align-items: center; margin-bottom: 20px;">
                                <div class="user-avatar" style="background-color: green;">RC</div>
                                <div style="margin-left: 10px;">
                                    <div><strong>Robert Chen</strong></div>
                                    <div style="font-size: 0.9rem; color: var(--dark-gray);">Ford Technician • 256 solutions</div>
                                </div>
                            </div>
                        </div>
                        
                        <h3 style="margin-top: 30px;">Car Parts Marketplace</h3>
                        <p>Browse and buy genuine parts and accessories for your vehicle.</p>
                        <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 10px; margin-top: 15px;">
                            <div style="background-color: var(--light); padding: 10px; border-radius: 5px; text-align: center;">
                                <i class="fas fa-cog" style="font-size: 1.5rem; color: var(--primary); margin-bottom: 5px;"></i>
                                <div>Engine Parts</div>
                            </div>
                            <div style="background-color: var(--light); padding: 10px; border-radius: 5px; text-align: center;">
                                <i class="fas fa-tire" style="font-size: 1.5rem; color: var(--primary); margin-bottom: 5px;"></i>
                                <div>Tires & Wheels</div>
                            </div>
                            <div style="background-color: var(--light); padding: 10px; border-radius: 5px; text-align: center;">
                                <i class="fas fa-tools" style="font-size: 1.5rem; color: var(--primary); margin-bottom: 5px;"></i>
                                <div>Tools & Equipment</div>
                            </div>
                            <div style="background-color: var(--light); padding: 10px; border-radius: 5px; text-align: center;">
                                <i class="fas fa-car-side" style="font-size: 1.5rem; color: var(--primary); margin-bottom: 5px;"></i>
                                <div>Body Parts</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Car Customizer -->
    <section id="customizer" class="customizer-section" style="background-color: var(--secondary); color: white;">
        <div class="container">
            <h2 class="section-title" style="color: white;">Build Your Dream Car</h2>
            <p style="text-align: center; max-width: 800px; margin: 0 auto 3rem; color: #ccc;">Use our advanced car configurator to design your perfect vehicle. Get expert guidance on compatibility, safety, and performance optimization.</p>
            
            <div class="customizer-container">
                <div class="customizer-controls">
                    <h3 style="color: var(--secondary);">Customization Options</h3>
                    
                    <div class="form-group">
                        <label>Base Model</label>
                        <select>
                            <option>Porsche 911 Carrera</option>
                            <option>Tesla Model S</option>
                            <option>Ford Mustang GT</option>
                            <option>BMW M3</option>
                            <option>Mercedes-AMG GT</option>
                        </select>
                    </div>
                    
                    <div class="form-group">
                        <label>Engine</label>
                        <select>
                            <option>3.0L Twin-Turbo V6 (400 HP)</option>
                            <option>4.0L Twin-Turbo V8 (550 HP)</option>
                            <option>5.2L V10 (620 HP) - Performance</option>
                            <option>Electric Dual Motor (750 HP)</option>
                        </select>
                    </div>
                    
                    <div class="form-group">
                        <label>Exterior Color</label>
                        <div style="display: flex; gap: 10px;">
                            <div style="width: 30px; height: 30px; background-color: #1a1a1a; border-radius: 50%; cursor: pointer; border: 2px solid white;"></div>
                            <div style="width: 30px; height: 30px; background-color: #d40000; border-radius: 50%; cursor: pointer;"></div>
                            <div style="width: 30px; height: 30px; background-color: #0077cc; border-radius: 50%; cursor: pointer;"></div>
                            <div style="width: 30px; height: 30px; background-color: #f5f5f5; border-radius: 50%; cursor: pointer;"></div>
                            <div style="width: 30px; height: 30px; background-color: #2e8b57; border-radius: 50%; cursor: pointer;"></div>
                        </div>
                    </div>
                    
                    <div class="form-group">
                        <label>Wheels & Tires</label>
                        <select>
                            <option>19" Alloy Wheels with All-Season Tires</option>
                            <option>20" Forged Wheels with Performance Tires</option>
                            <option>21" Carbon Fiber Wheels with Track Tires</option>
                        </select>
                    </div>
                    
                    <div class="form-group">
                        <label>Interior Package</label>
                        <select>
                            <option>Premium Leather (Black)</option>
                            <option>Carbon Fiber & Alcantara (Sport)</option>
                            <option>Full Nappa Leather (Luxury)</option>
                            <option>Racing Bucket Seats (Track)</option>
                        </select>
                    </div>
                    
                    <div class="form-group">
                        <label>Performance Upgrades</label>
                        <div>
                            <label style="display: flex; align-items: center; margin-bottom: 8px;">
                                <input type="checkbox" style="margin-right: 10px;">
                                Sport Exhaust System
                            </label>
                            <label style="display: flex; align-items: center; margin-bottom: 8px;">
                                <input type="checkbox" style="margin-right: 10px;">
                                Adjustable Coilover Suspension
                            </label>
                            <label style="display: flex; align-items: center; margin-bottom: 8px;">
                                <input type="checkbox" style="margin-right: 10px;">
                                Carbon Ceramic Brakes
                            </label>
                            <label style="display: flex; align-items: center;">
                                <input type="checkbox" style="margin-right: 10px;">
                                Rear Wing Spoiler
                            </div>
                        </div>
                    </div>
                    
                    <button class="btn" style="width: 100%;">Get Expert Review</button>
                    <button class="btn btn-outline" style="width: 100%; margin-top: 10px; color: var(--secondary); border-color: var(--secondary);">Request Quote from Modifiers</button>
                </div>
                
                <div class="customizer-preview">
                    <h3>Your Custom Car</h3>
                    <div class="car-visualization">
                        <div>3D Car Visualization</div>
                        <div class="car-part engine">Engine</div>
                        <div class="car-part spoiler">Spoiler</div>
                        <div class="car-part wheel-front">Wheel</div>
                        <div class="car-part wheel-back">Wheel</div>
                    </div>
                    
                    <div style="text-align: center; width: 100%;">
                        <h4>Expert Compatibility Check</h4>
                        <div style="background-color: rgba(255, 255, 255, 0.1); padding: 15px; border-radius: 8px; margin-top: 10px;">
                            <div style="display: flex; align-items: center; margin-bottom: 10px;">
                                <i class="fas fa-check-circle" style="color: #4CAF50; margin-right: 10px;"></i>
                                <div>Engine upgrade compatible with selected chassis</div>
                            </div>
                            <div style="display: flex; align-items: center; margin-bottom: 10px;">
                                <i class="fas fa-exclamation-triangle" style="color: #FFC107; margin-right: 10px;"></i>
                                <div>Wider tires may require fender modification</div>
                            </div>
                            <div style="display: flex; align-items: center;">
                                <i class="fas fa-check-circle" style="color: #4CAF50; margin-right: 10px;"></i>
                                <div>Spoiler provides adequate downforce at high speeds</div>
                            </div>
                        </div>
                        
                        <div style="margin-top: 20px; font-size: 1.2rem;">
                            <strong>Estimated Cost: </strong> <span style="color: var(--primary);">$142,500</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Merchandise -->
    <section id="merchandise" class="merchandise-section">
        <div class="container">
            <h2 class="section-title">Car Enthusiast Merchandise</h2>
            <p style="text-align: center; max-width: 800px; margin: 0 auto 3rem;">Show your love for cars with our premium merchandise. Customize or choose from our exclusive collection.</p>
            
            <div class="merch-grid">
                <!-- Hot Wheels -->
                <div class="merch-item">
                    <img src="https://i.ytimg.com/vi/0Ohi6aBoPQ4/hq720.jpg?sqp=-oaymwEhCK4FEIIDSFryq4qpAxMIARUAAAAAGAElAADIQj0AgKJD&rs=AOn4CLDKqFy_opPYShrOyT_KETpM0NQ9tA" alt="Hot Wheels Collection" class="merch-image">
                    <div class="merch-info">
                        <h3>Hot Wheels Collector's Edition</h3>
                        <p>Limited edition die-cast models including rare collectibles from Koenigsegg, Lamborghini, and McLaren.</p>
                        <div class="car-price">From $14.99</div>
                        <button class="btn" style="width: 100%; margin-top: 10px;">Browse Collection</button>
                    </div>
                </div>
                
                <!-- T-Shirts -->
                <div class="merch-item">
                    <img src="https://thefanboy.in/cdn/shop/files/Porsche_Printed_T-Shirt.jpg?v=1739538819&width=1445" alt="Car T-shirt" class="merch-image">
                    <div class="merch-info">
                        <h3>Premium Car Brand T-Shirts</h3>
                        <p>100% cotton t-shirts featuring iconic car brand logos and classic car designs.</p>
                        <div class="car-price">From $24.99</div>
                        <button class="btn" style="width: 100%; margin-top: 10px;">Customize & Buy</button>
                    </div>
                </div>
                
                <!-- Caps -->
                <div class="merch-item">
                    <img src="https://cdn.shopify.com/s/files/1/0936/0618/3205/files/a-photograph-of-a-sleek-navy-blue-formul_4NbcN1zhSQyMNAAtk8nUQw_U_3Q6RlLQROZqWuHrZ9zZA.jpg?v=1756210061" alt="Car Caps" class="merch-image">
                    <div class="merch-info">
                        <h3>Official Racing Team Caps</h3>
                        <p>Authentic Formula 1 and motorsport team caps with adjustable straps and premium embroidery.</p>
                        <div class="car-price">From $29.99</div>
                        <button class="btn" style="width: 100%; margin-top: 10px;">Shop Now</button>
                    </div>
                </div>
                
                <!-- Posters -->
                <div class="merch-item">
                    <img src="https://i.etsystatic.com/25734305/r/il/b648ce/7090663418/il_300x300.7090663418_1jqu.jpg" alt="Car Art Wall Posters" class="merch-image">
                    <div class="merch-info">
                        <h3>Car Art Wall Posters</h3>
                        <p>High-quality posters featuring iconic cars, racing moments, and automotive art prints.</p>
                        <div class="car-price">From $19.99</div>
                        <button class="btn" style="width: 100%; margin-top: 10px;">Shop Now</button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>EliteMotors</h3>
                    <p>Your ultimate destination for everything automotive. From buying your dream car to connecting with a global community of enthusiasts.</p>
                    <div style="display: flex; gap: 15px; margin-top: 20px;">
                        <a href="#" style="color: white; font-size: 1.2rem;"><i class="fab fa-facebook"></i></a>
                        <a href="#" style="color: white; font-size: 1.2rem;"><i class="fab fa-twitter"></i></a>
                        <a href="#" style="color: white; font-size: 1.2rem;"><i class="fab fa-instagram"></i></a>
                        <a href="#" style="color: white; font-size: 1.2rem;"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>
                
                <div class="footer-column">
                    <h3>Quick Links</h3>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#cars">Buy Cars</a></li>
                        <li><a href="#knowledge">Car Knowledge</a></li>
                        <li><a href="#community">Community</a></li>
                        <li><a href="#customizer">Car Customizer</a></li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h3>Services</h3>
                    <ul>
                        <li><a href="#">Car Financing</a></li>
                        <li><a href="#">Insurance</a></li>
                        <li><a href="#">Car Inspection</a></li>
                        <li><a href="#">Shipping & Delivery</a></li>
                        <li><a href="#">Trade-In</a></li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h3>Contact Us</h3>
                    <ul>
                        <li><i class="fas fa-map-marker-alt"></i> 123 Automotive Drive, Detroit, MI</li>
                        <li><i class="fas fa-phone"></i> (555) 123-4567</li>
                        <li><i class="fas fa-envelope"></i> info@elitemotors.com</li>
                        <li><i class="fas fa-clock"></i> Mon-Fri: 9AM-6PM EST</li>
                    </ul>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2025 EliteMotors. All rights reserved. | <a href="#" style="color: #aaa;">Privacy Policy</a> | <a href="#" style="color: #aaa;">Terms of Service</a></p>
            </div>
        </div>
    </footer>

    <script>
        // Mobile menu toggle
        const mobileMenuBtn = document.getElementById('mobileMenuBtn');
        const mainNav = document.getElementById('mainNav');
        
        mobileMenuBtn.addEventListener('click', () => {
            mainNav.classList.toggle('active');
            mobileMenuBtn.innerHTML = mainNav.classList.contains('active') 
                ? '<i class="fas fa-times"></i>' 
                : '<i class="fas fa-bars"></i>';
        });
        
        // Tab switching functionality
        const tabBtns = document.querySelectorAll('.tab-btn');
        const tabContents = document.querySelectorAll('.tab-content');
        
        tabBtns.forEach(btn => {
            btn.addEventListener('click', () => {
                // Remove active class from all buttons and contents
                tabBtns.forEach(b => b.classList.remove('active'));
                tabContents.forEach(c => c.classList.remove('active'));
                
                // Add active class to clicked button
                btn.classList.add('active');
                
                // Show corresponding content
                const tabId = btn.getAttribute('data-tab');
                document.getElementById(tabId).classList.add('active');
            });
        });
        
        // Form submission for problem posting
        const problemForm = document.getElementById('problemForm');
        
        problemForm.addEventListener('submit', (e) => {
            e.preventDefault();
            
            const title = document.getElementById('problemTitle').value;
            const description = document.getElementById('problemDescription').value;
            const carModel = document.getElementById('carModel').value;
            
            if(title && description && carModel) {
                alert('Your problem has been posted to the community! Experts and fellow enthusiasts will provide solutions soon.');
                problemForm.reset();
            } else {
                alert('Please fill in all fields before submitting.');
            }
        });
        
        // Car part interaction in customizer
        const carParts = document.querySelectorAll('.car-part');
        
        carParts.forEach(part => {
            part.addEventListener('click', () => {
                const partType = part.classList[1];
                const partNames = {
                    'engine': 'Engine',
                    'spoiler': 'Spoiler',
                    'wheel-front': 'Front Wheel',
                    'wheel-back': 'Rear Wheel'
                };
                
                alert(`Customize the ${partNames[partType]} of your car. In the full version, this would open a detailed customization panel.`);
            });
        });
        
        // Smooth scrolling for navigation links
        document.querySelectorAll('nav a').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                
                window.scrollTo({
                    top: targetElement.offsetTop - 80,
                    behavior: 'smooth'
                });
                
                // Close mobile menu if open
                if(mainNav.classList.contains('active')) {
                    mainNav.classList.remove('active');
                    mobileMenuBtn.innerHTML = '<i class="fas fa-bars"></i>';
                }
            });
        });
        
        // Search functionality simulation
        const searchInput = document.querySelector('.search-box input');
        const searchButton = document.querySelector('.search-box button');
        
        searchButton.addEventListener('click', () => {
            if(searchInput.value.trim()) {
                alert(`Searching for: "${searchInput.value}". In the full version, this would show relevant cars, parts, and knowledge articles.`);
            }
        });
        
        searchInput.addEventListener('keypress', (e) => {
            if(e.key === 'Enter') {
                searchButton.click();
            }
        });
    </script>
</body>
</html>
