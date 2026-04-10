<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Wick Bot Dashboard</title>
    <script src="https://telegram.org/js/telegram-web-app.js"></script>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
            background: var(--tg-theme-bg-color, #17212b);
            color: var(--tg-theme-text-color, #ffffff);
            padding: 16px;
            overflow-x: hidden;
        }

        .header {
            text-align: center;
            margin-bottom: 24px;
        }

        .header h1 {
            font-size: 24px;
            font-weight: 600;
            margin-bottom: 8px;
        }

        .status {
            display: inline-block;
            padding: 6px 16px;
            border-radius: 20px;
            font-size: 13px;
            font-weight: 500;
            background: var(--tg-theme-button-color, #5288c1);
            color: var(--tg-theme-button-text-color, #ffffff);
        }

        .card {
            background: var(--tg-theme-secondary-bg-color, #232e3c);
            border-radius: 12px;
            padding: 16px;
            margin-bottom: 16px;
        }

        .card-title {
            font-size: 16px;
            font-weight: 600;
            margin-bottom: 12px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .balance-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 12px;
        }

        .balance-item {
            text-align: center;
            padding: 12px;
            background: rgba(255,255,255,0.05);
            border-radius: 8px;
        }

        .balance-label {
            font-size: 12px;
            opacity: 0.7;
            margin-bottom: 4px;
        }

        .balance-value {
            font-size: 20px;
            font-weight: 700;
        }

        .profit { color: #4cd964; }
        .loss { color: #ff3b30; }

        .btn-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 10px;
        }

        .btn {
            padding: 14px;
            border: none;
            border-radius: 10px;
            font-size: 14px;
            font-weight: 600;
            cursor: pointer;
            transition: opacity 0.2s;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 6px;
        }

        .btn:active {
            opacity: 0.7;
        }

        .btn-primary {
            background: #4cd964;
            color: white;
        }

        .btn-danger {
            background: #ff3b30;
            color: white;
        }

        .btn-secondary {
            background: rgba(255,255,255,0.1);
            color: var(--tg-theme-text-color, #ffffff);
        }

        .btn-warning {
            background: #ff9500;
            color: white;
        }

        .position-list {
            max-height: 400px;
            overflow-y: auto;
        }

        .position-item {
            background: rgba(255,255,255,0.03);
            padding: 12px;
            border-radius: 8px;
            margin-bottom: 8px;
        }

        .position-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 8px;
        }

        .position-instrument {
            font-size: 16px;
            font-weight: 600;
        }

        .position-type {
            padding: 4px 12px;
            border-radius: 6px;
            font-size: 12px;
            font-weight: 600;
        }

        .type-long { background: #4cd964; color: white; }
        .type-short { background: #ff3b30; color: white; }

        .position-details {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 8px;
            font-size: 13px;
        }

        .detail-item {
            text-align: center;
        }

        .detail-label {
            opacity: 0.6;
            font-size: 11px;
            margin-bottom: 2px;
        }

        .detail-value {
            font-weight: 600;
        }

        .empty-state {
            text-align: center;
            padding: 32px 16px;
            opacity: 0.5;
        }

        .empty-icon {
            font-size: 48px;
            margin-bottom: 8px;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 12px;
        }

        .stat-item {
            text-align: center;
            padding: 12px;
            background: rgba(255,255,255,0.05);
            border-radius: 8px;
        }

        .stat-label {
            font-size: 11px;
            opacity: 0.7;
            margin-bottom: 4px;
        }

        .stat-value {
            font-size: 18px;
            font-weight: 700;
        }

        .tab-bar {
            display: flex;
            gap: 8px;
            margin-bottom: 16px;
        }

        .tab-btn {
            flex: 1;
            padding: 10px;
            background: rgba(255,255,255,0.05);
            border: none;
            border-radius: 8px;
            color: var(--tg-theme-text-color, #ffffff);
            cursor: pointer;
            font-size: 14px;
            font-weight: 500;
        }

        .tab-btn.active {
            background: var(--tg-theme-button-color, #5288c1);
            color: var(--tg-theme-button-text-color, #ffffff);
        }

        .loading {
            text-align: center;
            padding: 20px;
            opacity: 0.6;
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>⚡ Wick Bot</h1>
        <div class="status" id="status">🔴 Arrêté</div>
    </div>

    <div class="card">
        <div class="card-title">💰 Compte Trading</div>
        <div class="balance-grid">
            <div class="balance-item">
                <div class="balance-label">Solde</div>
                <div class="balance-value" id="balance">---</div>
            </div>
            <div class="balance-item">
                <div class="balance-label">P/L</div>
                <div class="balance-value profit" id="pl">---</div>
            </div>
        </div>
    </div>

    <div class="card">
        <div class="card-title">🎮 Contrôles</div>
        <div class="btn-grid">
            <button class="btn btn-primary" onclick="sendCommand('run')">
                🚀 Démarrer
            </button>
            <button class="btn btn-danger" onclick="sendCommand('stop')">
                🛑 Arrêter
            </button>
            <button class="btn btn-secondary" onclick="refresh()">
                🔄 Actualiser
            </button>
            <button class="btn btn-warning" onclick="confirmPanic()">
                🆘 Panic
            </button>
        </div>
    </div>

    <div class="tab-bar">
        <button class="tab-btn active" onclick="showTab('positions')">
            📊 Positions
        </button>
        <button class="tab-btn" onclick="showTab('stats')">
            📈 Stats
        </button>
    </div>

    <div class="card" id="positionsTab">
        <div class="card-title">📊 Positions Ouvertes</div>
        <div class="position-list" id="positionsList">
            <div class="loading">⏳ Chargement...</div>
        </div>
    </div>

    <div class="card" id="statsTab" style="display:none;">
        <div class="card-title">📈 Performance</div>
        <div class="stats-grid">
            <div class="stat-item">
                <div class="stat-label">Trades</div>
                <div class="stat-value" id="totalTrades">0</div>
            </div>
            <div class="stat-item">
                <div class="stat-label">Win Rate</div>
                <div class="stat-value profit" id="winRate">0%</div>
            </div>
            <div class="stat-item">
                <div class="stat-label">Profit</div>
                <div class="stat-value profit" id="profit">$0</div>
            </div>
            <div class="stat-item">
                <div class="stat-label">Net P/L</div>
                <div class="stat-value" id="netPL">$0</div>
            </div>
        </div>
    </div>

    <script>
        const tg = window.Telegram.WebApp;
        tg.expand();
        tg.ready();

        let botRunning = false;

        function sendCommand(cmd) {
            tg.sendData(JSON.stringify({ command: cmd }));
            
            if (cmd === 'run') {
                botRunning = true;
                updateStatus();
                tg.showAlert('🚀 Bot démarré !');
            } else if (cmd === 'stop') {
                botRunning = false;
                updateStatus();
                tg.showAlert('🛑 Bot arrêté');
            }
        }

        function confirmPanic() {
            tg.showConfirm('⚠️ Fermer TOUTES les positions ?', (confirmed) => {
                if (confirmed) {
                    sendCommand('panic');
                    tg.showAlert('🚨 Mode panique activé !');
                }
            });
        }

        function refresh() {
            sendCommand('refresh');
            loadData();
        }

        function updateStatus() {
            const status = document.getElementById('status');
            if (botRunning) {
                status.textContent = '🟢 Actif';
                status.style.background = '#4cd964';
            } else {
                status.textContent = '🔴 Arrêté';
                status.style.background = '#ff3b30';
            }
        }

        function loadData() {
            // Balance
            const balance = 10000 + Math.random() * 1000;
            const pl = (Math.random() - 0.5) * 200;
            
            document.getElementById('balance').textContent = `$${balance.toFixed(2)}`;
            
            const plEl = document.getElementById('pl');
            plEl.textContent = `${pl >= 0 ? '+' : ''}$${pl.toFixed(2)}`;
            plEl.className = pl >= 0 ? 'balance-value profit' : 'balance-value loss';

            // Positions (simulation)
            loadPositions();
            
            // Stats (simulation)
            loadStats();
        }

        function loadPositions() {
            const positions = [
                {
                    instrument: 'XAU/USD',
                    type: 'LONG',
                    units: 1000,
                    price: 2048.30,
                    pl: 28.50
                },
                {
                    instrument: 'XAU/USD',
                    type: 'SHORT',
                    units: 500,
                    price: 2046.10,
                    pl: -12.30
                }
            ];

            const list = document.getElementById('positionsList');
            
            if (positions.length === 0) {
                list.innerHTML = `
                    <div class="empty-state">
                        <div class="empty-icon">📦</div>
                        <div>Aucune position</div>
                    </div>
                `;
                return;
            }

            let html = '';
            positions.forEach(pos => {
                const typeClass = pos.type === 'LONG' ? 'type-long' : 'type-short';
                const plClass = pos.pl >= 0 ? 'profit' : 'loss';
                const emoji = pos.type === 'LONG' ? '🟢' : '🔴';
                
                html += `
                    <div class="position-item">
                        <div class="position-header">
                            <div class="position-instrument">${pos.instrument}</div>
                            <div class="position-type ${typeClass}">${emoji} ${pos.type}</div>
                        </div>
                        <div class="position-details">
                            <div class="detail-item">
                                <div class="detail-label">Unités</div>
                                <div class="detail-value">${pos.units}</div>
                            </div>
                            <div class="detail-item">
                                <div class="detail-label">Prix</div>
                                <div class="detail-value">${pos.price}</div>
                            </div>
                            <div class="detail-item">
                                <div class="detail-label">P/L</div>
                                <div class="detail-value ${plClass}">
                                    ${pos.pl >= 0 ? '+' : ''}$${pos.pl.toFixed(2)}
                                </div>
                            </div>
                        </div>
                    </div>
                `;
            });

            list.innerHTML = html;
        }

        function loadStats() {
            document.getElementById('totalTrades').textContent = '47';
            document.getElementById('winRate').textContent = '65%';
            document.getElementById('profit').textContent = '$1,245';
            document.getElementById('netPL').textContent = '$892';
        }

        function showTab(tab) {
            const tabs = document.querySelectorAll('.tab-btn');
            tabs.forEach(t => t.classList.remove('active'));
            event.target.classList.add('active');

            if (tab === 'positions') {
                document.getElementById('positionsTab').style.display = 'block';
                document.getElementById('statsTab').style.display = 'none';
            } else {
                document.getElementById('positionsTab').style.display = 'none';
                document.getElementById('statsTab').style.display = 'block';
            }
        }

        // Init
        loadData();

        // Auto-refresh si bot actif
        setInterval(() => {
            if (botRunning) {
                loadData();
            }
        }, 10000);
    </script>
</body>
</html>
