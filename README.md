
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Шашлыки с Мирой Шан · большое приключение</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Segoe UI', 'Montserrat', system-ui, sans-serif;
    }

    body {
      background: #b8d8e3; /* легкий голубой фон на случай просвечивания */
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    /* общий контейнер сайта */
    .site-wrapper {
      max-width: 1200px;
      width: 100%;
      background: white; /* подложка, поверх накладываются цветные секции */
      box-shadow: 0 0 50px rgba(0, 0, 0, 0.1);
    }

    /* СЕКЦИЯ 1: про Миру Шан (светло‑голубой + светло‑розовый) */
    .mira-section {
      background: linear-gradient(145deg, #fbe9f0 0%, #fbe9f0 30%, #d4eaf7 70%, #d4eaf7 100%);
      /* плавный переход от розового к голубому */
      padding: 4rem 2rem;
      border-bottom: 4px dashed #ffaaa0;
    }

    .mira-container {
      max-width: 1000px;
      margin: 0 auto;
    }

    .mira-title {
      font-size: 4.2rem;
      font-weight: 900;
      color: #992c5c;
      text-shadow: 3px 3px 0 #ffd9df;
      letter-spacing: 3px;
      line-height: 1.1;
      margin-bottom: 0.5rem;
    }

    .mira-sub {
      font-size: 1.8rem;
      color: #1d6381;
      background: rgba(255, 255, 255, 0.7);
      display: inline-block;
      padding: 0.5rem 2rem;
      border-radius: 60px;
      backdrop-filter: blur(4px);
      margin-bottom: 2rem;
      border: 3px solid white;
    }

    .mira-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 2rem;
      margin-top: 2rem;
    }

    .mira-card {
      flex: 1 1 250px;
      background: rgba(255, 255, 255, 0.6);
      backdrop-filter: blur(6px);
      border-radius: 48px;
      padding: 2rem 1.5rem;
      box-shadow: 0 15px 0 rgba(190, 140, 170, 0.3);
      border: 2px solid white;
    }

    .mira-card h3 {
      font-size: 2rem;
      color: #ad3f76;
      margin-bottom: 1rem;
      border-bottom: 3px dotted #ffbcd6;
      padding-bottom: 0.5rem;
    }

    .mira-card p {
      font-size: 1.2rem;
      color: #133e50;
      margin-bottom: 0.5rem;
      font-weight: 500;
    }

    .cosplay-badge {
      background: #ffe5b4;
      color: #a1416b;
      font-size: 1.5rem;
      font-weight: 800;
      padding: 1rem 2rem;
      border-radius: 60px;
      display: inline-block;
      border: 4px solid white;
      box-shadow: 0 8px 0 #b3829e;
      margin: 2rem 0 0;
      text-align: center;
      width: fit-content;
    }

    .cosplay-badge span {
      font-size: 2rem;
      background: white;
      padding: 0.2rem 1rem;
      border-radius: 40px;
      margin-left: 1rem;
      color: #1f6b8b;
    }

    /* СЕКЦИЯ 2: зелёное меню + билеты */
    .green-section {
      background: #1d4d3a; /* глубокий зелёный фон */
      padding: 4rem 2rem;
      border-top: 8px solid #b5e6a2;
      color: #f4f7e0;
    }

    .green-container {
      max-width: 1000px;
      margin: 0 auto;
    }

    .menu-header {
      font-size: 3.8rem;
      font-weight: 800;
      color: #ffecaa;
      text-shadow: 5px 5px 0 #2f6b4a;
      margin-bottom: 2rem;
      border-left: 15px solid #c3e3a0;
      padding-left: 1.5rem;
    }

    /* две колонки: меню и напитки */
    .menu-row {
      display: flex;
      flex-wrap: wrap;
      gap: 2rem;
      margin-bottom: 3rem;
    }

    .menu-col {
      flex: 2;
      min-width: 300px;
    }

    .drinks-col {
      flex: 1;
      min-width: 220px;
      background: #356b4b;
      border-radius: 64px 64px 30px 30px;
      padding: 2rem 1.8rem;
      border: 4px solid #b1d89b;
    }

    .menu-item {
      background: #296344;
      border-radius: 40px 40px 25px 25px;
      padding: 1.2rem 1.8rem;
      margin-bottom: 1rem;
      display: flex;
      align-items: center;
      gap: 1rem;
      flex-wrap: wrap;
      border: 2px solid #b1d470;
      box-shadow: 0 7px 0 #1d402b;
    }

    .menu-name {
      font-size: 1.9rem;
      font-weight: 700;
      color: #ffdd9e;
      min-width: 200px;
    }

    .menu-desc {
      font-size: 1.2rem;
      color: #e3ffcd;
      background: #1d4d31;
      padding: 0.3rem 1rem;
      border-radius: 40px;
    }

    .drinks-title {
      font-size: 2.3rem;
      color: #ffeeb5;
      border-bottom: 4px wavy #c7fc9d;
      margin-bottom: 1.5rem;
    }

    .drink-item {
      font-size: 1.7rem;
      padding: 0.6rem 0;
      border-bottom: 2px dashed #7bb877;
      display: flex;
      gap: 0.5rem;
    }

    .drink-item:before {
      content: "🥤";
      margin-right: 0.5rem;
    }

    /* Кнопка / место под ссылку на билеты */
    .ticket-box {
      background: #fbebb0;
      border-radius: 90px;
      padding: 2rem 2.5rem;
      margin-top: 3rem;
      text-align: center;
      border: 5px solid #9dcd7c;
      box-shadow: 0 15px 0 #58855f;
    }

    .ticket-box p {
      font-size: 2.2rem;
      font-weight: 800;
      color: #1a4b2d;
    }

    .ticket-box .placeholder-link {
      background: #1d3e2c;
      color: #ffeca2;
      font-size: 2rem;
      padding: 0.5rem 2rem;
      border-radius: 50px;
      display: inline-block;
      margin: 1rem 0 0.5rem;
      border: 3px dashed #f8ffc4;
      font-family: monospace;
      word-break: break-word;
    }

    .ticket-box small {
      font-size: 1.3rem;
      color: #353d1f;
      display: block;
    }

    /* сельдерейные тэги */
    .celery-badge {
      background: #98c779;
      color: #17381f;
      font-weight: 600;
      padding: 0.3rem 1.2rem;
      border-radius: 30px;
      font-size: 1.1rem;
      border: 2px solid #f5ffc0;
    }

    footer {
      background: #1c2b1c;
      color: #b4cba4;
      text-align: center;
      padding: 1.5rem;
      font-size: 1.1rem;
    }

    /* адаптация */
    @media (max-width: 700px) {
      .mira-title { font-size: 3rem; }
      .menu-header { font-size: 2.8rem; }
    }
  </style>
</head>
<body>
  <div class="site-wrapper">
    <!-- ЧАСТЬ 1: светлые тона (розовый+голубой) про Миру Шан -->
    <section class="mira-section">
      <div class="mira-container">
        <h1 class="mira-title">ШАШЛЫКИ<br>с Мирой Шан</h1>
        <div class="mira-sub">🌸 особенное событие весны 🌸</div>

        <div class="mira-grid">
          <div class="mira-card">
            <h3>Кто такая Мира?</h3>
            <p>🌿 блогерша, косплеерша и ценительница шашлыков</p>
            <p>🎤 КАРАОКЕ!!!</p>
            <p>📸 каждый гость попадёт в её сторис (если захочет)</p>
          </div>
          <div class="mira-card">
            <h3>формат встречи</h3>
            <p>🔥пикник с мангалом</p>
            <p>🌳просторная поляна </p>
            <p>🎶пение песен до заката</p>
          </div>
        </div>

        <!-- Косплей-скидка (жирный блок) -->
        <div class="cosplay-badge">
          ⚡ ЛЮДИ В КОСПЛЕЕ — СКИДКА 20% ⚡
          <span>👘🎭</span>
        </div>
        <p style="color:#4f2860; margin-top:1rem; font-size:1.4rem; background: rgba(255,255,240,0.7); padding:0.5rem 2rem; border-radius:40px; width: fit-content;">
           приходите в образе — удивите Миру!
        </p>
      </div>
    </section>

    <!-- ЧАСТЬ 2: зелёное меню (ВСЁ с сельдереем) и напитки -->
    <section class="green-section">
      <div class="green-container">
        <h2 class="menu-header">🍴 меню «Сельдерей-стайл»</h2>

        <div class="menu-row">
          <!-- Левая колонка: основные блюда -->
          <div class="menu-col">
            <!-- Шашлык из курицы -->
            <div class="menu-item">
              <span class="menu-name">🍗 шашлык из курицы</span>
              <span class="menu-desc"> курица с сельдереем в маринаде</span>
              <span class="celery-badge"> #сельдерей</span>
            </div>
            <!-- Шашлык из свинины -->
            <div class="menu-item">
              <span class="menu-name">🥩 шашлык из свинины</span>
              <span class="menu-desc">свинина с хрустящим сельдереем и травами</span>
              <span class="celery-badge"> #сельдерей</span>
            </div>
            <!-- Овощи гриль -->
            <div class="menu-item">
              <span class="menu-name">🌽 овощи гриль</span>
              <span class="menu-desc">кабачки, перцы + стебли сельдерея</span>
              <span class="celery-badge"> #сельдерей</span>
            </div>
            <!-- Сельдерей на мангале (целая позиция) -->
            <div class="menu-item">
              <span class="menu-name">🔥 сельдерей на мангале</span>
              <span class="menu-desc">целые стебли с пряным маслом</span>
              <span class="celery-badge"> #звезда вечера</span>
            </div>
            <!-- Бутерброд с сельдереем -->
            <div class="menu-item">
              <span class="menu-name">🥪 бутерброд с сельдереем</span>
              <span class="menu-desc">белый хлеб, сливочный сыр, тонкий сельдерей</span>
              <span class="celery-badge"> #сельдерей</span>
            </div>
            <!-- Сельдереевый сок (свежевыжатый) -->
            <div class="menu-item">
              <span class="menu-name">🧃 сельдереевый сок</span>
              <span class="menu-desc">фреш из стеблей и яблока</span>
              <span class="celery-badge"> #Detox</span>
            </div>
            <!-- Сельдерей в кляре -->
            <div class="menu-item">
              <span class="menu-name">🥨 сельдерей в кляре</span>
              <span class="menu-desc">хрустящие палочки сельдерея с соусом цезарь</span>
              <span class="celery-badge"> #сельдерей</span>
            </div>
            <!-- Добавим ещё один сельдерейный штрих (для счёта) -->
            <div class="menu-item">
              <span class="menu-name">🌿 сельдерей по-корейски</span>
              <span class="menu-desc">пряный, острый, в дополнение к мясу</span>
              <span class="celery-badge"> #сельдерей</span>
            </div>
          </div>

          <!-- Правая колонка: напитки (квас, вода, сок, чай) -->
          <div class="drinks-col">
            <div class="drinks-title">НАПИТКИ</div>
            <div class="drink-item">Квас (бочка)</div>
            <div class="drink-item">Вода (газ./негаз.)</div>
            <div class="drink-item">Сок (яблоко/апельсин/мультифрукт)</div>
            <div class="drink-item">Чай (черный, зеленый)</div>
            <div style="margin-top:2rem; background:#4d805d; border-radius:30px; padding:1rem; color:#fff2b3; font-size:1.4rem; border:3px solid #a2d686;">
              🌿 все напитки можно дополнить сельдереем 
            </div>
          </div>
        </div>

     
        <div class="ticket-box">
          <p>🎟️ БИЛЕТЫ НА СОБЫТИЕ</p>
          <!-- именно здесь вы вставите свою ссылку -->
          <div class="placeholder-link">
            *здесь будет ссылка на покупку билетов*
          </div>
          <small>👇 скопируйте свою ссылку и замените этот текст</small>
          <p style="font-size:1.5rem; margin-top:1rem;">👥 косплей-скидка действует при входе</p>
        </div>

        <!-- напоминание про сельдерей везде -->
        <p style="text-align:center; color:#b9f09b; font-size:1.5rem; margin-top:2rem;">
          ☘️ абсолютно всё в меню содержит сельдерей (даже чай можно попросить с палочкой сельдерея) ☘️
        </p>
      </div>
    </section>

    <!-- подвал с чисто техническим названием (без упоминания Миры лишнего) -->
    <footer>
      <p>Шашлыки с Мирой Шан · мероприятие для своих · сельдерей правит миром</p>
      <p style="font-size:0.9rem;">*название не является рекламой конкретного человека, только вдохновение</p>
    </footer>
  </div>
</body>
</html>
