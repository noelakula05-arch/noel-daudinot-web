[index.html.html](https://github.com/user-attachments/files/28687034/index.html.html)
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Ing. Noel Daudinot G - Especialista en Tecnología Médica (TAC, RM, RX) y Automatización Industrial (PLC, FPGA) en San Cristóbal, Táchira, Venezuela.">
    <meta name="keywords" content="ingeniero telecomunicaciones, tecnología médica, TAC, resonancia magnética, PLC, FPGA, variadores de frecuencia, mantenimiento industrial, San Cristóbal, Táchira, Venezuela">
    <meta name="author" content="Ing. Noel Daudinot G">
    <title>Ing. Noel Daudinot G | Tecnología Médica e Industrial - San Cristóbal</title>
    <style>
        /* =========================================
           VARIABLES & RESET (Mobile-First)
           ========================================= */
        :root {
            --primary-dark: #0A2540;
            --primary-blue: #0066FF;
            --primary-light: #E6F0FF;
            --accent-blue: #0052CC;
            --medical-teal: #00B4D8;
            --industrial-orange: #FF6B35;
            --whatsapp-green: #25D366;
            --text-main: #1A1A1A;
            --text-muted: #5C6B7F;
            --bg-light: #F8FAFC;
            --white: #FFFFFF;
            --error: #DC2626;
            --success: #16A34A;
            --shadow-sm: 0 2px 8px rgba(10, 37, 64, 0.08);
            --shadow-md: 0 8px 24px rgba(10, 37, 64, 0.12);
            --radius: 12px;
            --transition: all 0.3s ease;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        
        html { scroll-behavior: smooth; }
        
        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            color: var(--text-main);
            line-height: 1.6;
            background-color: var(--white);
            overflow-x: hidden;
        }

        h1, h2, h3, h4 { color: var(--primary-dark); line-height: 1.2; }
        p { color: var(--text-muted); }
        a { text-decoration: none; color: inherit; }
        img, iframe { max-width: 100%; display: block; }

        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            padding: 14px 28px;
            border-radius: 50px;
            font-weight: 600;
            font-size: 1rem;
            cursor: pointer;
            transition: var(--transition);
            border: none;
            gap: 8px;
            text-decoration: none;
        }

        .btn-primary {
            background: var(--primary-blue);
            color: var(--white);
            box-shadow: 0 4px 12px rgba(0, 102, 255, 0.3);
        }

        .btn-primary:hover {
            background: var(--accent-blue);
            transform: translateY(-2px);
            box-shadow: 0 6px 16px rgba(0, 102, 255, 0.4);
        }

        .btn-outline {
            background: transparent;
            color: var(--white);
            border: 2px solid var(--white);
        }

        .btn-outline:hover {
            background: var(--white);
            color: var(--primary-dark);
        }

        .section-title {
            text-align: center;
            font-size: clamp(1.8rem, 4vw, 2.5rem);
            margin-bottom: 1rem;
        }

        .section-subtitle {
            text-align: center;
            font-size: 1.1rem;
            max-width: 700px;
            margin: 0 auto 3rem;
        }

        section { padding: 60px 0; }

        /* =========================================
           HEADER & NAV
           ========================================= */
        header {
            position: fixed;
            top: 0; left: 0; right: 0;
            z-index: 1000;
            background: transparent;
            transition: var(--transition);
            padding: 20px 0;
        }

        header.scrolled {
            background: rgba(255, 255, 255, 0.98);
            backdrop-filter: blur(10px);
            box-shadow: var(--shadow-sm);
            padding: 12px 0;
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.3rem;
            font-weight: 800;
            color: var(--white);
            display: flex;
            align-items: center;
            gap: 10px;
            transition: var(--transition);
        }

        .logo-icon {
            width: 40px;
            height: 40px;
            background: linear-gradient(135deg, var(--medical-teal), var(--primary-blue));
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: 900;
            font-size: 1.1rem;
            flex-shrink: 0;
        }

        header.scrolled .logo { color: var(--primary-dark); }

        .logo-text {
            display: flex;
            flex-direction: column;
            line-height: 1.1;
        }

        .logo-text small {
            font-size: 0.7rem;
            font-weight: 400;
            opacity: 0.8;
        }

        .nav-links {
            display: none;
            list-style: none;
            gap: 28px;
        }

        .nav-links a {
            font-weight: 500;
            color: var(--white);
            transition: var(--transition);
            font-size: 0.95rem;
        }

        header.scrolled .nav-links a { color: var(--primary-dark); }
        .nav-links a:hover { color: var(--medical-teal); }

        .hamburger {
            display: block;
            background: none;
            border: none;
            color: var(--white);
            font-size: 1.8rem;
            cursor: pointer;
            transition: var(--transition);
        }

        header.scrolled .hamburger { color: var(--primary-dark); }

        .mobile-menu {
            display: none;
            position: fixed;
            top: 0; left: 0; right: 0; bottom: 0;
            background: var(--primary-dark);
            z-index: 999;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            gap: 30px;
        }

        .mobile-menu.active { display: flex; }

        .mobile-menu a {
            color: var(--white);
            font-size: 1.3rem;
            font-weight: 600;
        }

        .mobile-menu .close-btn {
            position: absolute;
            top: 20px;
            right: 20px;
            background: none;
            border: none;
            color: var(--white);
            font-size: 2rem;
            cursor: pointer;
        }

        /* =========================================
           HERO SECTION
           ========================================= */
        .hero {
            background: linear-gradient(135deg, var(--primary-dark) 0%, #1A3A66 50%, #0D4F8B 100%);
            color: var(--white);
            padding: 120px 0 80px;
            position: relative;
            overflow: hidden;
        }+

        .hero::before {
            content: '';
            position: absolute;
            top: -50%; right: -20%;
            width: 600px; height: 600px;
            background: radial-gradient(circle, rgba(0,180,216,0.2) 0%, transparent 70%);
            border-radius: 50%;
        }

        .hero-content { 
            position: relative; 
            z-index: 1; 
            max-width: 900px; 
            margin: 0 auto;
            text-align: center;
        }

        .hero-badge {
            display: inline-block;
            background: rgba(0, 180, 216, 0.2);
            border: 1px solid rgba(0, 180, 216, 0.4);
            color: var(--medical-teal);
            padding: 6px 16px;
            border-radius: 50px;
            font-size: 0.85rem;
            font-weight: 600;
            margin-bottom: 20px;
        }

        .hero h1 {
            color: var(--white);
            font-size: clamp(2rem, 5vw, 3.2rem);
            margin-bottom: 1rem;
            font-weight: 800;
        }

        .hero h1 span {
            background: linear-gradient(90deg, var(--medical-teal), var(--primary-blue));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero .subtitle {
            color: rgba(255,255,255,0.9);
            font-size: 1.15rem;
            margin-bottom: 2rem;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
        }

        .hero-buttons {
            display: flex;
            gap: 16px;
            justify-content: center;
            flex-wrap: wrap;
            margin-bottom: 3rem;
        }

        .hero-stats {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 15px;
            max-width: 600px;
            margin: 0 auto;
        }

        .stat-item {
            text-align: center;
            padding: 16px;
            background: rgba(255,255,255,0.05);
            border-radius: var(--radius);
            border: 1px solid rgba(255,255,255,0.1);
        }

        .stat-number {
            font-size: 1.8rem;
            font-weight: 800;
            color: var(--medical-teal);
            display: block;
        }

        .stat-label {
            font-size: 0.85rem;
            color: rgba(255,255,255,0.7);
        }

        /* =========================================
           ESPECIALIDADES
           ========================================= */
        .specialties { background: var(--bg-light); }
        
        .specialties-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 30px;
        }

        .specialty-block {
            background: var(--white);
            border-radius: var(--radius);
            padding: 32px 24px;
            box-shadow: var(--shadow-sm);
            border-top: 4px solid;
            transition: var(--transition);
        }

        .specialty-block:hover {
            transform: translateY(-5px);
            box-shadow: var(--shadow-md);
        }

        .specialty-medical { border-top-color: var(--medical-teal); }
        .specialty-industrial { border-top-color: var(--industrial-orange); }

        .specialty-header {
            display: flex;
            align-items: center;
            gap: 16px;
            margin-bottom: 24px;
        }

        .specialty-icon {
            width: 56px; height: 56px;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-shrink: 0;
        }

        .specialty-medical .specialty-icon {
            background: rgba(0, 180, 216, 0.1);
            color: var(--medical-teal);
        }

        .specialty-industrial .specialty-icon {
            background: rgba(255, 107, 53, 0.1);
            color: var(--industrial-orange);
        }

        .specialty-header h3 { font-size: 1.3rem; margin: 0; }
        .specialty-header small { color: var(--text-muted); font-size: 0.85rem; }

        .specialty-list {
            list-style: none;
            display: grid;
            gap: 12px;
        }

        .specialty-list li {
            display: flex;
            align-items: flex-start;
            gap: 10px;
            font-size: 0.95rem;
            color: var(--text-main);
        }

        .specialty-list li svg {
            flex-shrink: 0;
            margin-top: 3px;
        }

        .specialty-medical .specialty-list li svg { color: var(--medical-teal); }
        .specialty-industrial .specialty-list li svg { color: var(--industrial-orange); }

        /* =========================================
           PORTAFOLIO DE PROYECTOS
           ========================================= */
        .portfolio { background: var(--white); }

        .portfolio-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 24px;
        }

        .portfolio-card {
            background: var(--white);
            border-radius: var(--radius);
            overflow: hidden;
            box-shadow: var(--shadow-sm);
            border: 1px solid #E2E8F0;
            transition: var(--transition);
        }

        .portfolio-card:hover {
            transform: translateY(-5px);
            box-shadow: var(--shadow-md);
        }

        .portfolio-image {
            width: 100%;
            height: 200px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4rem;
            position: relative;
        }

        .portfolio-medical .portfolio-image {
            background: linear-gradient(135deg, rgba(0, 180, 216, 0.1), rgba(0, 102, 255, 0.1));
            color: var(--medical-teal);
        }

        .portfolio-industrial .portfolio-image {
            background: linear-gradient(135deg, rgba(255, 107, 53, 0.1), rgba(255, 154, 0, 0.1));
            color: var(--industrial-orange);
        }

        .portfolio-tag {
            position: absolute;
            top: 12px;
            right: 12px;
            padding: 4px 12px;
            border-radius: 50px;
            font-size: 0.75rem;
            font-weight: 600;
            color: white;
        }

        .portfolio-medical .portfolio-tag { background: var(--medical-teal); }
        .portfolio-industrial .portfolio-tag { background: var(--industrial-orange); }

        .portfolio-content {
            padding: 24px;
        }

        .portfolio-content h3 {
            font-size: 1.2rem;
            margin-bottom: 12px;
        }

        .portfolio-content p {
            font-size: 0.95rem;
            margin-bottom: 16px;
        }

        .portfolio-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
        }

        .tech-badge {
            background: var(--bg-light);
            color: var(--text-muted);
            padding: 4px 10px;
            border-radius: 50px;
            font-size: 0.75rem;
            font-weight: 500;
        }

        /* =========================================
           BLOG TÉCNICO
           ========================================= */
        .blog { background: var(--bg-light); }

        .blog-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 24px;
        }

        .blog-card {
            background: var(--white);
            border-radius: var(--radius);
            overflow: hidden;
            box-shadow: var(--shadow-sm);
            transition: var(--transition);
            cursor: pointer;
        }

        .blog-card:hover {
            transform: translateY(-5px);
            box-shadow: var(--shadow-md);
        }

        .blog-image {
            width: 100%;
            height: 180px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3rem;
            background: linear-gradient(135deg, var(--primary-light), var(--white));
            color: var(--primary-blue);
        }

        .blog-content {
            padding: 24px;
        }

        .blog-meta {
            display: flex;
            gap: 16px;
            margin-bottom: 12px;
            font-size: 0.85rem;
            color: var(--text-muted);
        }

        .blog-category {
            color: var(--primary-blue);
            font-weight: 600;
        }

        .blog-content h3 {
            font-size: 1.15rem;
            margin-bottom: 12px;
            line-height: 1.4;
        }

        .blog-content p {
            font-size: 0.9rem;
            margin-bottom: 16px;
        }

        .blog-link {
            color: var(--primary-blue);
            font-weight: 600;
            font-size: 0.9rem;
            display: inline-flex;
            align-items: center;
            gap: 6px;
            transition: var(--transition);
        }

        .blog-link:hover {
            gap: 10px;
        }

        /* =========================================
           SOBRE MÍ
           ========================================= */
        .about-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 40px;
            align-items: center;
        }

        .about-image {
            width: 100%;
            max-width: 300px;
            margin: 0 auto;
            aspect-ratio: 1;
            background: linear-gradient(135deg, var(--primary-light), var(--white));
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 6rem;
            color: var(--primary-blue);
            box-shadow: var(--shadow-md);
            position: relative;
        }

        .about-image::after {
            content: '';
            position: absolute;
            inset: -10px;
            border: 2px dashed var(--primary-light);
            border-radius: 50%;
            animation: rotate 30s linear infinite;
        }

        @keyframes rotate {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        .about-content h2 { margin-bottom: 1rem; }
        .about-content p { margin-bottom: 1rem; font-size: 1.05rem; }

        .credentials {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 20px;
        }

        .credential-tag {
            background: var(--primary-light);
            color: var(--primary-blue);
            padding: 6px 14px;
            border-radius: 50px;
            font-size: 0.85rem;
            font-weight: 600;
        }

        /* =========================================
           TESTIMONIOS
           ========================================= */
        .testimonials { background: var(--bg-light); }

        .testimonials-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 24px;
        }

        .testimonial-card {
            background: var(--white);
            padding: 28px;
            border-radius: var(--radius);
            box-shadow: var(--shadow-sm);
            border: 1px solid #E2E8F0;
            position: relative;
        }

        .testimonial-card::before {
            content: '"';
            position: absolute;
            top: 10px;
            right: 20px;
            font-size: 4rem;
            color: var(--primary-light);
            font-family: Georgia, serif;
            line-height: 1;
        }

        .stars { color: #FBBF24; margin-bottom: 16px; font-size: 1.1rem; }
        
        .testimonial-text {
            font-style: italic;
            margin-bottom: 20px;
            color: var(--text-main);
            position: relative;
            z-index: 1;
        }

        .testimonial-author {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .author-avatar {
            width: 48px; height: 48px;
            border-radius: 50%;
            background: linear-gradient(135deg, var(--medical-teal), var(--primary-blue));
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 700;
            color: var(--white);
            font-size: 1.1rem;
        }

        .author-info strong { display: block; font-size: 0.95rem; color: var(--primary-dark); }
        .author-info span { font-size: 0.85rem; color: var(--text-muted); }

        /* =========================================
           FAQ (ACORDEÓN)
           ========================================= */
        .faq-container { max-width: 800px; margin: 0 auto; }
        
        .faq-item {
            background: var(--white);
            border-radius: var(--radius);
            margin-bottom: 12px;
            box-shadow: var(--shadow-sm);
            overflow: hidden;
            border: 1px solid #E2E8F0;
        }

        .faq-question {
            width: 100%;
            text-align: left;
            padding: 20px 24px;
            background: none;
            border: none;
            font-size: 1rem;
            font-weight: 600;
            color: var(--primary-dark);
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 16px;
            transition: var(--transition);
            font-family: inherit;
        }

        .faq-question:hover { color: var(--primary-blue); }

        .faq-icon {
            transition: transform 0.3s ease;
            font-size: 1.5rem;
            color: var(--primary-blue);
            flex-shrink: 0;
            line-height: 1;
        }

        .faq-item.active .faq-icon { transform: rotate(45deg); }

        .faq-answer {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease, padding 0.3s ease;
            padding: 0 24px;
        }

        .faq-item.active .faq-answer {
            max-height: 400px;
            padding: 0 24px 20px;
        }

        /* =========================================
           CONTACTO
           ========================================= */
        .contact { background: var(--bg-light); }

        .contact-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 40px;
            max-width: 1100px;
            margin: 0 auto;
        }

        .contact-info h3 { margin-bottom: 16px; font-size: 1.5rem; }
        .contact-info > p { margin-bottom: 28px; }

        .info-item {
            display: flex;
            align-items: flex-start;
            gap: 14px;
            margin-bottom: 20px;
            padding: 16px;
            background: var(--white);
            border-radius: var(--radius);
            box-shadow: var(--shadow-sm);
            transition: var(--transition);
        }

        .info-item:hover {
            transform: translateX(5px);
            box-shadow: var(--shadow-md);
        }

        .info-icon {
            width: 44px; height: 44px;
            background: var(--primary-light);
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--primary-blue);
            flex-shrink: 0;
        }

        .info-item strong { display: block; color: var(--primary-dark); margin-bottom: 2px; }
        .info-item span, .info-item a { 
            color: var(--text-muted); 
            font-size: 0.95rem; 
            word-break: break-word;
        }
        .info-item a:hover { color: var(--primary-blue); }

        .social-links {
            display: flex;
            gap: 12px;
            margin-top: 24px;
            flex-wrap: wrap;
        }

        .social-link {
            width: 44px; height: 44px;
            border-radius: 10px;
            background: var(--white);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--primary-blue);
            box-shadow: var(--shadow-sm);
            transition: var(--transition);
        }

        .social-link:hover {
            background: var(--primary-blue);
            color: var(--white);
            transform: translateY(-3px);
        }

        .contact-form {
            background: var(--white);
            padding: 32px 24px;
            border-radius: var(--radius);
            box-shadow: var(--shadow-md);
        }

        .form-group { margin-bottom: 20px; }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            font-size: 0.9rem;
            color: var(--primary-dark);
        }

        .form-group input,
        .form-group select,
        .form-group textarea {
            width: 100%;
            padding: 12px 16px;
            border: 1px solid #CBD5E1;
            border-radius: 8px;
            font-size: 1rem;
            font-family: inherit;
            transition: var(--transition);
            outline: none;
            background: var(--white);
        }

        .form-group input:focus,
        .form-group select:focus,
        .form-group textarea:focus {
            border-color: var(--primary-blue);
            box-shadow: 0 0 0 3px rgba(0, 102, 255, 0.1);
        }

        .form-group textarea { resize: vertical; min-height: 120px; }
        
        .error-msg {
            color: var(--error);
            font-size: 0.85rem;
            margin-top: 6px;
            display: none;
        }

        .form-group.error input { border-color: var(--error); }
        .form-group.error .error-msg { display: block; }

        .form-success {
            display: none;
            background: #DCFCE7;
            color: var(--success);
            padding: 16px;
            border-radius: 8px;
            text-align: center;
            font-weight: 600;
            margin-top: 16px;
        }

        /* =========================================
           GOOGLE MAPS
           ========================================= */
        .map-section {
            padding: 0;
            background: var(--white);
        }

        .map-container {
            width: 100%;
            height: 400px;
            position: relative;
        }

        .map-container iframe {
            width: 100%;
            height: 100%;
            border: 0;
        }

        .map-overlay {
            position: absolute;
            bottom: 20px;
            left: 20px;
            background: var(--white);
            padding: 20px;
            border-radius: var(--radius);
            box-shadow: var(--shadow-md);
            max-width: 300px;
        }

        .map-overlay h4 {
            margin-bottom: 8px;
            font-size: 1.1rem;
        }

        .map-overlay p {
            font-size: 0.9rem;
            margin-bottom: 12px;
        }

        .map-overlay a {
            color: var(--primary-blue);
            font-weight: 600;
            font-size: 0.9rem;
        }

        /* =========================================
           FOOTER
           ========================================= */
        footer {
            background: var(--primary-dark);
            color: var(--white);
            padding: 60px 0 20px;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-col h4 {
            color: var(--white);
            margin-bottom: 20px;
            font-size: 1.1rem;
        }

        .footer-col p, .footer-col a {
            color: rgba(255,255,255,0.7);
            font-size: 0.95rem;
            margin-bottom: 12px;
            display: block;
            transition: var(--transition);
        }

        .footer-col a:hover { color: var(--medical-teal); }

        .footer-bottom {
            border-top: 1px solid rgba(255,255,255,0.1);
            padding-top: 20px;
            text-align: center;
            color: rgba(255,255,255,0.5);
            font-size: 0.85rem;
        }

        .footer-bottom a { 
            color: rgba(255,255,255,0.7); 
            margin: 0 10px;
            display: inline-block;
        }
        .footer-bottom a:hover { color: var(--white); }

        /* =========================================
           WHATSAPP FLOTANTE
           ========================================= */
        .whatsapp-float {
            position: fixed;
            bottom: 24px;
            right: 24px;
            width: 60px;
            height: 60px;
            background: var(--whatsapp-green);
            color: var(--white);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 4px 16px rgba(37, 211, 102, 0.4);
            z-index: 999;
            transition: var(--transition);
            animation: pulse 2s infinite;
        }

        .whatsapp-float:hover {
            transform: scale(1.1);
            animation: none;
        }

        @keyframes pulse {
            0% { box-shadow: 0 0 0 0 rgba(37, 211, 102, 0.7); }
            70% { box-shadow: 0 0 0 15px rgba(37, 211, 102, 0); }
            100% { box-shadow: 0 0 0 0 rgba(37, 211, 102, 0); }
        }

        /* =========================================
           MEDIA QUERIES (RESPONSIVIDAD TOTAL)
           ========================================= */
        
        /* Móviles Pequeños (< 480px) */
        @media (max-width: 480px) {
            .hero { padding: 100px 0 60px; }
            .hero h1 { font-size: 1.8rem; }
            .hero .subtitle { font-size: 1rem; }
            .btn { padding: 12px 20px; font-size: 0.9rem; }
            .section-title { font-size: 1.6rem; }
            .section-subtitle { font-size: 1rem; margin-bottom: 2rem; }
            .map-container { height: 300px; }
            .map-overlay { max-width: 80%; bottom: 10px; left: 10px; padding: 15px; }
        }

        /* Tablets y Laptops Pequeñas (>= 768px) */
        @media (min-width: 768px) {
            .nav-links { display: flex; }
            .hamburger { display: none; }
            
            .hero-stats { grid-template-columns: repeat(4, 1fr); }
            .specialties-grid { grid-template-columns: repeat(2, 1fr); }
            .portfolio-grid { grid-template-columns: repeat(2, 1fr); }
            .blog-grid { grid-template-columns: repeat(2, 1fr); }
            .about-grid { grid-template-columns: 1fr 1.5fr; }
            .testimonials-grid { grid-template-columns: repeat(2, 1fr); }
            .contact-grid { grid-template-columns: 1fr 1.2fr; }
            .footer-grid { grid-template-columns: repeat(2, 1fr); }
            .map-container { height: 450px; }
        }

        /* Escritorios y Monitores Grandes (>= 1024px) */
        @media (min-width: 1024px) {
            .portfolio-grid { grid-template-columns: repeat(3, 1fr); }
            .blog-grid { grid-template-columns: repeat(3, 1fr); }
            .testimonials-grid { grid-template-columns: repeat(3, 1fr); }
            .footer-grid { grid-template-columns: repeat(3, 1fr); }
            .map-container { height: 500px; }
        }

        /* Pantallas Ultra-Anchas (>= 1440px) */
        @media (min-width: 1440px) {
            .container { max-width: 1400px; }
            .hero h1 { font-size: 3.5rem; }
        }
    </style>
</head>
<body>

    <!-- HEADER -->
    <header id="main-header">
        <div class="container nav-container">
            <a href="#" class="logo">
                <div class="logo-icon">NDG</div>
                <div class="logo-text">
                    <span>Ing. Noel Daudinot</span>
                    <small>Tecnología Médica & Industrial</small>
                </div>
            </a>
            <nav>
                <ul class="nav-links">
                    <li><a href="#especialidades">Especialidades</a></li>
                    <li><a href="#portafolio">Portafolio</a></li>
                    <li><a href="#blog">Blog</a></li>
                    <li><a href="#sobre-mi">Sobre Mí</a></li>
                    <li><a href="#testimonios">Testimonios</a></li>
                    <li><a href="#faq">FAQ</a></li>
                    <li><a href="#contacto">Contacto</a></li>
                </ul>
            </nav>
            <button class="hamburger" id="hamburger" aria-label="Menú">☰</button>
        </div>
    </header>

    <!-- MOBILE MENU -->
    <div class="mobile-menu" id="mobileMenu">
        <button class="close-btn" id="closeMenu">✕</button>
        <a href="#especialidades" class="mobile-link">Especialidades</a>
        <a href="#portafolio" class="mobile-link">Portafolio</a>
        <a href="#blog" class="mobile-link">Blog</a>
        <a href="#sobre-mi" class="mobile-link">Sobre Mí</a>
        <a href="#testimonios" class="mobile-link">Testimonios</a>
        <a href="#faq" class="mobile-link">FAQ</a>
        <a href="#contacto" class="mobile-link">Contacto</a>
    </div>

    <main>
        <!-- HERO -->
        <section class="hero" id="inicio">
            <div class="container hero-content">
                <span class="hero-badge">⚡ Ingeniero Certificado • +20 años de experiencia</span>
                <h1>Soluciones Integrales en <span>Tecnología Médica e Industrial</span></h1>
                <p class="subtitle">Ing. Noel Daudinot G — Especialista en Telecomunicaciones y Electrónica. Experto en equipos de imagenología médica (TAC, RM, RX) y automatización industrial (PLC, FPGA, Variadores).</p>
                
                <div class="hero-buttons">
                    <a href="#contacto" class="btn btn-primary">
                        Cotizar ahora
                        <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><line x1="5" y1="12" x2="19" y2="12"></line><polyline points="12 5 19 12 12 19"></polyline></svg>
                    </a>
                    <a href="https://wa.me/584247067782?text=Hola%20Ing.%20Noel,%20necesito%20información%20sobre%20sus%20servicios" class="btn btn-outline" target="_blank" rel="noopener">
                        <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413Z"/></svg>
                        WhatsApp
                    </a>
                </div>

                <div class="hero-stats">
                    <div class="stat-item">
                        <span class="stat-number">20+</span>
                        <span class="stat-label">Años de Experiencia</span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-number">500+</span>
                        <span class="stat-label">Equipos Reparados</span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-number">100%</span>
                        <span class="stat-label">Garantía Técnica</span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-number">24/7</span>
                        <span class="stat-label">Soporte Remoto</span>
                    </div>
                </div>
            </div>
        </section>

        <!-- ESPECIALIDADES -->
        <section class="specialties" id="especialidades">
            <div class="container">
                <h2 class="section-title">Mis Áreas de Especialización</h2>
                <p class="section-subtitle">Dos décadas de experiencia combinada en los sectores más exigentes de la ingeniería electrónica y de telecomunicaciones.</p>
                
                <div class="specialties-grid">
                    <!-- TECNOLOGÍA MÉDICA -->
                    <div class="specialty-block specialty-medical">
                        <div class="specialty-header">
                            <div class="specialty-icon">
                                <svg width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M22 12h-4l-3 9L9 3l-3 9H2"/></svg>
                            </div>
                            <div>
                                <h3>Tecnología Médica</h3>
                                <small>Equipos de Imagenología Diagnóstica</small>
                            </div>
                        </div>
                        <ul class="specialty-list">
                            <li>
                                <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><polyline points="20 6 9 17 4 12"/></svg>
                                <div><strong>TAC (Tomografía Axial Computarizada)</strong> — Instalación, mantenimiento preventivo y correctivo.</div>
                            </li>
                            <li>
                                <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><polyline points="20 6 9 17 4 12"/></svg>
                                <div><strong>RM (Resonancia Magnética)</strong> — Diagnóstico de fallas en imanes, gradientes y RF.</div>
                            </li>
                            <li>
                                <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><polyline points="20 6 9 17 4 12"/></svg>
                                <div><strong>Rayos X (RX) y Fluoroscopía</strong> — Calibración y reparación de generadores.</div>
                            </li>
                            <li>
                                <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><polyline points="20 6 9 17 4 12"/></svg>
                                <div><strong>Mamografía (MX) y Densitometría (DX)</strong> — Optimización de imagen y dosis.</div>
                            </li>
                            <li>
                                <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><polyline points="20 6 9 17 4 12"/></svg>
                                <div><strong>Angiografía</strong> — Sistemas de sustracción digital y cateterismo.</div>
                            </li>
                        </ul>
                    </div>

                    <!-- TECNOLOGÍA INDUSTRIAL -->
                    <div class="specialty-block specialty-industrial">
                        <div class="specialty-header">
                            <div class="specialty-icon">
                                <svg width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M2 20a2 2 0 0 0 2 2h16a2 2 0 0 0 2-2V8l-7 5V8l-7 5V4a2 2 0 0 0-2-2H4a2 2 0 0 0-2 2Z"/></svg>
                            </div>
                            <div>
                                <h3>Automatización Industrial</h3>
                                <small>Control y Potencia</small>
                            </div>
                        </div>
                        <ul class="specialty-list">
                            <li>
                                <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><polyline points="20 6 9 17 4 12"/></svg>
                                <div><strong>Variadores de Frecuencia</strong> — Programación, parametrización y reparación.</div>
                            </li>
                            <li>
                                <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><polyline points="20 6 9 17 4 12"/></svg>
                                <div><strong>Sistemas PLC</strong> — Siemens, Allen Bradley, Schneider. Lógica y HMI.</div>
                            </li>
                            <li>
                                <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><polyline points="20 6 9 17 4 12"/></svg>
                                <div><strong>FPGA</strong> — Diseño y programación de lógica programable.</div>
                            </li>
                            <li>
                                <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><polyline points="20 6 9 17 4 12"/></svg>
                                <div><strong>Microcontroladores PIC</strong> — Desarrollo de firmware y hardware a medida.</div>
                            </li>
                            <li>
                                <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><polyline points="20 6 9 17 4 12"/></svg>
                                <div><strong>Inversores de Voltaje</strong> — UPS industriales y sistemas de respaldo.</div>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>

        <!-- PORTAFOLIO DE PROYECTOS -->
        <section class="portfolio" id="portafolio">
            <div class="container">
                <h2 class="section-title">Portafolio de Proyectos</h2>
                <p class="section-subtitle">Casos de éxito reales en tecnología médica e industrial que demuestran mi experiencia y capacidad técnica.</p>
                
                <div class="portfolio-grid">
                    <div class="portfolio-card portfolio-medical">
                        <div class="portfolio-image">
                            🏥
                            <span class="portfolio-tag">Médico</span>
                        </div>
                        <div class="portfolio-content">
                            <h3>Mantenimiento TAC Siemens Somatom</h3>
                            <p>Diagnóstico y reparación de falla en sistema de rotación del gantry. Restauración completa en 18 horas.</p>
                            <div class="portfolio-tech">
                                <span class="tech-badge">TAC</span>
                                <span class="tech-badge">Siemens</span>
                                <span class="tech-badge">Gantry</span>
                            </div>
                        </div>
                    </div>

                    <div class="portfolio-card portfolio-industrial">
                        <div class="portfolio-image">
                            🏭
                            <span class="portfolio-tag">Industrial</span>
                        </div>
                        <div class="portfolio-content">
                            <h3>Automatización Línea de Producción</h3>
                            <p>Diseño e implementación de sistema PLC Siemens S7-1200 con HMI para control de proceso continuo.</p>
                            <div class="portfolio-tech">
                                <span class="tech-badge">PLC</span>
                                <span class="tech-badge">Siemens S7-1200</span>
                                <span class="tech-badge">HMI</span>
                            </div>
                        </div>
                    </div>

                    <div class="portfolio-card portfolio-medical">
                        <div class="portfolio-image">
                            🧲
                            <span class="portfolio-tag">Médico</span>
                        </div>
                        <div class="portfolio-content">
                            <h3>Calibración Resonancia Magnética GE</h3>
                            <p>Optimización de secuencias de imagen y calibración de bobinas de gradiente en equipo 1.5T.</p>
                            <div class="portfolio-tech">
                                <span class="tech-badge">RM 1.5T</span>
                                <span class="tech-badge">GE Healthcare</span>
                                <span class="tech-badge">Calibración</span>
                            </div>
                        </div>
                    </div>

                    <div class="portfolio-card portfolio-industrial">
                        <div class="portfolio-image">
                            ⚡
                            <span class="portfolio-tag">Industrial</span>
                        </div>
                        <div class="portfolio-content">
                            <h3>Sistema de Control con FPGA</h3>
                            <p>Desarrollo de sistema de adquisición de datos de alta velocidad para monitoreo de vibraciones industriales.</p>
                            <div class="portfolio-tech">
                                <span class="tech-badge">FPGA</span>
                                <span class="tech-badge">Xilinx</span>
                                <span class="tech-badge">VHDL</span>
                            </div>
                        </div>
                    </div>

                    <div class="portfolio-card portfolio-medical">
                        <div class="portfolio-image">
                            📡
                            <span class="portfolio-tag">Médico</span>
                        </div>
                        <div class="portfolio-content">
                            <h3>Instalación Sistema de Angiografía</h3>
                            <p>Puesta en marcha de equipo de angiografía por sustracción digital con sistema de flat panel detector.</p>
                            <div class="portfolio-tech">
                                <span class="tech-badge">Angiografía</span>
                                <span class="tech-badge">Philips</span>
                                <span class="tech-badge">Flat Panel</span>
                            </div>
                        </div>
                    </div>

                    <div class="portfolio-card portfolio-industrial">
                        <div class="portfolio-image">
                            🔧
                            <span class="portfolio-tag">Industrial</span>
                        </div>
                        <div class="portfolio-content">
                            <h3>Reparación Variador de Frecuencia ABB</h3>
                            <p>Diagnóstico de falla en etapa de potencia y reemplazo de IGBTs. Pruebas de carga completadas exitosamente.</p>
                            <div class="portfolio-tech">
                                <span class="tech-badge">Variador</span>
                                <span class="tech-badge">ABB ACS800</span>
                                <span class="tech-badge">IGBT</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- BLOG TÉCNICO -->
        <section class="blog" id="blog">
            <div class="container">
                <h2 class="section-title">Blog Técnico</h2>
                <p class="section-subtitle">Artículos y guías técnicas sobre mantenimiento de equipos médicos y automatización industrial.</p>
                
                <div class="blog-grid">
                    <article class="blog-card">
                        <div class="blog-image">📋</div>
                        <div class="blog-content">
                            <div class="blog-meta">
                                <span class="blog-category">Tecnología Médica</span>
                                <span>5 min lectura</span>
                            </div>
                            <h3>Guía de Mantenimiento Preventivo para Equipos de TAC</h3>
                            <p>Aprende los protocolos esenciales de mantenimiento preventivo que todo centro de imagenología debe implementar para maximizar la vida útil de su tomógrafo.</p>
                            <a href="#" class="blog-link">
                                Leer más
                                <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><line x1="5" y1="12" x2="19" y2="12"/><polyline points="12 5 19 12 12 19"/></svg>
                            </a>
                        </div>
                    </article>

                    <article class="blog-card">
                        <div class="blog-image">⚙️</div>
                        <div class="blog-content">
                            <div class="blog-meta">
                                <span class="blog-category">Automatización</span>
                                <span>7 min lectura</span>
                            </div>
                            <h3>Programación PLC Siemens S7-1200: Mejores Prácticas</h3>
                            <p>Descubre las mejores prácticas para estructurar tus programas en TIA Portal, optimizar el uso de memoria y mejorar la mantenibilidad del código.</p>
                            <a href="#" class="blog-link">
                                Leer más
                                <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><line x1="5" y1="12" x2="19" y2="12"/><polyline points="12 5 19 12 12 19"/></svg>
                            </a>
                        </div>
                    </article>

                    <article class="blog-card">
                        <div class="blog-image">🔬</div>
                        <div class="blog-content">
                            <div class="blog-meta">
                                <span class="blog-category">Tecnología Médica</span>
                                <span>6 min lectura</span>
                            </div>
                            <h3>Diagnóstico de Fallas Comunes en Resonancia Magnética</h3>
                            <p>Identifica y resuelve las fallas más frecuentes en equipos de RM: problemas de RF, gradientes, criogenia y sistemas de enfriamiento.</p>
                            <a href="#" class="blog-link">
                                Leer más
                                <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><line x1="5" y1="12" x2="19" y2="12"/><polyline points="12 5 19 12 12 19"/></svg>
                            </a>
                        </div>
                    </article>

                    <article class="blog-card">
                        <div class="blog-image">🔌</div>
                        <div class="blog-content">
                            <div class="blog-meta">
                                <span class="blog-category">Automatización</span>
                                <span>8 min lectura</span>
                            </div>
                            <h3>Parametrización de Variadores de Frecuencia: Guía Completa</h3>
                            <p>Todo lo que necesitas saber para configurar correctamente un variador de frecuencia: parámetros básicos, avanzados y optimización de rendimiento.</p>
                            <a href="#" class="blog-link">
                                Leer más
                                <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><line x1="5" y1="12" x2="19" y2="12"/><polyline points="12 5 19 12 12 19"/></svg>
                            </a>
                        </div>
                    </article>

                    <article class="blog-card">
                        <div class="blog-image">💻</div>
                        <div class="blog-content">
                            <div class="blog-meta">
                                <span class="blog-category">Electrónica</span>
                                <span>10 min lectura</span>
                            </div>
                            <h3>Introducción a FPGA: De la Teoría a la Práctica</h3>
                            <p>Aprende los fundamentos de las FPGAs, diferencias con microcontroladores, lenguajes HDL (VHDL/Verilog) y casos de uso en aplicaciones industriales.</p>
                            <a href="#" class="blog-link">
                                Leer más
                                <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><line x1="5" y1="12" x2="19" y2="12"/><polyline points="12 5 19 12 12 19"/></svg>
                            </a>
                        </div>
                    </article>

                    <article class="blog-card">
                        <div class="blog-image"></div>
                        <div class="blog-content">
                            <div class="blog-meta">
                                <span class="blog-category">Tecnología Médica</span>
                                <span>5 min lectura</span>
                            </div>
                            <h3>Calibración de Equipos de Rayos X: Normativas y Procedimientos</h3>
                            <p>Conoce los estándares internacionales para calibración de equipos de radiología y los procedimientos que garantizan dosis óptimas y calidad de imagen.</p>
                            <a href="#" class="blog-link">
                                Leer más
                                <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><line x1="5" y1="12" x2="19" y2="12"/><polyline points="12 5 19 12 12 19"/></svg>
                            </a>
                        </div>
                    </article>
                </div>
            </div>
        </section>

        <!-- SOBRE MÍ -->
        <section class="about" id="sobre-mi">
            <div class="container">
                <div class="about-grid">
                    <div class="about-image">‍🔬</div>
                    <div class="about-content">
                        <h2>Sobre Mí</h2>
                        <p>Soy <strong>Noel Daudinot G</strong>, Ingeniero en Telecomunicaciones y Electrónica con más de dos décadas de experiencia resolviendo los desafíos técnicos más complejos en los sectores médico e industrial.</p>
                        <p>Mi carrera me ha permitido especializarme en <strong>tecnología médica de alta gama</strong> (equipos de imagenología como TAC, RM, Rayos X, Mamografía y Angiografía) y en <strong>automatización industrial</strong> (PLC, FPGA, variadores de frecuencia, microcontroladores PIC e inversores de voltaje).</p>
                        <p>Mi compromiso es ofrecer soluciones técnicas precisas, confiables y con garantía, minimizando el tiempo de inactividad de tus equipos críticos.</p>
                        
                        <div class="credentials">
                            <span class="credential-tag">Ing. Telecomunicaciones</span>
                            <span class="credential-tag">Ing. Electrónica</span>
                            <span class="credential-tag">TAC & RM</span>
                            <span class="credential-tag">PLC & FPGA</span>
                            <span class="credential-tag">Variadores</span>
                            <span class="credential-tag">PIC</span>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- TESTIMONIOS -->
        <section class="testimonials" id="testimonios">
            <div class="container">
                <h2 class="section-title">Lo que dicen mis clientes</h2>
                <p class="section-subtitle">Hospitales, clínicas e industrias que confían en mi experiencia técnica.</p>
                
                <div class="testimonials-grid">
                    <div class="testimonial-card">
                        <div class="stars">★★★★★</div>
                        <p class="testimonial-text">"El Ing. Daudinot reparó nuestro equipo de TAC en tiempo récord. Su conocimiento en tecnología médica es excepcional. Redujimos el tiempo de inactividad a solo 6 horas."</p>
                        <div class="testimonial-author">
                            <div class="author-avatar">DR</div>
                            <div class="author-info">
                                <strong>Dr. Rodríguez</strong>
                                <span>Director - Clínica Central</span>
                            </div>
                        </div>
                    </div>
                    <div class="testimonial-card">
                        <div class="stars">★★★★★</div>
                        <p class="testimonial-text">"Programó el PLC de nuestra línea de producción y optimizó el variador de frecuencia. La eficiencia aumentó un 25%. Profesionalismo y conocimiento técnico de primer nivel."</p>
                        <div class="testimonial-author">
                            <div class="author-avatar">JM</div>
                            <div class="author-info">
                                <strong>Juan Martínez</strong>
                                <span>Gerente de Planta Industrial</span>
                            </div>
                        </div>
                    </div>
                    <div class="testimonial-card">
                        <div class="stars">★★★★★</div>
                        <p class="testimonial-text">"Excelente servicio con nuestro equipo de Resonancia Magnética. Diagnóstico preciso y solución definitiva. Lo recomiendo totalmente para cualquier centro de imagenología."</p>
                        <div class="testimonial-author">
                            <div class="author-avatar">ML</div>
                            <div class="author-info">
                                <strong>Dra. María López</strong>
                                <span>Radióloga - Centro de Diagnóstico</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- FAQ -->
        <section class="faq" id="faq">
            <div class="container">
                <h2 class="section-title">Preguntas Frecuentes</h2>
                <p class="section-subtitle">Respuestas a las consultas más comunes sobre mis servicios.</p>
                
                <div class="faq-container">
                    <div class="faq-item">
                        <button class="faq-question">
                            ¿Qué tipos de equipos médicos atiende?
                            <span class="faq-icon">+</span>
                        </button>
                        <div class="faq-answer">
                            <p>Atiendo equipos de imagenología de alta complejidad: Tomografía Axial Computarizada (TAC), Resonancia Magnética (RM), Rayos X convencionales y digitales, Mamografía (MX), Densitometría Ósea (DX) y sistemas de Angiografía. Realizo mantenimiento preventivo, correctivo, calibración e instalación.</p>
                        </div>
                    </div>
                    <div class="faq-item">
                        <button class="faq-question">
                            ¿Trabaja con todas las marcas de PLC y variadores?
                            <span class="faq-icon">+</span>
                        </button>
                        <div class="faq-answer">
                            <p>Sí, tengo experiencia con las principales marcas del mercado: Siemens (S7-200, S7-300, S7-1200, S7-1500), Allen Bradley (CompactLogix, ControlLogix), Schneider Electric (Modicon), ABB, Danfoss, Siemens, WEG, entre otros. También programo FPGAs y desarrollo firmware para microcontroladores PIC.</p>
                        </div>
                    </div>
                    <div class="faq-item">
                        <button class="faq-question">
                            ¿Ofrece servicio de emergencia 24/7?
                            <span class="faq-icon">+</span>
                        </button>
                        <div class="faq-answer">
                            <p>Sí, entiendo que en el sector médico e industrial el tiempo de inactividad es crítico. Ofrezco soporte remoto 24/7 para diagnóstico inicial y asistencia técnica. Para servicios presenciales de emergencia, coordino la visita en el menor tiempo posible según la ubicación.</p>
                        </div>
                    </div>
                    <div class="faq-item">
                        <button class="faq-question">
                            ¿Realiza proyectos de automatización a medida?
                            <span class="faq-icon">+</span>
                        </button>
                        <div class="faq-answer">
                            <p>Absolutamente. Diseño y desarrollo soluciones de automatización personalizadas usando PLC, FPGA, PIC y sistemas SCADA. Desde el diseño del circuito impreso hasta la programación del firmware y la puesta en marcha en planta.</p>
                        </div>
                    </div>
                    <div class="faq-item">
                        <button class="faq-question">
                            ¿Cómo solicito una cotización?
                            <span class="faq-icon">+</span>
                        </button>
                        <div class="faq-answer">
                            <p>Puedes contactarme directamente por WhatsApp (+58 424-706-7782), llenar el formulario de contacto en esta página, o enviarme un correo a noelakula05@gmail.com. Incluyendo marca, modelo y descripción de la falla, te enviaré un presupuesto preliminar sin compromiso.</p>
                        </div>
                    </div>
                    <div class="faq-item">
                        <button class="faq-question">
                            ¿Ofrece capacitación técnica?
                            <span class="faq-icon">+</span>
                        </button>
                        <div class="faq-answer">
                            <p>Sí, ofrezco cursos y asesorías técnicas especializadas en: mantenimiento de equipos médicos de imagenología, programación de PLC, diseño con FPGA, programación de PIC y configuración de variadores de frecuencia. Consultame por programas personalizados para tu equipo.</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- CONTACTO -->
        <section class="contact" id="contacto">
            <div class="container">
                <h2 class="section-title">Contáctame</h2>
                <p class="section-subtitle">Cuéntame sobre tu proyecto o falla técnica. Respondo en menos de 2 horas.</p>
                
                <div class="contact-grid">
                    <div class="contact-info">
                        <h3>Información de Contacto</h3>
                        <p>Estoy disponible para atenderte por múltiples canales. Elige el que prefieras.</p>
                        
                        <div class="info-item">
                            <div class="info-icon">
                                <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z"/></svg>
                            </div>
                            <div>
                                <strong>Teléfonos</strong>
                                <a href="tel:+584247067782">+58 424-706-7782</a><br>
                                <a href="tel:+584247413224">+58 424-741-3224</a>
                            </div>
                        </div>
                        
                        <div class="info-item">
                            <div class="info-icon">
                                <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
                            </div>
                            <div>
                                <strong>Correos Electrónicos</strong>
                                <a href="mailto:noelakula05@gmail.com">noelakula05@gmail.com</a><br>
                                <a href="mailto:noeldg2002@yahoo.es">noeldg2002@yahoo.es</a>
                            </div>
                        </div>

                        <div class="info-item">
                            <div class="info-icon">
                                <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"/><polyline points="12 6 12 12 16 14"/></svg>
                            </div>
                            <div>
                                <strong>Horario de Atención</strong>
                                <span>Lun - Sáb: 8:00 AM - 6:00 PM</span><br>
                                <span>Emergencias: 24/7</span>
                            </div>
                        </div>

                        <div class="social-links">
                            <a href="https://x.com/NEUTRINO1205" class="social-link" target="_blank" rel="noopener" aria-label="Twitter/X">
                                <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor"><path d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z"/></svg>
                            </a>
                            <a href="https://t.me/NDGAkula" class="social-link" target="_blank" rel="noopener" aria-label="Telegram">
                                <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor"><path d="M11.944 0A12 12 0 0 0 0 12a12 12 0 0 0 12 12 12 12 0 0 0 12-12A12 12 0 0 0 12 0a12 12 0 0 0-.056 0zm4.962 7.224c.1-.002.321.023.465.14a.506.506 0 0 1 .171.325c.016.093.036.306.02.472-.18 1.898-.962 6.502-1.36 8.627-.168.9-.499 1.201-.82 1.23-.696.065-1.225-.46-1.9-.902-1.056-.693-1.653-1.124-2.678-1.8-1.185-.78-.417-1.21.258-1.91.177-.184 3.247-2.977 3.307-3.23.007-.032.014-.15-.056-.212s-.174-.041-.249-.024c-.106.024-1.793 1.14-5.061 3.345-.48.33-.913.49-1.302.48-.428-.008-1.252-.241-1.865-.44-.752-.245-1.349-.374-1.297-.789.027-.216.325-.437.893-.663 3.498-1.524 5.83-2.529 6.998-3.014 3.332-1.386 4.025-1.627 4.476-1.635z"/></svg>
                            </a>
                            <a href="https://wa.me/584247067782" class="social-link" target="_blank" rel="noopener" aria-label="WhatsApp" style="background: var(--whatsapp-green); color: white;">
                                <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413Z"/></svg>
                            </a>
                        </div>
                    </div>

                    <form class="contact-form" id="contactForm" novalidate>
                        <div class="form-group">
                            <label for="nombre">Nombre completo *</label>
                            <input type="text" id="nombre" name="nombre" required placeholder="Ej: Dr. Juan Pérez">
                        </div>
                        <div class="form-group">
                            <label for="email">Correo electrónico *</label>
                            <input type="email" id="email" name="email" required placeholder="tucorreo@ejemplo.com">
                            <span class="error-msg">Por favor, ingresa un correo electrónico válido.</span>
                        </div>
                        <div class="form-group">
                            <label for="telefono">Teléfono / WhatsApp</label>
                            <input type="tel" id="telefono" name="telefono" placeholder="+58 4XX-XXX-XXXX">
                        </div>
                        <div class="form-group">
                            <label for="servicio">Tipo de servicio *</label>
                            <select id="servicio" name="servicio" required>
                                <option value="">Selecciona una opción</option>
                                <optgroup label="Tecnología Médica">
                                    <option value="tac">Mantenimiento de TAC</option>
                                    <option value="rm">Mantenimiento de Resonancia Magnética</option>
                                    <option value="rx">Reparación de Rayos X</option>
                                    <option value="mamografia">Mamografía / Densitometría</option>
                                    <option value="angiografia">Angiografía</option>
                                    <option value="otro-medico">Otro equipo médico</option>
                                </optgroup>
                                <optgroup label="Automatización Industrial">
                                    <option value="plc">Programación/Reparación PLC</option>
                                    <option value="variador">Variadores de Frecuencia</option>
                                    <option value="fpga">Desarrollo FPGA</option>
                                    <option value="pic">Programación PIC</option>
                                    <option value="inversor">Inversores de Voltaje</option>
                                    <option value="otro-industrial">Otro servicio industrial</option>
                                </optgroup>
                                <option value="consultoria">Consultoría / Capacitación</option>
                            </select>
                        </div>
                        <div class="form-group">
                            <label for="mensaje">Describe tu requerimiento *</label>
                            <textarea id="mensaje" name="mensaje" required placeholder="Marca, modelo del equipo, tipo de falla o proyecto que necesitas desarrollar..."></textarea>
                        </div>
                        <button type="submit" class="btn btn-primary" style="width: 100%;">
                            Enviar Solicitud
                            <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><line x1="22" y1="2" x2="11" y2="13"/><polygon points="22 2 15 22 11 13 2 9 22 2"/></svg>
                        </button>
                        <div class="form-success" id="formSuccess">
                            ✅ ¡Mensaje enviado con éxito! Te contactaré en menos de 2 horas.
                        </div>
                    </form>
                </div>
            </div>
        </section>

        <!-- GOOGLE MAPS -->
        <section class="map-section">
            <div class="map-container">
                <!-- Mapa embebido apuntando a San Cristóbal, Táchira, Venezuela -->
                <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d126278.760928!2d-72.295!3d7.7669!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x8e64155555555555%3A0x0!2sSan+Crist%C3%B3bal%2C+T%C3%A1chira!5e0!3m2!1ses!2sve!4v1700000000000!5m2!1ses!2sve" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
                <div class="map-overlay">
                    <h4>📍 Ubicación</h4>
                    <p>San Cristóbal, Táchira<br>Venezuela<br>Servicio a nivel nacional</p>
                    <a href="https://maps.google.com/?q=San+Crist%C3%B3bal,+T%C3%A1chira,+Venezuela" target="_blank" rel="noopener">Ver en Google Maps →</a>
                </div>
            </div>
        </section>
    </main>

    <!-- FOOTER -->
    <footer>
        <div class="container">
            <div class="footer-grid">
                <div class="footer-col">
                    <h4>Ing. Noel Daudinot G</h4>
                    <p>Ingeniero en Telecomunicaciones y Electrónica. Especialista en Tecnología Médica (TAC, RM, RX, DX, MX, Angiografía) y Automatización Industrial (PLC, FPGA, PIC, Variadores).</p>
                </div>
                <div class="footer-col">
                    <h4>Enlaces Rápidos</h4>
                    <a href="#especialidades">Especialidades</a>
                    <a href="#portafolio">Portafolio</a>
                    <a href="#blog">Blog Técnico</a>
                    <a href="#sobre-mi">Sobre Mí</a>
                    <a href="#testimonios">Testimonios</a>
                    <a href="#faq">Preguntas Frecuentes</a>
                    <a href="#contacto">Contacto</a>
                </div>
                <div class="footer-col">
                    <h4>Contacto Directo</h4>
                    <p> +58 424-706-7782</p>
                    <p>📱 +58 424-741-3224</p>
                    <p>✉️ noelakula05@gmail.com</p>
                    <p>️ noeldg2002@yahoo.es</p>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2026 Ing. Noel Daudinot G. Todos los derechos reservados.</p>
                <p style="margin-top: 10px;">
                    <a href="#" onclick="alert('Política de Privacidad: Sus datos personales serán tratados con confidencialidad y utilizados únicamente para responder a su solicitud de servicio.'); return false;">Política de Privacidad</a> | 
                    <a href="#" onclick="alert('Términos y Condiciones del servicio técnico.'); return false;">Términos y Condiciones</a>
                </p>
            </div>
        </div>
    </footer>

    <!-- BOTÓN FLOTANTE WHATSAPP -->
    <a href="https://wa.me/584247067782?text=Hola%20Ing.%20Noel,%20necesito%20información%20sobre%20sus%20servicios%20técnicos" class="whatsapp-float" target="_blank" rel="noopener noreferrer" aria-label="Contactar por WhatsApp">
        <svg width="32" height="32" viewBox="0 0 24 24" fill="currentColor">
            <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413Z"/>
        </svg>
    </a>

    <!-- JAVASCRIPT -->
    <script>
        document.addEventListener('DOMContentLoaded', () => {
            // 1. HEADER SCROLL EFFECT
            const header = document.getElementById('main-header');
            window.addEventListener('scroll', () => {
                if (window.scrollY > 50) {
                    header.classList.add('scrolled');
                } else {
                    header.classList.remove('scrolled');
                }
            });

            // 2. MOBILE MENU
            const hamburger = document.getElementById('hamburger');
            const mobileMenu = document.getElementById('mobileMenu');
            const closeMenu = document.getElementById('closeMenu');
            const mobileLinks = document.querySelectorAll('.mobile-link');

            hamburger.addEventListener('click', () => mobileMenu.classList.add('active'));
            closeMenu.addEventListener('click', () => mobileMenu.classList.remove('active'));
            mobileLinks.forEach(link => {
                link.addEventListener('click', () => mobileMenu.classList.remove('active'));
            });

            // 3. FAQ ACCORDION
            const faqQuestions = document.querySelectorAll('.faq-question');
            faqQuestions.forEach(question => {
                question.addEventListener('click', () => {
                    const item = question.parentElement;
                    const isActive = item.classList.contains('active');
                    
                    document.querySelectorAll('.faq-item').forEach(faq => {
                        faq.classList.remove('active');
                    });

                    if (!isActive) {
                        item.classList.add('active');
                    }
                });
            });

            // 4. FORM VALIDATION (EMAIL)
            const form = document.getElementById('contactForm');
            const emailInput = document.getElementById('email');
            const formSuccess = document.getElementById('formSuccess');
            const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;

            emailInput.addEventListener('input', () => {
                if (emailInput.parentElement.classList.contains('error')) {
                    if (emailRegex.test(emailInput.value.trim())) {
                        emailInput.parentElement.classList.remove('error');
                    }
                }
            });

            form.addEventListener('submit', (e) => {
                e.preventDefault();
                let isValid = true;
                
                // Validar email
                const emailValue = emailInput.value.trim();
                if (!emailRegex.test(emailValue)) {
                    emailInput.parentElement.classList.add('error');
                    isValid = false;
                } else {
                    emailInput.parentElement.classList.remove('error');
                }

                // Validar campos requeridos
                const required = form.querySelectorAll('[required]');
                required.forEach(field => {
                    if (!field.value.trim()) {
                        isValid = false;
                        field.style.borderColor = 'var(--error)';
                    } else {
                        field.style.borderColor = '';
                    }
                });

                if (isValid) {
                    // Construir mensaje de WhatsApp con los datos del formulario
                    const nombre = document.getElementById('nombre').value;
                    const telefono = document.getElementById('telefono').value;
                    const servicio = document.getElementById('servicio').value;
                    const mensaje = document.getElementById('mensaje').value;
                    
                    const whatsappMsg = `Hola Ing. Noel, soy *${nombre}*.%0A%0A` +
                                       `📧 Email: ${emailValue}%0A` +
                                       `📱 Tel: ${telefono}%0A` +
                                       `🔧 Servicio: ${servicio}%0A%0A` +
                                       `📝 Detalle: ${mensaje}`;
                    
                    // Mostrar mensaje de éxito
                    formSuccess.style.display = 'block';
                    
                    // Redirigir a WhatsApp después de 1.5 segundos
                    setTimeout(() => {
                        window.open(`https://wa.me/584247067782?text=${whatsappMsg}`, '_blank');
                        form.reset();
                        formSuccess.style.display = 'none';
                    }, 1500);
                }
            });

            // 5. SMOOTH SCROLL PARA ENLACES INTERNOS
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function (e) {
                    const targetId = this.getAttribute('href');
                    if (targetId === '#') return;
                    
                    const targetElement = document.querySelector(targetId);
                    if (targetElement) {
                        e.preventDefault();
                        const headerOffset = 80;
                        const elementPosition = targetElement.getBoundingClientRect().top;
                        const offsetPosition = elementPosition + window.pageYOffset - headerOffset;
        
                        window.scrollTo({
                            top: offsetPosition,
                            behavior: 'smooth'
                        });
                    }
                });
            });
        });
    </script>
</body>
</html>
