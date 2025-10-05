<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Voyage Elite | Premium Travel Experiences</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Base Styles */
        :root {
            --primary: #667eea;
            --secondary: #764ba2;
            --accent: #f093fb;
            --gold: #FFD700;
            --dark: #1a202c;
            --light: #f7fafc;
            --text: #2d3748;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            margin: 0;
            padding: 0;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
            color: var(--text);
            line-height: 1.7;
        }
        
        .email-wrapper {
            max-width: 700px;
            margin: 30px auto;
            background: white;
            border-radius: 24px;
            overflow: hidden;
            box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.25);
        }

        /* Header with Animated Gradient Border */
        .header {
            padding: 30px 40px;
            text-align: center;
            background: white;
            position: relative;
        }
        
        .header:before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 6px;
            background: linear-gradient(90deg, var(--primary), var(--accent), var(--secondary), var(--gold), var(--primary));
            background-size: 400% 400%;
            animation: gradientShift 4s ease infinite;
        }
        
        @keyframes gradientShift {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
        
        .logo {
            font-size: 42px;
            font-weight: 800;
            background: linear-gradient(135deg, var(--primary), var(--secondary), var(--gold));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin: 0;
            letter-spacing: -1px;
        }
        
        .tagline {
            color: var(--text);
            font-size: 16px;
            margin: 12px 0 0 0;
            letter-spacing: 4px;
            text-transform: uppercase;
            font-weight: 500;
        }

        /* Premium Hero Section */
        .hero {
            position: relative;
            height: 480px;
            background: linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.5)), 
                        url('https://images.unsplash.com/photo-1682687221363-72518513620e?ixlib=rb-4.0.3&auto=format&fit=crop&w=2070&q=80');
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            padding: 0 40px;
        }
        
        .hero-content h1 {
            font-size: 56px;
            font-weight: 800;
            margin: 0 0 20px 0;
            line-height: 1.1;
            text-shadow: 0 4px 12px rgba(0,0,0,0.4);
            letter-spacing: -1px;
        }
        
        .hero-content p {
            font-size: 22px;
            margin: 0 0 35px 0;
            opacity: 0.9;
            font-weight: 300;
            max-width: 600px;
        }
        
        .cta-button {
            display: inline-block;
            padding: 18px 45px;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            text-decoration: none;
            font-weight: 700;
            border-radius: 50px;
            transition: all 0.4s ease;
            box-shadow: 0 12px 25px rgba(102, 126, 234, 0.4);
            font-size: 18px;
            position: relative;
            overflow: hidden;
            z-index: 1;
        }
        
        .cta-button:before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 0%;
            height: 100%;
            background: linear-gradient(135deg, var(--gold), var(--accent));
            transition: all 0.4s ease;
            z-index: -1;
        }
        
        .cta-button:hover:before {
            width: 100%;
        }
        
        .cta-button:hover {
            transform: translateY(-5px);
            box-shadow: 0 18px 30px rgba(102, 126, 234, 0.5);
        }

        /* Premium Features Grid */
        .features {
            padding: 80px 40px;
            background: var(--light);
        }
        
        .section-title {
            text-align: center;
            font-size: 38px;
            font-weight: 800;
            margin-bottom: 60px;
            color: var(--dark);
            position: relative;
        }
        
        .section-title:after {
            content: '';
            position: absolute;
            bottom: -20px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 5px;
            background: linear-gradient(90deg, var(--primary), var(--accent));
            border-radius: 3px;
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 40px;
        }
        
        .feature-card {
            background: white;
            padding: 40px 30px;
            border-radius: 20px;
            text-align: center;
            box-shadow: 0 10px 25px rgba(0,0,0,0.05);
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
            z-index: 1;
        }
        
        .feature-card:before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(90deg, var(--primary), var(--accent), var(--gold));
            z-index: 2;
        }
        
        .feature-card:hover {
            transform: translateY(-15px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
        }
        
        .feature-icon {
            width: 90px;
            height: 90px;
            margin: 0 auto 25px;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 36px;
            box-shadow: 0 10px 20px rgba(102, 126, 234, 0.3);
        }
        
        .feature-card h3 {
            margin: 0 0 20px 0;
            font-size: 24px;
            font-weight: 700;
            color: var(--dark);
        }
        
        .feature-card p {
            margin: 0;
            color: var(--text);
            font-size: 16px;
            line-height: 1.6;
        }

        /* Luxury Destinations Showcase */
        .destinations {
            padding: 80px 40px;
            background: white;
        }
        
        .destination-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 35px;
        }
        
        .destination-card {
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 15px 30px rgba(0,0,0,0.1);
            transition: all 0.4s ease;
            position: relative;
        }
        
        .destination-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 25px 50px rgba(0,0,0,0.15);
        }
        
        .destination-image {
            height: 250px;
            background-size: cover;
            background-position: center;
            transition: transform 0.7s ease;
            position: relative;
        }
        
        .destination-card:hover .destination-image {
            transform: scale(1.1);
        }
        
        .destination-overlay {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: linear-gradient(transparent, rgba(0,0,0,0.8));
            padding: 30px 25px 25px;
            color: white;
            transform: translateY(10px);
            transition: all 0.4s ease;
        }
        
        .destination-card:hover .destination-overlay {
            transform: translateY(0);
        }
        
        .destination-name {
            font-weight: 700;
            margin: 0 0 10px 0;
            font-size: 22px;
        }
        
        .destination-meta {
            display: flex;
            justify-content: space-between;
            align-items: center;
            opacity: 0;
            transition: opacity 0.4s ease;
        }
        
        .destination-card:hover .destination-meta {
            opacity: 1;
        }
        
        .destination-price {
            color: var(--gold);
            font-weight: 700;
            font-size: 20px;
        }
        
        .destination-rating {
            color: var(--gold);
            font-weight: 600;
        }

        /* Exclusive Offers Section */
        .offers {
            padding: 80px 40px;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            text-align: center;
        }
        
        .offers .section-title {
            color: white;
        }
        
        .offers .section-title:after {
            background: rgba(255,255,255,0.7);
        }
        
        .offer-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }
        
        .offer-card {
            background: rgba(255,255,255,0.1);
            backdrop-filter: blur(10px);
            padding: 40px 30px;
            border-radius: 20px;
            border: 1px solid rgba(255,255,255,0.2);
            transition: all 0.4s ease;
        }
        
        .offer-card:hover {
            transform: translateY(-10px);
            background: rgba(255,255,255,0.15);
        }
        
        .offer-badge {
            display: inline-block;
            padding: 8px 20px;
            background: var(--gold);
            color: var(--dark);
            font-weight: 700;
            border-radius: 30px;
            margin-bottom: 20px;
            font-size: 14px;
        }
        
        .offer-card h3 {
            font-size: 24px;
            margin-bottom: 15px;
        }
        
        .offer-card p {
            margin-bottom: 25px;
            opacity: 0.9;
        }

        /* Premium Newsletter */
        .newsletter {
            padding: 80px 40px;
            text-align: center;
            background: var(--light);
            position: relative;
            overflow: hidden;
        }
        
        .newsletter:before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(90deg, var(--primary), var(--accent), var(--gold));
        }
        
        .newsletter-form {
            max-width: 500px;
            margin: 40px auto 0;
            display: flex;
            gap: 15px;
        }
        
        .newsletter-input {
            flex: 1;
            padding: 18px 25px;
            border: none;
            border-radius: 50px;
            font-size: 16px;
            box-shadow: 0 10px 20px rgba(0,0,0,0.05);
            outline: none;
            transition: all 0.3s ease;
        }
        
        .newsletter-input:focus {
            box-shadow: 0 10px 20px rgba(102, 126, 234, 0.2);
        }
        
        .newsletter-button {
            padding: 18px 35px;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            border: none;
            border-radius: 50px;
            font-weight: 700;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 10px 20px rgba(102, 126, 234, 0.3);
        }
        
        .newsletter-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 25px rgba(102, 126, 234, 0.4);
        }

         /* Luxury Footer */
        .footer {
            background: var(--dark);
            color: white;
            padding: 70px 40px 40px;
        }
        
        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            margin-bottom: 50px;
        }
        
        .footer-column {
            text-align: center;
        }
        
        .footer-column h3 {
            margin: 0 0 25px 0;
            font-size: 20px;
            font-weight: 700;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-column h3:after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 40px;
            height: 3px;
            background: var(--gold);
        }
        
        .footer-links {
            list-style: none;
            padding: 0;
            margin: 0;
        }
        
        .footer-links li {
            margin-bottom: 12px;
        }
        
        .footer-links a {
            color: #cbd5e0;
            text-decoration: none;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .footer-links a:hover {
            color: white;
            transform: translateX(5px);
        }
        
        .footer-links a i {
            margin-right: 10px;
            color: var(--gold);
            width: 20px;
            text-align: center;
        }
        
        .social-links {
            display: flex;
            gap: 15px;
            justify-content: center;
            margin-top: 25px;
        }
        
        .social-links a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 45px;
            height: 45px;
            background: rgba(255,255,255,0.1);
            border-radius: 50%;
            color: white;
            text-decoration: none;
            transition: all 0.3s ease;
            font-size: 18px;
        }
        
        .social-links a:hover {
            background: var(--primary);
            transform: translateY(-5px);
        }
        
        .footer-bottom {
            text-align: center;
            padding-top: 40px;
            border-top: 1px solid #4a5568;
            color: #a0aec0;
            font-size: 14px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }
        
        .payment-methods {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 20px;
            font-size: 24px;
        }

        /* Responsive Design */
        @media (max-width: 700px) {
            .email-wrapper {
                margin: 10px;
                border-radius: 16px;
            }
            
            .header, .features, .destinations, .offers, .newsletter, .footer {
                padding-left: 25px;
                padding-right: 25px;
            }
            
            .hero {
                height: 400px;
                padding: 0 25px;
            }
            
            .hero-content h1 {
                font-size: 40px;
            }
            
            .hero-content p {
                font-size: 18px;
            }
            
            .section-title {
                font-size: 32px;
            }
            
            .newsletter-form {
                flex-direction: column;
            }
            
            .footer-grid {
                grid-template-columns: 1fr;
                gap: 30px;
            }
            
            .features-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="email-wrapper">
        <!-- Premium Header -->
        <div class="header">
            <h1 class="logo">VOYAGE ELITE</h1>
            <p class="tagline">Luxury Travel Redefined</p>
        </div>

        <!-- Stunning Hero Section -->
        <div class="hero">
            <div class="hero-content">
                <h1>Discover Extraordinary Destinations</h1>
                <p>Experience the world's most exclusive locations with our bespoke travel services</p>
                <a href="#" class="cta-button">Explore Premium Packages <i class="fas fa-arrow-right" style="margin-left: 10px;"></i></a>
            </div>
        </div>

        <!-- Premium Features - Now with 4 Cards -->
        <div class="features">
            <h2 class="section-title">Why Choose Voyage Elite?</h2>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-crown"></i>
                    </div>
                    <h3>Luxury Experiences</h3>
                    <p>Handpicked destinations and unique activities tailored to your preferences with exclusive access.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-hotel"></i>
                    </div>
                    <h3>5-Star Accommodations</h3>
                    <p>Stay at the world's most luxurious resorts and boutique hotels with premium amenities.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-user-tie"></i>
                    </div>
                    <h3>Personal Concierge</h3>
                    <p>24/7 dedicated travel experts to ensure your journey is seamless from start to finish.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-shield-alt"></i>
                    </div>
                    <h3>VIP Security</h3>
                    <p>Comprehensive safety measures and privacy protection for worry-free luxury travel.</p>
                </div>
            </div>
        </div>

        <!-- Luxury Destinations with Fixed First Image -->
        <div class="destinations">
            <h2 class="section-title">Featured Destinations</h2>
            <div class="destination-grid">
                <div class="destination-card">
                    <div class="destination-image" style="background-image: url('https://images.unsplash.com/photo-1514282401047-d79a71a590e8?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2065&q=80')"></div>
                    <div class="destination-overlay">
                        <h3 class="destination-name">Maldives Overwater Villas</h3>
                        <div class="destination-meta">
                            <span class="destination-price">From $4,299</span>
                            <span class="destination-rating">★★★★★</span>
                        </div>
                    </div>
                </div>
                <div class="destination-card">
                    <div class="destination-image" style="background-image: url('https://images.unsplash.com/photo-1520250497591-112f2f40a3f4?ixlib=rb-4.0.3&auto=format&fit=crop&w=2070&q=80')"></div>
                    <div class="destination-overlay">
                        <h3 class="destination-name">Japanese Cultural Journey</h3>
                        <div class="destination-meta">
                            <span class="destination-price">From $3,799</span>
                            <span class="destination-rating">★★★★☆</span>
                        </div>
                    </div>
                </div>
                <div class="destination-card">
                    <div class="destination-image" style="background-image: url('https://images.unsplash.com/photo-1506973035872-a4ec16b8e8d9?ixlib=rb-4.0.3&auto=format&fit=crop&w=2070&q=80')"></div>
                    <div class="destination-overlay">
                        <h3 class="destination-name">Swiss Alpine Retreat</h3>
                        <div class="destination-meta">
                            <span class="destination-price">From $4,899</span>
                            <span class="destination-rating">★★★★★</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Exclusive Offers -->
        <div class="offers">
            <h2 class="section-title">Exclusive Limited Offers</h2>
            <div class="offer-cards">
                <div class="offer-card">
                    <span class="offer-badge">LIMITED TIME</span>
                    <h3>Luxury Honeymoon Package</h3>
                    <p>Celebrate your special moment with our exclusive honeymoon package including private villa and couple's spa treatments.</p>
                    <a href="#" class="cta-button" style="font-size: 16px; padding: 12px 25px;">Book Now</a>
                </div>
                <div class="offer-card">
                    <span class="offer-badge">SAVE 25%</span>
                    <h3>Family Adventure Deal</h3>
                    <p>Create unforgettable memories with our family package including kid-friendly activities and accommodations.</p>
                    <a href="#" class="cta-button" style="font-size: 16px; padding: 12px 25px;">Book Now</a>
                </div>
            </div>
        </div>

        <!-- Premium Newsletter -->
        <div class="newsletter">
            <h2 class="section-title">Join Our Elite Travel Club</h2>
            <p>Be the first to receive exclusive travel offers, early access to new destinations, and VIP treatment.</p>
            <form class="newsletter-form">
                <input type="email" class="newsletter-input" placeholder="Your email address">
                <button type="submit" class="newsletter-button">Subscribe <i class="fas fa-paper-plane" style="margin-left: 8px;"></i></button>
            </form>
        </div>

       <!-- Luxury Footer (Updated Version) -->
        <div class="footer">
            <div class="footer-grid">
                <div class="footer-column">
                    <h3>Voyage Elite</h3>
					 <p style="color: #cbd5e0; margin-bottom: 25px; line-height: 1.6;">
                        Creating extraordinary travel experiences for discerning clients since 2015.
                    </p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-pinterest-p"></i></a>
                    </div>
                </div>
                <div class="footer-column">
                    <h3>Destinations</h3>
                    <ul class="footer-links">
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Europe</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Asia</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Africa</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Americas</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Oceania</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Services</h3>
                    <ul class="footer-links">
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Luxury Tours</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Private Jets</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Yacht Charters</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Event Planning</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Concierge Services</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Contact</h3>
                    <ul class="footer-links">
                        <li><a href="#"><i class="fas fa-phone"></i> +1 (888) 123-4567</a></li>
                        <li><a href="#"><i class="fas fa-envelope"></i> info@voyageelite.com</a></li>
                        <li><a href="#"><i class="fas fa-map-marker-alt"></i> 123 Luxury Lane, Travel City</a></li>
                        <li><a href="#"><i class="fas fa-clock"></i> Mon-Fri: 9AM-8PM EST</a></li>
                    </ul>
                </div>
            </div>

            <div class="footer-bottom">
                <div class="payment-methods">
                    <i class="fab fa-cc-visa"></i>
                    <i class="fab fa-cc-mastercard"></i>
                    <i class="fab fa-cc-amex"></i>
                    <i class="fab fa-cc-paypal"></i>
                    <i class="fab fa-cc-apple-pay"></i>
                </div>
                <p style="margin-top: 20px; text-align: center;">&copy; 2025 Voyage Elite Travel. All rights reserved.</p>
                <p style="text-align: center; margin-top: 10px;">
                    <a href="#" style="color: #a0aec0; text-decoration: underline; margin: 0 10px;">Privacy Policy</a> | 
                    <a href="#" style="color: #a0aec0; text-decoration: underline; margin: 0 10px;">Terms of Service</a> | 
                    <a href="#" style="color: #a0aec0; text-decoration: underline; margin: 0 10px;">Unsubscribe</a>
                </p>
            </div>
        </div>
    </div>
</body>
</html>
