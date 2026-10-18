<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>LifeOS — Планер</title>
    <meta name="theme-color" content="#F5F2EB">
    <meta name="apple-mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-status-bar-style" content="default">
    <meta name="apple-mobile-web-app-title" content="LifeOS">
    <link rel="apple-touch-icon" href="https://cdn-icons-png.flaticon.com/512/2965/2965358.png">
    <link rel="manifest" href="manifest.json">
    <script src="https://unpkg.com/@phosphor-icons/web"></script>
    <script src="https://cdn.jsdelivr.net/npm/apexcharts"></script>
    <link href="https://fonts.googleapis.com/css2?family=DM+Sans:opsz,wght@9..40,400;9..40,500;9..40,600;9..40,700&family=Playfair+Display:ital,wght@0,600;1,600&display=swap" rel="stylesheet">
    
    <style>
        :root { --bg: #F5F2EB; --surface: #FFFFFF; --surface-soft: #FDFCFA; --text: #2C2A29; --text-muted: #8C857D; --accent: #C48B73; --accent-hover: #B37961; --accent-light: #F3EAE5; --border: #EBE6DD; --shadow: 0 10px 40px -10px rgba(44, 42, 41, 0.05); --radius: 24px; --radius-sm: 12px; --good: #7B9C83; --good-bg: #EDF2EE; --bad: #C76D6D; --bad-bg: #F8EEEE; --warn: #D4A373; --warn-bg: #F9F2E9; --note-color: #7B8B9C; --note-bg: #EEF2F5; --overlay: rgba(44, 42, 41, 0.4); }
        [data-theme="dark"] { --bg: #181716; --surface: #242221; --surface-soft: #1C1B1A; --text: #F0ECE6; --text-muted: #948E87; --accent: #D19A82; --accent-hover: #E0B29C; --accent-light: #332B28; --border: #383431; --shadow: 0 10px 40px -10px rgba(0, 0, 0, 0.3); --good: #8AB595; --good-bg: #26302A; --bad: #D18A8A; --bad-bg: #332323; --warn: #E0B58C; --warn-bg: #332C24; --note-color: #9CAAB8; --note-bg: #2A2F33; --overlay: rgba(0, 0, 0, 0.6); }
        * { box-sizing: border-box; margin: 0; padding: 0; -webkit-tap-highlight-color: transparent; }
        body { background-color: var(--bg); color: var(--text); font-family: 'DM Sans', sans-serif; min-height: 100vh; transition: background 0.4s, color 0.4s; -webkit-font-smoothing: antialiased; }
        h1, h2, h3, .logo-text { font-family: 'Playfair Display', serif; font-weight: 600; }
        
        #authScreen, #paymentScreen { position: fixed; inset: 0; background: var(--bg); z-index: 9999; display: flex; align-items: center; justify-content: center; padding: 20px; overflow-y: auto; }
        .auth-box { background: var(--surface); padding: 40px; border-radius: var(--radius); box-shadow: var(--shadow); width: 100%; max-width: 400px; text-align: center; margin: auto; }
        .pricing-box { background: var(--surface); padding: 40px; border-radius: var(--radius); box-shadow: var(--shadow); width: 100%; max-width: 800px; text-align: center; margin: auto; }
        .auth-box h2, .pricing-box h2 { font-size: 28px; margin-bottom: 10px; color: var(--accent); }
        .auth-box p, .pricing-box p { color: var(--text-muted); margin-bottom: 30px; font-size: 14px; }
        .auth-input { width: 100%; padding: 15px; margin-bottom: 15px; border-radius: var(--radius-sm); border: 1px solid var(--border); background: var(--surface-soft); color: var(--text); font-size: 16px; outline: none; font-family: inherit; }
        .auth-btn { width: 100%; padding: 15px; border-radius: var(--radius-sm); background: var(--accent); color: #fff; border: none; font-size: 16px; font-weight: 600; cursor: pointer; transition: 0.2s; font-family: inherit; display: flex; align-items: center; justify-content: center; gap: 8px; }
        .auth-btn.outline { background: transparent; border: 1px solid var(--border); color: var(--text); margin-top: 10px; }
        .auth-error { color: var(--bad); font-size: 13px; margin-top: 10px; display: none; }
        #loadingText { color: var(--accent); font-size: 14px; margin-top: 15px; display: none; }
        
        .tariffs-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(160px, 1fr)); gap: 20px; margin-top: 30px; }
        .tariff-card { background: var(--surface-soft); border: 2px solid var(--border); border-radius: var(--radius-sm); padding: 25px 15px; cursor: pointer; transition: 0.3s; position: relative; }
        .tariff-card:hover { border-color: var(--accent); transform: translateY(-5px); }
        .tariff-name { font-size: 18px; font-weight: 700; margin-bottom: 10px; }
        .tariff-price { font-size: 24px; font-weight: 800; color: var(--accent); }
        .tariff-days { font-size: 13px; color: var(--text-muted); margin-top: 5px; }
        
        #appContainer { display: none; flex-direction: column; max-width: 1200px; margin: 0 auto; padding: 40px 20px; gap: 32px; }
        header { display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 20px; }
        .logo { font-size: 28px; display: flex; align-items: center; gap: 12px; color: var(--text); cursor: pointer; user-select: none; }
        .logo i { color: var(--accent); font-size: 32px; }
        .nav-tabs { display: flex; gap: 8px; background: var(--surface); padding: 6px; border-radius: 100px; box-shadow: var(--shadow); overflow-x: auto; }
        .nav-btn { border: none; background: transparent; padding: 12px 24px; border-radius: 100px; font-size: 14px; font-weight: 600; color: var(--text-muted); cursor: pointer; transition: all 0.3s ease; display: flex; align-items: center; gap: 8px; font-family: inherit; white-space: nowrap; }
        .nav-btn.active { background: var(--accent); color: #fff; }
        .actions { display: flex; gap: 12px; }
        .icon-btn { background: var(--surface); border: 1px solid var(--border); width: 44px; height: 44px; border-radius: 50%; cursor: pointer; color: var(--text); font-size: 20px; display: flex; align-items: center; justify-content: center; transition: all 0.3s ease; }
        .page { display: none; animation: slideUp 0.5s ease forwards; opacity: 0; flex-direction: column; gap: 32px; }
        .page.active { display: flex; }
        @keyframes slideUp { from { opacity: 0; transform: translateY(15px); } to { opacity: 1; transform: translateY(0); } }
        .card { background: var(--surface); border-radius: var(--radius); padding: 32px; box-shadow: var(--shadow); border: 1px solid var(--border); }
        .card-title { font-size: 22px; margin-bottom: 24px; display: flex; justify-content: space-between; align-items: center; }
        
        .dash-header-stats { display: grid; grid-template-columns: repeat(4, 1fr); gap: 20px; }
        .stat-card { padding: 24px; border-radius: var(--radius); border: 1px solid var(--border); display: flex; flex-direction: column; gap: 12px; background: var(--surface); }
        .stat-card.good { background: var(--good-bg); border-color: transparent; }
        .stat-card.bad { background: var(--bad-bg); border-color: transparent; }
        .stat-card.warn { background: var(--warn-bg); border-color: transparent; }
        .stat-header { font-size: 14px; font-weight: 600; color: var(--text-muted); display: flex; align-items: center; gap: 8px; }
        .stat-value { font-size: 36px; font-weight: 700; }
        .ai-briefing { background: var(--surface); border-radius: var(--radius); padding: 32px; box-shadow: var(--shadow); border: 1px solid var(--border); position: relative; overflow: hidden; }
        .ai-briefing::before { content: ''; position: absolute; left: 0; top: 0; bottom: 0; width: 6px; background: var(--accent); }
        .charts-row { display: grid; grid-template-columns: 1fr 1fr; gap: 32px; }
        .chart-box { height: 260px; width: 100%; }
        
        .month-calendar { display: grid; grid-template-columns: repeat(7, 1fr); gap: 8px; }
        .cal-day-name { text-align: center; font-size: 12px; font-weight: 600; color: var(--text-muted); }
        .cal-cell { min-height: 100px; background: var(--surface-soft); border: 1px solid var(--border); border-radius: var(--radius-sm); padding: 8px; cursor: pointer; }
        .cal-cell.today { background: var(--good-bg); border: 2px solid var(--good); }
        .cal-date { font-weight: 600; font-size: 14px; }
        .cal-events-container { display: flex; flex-direction: column; gap: 3px; margin-top: 4px; }
        .cal-pill { font-size: 10px; padding: 3px 6px; border-radius: 6px; white-space: nowrap; overflow: hidden; text-overflow: ellipsis; font-weight: 600; }
        .week-grid { display: grid; grid-template-columns: repeat(12, 1fr); gap: 20px; align-items: start; }
        .day-col:nth-child(1), .day-col:nth-child(2), .day-col:nth-child(3), .day-col:nth-child(4) { grid-column: span 3; }
        .day-col:nth-child(5), .day-col:nth-child(6), .day-col:nth-child(7) { grid-column: span 4; }
        .day-col { background: var(--surface-soft); border-radius: var(--radius-sm); padding: 16px; display: flex; flex-direction: column; gap: 12px; border: 1px solid var(--border); }
        .circle-prog { width: 40px; height: 40px; border-radius: 50%; margin: 8px auto; display: flex; align-items: center; justify-content: center; font-size: 11px; font-weight: 700; background: conic-gradient(var(--accent) var(--p, 0%), var(--border) 0); position: relative; }
        .circle-prog::after { content: ''; position: absolute; width: 32px; height: 32px; background: var(--surface-soft); border-radius: 50%; }
        .circle-prog span { position: relative; z-index: 1; }
        .t-item { display: flex; flex-direction: column; gap: 6px; background: var(--surface); padding: 12px; border-radius: var(--radius-sm); border: 1px solid var(--border); margin-bottom: 8px; }
        .t-header { display: flex; gap: 8px; }
        .task-text { flex: 1; border: none; background: transparent; font-size: 14px; outline: none; color: var(--text); resize: none; overflow: hidden; line-height: 1.5; font-family: inherit; }
        .t-footer { display: flex; justify-content: space-between; align-items: center; border-top: 1px dashed var(--border); padding-top: 6px; margin-top: 4px; }
        .task-note-input { width: 100%; padding: 8px; font-size: 13px; background: var(--surface-soft); border: 1px solid var(--border); border-radius: 6px; resize: vertical; outline: none; margin-top: 6px; font-family: inherit; }

        /* Стили для привычек */
        .habits-header { display: grid; grid-template-columns: 1fr auto 24px; gap: 16px; align-items: center; margin-bottom: 16px; padding: 0 16px; }
        .h-days { display: grid; grid-template-columns: repeat(7, 36px); gap: 10px; }
        .h-day-label { width: 36px; text-align: center; font-size: 12px; font-weight: 600; color: var(--text-muted); }
        .habits-list { display: flex; flex-direction: column; gap: 12px; }
        .habit-row { display: grid; grid-template-columns: 1fr auto 24px; gap: 16px; align-items: center; padding: 16px; background: var(--surface-soft); border-radius: var(--radius-sm); border: 1px solid var(--border); }
        .habit-name { font-weight: 600; font-size: 15px; border: none; background: transparent; color: var(--text); outline: none; width: 100%; font-family: 'DM Sans', sans-serif; }
        .habit-days { display: grid; grid-template-columns: repeat(7, 36px); gap: 10px; }
        .h-check { width: 36px; height: 36px; border-radius: 10px; border: 2px solid var(--border); display: flex; align-items: center; justify-content: center; cursor: pointer; transition: all 0.2s ease; color: transparent; background: var(--surface); }
        .h-check:hover { border-color: var(--accent); }
        .h-check.checked { background: var(--accent); border-color: var(--accent); color: #fff; }
        .h-del { background: none; border: none; color: var(--text-muted); font-size: 20px; cursor: pointer; transition: 0.2s; }
        .h-del:hover { color: var(--bad); }
        .add-btn { background: transparent; border: 2px dashed var(--border); padding: 16px; border-radius: var(--radius-sm); font-weight: 600; color: var(--text-muted); cursor: pointer; transition: 0.2s; width: 100%; margin-top: 20px; font-size: 14px; font-family: 'DM Sans', sans-serif; }
        .add-btn:hover { border-color: var(--accent); color: var(--accent); background: var(--surface-soft); }
        
        .health-layout { display: grid; grid-template-columns: 1fr 1fr; gap: 32px; }
        .rating-scale { display: flex; gap: 8px; margin-bottom: 15px; }
        .rating-item { flex: 1; aspect-ratio: 1; border-radius: 12px; background: var(--surface-soft); border: 1px solid var(--border); display: flex; align-items: center; justify-content: center; cursor: pointer; font-size: 22px; opacity: 0.4; transition: 0.2s; user-select: none; }
        .rating-item.active { opacity: 1 !important; background: var(--accent); border-color: var(--accent); }
        .mindstream-input { width: 100%; min-height: 100px; padding: 15px; border-radius: var(--radius-sm); border: 1px solid var(--border); background: var(--surface); font-size: 15px; resize: vertical; outline: none; font-family: inherit; }
        .thought-list { display: flex; flex-direction: column; gap: 16px; margin-top: 15px; }
        .thought-card { background: var(--surface); padding: 20px; border-radius: var(--radius-sm); border: 1px solid var(--border); }
        .thought-date { font-size: 12px; font-weight: 700; color: var(--accent); margin-bottom: 8px; display: block; }
        .thought-text { font-size: 14px; line-height: 1.6; white-space: pre-wrap; }
        
        .modal-overlay { position: fixed; inset: 0; background: var(--overlay); backdrop-filter: blur(4px); display: none; align-items: center; justify-content: center; z-index: 10000; opacity: 0; transition: 0.3s; }
        .modal-overlay.active { display: flex; opacity: 1; }
        .modal-content { background: var(--surface); border-radius: var(--radius); padding: 32px; width: 100%; max-width: 500px; max-height: 90vh; overflow-y: auto; }
        .input-field { width: 100%; padding: 12px 16px; border-radius: var(--radius-sm); border: 1px solid var(--border); background: var(--surface-soft); margin-bottom: 10px; font-family: inherit; color: var(--text); outline: none; }
        
        #secretAdminPanel { position: fixed; inset: 0; background: var(--bg); z-index: 10000; display: none; flex-direction: column; padding: 30px; overflow-y: auto; }
        .admin-header { display: flex; justify-content: space-between; align-items: center; margin-bottom: 30px; }
        .admin-stats-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 20px; margin-bottom: 30px; }
        .admin-table { width: 100%; border-collapse: collapse; margin-top: 15px; font-size: 14px; background: var(--surface); border-radius: var(--radius-sm); overflow: hidden; }
        .admin-table th, .admin-table td { padding: 15px; text-align: left; border-bottom: 1px solid var(--border); }
        .admin-table th { background: var(--surface-soft); font-weight: 600; color: var(--text-muted); }
        .admin-btn { padding: 6px 10px; border-radius: 6px; border: none; cursor: pointer; font-weight: 600; font-size: 12px; margin-right: 5px; margin-bottom: 5px; }
        .admin-btn.green { background: var(--good); color: white; }
        .admin-btn.red { background: var(--bad); color: white; }
        .admin-btn.outline { background: transparent; border: 1px solid var(--border); color: var(--text); }
        .admin-btn.money { background: #f59e0b; color: white; }
        
        @media (max-width: 1024px) { .dash-header-stats { grid-template-columns: repeat(2, 1fr); } .charts-row, .health-layout { grid-template-columns: 1fr; } .week-grid { grid-template-columns: repeat(6, 1fr); } .day-col:nth-child(n) { grid-column: span 2; } }
        @media (max-width: 768px) { #appContainer { padding: 15px 10px; gap: 20px; } header { flex-direction: column; align-items: stretch; gap: 15px; } .logo { justify-content: center; font-size: 24px; } .nav-tabs { width: 100%; justify-content: space-between; } .nav-btn { padding: 10px 12px; font-size: 12px; flex: 1; justify-content: center; } .nav-btn i { font-size: 18px; } .actions { justify-content: center; } .card { padding: 20px 15px; border-radius: 16px; } .dash-header-stats { grid-template-columns: 1fr 1fr; gap: 10px; } .stat-card { padding: 15px; } .stat-value { font-size: 24px; } .week-grid { grid-template-columns: 1fr; gap: 15px; } .day-col:nth-child(n) { grid-column: span 1; } .rating-scale { gap: 4px; } .rating-item { font-size: 18px; border-radius: 8px; } .cal-cell { min-height: 70px; padding: 4px; } .cal-pill { display: none; } .auth-box, .pricing-box { padding: 25px 15px; } .tariffs-grid { grid-template-columns: 1fr 1fr; gap: 10px; } .admin-table th, .admin-table td { padding: 8px; font-size: 12px; } .habit-row, .habits-header { grid-template-columns: 1fr; justify-items: center; gap: 16px; } .h-days, .habit-days { justify-content: center; } }
    </style>
</head>
<body>

<!-- СКРЫТАЯ АДМИНКА -->
<div id="secretAdminPanel">
    <div class="admin-header">
        <h2 style="font-family:'Playfair Display'; color:var(--accent);">Admin Dashboard</h2>
        <button class="auth-btn outline" style="width:auto; padding:10px 20px;" onclick="closeSecretAdmin()">Закрыть</button>
    </div>
    <div class="admin-stats-grid">
        <div class="stat-card good"><div class="stat-header"><i class="ph ph-currency-rub"></i> Выручка</div><div class="stat-value" id="adminRevenue">0 ₽</div></div>
        <div class="stat-card neutral"><div class="stat-header"><i class="ph ph-users"></i> Юзеров</div><div class="stat-value" id="adminTotalUsers">0</div></div>
        <div class="stat-card warn"><div class="stat-header"><i class="ph ph-pulse"></i> Онлайн</div><div class="stat-value" id="adminOnline">0</div></div>
    </div>
    <div class="card" style="margin-bottom: 20px;">
        <div class="card-title">Пользователи</div>
        
        <input type="text" id="adminSearch" class="input-field" placeholder="🔍 Поиск по логину (email)..." oninput="filterAdminTable()" style="margin-bottom: 15px;">
        
        <div style="overflow-x:auto;">
            <table class="admin-table" id="adminUsersTable">
                <thead><tr><th>Email</th><th>Статус</th><th>До</th><th>Действия</th></tr></thead>
                <tbody></tbody>
            </table>
        </div>
    </div>
    <div class="card">
        <div class="card-title">Тарифы</div>
        <div id="pricingSettings" style="display:flex; flex-direction:column; gap:10px;"></div>
        <button class="auth-btn" style="margin-top:15px; width:auto; padding:10px 20px;" onclick="savePricingSettings()">Сохранить</button>
    </div>
</div>

<!-- МОДАЛЬНЫЕ ОКНА -->
<div class="modal-overlay" id="secretPasswordModal" style="z-index: 10005;">
    <div class="modal-content" style="text-align:center; max-width:300px;">
        <h3 style="margin-bottom:15px;">Access Denied</h3>
        <input type="password" id="secretPassInput" class="input-field" placeholder="Password" style="text-align:center; font-size:20px;">
        <button class="auth-btn" onclick="checkSecretPassword()">Enter</button>
    </div>
</div>

<div class="modal-overlay" id="paymentLogModal" style="z-index: 10005;">
    <div class="modal-content" style="text-align:center; max-width:300px;">
        <h3 style="margin-bottom:15px;">Сумма оплаты (₽)</h3>
        <input type="number" id="paymentAmountInput" class="input-field" placeholder="Например: 499" style="text-align:center; font-size:20px;">
        <input type="hidden" id="paymentUid">
        <input type="hidden" id="paymentDays">
        <button class="auth-btn" onclick="confirmPaymentLog()">Добавить и выдать дни</button>
        <button class="auth-btn outline" onclick="closeModal('paymentLogModal')">Отмена</button>
    </div>
</div>

<!-- ЭКРАН ВХОДА -->
<div id="authScreen">
    <div class="auth-box">
        <h2>LifeOS</h2>
        <p id="authSubtitle">Вход в облачный планер</p>
        <input type="email" id="loginInput" class="auth-input" placeholder="Email">
        <input type="password" id="passwordInput" class="auth-input" placeholder="Пароль">
        <button class="auth-btn" id="mainAuthBtn" onclick="handleAuth()">Войти</button>
        <button class="auth-btn outline" id="switchAuthBtn" onclick="toggleAuthMode()">Нет аккаунта? Зарегистрироваться</button>
        <div id="authError" class="auth-error"></div>
        <div id="loadingText">Загрузка...</div>
    </div>
</div>

<!-- ЭКРАН ТАРИФОВ -->
<div id="paymentScreen" style="display: none;">
    <div class="pricing-box">
        <h2>Доступ приостановлен</h2>
        <p>Выберите тариф для продолжения.</p>
        <div class="tariffs-grid" id="pricingGrid"></div>
        <button class="auth-btn outline" style="margin-top: 30px;" onclick="logoutUser()">Выйти</button>
    </div>
</div>

<!-- МОДАЛКА ОПЛАТЫ -->
<div class="modal-overlay" id="payModal">
    <div class="modal-content" style="text-align:center;">
        <h3 style="margin-bottom:15px; font-size:22px;">Оплата через Telegram</h3>
        <p style="margin-bottom:20px; color:var(--text-muted); font-size:14px;">Нажмите кнопку, чтобы открыть чат с готовым сообщением.</p>
        <a href="#" id="tgLink" target="_blank" class="auth-btn" style="background:#2AABEE; text-decoration:none;"><i class="ph ph-telegram-logo"></i> Написать в Telegram</a>
        <button class="auth-btn outline" style="margin-top:10px;" onclick="closeModal('payModal')">Закрыть</button>
    </div>
</div>

<!-- ОСНОВНОЕ ПРИЛОЖЕНИЕ -->
<div id="appContainer">
    <header>
        <div class="logo" id="mainLogo"><i class="ph ph-flower-lotus"></i> LifeOS</div>
        <nav class="nav-tabs">
            <button class="nav-btn active" onclick="switchPage('dashboard', this)"><i class="ph ph-squares-four"></i> Обзор</button>
            <button class="nav-btn" onclick="switchPage('planner', this)"><i class="ph ph-calendar-blank"></i> Планировщик</button>
            <button class="nav-btn" onclick="switchPage('health', this)"><i class="ph ph-sparkle"></i> Состояние</button>
        </nav>
        <div class="actions">
            <button class="icon-btn" onclick="toggleTheme()" id="themeBtn"><i class="ph ph-moon"></i></button>
            <button class="icon-btn" onclick="logoutUser()" title="Выйти"><i class="ph ph-sign-out"></i></button>
        </div>
    </header>
    
    <!-- ДАШБОРД -->
    <div id="page-dashboard" class="page active">
        <div class="dash-header-stats" id="dashStatsContainer"></div>
        <div class="ai-briefing"><h3><i class="ph ph-sparkle"></i> Утренний брифинг</h3><p id="aiBriefingText">Загрузка...</p></div>
        <div class="charts-row">
            <div class="card"><div class="card-title">Продуктивность</div><div id="chartTasks" class="chart-box"></div></div>
            <div class="card"><div class="card-title">Ресурсы</div><div id="chartHealth" class="chart-box"></div></div>
        </div>
    </div>
    
    <!-- ПЛАНИРОВЩИК -->
    <div id="page-planner" class="page">
        <div class="card" style="padding-bottom: 16px;">
            <div class="card-title" style="margin-bottom: 12px;"><span>Мой месяц</span>
                <div style="display:flex; gap:12px; align-items:center;">
                    <button class="icon-btn" style="width:28px; height:28px; box-shadow:none; border:none;" onclick="changeMonth(-1)"><i class="ph ph-caret-left"></i></button>
                    <span id="monthTitle" style="font-size:15px; font-weight:600;">Месяц</span>
                    <button class="icon-btn" style="width:28px; height:28px; box-shadow:none; border:none;" onclick="changeMonth(1)"><i class="ph ph-caret-right"></i></button>
                </div>
            </div>
            <div class="calendar-wrapper"><div class="month-calendar" id="monthCalendarGrid"></div></div>
        </div>
        
        <div class="card">
            <div class="card-title" style="margin:0 0 24px 0;">Задачи <span id="weekRangeTitle" style="font-size: 14px; font-weight: 500; color: var(--text-muted);"></span></div>
            <div class="week-grid" id="weekGrid"></div>
        </div>

        <!-- ВОЗВРАЩЕННЫЕ ПРИВЫЧКИ -->
        <div class="card">
            <div class="card-title">Ритуалы</div>
            <div class="habits-header">
                <div></div>
                <div class="h-days" id="habitDatesHeader"></div>
                <div></div>
            </div>
            <div class="habits-list" id="habitsList"></div>
            <button class="add-btn" onclick="addHabit()">+ Новый ритуал</button>
        </div>
    </div>
    
    <!-- ЗДОРОВЬЕ -->
    <div id="page-health" class="page">
        <div class="health-layout">
            <div class="card">
                <div class="card-title">Как вы сегодня?</div>
                <div class="metric-header"><span><i class="ph ph-moon"></i> Сон</span><span class="metric-val" id="vSleep">0 / 10</span></div><div class="rating-scale" id="rsSleep"></div>
                <div class="metric-header"><span><i class="ph ph-lightning"></i> Энергия</span><span class="metric-val" id="vEnergy">0 / 10</span></div><div class="rating-scale" id="rsEnergy"></div>
                <div class="metric-header"><span><i class="ph ph-smiley"></i> Настроение</span><span class="metric-val" id="vMood">0 / 10</span></div><div class="rating-scale" id="rsMood"></div>
                <div class="metric-header"><span><i class="ph ph-drop"></i> Вода</span><span class="metric-val" id="vWater">0 / 10</span></div><div class="rating-scale" id="rsWater"></div>
                <div class="metric-header"><span><i class="ph ph-apple"></i> Питание</span><span class="metric-val" id="vFood">0 / 10</span></div><div class="rating-scale" id="rsFood"></div>
                <div class="metric-header"><span><i class="ph ph-barbell"></i> Активность</span><span class="metric-val" id="vSport">0 / 10</span></div><div class="rating-scale" id="rsSport"></div>
            </div>
            <div style="display:flex; flex-direction:column; gap:32px;">
                <div class="health-ai-box ai-briefing"><h3><i class="ph ph-magic-wand"></i> Анализ</h3><div class="health-ai-text" id="healthAdviceText">Отметьте показатели.</div></div>
                <div class="card"><div class="card-title">Хроника разума</div><textarea class="mindstream-input" id="thoughtInput" placeholder="Запишите мысль..."></textarea><button class="auth-btn" style="margin-top:10px;" onclick="saveThought()">Сохранить</button><div class="thought-list" id="thoughtsList"></div></div>
            </div>
        </div>
    </div>
</div>

<!-- МОДАЛКИ ПЛАНЕРА -->
<div class="modal-overlay" id="dayModal"><div class="modal-content" style="text-align:left;"><div class="modal-header" style="display:flex; justify-content:space-between; margin-bottom:20px;"><div class="modal-title" id="dayModalTitle">Дата</div><button class="close-modal" onclick="closeModal('dayModal')" style="background:none; border:none; font-size:24px; cursor:pointer;"><i class="ph ph-x"></i></button></div><div style="display:flex; gap:10px; margin-bottom:20px;"><input type="text" class="input-field" id="dayNoteInput" placeholder="Заметка..."><button class="auth-btn" style="padding:0 20px; width:auto;" onclick="addDayNote()">ОК</button></div><div class="event-list" id="dayEventsList" style="display:flex; flex-direction:column; gap:10px;"></div></div></div>
<div class="modal-overlay" id="manageEventsModal"><div class="modal-content" style="text-align:left;"><div class="modal-header" style="display:flex; justify-content:space-between; margin-bottom:20px;"><div class="modal-title">Важные даты</div><button class="close-modal" onclick="closeModal('manageEventsModal')" style="background:none; border:none; font-size:24px; cursor:pointer;"><i class="ph ph-x"></i></button></div><input type="text" class="input-field" id="impEventTitle" placeholder="Название"><input type="date" class="input-field" id="impEventDate"><label style="display:flex; gap:10px; margin-bottom:15px; cursor:pointer;"><input type="checkbox" id="impEventRecurring" style="width:18px; height:18px;"> Повторять каждый год</label><button class="auth-btn" style="margin-bottom:20px;" onclick="addImportantEvent()">Добавить</button><div class="event-list" id="importantEventsList" style="display:flex; flex-direction:column; gap:10px;"></div></div></div>

<script type="module">
    import { initializeApp } from "https://www.gstatic.com/firebasejs/10.8.0/firebase-app.js";
    import { getAuth, signInWithEmailAndPassword, createUserWithEmailAndPassword, onAuthStateChanged, signOut } from "https://www.gstatic.com/firebasejs/10.8.0/firebase-auth.js";
    import { initializeFirestore, doc, getDoc, setDoc, getDocs, collection, updateDoc, addDoc } from "https://www.gstatic.com/firebasejs/10.8.0/firebase-firestore.js";

    const firebaseConfig = {
        apiKey: "AIzaSyCP_GulwcPv-hduiYpftMCvIe_FT8JF1qw",
        authDomain: "planner-new-e5dc0.firebaseapp.com",
        projectId: "planner-new-e5dc0",
        storageBucket: "planner-new-e5dc0.firebasestorage.app",
        messagingSenderId: "323185215674",
        appId: "1:323185215674:web:12b23ff1d76beb765a9a83",
        measurementId: "G-TVECLM8ML1"
    };

    const MASTER_EMAIL = "master@lifeos.com"; 
    const MASTER_PASS = "AdminMasterPassword123!";
    const SECRET_CODE = "4682"; 
    const TG_LINK = "https://t.me/Denkal39";

    const app = initializeApp(firebaseConfig);
    const auth = getAuth(app);
    const db = initializeFirestore(app, { experimentalForceLongPolling: true });

    let currentUserId = null;
    let currentUserData = null;
    let isRegisterMode = false;
    let isSecretAdminMode = false;

    let appData = { settings: { theme: 'light' }, tasks: {}, health: {}, mindstream: [], habits: [], dayNotes: {}, importantEvents: [] };
    let pricingPlans = [
        { id: 'p1', name: '3 дня', days: 3, price: 99 },
        { id: 'p2', name: '1 неделя', days: 7, price: 199 },
        { id: 'p3', name: '1 месяц', days: 30, price: 499 },
        { id: 'p4', name: '1 год', days: 365, price: 3990 }
    ];

    window.onerror = function(msg, url, line) { console.error("Глобальная ошибка:", msg, "в строке", line); };

    // ==========================================
    // СКРЫТАЯ АДМИНКА
    // ==========================================
    let clickCount = 0;
    let clickTimer;

    document.getElementById('mainLogo').addEventListener('click', () => {
        if (window.innerWidth < 1024) return;
        clickCount++;
        clearTimeout(clickTimer);
        clickTimer = setTimeout(() => { clickCount = 0; }, 500);
        if (clickCount === 3) {
            clickCount = 0;
            document.getElementById('secretPassInput').value = '';
            document.getElementById('secretPasswordModal').classList.add('active');
        }
    });

    window.checkSecretPassword = async function() {
        const pass = document.getElementById('secretPassInput').value;
        if (pass === SECRET_CODE) {
            document.getElementById('secretPasswordModal').classList.remove('active');
            document.getElementById('loadingText').style.display = 'block';
            try {
                await signInWithEmailAndPassword(auth, MASTER_EMAIL, MASTER_PASS);
                isSecretAdminMode = true;
                document.getElementById('secretAdminPanel').style.display = 'flex';
                document.getElementById('loadingText').style.display = 'none';
                await loadPricing();
                loadAdminData();
            } catch (e) {
                alert("Ошибка фонового входа. Проверьте мастер-аккаунт в Firebase.");
                document.getElementById('loadingText').style.display = 'none';
            }
        } else {
            document.getElementById('secretPasswordModal').classList.remove('active');
        }
    }

    window.closeSecretAdmin = function() {
        isSecretAdminMode = false;
        document.getElementById('secretAdminPanel').style.display = 'none';
        signOut(auth);
    }

    // ==========================================
    // ОБЫЧНАЯ ЛОГИКА
    // ==========================================
    window.toggleAuthMode = function() {
        isRegisterMode = !isRegisterMode;
        document.getElementById('authSubtitle').textContent = isRegisterMode ? 'Создание аккаунта' : 'Вход';
        document.getElementById('mainAuthBtn').textContent = isRegisterMode ? 'Зарегистрироваться' : 'Войти';
        document.getElementById('switchAuthBtn').textContent = isRegisterMode ? 'Уже есть аккаунт? Войти' : 'Нет аккаунта? Зарегистрироваться';
        document.getElementById('authError').style.display = 'none';
    };

    window.handleAuth = function() {
        const email = document.getElementById('loginInput').value.trim();
        const pass = document.getElementById('passwordInput').value;
        const err = document.getElementById('authError');
        const btn = document.getElementById('mainAuthBtn');
        err.style.display = 'none';
        btn.textContent = 'Загрузка...';

        const authAction = isRegisterMode ? createUserWithEmailAndPassword : signInWithEmailAndPassword;

        authAction(auth, email, pass).catch((error) => {
            btn.textContent = isRegisterMode ? 'Зарегистрироваться' : 'Войти';
            err.style.display = 'block';
            if (error.code === 'auth/email-already-in-use') err.textContent = 'Этот email уже зарегистрирован.';
            else if (error.code === 'auth/wrong-password') err.textContent = 'Неверный пароль.';
            else if (error.code === 'auth/user-not-found') err.textContent = 'Пользователь не найден.';
            else err.textContent = 'Ошибка: ' + error.message;
        });
    };

    window.logoutUser = function() { signOut(auth); };

    onAuthStateChanged(auth, async (user) => {
        if (isSecretAdminMode) return;

        if (user) {
            currentUserId = user.uid;
            document.getElementById('authScreen').style.display = 'none';
            document.getElementById('loadingText').style.display = 'block';
            
            try {
                await loadUserData(user.uid);
                await loadPricing();
                document.getElementById('loadingText').style.display = 'none';
                checkSubscription();

                setInterval(() => {
                    if(currentUserId && !isSecretAdminMode) {
                        updateDoc(doc(db, "users", currentUserId), { lastSeen: new Date().toISOString() }).catch(()=>{});
                    }
                }, 60000);
            } catch(e) {
                console.error("Ошибка при загрузке данных:", e);
                document.getElementById('loadingText').style.display = 'none';
                alert("Ошибка базы данных: " + e.message + ". Проверьте правила (Rules) и имя базы в Firebase.");
                document.getElementById('authScreen').style.display = 'flex';
                document.getElementById('appContainer').style.display = 'none';
            }
        } else {
            currentUserId = null;
            currentUserData = null;
            document.getElementById('authScreen').style.display = 'flex';
            document.getElementById('appContainer').style.display = 'none';
            document.getElementById('paymentScreen').style.display = 'none';
        }
    });

    async function loadUserData(uid) {
        try {
            const docSnap = await getDoc(doc(db, "users", uid));
            if (docSnap.exists()) {
                currentUserData = docSnap.data();
                if (currentUserData.appData) appData = { ...appData, ...currentUserData.appData };
            } else {
                const now = new Date();
                const trialEnd = new Date(now.getTime() + 7 * 24 * 60 * 60 * 1000);
                currentUserData = { email: auth.currentUser.email, createdAt: now.toISOString(), subEndDate: trialEnd.toISOString(), isBlocked: false, appData: appData, lastSeen: now.toISOString() };
                await setDoc(doc(db, "users", uid), currentUserData);
            }
        } catch (e) { console.error("Ошибка loadUserData:", e); throw e; }
    }

    async function loadPricing() {
        try {
            const docSnap = await getDoc(doc(db, "settings", "pricing"));
            if (docSnap.exists()) pricingPlans = docSnap.data().plans;
            renderPricingGrid();
            if (isSecretAdminMode) renderAdminPricing();
        } catch (e) { console.error("Ошибка loadPricing:", e); throw e; }
    }

    function checkSubscription() {
        if (!currentUserData) return;
        const now = new Date();
        if (currentUserData.isBlocked || now > new Date(currentUserData.subEndDate)) {
            showPaymentScreen();
        } else {
            showApp();
        }
    }

    function showApp() {
        document.getElementById('paymentScreen').style.display = 'none';
        document.getElementById('appContainer').style.display = 'flex';
        if (appData.settings.theme === 'dark') {
            document.documentElement.setAttribute('data-theme', 'dark');
            document.getElementById('themeBtn').innerHTML = '<i class="ph ph-sun"></i>';
        }
        try { initApp(); } catch(e) { console.error("Ошибка initApp:", e); }
    }

    function showPaymentScreen() {
        document.getElementById('appContainer').style.display = 'none';
        document.getElementById('paymentScreen').style.display = 'flex';
    }

    let saveTimeout;
    function save() {
        try {
            updateAI(); updateDashboardStats();
            if(document.getElementById('page-dashboard').classList.contains('active')) updateCharts();
            if(document.getElementById('page-planner').classList.contains('active')) renderMonthCalendar();
            if (!currentUserId || isSecretAdminMode) return;
            
            clearTimeout(saveTimeout);
            saveTimeout = setTimeout(async () => {
                try { await setDoc(doc(db, "users", currentUserId), { ...currentUserData, appData: appData }); } catch (e) { console.error("Save error:", e); }
            }, 1000); 
        } catch(e) { console.error("Ошибка save:", e); }
    }

    function renderPricingGrid() {
        const grid = document.getElementById('pricingGrid'); grid.innerHTML = '';
        pricingPlans.forEach(plan => {
            const card = document.createElement('div');
            card.className = 'tariff-card';
            card.onclick = () => openTelegramPayment(plan);
            card.innerHTML = `<div class="tariff-name">${plan.name}</div><div class="tariff-price">${plan.price} ₽</div><div class="tariff-days">${plan.days} дн.</div>`;
            grid.appendChild(card);
        });
    }

    window.openTelegramPayment = function(plan) {
        const email = currentUserData ? currentUserData.email : "Unknown";
        const text = encodeURIComponent(`Привет! Мой логин: ${email}. Хочу оплатить тариф "${plan.name}" (${plan.days} дней) за ${plan.price} рублей.`);
        document.getElementById('tgLink').href = `${TG_LINK}?text=${text}`;
        document.getElementById('payModal').classList.add('active');
    };

    window.closeModal = function(id) { document.getElementById(id).classList.remove('active'); }

    // ==========================================
    // АДМИНКА
    // ==========================================
    window.loadAdminData = async function() {
        const tbody = document.querySelector('#adminUsersTable tbody');
        tbody.innerHTML = '<tr><td colspan="4" style="text-align:center;">Загрузка...</td></tr>';
        document.getElementById('adminSearch').value = '';

        try {
            const paySnap = await getDocs(collection(db, "payments"));
            let revenue = 0;
            paySnap.forEach(d => revenue += d.data().amount);
            document.getElementById('adminRevenue').textContent = revenue.toLocaleString('ru-RU') + ' ₽';

            const querySnapshot = await getDocs(collection(db, "users"));
            let totalUsers = 0;
            let onlineUsers = 0;
            const now = new Date();
            
            tbody.innerHTML = '';
            querySnapshot.forEach((doc) => {
                const u = doc.data(); const uid = doc.id;
                if(u.email === MASTER_EMAIL) return;
                
                totalUsers++;
                if (u.lastSeen && (now - new Date(u.lastSeen)) < 120000) onlineUsers++;

                const isBlocked = u.isBlocked;
                const subEnd = new Date(u.subEndDate).toLocaleDateString('ru-RU');
                const isExpired = new Date(u.subEndDate) < new Date();
                
                let statusText = isBlocked ? '🚫 Заблок' : (isExpired ? '⌛ Истек' : '✅ Активен');
                let statusColor = isBlocked ? 'var(--bad)' : (isExpired ? 'var(--warn)' : 'var(--good)');

                const tr = document.createElement('tr');
                tr.innerHTML = `
                    <td class="user-email">${u.email}</td>
                    <td style="color:${statusColor}; font-weight:600;">${statusText}</td>
                    <td>${subEnd}</td>
                    <td>
                        <button class="admin-btn money" onclick="openPaymentLogger('${uid}', 3)">💰 +3д</button>
                        <button class="admin-btn money" onclick="openPaymentLogger('${uid}', 7)">💰 +7д</button>
                        <button class="admin-btn money" onclick="openPaymentLogger('${uid}', 30)">💰 +30д</button>
                        <button class="admin-btn money" onclick="openPaymentLogger('${uid}', 365)">💰 +1г</button>
                        <button class="admin-btn outline" style="color:${isBlocked ? 'var(--good)' : 'var(--bad)'}; border-color:${isBlocked ? 'var(--good)' : 'var(--bad)'}" onclick="adminToggleBlock('${uid}', ${isBlocked})">${isBlocked ? 'Разблок' : 'Блок'}</button>
                    </td>
                `;
                tbody.appendChild(tr);
            });
            
            document.getElementById('adminTotalUsers').textContent = totalUsers;
            document.getElementById('adminOnline').textContent = onlineUsers;

        } catch(e) { console.error(e); tbody.innerHTML = '<tr><td colspan="4" style="color:red;">Ошибка (Проверьте Rules)</td></tr>'; }
    }

    window.filterAdminTable = function() {
        const query = document.getElementById('adminSearch').value.toLowerCase();
        const rows = document.querySelectorAll('#adminUsersTable tbody tr');
        rows.forEach(row => {
            const emailCell = row.querySelector('.user-email');
            if (emailCell) {
                if (emailCell.textContent.toLowerCase().includes(query)) row.style.display = '';
                else row.style.display = 'none';
            }
        });
    }

    window.openPaymentLogger = function(uid, days) {
        document.getElementById('paymentUid').value = uid;
        document.getElementById('paymentDays').value = days;
        document.getElementById('paymentAmountInput').value = '';
        document.getElementById('paymentLogModal').classList.add('active');
    }

    window.confirmPaymentLog = async function() {
        const uid = document.getElementById('paymentUid').value;
        const days = Number(document.getElementById('paymentDays').value);
        const amount = Number(document.getElementById('paymentAmountInput').value);
        
        if (!amount || amount <= 0) return alert('Введите корректную сумму');

        try {
            const userRef = doc(db, "users", uid);
            const userSnap = await getDoc(userRef);
            const userData = userSnap.data();
            
            await addDoc(collection(db, "payments"), { uid: uid, email: userData.email, amount: amount, date: new Date().toISOString(), days: days });

            let currentEnd = new Date(userData.subEndDate);
            let now = new Date();
            let startFrom = currentEnd > now ? currentEnd : now;
            let newEnd = new Date(startFrom.getTime() + days * 24 * 60 * 60 * 1000);
            
            await updateDoc(userRef, { subEndDate: newEnd.toISOString(), isBlocked: false });
            
            closeModal('paymentLogModal');
            loadAdminData();
        } catch(e) { alert("Ошибка: " + e.message); }
    }

    window.adminToggleBlock = async function(uid, currentStatus) {
        try { await updateDoc(doc(db, "users", uid), { isBlocked: !currentStatus }); loadAdminData(); } catch(e) {}
    }

    window.renderAdminPricing = function() {
        const container = document.getElementById('pricingSettings'); container.innerHTML = '';
        pricingPlans.forEach((plan, idx) => {
            container.innerHTML += `
                <div style="display:grid; grid-template-columns: 1fr 1fr 1fr; gap:10px;">
                    <input type="text" class="input-field" value="${plan.name}" id="pname-${idx}" placeholder="Название">
                    <input type="number" class="input-field" value="${plan.days}" id="pdays-${idx}" placeholder="Дней">
                    <input type="number" class="input-field" value="${plan.price}" id="pprice-${idx}" placeholder="Цена (₽)">
                </div>`;
        });
    }

    window.savePricingSettings = async function() {
        let newPlans = [];
        pricingPlans.forEach((plan, idx) => {
            newPlans.push({ id: plan.id, name: document.getElementById(`pname-${idx}`).value, days: Number(document.getElementById(`pdays-${idx}`).value), price: Number(document.getElementById(`pprice-${idx}`).value) });
        });
        try {
            await setDoc(doc(db, "settings", "pricing"), { plans: newPlans });
            pricingPlans = newPlans;
            alert("Тарифы обновлены!");
            renderPricingGrid();
        } catch(e) { alert("Ошибка: " + e.message); }
    }

    // --- ЛОГИКА ПЛАНЕРА ---
    const emojis = { sleep: '😴', energy: '🔋', mood: '🤩', water: '💧', food: '🍏', sport: '🏋️' };
    function initApp() {
        ['sleep', 'energy', 'mood', 'water', 'food', 'sport'].forEach(metric => {
            const scale = document.getElementById('rs' + metric.charAt(0).toUpperCase() + metric.slice(1));
            if(scale.innerHTML !== '') return;
            for(let i=1; i<=10; i++) {
                let emoji = emojis[metric];
                if(metric === 'mood') { if(i<=3) emoji='🙁'; else if(i<=5) emoji='😐'; else if(i<=7) emoji='🙂'; else if(i<=9) emoji='😃'; else emoji='🤩'; }
                if(metric === 'food') { if(i<=3) emoji='🍔'; else if(i<=5) emoji='🍕'; else if(i<=8) emoji='🥦'; else emoji='🍏'; }
                if(metric === 'sport') { if(i<=2) emoji='🛋️'; else if(i<=5) emoji='🚶'; else if(i<=7) emoji='🏃'; else emoji='🏋️'; }
                scale.innerHTML += `<div class="rating-item" onclick="setRating('${metric}', ${i})">${emoji}</div>`;
            }
        });
        updateDashboardStats(); setTimeout(() => updateCharts(), 100); renderThoughts(); loadHealthData(); renderHabits();
    }

    window.switchPage = function(pageId, btn) {
        document.querySelectorAll('.page').forEach(el => el.classList.remove('active'));
        document.querySelectorAll('.nav-btn').forEach(el => el.classList.remove('active'));
        document.getElementById('page-' + pageId).classList.add('active'); btn.classList.add('active');
        if(pageId === 'dashboard') { updateDashboardStats(); setTimeout(() => updateCharts(), 50); }
        if(pageId === 'health') { loadHealthData(); renderThoughts(); }
        if(pageId === 'planner') { renderMonthCalendar(); renderPlanner(); renderHabits(); }
    };

    window.toggleTheme = function() {
        const root = document.documentElement;
        if (root.getAttribute('data-theme') === 'dark') { root.removeAttribute('data-theme'); appData.settings.theme = 'light'; document.getElementById('themeBtn').innerHTML = '<i class="ph ph-moon"></i>'; } 
        else { root.setAttribute('data-theme', 'dark'); appData.settings.theme = 'dark'; document.getElementById('themeBtn').innerHTML = '<i class="ph ph-sun"></i>'; }
        save();
    };

    let currentDate = new Date(); let currentWeekStart = getMonday(new Date()); let activeModalDate = ''; 
    function getMonday(d) { d = new Date(d); const day = d.getDay(); const diff = d.getDate() - day + (day === 0 ? -6 : 1); return new Date(d.setDate(diff)); }
    function getFormattedDate(date) { const d = new Date(date); return d.getFullYear() + '-' + String(d.getMonth()+1).padStart(2,'0') + '-' + String(d.getDate()).padStart(2,'0'); }

    window.changeMonth = function(offset) { currentDate.setMonth(currentDate.getMonth() + offset); renderMonthCalendar(); };

    function renderMonthCalendar() {
        const year = currentDate.getFullYear(); const month = currentDate.getMonth();
        const monthNames = ["Январь", "Февраль", "Март", "Апрель", "Май", "Июнь", "Июль", "Август", "Сентябрь", "Октябрь", "Ноябрь", "Декабрь"];
        document.getElementById('monthTitle').textContent = `${monthNames[month]} ${year}`;
        const firstDay = new Date(year, month, 1); const lastDay = new Date(year, month + 1, 0);
        let startDayOfWeek = firstDay.getDay(); if (startDayOfWeek === 0) startDayOfWeek = 7; 
        const grid = document.getElementById('monthCalendarGrid'); grid.innerHTML = '';
        ['Пн', 'Вт', 'Ср', 'Чт', 'Пт', 'Сб', 'Вс'].forEach(d => grid.innerHTML += `<div class="cal-day-name">${d}</div>`);
        for (let i = 1; i < startDayOfWeek; i++) grid.innerHTML += `<div class="cal-cell empty"></div>`;
        const todayStr = getFormattedDate(new Date());
        for (let i = 1; i <= lastDay.getDate(); i++) {
            const dateStr = `${year}-${String(month + 1).padStart(2, '0')}-${String(i).padStart(2, '0')}`; const dateMMDD = dateStr.slice(5); 
            let classes = 'cal-cell'; if (dateStr === todayStr) classes += ' today';
            let dayItems = []; const dayTasks = appData.tasks[dateStr] || []; dayTasks.forEach(t => dayItems.push({ text: t.text, type: 'task' }));
            appData.importantEvents.forEach(ev => { if (ev.recurring && ev.date === dateMMDD) dayItems.unshift({ text: ev.title, type: 'important' }); else if (!ev.recurring && ev.date === dateStr) dayItems.unshift({ text: ev.title, type: 'important' }); });
            const notes = appData.dayNotes[dateStr] || []; notes.forEach(n => { if (!n.isTask) dayItems.push({ text: n.text, type: 'note' }); });
            let pillsHTML = ''; dayItems.slice(0, 3).forEach(item => { pillsHTML += `<div class="cal-pill ${item.type}" style="background:var(--surface-soft); color:var(--text);" title="${item.text}">${item.text}</div>`; });
            if (dayItems.length > 3) pillsHTML += `<div class="cal-pill more">+${dayItems.length - 3}</div>`;
            grid.innerHTML += `<div class="${classes}" onclick="openDayModal('${dateStr}')"><div class="cal-date">${i}</div><div class="cal-events-container">${pillsHTML}</div></div>`;
        }
    }

    window.openDayModal = function(dateStr) { activeModalDate = dateStr; const d = new Date(dateStr); document.getElementById('dayModalTitle').textContent = d.toLocaleDateString('ru-RU', { weekday: 'long', day: 'numeric', month: 'long' }); renderDayModalList(); document.getElementById('dayModal').classList.add('active'); }

    function renderDayModalList() {
        const list = document.getElementById('dayEventsList'); list.innerHTML = '';
        const dayTasks = appData.tasks[activeModalDate] || []; const notes = appData.dayNotes[activeModalDate] || [];
        if (notes.length === 0 && dayTasks.length === 0) { list.innerHTML = '<div style="text-align:center; color:var(--text-muted); font-size:13px; padding:20px 0;">Нет записей</div>'; return; }
        notes.forEach(note => { const div = document.createElement('div'); div.className = 'event-item'; div.style = "display:flex; justify-content:space-between; padding:10px; background:var(--surface-soft); border-radius:8px;"; div.innerHTML = `<span>${note.text}</span><div style="display:flex; gap:10px;"><button style="background:none; border:none; cursor:pointer; color:var(--accent);" onclick="convertNoteToTask('${note.id}')"><i class="ph ph-arrow-right"></i></button><button style="background:none; border:none; cursor:pointer; color:var(--bad);" onclick="deleteDayItem('${note.id}', 'note')"><i class="ph ph-trash"></i></button></div>`; list.appendChild(div); });
        dayTasks.forEach(task => { const div = document.createElement('div'); div.className = 'event-item'; div.style = "display:flex; justify-content:space-between; padding:10px; background:var(--surface-soft); border-radius:8px;"; div.innerHTML = `<div style="display:flex; gap:10px; align-items:center;"><input type="checkbox" ${task.done ? 'checked' : ''} onchange="toggleTaskStatus('${task.id}')"><span style="${task.done ? 'text-decoration:line-through; color:var(--text-muted);' : ''}">${task.text}</span></div><button style="background:none; border:none; cursor:pointer; color:var(--bad);" onclick="deleteDayItem('${task.id}', 'task')"><i class="ph ph-trash"></i></button>`; list.appendChild(div); });
    }

    window.addDayNote = function() { const input = document.getElementById('dayNoteInput'); const text = input.value.trim(); if (!text) return; if (!appData.dayNotes[activeModalDate]) appData.dayNotes[activeModalDate] = []; appData.dayNotes[activeModalDate].push({ id: Date.now().toString(), text: text, isTask: false }); input.value = ''; save(); renderDayModalList(); }
    window.convertNoteToTask = function(id) { const notes = appData.dayNotes[activeModalDate]; const noteIdx = notes.findIndex(n => n.id === id); if (noteIdx > -1) { const note = notes.splice(noteIdx, 1)[0]; if (!appData.tasks[activeModalDate]) appData.tasks[activeModalDate] = []; appData.tasks[activeModalDate].push({ id: note.id, text: note.text, done: false, note: '', noteHeight: '60px' }); save(); renderDayModalList(); renderPlanner(); } }
    window.toggleTaskStatus = function(id) { const task = appData.tasks[activeModalDate].find(t => t.id === id); if (task) { task.done = !task.done; save(); renderDayModalList(); renderPlanner(); } }
    window.deleteDayItem = function(id, source) { if (source === 'note') appData.dayNotes[activeModalDate] = appData.dayNotes[activeModalDate].filter(n => n.id !== id); else appData.tasks[activeModalDate] = appData.tasks[activeModalDate].filter(t => t.id !== id); save(); renderDayModalList(); renderPlanner(); }

    let openNotes = new Set(); 
    function renderPlanner() {
        const grid = document.getElementById('weekGrid'); grid.innerHTML = '';
        const days = ['Пн', 'Вт', 'Ср', 'Чт', 'Пт', 'Сб', 'Вс'];
        const endOfWeek = new Date(currentWeekStart); endOfWeek.setDate(endOfWeek.getDate() + 6);
        document.getElementById('weekRangeTitle').textContent = `${currentWeekStart.toLocaleDateString('ru-RU', {day:'numeric', month:'short'})} — ${endOfWeek.toLocaleDateString('ru-RU', {day:'numeric', month:'short'})}`;
        for (let i = 0; i < 7; i++) {
            const d = new Date(currentWeekStart); d.setDate(d.getDate() + i); const dateStr = getFormattedDate(d); const isToday = dateStr === getFormattedDate(new Date());
            if (!appData.tasks[dateStr]) appData.tasks[dateStr] = []; const tasks = appData.tasks[dateStr]; const done = tasks.filter(t => t.done).length; const pct = tasks.length === 0 ? 0 : Math.round((done / tasks.length) * 100);
            const col = document.createElement('div'); col.className = 'day-col'; col.id = `day-col-${dateStr}`; if (isToday) col.style.borderColor = 'var(--good)';
            let tasksHTML = tasks.map((t, idx) => { const isNoteOpen = openNotes.has(t.id); const displayStyle = isNoteOpen ? 'block' : 'none'; const noteBtnClass = isNoteOpen ? 'note-btn active' : 'note-btn'; const noteHeight = t.noteHeight || '60px'; return `<div class="t-item"><div class="t-header"><input type="checkbox" ${t.done ? 'checked' : ''} onchange="toggleTask('${dateStr}', ${idx}, event)"><textarea class="task-text" rows="1" placeholder="Что нужно сделать?" oninput="autoResize(this)" onchange="editTask('${dateStr}', ${idx}, this.value)" style="${t.done ? 'text-decoration: line-through; color: var(--text-muted);' : ''}">${t.text}</textarea></div><div class="t-footer"><button class="${noteBtnClass}" onclick="toggleTaskNote('${t.id}')" title="Детали/Заметка" style="background:none; border:none; color:var(--text-muted); cursor:pointer; font-size:13px;"><i class="ph ph-note-pencil"></i> Детали</button><button class="del" onclick="delTask('${dateStr}', ${idx})" style="background:none; border:none; color:var(--text-muted); cursor:pointer;"><i class="ph ph-trash"></i></button></div><div class="task-note-container" id="note-${t.id}" style="display: ${displayStyle};"><textarea class="task-note-input" style="height: ${noteHeight};" placeholder="Список покупок, упражнения..." oninput="saveTaskNote('${dateStr}', ${idx}, this.value)" onblur="saveNoteHeight('${dateStr}', ${idx}, this.style.height)">${t.note || ''}</textarea></div></div>`; }).join('');
            col.innerHTML = `<div class="day-head" style="display:flex; justify-content:space-between; align-items:center;"><div><div style="font-weight:600; font-size:14px;">${days[i]}</div><div style="font-size:12px; color:var(--text-muted);">${d.getDate()} ${d.toLocaleDateString('ru-RU', {month:'short'})}</div></div><button style="background:none; border:none; color:var(--accent); font-size:20px; cursor:pointer;" onclick="addTask('${dateStr}')"><i class="ph ph-plus"></i></button></div><div class="circle-prog" style="--p: ${pct}%"><span>${pct}%</span></div><div class="task-list" id="tl-${dateStr}">${tasksHTML}</div>`;
            grid.appendChild(col);
        }
        setTimeout(() => document.querySelectorAll('.task-text').forEach(ta => autoResize(ta)), 50);
    }

    window.autoResize = function(textarea) { textarea.style.height = 'auto'; textarea.style.height = textarea.scrollHeight + 'px'; }
    window.addTask = function(dateStr) { if (!appData.tasks[dateStr]) appData.tasks[dateStr] = []; appData.tasks[dateStr].push({ id: Date.now().toString(), text: '', done: false, note: '', noteHeight: '60px' }); save(); renderPlanner(); setTimeout(() => { const inputs = document.querySelectorAll(`#tl-${dateStr} .task-text`); if(inputs.length) inputs[inputs.length-1].focus(); }, 50); }
    window.toggleTask = function(date, idx, event) { appData.tasks[date][idx].done = !appData.tasks[date][idx].done; save(); const checkbox = event.target; const textarea = checkbox.nextElementSibling; if (appData.tasks[date][idx].done) { textarea.style.textDecoration = 'line-through'; textarea.style.color = 'var(--text-muted)'; } else { textarea.style.textDecoration = 'none'; textarea.style.color = 'var(--text)'; } const tasks = appData.tasks[date]; const done = tasks.filter(t => t.done).length; const pct = tasks.length === 0 ? 0 : Math.round((done / tasks.length) * 100); const circle = document.querySelector(`#day-col-${date} .circle-prog`); if(circle) { circle.style.setProperty('--p', `${pct}%`); circle.querySelector('span').textContent = `${pct}%`; } renderMonthCalendar(); }
    window.editTask = function(date, idx, val) { appData.tasks[date][idx].text = val; save(); }
    window.delTask = function(date, idx) { appData.tasks[date].splice(idx, 1); save(); renderPlanner(); renderMonthCalendar(); }
    window.toggleTaskNote = function(taskId) { const container = document.getElementById(`note-${taskId}`); const btn = container.closest('.t-item').querySelector('.note-btn'); if (container.style.display === 'none' || container.style.display === '') { container.style.display = 'block'; btn.classList.add('active'); openNotes.add(taskId); container.querySelector('textarea').focus(); } else { container.style.display = 'none'; btn.classList.remove('active'); openNotes.delete(taskId); } }
    window.saveTaskNote = function(dateStr, idx, val) { appData.tasks[dateStr][idx].note = val; save(); }
    window.saveNoteHeight = function(dateStr, idx, height) { appData.tasks[dateStr][idx].noteHeight = height; save(); }

    // --- ПРИВЫЧКИ ---
    window.renderHabits = function() {
        const list = document.getElementById('habitsList'); const header = document.getElementById('habitDatesHeader');
        if(!list || !header) return;
        
        header.innerHTML = '';
        const days = ['Пн', 'Вт', 'Ср', 'Чт', 'Пт', 'Сб', 'Вс'];
        
        for (let i = 0; i < 7; i++) {
            const d = new Date(currentWeekStart);
            d.setDate(d.getDate() + i);
            header.innerHTML += `<div class="h-day-label">${days[i]}<br><span style="font-size:11px;font-weight:400;opacity:0.6;">${d.getDate()}</span></div>`;
        }

        list.innerHTML = '';
        appData.habits.forEach(h => {
            const row = document.createElement('div'); row.className = 'habit-row';
            const nameInput = document.createElement('input'); nameInput.className = 'habit-name'; nameInput.value = h.name;
            nameInput.onchange = (e) => { h.name = e.target.value; save(); };
            
            const checksDiv = document.createElement('div'); checksDiv.className = 'habit-days';
            
            for (let i = 0; i < 7; i++) {
                const d = new Date(currentWeekStart); d.setDate(d.getDate() + i);
                const dateStr = getFormattedDate(d);
                const isDone = h.history.includes(dateStr);
                const check = document.createElement('div');
                check.className = `h-check ${isDone ? 'checked' : ''}`;
                check.innerHTML = '<i class="ph ph-check"></i>';
                check.onclick = () => toggleHabit(h.id, dateStr);
                checksDiv.appendChild(check);
            }

            const delBtn = document.createElement('button'); delBtn.className = 'h-del'; delBtn.innerHTML = '<i class="ph ph-x"></i>';
            delBtn.onclick = () => { appData.habits = appData.habits.filter(x => x.id !== h.id); save(); renderHabits(); };
            
            row.appendChild(nameInput); row.appendChild(checksDiv); row.appendChild(delBtn); list.appendChild(row);
        });
    }

    window.toggleHabit = function(id, dateStr) {
        const habit = appData.habits.find(h => h.id === id);
        const idx = habit.history.indexOf(dateStr);
        if (idx > -1) habit.history.splice(idx, 1);
        else habit.history.push(dateStr);
        save(); renderHabits();
    }

    window.addHabit = function() {
        appData.habits.push({ id: Date.now().toString(), name: 'Новый ритуал', history: [] });
        save(); renderHabits();
    }

    window.setRating = function(metric, value) { const today = getFormattedDate(new Date()); if (!appData.health[today]) appData.health[today] = { sleep: 0, energy: 0, mood: 0, water: 0, food: 0, sport: 0 }; const h = appData.health[today]; h[metric] = (h[metric] === value) ? 0 : value; save(); loadHealthData(); }
    function loadHealthData() { const today = getFormattedDate(new Date()); if (!appData.health[today]) appData.health[today] = { sleep: 0, energy: 0, mood: 0, water: 0, food: 0, sport: 0 }; const h = appData.health[today]; document.getElementById('vSleep').textContent = h.sleep + ' / 10'; document.getElementById('vEnergy').textContent = h.energy + ' / 10'; document.getElementById('vMood').textContent = h.mood + ' / 10'; document.getElementById('vWater').textContent = h.water + ' / 10'; document.getElementById('vFood').textContent = h.food + ' / 10'; document.getElementById('vSport').textContent = h.sport + ' / 10'; document.querySelectorAll('.rating-item').forEach(el => el.classList.remove('active')); ['sleep', 'energy', 'mood', 'water', 'food', 'sport'].forEach(metric => { const scale = document.getElementById('rs' + metric.charAt(0).toUpperCase() + metric.slice(1)); const items = scale.querySelectorAll('.rating-item'); for (let i = 0; i < h[metric]; i++) { if(items[i]) items[i].classList.add('active'); } }); updateHealthAI(h); }

    function updateHealthAI(h) { let paragraphs = []; const isSleepBad = h.sleep > 0 && h.sleep <= 4; const isSleepGood = h.sleep >= 7; const isEnergyBad = h.energy > 0 && h.energy <= 4; const isWaterBad = h.water > 0 && h.water <= 4; const isFoodBad = h.food > 0 && h.food <= 4; const isSportGood = h.sport >= 7; if (h.sleep === 0 && h.energy === 0) { document.getElementById('healthAdviceText').innerHTML = "Привет! Отметь показатели слева, чтобы я проанализировал твой день."; return; } paragraphs.push("Привет! Давай посмотрим на твое состояние сегодня."); if (isSleepBad) paragraphs.push(`🚨 <b>Внимание на сон.</b> Ты спал мало. Когнитивные способности снижены, отложи сложные задачи.`); else if (isSleepGood) paragraphs.push(`✅ <b>Отличный сон!</b> Идеальное время для важных дел.`); if (isEnergyBad) paragraphs.push(`🔋 <b>Низкая энергия.</b> Не работай через силу. Сделай разминку или выпей чаю.`); if (isFoodBad && isSportGood) paragraphs.push(`🍔 <b>Дисбаланс питания и нагрузок.</b> Тяжелая пища при тренировке вызовет сонливость.`); else if (isSportGood) paragraphs.push(`🏋️ <b>Отличная тренировка!</b> Не забудь восполнить водный баланс.`); if (isWaterBad) paragraphs.push(`💧 <b>Мало воды.</b> Выпей стакан прямо сейчас.`); if (h.sleep <= 5 && isSportGood) paragraphs.push(`⚠️ <b>Переутомление:</b> Тренировка при недосыпе — стресс. Ляг пораньше.`); paragraphs.push("Береги себя!"); document.getElementById('healthAdviceText').innerHTML = paragraphs.map(p => `<p>${p}</p>`).join(''); }

    window.saveThought = function() { const input = document.getElementById('thoughtInput'); const text = input.value.trim(); if (!text) return; appData.mindstream.push({ id: Date.now().toString(), timestamp: new Date().toISOString(), text: text }); input.value = ''; save(); renderThoughts(); }
    function renderThoughts() { const list = document.getElementById('thoughtsList'); list.innerHTML = ''; if (appData.mindstream.length === 0) { list.innerHTML = '<div style="text-align:center; color:var(--text-muted); font-size:13px;">Хроника пуста</div>'; return; } const sorted = [...appData.mindstream].sort((a, b) => new Date(b.timestamp) - new Date(a.timestamp)); sorted.forEach(t => { const card = document.createElement('div'); card.className = 'thought-card'; const d = new Date(t.timestamp); card.innerHTML = `<div style="display:flex; justify-content:space-between; margin-bottom:8px;"><span class="thought-date">${d.toLocaleDateString('ru-RU')} ${d.toLocaleTimeString('ru-RU', {hour:'2-digit', minute:'2-digit'})}</span><button style="background:none; border:none; color:var(--bad); cursor:pointer;" onclick="deleteThought('${t.id}')"><i class="ph ph-trash"></i></button></div><div class="thought-text">${t.text}</div>`; list.appendChild(card); }); }
    window.deleteThought = function(id) { if(confirm('Удалить запись?')) { appData.mindstream = appData.mindstream.filter(t => t.id !== id); save(); renderThoughts(); } }

    let chartTasks = null, chartHealth = null;
    function updateDashboardStats() { const todayStr = getFormattedDate(new Date()); const h = appData.health[todayStr] || { sleep: 0, energy: 0, mood: 0, water: 0, food: 0, sport: 0 }; const tasksToday = appData.tasks[todayStr] || []; const doneTasks = tasksToday.filter(t => t.done).length; const totalTasks = tasksToday.length; function getCardClass(val, type) { if (val === 0) return 'neutral'; if (type === 'tasks') return val === 0 ? 'bad' : 'good'; if (val <= 4) return 'bad'; if (val <= 7) return 'warn'; return 'good'; } document.getElementById('dashStatsContainer').innerHTML = `<div class="stat-card ${getCardClass(h.sleep, 'health')}"><div class="stat-header"><i class="ph ph-moon"></i> Сон</div><div class="stat-value">${h.sleep} <span style="font-size:18px; opacity:0.5;">/ 10</span></div></div><div class="stat-card ${getCardClass(h.energy, 'health')}"><div class="stat-header"><i class="ph ph-lightning"></i> Энергия</div><div class="stat-value">${h.energy} <span style="font-size:18px; opacity:0.5;">/ 10</span></div></div><div class="stat-card ${getCardClass(h.mood, 'health')}"><div class="stat-header"><i class="ph ph-smiley"></i> Настроение</div><div class="stat-value">${h.mood} <span style="font-size:18px; opacity:0.5;">/ 10</span></div></div><div class="stat-card ${totalTasks === 0 ? 'neutral' : (doneTasks === totalTasks ? 'good' : 'warn')}"><div class="stat-header"><i class="ph ph-check-circle"></i> Задачи</div><div class="stat-value">${doneTasks} <span style="font-size:18px; opacity:0.5;">из ${totalTasks}</span></div></div>`; let brief = h.sleep === 0 ? "Заполните данные во вкладке 'Состояние' для утреннего брифинга." : `Сон: <b>${h.sleep}/10</b>. Энергия и настроение: <b>${h.energy}</b> и <b>${h.mood}</b>. Выполнено <b>${doneTasks}</b> задач.`; document.getElementById('aiBriefingText').innerHTML = brief; }

    function updateCharts() {
        const dates = [], data = [];
        for (let i = 6; i >= 0; i--) { const d = new Date(); d.setDate(d.getDate() - i); dates.push(d.toLocaleDateString('ru-RU', {weekday:'short'})); const dt = appData.tasks[getFormattedDate(d)] || []; data.push(dt.filter(t => t.done).length); }
        const isDark = appData.settings.theme === 'dark';
        const optTasks = { series: [{ name: 'Выполнено', data: data }], chart: { type: 'bar', height: 260, toolbar: { show: false }, fontFamily: 'DM Sans' }, colors: ['#C48B73'], plotOptions: { bar: { borderRadius: 6, columnWidth: '35%' } }, xaxis: { categories: dates, labels: { style: { colors: isDark ? '#948E87' : '#8C857D' } } }, yaxis: { labels: { style: { colors: isDark ? '#948E87' : '#8C857D' } } }, grid: { borderColor: isDark ? '#383431' : '#EBE6DD', strokeDashArray: 4 }, theme: { mode: isDark ? 'dark' : 'light' } };
        if (chartTasks) chartTasks.destroy(); chartTasks = new ApexCharts(document.querySelector("#chartTasks"), optTasks); chartTasks.render();
        const sleepData = [], energyData = [];
        for (let i = 6; i >= 0; i--) { const d = new Date(); d.setDate(d.getDate() - i); const h = appData.health[getFormattedDate(d)] || { sleep: 0, energy: 0 }; sleepData.push(h.sleep); energyData.push(h.energy); }
        const optHealth = { series: [{ name: 'Сон', data: sleepData }, { name: 'Энергия', data: energyData }], chart: { type: 'area', height: 260, toolbar: { show: false }, fontFamily: 'DM Sans' }, colors: ['#7B9C83', '#D4A373'], fill: { type: 'gradient', gradient: { opacityFrom: 0.3, opacityTo: 0.05 } }, stroke: { curve: 'smooth', width: 3 }, xaxis: { categories: dates, labels: { style: { colors: isDark ? '#948E87' : '#8C857D' } } }, yaxis: { max: 10, min: 0, tickAmount: 5, labels: { style: { colors: isDark ? '#948E87' : '#8C857D' } } }, grid: { borderColor: isDark ? '#383431' : '#EBE6DD', strokeDashArray: 4 }, theme: { mode: isDark ? 'dark' : 'light' }, legend: { labels: { colors: isDark ? '#F0ECE6' : '#2C2A29' } } };
        if (chartHealth) chartHealth.destroy(); chartHealth = new ApexCharts(document.querySelector("#chartHealth"), optHealth); chartHealth.render();
    }
</script>
</body>
</html>
