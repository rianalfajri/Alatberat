<?php
// =========================================================================
// ENGINE BACKEND FULL-STACK CORE v20.99.50 - MAXIMUM FEATURE EXPANSION
// =========================================================================
session_start();

// DATABASE AKUN UTUH & KINI DITAMBAHKAN VALUE LEVEL DAN TIER PROFIL SECARA REAL BACKEND
$server_users_db = [
    'admin1' => [
        'password' => 'admin123', 'name' => 'Rian alfajri', 'role' => 'Super Admin', 'discount' => 0.0,
        'company' => 'Heavy Gear Headquarte', 'joined' => '12 Jan 2024', 'tier' => 'Executive Sovereign', 
        'avatar' => '👨‍✈️', 'level' => 99, 'exp' => 'MAX EXP', 'status' => 'ACTIVE CORE'
    ],
    'vip_client' => [
        'password' => 'vip2026', 'name' => 'Ir. H. Wijaya', 'role' => 'VIP Member', 'discount' => 0.15,
        'company' => 'Wijaya Konstruksi Corp', 'joined' => '05 Feb 2025', 'tier' => 'Diamond VIP Titan', 
        'avatar' => '🏢', 'level' => 50, 'exp' => '7,500 / 10,000', 'status' => 'PREMIUM NODE'
    ],
    'user_biasa' => [
        'password' => 'user123', 'name' => 'Rian Hidayat', 'role' => 'User Pengguna', 'discount' => 0.0,
        'company' => 'Sub-Contractor Node', 'joined' => '20 Mar 2026', 'tier' => 'Standard Node', 
        'avatar' => '👷', 'level' => 12, 'exp' => '1,250 / 2,500', 'status' => 'BASIC NODE'
    ]
];

// Handle Request Login via POST
$error_msg = "";
if ($_SERVER['REQUEST_METHOD'] === 'POST' && isset($_POST['action']) && $_POST['action'] === 'login') {
    $input_user = trim($_POST['username'] ?? '');
    $input_pass = $_POST['password'] ?? '';

    if (isset($server_users_db[$input_user]) && $server_users_db[$input_user]['password'] === $input_pass) {
        $_SESSION['user'] = $server_users_db[$input_user];
        header("Location: " . $_SERVER['PHP_SELF']);
        exit;
    } else {
        $error_msg = "Kredensial salah! Otorisasi ditolak server.";
    }
}

// Handle Logout
if (isset($_GET['action']) && $_GET['action'] === 'logout') {
    session_destroy();
    header("Location: " . $_SERVER['PHP_SELF']);
    exit;
}

