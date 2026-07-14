[entrance-book.html](https://github.com/user-attachments/files/30003702/entrance-book.html)
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Entrance Book | 採用情報・会社紹介</title>
  <style>
    /* ==========================================================================
       Reset & Base Styles
       ========================================================================== */
    *, *::before, *::after {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, "Hiragino Kaku Gothic ProN", "Hiragino Sans", Meiryo, sans-serif;
      color: #1a1a1a;
      background-color: #fafbfe;
      line-height: 1.8;
      -webkit-font-smoothing: antialiased;
    }

    a {
      color: inherit;
      text-decoration: none;
      transition: all 0.2s ease;
    }

    /* ==========================================================================
       Layout (Desktop Split Screen)
       ========================================================================== */
    .container {
      display: flex;
      min-height: 100vh;
    }

    /* Left Sidebar - Fixed */
    .sidebar {
      width: 340px;
      background-color: #ffffff;
      border-right: 1px solid #eef2f6;
      position: fixed;
      top: 0;
      bottom: 0;
      left: 0;
      padding: 48px 40px;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      z-index: 100;
    }

    .brand {
      margin-bottom: 48px;
    }

    .brand-logo {
      display: flex;
      align-items: center;
      gap: 12px;
      font-weight: 800;
      font-size: 22px;
      color: #0f172a;
      letter-spacing: -0.5px;
    }

    .brand-logo svg {
      width: 32px;
      height: 32px;
      fill: #2563eb;
    }

    .brand-subtitle {
      font-size: 12px;
      color: #64748b;
      margin-top: 4px;
      font-weight: 500;
      letter-spacing: 1px;
      text-transform: uppercase;
    }

    /* Navigation */
    .nav-menu {
      flex-grow: 1;
    }

    .nav-menu ul {
      list-style: none;
    }

    .nav-menu li {
      margin-bottom: 8px;
    }

    .nav-menu a {
      display: flex;
      align-items: center;
      gap: 12px;
      padding: 12px 16px;
      font-size: 15px;
      font-weight: 600;
      color: #64748b;
      border-radius: 8px;
    }

    .nav-menu a:hover {
      color: #2563eb;
      background-color: #f1f5f9;
    }

    .nav-menu a.active {
      color: #2563eb;
      background-color: #eff6ff;
    }

    .sidebar-footer {
      font-size: 12px;
      color: #94a3b8;
      border-top: 1px solid #f1f5f9;
      padding-top: 24px;
    }

    /* Right Content - Scrollable */
    .main-content {
      margin-left: 340px;
      flex-grow: 1;
      padding: 80px 8% 120px 8%;
      max-width: 1100px;
    }

    /* ==========================================================================
       Typography & Section Styles
       ========================================================================== */
    .section {
      padding-top: 40px;
      margin-bottom: 120px;
    }

    .section-header {
      margin-bottom: 32px;
    }

    .section-tag {
      font-size: 12px;
      font-weight: 700;
      color: #2563eb;
      text-transform: uppercase;
      letter-spacing: 1.5px;
      display: inline-block;
      margin-bottom: 8px;
    }

    .section-title {
      font-size: 32px;
      font-weight: 800;
      color: #0f172a;
      letter-spacing: -0.5px;
    }

    .lead-text {
      font-size: 18px;
      color: #475569;
      margin-bottom: 24px;
      font-weight: 500;
    }

    p {
      color: #475569;
      font-size: 16px;
      margin-bottom: 16px;
    }

    /* ==========================================================================
       Components
       ========================================================================== */
    /* Hero Banner Placeholder */
    .hero-banner {
      background: linear-gradient(135deg, #1e293b 0%, #0f172a 100%);
      border-radius: 16px;
      padding: 60px 48px;
      color: #ffffff;
      margin-bottom: 60px;
      position: relative;
      overflow: hidden;
    }

    .hero-banner::after {
      content: "";
      position: absolute;
      top: -50%;
      right: -20%;
      width: 400px;
      height: 400px;
      background: radial-gradient(circle, rgba(37,99,235,0.15) 0%, rgba(0,0,0,0) 70%);
      border-radius: 50%;
    }

    .hero-tag {
      background: rgba(255, 255, 255, 0.1);
      padding: 4px 12px;
      border-radius: 20px;
      font-size: 12px;
      font-weight: 600;
      display: inline-block;
      margin-bottom: 16px;
      backdrop-filter: blur(4px);
    }

    .hero-title {
      font-size: 38px;
      font-weight: 800;
      line-height: 1.3;
      margin-bottom: 16px;
    }

    .hero-desc {
      font-size: 16px;
      color: #cbd5e1;
      max-width: 600px;
    }

    /* Cards Grid (Culture) */
    .grid-2 {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 24px;
      margin-top: 32px;
    }

    .card {
      background: #ffffff;
      border: 1px solid #eef2f6;
      border-radius: 12px;
      padding: 32px;
      transition: all 0.3s ease;
    }

    .card:hover {
      transform: translateY(-4px);
      box-shadow: 0 12px 24px rgba(15, 23, 42, 0.04);
      border-color: #e2e8f0;
    }

    .card-icon {
      width: 48px;
      height: 48px;
      background-color: #eff6ff;
      border-radius: 10px;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-bottom: 20px;
    }

    .card-icon svg {
      width: 24px;
      height: 24px;
      fill: #2563eb;
    }

    .card-title {
      font-size: 18px;
      font-weight: 700;
      color: #0f172a;
      margin-bottom: 12px;
    }

    .card-desc {
      font-size: 14px;
      color: #64748b;
      line-height: 1.6;
    }

    /* Team Members List */
    .member-list {
      display: flex;
      flex-direction: column;
      gap: 20px;
    }

    .member-item {
      display: flex;
      align-items: center;
      gap: 24px;
      background: #ffffff;
      border: 1px solid #eef2f6;
      border-radius: 12px;
      padding: 24px;
    }

    .member-avatar {
      width: 80px;
      height: 80px;
      border-radius: 50%;
      background-color: #e2e8f0;
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: 700;
      color: #64748b;
      flex-shrink: 0;
    }

    .member-info {
      flex-grow: 1;
    }

    .member-meta {
      display: flex;
      align-items: center;
      gap: 12px;
      margin-bottom: 6px;
    }

    .member-role {
      font-size: 12px;
      font-weight: 700;
      color: #2563eb;
      background: #eff6ff;
      padding: 2px 8px;
      border-radius: 4px;
    }

    .member-name {
      font-size: 18px;
      font-weight: 700;
      color: #0f172a;
    }

    .member-quote {
      font-size: 14px;
      color: #475569;
      font-style: italic;
    }

    /* Jobs List */
    .jobs-list {
      display: flex;
      flex-direction: column;
      gap: 16px;
    }

    .job-card {
      background: #ffffff;
      border: 1px solid #eef2f6;
      border-radius: 12px;
      padding: 24px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      transition: all 0.2s ease;
    }

    .job-card:hover {
      border-color: #cbd5e1;
      transform: translateX(4px);
    }

    .job-title {
      font-size: 18px;
      font-weight: 700;
      color: #0f172a;
      margin-bottom: 8px;
    }

    .job-tags {
      display: flex;
      gap: 8px;
    }

    .job-tag {
      font-size: 12px;
      color: #64748b;
      background: #f1f5f9;
      padding: 4px 10px;
      border-radius: 6px;
      font-weight: 500;
    }

    .job-apply-btn {
      background-color: #0f172a;
      color: #ffffff;
      padding: 10px 20px;
      border-radius: 8px;
      font-size: 14px;
      font-weight: 600;
    }

    .job-apply-btn:hover {
      background-color: #2563eb;
    }

    /* ==========================================================================
       Responsive Styles
       ========================================================================== */
    @media (max-width: 992px) {
      .container {
        flex-direction: column;
      }

      .sidebar {
        position: relative;
        width: 100%;
        height: auto;
        border-right: none;
        border-bottom: 1px solid #eef2f6;
        padding: 32px 24px;
      }

      .brand {
        margin-bottom: 24px;
      }

      .nav-menu ul {
        display: flex;
        flex-wrap: wrap;
        gap: 8px;
      }

      .nav-menu li {
        margin-bottom: 0;
      }

      .nav-menu a {
        padding: 8px 16px;
        font-size: 14px;
      }

      .sidebar-footer {
        display: none; /* Hide standard footer in mobile sidebar */
      }

      .main-content {
        margin-left: 0;
        padding: 48px 24px;
      }

      .hero-banner {
        padding: 40px 24px;
      }

      .hero-title {
        font-size: 28px;
      }

      .grid-2 {
        grid-template-columns: 1fr;
      }

      .member-item {
        flex-direction: column;
        align-items: flex-start;
        gap: 16px;
      }

      .job-card {
        flex-direction: column;
        align-items: flex-start;
        gap: 16px;
      }

      .job-apply-btn {
        width: 100%;
        text-align: center;
      }
    }
  </style>
</head>
<body>

  <div class="container">
    <!-- Left Sidebar (Fixed) -->
    <aside class="sidebar">
      <div class="brand">
        <div class="brand-logo">
          <!-- Inline SVG Icon for Brand -->
          <svg viewBox="0 0 24 24">
            <path d="M12 2L2 22h20L12 2zm0 3.99L19.53 19H4.47L12 5.99zM13 16h-2v2h2v-2zm0-6h-2v4h2v-4z"/>
          </svg>
          <span>ITANDI Style</span>
        </div>
        <div class="brand-subtitle">Entrance Book</div>
      </div>

      <nav class="nav-menu">
        <ul>
          <li><a href="#about" class="active">私たちについて</a></li>
          <li><a href="#culture">カルチャー</a></li>
          <li><a href="#member">メンバー</a></li>
          <li><a href="#jobs">募集職種</a></li>
        </ul>
      </nav>

      <div class="sidebar-footer">
        <p>© 2026 ITANDI Style Inc.</p>
      </div>
    </aside>

    <!-- Right Main Content -->
    <main class="main-content">
      <!-- Welcome Hero Banner -->
      <div class="hero-banner">
        <span class="hero-tag">Welcome to Our Team</span>
        <h1 class="hero-title">テクノロジーの力で、<br>社会の仕組みをなめらかに。</h1>
        <p class="hero-desc">ITANDI Styleの入社案内（Entrance Book）へようこそ。私たちは、業界の常識をテクノロジーでアップデートする仲間を探しています。</p>
      </div>

      <!-- About Section -->
      <section id="about" class="section">
        <div class="section-header">
          <span class="section-tag">About Us</span>
          <h2 class="section-title">私たちについて</h2>
        </div>
        <p class="lead-text">産業のインフラ、そして個人の暮らしを支える仕組みを、より効率的で滑らかなものへと作り変えます。</p>
        <p>私たちの使命は、複雑で不透明なプロセスをシンプルに解きほぐし、すべてのステークホルダーがストレスなく情報やサービスにアクセスできる基盤を構築することです。最新のテクノロジー、ユーザー視点に寄り添ったUX、そしてデータ駆動型のソリューションを掛け合わせることで、新しい時代のスタンダードを創出します。</p>
      </section>

      <!-- Culture Section -->
      <section id="culture" class="section">
        <div class="section-header">
          <span class="section-tag">Culture</span>
          <h2 class="section-title">カルチャー＆バリュー</h2>
        </div>
        <p class="lead-text">私たちが日常の業務や意思決定において大切にしている、コアとなる3つの行動指針です。</p>
        
        <div class="grid-2">
          <!-- Card 1 -->
          <div class="card">
            <div class="card-icon">
              <svg viewBox="0 0 24 24"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm1 15h-2v-6h2v6zm0-8h-2V7h2v2z"/></svg>
            </div>
            <h3 class="card-title">Flat & Open</h3>
            <p class="card-desc">役職や職種、年齢にとらわれず、誰もが率直に意見を交わし合えるフラットなチームです。情報は原則としてオープンに共有されます。</p>
          </div>

          <!-- Card 2 -->
          <div class="card">
            <div class="card-icon">
              <svg viewBox="0 0 24 24"><path d="M13 10V3L4 14h7v7l9-11h-7z"/></svg>
            </div>
            <h3 class="card-title">Speed & Agility</h3>
            <p class="card-desc">素早い仮説検証を最も重視します。完璧な計画よりも、小さく実行して素早く学ぶサイクルを回し、変化へ柔軟に適応します。</p>
          </div>

          <!-- Card 3 -->
          <div class="card">
            <div class="card-icon">
              <svg viewBox="0 0 24 24"><path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42 4.42 3 7.5 3c1.74 0 3.41.81 4.5 2.09C13.09 3.81 14.76 3 16.5 3 19.58 3 22 5.42 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/></svg>
            </div>
            <h3 class="card-title">User Centric</h3>
            <p class="card-desc">すべてのプロダクトはユーザーのために。真の課題はどこにあるのか、常にユーザーの声と行動データに深く向き合い設計します。</p>
          </div>

          <!-- Card 4 -->
          <div class="card">
            <div class="card-icon">
              <svg viewBox="0 0 24 24"><path d="M12 12c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm0 2c-2.67 0-8 1.34-8 4v2h16v-2c0-2.66-5.33-4-8-4z"/></svg>
            </div>
            <h3 class="card-title">Professional Autonomy</h3>
            <p class="card-desc">メンバー一人ひとりが自律したプロフェッショナルとして、大きな裁量と責任を持って挑戦の意思決定を推進します。</p>
          </div>
        </div>
      </section>

      <!-- Member Section -->
      <section id="member" class="section">
        <div class="section-header">
          <span class="section-tag">Members</span>
          <h2 class="section-title">働くメンバー</h2>
        </div>
        <p class="lead-text">それぞれの分野で高い専門性を持った多様なメンバーが協働しています。</p>

        <div class="member-list">
          <div class="member-item">
            <div class="member-avatar">E.T</div>
            <div class="member-info">
              <div class="member-meta">
                <span class="member-name">田中 栄治</span>
                <span class="member-role">Software Engineer</span>
              </div>
              <p class="member-quote">「モダンな技術選定と、複雑なビジネス要件をコードに落とし込む仕事に大きなやりがいを感じています。裁量が大きく成長できる環境です。」</p>
            </div>
          </div>

          <div class="member-item">
            <div class="member-avatar">M.S</div>
            <div class="member-info">
              <div class="member-meta">
                <span class="member-name">佐藤 美咲</span>
                <span class="member-role">Product Designer</span>
              </div>
              <p class="member-quote">「単なる美しさではなく、複雑な仕組みをいかにシンプルにユーザーに届けるか、エンジニアやPMと毎日徹底的に議論しながら創っています。」</p>
            </div>
          </div>
        </div>
      </section>

      <!-- Jobs Section -->
      <section id="jobs" class="section">
        <div class="section-header">
          <span class="section-tag">Job Openings</span>
          <h2 class="section-title">現在募集中の職種</h2>
        </div>
        <p class="lead-text">事業の急成長に伴い、全ポジションで積極採用を行っています。</p>

        <div class="jobs-list">
          <div class="job-card">
            <div>
              <h3 class="job-title">フロントエンドエンジニア (React / Next.js)</h3>
              <div class="job-tags">
                <span class="job-tag">正社員</span>
                <span class="job-tag">リモート可</span>
                <span class="job-tag">東京オフィス</span>
              </div>
            </div>
            <a href="#" class="job-apply-btn">詳細を見る</a>
          </div>

          <div class="job-card">
            <div>
              <h3 class="job-title">サーバーサイドエンジニア (Go / Python)</h3>
              <div class="job-tags">
                <span class="job-tag">正社員</span>
                <span class="job-tag">フレックスタイム</span>
                <span class="job-tag">東京オフィス</span>
              </div>
            </div>
            <a href="#" class="job-apply-btn">詳細を見る</a>
          </div>

          <div class="job-card">
            <div>
              <h3 class="job-title">プロダクトマネージャー (PM)</h3>
              <div class="job-tags">
                <span class="job-tag">正社員</span>
                <span class="job-tag">リモート可</span>
                <span class="job-tag">東京オフィス</span>
              </div>
            </div>
            <a href="#" class="job-apply-btn">詳細を見る</a>
          </div>
        </div>
      </section>
    </main>
  </div>

  <script>
    // Smooth navigation active link switching on scroll
    const sections = document.querySelectorAll(".section");
    const navLinks = document.querySelectorAll(".nav-menu a");

    window.addEventListener("scroll", () => {
      let current = "";
      sections.forEach((section) => {
        const sectionTop = section.offsetTop;
        const sectionHeight = section.clientHeight;
        if (pageYOffset >= sectionTop - 150) {
          current = section.getAttribute("id");
        }
      });

      navLinks.forEach((link) => {
        link.classList.remove("active");
        if (link.getAttribute("href").includes(current)) {
          link.classList.add("active");
        }
      });
    });
  </script>
</body>
</html>
