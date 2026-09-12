<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>SuvaiBox | Food Delivery Platform</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, Helvetica, sans-serif;
            background: #faf7ff;
            color: #241832;
            line-height: 1.6;
        }

        /* Navigation */

        nav {
            position: sticky;
            top: 0;
            z-index: 100;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid #eadff7;
            padding: 18px 7%;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 25px;
            font-weight: bold;
            color: #7c3aed;
        }

        nav a {
            text-decoration: none;
            color: #5b4b69;
            margin-left: 25px;
            font-weight: 600;
        }

        nav a:hover {
            color: #7c3aed;
        }

        /* Hero */

        .hero {
            min-height: 90vh;
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 80px 20px;
            background:
                radial-gradient(circle at top left, #eadcff, transparent 35%),
                radial-gradient(circle at bottom right, #e5d5ff, transparent 35%),
                #faf7ff;
        }

        .hero-content {
            max-width: 900px;
        }

        .hero-icon {
            width: 90px;
            height: 90px;
            margin: auto;
            border-radius: 25px;
            background: linear-gradient(135deg, #8b5cf6, #6d28d9);
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 45px;
            box-shadow: 0 20px 40px rgba(124, 58, 237, 0.25);
        }

        .hero h1 {
            margin-top: 30px;
            font-size: 65px;
            color: #5b21b6;
        }

        .hero h2 {
            font-size: 25px;
            color: #6b5b78;
            margin: 10px 0 25px;
            font-weight: 500;
        }

        .hero p {
            max-width: 700px;
            margin: auto;
            color: #75677f;
            font-size: 18px;
        }

        .buttons {
            margin-top: 35px;
        }

        .button {
            display: inline-block;
            padding: 13px 25px;
            margin: 5px;
            border-radius: 12px;
            text-decoration: none;
            font-weight: bold;
            transition: 0.3s;
        }

        .primary {
            background: #7c3aed;
            color: white;
        }

        .primary:hover {
            background: #5b21b6;
            transform: translateY(-2px);
        }

        .secondary {
            border: 2px solid #7c3aed;
            color: #7c3aed;
        }

        .secondary:hover {
            background: #7c3aed;
            color: white;
        }

        /* Sections */

        section {
            padding: 80px 7%;
        }

        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }

        .section-title h2 {
            font-size: 38px;
            color: #5b21b6;
        }

        .section-title p {
            color: #776984;
            margin-top: 8px;
        }

        /* Cards */

        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(270px, 1fr));
            gap: 25px;
        }

        .card {
            background: white;
            padding: 30px;
            border-radius: 20px;
            border: 1px solid #eadff7;
            box-shadow: 0 10px 30px rgba(91, 33, 182, 0.07);
            transition: 0.3s;
        }

        .card:hover {
            transform: translateY(-6px);
            box-shadow: 0 18px 40px rgba(91, 33, 182, 0.14);
        }

        .card-icon {
            font-size: 35px;
            margin-bottom: 15px;
        }

        .card h3 {
            color: #5b21b6;
            margin-bottom: 12px;
        }

        .card ul {
            list-style: none;
        }

        .card li {
            padding: 5px 0;
            color: #66586f;
        }

        /* Payment */

        .payment {
            background: #5b21b6;
            color: white;
            border-radius: 30px;
            padding: 60px;
            text-align: center;
        }

        .payment h2 {
            font-size: 38px;
            margin-bottom: 15px;
        }

        .payment p {
            max-width: 700px;
            margin: auto;
            color: #eee5ff;
        }

        .payment-box {
            margin: 30px auto 0;
            max-width: 650px;
            background: rgba(255,255,255,0.1);
            padding: 25px;
            border-radius: 15px;
            font-family: monospace;
            font-size: 16px;
        }

        /* Technology */

        .tech {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 15px;
        }

        .tech span {
            background: white;
            border: 1px solid #dfd1f2;
            padding: 12px 20px;
            border-radius: 30px;
            color: #5b21b6;
            font-weight: bold;
        }

        /* Developers */

        .developer {
            text-align: center;
        }

        .developer-avatar {
            width: 80px;
            height: 80px;
            margin: auto;
            border-radius: 50%;
            background: linear-gradient(135deg, #8b5cf6, #6d28d9);
            color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 25px;
            font-weight: bold;
        }

        .developer h3 {
            margin-top: 18px;
            color: #5b21b6;
            font-size: 23px;
        }

        .role {
            color: #7c3aed;
            font-weight: bold;
            margin: 5px 0 12px;
        }

        .developer p {
            color: #6d6175;
        }

        .linkedin {
            display: inline-block;
            margin-top: 15px;
            color: #7c3aed;
            text-decoration: none;
            font-weight: bold;
        }

        /* Vision */

        .vision {
            text-align: center;
            background: linear-gradient(135deg, #ede5ff, #faf7ff);
        }

        .vision h2 {
            font-size: 40px;
            color: #5b21b6;
        }

        .vision p {
            max-width: 750px;
            margin: 20px auto;
            color: #675875;
            font-size: 18px;
        }

        /* Footer */

        footer {
            background: #241832;
            color: white;
            text-align: center;
            padding: 35px 20px;
        }

        footer strong {
            color: #b794f6;
        }

        /* Responsive */

        @media (max-width: 700px) {

            nav {
                padding: 15px 5%;
            }

            nav div:last-child {
                display: none;
            }

            .hero h1 {
                font-size: 45px;
            }

            .hero h2 {
                font-size: 20px;
            }

            section {
                padding: 60px 5%;
            }

            .payment {
                padding: 40px 20px;
            }
        }
    </style>
</head>

<body>

    <!-- Navigation -->

    <nav>
        <div class="logo">🍽️ SuvaiBox</div>

        <div>
            <a href="#features">Features</a>
            <a href="#technology">Technology</a>
            <a href="#team">Team</a>
        </div>
    </nav>


    <!-- Hero -->

    <header class="hero">

        <div class="hero-content">

            <div class="hero-icon">
                🍽️
            </div>

            <h1>SuvaiBox</h1>

            <h2>Discover. Order. Enjoy.</h2>

            <p>
                A modern food delivery platform connecting customers
                with restaurants through a simple, convenient and
                enjoyable digital experience.
            </p>

            <div class="buttons">

                <a href="#features" class="button primary">
                    Explore Features
                </a>

                <a href="#team" class="button secondary">
                    Meet the Team
                </a>

            </div>

        </div>

    </header>


    <!-- Features -->

    <section id="features">

        <div class="section-title">

            <h2>✨ Features</h2>

            <p>
                Everything needed for a complete food delivery experience.
            </p>

        </div>


        <div class="grid">

            <div class="card">

                <div class="card-icon">👤</div>

                <h3>Customer</h3>

                <ul>
                    <li>🔐 Registration & Login</li>
                    <li>📍 Location-based discovery</li>
                    <li>🔎 Food & restaurant search</li>
                    <li>❤️ Favourites</li>
                    <li>🛒 Shopping cart</li>
                    <li>💳 Online payments</li>
                    <li>📦 Order tracking</li>
                    <li>⭐ Reviews & ratings</li>
                    <li>🔄 Reorder</li>
                    <li>🔔 Notifications</li>
                </ul>

            </div>


            <div class="card">

                <div class="card-icon">🏪</div>

                <h3>Seller</h3>

                <ul>
                    <li>🔐 Seller login</li>
                    <li>🏬 Multiple restaurant management</li>
                    <li>🍔 Food & menu management</li>
                    <li>📂 Custom categories</li>
                    <li>🖼️ Food images</li>
                    <li>➕ Add-ons & variants</li>
                    <li>🎟️ Offers & coupons</li>
                    <li>📋 Order management</li>
                    <li>💬 Review replies</li>
                    <li>📊 Business analytics</li>
                </ul>

            </div>


            <div class="card">

                <div class="card-icon">🛡️</div>

                <h3>Admin</h3>

                <ul>
                    <li>👨‍💼 Seller verification</li>
                    <li>🏪 Restaurant management</li>
                    <li>🚫 Account restrictions</li>
                    <li>🚨 Report management</li>
                    <li>⭐ Review moderation</li>
                    <li>📜 FSSAI management</li>
                    <li>❓ Help Center management</li>
                    <li>📊 Platform monitoring</li>
                </ul>

            </div>


            <div class="card">

                <div class="card-icon">🚚</div>

                <h3>Delivery</h3>

                <ul>
                    <li>👤 Delivery partner support</li>
                    <li>📦 Order status updates</li>
                    <li>📍 Delivery tracking</li>
                    <li>🗺️ Real-time location support</li>
                </ul>

            </div>

        </div>

    </section>


    <!-- Payment -->

    <section>

        <div class="payment">

            <h2>💳 Secure Payments</h2>

            <p>
                SuvaiBox is designed to support secure online payments
                using Razorpay with backend payment verification.
            </p>

            <div class="payment-box">

                Customer → Checkout → Razorpay
                → Payment Verification → Order Confirmation

            </div>

        </div>

    </section>


    <!-- Technology -->

    <section id="technology">

        <div class="section-title">

            <h2>🛠️ Technology</h2>

            <p>Technologies planned for building SuvaiBox.</p>

        </div>


        <div class="tech">

            <span>React</span>
            <span>Vite</span>
            <span>JavaScript</span>
            <span>Tailwind CSS</span>
            <span>Node.js</span>
            <span>Express.js</span>
            <span>MongoDB</span>
            <span>Mongoose</span>
            <span>JWT</span>
            <span>REST APIs</span>
            <span>Razorpay</span>
            <span>Cloud Image Storage</span>

        </div>

    </section>


    <!-- User Experience -->

    <section>

        <div class="section-title">

            <h2>🎨 User Experience</h2>

            <p>
                Designed to be simple, modern and enjoyable.
            </p>

        </div>


        <div class="grid">

            <div class="card">
                <div class="card-icon">💜</div>
                <h3>Modern Design</h3>
                <p>
                    A clean and modern purple-themed interface.
                </p>
            </div>

            <div class="card">
                <div class="card-icon">🌙</div>
                <h3>Dark Mode</h3>
                <p>
                    Comfortable light and dark viewing modes.
                </p>
            </div>

            <div class="card">
                <div class="card-icon">📱</div>
                <h3>Responsive</h3>
                <p>
                    Designed to work across desktop and mobile screens.
                </p>
            </div>

            <div class="card">
                <div class="card-icon">⚡</div>
                <h3>Simple Experience</h3>
                <p>
                    Easy navigation and convenient food ordering.
                </p>
            </div>

        </div>

    </section>


    <!-- Security -->

    <section>

        <div class="section-title">

            <h2>🔐 Security</h2>

            <p>
                Security and data protection are important parts of SuvaiBox.
            </p>

        </div>


        <div class="grid">

            <div class="card">
                <h3>👤 Account Protection</h3>
                <p>
                    Customer and seller accounts are protected using
                    secure authentication.
                </p>
            </div>

            <div class="card">
                <h3>💳 Payment Security</h3>
                <p>
                    Payment processing and verification are handled securely.
                </p>
            </div>

            <div class="card">
                <h3>🛡️ Role-Based Access</h3>
                <p>
                    Customers, sellers, delivery partners and admins
                    have appropriate access levels.
                </p>
            </div>

        </div>

    </section>


    <!-- Development Team -->

    <section id="team">

        <div class="section-title">

            <h2>👩‍💻 Development Team</h2>

            <p>
                Built with passion by our development team.
            </p>

        </div>


        <div class="grid">

            <div class="card developer">

                <div class="developer-avatar">
                    DM
                </div>

                <h3>Dhanya M</h3>

                <div class="role">
                    Backend Developer
                </div>

                <p>
                    Responsible for backend functionality, APIs,
                    database management, authentication, payments,
                    security and server-side features.
                </p>

                <a
                    class="linkedin"
                    href="https://www.linkedin.com/in/mnidhanya/"
                    target="_blank"
                >
                    🔗 LinkedIn
                </a>

            </div>


            <div class="card developer">

                <div class="developer-avatar">
                    PB
                </div>

                <h3>Pragathi B</h3>

                <div class="role">
                    Frontend Developer
                </div>

                <p>
                    Responsible for the user interface, user experience,
                    responsive design and frontend functionality.
                </p>

                <a
                    class="linkedin"
                    href="https://www.linkedin.com/in/pragathi-bala-596767366/"
                    target="_blank"
                >
                    🔗 LinkedIn
                </a>

            </div>

        </div>

    </section>


    <!-- Vision -->

    <section class="vision">

        <h2>🚀 Our Vision</h2>

        <p>
            To create a smooth and reliable digital food ordering
            experience for customers while helping restaurants
            manage their online food business.
        </p>

        <h3>
            🍽️ Discover. Order. Enjoy.
        </h3>

    </section>


    <!-- Footer -->

    <footer>

        <p>
            Made with ❤️ by
            <strong>Dhanya M</strong>
            &
            <strong>Pragathi B</strong>
        </p>

        <p>
            © 2026 SuvaiBox. All rights reserved.
        </p>

    </footer>

</body>
</html>