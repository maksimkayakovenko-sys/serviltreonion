<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>АвтоСервисы Воронежа — каталог СТО с ценами и отзывами</title>
  <meta name="description" content="Каталог автосервисов Воронежа: адреса, телефоны, цены на услуги, отзывы.">

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700;800&display=swap" rel="stylesheet">

  <style>
    :root {
      --bg-body: #f4f6fb;
      --bg-card: #ffffff;
      --text-primary: #0f172a;
      --text-secondary: #475569;
      --text-muted: #94a3b8;
      --border-color: #e2e8f0;
      --accent-primary: #3b82f6;
      --accent-gradient: linear-gradient(135deg, #2563eb 0%, #4f46e5 100%);
      --accent-glow: rgba(37, 99, 235, 0.25);
      --status-green: #10b981;
      --status-green-bg: #ecfdf5;
      --shadow-sm: 0 4px 12px rgba(15, 23, 42, 0.03);
      --shadow-md: 0 12px 28px rgba(15, 23, 42, 0.06);
      --radius-pill: 999px;
      --radius-card: 20px;
      --radius-input: 12px;
      --font-main: 'Montserrat', -apple-system, sans-serif;
    }

    * { box-sizing: border-box; margin: 0; padding: 0; font-family: var(--font-main); }
    body { background-color: var(--bg-body); color: var(--text-primary); line-height: 1.5; -webkit-font-smoothing: antialiased; }

    /* ===== ШАПКА ===== */
    .header {
      background: rgba(255, 255, 255, 0.9);
      backdrop-filter: blur(16px);
      -webkit-backdrop-filter: blur(16px);
      position: sticky;
      top: 0;
      z-index: 1000;
      border-bottom: 1px solid var(--border-color);
    }
    .header-container {
      max-width: 1240px;
      margin: 0 auto;
      padding: 14px 24px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 16px;
      position: relative;
    }
    .logo { display: flex; align-items: center; gap: 10px; text-decoration: none; color: var(--text-primary); min-width: 0; }
    .logo-icon {
      width: 38px; height: 38px;
      background: var(--accent-gradient);
      border-radius: 10px;
      display: flex; align-items: center; justify-content: center;
      color: #fff; font-weight: 800; font-size: 1rem;
      box-shadow: 0 4px 12px var(--accent-glow);
      flex-shrink: 0;
    }
    .logo-text { display: flex; flex-direction: column; line-height: 1.15; min-width: 0; }
    .logo-name { font-weight: 800; font-size: 1.05rem; letter-spacing: -0.3px; color: var(--text-primary); white-space: nowrap; }
    .logo-tagline { font-size: 0.68rem; font-weight: 500; color: var(--text-muted); margin-top: 1px; white-space: nowrap; }

    .nav { display: flex; gap: 8px; align-items: center; }
    .nav-link { color: var(--text-secondary); text-decoration: none; font-size: 0.85rem; font-weight: 600; padding: 8px 14px; border-radius: var(--radius-pill); transition: all 0.2s; white-space: nowrap; }
    .nav-link:hover { color: var(--text-primary); background: #e2e8f0; }
    .nav-link.nav-accent { background: var(--accent-gradient); color: #fff; box-shadow: 0 4px 12px var(--accent-glow); }

    .menu-toggle {
      display: none;
      width: 40px; height: 40px;
      background: #f1f5f9;
      border: 1px solid var(--border-color);
      border-radius: 10px;
      cursor: pointer;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      gap: 4px;
      padding: 0;
      flex-shrink: 0;
    }
    .menu-toggle span { display: block; width: 18px; height: 2px; background: var(--text-primary); border-radius: 2px; transition: all 0.25s; }
    .menu-toggle.active span:nth-child(1) { transform: translateY(6px) rotate(45deg); }
    .menu-toggle.active span:nth-child(2) { opacity: 0; }
    .menu-toggle.active span:nth-child(3) { transform: translateY(-6px) rotate(-45deg); }

    /* ===== HERO ===== */
    .hero {
      background: var(--accent-gradient);
      color: #fff;
      padding: 48px 24px 56px;
      position: relative;
      overflow: hidden;
    }
    .hero::before {
      content: "";
      position: absolute;
      top: -30%;
      right: -10%;
      width: 500px;
      height: 500px;
      background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
      pointer-events: none;
    }
    .hero-inner {
      max-width: 1240px;
      margin: 0 auto;
      position: relative;
      z-index: 1;
    }
    .hero-title {
      font-size: 2.2rem;
      font-weight: 800;
      letter-spacing: -0.8px;
      line-height: 1.2;
      margin-bottom: 12px;
      max-width: 720px;
    }
    .hero-subtitle {
      font-size: 1rem;
      color: rgba(255, 255, 255, 0.9);
      max-width: 620px;
      margin-bottom: 28px;
      font-weight: 500;
    }

    .search-box {
      background: #fff;
      border-radius: var(--radius-card);
      padding: 10px;
      display: flex;
      gap: 10px;
      box-shadow: 0 20px 40px rgba(0,0,0,0.15);
      max-width: 900px;
      flex-wrap: wrap;
      position: relative;
    }
    .search-field {
      flex: 1;
      min-width: 200px;
      position: relative;
    }
    .search-field input {
      width: 100%;
      padding: 14px 16px 14px 44px;
      border: none;
      border-radius: 12px;
      font-size: 0.95rem;
      font-weight: 500;
      outline: none;
      background: #f8fafc;
      color: var(--text-primary);
      font-family: var(--font-main);
    }
    .search-field::before {
      content: "🔍";
      position: absolute;
      left: 16px;
      top: 50%;
      transform: translateY(-50%);
      font-size: 0.95rem;
      opacity: 0.5;
      pointer-events: none;
    }
    .search-field input:focus { background: #fff; box-shadow: 0 0 0 2px var(--accent-primary) inset; }
    .search-btn {
      background: #0f172a;
      color: #fff;
      border: none;
      padding: 14px 28px;
      border-radius: 12px;
      font-size: 0.9rem;
      font-weight: 700;
      cursor: pointer;
      font-family: var(--font-main);
      transition: all 0.2s;
      white-space: nowrap;
      flex-shrink: 0;
    }
    .search-btn:hover { background: #1e293b; }

    /* ===== КОНТЕЙНЕР ===== */
    .container {
      max-width: 1240px;
      margin: 0 auto;
      padding: 32px 24px 60px;
    }

    /* ===== ФИЛЬТРЫ ===== */
    .filters-bar {
      background: var(--bg-card);
      border-radius: var(--radius-card);
      padding: 20px 24px;
      box-shadow: var(--shadow-sm);
      border: 1px solid var(--border-color);
      margin-bottom: 24px;
    }
    .filters-title {
      font-size: 0.75rem;
      font-weight: 700;
      color: var(--text-muted);
      text-transform: uppercase;
      letter-spacing: 0.8px;
      margin-bottom: 12px;
      display: flex;
      align-items: center;
      gap: 8px;
    }
    .filters-title::before {
      content: "";
      width: 4px;
      height: 14px;
      background: var(--accent-gradient);
      border-radius: 2px;
    }
    .filters-chips {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-bottom: 16px;
    }
    .chip {
      display: inline-flex;
      align-items: center;
      gap: 6px;
      padding: 8px 16px;
      background: #fff;
      border: 1px solid var(--border-color);
      border-radius: var(--radius-pill);
      font-size: 0.82rem;
      font-weight: 600;
      color: var(--text-secondary);
      cursor: pointer;
      transition: all 0.2s;
      white-space: nowrap;
      font-family: var(--font-main);
    }
    .chip:hover { border-color: var(--accent-primary); color: var(--accent-primary); background: #eff6ff; }
    .chip.active { background: var(--accent-gradient); color: #fff; border-color: transparent; box-shadow: 0 4px 12px var(--accent-glow); }
    .chip-count {
      font-size: 0.7rem;
      opacity: 0.7;
      font-weight: 700;
    }
    .chip.active .chip-count { opacity: 0.9; }

    .filters-selects {
      display: grid;
      grid-template-columns: 1fr 1fr 1fr 1fr;
      gap: 10px;
    }
    .filters-selects select {
      padding: 11px 14px;
      border: 1px solid var(--border-color);
      border-radius: 10px;
      font-size: 0.85rem;
      font-weight: 500;
      font-family: var(--font-main);
      outline: none;
      background: #fff;
      color: var(--text-primary);
      cursor: pointer;
      appearance: none;
      background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='12' height='12' viewBox='0 0 12 12'%3E%3Cpath fill='%2364748b' d='M6 8L2 4h8z'/%3E%3C/svg%3E");
      background-repeat: no-repeat;
      background-position: right 14px center;
      padding-right: 36px;
    }
    .filters-selects select:focus { border-color: var(--accent-primary); box-shadow: 0 0 0 3px rgba(59, 130, 246, 0.15); }

    /* ===== РЕЗУЛЬТАТЫ ===== */
    .results-bar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 16px;
      margin-bottom: 20px;
      flex-wrap: wrap;
    }
    .results-count {
      font-size: 0.9rem;
      color: var(--text-secondary);
      font-weight: 600;
    }
    .results-count strong { color: var(--text-primary); font-weight: 800; }
    .view-toggle {
      display: flex;
      gap: 4px;
      background: #fff;
      padding: 4px;
      border-radius: 12px;
      border: 1px solid var(--border-color);
    }
    .view-btn {
      padding: 8px 16px;
      border: none;
      background: transparent;
      font-size: 0.82rem;
      font-weight: 600;
      color: var(--text-secondary);
      cursor: pointer;
      border-radius: 8px;
      transition: all 0.2s;
      font-family: var(--font-main);
      display: flex;
      align-items: center;
      gap: 6px;
    }
    .view-btn.active { background: var(--accent-gradient); color: #fff; }

    /* ===== СПИСОК СТО ===== */
    .sto-list {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 16px;
    }

    .sto-card {
      background: var(--bg-card);
      border: 1px solid var(--border-color);
      border-radius: var(--radius-card);
      transition: all 0.25s;
      display: flex;
      flex-direction: column;
      overflow: hidden;
      position: relative;
    }
    .sto-card:hover {
      border-color: var(--accent-primary);
      box-shadow: var(--shadow-md);
      transform: translateY(-2px);
    }

    /* ===== ГАЛЕРЕЯ ФОТО (3 фото в ряд) ===== */
    .sto-gallery-row {
      display: grid;
      grid-template-columns: 2fr 1fr 1fr;
      grid-template-rows: 180px;
      gap: 4px;
      position: relative;
      background: #f1f5f9;
      overflow: hidden;
    }

    .sto-photo {
      position: relative;
      overflow: hidden;
      display: flex;
      align-items: center;
      justify-content: center;
      cursor: pointer;
      transition: transform 0.3s;
    }
    .sto-photo:hover {
      transform: scale(1.03);
    }
    .sto-photo::before {
      content: "";
      position: absolute;
      inset: 0;
      background: radial-gradient(circle at 30% 30%, rgba(255,255,255,0.2) 0%, transparent 60%);
      pointer-events: none;
    }
    .sto-photo-icon {
      font-size: 2.5rem;
      position: relative;
      z-index: 1;
      filter: drop-shadow(0 4px 12px rgba(0,0,0,0.25));
    }
    .sto-photo.main .sto-photo-icon { font-size: 3.2rem; }

    /* Цвета для фото */
    .photo-blue { background: linear-gradient(135deg, #1e40af 0%, #3b82f6 100%); }
    .photo-red { background: linear-gradient(135deg, #dc2626 0%, #f97316 100%); }
    .photo-dark { background: linear-gradient(135deg, #0f172a 0%, #475569 100%); }
    .photo-green { background: linear-gradient(135deg, #059669 0%, #10b981 100%); }
    .photo-yellow { background: linear-gradient(135deg, #f59e0b 0%, #fbbf24 100%); }
    .photo-purple { background: linear-gradient(135deg, #7c3aed 0%, #a855f7 100%); }
    .photo-cyan { background: linear-gradient(135deg, #0891b2 0%, #06b6d4 100%); }
    .photo-pink { background: linear-gradient(135deg, #db2777 0%, #ec4899 100%); }

    /* Бейджи поверх галереи */
    .sto-cover-badges {
      position: absolute;
      top: 12px;
      left: 12px;
      display: flex;
      gap: 6px;
      flex-wrap: wrap;
      z-index: 5;
    }
    .badge {
      display: inline-flex;
      align-items: center;
      gap: 4px;
      font-size: 0.65rem;
      font-weight: 700;
      padding: 4px 10px;
      border-radius: 6px;
      white-space: nowrap;
      backdrop-filter: blur(10px);
      border: 1px solid rgba(255,255,255,0.3);
    }
    .badge-verified { background: rgba(16, 185, 129, 0.95); color: #fff; }
    .badge-top { background: rgba(251, 191, 36, 0.95); color: #78350f; }
    .badge-new { background: rgba(59, 130, 246, 0.95); color: #fff; }

    /* Счётчик фото */
    .sto-photo-count {
      position: absolute;
      bottom: 12px;
      right: 12px;
      background: rgba(15, 23, 42, 0.85);
      color: #fff;
      font-size: 0.7rem;
      font-weight: 700;
      padding: 5px 10px;
      border-radius: 8px;
      backdrop-filter: blur(10px);
      z-index: 5;
      display: flex;
      align-items: center;
      gap: 4px;
    }

    /* Контент карточки */
    .sto-content {
      padding: 18px 20px 20px;
      display: flex;
      flex-direction: column;
      gap: 12px;
      flex: 1;
    }

    .sto-name {
      font-size: 1.05rem;
      font-weight: 800;
      color: var(--text-primary);
      letter-spacing: -0.3px;
      line-height: 1.3;
    }
    .sto-type {
      font-size: 0.78rem;
      color: var(--text-secondary);
      font-weight: 500;
      margin-top: 2px;
    }
    .sto-rating {
      display: flex;
      align-items: center;
      gap: 6px;
      font-size: 0.8rem;
      margin-top: 4px;
    }
    .sto-stars { color: #fbbf24; letter-spacing: 1px; font-size: 0.85rem; }
    .sto-rating-num { font-weight: 800; color: var(--text-primary); }
    .sto-reviews { color: var(--text-muted); font-size: 0.75rem; }

    .sto-address {
      display: flex;
      align-items: flex-start;
      gap: 8px;
      font-size: 0.82rem;
      color: var(--text-secondary);
      line-height: 1.4;
    }
    .sto-address-icon {
      font-size: 0.9rem;
      flex-shrink: 0;
      margin-top: 1px;
    }
    .sto-address strong { color: var(--text-primary); font-weight: 600; }

    .sto-services {
      display: flex;
      flex-wrap: wrap;
      gap: 5px;
      padding-top: 12px;
      border-top: 1px solid var(--border-color);
    }
    .service-tag {
      font-size: 0.7rem;
      font-weight: 600;
      padding: 3px 9px;
      background: #f1f5f9;
      color: var(--text-secondary);
      border-radius: 6px;
      white-space: nowrap;
    }
    .service-tag.more {
      background: #eff6ff;
      color: var(--accent-primary);
    }

    .sto-footer {
      display: flex;
      gap: 8px;
      align-items: center;
      padding-top: 12px;
      border-top: 1px solid var(--border-color);
      margin-top: auto;
    }
    .btn-call {
      flex: 1;
      padding: 11px 16px;
      background: var(--accent-gradient);
      color: #fff;
      border: none;
      border-radius: 10px;
      font-size: 0.85rem;
      font-weight: 700;
      cursor: pointer;
      transition: all 0.2s;
      font-family: var(--font-main);
      white-space: nowrap;
    }
    .btn-call:hover { opacity: 0.95; transform: translateY(-1px); box-shadow: 0 6px 16px var(--accent-glow); }
    .btn-map {
      padding: 11px 14px;
      background: #f1f5f9;
      color: var(--text-primary);
      border: 1px solid var(--border-color);
      border-radius: 10px;
      font-size: 0.85rem;
      font-weight: 600;
      cursor: pointer;
      transition: all 0.2s;
      font-family: var(--font-main);
      white-space: nowrap;
    }
    .btn-map:hover { background: #e2e8f0; }

    /* ===== CTA ДЛЯ СТО ===== */
    .cta-sto {
      max-width: 1240px;
      margin: 0 auto 60px;
      padding: 0 24px;
    }
    .cta-sto-inner {
      background: linear-gradient(135deg, #78350f 0%, #92400e 100%);
      border-radius: var(--radius-card);
      padding: 36px 40px;
      color: #fff;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 24px;
      flex-wrap: wrap;
      position: relative;
      overflow: hidden;
      box-shadow: 0 16px 40px rgba(120, 53, 15, 0.25);
    }
    .cta-sto-inner::before {
      content: "";
      position: absolute;
      top: -50%;
      right: -5%;
      width: 400px;
      height: 400px;
      background: radial-gradient(circle, rgba(251, 191, 36, 0.25) 0%, transparent 70%);
      pointer-events: none;
    }
    .cta-sto-left {
      display: flex;
      align-items: center;
      gap: 20px;
      position: relative;
      z-index: 1;
      flex: 1;
      min-width: 280px;
    }
    .cta-sto-icon {
      width: 64px;
      height: 64px;
      background: rgba(255,255,255,0.15);
      backdrop-filter: blur(10px);
      border: 1px solid rgba(255,255,255,0.25);
      border-radius: 16px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.8rem;
      flex-shrink: 0;
    }
    .cta-sto-title { font-size: 1.3rem; font-weight: 800; margin-bottom: 6px; letter-spacing: -0.3px; }
    .cta-sto-text { font-size: 0.88rem; color: rgba(255,255,255,0.85); line-height: 1.5; }
    .cta-sto-btn {
      padding: 14px 28px;
      background: #fbbf24;
      color: #78350f;
      border: none;
      border-radius: 14px;
      font-size: 0.9rem;
      font-weight: 800;
      cursor: pointer;
      text-decoration: none;
      white-space: nowrap;
      transition: all 0.2s;
      box-shadow: 0 8px 20px rgba(0,0,0,0.2);
      position: relative;
      z-index: 1;
      flex-shrink: 0;
    }
    .cta-sto-btn:hover { background: #fde68a; transform: translateY(-2px); }

    /* ===== ТАРИФЫ ===== */
    .pricing-section {
      max-width: 1240px;
      margin: 0 auto 60px;
      padding: 0 24px;
    }
    .pricing-title {
      font-size: 1.6rem;
      font-weight: 800;
      text-align: center;
      letter-spacing: -0.5px;
      margin-bottom: 6px;
    }
    .pricing-sub {
      font-size: 0.9rem;
      color: var(--text-secondary);
      text-align: center;
      margin-bottom: 32px;
      font-weight: 500;
    }
    .pricing-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 20px;
      max-width: 880px;
      margin: 0 auto;
    }
    .pricing-card {
      background: var(--bg-card);
      border: 1px solid var(--border-color);
      border-radius: var(--radius-card);
      padding: 32px 28px;
      box-shadow: var(--shadow-sm);
      transition: all 0.25s;
      position: relative;
      display: flex;
      flex-direction: column;
    }
    .pricing-card:hover { transform: translateY(-4px); box-shadow: var(--shadow-md); border-color: #cbd5e1; }
    .pricing-card.featured { border: 2px solid #4f46e5; box-shadow: 0 16px 40px rgba(79, 70, 229, 0.15); }
    .pricing-card.featured::before {
      content: "Выбирают чаще";
      position: absolute;
      top: 16px;
      right: 16px;
      background: var(--accent-gradient);
      color: #fff;
      padding: 5px 12px;
      border-radius: var(--radius-pill);
      font-size: 0.68rem;
      font-weight: 800;
      text-transform: uppercase;
    }
    .pricing-tag {
      display: inline-block;
      background: #f1f5f9;
      color: var(--text-secondary);
      font-size: 0.72rem;
      font-weight: 700;
      padding: 4px 10px;
      border-radius: 6px;
      margin-bottom: 14px;
      text-transform: uppercase;
      align-self: flex-start;
    }
    .pricing-title-card { font-size: 1.15rem; font-weight: 800; margin-bottom: 6px; letter-spacing: -0.3px; }
    .pricing-desc { font-size: 0.82rem; color: var(--text-secondary); margin-bottom: 20px; font-weight: 500; }
    .pricing-price { font-size: 2rem; font-weight: 800; letter-spacing: -1px; line-height: 1; margin-bottom: 4px; }
    .pricing-price span { font-size: 0.85rem; font-weight: 600; color: var(--text-muted); }
    .pricing-note { font-size: 0.75rem; color: var(--text-muted); margin-bottom: 20px; font-weight: 500; }
    .pricing-features { list-style: none; margin-bottom: 24px; padding-top: 20px; border-top: 1px solid var(--border-color); flex: 1; }
    .pricing-features li {
      font-size: 0.83rem;
      color: var(--text-secondary);
      padding: 6px 0;
      display: flex;
      align-items: flex-start;
      gap: 10px;
      line-height: 1.5;
    }
    .pricing-features li::before { content: "✓"; color: var(--status-green); font-weight: 800; flex-shrink: 0; }
    .pricing-btn {
      width: 100%;
      padding: 13px 20px;
      border-radius: 12px;
      font-size: 0.88rem;
      font-weight: 700;
      cursor: pointer;
      text-decoration: none;
      display: block;
      text-align: center;
      border: none;
      font-family: var(--font-main);
      transition: all 0.2s;
    }
    .pricing-btn.outline { background: #fff; color: var(--text-primary); border: 2px solid var(--border-color); }
    .pricing-btn.outline:hover { border-color: var(--accent-primary); color: var(--accent-primary); }
    .pricing-btn.primary { background: var(--accent-gradient); color: #fff; box-shadow: 0 6px 16px var(--accent-glow); }

    /* ===== ФУТЕР ===== */
    .footer { background: #fff; padding: 48px 24px 28px; border-top: 1px solid var(--border-color); font-size: 0.8rem; color: var(--text-secondary); }
    .footer-inner { max-width: 1240px; margin: 0 auto; display: grid; grid-template-columns: 2fr 1fr 1fr 1fr; gap: 32px; margin-bottom: 28px; }
    .footer-heading { color: var(--text-primary); font-weight: 700; font-size: 0.85rem; margin-bottom: 14px; }
    .footer-ul { list-style: none; }
    .footer-ul li { margin-bottom: 8px; }
    .footer-ul a { color: var(--text-secondary); text-decoration: none; transition: color 0.2s; }
    .footer-ul a:hover { color: var(--accent-primary); }
    .footer-copy { max-width: 1240px; margin: 0 auto; border-top: 1px solid var(--border-color); padding-top: 20px; text-align: center; font-size: 0.75rem; color: var(--text-muted); }

    /* ===== АДАПТИВ ===== */
    @media (max-width: 1024px) {
      .sto-list { grid-template-columns: 1fr; }
      .filters-selects { grid-template-columns: 1fr 1fr; }
      .footer-inner { grid-template-columns: 1fr 1fr; gap: 24px; }
    }

    @media (max-width: 900px) {
      .header-container { padding: 12px 14px; }
      .logo-tagline { display: none; }
      .logo-name { font-size: 0.92rem; }
      .logo-icon { width: 34px; height: 34px; font-size: 0.9rem; }
      .menu-toggle { display: flex; }

      .nav {
        position: absolute;
        top: 100%;
        left: 0;
        right: 0;
        background: #fff;
        flex-direction: column;
        align-items: stretch;
        gap: 0;
        padding: 8px 14px 14px;
        box-shadow: 0 8px 24px rgba(0,0,0,0.1);
        border-top: 1px solid var(--border-color);
        transform: translateY(-10px);
        opacity: 0;
        visibility: hidden;
        transition: all 0.25s;
        z-index: 999;
      }
      .nav.open { transform: translateY(0); opacity: 1; visibility: visible; }
      .nav-link { padding: 12px 14px; border-radius: 8px; text-align: center; }
    }

    @media (max-width: 640px) {
      .hero { padding: 32px 16px 40px; }
      .hero-title { font-size: 1.5rem; }
      .hero-subtitle { font-size: 0.9rem; margin-bottom: 20px; }
      .search-box { padding: 8px; }
      .search-field input { padding: 13px 14px 13px 42px; font-size: 0.9rem; }
      .search-btn { width: 100%; padding: 13px; }

      .container { padding: 20px 16px 40px; }

      .filters-bar { padding: 16px; }
      .filters-selects { grid-template-columns: 1fr; gap: 8px; }

      .results-bar { flex-direction: column; align-items: stretch; gap: 10px; }
      .view-toggle { align-self: flex-start; }

      /* На мобильном — 2 фото сверху и 1 снизу */
      .sto-gallery-row {
        grid-template-columns: 1fr 1fr;
        grid-template-rows: 120px 120px;
      }
      .sto-gallery-row .sto-photo.main {
        grid-column: 1 / -1;
      }
      .sto-photo-icon { font-size: 2rem; }
      .sto-photo.main .sto-photo-icon { font-size: 2.6rem; }

      .sto-content { padding: 16px; }
      .sto-name { font-size: 0.98rem; }
      .sto-footer { flex-direction: column; gap: 8px; }
      .btn-call, .btn-map { width: 100%; }

      .cta-sto { padding: 0 16px; margin-bottom: 40px; }
      .cta-sto-inner { padding: 24px 20px; flex-direction: column; align-items: stretch; gap: 18px; }
      .cta-sto-left { flex-direction: row; align-items: flex-start; }
      .cta-sto-icon { width: 48px; height: 48px; font-size: 1.3rem; }
      .cta-sto-title { font-size: 1.1rem; }
      .cta-sto-btn { width: 100%; text-align: center; }

      .pricing-section { padding: 0 16px; margin-bottom: 40px; }
      .pricing-title { font-size: 1.3rem; }
      .pricing-grid { grid-template-columns: 1fr; }
      .pricing-card { padding: 24px 20px; }
      .pricing-price { font-size: 1.6rem; }

      .footer { padding: 32px 16px 20px; }
      .footer-inner { grid-template-columns: 1fr; gap: 24px; }
    }
  </style>
</head>
<body>

  <!-- ШАПКА -->
  <header class="header">
    <div class="header-container">
      <a href="#" class="logo">
        <div class="logo-icon">АС</div>
        <div class="logo-text">
          <span class="logo-name">АвтоСервисы Воронежа</span>
          <span class="logo-tagline">Каталог СТО с ценами и отзывами</span>
        </div>
      </a>

      <button class="menu-toggle" id="menuToggle" aria-label="Меню">
        <span></span><span></span><span></span>
      </button>

      <nav class="nav" id="headerNav">
        <a href="#catalog" class="nav-link">Каталог СТО</a>
        <a href="#pricing" class="nav-link">СТО — размещение</a>
        <a href="#pricing" class="nav-link nav-accent">Добавить сервис</a>
      </nav>
    </div>
  </header>

  <!-- HERO -->
  <section class="hero">
    <div class="hero-inner">
      <h1 class="hero-title">Найдите автосервис в Воронеже</h1>
      <p class="hero-subtitle">Проверенные СТО с ценами, отзывами и адресами. Ищите по району, марке авто и типу ремонта.</p>

      <div class="search-box">
        <div class="search-field">
          <input type="text" id="searchInput" placeholder="Название СТО, услуга или адрес...">
        </div>
        <button class="search-btn" id="searchBtn">Найти</button>
      </div>
    </div>
  </section>

  <div class="container" id="catalog">

    <!-- ФИЛЬТРЫ -->
    <div class="filters-bar">
      <div class="filters-title">Районы Воронежа</div>
      <div class="filters-chips" id="districtsChips">
        <button class="chip active" data-district="all">Все районы <span class="chip-count">48</span></button>
        <button class="chip" data-district="leninsky">Ленинский <span class="chip-count">8</span></button>
        <button class="chip" data-district="central">Центральный <span class="chip-count">11</span></button>
        <button class="chip" data-district="kominter">Коминтерновский <span class="chip-count">12</span></button>
        <button class="chip" data-district="sovetsky">Советский <span class="chip-count">7</span></button>
        <button class="chip" data-district="zheleznodor">Железнодорожный <span class="chip-count">5</span></button>
        <button class="chip" data-district="levoberezh">Левобережный <span class="chip-count">5</span></button>
      </div>

      <div class="filters-title" style="margin-top: 8px;">Параметры</div>
      <div class="filters-selects">
        <select id="serviceFilter">
          <option value="">Все услуги</option>
          <option value="to">ТО и обслуживание</option>
          <option value="body">Кузовной ремонт</option>
          <option value="diagnostics">Диагностика</option>
          <option value="tires">Шиномонтаж</option>
          <option value="engine">Ремонт двигателя</option>
          <option value="transmission">Ремонт АКПП/МКПП</option>
        </select>
        <select id="brandFilter">
          <option value="">Все марки</option>
          <option value="universal">Универсальные</option>
          <option value="german">Немецкие (BMW, Audi, VW)</option>
          <option value="korean">Корейские (Kia, Hyundai)</option>
          <option value="japanese">Японские (Toyota, Nissan)</option>
          <option value="russian">Российские (Lada, ГАЗ)</option>
        </select>
        <select id="priceFilter">
          <option value="">Любые цены</option>
          <option value="low">₽ — бюджетные</option>
          <option value="mid">₽₽ — средние</option>
          <option value="high">₽₽₽ — премиум</option>
        </select>
        <select id="ratingFilter">
          <option value="">Любой рейтинг</option>
          <option value="4.5">4.5+ звёзд</option>
          <option value="4.0">4.0+ звёзд</option>
          <option value="3.5">3.5+ звёзд</option>
        </select>
      </div>
    </div>

    <!-- РЕЗУЛЬТАТЫ -->
    <div class="results-bar">
      <div class="results-count">Найдено: <strong id="resultsCount">48</strong> автосервисов</div>
      <div class="view-toggle">
        <button class="view-btn active" data-view="grid">☰ Список</button>
        <button class="view-btn" data-view="map">🗺 Карта</button>
      </div>
    </div>

    <!-- СПИСОК СТО -->
    <div class="sto-list" id="stoList">

      <!-- СТО 1 -->
      <div class="sto-card" data-district="leninsky" data-service="to,diagnostics" data-brand="german,korean" data-price="mid" data-rating="4.8">
        <div class="sto-gallery-row">
          <div class="sto-photo main photo-blue">
            <div class="sto-photo-icon">🔧</div>
          </div>
          <div class="sto-photo photo-dark">
            <div class="sto-photo-icon">⚙️</div>
          </div>
          <div class="sto-photo photo-cyan">
            <div class="sto-photo-icon">🛠</div>
          </div>

          <div class="sto-cover-badges">
            <span class="badge badge-verified">✓ Проверено</span>
            <span class="badge badge-top">★ Топ</span>
          </div>

          <div class="sto-photo-count">
            📷 8 фото
          </div>
        </div>
        <div class="sto-content">
          <div>
            <div class="sto-name">АвтоТехЦентр на Ленинском</div>
            <div class="sto-type">СТО полного цикла · 12 лет на рынке</div>
            <div class="sto-rating">
              <span class="sto-stars">★★★★★</span>
              <span class="sto-rating-num">4.8</span>
              <span class="sto-reviews">· 127 отзывов</span>
            </div>
          </div>

          <div class="sto-address">
            <span class="sto-address-icon">📍</span>
            <span><strong>ул. Ленинский проспект, 174</strong> · Ленинский район</span>
          </div>

          <div class="sto-services">
            <span class="service-tag">ТО</span>
            <span class="service-tag">Диагностика</span>
            <span class="service-tag">Ремонт двигателя</span>
            <span class="service-tag more">+4 услуги</span>
          </div>

          <div class="sto-footer">
            <button class="btn-call">📞 Позвонить</button>
            <button class="btn-map">🗺 На карте</button>
          </div>
        </div>
      </div>

      <!-- СТО 2 -->
      <div class="sto-card" data-district="central" data-service="body" data-brand="universal" data-price="high" data-rating="4.9">
        <div class="sto-gallery-row">
          <div class="sto-photo main photo-red">
            <div class="sto-photo-icon">🚗</div>
          </div>
          <div class="sto-photo photo-yellow">
            <div class="sto-photo-icon">🎨</div>
          </div>
          <div class="sto-photo photo-pink">
            <div class="sto-photo-icon">🖌</div>
          </div>

          <div class="sto-cover-badges">
            <span class="badge badge-verified">✓ Проверено</span>
            <span class="badge badge-top">★ Топ</span>
          </div>

          <div class="sto-photo-count">
            📷 12 фото
          </div>
        </div>
        <div class="sto-content">
          <div>
            <div class="sto-name">Кузовной центр «Мастер»</div>
            <div class="sto-type">Кузовной ремонт · Работа с ОСАГО</div>
            <div class="sto-rating">
              <span class="sto-stars">★★★★★</span>
              <span class="sto-rating-num">4.9</span>
              <span class="sto-reviews">· 89 отзывов</span>
            </div>
          </div>

          <div class="sto-address">
            <span class="sto-address-icon">📍</span>
            <span><strong>ул. Кольцовская, 24</strong> · Центральный район</span>
          </div>

          <div class="sto-services">
            <span class="service-tag">Кузовной ремонт</span>
            <span class="service-tag">Покраска</span>
            <span class="service-tag">ОСАГО</span>
            <span class="service-tag more">+3 услуги</span>
          </div>

          <div class="sto-footer">
            <button class="btn-call">📞 Позвонить</button>
            <button class="btn-map">🗺 На карте</button>
          </div>
        </div>
      </div>

      <!-- СТО 3 -->
      <div class="sto-card" data-district="kominter" data-service="diagnostics,transmission" data-brand="german" data-price="high" data-rating="4.7">
        <div class="sto-gallery-row">
          <div class="sto-photo main photo-dark">
            <div class="sto-photo-icon">⚙️</div>
          </div>
          <div class="sto-photo photo-blue">
            <div class="sto-photo-icon">🔩</div>
          </div>
          <div class="sto-photo photo-cyan">
            <div class="sto-photo-icon">🔧</div>
          </div>

          <div class="sto-cover-badges">
            <span class="badge badge-verified">✓ Проверено</span>
          </div>

          <div class="sto-photo-count">
            📷 9 фото
          </div>
        </div>
        <div class="sto-content">
          <div>
            <div class="sto-name">Немецкий АвтоСервис</div>
            <div class="sto-type">Специализация: BMW, Audi, VW</div>
            <div class="sto-rating">
              <span class="sto-stars">★★★★☆</span>
              <span class="sto-rating-num">4.7</span>
              <span class="sto-reviews">· 156 отзывов</span>
            </div>
          </div>

          <div class="sto-address">
            <span class="sto-address-icon">📍</span>
            <span><strong>Московский пр-т, 142Б</strong> · Коминтерновский район</span>
          </div>

          <div class="sto-services">
            <span class="service-tag">Диагностика</span>
            <span class="service-tag">Ремонт АКПП</span>
            <span class="service-tag">Электрика</span>
            <span class="service-tag more">+5 услуг</span>
          </div>

          <div class="sto-footer">
            <button class="btn-call">📞 Позвонить</button>
            <button class="btn-map">🗺 На карте</button>
          </div>
        </div>
      </div>

      <!-- СТО 4 -->
      <div class="sto-card" data-district="sovetsky" data-service="tires" data-brand="universal" data-price="low" data-rating="4.5">
        <div class="sto-gallery-row">
          <div class="sto-photo main photo-green">
            <div class="sto-photo-icon">🛞</div>
          </div>
          <div class="sto-photo photo-cyan">
            <div class="sto-photo-icon">🔧</div>
          </div>
          <div class="sto-photo photo-blue">
            <div class="sto-photo-icon">⚙️</div>
          </div>

          <div class="sto-cover-badges">
            <span class="badge badge-verified">✓ Проверено</span>
          </div>

          <div class="sto-photo-count">
            📷 6 фото
          </div>
        </div>
        <div class="sto-content">
          <div>
            <div class="sto-name">Шиномонтаж 24/7 на Советской</div>
            <div class="sto-type">Круглосуточный шиномонтаж</div>
            <div class="sto-rating">
              <span class="sto-stars">★★★★☆</span>
              <span class="sto-rating-num">4.5</span>
              <span class="sto-reviews">· 203 отзыва</span>
            </div>
          </div>

          <div class="sto-address">
            <span class="sto-address-icon">📍</span>
            <span><strong>ул. Космонавтов, 16</strong> · Советский район</span>
          </div>

          <div class="sto-services">
            <span class="service-tag">Шиномонтаж</span>
            <span class="service-tag">Балансировка</span>
            <span class="service-tag">Правка дисков</span>
          </div>

          <div class="sto-footer">
            <button class="btn-call">📞 Позвонить</button>
            <button class="btn-map">🗺 На карте</button>
          </div>
        </div>
      </div>

      <!-- СТО 5 -->
      <div class="sto-card" data-district="zheleznodor" data-service="to,engine" data-brand="korean,japanese" data-price="mid" data-rating="4.6">
        <div class="sto-gallery-row">
          <div class="sto-photo main photo-yellow">
            <div class="sto-photo-icon">🔩</div>
          </div>
          <div class="sto-photo photo-pink">
            <div class="sto-photo-icon">🔧</div>
          </div>
          <div class="sto-photo photo-dark">
            <div class="sto-photo-icon">⚙️</div>
          </div>

          <div class="sto-cover-badges">
            <span class="badge badge-new">Новое</span>
          </div>

          <div class="sto-photo-count">
            📷 5 фото
          </div>
        </div>
        <div class="sto-content">
          <div>
            <div class="sto-name">Азиатский АвтоСервис</div>
            <div class="sto-type">Kia, Hyundai, Toyota, Nissan</div>
            <div class="sto-rating">
              <span class="sto-stars">★★★★☆</span>
              <span class="sto-rating-num">4.6</span>
              <span class="sto-reviews">· 67 отзывов</span>
            </div>
          </div>

          <div class="sto-address">
            <span class="sto-address-icon">📍</span>
            <span><strong>ул. Дорожная, 8</strong> · Железнодорожный район</span>
          </div>

          <div class="sto-services">
            <span class="service-tag">ТО</span>
            <span class="service-tag">Ремонт двигателя</span>
            <span class="service-tag">Запчасти</span>
          </div>

          <div class="sto-footer">
            <button class="btn-call">📞 Позвонить</button>
            <button class="btn-map">🗺 На карте</button>
          </div>
        </div>
      </div>

      <!-- СТО 6 -->
      <div class="sto-card" data-district="levoberezh" data-service="to,diagnostics,engine" data-brand="russian" data-price="low" data-rating="4.4">
        <div class="sto-gallery-row">
          <div class="sto-photo main photo-purple">
            <div class="sto-photo-icon">🔧</div>
          </div>
          <div class="sto-photo photo-blue">
            <div class="sto-photo-icon">🛠</div>
          </div>
          <div class="sto-photo photo-cyan">
            <div class="sto-photo-icon">⚙️</div>
          </div>

          <div class="sto-cover-badges">
            <span class="badge badge-verified">✓ Проверено</span>
          </div>

          <div class="sto-photo-count">
            📷 10 фото
          </div>
        </div>
        <div class="sto-content">
          <div>
            <div class="sto-name">Гараж на Левом берегу</div>
            <div class="sto-type">Ремонт отечественных авто</div>
            <div class="sto-rating">
              <span class="sto-stars">★★★★☆</span>
              <span class="sto-rating-num">4.4</span>
              <span class="sto-reviews">· 112 отзывов</span>
            </div>
          </div>

          <div class="sto-address">
            <span class="sto-address-icon">📍</span>
            <span><strong>ул. Волгодонская, 2</strong> · Левобережный район</span>
          </div>

          <div class="sto-services">
            <span class="service-tag">ТО</span>
            <span class="service-tag">Диагностика</span>
            <span class="service-tag">Ремонт двигателя</span>
            <span class="service-tag more">+6 услуг</span>
          </div>

          <div class="sto-footer">
            <button class="btn-call">📞 Позвонить</button>
            <button class="btn-map">🗺 На карте</button>
          </div>
        </div>
      </div>

    </div>
  </div>

  <!-- CTA ДЛЯ СТО -->
  <div class="cta-sto">
    <div class="cta-sto-inner">
      <div class="cta-sto-left">
        <div class="cta-sto-icon">🔧</div>
        <div>
          <div class="cta-sto-title">Вы владелец автосервиса?</div>
          <div class="cta-sto-text">Разместите свой СТО в каталоге — первый месяц бесплатно. Дальше — по желанию, от 3000 ₽ в год.</div>
        </div>
      </div>
      <a href="#pricing" class="cta-sto-btn">Разместить СТО →</a>
    </div>
  </div>

  <!-- ТАРИФЫ -->
  <section class="pricing-section" id="pricing">
    <h2 class="pricing-title">Размещение для СТО</h2>
    <p class="pricing-sub">Платите только если видите смысл. Первый месяц — бесплатно.</p>

    <div class="pricing-grid">
      <div class="pricing-card">
        <span class="pricing-tag">Старт</span>
        <div class="pricing-title-card">Базовое размещение</div>
        <div class="pricing-desc">Попробовать без риска</div>
        <div class="pricing-price">0 ₽ <span>/ 1 месяц</span></div>
        <div class="pricing-note">Затем 3000 ₽ в год</div>

        <ul class="pricing-features">
          <li>Карточка СТО в каталоге Воронежа</li>
          <li>Адрес, телефон, услуги</li>
          <li>3 фото в галерее</li>
          <li>Статистика показов в кабинете</li>
          <li>Можно отменить в любой момент</li>
        </ul>

        <a href="#" class="pricing-btn outline">Попробовать</a>
      </div>

      <div class="pricing-card featured">
        <span class="pricing-tag">Профи</span>
        <div class="pricing-title-card">Поднятие в топ</div>
        <div class="pricing-desc">Хочу больше клиентов</div>
        <div class="pricing-price">от 10 000 ₽ <span>/ год</span></div>
        <div class="pricing-note">Верх каталога по вашему району и услуге</div>

        <ul class="pricing-features">
          <li>Всё из тарифа «Старт»</li>
          <li>Позиция в топе каталога</li>
          <li>Бейдж «Проверено» и выделение</li>
          <li>До 15 фото в галерее</li>
          <li>Расширенная статистика: клики и звонки</li>
          <li>Приоритетная поддержка</li>
        </ul>

        <a href="#" class="pricing-btn primary">В топ</a>
      </div>
    </div>
  </section>

  <!-- ПОДВАЛ -->
  <footer class="footer">
    <div class="footer-inner">
      <div>
        <div class="footer-heading">АвтоСервисы Воронежа</div>
        <p>Каталог СТО с ценами, отзывами и адресами. Помогаем найти надёжный автосервис рядом с домом.</p>
      </div>
      <div>
        <div class="footer-heading">Каталог</div>
        <ul class="footer-ul">
          <li><a href="#">Все СТО</a></li>
          <li><a href="#">Кузовной ремонт</a></li>
          <li><a href="#">Шиномонтаж</a></li>
          <li><a href="#">Диагностика</a></li>
        </ul>
      </div>
      <div>
        <div class="footer-heading">Районы</div>
        <ul class="footer-ul">
          <li><a href="#">Ленинский</a></li>
          <li><a href="#">Центральный</a></li>
          <li><a href="#">Коминтерновский</a></li>
          <li><a href="#">Советский</a></li>
        </ul>
      </div>
      <div>
        <div class="footer-heading">Сервис</div>
        <ul class="footer-ul">
          <li><a href="#">Для СТО</a></li>
          <li><a href="#">Размещение</a></li>
          <li><a href="#">Контакты</a></li>
          <li><a href="#">Политика ПДн</a></li>
        </ul>
      </div>
    </div>
    <div class="footer-copy">
      © 2026 АвтоСервисы Воронежа · Бесплатно для клиентов · Данные из открытых источников
    </div>
  </footer>

  <script>
    // Мобильное меню
    const menuToggle = document.getElementById('menuToggle');
    const headerNav = document.getElementById('headerNav');

    if (menuToggle && headerNav) {
      menuToggle.addEventListener('click', () => {
        menuToggle.classList.toggle('active');
        headerNav.classList.toggle('open');
      });
      headerNav.querySelectorAll('a').forEach(link => {
        link.addEventListener('click', () => {
          menuToggle.classList.remove('active');
          headerNav.classList.remove('open');
        });
      });
    }

    // Фильтрация
    const districtChips = document.querySelectorAll('#districtsChips .chip');
    const serviceFilter = document.getElementById('serviceFilter');
    const brandFilter = document.getElementById('brandFilter');
    const priceFilter = document.getElementById('priceFilter');
    const ratingFilter = document.getElementById('ratingFilter');
    const searchInput = document.getElementById('searchInput');
    const searchBtn = document.getElementById('searchBtn');
    const stoCards = document.querySelectorAll('.sto-card');
    const resultsCount = document.getElementById('resultsCount');

    let activeDistrict = 'all';

    function applyFilters() {
      const service = serviceFilter.value;
      const brand = brandFilter.value;
      const price = priceFilter.value;
      const rating = ratingFilter.value;
      const query = searchInput.value.trim().toLowerCase();

      let visible = 0;

      stoCards.forEach(card => {
        const cardDistrict = card.dataset.district;
        const cardServices = (card.dataset.service || '').split(',');
        const cardBrands = (card.dataset.brand || '').split(',');
        const cardPrice = card.dataset.price;
        const cardRating = parseFloat(card.dataset.rating);
        const cardText = card.innerText.toLowerCase();

        let ok = true;

        if (activeDistrict !== 'all' && cardDistrict !== activeDistrict) ok = false;
        if (service && !cardServices.includes(service)) ok = false;
        if (brand && !cardBrands.includes(brand)) ok = false;
        if (price && cardPrice !== price) ok = false;
        if (rating && cardRating < parseFloat(rating)) ok = false;
        if (query && !cardText.includes(query)) ok = false;

        if (ok) {
          card.style.display = '';
          visible++;
        } else {
          card.style.display = 'none';
        }
      });

      resultsCount.textContent = visible;
    }

    districtChips.forEach(chip => {
      chip.addEventListener('click', () => {
        districtChips.forEach(c => c.classList.remove('active'));
        chip.classList.add('active');
        activeDistrict = chip.dataset.district;
        applyFilters();
      });
    });

    serviceFilter.addEventListener('change', applyFilters);
    brandFilter.addEventListener('change', applyFilters);
    priceFilter.addEventListener('change', applyFilters);
    ratingFilter.addEventListener('change', applyFilters);
    searchBtn.addEventListener('click', applyFilters);
    searchInput.addEventListener('input', applyFilters);

    // Переключатель вида
    const viewBtns = document.querySelectorAll('.view-btn');
    viewBtns.forEach(btn => {
      btn.addEventListener('click', () => {
        viewBtns.forEach(b => b.classList.remove('active'));
        btn.classList.add('active');
        if (btn.dataset.view === 'map') {
          alert('Здесь будет карта с СТО. В разработке.');
        }
      });
    });

    // Заглушки для кнопок
    document.querySelectorAll('.btn-call').forEach(btn => {
      btn.addEventListener('click', () => alert('Позвонить в СТО — здесь будет переход на номер телефона.'));
    });
    document.querySelectorAll('.btn-map').forEach(btn => {
      btn.addEventListener('click', () => alert('Показать на карте — здесь будет открытие Яндекс.Карт.'));
    });
  </script>

</body>
</html>
