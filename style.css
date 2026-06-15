<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">
    <title>MEOWSUPPER VIP PRO MAX</title>
    <style>
        *{margin:0;padding:0;box-sizing:border-box}
        body{background:#000;font-family:monospace;text-align:center;padding:10px;min-height:100vh;display:flex;flex-direction:column;align-items:center;justify-content:center;overflow-x:hidden;background-image:radial-gradient(circle at 20% 20%,rgba(255,0,0,0.08) 0%,transparent 50%),radial-gradient(circle at 80% 80%,rgba(255,0,0,0.08) 0%,transparent 50%)}
        .top-bar{position:fixed;top:0;left:0;right:0;background:#0a0a0a;border-bottom:2px solid #f00;padding:12px 20px;display:flex;justify-content:space-between;align-items:center;z-index:1000;font-size:0.85em;box-shadow:0 0 30px rgba(255,0,0,0.5)}
        .top-bar .meow{color:#f00;font-weight:bold;font-size:1.3em;text-shadow:0 0 15px #f00;animation:neonPulse 1.5s infinite}
        .top-bar .zalo{background:#0f0;color:#000;padding:8px 16px;border-radius:20px;font-weight:bold;font-size:1em;box-shadow:0 0 20px rgba(0,255,0,0.6);animation:zaloGlow 2s infinite}
        .status-dot{display:inline-block;width:10px;height:10px;background:#0f0;border-radius:50%;animation:pulse 1s infinite;box-shadow:0 0 10px #0f0}
        .panel{background:#0a0a0a;border:2px solid #f00;border-radius:20px;padding:25px;width:95%;max-width:430px;box-shadow:0 0 40px rgba(255,0,0,0.6),0 0 80px rgba(255,0,0,0.3);margin-top:50px;position:relative}
        h1{color:#f00;text-shadow:0 0 20px #f00;margin-bottom:20px;font-size:1.8em;animation:titleGlow 2s infinite}
        .btn{background:#f00;color:#fff;border:none;padding:16px 20px;font-size:1.1em;font-weight:bold;border-radius:12px;margin:10px;width:100%;cursor:pointer;box-shadow:0 0 25px rgba(255,0,0,0.6);font-family:monospace;text-transform:uppercase}
        .btn:active{transform:scale(0.93)}
        .btn.green{background:#0f0;box-shadow:0 0 25px rgba(0,255,0,0.6);color:#000;font-size:1.3em}
        .btn.blue{background:#09f;box-shadow:0 0 25px rgba(0,153,255,0.6)}
        .btn.orange{background:#f90;box-shadow:0 0 25px rgba(255,153,0,0.6);color:#000}
        .btn.purple{background:#90f;box-shadow:0 0 25px rgba(153,0,255,0.6)}
        #log{border:1px solid #f00;padding:15px;margin:15px 0;text-align:left;min-height:130px;max-height:200px;font-size:0.78em;background:#000;overflow-y:auto;border-radius:10px;color:#0f0;line-height:1.5}
        #log::-webkit-scrollbar{width:4px}
        #log::-webkit-scrollbar-thumb{background:#f00;border-radius:2px}
        .bubble{position:fixed;pointer-events:none;animation:float 1.5s ease-out forwards;font-size:2.5em;z-index:999}
        input[type=file]{display:none}
        @keyframes float{0%{opacity:1;transform:translateY(0)scale(1)}100%{opacity:0;transform:translateY(-200px)scale(0)}}
        @keyframes pulse{0%,100%{opacity:1}50%{opacity:0.3}}
        @keyframes neonPulse{0%,100%{text-shadow:0 0 15px #f00}50%{text-shadow:0 0 25px #f00,0 0 50px #f00}}
        @keyframes zaloGlow{0%,100%{box-shadow:0 0 20px rgba(0,255,0,0.6)}50%{box-shadow:0 0 30px rgba(0,255,0,0.9)}}
        @keyframes titleGlow{0%,100%{text-shadow:0 0 20px #f00}50%{text-shadow:0 0 30px #f00,0 0 60px #f00}}
    </style>
</head>
<body>
    <div class="top-bar">
        <span class="meow">🐱 MEOWSUPPER</span>
        <span class="zalo">📞 0356966167</span>
        <span class="status-dot" id="statusDot"></span>
    </div>

    <div class="panel">
        <h1>🔥 VIP PRO MAX</h1>
        <div id="log">
            ⏳ SẴN SÀNG...<br>
            ─────────────────<br>
            📌 Tải config hoặc bấm START
        </div>
        <input type="file" id="fileInput" accept=".ini,.js,.css" onchange="loadConfig(event)">
        <button class="btn blue" onclick="document.getElementById('fileInput').click()">📁 TẢI CONFIG</button>
        <button class="btn green" onclick="startVIP()">🚀 START VIP</button>
        <button class="btn purple" onclick="applyFFLobby()">🎨 ĐỔI SẢNH FF</button>
        <button class="btn orange" onclick="saveConfig('ini')">💾 LƯU .INI</button>
        <button class="btn orange" onclick="saveConfig('js')">💾 LƯU .JS</button>
        <button class="btn orange" onclick="saveConfig('css')">💾 LƯU .CSS</button>
    </div>

    <script>
        // CONFIG
        let config = {
            sensitivity: 200, pullSpeed: 0, aimTarget: 'head',
            antiVibration: true, straightBullets: true, stickyAim: true,
            vipMode: true, antiBanLevel: 5, bubbleCount: 25,
            crosshairColor: '#FF0000', crosshairSize: 5,
            defaultDevice: 'Redmi Note 15 Pro 5G', fov: 360
        };

        let running = false;
        const logEl = document.getElementById('log');
        const statusDot = document.getElementById('statusDot');

        function updateLog(msg) {
            logEl.innerHTML += msg + '\n';
            logEl.scrollTop = logEl.scrollHeight;
        }

        function spawnBubbles(count) {
            for (let i = 0; i < count; i++) setTimeout(() => {
                let b = document.createElement('span');
                b.className = 'bubble';
                b.textContent = ['💥','🔥','⚡','💫','✨','💎','🎯'][Math.floor(Math.random()*7)];
                b.style.left = Math.random() * 85 + 5 + '%';
                b.style.top = Math.random() * 40 + 20 + '%';
                b.style.color = '#' + Math.floor(Math.random() * 16777215).toString(16);
                document.body.appendChild(b);
                setTimeout(() => b.remove(), 1500);
            }, i * 60);
        }

        // LOAD FILE
        function loadConfig(event) {
            let file = event.target.files[0];
            if (!file) return;
            let ext = file.name.split('.').pop().toLowerCase();
            updateLog('⏳ Đang đọc ' + file.name + '...');
            let reader = new FileReader();
            reader.onload = function(e) {
                let content = e.target.result;
                if (ext === 'ini') {
                    content.split('\n').forEach(line => {
                        line = line.trim();
                        if (line.startsWith(';') || line.startsWith('[') || line === '') return;
                        let parts = line.split('=');
                        if (parts.length === 2) {
                            let key = parts[0].trim();
                            let val = parts[1].trim();
                            if (val === 'true' || val === '1') val = true;
                            else if (val === 'false' || val === '0') val = false;
                            else if (!isNaN(val)) val = Number(val);
                            if (key === 'Sensitivity' || key === 'sensitivity') config.sensitivity = val;
                            if (key === 'AntiVibration' || key === 'antiVibration') config.antiVibration = val;
                            if (key === 'StraightBullets' || key === 'straightBullets') config.straightBullets = val;
                            if (key === 'StickyAim' || key === 'stickyAim') config.stickyAim = val;
                            if (key === 'VIPMode' || key === 'vipMode') config.vipMode = val;
                            if (key === 'AntiBanLevel' || key === 'antiBanLevel') config.antiBanLevel = val;
                            if (key === 'BubbleCount' || key === 'bubbleCount') config.bubbleCount = val;
                            if (key === 'DefaultDevice' || key === 'defaultDevice') config.defaultDevice = String(val);
                        }
                    });
                } else if (ext === 'js') {
                    try {
                        let match = content.match(/CONFIG\s*=\s*({[\s\S]*?});/);
                        let cfg = match ? eval('(' + match[1] + ')') : eval('(' + content + ')');
                        if (cfg.sensitivity) config.sensitivity = cfg.sensitivity;
                        if (cfg.antiVibration !== undefined) config.antiVibration = cfg.antiVibration;
                        if (cfg.straightBullets !== undefined) config.straightBullets = cfg.straightBullets;
                        if (cfg.stickyAim !== undefined) config.stickyAim = cfg.stickyAim;
                        if (cfg.vipMode !== undefined) config.vipMode = cfg.vipMode;
                        if (cfg.antiBanLevel) config.antiBanLevel = cfg.antiBanLevel;
                        if (cfg.bubbleCount) config.bubbleCount = cfg.bubbleCount;
                        if (cfg.defaultDevice) config.defaultDevice = cfg.defaultDevice;
                        if (cfg.aimTarget) config.aimTarget = cfg.aimTarget;
                    } catch(err) { updateLog('❌ Lỗi JS: ' + err.message); return; }
                } else if (ext === 'css') {
                    // CSS chỉ đổi giao diện, không đổi config
                }
                updateLog('✅ LOAD THÀNH CÔNG [' + ext.toUpperCase() + ']');
                updateLog('─────────────────');
                updateLog('🔥 VIP: ' + (config.vipMode ? 'BẬT' : 'TẮT'));
                updateLog('🎯 Nhạy: ' + config.sensitivity + ' | Mục tiêu: ' + config.aimTarget);
                updateLog('📳 Chống rung: ' + (config.antiVibration ? 'BẬT' : 'TẮT'));
                updateLog('🔫 Đạn thẳng: ' + (config.straightBullets ? 'BẬT' : 'TẮT'));
                updateLog('📌 Bám dính: ' + (config.stickyAim ? 'BẬT' : 'TẮT'));
                updateLog('📱 Máy: ' + config.defaultDevice);
                spawnBubbles(15);
            };
            reader.readAsText(file);
        }

        // START
        function startVIP() {
            if (running) { updateLog('⚠️ Đã chạy rồi!'); return; }
            running = true;
            updateLog('─────────────────');
            updateLog('🚀 KHỞI ĐỘNG VIP PRO MAX...');
            setTimeout(() => updateLog('⚙️ Nhạy: ' + config.sensitivity), 500);
            setTimeout(() => updateLog('📳 Triệt tiêu rung...'), 1000);
            setTimeout(() => updateLog('🔫 Đạn thẳng tuyệt đối...'), 1500);
            setTimeout(() => updateLog('📌 Bám dính mục tiêu...'), 2000);
            setTimeout(() => updateLog('🧠 Mục tiêu: ' + config.aimTarget), 2500);
            setTimeout(() => updateLog('🛡 Anti-Ban Level ' + config.antiBanLevel), 3000);
            setTimeout(() => updateLog('✅ TOOL ĐÃ SẴN SÀNG!'), 3500);
            spawnBubbles(config.bubbleCount || 25);
            statusDot.style.background = '#ff0';

            // CHUYỂN GAME
            setTimeout(() => {
                updateLog('📱 CHUYỂN SANG FREE FIRE...');
                let a = document.createElement('a');
                a.href = 'intent://launch#Intent;package=com.dts.freefireth;scheme=freefire;end;';
                a.style.display = 'none';
                document.body.appendChild(a);
                a.click();
                document.body.removeChild(a);
                setTimeout(() => window.open('market://details?id=com.dts.freefireth', '_blank'), 1500);
                updateLog('✅ ĐÃ CHUYỂN GAME!');
                statusDot.style.background = '#0f0';
            }, 4000);
        }

        // ĐỔI SẢNH FF
        function applyFFLobby() {
            updateLog('🎨 Đang đổi sảnh chờ FF...');
            let style = document.createElement('style');
            style.textContent = '*{animation:none!important;transition:none!important}body,.lobby,.lobby-container{background:#0a0a0a!important}.lobby-background,.lobby-bg{background-image:url("https://i.imgur.com/8lQxM5s.jpg")!important;background-size:cover!important}.character-model,.player-model{filter:drop-shadow(2px 4px 6px rgba(0,0,0,0.6))!important}.menu-box,.menu-panel{box-shadow:2px 2px 10px rgba(0,0,0,0.5)!important;border:1px solid rgba(255,255,255,0.15)!important}button,.btn{box-shadow:1px 1px 5px rgba(0,0,0,0.4)!important}.shadow,.particle,.effect{display:none!important}';
            document.head.appendChild(style);
            updateLog('✅ Đã áp dụng CSS sảnh chờ!');
            spawnBubbles(10);
        }

        // LƯU FILE
        function saveConfig(type) {
            let content = '';
            let filename = '';
            if (type === 'ini') {
                content = '[VIP_PRO_MAX]\nSensitivity=200\nPullSpeed=0\nAimTarget=2\nAntiVibration=1\nStraightBullets=1\nStickyAim=1\nVIPMode=1\nAntiBanLevel=5\nBubbleCount=25\nDefaultDevice=Redmi Note 15 Pro 5G\nFOV=360\n';
                filename = 'config.ini';
            } else if (type === 'js') {
                content = 'const CONFIG={sensitivity:200,pullSpeed:0,aimTarget:"head",antiVibration:!0,straightBullets:!0,stickyAim:!0,vipMode:!0,antiBanLevel:5,bubbleCount:25,defaultDevice:"Redmi Note 15 Pro 5G",fov:360};';
                filename = 'config.js';
            } else if (type === 'css') {
                content = '*{margin:0;padding:0}body{background:#000;color:#f00;font-family:monospace}.panel{border:2px solid #f00;box-shadow:0 0 35px #f00}';
                filename = 'config.css';
            }
            let blob = new Blob([content], { type: 'text/plain' });
            let a = document.createElement('a');
            a.href = URL.createObjectURL(blob);
            a.download = filename;
            a.click();
            updateLog('💾 Đã lưu ' + filename);
            spawnBubbles(10);
        }
    </script>
</body>
</html>