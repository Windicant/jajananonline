
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="theme-color" content="#ff4757">
    <meta name="apple-mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
    <title>Jajanan Online - Seblak, Mie Jebew & Camilan Enak</title>
    <style>
        :root {
            --primary: #ff4757;
            --secondary: #ff6b81;
            --dark: #2f3542;
            --light: #f1f2f6;
            --success: #2ed573;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }
        
        body {
            background-color: #f8f9fa;
            color: #333;
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        header {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 2rem 0;
            text-align: center;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
            width: 100%;
        }
        
        nav {
            background-color: white;
            padding: 1rem 0;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        nav ul {
            display: flex;
            justify-content: center;
            list-style: none;
            flex-wrap: wrap;
        }
        
        nav ul li {
            margin: 0 15px;
        }
        
        nav ul li a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 500;
            transition: color 0.3s;
            font-size: 1rem;
            padding: 5px 0;
            display: inline-block;
        }
        
        nav ul li a:hover {
            color: var(--primary);
        }
        
        .hero {
            background: url('images/logo.jpeg') no-repeat center center/cover;
            height: 60vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            position: relative;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.5);
        }
        
        .hero-content {
            position: relative;
            z-index: 1;
            max-width: 800px;
            padding: 0 20px;
            width: 100%;
        }
        
        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
            line-height: 1.2;
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--primary);
            color: white;
            padding: 12px 30px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
            text-align: center;
            min-width: 120px;
            min-height: 44px;
        }
        
        .btn:hover {
            background-color: var(--secondary);
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
        
        .btn:active {
            transform: scale(0.98);
        }
        
        .btn-outline {
            background-color: transparent;
            border: 2px solid white;
            margin-left: 15px;
        }
        
        .btn-outline:hover {
            background-color: white;
            color: var(--primary);
        }
        
        section {
            padding: 5rem 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            color: var(--dark);
            position: relative;
            display: inline-block;
            padding-bottom: 10px;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background-color: var(--primary);
        }
        
        .menu-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .menu-item {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }
        
        .menu-item:hover {
            transform: translateY(-10px);
        }
        
        .menu-img {
            height: 200px;
            overflow: hidden;
        }
        
        .menu-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        
        .menu-item:hover .menu-img img {
            transform: scale(1.1);
        }
        
        .menu-content {
            padding: 20px;
        }
        
        .menu-content h3 {
            font-size: 1.5rem;
            margin-bottom: 10px;
            color: var(--dark);
        }
        
        .menu-content p {
            color: #666;
            margin-bottom: 15px;
            font-size: 0.95rem;
        }
        
        .price {
            font-size: 1.3rem;
            font-weight: 700;
            color: var(--primary);
        }
        
        .promo-banner {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 3rem;
            text-align: center;
            border-radius: 10px;
            margin-bottom: 5rem;
        }
        
        .promo-banner h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }
        
        .promo-banner p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
        }
        
        .testimonials {
            background-color: var(--light);
        }
        
        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .testimonial {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }
        
        .testimonial-content {
            margin-bottom: 20px;
            font-style: italic;
            color: #555;
        }
        
        .testimonial-author {
            display: flex;
            align-items: center;
        }
        
        .testimonial-author img {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            object-fit: cover;
            margin-right: 15px;
        }
        
        .author-info h4 {
            color: var(--dark);
            margin-bottom: 5px;
        }
        
        .author-info p {
            color: #777;
            font-size: 0.9rem;
        }
        
        .contact {
            background-color: white;
        }
        
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 50px;
        }
        
        .contact-info h3 {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: var(--dark);
        }
        
        .contact-info p {
            margin-bottom: 15px;
            color: #555;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .social-links {
            display: flex;
            margin-top: 20px;
            flex-wrap: wrap;
            gap: 10px;
        }
        
        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background-color: var(--primary);
            color: white;
            border-radius: 50%;
            text-decoration: none;
            transition: background-color 0.3s;
            font-size: 1.2rem;
        }
        
        .social-links a:hover {
            background-color: var(--secondary);
        }
        
        .contact-form input,
        .contact-form textarea {
            width: 100%;
            padding: 15px;
            margin-bottom: 20px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
            -webkit-appearance: none;
        }
        
        .contact-form textarea {
            height: 150px;
            resize: vertical;
        }
        
        footer {
            background-color: var(--dark);
            color: white;
            padding: 3rem 0;
            text-align: center;
        }
        
        .footer-content {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .footer-content p {
            margin-bottom: 20px;
        }
        
        .footer-links {
            display: flex;
            justify-content: center;
            list-style: none;
            margin-bottom: 20px;
            flex-wrap: wrap;
        }
        
        .footer-links li {
            margin: 0 15px;
        }
        
        .footer-links a {
            color: white;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-links a:hover {
            color: var(--primary);
        }
        
        .copyright {
            color: #aaa;
            font-size: 0.9rem;
        }

        /* Mobile Styles */
        @media (max-width: 768px) {
            header {
                padding: 1.5rem 0;
            }
            
            nav ul {
                flex-direction: column;
                align-items: center;
                padding: 10px 0;
            }
            
            nav ul li {
                margin: 8px 0;
            }
            
            .hero {
                height: 50vh;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
            
            .hero p {
                font-size: 1rem;
                margin-bottom: 1.5rem;
            }
            
            .btn-container {
                display: flex;
                flex-direction: column;
                gap: 10px;
            }
            
            .btn {
                padding: 12px 24px;
                margin: 0;
                width: 100%;
            }
            
            .btn-outline {
                margin-left: 0;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
            
            .menu-grid {
                grid-template-columns: 1fr;
                gap: 20px;
            }
            
            .promo-banner {
                padding: 2rem 1rem;
            }
            
            .promo-banner h2 {
                font-size: 1.8rem;
            }
            
            .testimonial-grid {
                grid-template-columns: 1fr;
            }
            
            .contact-grid {
                grid-template-columns: 1fr;
                gap: 30px;
            }
            
            .contact-form input, 
            .contact-form textarea {
                padding: 12px;
                font-size: 16px;
            }
            
            .footer-links {
                flex-direction: column;
            }
            
            .footer-links li {
                margin: 8px 0;
            }
            
            section {
                padding: 3rem 0;
            }
        }

        @media (max-width: 480px) {
            .hero h1 {
                font-size: 1.8rem;
            }
            
            .section-title h2 {
                font-size: 1.5rem;
            }
            
            .menu-content h3 {
                font-size: 1.3rem;
            }
            
            .price {
                font-size: 1.1rem;
            }
            
            .social-links a {
                width: 36px;
                height: 36px;
                font-size: 1rem;
            }

            .contact-info p {
                font-size: 0.9rem;
            }

            .testimonial {
                padding: 20px;
            }
        }
    </style>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css">
</head>
<body>
    <header>
        <div class="container">
            <h1>Jajanan Online</h1>
            <p>Seblak Pedas, Mie Jebew, & Camilan Enak Lainnya</p>
        </div>
    </header>
    
    <nav>
        <div class="container">
            <ul>
                <li><a href="#home">Beranda</a></li>
                <li><a href="#menu">Menu</a></li>
                <li><a href="#testimonials">Testimoni</a></li>
                <li><a href="#contact">Kontak</a></li>
            </ul>
        </div>
    </nav>
    
    <section class="hero" id="home">
        <div class="hero-content">
            <h1>Jajanan Online Enak & Pedasnya Nagih!</h1>
            <p>Temukan berbagai macam jajanan pedas dan minuman segar yang bikin ketagihan. Pesan sekarang dan nikmati di rumah!</p>
            <div class="btn-container">
                <a href="#menu" class="btn">Lihat Menu</a>
                <a href="#contact" class="btn btn-outline">Pesan Sekarang</a>
            </div>
        </div>
    </section>
    <section id="menu">
        <div class="container">
            <div class="section-title">
                <h2>Menu Andalan Kami</h2>
            </div>
            
            <div class="promo-banner">
                <h2>Seblak Parasmanan</h2>
                <p>Bebas pilih toping sesuka hati <strong></strong>Rasanya gak bakal bikin kecewa ;)</p>
                <a href="#contact" class="btn">Pesan Sekarang</a>
            </div>
            
            <h3 style="text-align: center; margin-bottom: 2rem; font-size: 1.8rem; color: var(--dark);">Makanan Pedas</h3>
            <div class="menu-grid">
                <div class="menu-item">
                    <div class="menu-img">
                        <img src="images/seblak1.jpeg" alt="seblak1" loading="lazy">
                    </div>
                    <div class="menu-content">
                        <h3>Seblak Kuah/Nyemek Parasmanan</h3>
                        <p>Kerupuk basah dengan bumbu khas, bisa pilih level pedas 0-5</p>
                        <p class="price">mulai dari Rp10.000</p>
                    </div>
                </div>
                
                <div class="menu-item">
                    <div class="menu-img">
                        <img src="images/jebew.jpeg" alt="jebew" loading="lazy">
                    </div>
                    <div class="menu-content">
                        <h3>Mie Jebew</h3>
                        <p>Mie kenyal dengan bumbu pedas level 0-5, bikin nagih!</p>
                        <p class="price">Rp10.000</p>
                    </div>
                </div>
                
                <div class="menu-item">
                    <div class="menu-img">
                        <img src="images/aci.jpeg" alt="aci" loading="lazy">
                    </div>
                    <div class="menu-content">
                        <h3>Baso Aci</h3>
                        <p>Baso kenyal dengan kuah gurih, bisa ditambah level pedas</p>
                        <p class="price">Rp10.000</p>
                    </div>
                </div>
                
                <div class="menu-item">
                    <div class="menu-img">
                        <img src="images/miset.jpeg" alt="miset" loading="lazy">
                    </div>
                    <div class="menu-content">
                        <h3>Miset</h3>
                        <p>Misetnya gurih, pedas, maknyos</p>
                        <p class="price">Rp10.000</p>
                    </div>
                </div>
            </div>
            
            <h3 style="text-align: center; margin: 3rem 0 2rem; font-size: 1.8rem; color: var(--dark);">Camilan & Minuman</h3>
            <div class="menu-grid">
                <div class="menu-item">
                    <div class="menu-img">
                        <img src="images/crispy.jpeg" alt="crispy" loading="lazy">
                    </div>
                    <div class="menu-content">
                        <h3>Banana Crispy</h3>
                        <p>Pisang goreng tepung krispi, manis & lembut dalam</p>
                        <p class="price">Rp10.000</p>
                    </div>
                </div>
                
                <div class="menu-item">
                    <div class="menu-img">
                        <img src="images/roll.jpg" alt="roll" loading="lazy">
                    </div>
                    <div class="menu-content">
                        <h3>Banana Roll</h3>
                        <p>Pisang dibalut kulit lumpia, digoreng sampai golden brown</p>
                        <p class="price">Rp10.000</p>
                    </div>
                </div>
                
                <div class="menu-item">
                    <div class="menu-img">
                        <img src="images/cireng.jpeg" alt="cireng" loading="lazy">
                    </div>
                    <div class="menu-content">
                        <h3>Cireng Rasa Ayam atau usus</h3>
                        <p>Cireng isi ayam enak banget buat ngemil</p>
                        <p class="price">Rp1.000/pcs</p>
                    </div>
                </div>
                
                <div class="menu-item">
                    <div class="menu-img">
                        <img src="images/peras.jpeg" alt="peras" loading="lazy">
                    </div>
                    <div class="menu-content">
                        <h3>Es Jeruk Peras</h3>
                        <p>Segar alami, bikin melek! Cocok teman makanan pedas</p>
                        <p class="price">Rp5.000</p>
                    </div>
                </div>
                
                <div class="menu-item">
                    <div class="menu-img">
                        <img src="images/kuwut.jpg" alt="kuwut" loading="lazy">
                    </div>
                    <div class="menu-content">
                        <h3>Es Kuwut</h3>
                        <p>Kelapa muda + sirup, pelepas dahaga terbaik</p>
                        <p class="price">Rp.7000</p>
                    </div>
                </div>
                
                <div class="menu-item">
                    <div class="menu-img">
                        <img src="images/campur.jpg" alt="campur" loading="lazy">
                    </div>
                    <div class="menu-content">
                        <h3>Es Campur & Sop Buah</h3>
                        <p>Mix buah segar dengan sirup & susu, manisnya pas</p>
                        <p class="price">Rp7.000 - Rp10.000</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <section class="testimonials" id="testimonials">
        <div class="container">
            <div class="section-title">
                <h2>Apa Kata Pelanggan Kami?</h2>
            </div>
            
            <div class="testimonial-grid">
                <div class="testimonial">
                    <div class="testimonial-content">
                        <p>"Seblak level 3 nya pas banget pedasnya! Nagih banget, udah pesen berkali-kali. Baso Acinya juga enak, kuahnya gurih."</p>
                    </div>
                    <div class="testimonial-author">
                        <img src="images/desti.jpeg" alt="desti" loading="lazy">
                        <div class="author-info">
                            <h4>Desti R</h4>
                            <p>Pelanggan Setia</p>
                        </div>
                    </div>
                </div>
                
                <div class="testimonial">
                    <div class="testimonial-content">
                        <p>"Mie Jebew level 5 beneran nendang! Cocok buat pecinta pedas ekstrim. Banana Rollnya juga enak, manisnya pas."</p>
                    </div>
                    <div class="testimonial-author">
                        <img src="images/shofil.jpeg" alt="shofil" loading="lazy">
                        <div class="author-info">
                            <h4>Shofil F</h4>
                            <p>Pecinta Pedas</p>
                        </div>
                    </div>
                </div>
                
                <div class="testimonial">
                    <div class="testimonial-content">
                        <p>"Pesen Es Kuwut sama Basreng Bojot buat teman ngerjain tugas, enak banget! Pengirimannya juga cepat. Recommended!"</p>
                    </div>
                    <div class="testimonial-author">
                        <img src="images/meli.jpeg" alt="meli" loading="lazy">
                        <div class="author-info">
                            <h4>Meli A</h4>
                            <p>Mahasiswa</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <section class="contact" id="contact">
        <div class="container">
            <div class="section-title">
                <h2>Pesan Sekarang</h2>
            </div>
            
            <div class="contact-grid">
                <div class="contact-info">
                    <h3>Hubungi Kami</h3>
                    <p><i class="fas fa-map-marker-alt"></i> Jl.Bantarpayung,Cibalong, Tasikmalaya</p>
                    <p><i class="fas fa-phone"></i> +62 838-4884-7331</p>
                    <p><i class="fas fa-envelope"></i> jajananonline@gmail.com</p>
                    <p><i class="fas fa-clock"></i> Buka setiap hari 11.00 - 21.00 WIB</p>
                    
                    <div class="social-links">
                        <a href="https://wa.me/6283848847331"><i class="fab fa-whatsapp"></i></a>
                       <a href="https://instagram.com/wndpstsr_20" target="_blank"><i class="fab fa-instagram"></i></a>
                        <a href="https://facebook.com/puspitasariwnd" target="_blank"><i class="fab fa-facebook-f"></i></a>
                    </div>
                </div>
                
                <div class="contact-form">
                    <form id="orderForm">
                        <input type="text" name="nama" placeholder="Nama Anda" required inputmode="text">
                        <input type="tel" name="whatsapp" placeholder="Nomor WhatsApp" required inputmode="tel">
                        <textarea name="pesanan" placeholder="Pesanan Anda (Contoh: 1 Seblak Level 3, 2 Mie Jebew Level 2, 1 Es Jeruk Peras)" required></textarea>
                        <textarea name="alamat" placeholder="Alamat Pengiriman (Jika delivery)" required></textarea>
                        <textarea name="catatan" placeholder="Catatan Tambahan (Level pedas, dll)"></textarea>
                        <button type="submit" class="btn">Kirim Pesanan via WhatsApp</button>
                    </form>
                </div>
            </div>
        </div>
    </section>
    
    <footer>
        <div class="container">
            <div class="footer-content">
                <h3>Jajanan Online</h3>
                <p>Seblak Pedas, Mie Jebew, & Camilan Enak Lainnya</p>
                
                <ul class="footer-links">
                    <li><a href="#home">Beranda</a></li>
                    <li><a href="#menu">Menu</a></li>
                    <li><a href="#testimonials">Testimoni</a></li>
                    <li><a href="#contact">Kontak</a></li>
                </ul>
                
                <p class="copyright">© 2025 Jajanan Online</p>
            </div>
        </div>
    </footer>
    
    <script>
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
        
        // WhatsApp order form handling
        document.getElementById('orderForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Get form values
            const nama = this.nama.value;
            const whatsapp = this.whatsapp.value;
            const pesanan = this.pesanan.value;
            const alamat = this.alamat.value;
            const catatan = this.catatan.value;
            
          // Format WhatsApp message
const message = `Halo Jajanan Online, saya ingin memesan:\n\nNama: ${nama}\nNo. WhatsApp: ${whatsapp}\n\nPesanan:\n${pesanan}\n\nAlamat: ${alamat}\n\nCatatan: ${catatan || 'Tidak ada catatan'}\n\nTerima kasih!`;

// Encode message for URL
const encodedMessage = encodeURIComponent(message);

// WhatsApp number (pastikan format benar)
const whatsappNumber = '6283848847331'; // Ganti dengan nomor Anda

// Create WhatsApp link (pastikan tidak ada "+" atau "0" di depan)
const whatsappUrl = `https://wa.me/${whatsappNumber}?text=${encodedMessage}`;

// Open WhatsApp in new tab
window.open(whatsappUrl, '_blank');
            
            // Reset form
            this.reset();
        });

        // Mobile adjustments
        function adjustForMobile() {
            if (window.innerWidth <= 768) {
                document.querySelectorAll('.menu-item').forEach(item => {
                    item.style.marginBottom = '20px';
                });
            }
        }

        window.addEventListener('load', adjustForMobile);
        window.addEventListener('resize', adjustForMobile);
    </script>
</body>
</html>