// Cek status session backend
$is_logged_in = isset($_SESSION['user']);
$current_user = $is_logged_in ? $_SESSION['user'] : null;
$user_role = $current_user ? $current_user['role'] : 'Guest';
?>
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>RIAN GEAR</title>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Segoe UI', system-ui, sans-serif; }
        :root {
            --bg-main: #010409; --bg-card: #040815; --bg-surface: #0a1126;
            --text-main: #F9FAFB; --text-muted: #6B7280; --border-core: #16223f;
            --primary: #00E5FF; --primary-hover: #00B8D4; --success: #10B981; --danger: #EF4444; --warning: #F59E0B;
            --sidebar-width: 340px;
        }
        body { background-color: var(--bg-main); color: var(--text-main); min-height: 100vh; display: flex; flex-direction: column; overflow-x: hidden; }
        
        /* AUTH OVERLAY */
        .login-gate-overlay { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: radial-gradient(circle at center, #071635 0%, var(--bg-main) 80%); z-index: 9999; display: flex; align-items: center; justify-content: center; padding: 20px; }
        .login-card { background: var(--bg-card); border: 1px solid rgba(0, 229, 255, 0.2); width: 100%; max-width: 480px; border-radius: 16px; padding: 30px; box-shadow: 0 0 50px rgba(0, 229, 255, 0.15); }
        .form-group { margin-bottom: 14px; }
        .form-group label { display: block; font-size: 11px; color: var(--text-muted); margin-bottom: 5px; font-weight: 700; text-transform: uppercase; }
        .form-control { width: 100%; padding: 11px; background-color: var(--bg-surface); border: 1px solid var(--border-core); color: var(--text-main); border-radius: 6px; }

        /* LAYOUT CORE */
        header { background-color: var(--bg-card); border-bottom: 1px solid var(--border-core); position: sticky; top: 0; z-index: 900; }
        .header-container { padding: 12px 30px; display: flex; justify-content: space-between; align-items: center; }
        .brand-core { font-size: 15px; font-weight: 900; color: var(--primary); text-transform: uppercase; letter-spacing: 0.5px; }

        .app-body-wrapper { display: flex; flex: 1; width: 100%; }
        .sidebar-menu { width: var(--sidebar-width); background: var(--bg-card); border-right: 1px solid var(--border-core); padding: 20px 15px; display: flex; flex-direction: column; justify-content: space-between; position: sticky; top: 61px; height: calc(100vh - 61px); overflow-y: auto; }
        .sidebar-links { list-style: none; display: flex; flex-direction: column; gap: 4px; }
        .sidebar-links .section-title { font-size: 10px; font-weight: 800; color: var(--primary); text-transform: uppercase; padding: 10px 12px 4px 12px; }
        
        .sidebar-links button.nav-btn-link, .sidebar-links a.nav-btn-link { background: none; border: none; width: 100%; text-align: left; color: var(--text-main); font-size: 12px; font-weight: 600; padding: 10px 12px; border-radius: 6px; display: flex; align-items: center; gap: 10px; cursor: pointer; text-decoration: none; }
        .sidebar-links button.nav-btn-link.active { color: #000 !important; background-color: var(--primary); font-weight: 700; }
        
        .role-tag-badge { font-size: 8px; font-weight: 800; padding: 2px 6px; border-radius: 4px; text-transform: uppercase; margin-left: auto; }
        .tag-admin { background: rgba(239, 68, 68, 0.2); color: var(--danger); border: 1px solid var(--danger); }
        .tag-vip { background: rgba(245, 158, 11, 0.2); color: var(--warning); border: 1px solid var(--warning); }
        .tag-all { background: rgba(16, 185, 129, 0.2); color: var(--success); border: 1px solid var(--success); }

        /* PANELS WORKSPACE */
        .workspace-content { flex: 1; padding: 30px; display: grid; grid-template-columns: 1fr 400px; gap: 25px; }
        .panel { background-color: var(--bg-card); border: 1px solid var(--border-core); border-radius: 12px; padding: 24px; margin-bottom: 25px; }
        .panel-title { font-size: 11px; font-weight: 800; text-transform: uppercase; margin-bottom: 18px; display: flex; align-items: center; gap: 8px; border-bottom: 1px solid var(--border-core); padding-bottom: 12px; color: var(--primary); }
        
        .view-pane { display: none; }
        .view-pane.active { display: block; }

        /* VIEWPORT GRID */
        .products-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(220px, 1fr)); gap: 20px; }
        .product-card { background-color: var(--bg-surface); border: 2px solid var(--border-core); border-radius: 12px; overflow: hidden; display: flex; flex-direction: column; }
        .catalog-3d-viewport { width: 100%; height: 180px; background: radial-gradient(circle at center, #040e22 0%, #01040a 100%); }
        .product-details { padding: 14px; background: #030710; display: flex; flex-direction: column; flex: 1; justify-content: space-between; }
        
        .btn { padding: 11px 18px; border-radius: 6px; font-weight: 700; font-size: 11px; cursor: pointer; border: none; display: inline-flex; align-items: center; justify-content: center; gap: 6px; text-transform: uppercase; }
        .btn-primary { background-color: var(--primary); color: #000; }
        .btn-warning { background-color: var(--warning); color: #000; }
        .btn-danger { background-color: var(--danger); color: #fff; }
        .btn-block { width: 100%; }

        .cart-item-row { display: flex; justify-content: space-between; align-items: center; padding: 10px 0; border-bottom: 1px dashed var(--border-core); font-size: 12px; }
        .invoice-box { background-color: var(--bg-surface); border: 1px solid var(--border-core); padding: 18px; border-radius: 8px; margin-top: 15px; display: flex; flex-direction: column; gap: 8px; }
        .invoice-line { display: flex; justify-content: space-between; font-size: 12px; }
        
        /* EXPANSION DESIGN METRICS */
        .dynamic-3d-viewport { width: 100%; height: 260px; background: radial-gradient(circle at center, #04142c 0%, #010512 100%); border-radius: 10px; border: 1px solid var(--border-core); margin-bottom: 15px; }
        .profile-data-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; margin-top: 15px; }
        .data-node { background: var(--bg-surface); padding: 12px; border-radius: 6px; border: 1px solid var(--border-core); }
        .level-progress-bar { background: #16223f; width: 100%; height: 8px; border-radius: 4px; margin-top: 5px; overflow: hidden; }
        .level-progress-fill { background: var(--primary); height: 100%; transition: width 0.4s ease; }

        /* ACCOUNT CONTROL MATRIX STYLES */
        .control-panel-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 15px; margin-top: 15px; }
        .control-card { background: var(--bg-surface); border: 1px solid var(--border-core); padding: 15px; border-radius: 8px; }

        #systemToast { position: fixed; bottom: 25px; right: 25px; background: #041226; border: 1px solid var(--primary); padding: 14px 22px; border-radius: 8px; font-size: 12px; font-weight: 600; color: #fff; z-index: 100000; transform: translateY(150%); transition: transform 0.3s ease; }
        #systemToast.show { transform: translateY(0); }
    </style>
</head>
<body>

    <?php if (!$is_logged_in): ?>
    <div class="login-gate-overlay">
        <div class="login-card">
            <div style="text-align: center; margin-bottom: 20px;">
                <span style="font-size: 40px;">🛡️</span>
                <h2 style="font-size: 16px; font-weight: 900; color: var(--primary); text-transform: uppercase;">RIAN GEAR</h2>
                <?php if ($error_msg): ?>
                    <p style="color: var(--danger); font-size: 12px; margin-top: 5px; font-weight: bold;"><?= $error_msg ?></p>
                <?php else: ?>
                    <p style="font-size: 11px; color: var(--text-muted); margin-top: 5px;">Gunakan node akun: admin1, vip_client, atau user_biasa</p>
                <?php endif; ?>
            </div>
            <form method="POST" action="">
                <input type="hidden" name="action" value="login">
                <div class="form-group">
                    <label>ID Kredensial Korporat</label>
                    <input type="text" name="username" class="form-control" placeholder="ID Akun..." required autocomplete="off">
                </div>
                <div class="form-group" style="margin-bottom: 20px;">
                    <label>Token Sandi Enkripsi</label>
                    <input type="password" name="password" class="form-control" placeholder="••••••••" required>
                </div>
                <button type="submit" class="btn btn-primary btn-block">Otorisasi & Masuk Sektor</button>
            </form>
        </div>
    </div>
    <?php endif; ?>

    <header>
        <div class="header-container">
            <div class="brand-core">RIAN GEAR</div>
            <?php if ($is_logged_in): ?>
                <div style="display:flex; gap:10px; align-items:center;">
                    <span style="font-size:11px; background:var(--bg-surface); padding: 5px 10px; border-radius:4px; border:1px solid var(--border-core);">SERVER DATE: 2026-07-12</span>
                    <a href="?action=logout" class="btn btn-danger" style="padding: 6px 12px; font-size: 10px;">❌ DISCONNECT</a>
                </div>
            <?php endif; ?>
        </div>
    </header>

    <div class="app-body-wrapper">
        <aside class="sidebar-menu">
            <ul class="sidebar-links" id="sidebarLinkContainer">
                <li class="section-title">Global Sectors</li>
                <li><button class="nav-btn-link active" onclick="navigatePanel('dashboard')">📊 Live 3D Catalog POS <span class="role-tag-badge tag-all">ALL</span></button></li>
                <li><button class="nav-btn-link" onclick="navigatePanel('cart-view')">🛒 Menu Keranjang Detail <span class="role-tag-badge tag-all">ALL</span></button></li>
                <li><button class="nav-btn-link" onclick="navigatePanel('profile')">👤 Tier Profil & Level <span class="role-tag-badge tag-all">ALL</span></button></li>
                <li><button class="nav-btn-link" onclick="navigatePanel('account-control')">🛠️ Menu Account Control <span class="role-tag-badge tag-all">ALL</span></button></li>
                
                <?php if ($user_role === 'Super Admin' || $user_role === 'VIP Member'): ?>
                <li class="section-title">VIP Client Sectors</li>
                <li><button class="nav-btn-link" onclick="navigatePanel('battle')">🏟️ Fleet Battle Arena (3D) <span class="role-tag-badge tag-vip">VIP+</span></button></li>
                <li><button class="nav-btn-link" onclick="navigatePanel('barracks')">🏗️ Builder Barracks (3D) <span class="role-tag-badge tag-vip">VIP+</span></button></li>
                <?php endif; ?>
                
                <?php if ($user_role === 'Super Admin'): ?>
                <li class="section-title">Super Admin Core Matrices</li>
                <li>
                    <button class="nav-btn-link" onclick="navigatePanel('restricted')">
                        <span>收 Neraca Finansial (🔒)</span>
                        <span class="role-tag-badge tag-admin">ADMIN</span>
                    </button>
                </li>
                <?php endif; ?>
            </ul>

            <div style="background: var(--bg-surface); padding: 14px; border-radius: 10px; border: 1px solid var(--border-core);">
                <div style="display: flex; align-items: center; gap: 10px;">
                    <span style="font-size: 24px;"><?= $current_user ? $current_user['avatar'] : '👤' ?></span>
                    <div>
                        <div style="font-size: 12px; font-weight:800;"><?= $current_user ? $current_user['name'] : 'Guest Node' ?></div>
                        <div style="font-size: 10px; color: var(--primary); font-weight: 700;"><?= $user_role ?> [LV <?= $current_user ? $current_user['level'] : 0 ?>]</div>
                    </div>
                </div>
            </div>
        </aside>

        <main class="workspace-content">
            <div class="left-workspace-column">
                
                <div id="view-dashboard" class="view-pane active">
                    <div class="panel">
                        <div class="panel-title">📦 Katalog Konstruksi Armada 3D Live Engine (High Lightning Mod)</div>
                        <div class="products-grid">
                            <div class="product-card">
                                <div class="catalog-3d-viewport" id="canvas-container-E01"></div>
                                <div class="product-details">
                                    <div style="font-weight:bold; font-size:13px;">Excavator Titan Breaker X1</div>
                                    <button class="btn btn-primary btn-block" style="margin-top:10px;" onclick="alterCartQuantity('E01', 3500000, 'Excavator Titan Breaker X1', 1)">+ Sewa (3.5M)</button>
                                </div>
                            </div>
                            <div class="product-card">
                                <div class="catalog-3d-viewport" id="canvas-container-L01"></div>
                                <div class="product-details">
                                    <div style="font-weight:bold; font-size:13px;">Goliath Heavy Crane C5</div>
                                    <button class="btn btn-primary btn-block" style="margin-top:10px;" onclick="alterCartQuantity('L01', 7200000, 'Goliath Heavy Crane C5', 1)">+ Sewa (7.2M)</button>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div id="view-cart-view" class="view-pane">
                    <div class="panel">
                        <div class="panel-title">🛒 Log Manifest & Manajemen Keranjang Fleet Server</div>
                        <div style="background: var(--bg-surface); padding: 20px; border-radius: 8px; border:1px solid var(--border-core);">
                            <div id="extendedCartTable" style="font-size:13px;">
                                <p style="color:var(--text-muted)">Keranjang Anda kosong. Silakan tambahkan unit armada dari katalog.</p>
                            </div>
                        </div>
                    </div>
                </div>

                <div id="view-profile" class="view-pane">
                    <div class="panel">
                        <div class="panel-title">👤 Member Account Security Profile Center & Level System</div>
                        <div class="dynamic-3d-viewport" id="profile3DContainer"></div>
                        <div class="profile-data-grid">
                            <div class="data-node"><strong>Nama Node:</strong> <span><?= $current_user ? $current_user['name'] : '-' ?></span></div>
                            <div class="data-node"><strong>Otoritas Role:</strong> <span><?= $user_role ?></span></div>
                            <div class="data-node"><strong>Corporate Tier:</strong> <span style="color:var(--primary); font-weight:bold;"><?= $current_user ? $current_user['tier'] : '-' ?></span></div>
                            <div class="data-node"><strong>Node Level:</strong> <span style="color:var(--warning); font-weight:bold;">LV <?= $current_user ? $current_user['level'] : 0 ?></span></div>
                            <div class="data-node" style="grid-column: span 2;">
                                <strong>Rasio EXP Penyewaan:</strong> <span style="float:right; font-size:11px;"><?= $current_user ? $current_user['exp'] : '0/0' ?></span>
                                <div class="level-progress-bar">
                                    <div class="level-progress-fill" style="width: <?= ($user_role==='Super Admin') ? '100%' : (($user_role==='VIP Member') ? '75%' : '50%') ?>;"></div>
                                </div>
                            </div>
                            <div class="data-node"><strong>Status Sistem:</strong> <span style="color:var(--success)"><?= $current_user ? $current_user['status'] : 'UNVERIFIED' ?></span></div>
                            <div class="data-node"><strong>Sisa Saldo Riset:</strong> <span style="color:var(--success)">Rp 25.000.000.000</span></div>
                        </div>
                        <button class="btn btn-warning btn-block" style="margin-top:15px;" onclick="triggerProfileInteraction()">Animasikan Reaktor Profil</button>
                    </div>
                </div>

                <div id="view-account-control" class="view-pane">
                    <div class="panel">
                        <div class="panel-title">🛠️ Sektor Konfigurasi & Account Control Matrix</div>
                        <div class="control-panel-grid">
                            <div class="control-card">
                                <h4 style="font-size:12px; margin-bottom:8px; color:var(--primary);">🔒 Enkripsi Sesi</h4>
                                <p style="font-size:11px; color:var(--text-muted); margin-bottom:10px;">Ganti status penyamaran node jaringan atau enkripsi ulang token.</p>
                                <button class="btn btn-warning" style="padding:6px 10px; font-size:10px;" onclick="showSystemToast('Enkripsi ulang berhasil di-generate!')">Re-Key Token</button>
                            </div>
                            <div class="control-card">
                                <h4 style="font-size:12px; margin-bottom:8px; color:var(--success);">🌐 Lokasi Node</h4>
                                <p style="font-size:11px; color:var(--text-muted); margin-bottom:10px;">Lokasi Server Aktif saat ini terikat pada IP Terproteksi Nasional.</p>
                                <button class="btn btn-primary" style="padding:6px 10px; font-size:10px;" onclick="showSystemToast('Lokasi Jaringan Diperbarui!')">Ping Cluster</button>
                            </div>
                        </div>
                    </div>
                </div>

                <?php if ($user_role === 'Super Admin' || $user_role === 'VIP Member'): ?>
                <div id="view-battle" class="view-pane">
                    <div class="panel">
                        <div class="panel-title">🏟️ Fleet Battle Arena Tactical Mode</div>
                        <div class="dynamic-3d-viewport" id="battleArena3DContainer"></div>
                        <button class="btn btn-primary btn-block" onclick="triggerArenaInteraction()">Kirim Sinyal Tempur (Deploy Hologram)</button>
                    </div>
                </div>

                <div id="view-barracks" class="view-pane">
                    <div class="panel">
                        <div class="panel-title">🏗️ Project Builder Barracks Terminal</div>
                        <div class="dynamic-3d-viewport" id="barracks3DContainer"></div>
                        <button class="btn btn-warning btn-block" onclick="triggerBarracksInteraction()">Nyalakan Reaktor Tukang</button>
                    </div>
                </div>
                <?php endif; ?>

                <?php if ($user_role === 'Super Admin'): ?>
                <div id="view-restricted" class="view-pane">
                    <div class="panel">
                        <div class="panel-title" style="color:var(--success)">... CORE ACCESS GRANTED SERVER-SIDE ...</div>
                        <div style="background:#020617; border:1px solid var(--success); padding: 20px; border-radius:6px;">
                            <p>Brankas Dana Konstruksi Utama: <strong>Rp 847.250.000.000,00</strong></p>
                        </div>
                    </div>
                </div>
                <?php endif; ?>

            </div>

            <div class="right-workspace-column">
                <div class="panel">
                    <div class="panel-title">🛒 Kasir POS Terminal & Billing Invoice</div>
                    <div id="cartBasketZone" style="max-height: 180px; overflow-y: auto; margin-bottom: 15px;"></div>
                    <div class="invoice-box">
                        <div class="invoice-line"><span>Subtotal Armada:</span><span id="invSubtotalNode">Rp 0</span></div>
                        <div class="invoice-line"><span style="color:var(--warning);">Diskon Tier Akun:</span><span id="invDiscountNode"><?= ($current_user ? $current_user['discount'] : 0) * 100 ?>%</span></div>
                        <div class="invoice-line"><span>PPN (11%):</span><span id="invPpnNode">Rp 0</span></div>
                        <div class="invoice-line"><span>Pajak Logistik:</span><span>Rp 150.000</span></div>
                        <div class="invoice-line" style="font-size:14px; font-weight:800; padding-top:4px;"><span>Grand Total:</span><strong id="invTotalNode" style="color:var(--primary);">Rp 0</strong></div>
                    </div>
                    <button class="btn btn-primary btn-block" style="margin-top:12px;" onclick="executeCheckoutOrder()">Eksekusi Distribusi Sewa</button>
                </div>
            </div>
        </main>
    </div>

    <div id="systemToast"><span id="toastMessage">Sistem Terkoneksi.</span></div>

    <script>
        const serverUserDiscount = <?= $current_user ? $current_user['discount'] : 0 ?>;
        let activeCart = {}; let cachedScenes = {};

        function navigatePanel(targetId) {
            document.querySelectorAll('#sidebarLinkContainer button.nav-btn-link').forEach(b => b.classList.remove('active'));
            if(event && event.currentTarget.tagName === 'BUTTON') event.currentTarget.classList.add('active');
            
            document.querySelectorAll('.view-pane').forEach(p => p.classList.remove('active'));
            const element = document.getElementById('view-' + targetId);
            if(element) {
                element.classList.add('active');
                if(['battle', 'barracks', 'profile'].includes(targetId)) {
                    initOrUpdateMenuHologram(targetId);
                }
            }
        }

        function alterCartQuantity(prodId, price, name, delta) {
            if(!activeCart[prodId]) activeCart[prodId] = { qty: 0, price: price, name: name };
            activeCart[prodId].qty += delta;
            if(activeCart[prodId].qty <= 0) delete activeCart[prodId];
            renderInvoiceCart();
            updateExtendedCartMenu();
        }

        function renderInvoiceCart() {
            const container = document.getElementById('cartBasketZone');
            if(!container) return;
            container.innerHTML = ""; let subtotal = 0;
            for (const key in activeCart) {
                const item = activeCart[key]; subtotal += item.price * item.qty;
                container.innerHTML += `<div class="cart-item-row"><span>${item.name} (x${item.qty})</span><strong>Rp ${(item.price * item.qty).toLocaleString('id-ID')}</strong></div>`;
            }
            const finalTax = (subtotal - (subtotal * serverUserDiscount)) * 0.11;
            const grand = (subtotal - (subtotal * serverUserDiscount)) + finalTax + (subtotal > 0 ? 150000 : 0);
            
            document.getElementById('invSubtotalNode').innerText = `Rp ${subtotal.toLocaleString('id-ID')}`;
            document.getElementById('invPpnNode').innerText = `Rp ${finalTax.toLocaleString('id-ID')}`;
            document.getElementById('invTotalNode').innerText = `Rp ${grand.toLocaleString('id-ID')}`;
        }

        // UPDATE DATA UNTUK MENU KERANJANG DETAIL SEKTOR KIRI
        function updateExtendedCartMenu() {
            const extContainer = document.getElementById('extendedCartTable');
            if(!extContainer) return;
            
            let html = ""; let count = 0;
            for (const key in activeCart) {
                count++; const item = activeCart[key];
                html += `
                <div style="display:flex; justify-content:space-between; align-items:center; border-bottom:1px solid var(--border-core); padding:12px 0;">
                    <div>
                        <strong>${item.name}</strong><br>
                        <span style="color:var(--text-muted); font-size:11px;">Harga Satuan: Rp ${item.price.toLocaleString('id-ID')}</span>
                    </div>
                    <div style="display:flex; align-items:center; gap:10px;">
                        <button class="btn btn-warning" style="padding:4px 8px; font-size:10px;" onclick="alterCartQuantity('${key}', ${item.price}, '${item.name}', -1)">-</button>
                        <strong style="color:var(--primary); font-size:14px;">${item.qty}</strong>
                        <button class="btn btn-primary" style="padding:4px 8px; font-size:10px;" onclick="alterCartQuantity('${key}', ${item.price}, '${item.name}', 1)">+</button>
                    </div>
                </div>`;
            }
            if(count === 0) {
                extContainer.innerHTML = `<p style="color:var(--text-muted)">Keranjang Anda kosong. Silakan tambahkan unit armada dari katalog.</p>`;
            } else {
                extContainer.innerHTML = html;
            }
        }

        function executeCheckoutOrder() { alert("Pemesanan aman terkirim ke database server!"); activeCart = {}; renderInvoiceCart(); updateExtendedCartMenu(); }
        function showSystemToast(msg) { const t = document.getElementById('systemToast'); t.innerText = msg; t.classList.add('show'); setTimeout(() => t.classList.remove('show'), 2500); }

        // ENGINE CAHAYA PRESET THREE.JS GAME STUDIO v2
        function initOrUpdateMenuHologram(type) {
            let containerId = type === 'battle' ? 'battleArena3DContainer' : (type === 'barracks' ? 'barracks3DContainer' : 'profile3DContainer');
            const container = document.getElementById(containerId);
            if(!container || container.children.length > 0) return;

            const scene = new THREE.Scene();
            const camera = new THREE.PerspectiveCamera(45, container.clientWidth / container.clientHeight, 0.1, 100);
            camera.position.set(0, 0, 5);

            const renderer = new THREE.WebGLRenderer({ antialias: true, alpha: true });
            renderer.setSize(container.clientWidth, container.clientHeight);
            container.appendChild(renderer.domElement);

            scene.add(new THREE.AmbientLight(0x0e1e38, 3.0));
            const dirLight = new THREE.DirectionalLight(0x00E5FF, 4.0); dirLight.position.set(5, 5, 5); scene.add(dirLight);
            const pointLight = new THREE.PointLight(0xF59E0B, 3.0, 15); pointLight.position.set(-3, -3, 3); scene.add(pointLight);

            let geometry;
            if(type === 'battle') geometry = new THREE.OctahedronGeometry(1.3, 0);
            else if(type === 'barracks') geometry = new THREE.TorusKnotGeometry(0.6, 0.2, 70, 10);
            else geometry = new THREE.CylinderGeometry(1.1, 1.1, 0.2, 32, 1, true); 

            const material = new THREE.MeshStandardMaterial({ 
                color: type === 'profile' ? 0x00E5FF : (type === 'barracks' ? 0xF59E0B : 0x10B981), 
                wireframe: type !== 'barracks', metalness: 0.9, roughness: 0.1 
            });

            const mesh = new THREE.Mesh(geometry, material);
            scene.add(mesh);
            cachedScenes[type] = mesh;

            function animate() {
                requestAnimationFrame(animate);
                mesh.rotation.x += 0.01; mesh.rotation.y += 0.015;
                renderer.render(scene, camera);
            }
            animate();
        }

        function triggerProfileInteraction() {
            showSystemToast("Sinkronisasi Avatar Kredensial!");
            if(cachedScenes['profile']) { cachedScenes['profile'].scale.set(1.3, 1.3, 1.3); setTimeout(() => cachedScenes['profile'].scale.set(1,1,1), 400); }
        }
        function triggerArenaInteraction() {
            showSystemToast("Hologram Arena Dipercepat!");
            if(cachedScenes['battle']) cachedScenes['battle'].rotation.y += 1.5;
        }
        function triggerBarracksInteraction() {
            showSystemToast("Barracks Overdrive Active!");
            if(cachedScenes['barracks']) { cachedScenes['barracks'].scale.set(1.4, 1.4, 1.4); setTimeout(() => cachedScenes['barracks'].scale.set(1,1,1), 500); }
        }

        // 3D MODEL CATALOG BUILDER
        function buildCatalog3D(id, designType) {
            const el = document.getElementById(id); if(!el) return;
            const scene = new THREE.Scene();
            const camera = new THREE.PerspectiveCamera(45, el.clientWidth / el.clientHeight, 0.1, 100); camera.position.set(0, 2, 5);

            const ren = new THREE.WebGLRenderer({ antialias: true, alpha: true }); ren.setSize(el.clientWidth, el.clientHeight); el.appendChild(ren.domElement);

            scene.add(new THREE.AmbientLight(0x0a1a35, 2.5));
            const keyLight = new THREE.DirectionalLight(0x00E5FF, 3.5); keyLight.position.set(3, 4, 3); scene.add(keyLight);
            const fillLight = new THREE.PointLight(0xF59E0B, 2.0, 10); fillLight.position.set(-3, 2, -2); scene.add(fillLight);

            const group = new THREE.Group();
            const bodyMat = new THREE.MeshStandardMaterial({ color: 0x112756, metalness: 0.8, roughness: 0.2 });
            const jointMat = new THREE.MeshStandardMaterial({ color: 0xF59E0B, metalness: 0.9, roughness: 0.1 });

            if (designType === 'excavator') {
                const trackBase = new THREE.Mesh(new THREE.BoxGeometry(1.5, 0.4, 1.3), bodyMat);
                const cabin = new THREE.Mesh(new THREE.BoxGeometry(0.7, 0.7, 0.7), jointMat); cabin.position.set(-0.2, 0.5, 0);
                const arm = new THREE.Mesh(new THREE.CylinderGeometry(0.08, 0.08, 1.4), jointMat); arm.position.set(0.4, 0.8, 0); arm.rotation.z = -0.5;
                group.add(trackBase, cabin, arm);
            } else {
                const towerBase = new THREE.Mesh(new THREE.CylinderGeometry(0.15, 0.2, 2.2), bodyMat);
                const boomJib = new THREE.Mesh(new THREE.BoxGeometry(2.0, 0.12, 0.15), jointMat); boomJib.position.y = 1.1; boomJib.position.x = 0.3;
                group.add(towerBase, boomJib);
            }
            scene.add(group);

            function anim() { requestAnimationFrame(anim); group.rotation.y += 0.015; ren.render(scene, camera); } anim();
        }

        window.addEventListener('DOMContentLoaded', () => {
            buildCatalog3D('canvas-container-E01', 'excavator');
            buildCatalog3D('canvas-container-L01', 'crane');
            renderInvoiceCart();
            updateExtendedCartMenu();
            <?php if($is_logged_in): ?> showSystemToast("Koneksi Core Jaringan Stabil!"); <?php endif; ?>
        });
    </script>
</body>
</html>
