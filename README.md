<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Code for Green School: Eco Survival — README</title>
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&family=Lexend:wght@300;400;500;600;700;800&family=JetBrains+Mono:wght@400;600&display=swap" rel="stylesheet" />
<style>
  /* ==========================================================
     RESET & BASE
  ========================================================== */
  * { margin: 0; padding: 0; box-sizing: border-box; }
  html { scroll-behavior: smooth; }
  body {
    font-family: 'Lexend', -apple-system, BlinkMacSystemFont, sans-serif;
    background: #0a0e14;
    color: #e2e8f0;
    line-height: 1.7;
    font-size: 15px;
    overflow-x: hidden;
  }

  /* Background gradient động */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background:
      radial-gradient(circle at 15% 20%, rgba(16, 185, 129, 0.08) 0%, transparent 40%),
      radial-gradient(circle at 85% 60%, rgba(59, 130, 246, 0.06) 0%, transparent 40%),
      radial-gradient(circle at 50% 90%, rgba(168, 85, 247, 0.05) 0%, transparent 40%);
    pointer-events: none;
    z-index: 0;
  }

  /* ==========================================================
     LAYOUT
  ========================================================== */
  .page {
    position: relative;
    z-index: 1;
    max-width: 1100px;
    margin: 0 auto;
    padding: 0 20px 60px;
  }

  /* ==========================================================
     HERO SECTION
  ========================================================== */
  .hero {
    text-align: center;
    padding: 70px 20px 50px;
    border-bottom: 2px solid rgba(16, 185, 129, 0.2);
    margin-bottom: 40px;
  }

  .hero-badge {
    display: inline-block;
    font-family: 'Press Start 2P', monospace;
    font-size: 10px;
    color: #facc15;
    letter-spacing: 2px;
    padding: 6px 14px;
    background: rgba(250, 204, 21, 0.1);
    border: 1px solid rgba(250, 204, 21, 0.3);
    border-radius: 20px;
    margin-bottom: 20px;
  }

  .hero-logo {
    font-size: 64px;
    margin-bottom: 12px;
    animation: float 3s ease-in-out infinite;
  }

  @keyframes float {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-8px); }
  }

  .hero h1 {
    font-family: 'Press Start 2P', monospace;
    font-size: clamp(18px, 3vw, 28px);
    color: #10b981;
    letter-spacing: 1px;
    margin-bottom: 14px;
    line-height: 1.4;
  }

  .hero .subtitle {
    font-size: clamp(14px, 1.6vw, 18px);
    color: #fbbf24;
    font-weight: 700;
    font-style: italic;
    margin-bottom: 8px;
  }

  .hero .tagline {
    font-size: 14px;
    color: #94a3b8;
    margin-bottom: 28px;
  }

  /* Badges */
  .badges {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 8px;
    margin-bottom: 28px;
  }

  .badge {
    display: inline-flex;
    align-items: center;
    gap: 4px;
    padding: 4px 10px;
    border-radius: 6px;
    font-size: 11px;
    font-weight: 700;
    text-decoration: none;
    transition: transform 0.15s;
    border: 1px solid rgba(255, 255, 255, 0.1);
  }

  .badge:hover { transform: translateY(-2px); }
  .badge-gpl   { background: #1e40af; color: white; }
  .badge-js    { background: #facc15; color: #000; }
  .badge-fb    { background: #ea580c; color: white; }
  .badge-gh    { background: #16a34a; color: white; }
  .badge-star  { background: #1e293b; color: #facc15; }

  /* CTA Button */
  .cta-btn {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    padding: 16px 34px;
    background: linear-gradient(135deg, #10b981, #059669);
    color: #fff;
    text-decoration: none;
    font-family: 'Press Start 2P', monospace;
    font-size: 12px;
    letter-spacing: 1px;
    border-radius: 12px;
    box-shadow: 0 6px 0 #065f46, 0 10px 30px rgba(16, 185, 129, 0.4);
    transition: all 0.15s;
    margin-bottom: 12px;
  }

  .cta-btn:hover {
    transform: translateY(-2px);
    box-shadow: 0 8px 0 #065f46, 0 14px 40px rgba(16, 185, 129, 0.5);
  }

  .cta-btn:active {
    transform: translateY(4px);
    box-shadow: 0 2px 0 #065f46;
  }

  .link-code {
    font-family: 'JetBrains Mono', monospace;
    font-size: 12px;
    color: #6ee7b7;
    background: rgba(16, 185, 129, 0.08);
    padding: 6px 14px;
    border-radius: 6px;
    border: 1px dashed rgba(16, 185, 129, 0.3);
    display: inline-block;
    margin-top: 8px;
    user-select: all;
  }

  /* ==========================================================
     TABLE OF CONTENTS
  ========================================================== */
  .toc {
    background: linear-gradient(160deg, #0f172a 0%, #1e1b4b 100%);
    border: 2px solid rgba(16, 185, 129, 0.3);
    border-radius: 16px;
    padding: 24px 28px;
    margin-bottom: 50px;
    box-shadow: 0 8px 32px rgba(0, 0, 0, 0.4);
  }

  .toc-title {
    font-family: 'Press Start 2P', monospace;
    font-size: 12px;
    color: #10b981;
    margin-bottom: 16px;
    letter-spacing: 1px;
  }

  .toc-list {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 8px 20px;
    list-style: none;
  }

  .toc-list a {
    color: #cbd5e1;
    text-decoration: none;
    font-size: 14px;
    padding: 6px 10px;
    border-radius: 6px;
    display: flex;
    align-items: center;
    gap: 8px;
    transition: all 0.15s;
  }

  .toc-list a:hover {
    background: rgba(16, 185, 129, 0.1);
    color: #10b981;
    transform: translateX(4px);
  }

  .toc-list a::before {
    content: '▸';
    color: #10b981;
    font-weight: bold;
  }

  /* ==========================================================
     SECTIONS
  ========================================================== */
  section {
    margin-bottom: 50px;
    scroll-margin-top: 20px;
  }

  h2 {
    font-family: 'Press Start 2P', monospace;
    font-size: clamp(14px, 1.6vw, 18px);
    color: #10b981;
    padding-bottom: 14px;
    margin-bottom: 24px;
    border-bottom: 2px solid rgba(16, 185, 129, 0.2);
    letter-spacing: 1px;
    display: flex;
    align-items: center;
    gap: 12px;
    line-height: 1.5;
  }

  h3 {
    font-family: 'Lexend', sans-serif;
    font-size: 18px;
    color: #34d399;
    font-weight: 700;
    margin: 28px 0 14px;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  h3::before {
    content: '';
    width: 4px;
    height: 20px;
    background: linear-gradient(180deg, #10b981, #059669);
    border-radius: 2px;
  }

  h4 {
    font-size: 15px;
    color: #fbbf24;
    font-weight: 700;
    margin: 20px 0 10px;
  }

  p {
    color: #cbd5e1;
    margin-bottom: 14px;
    font-size: 15px;
  }

  /* ==========================================================
     CARDS
  ========================================================== */
  .card-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 16px;
    margin: 20px 0;
  }

  .card {
    background: linear-gradient(160deg, #0f172a, #1e1b4b);
    border: 2px solid rgba(51, 65, 85, 0.6);
    border-radius: 14px;
    padding: 20px;
    transition: all 0.2s;
  }

  .card:hover {
    border-color: #10b981;
    transform: translateY(-4px);
    box-shadow: 0 12px 30px rgba(16, 185, 129, 0.15);
  }

  .card-icon {
    font-size: 32px;
    margin-bottom: 10px;
    display: block;
  }

  .card-title {
    font-weight: 800;
    color: #10b981;
    font-size: 15px;
    margin-bottom: 6px;
  }

  .card-desc {
    color: #94a3b8;
    font-size: 13px;
    line-height: 1.6;
  }

  /* ==========================================================
     TABLES
  ========================================================== */
  .table-wrap {
    overflow-x: auto;
    border-radius: 12px;
    border: 2px solid rgba(51, 65, 85, 0.6);
    margin: 16px 0;
    background: rgba(15, 23, 42, 0.6);
  }

  table {
    width: 100%;
    border-collapse: collapse;
    font-size: 14px;
    min-width: 500px;
  }

  thead {
    background: linear-gradient(90deg, rgba(16, 185, 129, 0.15), rgba(59, 130, 246, 0.15));
  }

  th {
    padding: 14px 16px;
    text-align: left;
    color: #10b981;
    font-weight: 800;
    font-size: 12px;
    text-transform: uppercase;
    letter-spacing: 0.5px;
    border-bottom: 2px solid rgba(16, 185, 129, 0.3);
  }

  td {
    padding: 12px 16px;
    border-bottom: 1px solid rgba(51, 65, 85, 0.4);
    color: #cbd5e1;
  }

  tbody tr:hover { background: rgba(16, 185, 129, 0.04); }
  tbody tr:last-child td { border-bottom: none; }

  td strong { color: #fbbf24; }

  /* ==========================================================
     CODE BLOCKS
  ========================================================== */
  pre, code {
    font-family: 'JetBrains Mono', monospace;
  }

  code {
    background: rgba(16, 185, 129, 0.1);
    color: #6ee7b7;
    padding: 2px 7px;
    border-radius: 4px;
    font-size: 13px;
    border: 1px solid rgba(16, 185, 129, 0.2);
  }

  pre {
    background: #020617;
    border: 2px solid rgba(51, 65, 85, 0.8);
    border-left: 4px solid #10b981;
    border-radius: 10px;
    padding: 16px 20px;
    overflow-x: auto;
    margin: 16px 0;
    font-size: 13px;
    line-height: 1.6;
    color: #e2e8f0;
    position: relative;
  }

  pre code {
    background: none;
    border: none;
    padding: 0;
    color: inherit;
    font-size: inherit;
  }

  /* Nút copy cho code block */
  .code-wrap { position: relative; margin: 16px 0; }
  .code-wrap pre { margin: 0; }

  .copy-btn {
    position: absolute;
    top: 10px;
    right: 10px;
    background: #1e293b;
    border: 1px solid #334155;
    color: #94a3b8;
    padding: 5px 10px;
    border-radius: 6px;
    font-size: 11px;
    font-family: 'Lexend', sans-serif;
    cursor: pointer;
    transition: all 0.15s;
    z-index: 2;
  }

  .copy-btn:hover { background: #10b981; color: white; border-color: #10b981; }
  .copy-btn.copied { background: #10b981; color: white; border-color: #10b981; }

  /* ==========================================================
     ASCII DIAGRAM (Thời khóa biểu)
  ========================================================== */
  .schedule-diagram {
    background: #020617;
    border: 2px solid rgba(16, 185, 129, 0.3);
    border-radius: 12px;
    padding: 20px;
    overflow-x: auto;
    margin: 20px 0;
    font-family: 'JetBrains Mono', monospace;
    font-size: 12px;
    line-height: 1.7;
    color: #6ee7b7;
  }

  .schedule-diagram .label { color: #94a3b8; }
  .schedule-diagram .lesson { color: #fbbf24; font-weight: 700; }
  .schedule-diagram .break { color: #38bdf8; font-weight: 700; }

  /* ==========================================================
     CALLOUT BOXES
  ========================================================== */
  .callout {
    border-radius: 12px;
    padding: 16px 20px;
    margin: 16px 0;
    display: flex;
    gap: 14px;
    align-items: flex-start;
    font-size: 14px;
    line-height: 1.6;
  }

  .callout-icon { font-size: 22px; flex-shrink: 0; line-height: 1; margin-top: 2px; }
  .callout-content { flex: 1; }
  .callout-content strong { display: block; margin-bottom: 4px; font-size: 15px; }

  .callout-info    { background: rgba(59, 130, 246, 0.08);   border-left: 4px solid #3b82f6; }
  .callout-info strong    { color: #60a5fa; }
  .callout-success { background: rgba(16, 185, 129, 0.08);   border-left: 4px solid #10b981; }
  .callout-success strong { color: #34d399; }
  .callout-warning { background: rgba(250, 204, 21, 0.08);   border-left: 4px solid #facc15; }
  .callout-warning strong { color: #fbbf24; }
  .callout-danger  { background: rgba(239, 68, 68, 0.08);    border-left: 4px solid #ef4444; }
  .callout-danger strong  { color: #f87171; }
  .callout-tip     { background: rgba(168, 85, 247, 0.08);   border-left: 4px solid #a855f7; }
  .callout-tip strong     { color: #c084fc; }

  /* ==========================================================
     STEPS (Cài đặt)
  ========================================================== */
  .steps {
    counter-reset: step-counter;
    margin: 20px 0;
  }

  .step {
    position: relative;
    padding: 20px 20px 20px 70px;
    background: linear-gradient(160deg, #0f172a, #1e1b4b);
    border: 2px solid rgba(51, 65, 85, 0.6);
    border-radius: 14px;
    margin-bottom: 14px;
    counter-increment: step-counter;
    transition: all 0.2s;
  }

  .step:hover {
    border-color: rgba(16, 185, 129, 0.5);
    transform: translateX(4px);
  }

  .step::before {
    content: counter(step-counter);
    position: absolute;
    left: 20px;
    top: 20px;
    width: 36px;
    height: 36px;
    background: linear-gradient(135deg, #10b981, #059669);
    color: white;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'Press Start 2P', monospace;
    font-size: 12px;
    box-shadow: 0 4px 12px rgba(16, 185, 129, 0.4);
  }

  .step-title {
    font-weight: 800;
    color: #10b981;
    font-size: 16px;
    margin-bottom: 8px;
  }

  .step-desc {
    color: #cbd5e1;
    font-size: 14px;
    line-height: 1.6;
  }

  .step-desc strong { color: #fbbf24; }

  /* ==========================================================
     FEATURE LIST
  ========================================================== */
  .feature-list {
    list-style: none;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 10px;
    margin: 16px 0;
  }

  .feature-list li {
    display: flex;
    align-items: flex-start;
    gap: 10px;
    padding: 10px 14px;
    background: rgba(15, 23, 42, 0.6);
    border: 1px solid rgba(51, 65, 85, 0.5);
    border-radius: 10px;
    font-size: 14px;
    color: #cbd5e1;
    transition: all 0.15s;
  }

  .feature-list li:hover {
    border-color: rgba(16, 185, 129, 0.4);
    background: rgba(16, 185, 129, 0.05);
  }

  .feature-list li::before {
    content: '✓';
    color: #10b981;
    font-weight: 900;
    flex-shrink: 0;
  }

  /* ==========================================================
     CHARACTER CARDS
  ========================================================== */
  .char-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 16px;
    margin: 20px 0;
  }

  .char-card {
    background: linear-gradient(160deg, #0f172a, #1e1b4b);
    border: 2px solid rgba(51, 65, 85, 0.6);
    border-radius: 14px;
    padding: 20px;
    text-align: center;
    transition: all 0.2s;
    position: relative;
    overflow: hidden;
  }

  .char-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 4px;
    background: var(--char-color, #10b981);
  }

  .char-card:hover {
    transform: translateY(-6px);
    box-shadow: 0 16px 40px rgba(0, 0, 0, 0.5);
    border-color: var(--char-color, #10b981);
  }

  .char-avatar {
    font-size: 48px;
    margin-bottom: 10px;
  }

  .char-name {
    font-family: 'Press Start 2P', monospace;
    font-size: 13px;
    color: var(--char-color, #10b981);
    margin-bottom: 6px;
    letter-spacing: 0.5px;
  }

  .char-role {
    font-size: 12px;
    color: #94a3b8;
    margin-bottom: 12px;
    font-weight: 600;
  }

  .char-skill {
    background: rgba(16, 185, 129, 0.1);
    border: 1px solid rgba(16, 185, 129, 0.3);
    border-radius: 8px;
    padding: 8px 12px;
    font-size: 13px;
    color: #6ee7b7;
    font-weight: 600;
  }

  .char-traits {
    margin-top: 10px;
    font-size: 11px;
    color: #64748b;
    line-height: 1.5;
  }

  /* ==========================================================
     WEATHER CARDS
  ========================================================== */
  .weather-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
    gap: 16px;
    margin: 20px 0;
  }

  .weather-card {
    border-radius: 14px;
    padding: 20px;
    border: 2px solid;
    transition: all 0.2s;
  }

  .weather-card:hover { transform: scale(1.03); }

  .weather-hot {
    background: linear-gradient(160deg, rgba(249, 115, 22, 0.15), rgba(239, 68, 68, 0.08));
    border-color: rgba(249, 115, 22, 0.5);
  }

  .weather-pollution {
    background: linear-gradient(160deg, rgba(168, 85, 247, 0.15), rgba(126, 34, 206, 0.08));
    border-color: rgba(168, 85, 247, 0.5);
  }

  .weather-rain {
    background: linear-gradient(160deg, rgba(56, 189, 248, 0.15), rgba(30, 58, 138, 0.08));
    border-color: rgba(56, 189, 248, 0.5);
  }

  .weather-icon {
    font-size: 40px;
    margin-bottom: 10px;
  }

  .weather-name {
    font-weight: 800;
    font-size: 16px;
    margin-bottom: 8px;
    letter-spacing: 1px;
  }

  .weather-hot .weather-name { color: #fb923c; }
  .weather-pollution .weather-name { color: #c084fc; }
  .weather-rain .weather-name { color: #38bdf8; }

  .weather-desc {
    font-size: 13px;
    color: #cbd5e1;
    line-height: 1.6;
    margin-bottom: 10px;
  }

  .weather-counter {
    font-size: 12px;
    padding: 6px 10px;
    background: rgba(0, 0, 0, 0.3);
    border-radius: 6px;
    color: #94a3b8;
    display: inline-block;
  }

  /* ==========================================================
     AUTHOR SECTION
  ========================================================== */
  .author-box {
    display: flex;
    align-items: center;
    gap: 20px;
    padding: 24px;
    background: linear-gradient(160deg, #0f172a, #1e1b4b);
    border: 2px solid rgba(16, 185, 129, 0.3);
    border-radius: 16px;
    margin: 20px 0;
    flex-wrap: wrap;
  }

  .author-avatar {
    font-size: 64px;
    width: 100px;
    height: 100px;
    display: flex;
    align-items: center;
    justify-content: center;
    background: linear-gradient(135deg, rgba(16, 185, 129, 0.2), rgba(59, 130, 246, 0.2));
    border-radius: 50%;
    border: 3px solid rgba(16, 185, 129, 0.5);
    flex-shrink: 0;
  }

  .author-info { flex: 1; min-width: 200px; }
  .author-name {
    font-family: 'Press Start 2P', monospace;
    font-size: 16px;
    color: #10b981;
    margin-bottom: 6px;
  }
  .author-role {
    color: #94a3b8;
    font-size: 13px;
    margin-bottom: 12px;
  }
  .author-links {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }

  .author-link {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 6px 14px;
    background: #1e293b;
    border: 1px solid #334155;
    border-radius: 8px;
    color: #cbd5e1;
    text-decoration: none;
    font-size: 12px;
    font-weight: 600;
    transition: all 0.15s;
  }

  .author-link:hover {
    background: #10b981;
    color: white;
    border-color: #10b981;
    transform: translateY(-2px);
  }

  /* ==========================================================
     LICENSE
  ========================================================== */
  .license-box {
    background: #020617;
    border: 2px solid rgba(250, 204, 21, 0.4);
    border-radius: 14px;
    padding: 20px;
    margin: 20px 0;
  }

  .license-box pre {
    border: none;
    border-left: 4px solid #facc15;
    background: transparent;
    margin: 0;
  }

  .license-img {
    display: block;
    margin: 20px auto;
    max-width: 130px;
  }

  .perm-table {
    margin-top: 20px;
  }

  /* ==========================================================
     THANKS
  ========================================================== */
  .thanks-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 12px;
    margin: 20px 0;
  }

  .thanks-item {
    padding: 14px 16px;
    background: rgba(15, 23, 42, 0.6);
    border: 1px solid rgba(51, 65, 85, 0.5);
    border-radius: 10px;
    display: flex;
    align-items: center;
    gap: 12px;
    font-size: 14px;
    color: #cbd5e1;
    transition: all 0.15s;
  }

  .thanks-item:hover {
    border-color: rgba(16, 185, 129, 0.4);
    background: rgba(16, 185, 129, 0.05);
  }

  .thanks-icon {
    font-size: 24px;
    flex-shrink: 0;
  }

  /* ==========================================================
     FOOTER
  ========================================================== */
  footer {
    text-align: center;
    padding: 60px 20px 30px;
    border-top: 2px solid rgba(16, 185, 129, 0.2);
    margin-top: 60px;
  }

  footer h2 {
    border: none;
    justify-content: center;
    font-size: clamp(14px, 1.8vw, 20px);
    color: #10b981;
    padding: 0;
    margin-bottom: 16px;
    display: block;
    text-align: center;
  }

  footer .quote {
    font-style: italic;
    color: #fbbf24;
    font-size: 15px;
    margin: 16px 0;
    font-weight: 600;
  }

  footer .club {
    font-family: 'Press Start 2P', monospace;
    font-size: 10px;
    color: #94a3b8;
    letter-spacing: 1px;
    margin-bottom: 20px;
  }

  footer .star-cta {
    margin: 24px 0 16px;
  }

  footer .star-cta a {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 12px 24px;
    background: linear-gradient(135deg, #facc15, #f59e0b);
    color: #0a0e14;
    text-decoration: none;
    border-radius: 10px;
    font-weight: 800;
    font-size: 14px;
    box-shadow: 0 4px 0 #b45309, 0 8px 24px rgba(250, 204, 21, 0.3);
    transition: all 0.15s;
  }

  footer .star-cta a:hover {
    transform: translateY(-2px);
    box-shadow: 0 6px 0 #b45309, 0 12px 32px rgba(250, 204, 21, 0.4);
  }

  footer .made-in {
    color: #64748b;
    font-size: 12px;
    margin-top: 20px;
  }

  /* ==========================================================
     BACK TO TOP
  ========================================================== */
  .back-to-top {
    position: fixed;
    bottom: 24px;
    right: 24px;
    width: 48px;
    height: 48px;
    background: linear-gradient(135deg, #10b981, #059669);
    color: white;
    border: none;
    border-radius: 50%;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 20px;
    box-shadow: 0 6px 20px rgba(16, 185, 129, 0.4);
    opacity: 0;
    transform: translateY(20px);
    transition: all 0.25s;
    z-index: 100;
  }

  .back-to-top.visible {
    opacity: 1;
    transform: translateY(0);
  }

  .back-to-top:hover {
    transform: translateY(-4px);
    box-shadow: 0 10px 30px rgba(16, 185, 129, 0.6);
  }

  /* ==========================================================
     RESPONSIVE
  ========================================================== */
  @media (max-width: 768px) {
    .page { padding: 0 14px 40px; }
    .hero { padding: 40px 10px 30px; }
    .hero-logo { font-size: 48px; }
    .card-grid, .char-grid, .weather-grid, .thanks-grid {
      grid-template-columns: 1fr;
    }
    .author-box { flex-direction: column; text-align: center; }
    .author-links { justify-content: center; }
    .toc-list { grid-template-columns: 1fr; }
    .step { padding: 60px 16px 16px; }
    .step::before { left: 50%; transform: translateX(-50%); top: 12px; }
    h2 { font-size: 13px; }
    pre { padding: 12px 14px; font-size: 12px; }
    .schedule-diagram { font-size: 10px; padding: 14px; }
    .back-to-top { bottom: 16px; right: 16px; width: 42px; height: 42px; }
  }

  /* Scrollbar */
  ::-webkit-scrollbar { width: 10px; height: 10px; }
  ::-webkit-scrollbar-track { background: #0a0e14; }
  ::-webkit-scrollbar-thumb {
    background: linear-gradient(180deg, #10b981, #059669);
    border-radius: 5px;
  }
  ::-webkit-scrollbar-thumb:hover { background: #34d399; }
</style>
</head>
<body>

<div class="page">

  <!-- ==========================================================
       HERO SECTION
  ========================================================== -->
  <header class="hero">
    <div class="hero-badge">HỘI THI CLB TIN HỌC 2026–2027</div>
    <div class="hero-logo">🌱</div>
    <h1>CODE FOR GREEN SCHOOL</h1>
    <div class="subtitle">"CÙNG THPT BÌNH CHÁNH SỐNG XANH"</div>
    <p class="tagline">Trò chơi 2D pixel art giáo dục về bảo vệ môi trường</p>

    <div class="badges">
      <a href="https://www.gnu.org/licenses/gpl-3.0" class="badge badge-gpl" target="_blank">
        📜 GPL v3.0
      </a>
      <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" class="badge badge-js" target="_blank">
        ⚡ JavaScript
      </a>
      <a href="https://firebase.google.com/" class="badge badge-fb" target="_blank">
        🔥 Firebase
      </a>
      <a href="https://pages.github.com/" class="badge badge-gh" target="_blank">
        🚀 GitHub Pages
      </a>
    </div>

    <a href="https://hihiquan2010.github.io/GreenProject/" class="cta-btn" target="_blank">
      🎮 BẤM VÀO ĐÂY ĐỂ CHƠI NGAY
    </a>
    <br />
    <span class="link-code">https://hihiquan2010.github.io/GreenProject/</span>
  </header>

  <!-- ==========================================================
       TABLE OF CONTENTS
  ========================================================== -->
  <nav class="toc">
    <div class="toc-title">📑 MỤC LỤC</div>
    <ul class="toc-list">
      <li><a href="#gioi-thieu">📖 Giới thiệu</a></li>
      <li><a href="#gameplay">🎮 Gameplay</a></li>
      <li><a href="#multiplayer">👥 Chơi nhóm</a></li>
      <li><a href="#graphics">🎨 Đồ họa</a></li>
      <li><a href="#caidat">🚀 Cài đặt</a></li>
      <li><a href="#dieukhien">🎯 Điều khiển</a></li>
      <li><a href="#congnghe">🛠️ Công nghệ</a></li>
      <li><a href="#cautruc">📁 Cấu trúc</a></li>
      <li><a href="#giaoduc">🎓 Giáo dục</a></li>
      <li><a href="#donggop">🤝 Đóng góp</a></li>
      <li><a href="#tacgia">👨‍💻 Tác giả</a></li>
      <li><a href="#license">📜 Giấy phép</a></li>
      <li><a href="#thanks">🙏 Cảm ơn</a></li>
    </ul>
  </nav>

  <!-- ==========================================================
       GIỚI THIỆU
  ========================================================== -->
  <section id="gioi-thieu">
    <h2>📖 GIỚI THIỆU</h2>
    <p>
      <strong>Code for Green School: Eco Survival</strong> là một trò chơi
      <strong style="color: #6ee7b7;">web 2D top-down pixel art</strong> mô phỏng một ngày học tập tại
      <strong style="color: #fbbf24;">Trường THPT Bình Chánh</strong>. Người chơi hóa thân thành
      một học sinh, phải vượt qua những ngày học tập với thời tiết khắc nghiệt, bảo vệ môi trường và sinh tồn qua từng tiết học.
    </p>

    <h3>🎯 Nhiệm vụ chính</h3>
    <div class="card-grid">
      <div class="card">
        <span class="card-icon">🎒</span>
        <div class="card-title">Sinh tồn</div>
        <div class="card-desc">Sống sót qua nhiều ngày, giữ HP trên 0</div>
      </div>
      <div class="card">
        <span class="card-icon">☀️</span>
        <div class="card-title">Đối phó thời tiết</div>
        <div class="card-desc">Thích nghi với Oi bức, Ô nhiễm, Mưa phùn</div>
      </div>
      <div class="card">
        <span class="card-icon">♻️</span>
        <div class="card-title">Dọn rác</div>
        <div class="card-desc">Bảo vệ môi trường, hồi máu, giảm ô nhiễm</div>
      </div>
      <div class="card">
        <span class="card-icon">🪑</span>
        <div class="card-title">Ngồi ghế</div>
        <div class="card-desc">Tuân thủ giờ học, không bị khiển trách</div>
      </div>
      <div class="card">
        <span class="card-icon">⚡</span>
        <div class="card-title">Tiết kiệm điện</div>
        <div class="card-desc">Tắt thiết bị khi ra chơi</div>
      </div>
      <div class="card">
        <span class="card-icon">🔇</span>
        <div class="card-title">Tập trung</div>
        <div class="card-desc">Vượt minigame "Giữ im lặng" trong tiết</div>
      </div>
      <div class="card">
        <span class="card-icon">👥</span>
        <div class="card-title">Chơi nhóm</div>
        <div class="card-desc">Cùng bạn bè sinh tồn qua Firebase</div>
      </div>
    </div>

    <div class="callout callout-info">
      <span class="callout-icon">💡</span>
      <div class="callout-content">
        <strong>Nguồn cảm hứng</strong>
        Bản đồ game được thiết kế dựa trên ảnh chụp thực tế của trường THPT Bình Chánh: dãy nhà 2 tầng mái ngói đỏ,
        sân trước rộng lớn, cột cờ Tổ quốc, hàng cây xanh hai bên.
      </div>
    </div>
  </section>

  <!-- ==========================================================
       GAMEPLAY
  ========================================================== -->
  <section id="gameplay">
    <h2>🎮 GAMEPLAY</h2>

    <h3>⏰ Thời khóa biểu một ngày</h3>
    <div class="schedule-diagram">
<pre><span class="break">┌──────────────────┐</span>   <span class="lesson">┌────────┐</span>   <span class="lesson">┌────────┐</span>   <span class="break">┌──────────┐</span>
<span class="break">│ RA CHƠI SÁNG 30s │</span> → <span class="lesson">│ TIẾT 1 │</span> → <span class="lesson">│ TIẾT 2 │</span> → <span class="break">│ RA CHƠI  │</span>
<span class="break">└──────────────────┘</span>   <span class="lesson">│  60s   │</span>   <span class="lesson">│  60s   │</span>   <span class="break">│   30s    │</span>
                       <span class="lesson">└────────┘</span>   <span class="lesson">└────────┘</span>   <span class="break">└──────────┘</span>
                                                        ↓
<span class="lesson">┌────────┐</span>   <span class="lesson">┌────────┐</span>   <span class="lesson">┌────────┐</span>   <span class="break">┌──────────┐</span>   <span class="lesson">┌────────┐</span>
<span class="lesson">│ TIẾT 7 │</span> ← <span class="lesson">│ TIẾT 6 │</span> ← <span class="lesson">│ TIẾT 5 │</span> ← <span class="break">│ RA CHƠI  │</span> ← <span class="lesson">│ TIẾT 3 │</span>
<span class="lesson">│  60s   │</span>   <span class="lesson">│  60s   │</span>   <span class="lesson">│  60s   │</span>   <span class="break">│   30s    │</span>   <span class="lesson">│  60s   │</span>
<span class="lesson">└────────┘</span>   <span class="lesson">└────────┘</span>   <span class="lesson">└────────┘</span>   <span class="break">└──────────┘</span>   <span class="lesson">└────────┘</span></pre>
    </div>

    <div class="feature-list">
      <li>Mỗi tiết: <strong style="color: #fbbf24;">60 giây</strong></li>
      <li>Mỗi giờ ra chơi: <strong style="color: #38bdf8;">30 giây</strong></li>
      <li>Chuyển tiết: <strong style="color: #c084fc;">3 giây</strong> (có tiếng chuông 🔔)</li>
    </div>

    <h3>🌤️ Ba loại thời tiết</h3>
    <p>Mỗi ngày chỉ có <strong>DUY NHẤT MỘT</strong> loại thời tiết. Từ <strong>ngày 4 trở đi</strong> mới random (không lặp lại ngày trước).</p>

    <div class="weather-grid">
      <div class="weather-card weather-hot">
        <div class="weather-icon">☀️</div>
        <div class="weather-name">OI BỨC</div>
        <div class="weather-desc">Nhiệt độ tăng khi ở lớp không có quạt. Gây sốc nhiệt nếu nhiệt độ vượt 85°.</div>
        <span class="weather-counter">Tắt điện khi ra chơi, bật quạt khi vào lớp</span>
      </div>

      <div class="weather-card weather-pollution">
        <div class="weather-icon">☣️</div>
        <div class="weather-name">Ô NHIỄM</div>
        <div class="weather-desc">Rác vương vãi bốc mùi hôi. Càng nhiều rác, không khí càng độc hại.</div>
        <span class="weather-counter">Nhặt rác bỏ vào Thùng Xanh</span>
      </div>

      <div class="weather-card weather-rain">
        <div class="weather-icon">🌧️</div>
        <div class="weather-name">MƯA PHÙN</div>
        <div class="weather-desc">Vũng nước trơn trượt, cống tắc. Quạt tay sẽ gây hạ thân nhiệt nguy hiểm.</div>
        <span class="weather-counter">Tắt quạt, tránh vũng, thông cống</span>
      </div>
    </div>

    <h3>🌡️ Cơ chế nhiệt độ cơ thể</h3>
    <p>Thanh nhiệt độ hiển thị <strong>0° → 100°</strong>, mức chuẩn là <strong style="color: #10b981;">50°</strong>.</p>

    <div class="table-wrap">
      <table>
        <thead>
          <tr>
            <th>Trạng thái</th>
            <th>Điều kiện</th>
            <th>Tác động</th>
          </tr>
        </thead>
        <tbody>
          <tr><td>🔥 Sốc nhiệt</td><td>Nhiệt độ &gt; 85°</td><td><strong>Mất 4 HP/giây</strong></td></tr>
          <tr><td>♨️ Nóng</td><td>Nhiệt độ &gt; 70°</td><td>Mất 1 HP/giây</td></tr>
          <tr><td>✅ Bình thường</td><td>30° ≤ Nhiệt độ ≤ 70°</td><td>Không ảnh hưởng</td></tr>
          <tr><td>🧊 Mát</td><td>Nhiệt độ &lt; 30°</td><td>Mất 1 HP/giây</td></tr>
          <tr><td>❄️ Hạ thân nhiệt</td><td>Nhiệt độ &lt; 15°</td><td><strong>Mất 3 HP/giây</strong></td></tr>
        </tbody>
      </table>
    </div>

    <div class="callout callout-warning">
      <span class="callout-icon">⚠️</span>
      <div class="callout-content">
        <strong>Quy tắc vàng</strong>
        • ☀️ <b>Trời nóng:</b> quạt chỉ làm mát <b>VỀ 50°</b> — không thể xuống dưới.<br>
        • 🌧️ <b>Trời mưa:</b> quạt làm mát <b>XUỐNG DƯỚI 50°</b> — nguy cơ hạ thân nhiệt!
      </div>
    </div>

    <h3>♻️ Cơ chế nhặt rác hồi máu</h3>
    <p>Bỏ rác vào <strong style="color: #10b981;">Thùng Rác Xanh</strong> (góc dưới phải sân) sẽ <strong>hồi HP</strong>:</p>

    <div class="table-wrap">
      <table>
        <thead>
          <tr>
            <th>Số rác</th>
            <th>HP hồi thường</th>
            <th>HP hồi (Bảo Ngọc × 1.5)</th>
          </tr>
        </thead>
        <tbody>
          <tr><td>1 rác</td><td>+4 HP</td><td>+6 HP</td></tr>
          <tr><td>3 rác</td><td>+12 HP</td><td>+18 HP</td></tr>
          <tr><td><strong>5 rác (đầy túi)</strong></td><td><strong>+25 HP</strong> (bonus +5)</td><td><strong>+38 HP</strong></td></tr>
        </tbody>
      </table>
    </div>

    <h3>🌿 Cơ chế giảm ô nhiễm</h3>
    <p>Càng dọn nhiều rác → ngày mai càng <strong>ít khả năng có thời tiết Ô nhiễm</strong>:</p>

    <div class="table-wrap">
      <table>
        <thead>
          <tr>
            <th>Rác dọn hôm qua</th>
            <th>Giảm ô nhiễm</th>
            <th>Xác suất Ô nhiễm ngày mai</th>
          </tr>
        </thead>
        <tbody>
          <tr><td>0 rác</td><td>0%</td><td>35%</td></tr>
          <tr><td>5 rác</td><td>25%</td><td>26%</td></tr>
          <tr><td>10 rác</td><td>50%</td><td>17%</td></tr>
          <tr><td><strong>12+ rác</strong></td><td><strong>60% (tối đa)</strong></td><td><strong>14% (thấp nhất)</strong></td></tr>
        </tbody>
      </table>
    </div>

    <h3>🔇 Minigame "Giữ im lặng"</h3>
    <div class="callout callout-tip">
      <span class="callout-icon">🎯</span>
      <div class="callout-content">
        Trong mỗi tiết học, cô giáo nhắc nhở học sinh tập trung:
        <ul style="margin: 10px 0 0 20px; color: #cbd5e1;">
          <li>⏱️ Cứ <strong>10 giây</strong>, có <strong>80% cơ hội</strong> minigame xuất hiện</li>
          <li>🎯 Nhấn <strong>SPACE / CLICK / TAP</strong> khi kim trượt vào <strong style="color: #10b981;">vùng xanh</strong></li>
          <li>✅ Vùng xanh rộng: nhân vật <strong>Gia Uy</strong> (40%) — dễ hơn</li>
          <li>❌ Trượt 3 lần: mất <strong style="color: #ef4444;">10 HP</strong> + cô giáo khiển trách</li>
        </ul>
      </div>
    </div>
  </section>

  <!-- ==========================================================
       NHÂN VẬT
  ========================================================== -->
  <section id="nhanvat">
    <h2>🎭 BỐN NHÂN VẬT</h2>
    <p>Mỗi nhân vật có <strong>tạo hình riêng biệt</strong> và <strong>kỹ năng đặc biệt</strong>:</p>

    <div class="char-grid">
      <div class="char-card" style="--char-color: #f97316;">
        <div class="char-avatar">🏃</div>
        <div class="char-name">GIA HƯNG</div>
        <div class="char-role">Học sinh Năng động</div>
        <div class="char-skill">🏃 Tốc độ +20%</div>
        <div class="char-traits">Cao · Cân đối · Tóc ngắn</div>
      </div>

      <div class="char-card" style="--char-color: #34d399;">
        <div class="char-avatar">♻️</div>
        <div class="char-name">BẢO NGỌC</div>
        <div class="char-role">Cán bộ Lớp Xanh</div>
        <div class="char-skill">♻️ Hồi +8 HP/ngày</div>
        <div class="char-traits">Nữ · Thấp · Mảnh mai · <strong>Tóc dài</strong></div>
      </div>

      <div class="char-card" style="--char-color: #fbbf24;">
        <div class="char-avatar">🛡️</div>
        <div class="char-name">MINH THÁI</div>
        <div class="char-role">Đội viên Cờ đỏ</div>
        <div class="char-skill">🛡️ Chống chịu tốt</div>
        <div class="char-traits"><strong>Cao nhất · To con</strong></div>
      </div>

      <div class="char-card" style="--char-color: #38bdf8;">
        <div class="char-avatar">💻</div>
        <div class="char-name">GIA UY</div>
        <div class="char-role">CLB Tin Học</div>
        <div class="char-skill">💻 Quạt ×2 · Minigame dễ</div>
        <div class="char-traits">Cao · <strong>Đeo kính</strong></div>
      </div>
    </div>
  </section>

  <!-- ==========================================================
       MULTIPLAYER
  ========================================================== -->
  <section id="multiplayer">
    <h2>👥 CHƠI NHÓM ONLINE</h2>
    <p>
      Game hỗ trợ <strong>multiplayer realtime</strong> qua
      <strong style="color: #fb923c;">Firebase Realtime Database</strong> — không cần tự dựng server,
      chơi được với bạn bè ở bất kỳ đâu.
    </p>

    <h3>📋 Các bước chơi nhóm</h3>
    <div class="schedule-diagram">
<pre><span class="break">┌─────────────────┐</span>                              <span class="lesson">┌─────────────────┐</span>
<span class="break">│   CHỦ PHÒNG     │</span>                              <span class="lesson">│    BẠN BÈ       │</span>
<span class="break">├─────────────────┤</span>                              <span class="lesson">├─────────────────┤</span>
<span class="break">│ 1. 👥 Online    │</span>                              <span class="lesson">│ 1. 👥 Online    │</span>
<span class="break">│ 2. 🎮 Tạo phòng │</span> ──── Chia sẻ mã ────→        <span class="lesson">│ 2. 🔗 Vào phòng │</span>
<span class="break">│ 3. Nhận mã 6 KT │</span>      (Zalo/Mess)              <span class="lesson">│ 3. Nhập mã      │</span>
<span class="break">│ 4. ▶ Bắt đầu    │</span> ←───── Tham gia ─────         <span class="lesson">│ 4. Chờ bắt đầu  │</span>
<span class="break">└─────────────────┘</span>                              <span class="lesson">└─────────────────┘</span></pre>
    </div>

    <h3>🔄 Tính năng đồng bộ</h3>
    <div class="feature-list">
      <li>Vị trí (x, y) của mọi người chơi</li>
      <li>Hướng nhìn: trái / phải / lên / xuống</li>
      <li>Animation đi bộ, animation quạt tay</li>
      <li>Trạng thái ngồi ghế, cầm rác, quạt tay</li>
      <li>Hành động: tắt đèn, bật quạt, mở cửa, nhặt rác</li>
      <li>Thanh nhiệt độ của đồng đội</li>
      <li>Tiến trình tiết học / giờ ra chơi</li>
      <li>Thời tiết và thời khóa biểu chung</li>
    </div>
  </section>

  <!-- ==========================================================
       ĐỒ HỌA
  ========================================================== -->
  <section id="graphics">
    <h2>🎨 ĐỒ HỌA PIXEL ART</h2>

    <h3>🏫 Bản đồ trường học</h3>
    <p>Bản đồ được <strong>tái hiện từ ảnh chụp thật</strong> của trường THPT Bình Chánh:</p>

    <div class="card-grid">
      <div class="card">
        <span class="card-icon">🏫</span>
        <div class="card-title">Dãy nhà chính</div>
        <div class="card-desc">2 tầng, mái ngói đỏ, 12 cửa sổ, hàng hiên 12 cột</div>
      </div>
      <div class="card">
        <span class="card-icon">🚩</span>
        <div class="card-title">Cột cờ</div>
        <div class="card-desc">Ở giữa sân, cờ đỏ sao vàng bay theo gió</div>
      </div>
      <div class="card">
        <span class="card-icon">🌳</span>
        <div class="card-title">Cây xanh</div>
        <div class="card-desc">6 cây 2 bên sân trường</div>
      </div>
      <div class="card">
        <span class="card-icon">🌸</span>
        <div class="card-title">Bồn hoa</div>
        <div class="card-desc">2 bồn hoa trước sân</div>
      </div>
      <div class="card">
        <span class="card-icon">🛡️</span>
        <div class="card-title">Bốt bảo vệ</div>
        <div class="card-desc">Góc dưới trái</div>
      </div>
      <div class="card">
        <span class="card-icon">♻️</span>
        <div class="card-title">Thùng rác xanh</div>
        <div class="card-desc">Góc dưới phải</div>
      </div>
      <div class="card">
        <span class="card-icon">🚰</span>
        <div class="card-title">Cống thoát nước</div>
        <div class="card-desc">2 cống trên sân</div>
      </div>
      <div class="card">
        <span class="card-icon">📚</span>
        <div class="card-title">3 lớp học</div>
        <div class="card-desc">10A3, 11A3, 12A3 với bàn ghế</div>
      </div>
    </div>

    <h3>👤 Nhân vật pixel</h3>
    <p>Mỗi nhân vật có <strong>bộ thông số tạo hình riêng</strong>:</p>

    <div class="table-wrap">
      <table>
        <thead>
          <tr>
            <th>Thuộc tính</th>
            <th>Giá trị</th>
            <th>Ý nghĩa</th>
          </tr>
        </thead>
        <tbody>
          <tr><td><code>height</code></td><td>0.92 → 1.28</td><td>Chiều cao (thấp → cao)</td></tr>
          <tr><td><code>width</code></td><td>0.92 → 1.22</td><td>Vóc dáng (mảnh → to)</td></tr>
          <tr><td><code>hasLongHair</code></td><td>true / false</td><td>Có tóc dài không (chỉ Bảo Ngọc)</td></tr>
          <tr><td><code>hasGlasses</code></td><td>true / false</td><td>Có đeo kính không (chỉ Gia Uy)</td></tr>
          <tr><td><code>skin, hair, shirt, pants</code></td><td>Hex colors</td><td>Màu da, tóc, áo, quần</td></tr>
        </tbody>
      </table>
    </div>
  </section>

  <!-- ==========================================================
       CÀI ĐẶT
  ========================================================== -->
  <section id="caidat">
    <h2>🚀 CÀI ĐẶT VÀ CHẠY</h2>

    <div class="callout callout-info">
      <span class="callout-icon">📋</span>
      <div class="callout-content">
        <strong>Yêu cầu hệ thống</strong>
        • Trình duyệt hiện đại hỗ trợ ES6+, Canvas 2D<br>
        • Kết nối Internet (để load Firebase SDK và Google Fonts)
      </div>
    </div>

    <h3>🔧 Các bước cài đặt</h3>
    <div class="steps">

      <div class="step">
        <div class="step-title">Clone repository</div>
        <div class="step-desc">Mở terminal và chạy lệnh sau:</div>
        <div class="code-wrap">
          <button class="copy-btn" onclick="copyCode(this)">Copy</button>
          <pre><code>git clone https://github.com/hihiquan2010/GreenProject.git
cd GreenProject</code></pre>
        </div>
      </div>

      <div class="step">
        <div class="step-title">Tạo Firebase Project</div>
        <div class="step-desc">
          1. Truy cập <a href="https://console.firebase.google.com/" target="_blank" style="color: #60a5fa;">Firebase Console</a><br>
          2. Bấm <strong>Add project</strong> → Đặt tên (VD: <code>cfg-eco-thptbc</code>) → <strong>Create</strong><br>
          3. Menu trái: <strong>Build</strong> → <strong>Realtime Database</strong> → <strong>Create Database</strong><br>
          4. Chọn location <strong>Singapore</strong> → <strong>Start in Test mode</strong> → <strong>Enable</strong><br>
          5. Vào tab <strong>Rules</strong>, paste đoạn JSON sau rồi <strong>Publish</strong>:
        </div>
        <div class="code-wrap">
          <button class="copy-btn" onclick="copyCode(this)">Copy</button>
          <pre><code>{
  "rules": {
    "rooms": {
      "$roomCode": {
        ".read": true,
        ".write": true
      }
    }
  }
}</code></pre>
        </div>
      </div>

      <div class="step">
        <div class="step-title">Lấy Firebase Config</div>
        <div class="step-desc">
          1. <strong>Project Settings</strong> (icon ⚙️) → tab <strong>General</strong><br>
          2. Kéo xuống <strong>Your apps</strong> → chọn <strong>Web</strong> (icon <code>&lt;/&gt;</code>)<br>
          3. Đặt nickname → <strong>Register app</strong><br>
          4. Copy đoạn <code>firebaseConfig</code>:
        </div>
        <div class="code-wrap">
          <button class="copy-btn" onclick="copyCode(this)">Copy</button>
          <pre><code>const firebaseConfig = {
  apiKey: "AIzaSy...",
  authDomain: "your-project.firebaseapp.com",
  databaseURL: "https://your-project-default-rtdb.asia-southeast1.firebasedatabase.app",
  projectId: "your-project",
  storageBucket: "your-project.appspot.com",
  messagingSenderId: "123456789",
  appId: "1:123456789:web:abcdef"
};</code></pre>
        </div>
      </div>

      <div class="step">
        <div class="step-title">Thay config vào index.html</div>
        <div class="step-desc">
          Mở file <code>index.html</code>, tìm dòng có chú thích <code>// ⚠️ THAY CONFIG FIREBASE CỦA BẠN VÀO ĐÂY</code>, thay bằng config vừa copy ở Bước 3.
        </div>
      </div>

      <div class="step">
        <div class="step-title">Deploy lên GitHub Pages</div>
        <div class="step-desc">Chạy lệnh sau để push code lên GitHub:</div>
        <div class="code-wrap">
          <button class="copy-btn" onclick="copyCode(this)">Copy</button>
          <pre><code>git add index.html
git commit -m "Setup Firebase config"
git push origin main</code></pre>
        </div>
        <div class="step-desc" style="margin-top: 12px;">
          Sau đó vào <strong>Settings → Pages → Source: main → Save</strong>. <br>
          Sau 1-2 phút, truy cập: <a href="https://hihiquan2010.github.io/GreenProject/" target="_blank" style="color: #10b981;">https://hihiquan2010.github.io/GreenProject/</a>
        </div>
      </div>

    </div>
  </section>

  <!-- ==========================================================
       ĐIỀU KHIỂN
  ========================================================== -->
  <section id="dieukhien">
    <h2>🎯 ĐIỀU KHIỂN</h2>

    <h3>💻 Trên máy tính</h3>
    <div class="table-wrap">
      <table>
        <thead>
          <tr><th>Phím</th><th>Chức năng</th></tr>
        </thead>
        <tbody>
          <tr><td><code>WASD</code> hoặc <code>↑↓←→</code></td><td>Di chuyển nhân vật</td></tr>
          <tr><td><code>E</code></td><td>Tương tác (nhặt rác, công tắc, mở cửa, nói chuyện)</td></tr>
          <tr><td><code>F</code> hoặc <code>Space</code></td><td>Quạt tay / Ngồi ghế</td></tr>
          <tr><td><code>SPACE</code></td><td>Nhấn trong minigame "Giữ im lặng"</td></tr>
        </tbody>
      </table>
    </div>

    <h3>📱 Trên điện thoại</h3>
    <p>Game hỗ trợ <strong>cảm ứng đa điểm</strong> với giao diện được thiết kế riêng:</p>

    <div class="table-wrap">
      <table>
        <thead>
          <tr><th>Nút</th><th>Vị trí</th><th>Chức năng</th></tr>
        </thead>
        <tbody>
          <tr><td>🕹️ <strong>Joystick ảo</strong></td><td>Góc trái</td><td>Di chuyển 360°</td></tr>
          <tr><td>🅴 <strong>Nút E</strong></td><td>Góc phải</td><td>Tương tác</td></tr>
          <tr><td>🅵 <strong>Nút F</strong></td><td>Góc phải</td><td>Quạt tay</td></tr>
          <tr><td>🪑 <strong>Nút ghế</strong></td><td>Góc phải</td><td>Ngồi / Đứng dậy</td></tr>
          <tr><td>⚙️ <strong>Nút menu</strong></td><td>Góc phải</td><td>Mở hướng dẫn</td></tr>
        </tbody>
      </table>
    </div>
  </section>

  <!-- ==========================================================
       CÔNG NGHỆ
  ========================================================== -->
  <section id="congnghe">
    <h2>🛠️ CÔNG NGHỆ SỬ DỤNG</h2>

    <div class="table-wrap">
      <table>
        <thead>
          <tr>
            <th>Thành phần</th>
            <th>Công nghệ</th>
            <th>Ghi chú</th>
          </tr>
        </thead>
        <tbody>
          <tr><td><strong>Frontend</strong></td><td>HTML5, CSS3, Vanilla JS</td><td>Không dùng framework</td></tr>
          <tr><td><strong>Đồ họa</strong></td><td>Canvas 2D API</td><td><code>image-rendering: pixelated</code></td></tr>
          <tr><td><strong>Âm thanh</strong></td><td>Web Audio API</td><td>Procedural synthesis (không cần file MP3)</td></tr>
          <tr><td><strong>Multiplayer</strong></td><td>Firebase Realtime DB 10.12.0</td><td>Sync realtime, free tier</td></tr>
          <tr><td><strong>Fonts</strong></td><td>Press Start 2P, Lexend</td><td>Google Fonts</td></tr>
          <tr><td><strong>Hosting</strong></td><td>GitHub Pages</td><td>Miễn phí, HTTPS sẵn</td></tr>
        </tbody>
      </table>
    </div>

    <div class="callout callout-success">
      <span class="callout-icon">⚡</span>
      <div class="callout-content">
        <strong>Ưu điểm thiết kế</strong>
        Game chạy <strong>mượt trên điện thoại tầm trung</strong> vì không dùng framework nặng,
        mọi asset đều được <strong>vẽ bằng Canvas procedural</strong>.
      </div>
    </div>
  </section>

  <!-- ==========================================================
       CẤU TRÚC
  ========================================================== -->
  <section id="cautruc">
    <h2>📁 CẤU TRÚC DỰ ÁN</h2>

    <div class="code-wrap">
      <button class="copy-btn" onclick="copyCode(this)">Copy</button>
      <pre><code>GreenProject/
│
├── index.html          # ⭐ Toàn bộ game (single-file)
├── README.md           # 📄 File này (dạng Markdown)
├── README.html         # 🌐 File này (dạng HTML đẹp)
├── LICENSE             # 📜 GNU GPL v3.0
└── .gitignore          # (tuỳ chọn)</code></pre>
    </div>

    <p>Game được thiết kế theo kiểu <strong>single-file</strong> để dễ deploy, chia sẻ và bảo trì. Mọi thứ — từ logic, đồ họa, âm thanh — đều nằm trong <strong>một file <code>index.html</code> duy nhất</strong>.</p>
  </section>

  <!-- ==========================================================
       GIÁO DỤC
  ========================================================== -->
  <section id="giaoduc">
    <h2>🎓 MỤC ĐÍCH GIÁO DỤC</h2>
    <p>Đây là một dự án game có <strong>giá trị giáo dục cao</strong>, hướng đến việc nâng cao ý thức bảo vệ môi trường cho học sinh THPT:</p>

    <div class="table-wrap">
      <table>
        <thead>
          <tr>
            <th>Bài học</th>
            <th>Thể hiện trong game</th>
          </tr>
        </thead>
        <tbody>
          <tr><td>♻️ <strong>Phân loại rác</strong></td><td>Nhặt rác và bỏ đúng vào Thùng Xanh</td></tr>
          <tr><td>⚡ <strong>Tiết kiệm điện</strong></td><td>Tắt đèn, quạt khi ra khỏi lớp</td></tr>
          <tr><td>🌿 <strong>Giảm ô nhiễm</strong></td><td>Dọn rác để ngày mai bầu trời trong xanh</td></tr>
          <tr><td>💧 <strong>Giữ vệ sinh</strong></td><td>Thông cống, tránh vũng nước</td></tr>
          <tr><td>🧘 <strong>Tập trung</strong></td><td>Minigame giữ im lặng trong giờ học</td></tr>
          <tr><td>👥 <strong>Trách nhiệm tập thể</strong></td><td>Chơi nhóm, cùng sinh tồn</td></tr>
        </tbody>
      </table>
    </div>

    <div class="callout callout-success">
      <span class="callout-icon">🌱</span>
      <div class="callout-content">
        <strong>Triết lý thiết kế</strong>
        Mỗi hành động nhỏ đều có <strong>tác động đến ngày mai</strong> — đây là bài học về
        <strong>trách nhiệm cá nhân với môi trường tập thể</strong>.
      </div>
    </div>
  </section>

  <!-- ==========================================================
       ĐÓNG GÓP
  ========================================================== -->
  <section id="donggop">
    <h2>🤝 ĐÓNG GÓP</h2>
    <p>Mọi đóng góp — dù nhỏ — đều được hoan nghênh!</p>

    <h3>Quy trình đóng góp</h3>
    <div class="code-wrap">
      <button class="copy-btn" onclick="copyCode(this)">Copy</button>
      <pre><code># 1. Fork repository trên GitHub
# 2. Clone bản fork của bạn
git clone https://github.com/YOUR_USERNAME/GreenProject.git
cd GreenProject

# 3. Tạo branch mới
git checkout -b feature/tinh-nang-moi

# 4. Commit thay đổi
git add .
git commit -m "feat: thêm tính năng X"

# 5. Push lên fork của bạn
git push origin feature/tinh-nang-moi

# 6. Mở Pull Request trên GitHub</code></pre>
    </div>

    <h3>💡 Ý tưởng phát triển</h3>
    <div class="feature-list">
      <li>🏫 Thêm nhiều lớp học hơn (10A1, 11A2, 12A3)</li>
      <li>🌱 Minigame phụ: trồng cây, tưới hoa</li>
      <li>🎉 Boss cuối tuần: "Ngày hội môi trường"</li>
      <li>🏆 Hệ thống thành tích (achievements)</li>
      <li>👥 Chế độ co-op nhiều đội thi đua</li>
      <li>📊 Bảng xếp hạng online</li>
      <li>🌍 Thêm bản đồ các trường khác</li>
      <li>🎵 Nhạc nền theo ngày/đêm</li>
    </div>
  </section>

  <!-- ==========================================================
       TÁC GIẢ
  ========================================================== -->
  <section id="tacgia">
    <h2>👨‍💻 TÁC GIẢ</h2>

    <div class="author-box">
      <div class="author-avatar">🍪</div>
      <div class="author-info">
        <div class="author-name">COOKIE</div>
        <div class="author-role">Thành viên CLB Tin Học — Trường THPT Bình Chánh</div>
        <div class="author-links">
          <a href="mailto:uyp079658@gmail.com" class="author-link">
            📧 uyp079658@gmail.com
          </a>
          <a href="https://github.com/hihiquan2010" class="author-link" target="_blank">
            🐙 @hihiquan2010
          </a>
        </div>
      </div>
    </div>

    <div class="callout callout-tip">
      <span class="callout-icon">🏆</span>
      <div class="callout-content">
        <strong>Hội thi CLB Tin Học 2026–2027</strong>
        Chủ đề: <em>"Lập Trình Vì Ngôi Trường Xanh"</em>
      </div>
    </div>
  </section>

  <!-- ==========================================================
       LICENSE
  ========================================================== -->
  <section id="license">
    <h2>📜 GIẤY PHÉP — GNU GPL v3.0</h2>

    <div style="text-align: center; margin: 20px 0;">
      <div style="font-family: 'Press Start 2P', monospace; font-size: 12px; color: #facc15; letter-spacing: 2px;">
        GNU GENERAL PUBLIC LICENSE
      </div>
      <div style="font-family: 'Press Start 2P', monospace; font-size: 24px; color: #facc15; margin-top: 8px;">
        v3.0
      </div>
    </div>

    <div class="license-box">
      <pre><code>Code for Green School: Eco Survival
Copyright (C) 2026  Cookie &amp; CLB Tin Học THPT Bình Chánh

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see &lt;https://www.gnu.org/licenses/&gt;.</code></pre>
    </div>

    <h3>✅ Quyền lợi</h3>
    <div class="table-wrap">
      <table>
        <thead>
          <tr><th>Quyền</th><th>Mô tả</th></tr>
        </thead>
        <tbody>
          <tr><td>✅ <strong>Sử dụng</strong></td><td>Cho mục đích cá nhân, giáo dục, thương mại</td></tr>
          <tr><td>✅ <strong>Nghiên cứu</strong></td><td>Đọc, tìm hiểu mã nguồn</td></tr>
          <tr><td>✅ <strong>Sửa đổi</strong></td><td>Chỉnh sửa, tùy biến theo nhu cầu</td></tr>
          <tr><td>✅ <strong>Phân phối</strong></td><td>Chia sẻ bản gốc hoặc bản sửa đổi</td></tr>
        </tbody>
      </table>
    </div>

    <h3>⚠️ Điều kiện bắt buộc</h3>
    <div class="table-wrap">
      <table>
        <thead>
          <tr><th>Điều kiện</th><th>Mô tả</th></tr>
        </thead>
        <tbody>
          <tr><td>📢 <strong>Ghi nguồn</strong></td><td>Nêu rõ tác giả gốc (Cookie + CLB Tin Học THPT Bình Chánh)</td></tr>
          <tr><td>📄 <strong>Giữ giấy phép</strong></td><td>Không được đổi giấy phép GPL v3.0 khi phân phối lại</td></tr>
          <tr><td>🔓 <strong>Mở mã nguồn</strong></td><td>Nếu phát hành bản sửa đổi, phải công khai source code</td></tr>
          <tr><td>⚠️ <strong>Không bảo hành</strong></td><td>Tác giả không chịu trách nhiệm nếu có lỗi</td></tr>
        </tbody>
      </table>
    </div>

    <h3>🔗 Liên kết</h3>
    <div class="feature-list">
      <li><a href="https://www.gnu.org/licenses/gpl-3.0" target="_blank" style="color: #60a5fa;">Website GPL v3.0</a></li>
      <li><a href="https://www.gnu.org/licenses/gpl-3.0.txt" target="_blank" style="color: #60a5fa;">Toàn văn GPL v3.0</a></li>
    </div>

    <div class="callout callout-warning">
      <span class="callout-icon">💡</span>
      <div class="callout-content">
        <strong>Lưu ý</strong>
        Tạo file <code>LICENSE</code> riêng bằng cách copy toàn văn từ
        <a href="https://www.gnu.org/licenses/gpl-3.0.txt" target="_blank" style="color: #fbbf24;">đây</a>
        và lưu vào thư mục gốc dự án.
      </div>
    </div>
  </section>

  <!-- ==========================================================
       CẢM ƠN
  ========================================================== -->
  <section id="thanks">
    <h2>🙏 LỜI CẢM ƠN</h2>
    <p>Dự án này không thể hoàn thành nếu thiếu sự hỗ trợ của:</p>

    <div class="thanks-grid">
      <div class="thanks-item">
        <span class="thanks-icon">🌱</span>
        <div><strong>Ban giám hiệu THPT Bình Chánh</strong><br><span style="font-size: 12px; color: #94a3b8;">Nguồn cảm hứng từ ngôi trường thật</span></div>
      </div>
      <div class="thanks-item">
        <span class="thanks-icon">💚</span>
        <div><strong>Thầy cô CLB Tin Học</strong><br><span style="font-size: 12px; color: #94a3b8;">Hướng dẫn và hỗ trợ</span></div>
      </div>
      <div class="thanks-item">
        <span class="thanks-icon">👥</span>
        <div><strong>Các bạn học sinh</strong><br><span style="font-size: 12px; color: #94a3b8;">Người chơi và tester nhiệt tình</span></div>
      </div>
      <div class="thanks-item">
        <span class="thanks-icon">🎨</span>
        <div><strong>Cộng đồng pixel art VN</strong><br><span style="font-size: 12px; color: #94a3b8;">Nguồn cảm hứng đồ họa</span></div>
      </div>
      <div class="thanks-item">
        <span class="thanks-icon">🔥</span>
        <div><strong>Firebase</strong><br><span style="font-size: 12px; color: #94a3b8;">Backend miễn phí cho multiplayer</span></div>
      </div>
      <div class="thanks-item">
        <span class="thanks-icon">📚</span>
        <div><strong>Cộng đồng mã nguồn mở</strong><br><span style="font-size: 12px; color: #94a3b8;">Kiến thức chia sẻ vô giá</span></div>
      </div>
    </div>
  </section>

  <!-- ==========================================================
       FOOTER
  ========================================================== -->
  <footer>
    <h2>🌱 HÃY CHƠI, HỌC VÀ LAN TỎA TINH THẦN SỐNG XANH! 🌱</h2>
    <div class="quote">"Lập Trình Vì Ngôi Trường Xanh"</div>
    <div class="club">CLB TIN HỌC THPT BÌNH CHÁNH — NH 2026–2027</div>

    <div class="star-cta">
      <a href="https://github.com/hihiquan2010/GreenProject" target="_blank">
        ⭐ STAR REPOSITORY
      </a>
    </div>

    <div class="made-in">
      Made with 💚 in Vietnam
    </div>
  </footer>

</div>

<!-- Back to top -->
<button class="back-to-top" id="backToTop" onclick="window.scrollTo({top: 0, behavior: 'smooth'})">▲</button>

<script>
  // ==========================================================
  // COPY CODE
  // ==========================================================
  function copyCode(btn) {
    const pre = btn.parentElement.querySelector('pre code');
    const text = pre.innerText;

    navigator.clipboard.writeText(text).then(() => {
      const originalText = btn.textContent;
      btn.textContent = '✓ Đã copy!';
      btn.classList.add('copied');
      setTimeout(() => {
        btn.textContent = originalText;
        btn.classList.remove('copied');
      }, 1500);
    }).catch(() => {
      // Fallback for older browsers
      const ta = document.createElement('textarea');
      ta.value = text;
      document.body.appendChild(ta);
      ta.select();
      document.execCommand('copy');
      document.body.removeChild(ta);
      btn.textContent = '✓ Đã copy!';
      btn.classList.add('copied');
      setTimeout(() => {
        btn.textContent = 'Copy';
        btn.classList.remove('copied');
      }, 1500);
    });
  }

  // ==========================================================
  // BACK TO TOP
  // ==========================================================
  const backToTop = document.getElementById('backToTop');
  window.addEventListener('scroll', () => {
    if (window.scrollY > 400) {
      backToTop.classList.add('visible');
    } else {
      backToTop.classList.remove('visible');
    }
  });

  // ==========================================================
  // SMOOTH SCROLL FOR TOC LINKS
  // ==========================================================
  document.querySelectorAll('.toc-list a').forEach(link => {
    link.addEventListener('click', (e) => {
      e.preventDefault();
      const targetId = link.getAttribute('href').substring(1);
      const target = document.getElementById(targetId);
      if (target) {
        target.scrollIntoView({ behavior: 'smooth', block: 'start' });
      }
    });
  });

  // ==========================================================
  // ANIMATE SECTIONS ON SCROLL
  // ==========================================================
  const observerOptions = {
    threshold: 0.05,
    rootMargin: '0px 0px -50px 0px'
  };

  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.style.opacity = '1';
        entry.target.style.transform = 'translateY(0)';
      }
    });
  }, observerOptions);

  document.querySelectorAll('section').forEach(section => {
    section.style.opacity = '0';
    section.style.transform = 'translateY(20px)';
    section.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
    observer.observe(section);
  });

  // Immediately show first section
  setTimeout(() => {
    document.querySelectorAll('section')[0].style.opacity = '1';
    document.querySelectorAll('section')[0].style.transform = 'translateY(0)';
  }, 100);
</script>

</body>
</html>
