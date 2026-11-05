<!DOCTYPE html>
<html lang="zh-CN" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>IYKYK TICKET | 韩国本土预售票务管家 · Korean Presale Concierge</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&family=Noto+Sans+KR:wght@300;400;500;700&display=swap" rel="stylesheet">
    <!-- Lucide Icons -->
    <script src="https://unpkg.com/lucide@latest"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        kpink: {
                            50: '#FFF5F7',
                            100: '#FFE3E8',
                            200: '#FFD6E0',
                            300: '#FFB3C6',
                            400: '#FF85A1',
                            500: '#FF5C8A',
                            600: '#E03A6E',
                            700: '#C72557'
                        },
                        ktext: {
                            primary: '#2D3748',
                            secondary: '#718096',
                            light: '#A0AEC0'
                        },
                        kbg: '#FCF8F9'
                    },
                    fontFamily: {
                        sans: ['Inter', 'Noto Sans KR', 'sans-serif'],
                    },
                    borderRadius: {
                        '3xl': '1.75rem',
                        '4xl': '2.25rem',
                        '5xl': '2.75rem'
                    },
                    boxShadow: {
                        'soft': '0 12px 32px -8px rgba(255, 179, 198, 0.3)',
                        'soft-lg': '0 20px 48px -12px rgba(255, 133, 161, 0.35)',
                        'card': '0 8px 30px -6px rgba(113, 128, 150, 0.08)'
                    }
                }
            }
        }
    </script>
    <style>
        body {
            background-color: #FCF8F9;
            color: #2D3748;
            font-family: 'Inter', 'Noto Sans KR', sans-serif;
            overflow-x: hidden;
        }

        @keyframes floatSlow {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-6px) rotate(1deg); }
        }

        @keyframes pulseGlow {
            0%, 100% { opacity: 0.35; transform: scale(1); }
            50% { opacity: 0.6; transform: scale(1.05); }
        }

        .animate-float-slow {
            animation: floatSlow 6s ease-in-out infinite;
        }

        .animate-glow {
            animation: pulseGlow 7s ease-in-out infinite;
        }

        .k-glass {
            background: rgba(255, 255, 255, 0.92);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border: 1px solid rgba(255, 214, 224, 0.7);
        }

        .no-scrollbar::-webkit-scrollbar {
            display: none;
        }
        .no-scrollbar {
            -ms-overflow-style: none;
            scrollbar-width: none;
        }
    </style>
</head>
<body class="min-h-screen flex flex-col relative selection:bg-kpink-200 selection:text-kpink-600">

    <!-- SUBTLE BACKGROUND DECORATIONS -->
    <div class="absolute inset-0 pointer-events-none z-0 overflow-hidden">
        <div class="absolute -top-24 -left-20 w-[32rem] h-[32rem] bg-kpink-100/70 rounded-full blur-3xl opacity-70 animate-glow"></div>
        <div class="absolute top-1/3 -right-24 w-[28rem] h-[28rem] bg-kpink-200/50 rounded-full blur-3xl opacity-50 animate-glow" style="animation-delay: 2.5s;"></div>
        <div class="absolute bottom-1/4 left-1/6 w-[30rem] h-[30rem] bg-rose-100/60 rounded-full blur-3xl opacity-60 animate-glow" style="animation-delay: 4.5s;"></div>
        <div class="absolute inset-0 opacity-[0.02]" style="background-image: radial-gradient(#2D3748 1px, transparent 1px); background-size: 28px 28px;"></div>
    </div>

    <!-- MAIN HEADER -->
    <header class="w-full max-w-6xl mx-auto px-4 sm:px-8 pt-6 pb-2 z-20 relative">
        <div class="k-glass rounded-full px-5 sm:px-7 py-3.5 flex items-center justify-between shadow-card">
            <a href="#" class="flex items-center gap-3 group">
                <div class="w-10 h-10 rounded-full bg-gradient-to-tr from-kpink-400 via-kpink-300 to-kpink-200 flex items-center justify-center text-white font-black text-sm shadow-sm group-hover:scale-105 transition-transform">
                    IY
                </div>
                <div class="flex flex-col">
                    <span class="font-extrabold tracking-tight text-lg text-ktext-primary flex items-center gap-1.5">
                        IYKYK <span class="text-[10px] font-medium px-2 py-0.5 rounded-full bg-kpink-50 text-kpink-600 border border-kpink-200">Ticket</span>
                    </span>
                </div>
            </a>

            <nav class="hidden md:flex items-center gap-6 text-xs sm:text-sm font-medium text-ktext-secondary">
                <a href="#services" class="hover:text-kpink-500 transition-colors" data-i18n="navServices">服务优势</a>
                <a href="#concerts" class="hover:text-kpink-500 transition-colors" data-i18n="navConcerts">演出 Schedule</a>
                <a href="#calculator" class="hover:text-kpink-500 transition-colors" data-i18n="navCalc">试算测算</a>
                <a href="#orders" class="hover:text-kpink-500 transition-colors" data-i18n="navOrders">订单查询</a>
                <a href="#trust" class="hover:text-kpink-500 transition-colors" data-i18n="navTrust">安全保障</a>
            </nav>

            <div class="flex items-center gap-2.5">
                <!-- Language Selector -->
                <div class="relative">
                    <select id="language-picker" aria-label="Select language" onchange="setSiteLanguage(this.value)" class="bg-white/90 border border-kpink-200 rounded-full px-3 py-1.5 text-xs font-semibold text-ktext-primary focus:outline-none focus:ring-2 focus:ring-kpink-300 cursor-pointer shadow-sm">
                        <option value="zh">中文</option>
                        <option value="en">English</option>
                        <option value="ko">한국어</option>
                        <option value="ja">日本語</option>
                    </select>
                </div>

                <button onclick="scrollToSection('orders')" class="hidden sm:flex items-center gap-1.5 bg-white border border-kpink-200 hover:bg-kpink-50 text-ktext-primary font-medium text-xs px-4 py-2 rounded-full transition-all">
                    <i data-lucide="search" class="w-3.5 h-3.5 text-kpink-500"></i>
                    <span data-i18n="btnSearch">查询订单</span>
                </button>
                <button onclick="scrollToSection('concerts')" class="bg-gradient-to-r from-kpink-400 to-kpink-500 hover:from-kpink-500 hover:to-kpink-600 text-white font-semibold text-xs sm:text-sm px-5 py-2 rounded-full shadow-soft hover:shadow-soft-lg transition-all transform hover:-translate-y-0.5">
                    <span data-i18n="btnBook">立即预订</span>
                </button>
            </div>
        </div>
    </header>

    <!-- MAIN CONTENT -->
    <main class="flex-grow z-10 max-w-6xl mx-auto px-4 sm:px-6 py-6 space-y-16">

        <!-- SERVICE NOTICE BANNER -->
        <div class="max-w-5xl mx-auto p-4 sm:p-5 rounded-3xl border border-kpink-300 bg-kpink-50/90 shadow-sm text-xs sm:text-sm text-ktext-primary flex items-start gap-3" role="note" id="service-notice">
            <div class="w-7 h-7 rounded-full bg-kpink-400 text-white flex items-center justify-center shrink-0 mt-0.5">
                <i data-lucide="alert-circle" class="w-4 h-4"></i>
            </div>
            <div class="leading-relaxed">
                <strong class="font-bold text-kpink-600" data-i18n="noticeTitle">限量预约服务</strong>
                <span data-i18n="noticeBody">：目前仅接受少量购票协助申请。提交预约后请添加微信客服 Chloe_ii0514 确认是否接单、最终报价及退款条款；未经确认请勿付款。预约信息目前仅保存在提交者浏览器中，团队不会自动收到。</span>
            </div>
        </div>

        <!-- HERO SECTION -->
        <section class="relative pt-4 pb-4 text-center flex flex-col items-center justify-center">
            
            <div class="inline-flex items-center gap-2 px-4 py-1.5 rounded-full bg-white/90 border border-kpink-200 text-xs font-semibold text-kpink-600 shadow-sm mb-6 animate-float-slow">
                <span class="w-2 h-2 rounded-full bg-kpink-400 animate-ping"></span>
                <span data-i18n="heroBadge">IYKYK / 韩国本土预售优先抢订服务</span>
            </div>

            <h1 class="text-3xl sm:text-5xl md:text-6xl font-black tracking-tight text-ktext-primary max-w-3xl leading-tight mb-3" data-i18n="heroTitle1">
                直通韩国本土优先预售通道
            </h1>
            <h2 class="text-2xl sm:text-4xl md:text-5xl font-black tracking-tight bg-clip-text text-transparent bg-gradient-to-r from-kpink-500 via-kpink-400 to-rose-400 max-w-3xl leading-tight mb-6" data-i18n="heroTitle2">
                安全·透明·极速抢占优质席位
            </h2>

            <p class="text-xs sm:text-sm md:text-base text-ktext-secondary max-w-2xl font-normal leading-relaxed mb-8" data-i18n="heroDesc">
                由专业团队提供韩国本土实名认证账号与优先开售抢订支持。绕过 Global 通道漫长等候与天价黄牛，采用“抢到后付服务费 / 未成功定金全退”安全保障机制。
            </p>

            <!-- Value Highlights -->
            <div class="grid grid-cols-2 sm:grid-cols-4 gap-3 sm:gap-4 w-full max-w-3xl mb-8">
                <div class="k-glass p-4 rounded-3xl text-center shadow-card hover:border-kpink-300 transition-all">
                    <div class="w-8 h-8 mx-auto mb-2 rounded-full bg-kpink-50 flex items-center justify-center text-kpink-500">
                        <i data-lucide="shield-check" class="w-4 h-4"></i>
                    </div>
                    <div class="text-xs font-bold text-ktext-primary" data-i18n="v1Title">成功后再付尾款</div>
                    <div class="text-[11px] text-ktext-light mt-0.5" data-i18n="v1Sub">第三方托管低风险</div>
                </div>
                <div class="k-glass p-4 rounded-3xl text-center shadow-card hover:border-kpink-300 transition-all">
                    <div class="w-8 h-8 mx-auto mb-2 rounded-full bg-kpink-50 flex items-center justify-center text-kpink-500">
                        <i data-lucide="zap" class="w-4 h-4"></i>
                    </div>
                    <div class="text-xs font-bold text-ktext-primary" data-i18n="v2Title">本土提前优先购票</div>
                    <div class="text-[11px] text-ktext-light mt-0.5" data-i18n="v2Sub">优先抢占内场与VIP</div>
                </div>
                <div class="k-glass p-4 rounded-3xl text-center shadow-card hover:border-kpink-300 transition-all">
                    <div class="w-8 h-8 mx-auto mb-2 rounded-full bg-kpink-50 flex items-center justify-center text-kpink-500">
                        <i data-lucide="user-check" class="w-4 h-4"></i>
                    </div>
                    <div class="text-xs font-bold text-ktext-primary" data-i18n="v3Title">在韩实名认证账号</div>
                    <div class="text-[11px] text-ktext-light mt-0.5" data-i18n="v3Sub">避开海外 IP 排队限制</div>
                </div>
                <div class="k-glass p-4 rounded-3xl text-center shadow-card hover:border-kpink-300 transition-all">
                    <div class="w-8 h-8 mx-auto mb-2 rounded-full bg-kpink-50 flex items-center justify-center text-kpink-500">
                        <i data-lucide="sparkles" class="w-4 h-4"></i>
                    </div>
                    <div class="text-xs font-bold text-ktext-primary" data-i18n="v4Title">费用明细公开透明</div>
                    <div class="text-[11px] text-ktext-light mt-0.5" data-i18n="v4Sub">服务费 10%-15% 起</div>
                </div>
            </div>

            <!-- Active Status Line -->
            <div class="bg-white/90 border border-kpink-200 shadow-soft rounded-full px-5 py-2.5 flex items-center gap-3 text-xs text-ktext-secondary">
                <span class="flex h-2.5 w-2.5 relative">
                  <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-emerald-400 opacity-75"></span>
                  <span class="relative inline-flex rounded-full h-2.5 w-2.5 bg-emerald-500"></span>
                </span>
                <span><span data-i18n="statusLabel">当前本土预售通道运行中：</span><strong class="text-ktext-primary font-bold">CHENLE / NCT WISH / aespa / CHANYEOL</strong> <span data-i18n="statusSuffix">等演出接单中</span></span>
            </div>
        </section>

        <!-- SECTION 1: CONCERT SCHEDULE & BOOKING HUB -->
        <section id="concerts" class="space-y-6">
            <div class="flex flex-col md:flex-row md:items-end justify-between gap-4">
                <div>
                    <div class="text-xs font-bold text-kpink-500 uppercase tracking-wider mb-1 flex items-center gap-1">
                        Live Concert Schedule
                    </div>
                    <h2 class="text-2xl sm:text-3xl font-extrabold text-ktext-primary" data-i18n="concertsHeader">热门演出与代抢预订列表</h2>
                    <p class="text-xs sm:text-sm text-ktext-secondary mt-1" data-i18n="concertsSubHeader">
                        同步韩国本土 (KR Page) 与全球 (Global Page) 官方预售节点
                    </p>
                </div>
                
                <div class="flex flex-wrap items-center gap-2 w-full md:w-auto">
                    <div class="relative flex-grow sm:flex-grow-0">
                        <i data-lucide="search" class="w-3.5 h-3.5 text-ktext-light absolute left-3 top-1/2 -translate-y-1/2"></i>
                        <input type="text" id="concert-search" oninput="filterConcerts()" placeholder="搜索艺人/场地..." data-i18n-placeholder="searchPlaceholder" class="w-full sm:w-56 bg-white/90 border border-kpink-200 rounded-full pl-9 pr-4 py-1.5 text-xs text-ktext-primary focus:outline-none focus:ring-2 focus:ring-kpink-300">
                    </div>

                    <div class="flex items-center gap-1.5 bg-white/80 p-1 rounded-full border border-kpink-100 text-xs font-semibold">
                        <button onclick="setCategoryFilter('all')" id="tab-all" class="concert-tab bg-kpink-400 text-white px-3.5 py-1 rounded-full transition-all shadow-sm" data-i18n="tabAll">全部</button>
                        <button onclick="setCategoryFilter('dome')" id="tab-dome" class="concert-tab text-ktext-secondary hover:text-ktext-primary px-3.5 py-1 rounded-full transition-all" data-i18n="tabDome">大型/Dome</button>
                        <button onclick="setCategoryFilter('fanmeeting')" id="tab-fanmeeting" class="concert-tab text-ktext-secondary hover:text-ktext-primary px-3.5 py-1 rounded-full transition-all" data-i18n="tabFM">FM/Party</button>
                    </div>
                </div>
            </div>

            <div id="concert-grid" class="grid grid-cols-1 md:grid-cols-2 gap-6">
                <!-- Injected via JS -->
            </div>
        </section>

        <!-- SECTION 2: SERVICE PLANS -->
        <section id="services" class="space-y-6">
            <div class="text-center space-y-2 max-w-xl mx-auto">
                <span class="text-xs font-bold text-kpink-500 uppercase tracking-wider">Transparent Service Plans</span>
                <h2 class="text-2xl sm:text-3xl font-extrabold text-ktext-primary" data-i18n="plansHeader">选择最适合您的代抢服务方案</h2>
                <p class="text-xs sm:text-sm text-ktext-secondary" data-i18n="plansSubHeader">
                    包含本土实名认证账号使用权、抢订操作及全程票务对接指导
                </p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                <!-- Plan A -->
                <div class="k-glass rounded-4xl p-6 sm:p-8 border-2 border-kpink-300 relative shadow-soft flex flex-col justify-between space-y-6">
                    <div class="absolute -top-3.5 right-6 bg-gradient-to-r from-kpink-400 to-kpink-500 text-white text-xs font-semibold px-4 py-1 rounded-full shadow-sm">
                        限量预约 · 客服确认后付款
                    </div>
                    <div class="space-y-4">
                        <div class="w-10 h-10 rounded-2xl bg-kpink-100 flex items-center justify-center text-kpink-600">
                            <i data-lucide="shield-check" class="w-5 h-5"></i>
                        </div>
                        <div>
                            <h3 class="text-lg font-bold text-ktext-primary" data-i18n="planATitle">抢到后付模式 (Success-First)</h3>
                            <p class="text-xs text-ktext-secondary mt-1" data-i18n="planADesc">资金安全优先，出票成功后再付主体服务费</p>
                        </div>
                        <div class="text-2xl font-black text-kpink-600">
                            定金 ¥100 <span class="text-xs font-normal text-ktext-secondary">+ 服务费 10%–20%（定金抵扣最终费用）</span>
                        </div>
                        <ul class="text-xs text-ktext-secondary space-y-2.5 pt-2">
                            <li class="flex items-center gap-2">
                                <i data-lucide="check" class="w-4 h-4 text-emerald-500 shrink-0"></i>
                                <span>分配专人韩国本土实名认证账号</span>
                            </li>
                            <li class="flex items-center gap-2">
                                <i data-lucide="check" class="w-4 h-4 text-emerald-500 shrink-0"></i>
                                <span>抢票未成功：¥100 定金全额退还</span>
                            </li>
                            <li class="flex items-center gap-2">
                                <i data-lucide="check" class="w-4 h-4 text-emerald-500 shrink-0"></i>
                                <span>成功出票后支付剩余款项，已付 ¥100 定金抵扣最终应付金额</span>
                            </li>
                        </ul>
                    </div>
                    <button onclick="openBookingModal('Success-First')" class="w-full bg-gradient-to-r from-kpink-400 to-kpink-500 hover:from-kpink-500 hover:to-kpink-600 text-white font-bold py-3.5 rounded-full text-xs shadow-soft transition-all">
                        按此方案预订
                    </button>
                </div>

                <!-- Plan B -->
                <div class="k-glass rounded-4xl p-6 sm:p-8 border border-kpink-200 relative shadow-card flex flex-col justify-between space-y-6">
                    <div class="space-y-4">
                        <div class="w-10 h-10 rounded-2xl bg-kpink-100 flex items-center justify-center text-kpink-600">
                            <i data-lucide="award" class="w-5 h-5"></i>
                        </div>
                        <div>
                            <h3 class="text-lg font-bold text-ktext-primary" data-i18n="planBTitle">VIP 前排锁位方案 (VIP Priority)</h3>
                            <p class="text-xs text-ktext-secondary mt-1" data-i18n="planBDesc">适合拟冲刺首尔内场 VIP / 极其紧缺席位</p>
                        </div>
                        <div class="text-2xl font-black text-ktext-primary">
                            定金 ¥100 <span class="text-xs font-normal text-ktext-secondary">+ 服务费 10%–20%（定金抵扣最终费用）</span>
                        </div>
                        <ul class="text-xs text-ktext-secondary space-y-2.5 pt-2">
                            <li class="flex items-center gap-2">
                                <i data-lucide="check" class="w-4 h-4 text-emerald-500 shrink-0"></i>
                                <span>优先调配高响应度本土账号组</span>
                            </li>
                            <li class="flex items-center gap-2">
                                <i data-lucide="check" class="w-4 h-4 text-emerald-500 shrink-0"></i>
                                <span>专属客服一对一全程同步抢票截图</span>
                            </li>
                            <li class="flex items-center gap-2">
                                <i data-lucide="check" class="w-4 h-4 text-emerald-500 shrink-0"></i>
                                <span>未出票：¥100 定金全额退还</span>
                            </li>
                        </ul>
                    </div>
                    <button onclick="openBookingModal('VIP-Priority')" class="w-full bg-white hover:bg-kpink-50 border border-kpink-200 text-ktext-primary font-bold py-3.5 rounded-full text-xs transition-all">
                        按此方案预订
                    </button>
                </div>
            </div>
        </section>

        <!-- SECTION 3: TRANSPARENT CALCULATOR -->
        <section id="calculator" class="k-glass rounded-4xl p-6 sm:p-10 shadow-soft border border-kpink-200">
            <div class="max-w-3xl mx-auto space-y-8">
                <div class="text-center space-y-2">
                    <span class="text-xs font-bold text-kpink-500 uppercase tracking-wider">Cost Transparency</span>
                    <h2 class="text-2xl sm:text-3xl font-extrabold text-ktext-primary" data-i18n="calcHeader">代抢服务费用实时测算</h2>
                    <p class="text-xs sm:text-sm text-ktext-secondary max-w-xl mx-auto" data-i18n="calcSubHeader">
                        拒绝黄牛动辄数倍的恶劣溢价。依据官方票面与合理服务费率计算，拒绝隐藏收费。
                    </p>
                </div>

                <div class="bg-white/90 rounded-3xl p-6 sm:p-8 border border-kpink-100 shadow-sm space-y-6">
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-6">
                        <div class="space-y-2">
                            <label class="block text-xs font-semibold text-ktext-primary" data-i18n="calcSelectShow">选择拟代抢演出项目</label>
                            <select id="calc-show" onchange="updateCalculator()" class="w-full bg-kbg border border-kpink-200 rounded-2xl px-4 py-3 text-xs sm:text-sm text-ktext-primary focus:outline-none focus:ring-2 focus:ring-kpink-300">
                                <option value="77000" selected>CHENLE / GISELLE / CHANYEOL 生日会 - 77,000 韩元</option>
                                <option value="165000">NCT WISH (一般席) - 165,000 韩元</option>
                                <option value="220000">NCT WISH (VIP席) - 220,000 韩元</option>
                                <option value="121000">aespa FAN MEETING - 121,000 韩元</option>
                                <option value="143000">AND2BLE FAN-CON - 143,000 韩元</option>
                                <option value="154000">NMIXX 1ST WORLD TOUR - 154,000 韩元</option>
                            </select>
                        </div>

                        <div class="space-y-2">
                            <label class="block text-xs font-semibold text-ktext-primary" data-i18n="calcSelectTier">服务档位</label>
                            <select id="calc-markup" onchange="updateCalculator()" class="w-full bg-kbg border border-kpink-200 rounded-2xl px-4 py-3 text-xs sm:text-sm text-ktext-primary focus:outline-none focus:ring-2 focus:ring-kpink-300">
                                <option value="0.10">基础档: 10% 服务费 (一般席位/看台)</option>
                                <option value="0.15" selected>标准档: 15% 服务费 (热门推荐)</option>
                                <option value="0.20">冲刺档: 20% 服务费 (稀缺前排 VIP)</option>
                            </select>
                        </div>
                    </div>

                    <div class="pt-4 border-t border-kpink-100">
                        <div class="grid grid-cols-1 md:grid-cols-3 gap-4 text-center">
                            <div class="p-4 rounded-2xl bg-gray-50 border border-gray-100 space-y-1">
                                <div class="text-xs font-bold text-gray-500">官方原票价 (折合RMB)</div>
                                <div class="text-lg font-bold text-gray-700" id="calc-cost-face">¥ 406</div>
                                <div class="text-[10px] text-gray-400">按实时汇率折算</div>
                            </div>

                            <div class="p-4 rounded-2xl bg-kpink-50 border-2 border-kpink-300 space-y-1 relative shadow-sm">
                                <div class="text-xs font-bold text-kpink-600">IYKYK 预估总支出</div>
                                <div class="text-xl font-extrabold text-kpink-600" id="calc-cost-iykyk">¥ 609</div>
                                <div class="text-[10px] text-kpink-500 font-semibold" id="calc-fee-detail">含服务费 ¥203</div>
                            </div>

                            <div class="p-4 rounded-2xl bg-rose-50/60 border border-rose-100 space-y-1">
                                <div class="text-xs font-bold text-rose-500">传统二手黄牛参考价</div>
                                <div class="text-lg font-bold text-rose-600" id="calc-cost-scalper">¥ 812 ~ 1,218</div>
                                <div class="text-[10px] text-rose-400">200%-300% 天价溢价</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- SECTION 4: ORDER LOOKUP PORTAL -->
        <section id="orders" class="space-y-6">
            <div class="text-center space-y-2 max-w-xl mx-auto">
                <span class="text-xs font-bold text-kpink-500 uppercase tracking-wider">Real-time Order Tracking</span>
                <h2 class="text-2xl sm:text-3xl font-extrabold text-ktext-primary" data-i18n="orderHeader">订单进度查询与状态跟踪</h2>
                <p class="text-xs sm:text-sm text-ktext-secondary" data-i18n="orderSubHeader">
                    输入订单号（如 M4-XXXX 或 IY-2026-8812）或下单时填写的手机/社交账号进行实时检索
                </p>
            </div>

            <div class="max-w-xl mx-auto k-glass p-6 sm:p-8 rounded-4xl border border-kpink-200 shadow-soft space-y-6">
                <div class="flex gap-2">
                    <input type="text" id="search-order-input" placeholder="输入订单号或手机/微信账号" data-i18n-placeholder="orderSearchPlaceholder" class="flex-grow bg-white border border-kpink-200 rounded-2xl px-4 py-3 text-xs sm:text-sm text-ktext-primary focus:outline-none focus:ring-2 focus:ring-kpink-300">
                    <button onclick="searchOrder()" class="bg-gradient-to-r from-kpink-400 to-kpink-500 text-white font-bold px-6 py-3 rounded-2xl text-xs hover:from-kpink-500 hover:to-kpink-600 transition-all shrink-0">
                        查询状态
                    </button>
                </div>

                <div id="order-result-box" class="hidden bg-white p-5 rounded-3xl border border-kpink-100 space-y-4 shadow-sm">
                    <div class="flex items-center justify-between border-b border-kpink-100 pb-3">
                        <div>
                            <span class="text-xs font-bold text-ktext-primary" id="res-order-id">#IY-2026-8812</span>
                            <div class="text-[11px] text-ktext-secondary" id="res-show-title">2026 CHENLE B-day PARTY [Lele’s Show 2]</div>
                        </div>
                        <span class="text-xs font-semibold px-3 py-1 rounded-full bg-kpink-100 text-kpink-600" id="res-status-badge">
                            YES24 本土实名账号锁定中
                        </span>
                    </div>

                    <div class="space-y-3 text-xs">
                        <div class="flex items-start gap-3">
                            <div class="w-5 h-5 rounded-full bg-emerald-500 text-white flex items-center justify-center text-[10px] font-bold shrink-0 mt-0.5">✓</div>
                            <div>
                                <div class="font-bold text-ktext-primary">抢票需求提交与方案锁定</div>
                                <div class="text-[10px] text-ktext-light">客户信息提交成功，第三方退订担保生效</div>
                            </div>
                        </div>
                        <div class="flex items-start gap-3">
                            <div class="w-5 h-5 rounded-full bg-emerald-500 text-white flex items-center justify-center text-[10px] font-bold shrink-0 mt-0.5">✓</div>
                            <div>
                                <div class="font-bold text-ktext-primary">本土实名认证账号完成匹配</div>
                                <div class="text-[10px] text-ktext-light">已分发首尔本土高响应 YES24 账号</div>
                            </div>
                        </div>
                        <div class="flex items-start gap-3">
                            <div class="w-5 h-5 rounded-full bg-kpink-400 text-white flex items-center justify-center text-[10px] font-bold shrink-0 mt-0.5 animate-pulse">3</div>
                            <div>
                                <div class="font-bold text-kpink-600">等待韩国本土预售窗口开启</div>
                                <div class="text-[10px] text-ktext-secondary">抢票人员已准备完毕，预计开售即刻进入抢订</div>
                            </div>
                        </div>
                        <div class="flex items-start gap-3 opacity-40">
                            <div class="w-5 h-5 rounded-full bg-gray-200 text-gray-500 flex items-center justify-center text-[10px] font-bold shrink-0 mt-0.5">4</div>
                            <div>
                                <div class="font-bold text-ktext-primary">出票凭证确认与尾款结算</div>
                                <div class="text-[10px] text-ktext-light">发送官方订票截图与实体/电子票查验</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- SECTION 5: TRUST & GUARANTEES -->
        <section id="trust" class="space-y-8">
            <div class="text-center space-y-2">
                <span class="text-xs font-bold text-kpink-500 uppercase tracking-wider">Safety & Service Protocol</span>
                <h2 class="text-2xl sm:text-3xl font-extrabold text-ktext-primary" data-i18n="trustHeader">服务保障与隐私承诺</h2>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                <div class="k-glass p-6 rounded-3xl space-y-3 border border-kpink-200 shadow-card">
                    <div class="w-10 h-10 rounded-2xl bg-kpink-100 flex items-center justify-center text-kpink-600">
                        <i data-lucide="lock" class="w-5 h-5"></i>
                    </div>
                    <h3 class="font-bold text-sm text-ktext-primary" data-i18n="t1Title">严格个人信息保护</h3>
                    <p class="text-xs text-ktext-secondary leading-relaxed" data-i18n="t1Desc">
                        客户所有身份证照及观演人信息仅用于本次门票实名绑定与官方查验，抢票结束后即刻清空，绝不留存。
                    </p>
                </div>

                <div class="k-glass p-6 rounded-3xl space-y-3 border border-kpink-200 shadow-card">
                    <div class="w-10 h-10 rounded-2xl bg-kpink-100 flex items-center justify-center text-kpink-600">
                        <i data-lucide="user-check" class="w-5 h-5"></i>
                    </div>
                    <h3 class="font-bold text-sm text-ktext-primary" data-i18n="t2Title">真实本土合规账号</h3>
                    <p class="text-xs text-ktext-secondary leading-relaxed" data-i18n="t2Desc">
                        仅使用在韩留学生持有之本土实名认证账号，避免海外网络封锁，合规抢订，杜绝非法外挂脚本导致的封号风险。
                    </p>
                </div>

                <div class="k-glass p-6 rounded-3xl space-y-3 border border-kpink-200 shadow-card">
                    <div class="w-10 h-10 rounded-2xl bg-kpink-100 flex items-center justify-center text-kpink-600">
                        <i data-lucide="refresh-cw" class="w-5 h-5"></i>
                    </div>
                    <h3 class="font-bold text-sm text-ktext-primary" data-i18n="t3Title">未出票 100% 全额退款</h3>
                    <p class="text-xs text-ktext-secondary leading-relaxed" data-i18n="t3Desc">
                        若因席位极度紧缺导致未能成功出票，所有定金无条件原路退回，并提供二次转让防诈鉴别指导。
                    </p>
                </div>
            </div>
        </section>

    </main>

    <!-- FOOTER -->
    <footer class="mt-20 bg-white/80 border-t border-kpink-200 py-8 text-center text-xs text-ktext-light z-10 relative">
        <div class="max-w-6xl mx-auto px-4 space-y-3">
            <div class="flex items-center justify-center gap-2 font-bold text-ktext-primary text-sm">
                <span class="w-2 h-2 rounded-full bg-kpink-400"></span>
                IYKYK Ticket Platform
            </div>
            <p class="max-w-xl mx-auto leading-relaxed text-[11px] text-ktext-secondary">
                IYKYK 为海外粉丝提供韩国演唱会本土优先预售协助、抢订及全程协助服务。演出日程及票价来源于 2026 官方公布数据。
            </p>
            <p class="text-[10px] text-ktext-light">
                © 2026 IYKYK Team. All rights reserved.
            </p>
        </div>
    </footer>

    <!-- INTERACTIVE BOOKING MODAL -->
    <div id="booking-modal" class="fixed inset-0 bg-black/40 backdrop-blur-sm z-50 flex items-center justify-center p-4 opacity-0 pointer-events-none transition-opacity duration-300">
        <div class="bg-white w-full max-w-lg rounded-4xl p-6 sm:p-8 shadow-2xl space-y-6 transform scale-95 transition-transform duration-300 max-h-[90vh] overflow-y-auto" id="modal-card">
            
            <div class="flex items-center justify-between border-b border-kpink-100 pb-4">
                <div class="flex items-center gap-2">
                    <div class="w-8 h-8 rounded-full bg-gradient-to-tr from-kpink-400 to-kpink-200 text-white font-bold text-xs flex items-center justify-center">
                        IY
                    </div>
                    <span class="font-bold text-base text-ktext-primary" data-i18n="modalTitle">预订代抢服务</span>
                </div>
                <button onclick="closeBookingModal()" class="text-ktext-light hover:text-ktext-primary p-1">
                    <i data-lucide="x" class="w-5 h-5"></i>
                </button>
            </div>

            <!-- Form -->
            <form id="booking-form" onsubmit="submitBooking(event)" class="space-y-4 text-xs">
                <div class="space-y-1.5">
                    <label class="font-semibold text-ktext-primary" data-i18n="f1">1. 选择演出项目</label>
                    <select id="dw-show" onchange="updateModalPrice()" class="w-full bg-kbg border border-kpink-200 rounded-2xl px-4 py-3 text-ktext-primary focus:outline-none focus:ring-2 focus:ring-kpink-300">
                        <option value="2026 CHENLE B-day PARTY [Lele’s Show 2]" data-price="77000">2026 CHENLE B-day PARTY [Lele’s Show 2]</option>
                        <option value="NCT WISH 2nd CONCERT TOUR" data-price="165000">NCT WISH 2nd CONCERT TOUR (高尺巨蛋)</option>
                        <option value="2026 aespa FAN MEETING" data-price="121000">2026 aespa FAN MEETING (高丽大华正)</option>
                        <option value="2026 GISELLE B-day PARTY" data-price="77000">2026 GISELLE B-day PARTY (明和Live Hall)</option>
                        <option value="2026 AND2BLE FAN-CON" data-price="143000">2026 AND2BLE FAN-CON (Tiger Dome)</option>
                        <option value="2026 SUNWOO 粉丝见面会" data-price="99000">2026 SUNWOO 粉丝见面会《UNCHAINED》</option>
                        <option value="2026 CLOSE YOUR EYES FANCON" data-price="121000">2026 CLOSE YOUR EYES FANCON</option>
                        <option value="NMIXX 1ST WORLD TOUR INCHEON" data-price="154000">NMIXX 1ST WORLD TOUR FINALE</option>
                        <option value="2026 CHANYEOL B-day PARTY" data-price="77000">2026 CHANYEOL B-day PARTY</option>
                    </select>
                </div>

                <div class="grid grid-cols-2 gap-3">
                    <div class="space-y-1.5">
                        <label class="font-semibold text-ktext-primary" data-i18n="f2">2. 席位偏好</label>
                        <select id="dw-tier" class="w-full bg-kbg border border-kpink-200 rounded-2xl px-3 py-3 text-ktext-primary focus:outline-none focus:ring-2 focus:ring-kpink-300">
                            <option value="VIP 席位 / 内场前排">VIP 席位 / 内场前排</option>
                            <option value="指定席 / 一般看台">指定席 / 一般看台</option>
                            <option value="任意可接受席位">任意可接受席位</option>
                        </select>
                    </div>
                    <div class="space-y-1.5">
                        <label class="font-semibold text-ktext-primary" data-i18n="f3">3. 张数</label>
                        <select id="dw-qty" onchange="updateModalPrice()" class="w-full bg-kbg border border-kpink-200 rounded-2xl px-3 py-3 text-ktext-primary focus:outline-none focus:ring-2 focus:ring-kpink-300">
                            <option value="1">1 张</option>
                            <option value="2">2 张</option>
                        </select>
                    </div>
                </div>

                <div class="space-y-1.5">
                    <label class="font-semibold text-ktext-primary" data-i18n="f4">4. 付费服务方案</label>
                    <select id="dw-plan" onchange="updateModalPrice()" class="w-full bg-kbg border border-kpink-200 rounded-2xl px-4 py-3 text-ktext-primary focus:outline-none focus:ring-2 focus:ring-kpink-300">
                        <option value="Success-First">成功后付款（需客服确认接单）</option>
                        <option value="VIP-Priority">优先服务咨询（需客服确认接单）</option>
                    </select>
                </div>

                <div class="space-y-1.5">
                    <label class="font-semibold text-ktext-primary" data-i18n="f5">5. 昵称（请勿填写证件姓名）</label>
                    <input type="text" id="dw-name" placeholder="如：K-pop fan" data-i18n-placeholder="nickPlaceholder" class="w-full bg-kbg border border-kpink-200 rounded-2xl px-4 py-3 text-ktext-primary placeholder:text-ktext-light focus:outline-none focus:ring-2 focus:ring-kpink-300">
                </div>

                <div class="space-y-1.5">
                    <label class="font-semibold text-ktext-primary" data-i18n="f6">6. 联系方式（可选；请勿填写证件或支付信息）</label>
                    <input type="text" id="dw-contact" placeholder="可留微信或邮箱；请勿提供敏感信息" data-i18n-placeholder="contactPlaceholder" class="w-full bg-kbg border border-kpink-200 rounded-2xl px-4 py-3 text-ktext-primary placeholder:text-ktext-light focus:outline-none focus:ring-2 focus:ring-kpink-300">
                </div>

                <!-- Price Summary Box -->
                <div class="p-4 rounded-2xl bg-kpink-50/80 border border-kpink-200 space-y-1.5">
                    <div class="flex justify-between items-center text-xs">
                        <span class="text-ktext-secondary">票面估算：</span>
                        <span class="font-bold text-ktext-primary" id="dw-face-val">¥ 406</span>
                    </div>
                    <div class="flex justify-between items-center text-xs">
                        <span class="text-ktext-secondary">服务费及费用明细：</span>
                        <span class="font-bold text-kpink-600 text-sm" id="dw-deposit-val">服务费按 10%–20% 计算</span>
                    </div>
                    <div class="text-[10px] text-ktext-light pt-1 border-t border-kpink-200/60">
                        * 定金 ¥100 可抵扣最终费用，并非额外收费；抢票失败全额退还定金。少量接单，实际票价、库存、服务费及付款时机以客服书面确认为准。请勿在客服确认前付款。
                    </div>
                </div>

                <p class="text-xs text-amber-800 bg-amber-50 border border-amber-200 p-3 rounded-xl">⚠️ 限量人工接单：提交仅代表预约申请，不代表已接单、已付款或已购票。受邀朋友请使用 <strong>?test=1</strong> 测试链接，不要付款。请核实实名制及官方售票平台规则。</p>
                <button type="submit" class="w-full bg-gradient-to-r from-kpink-400 to-kpink-500 hover:from-kpink-500 hover:to-kpink-600 text-white font-bold py-3.5 rounded-full shadow-soft hover:shadow-soft-lg transition-all text-sm flex items-center justify-center gap-2">
                    <span data-i18n="btnSubmitBooking">提交预约申请 · 联系客服确认</span>
                    <i data-lucide="arrow-right" class="w-4 h-4"></i>
                </button>
            </form>
        </div>
    </div>

    <!-- POST-BOOKING CONTACT & PAYMENT INFORMATION -->
    <div id="after-booking-modal" role="dialog" aria-modal="true" aria-labelledby="after-booking-title" class="fixed inset-0 bg-black/50 backdrop-blur-sm z-[60] hidden items-center justify-center p-4">
      <div class="bg-white w-full max-w-xl rounded-3xl p-5 sm:p-7 shadow-2xl max-h-[90vh] overflow-y-auto space-y-4">
        <div class="flex justify-between items-center">
            <h2 id="after-booking-title" class="text-xl font-bold text-ktext-primary" data-i18n="afterTitle">💗 预约申请已提交（待人工确认）</h2>
            <button onclick="closeAfterBooking()" aria-label="关闭" class="text-2xl text-gray-500 hover:text-gray-800">×</button>
        </div>
        
        <p class="text-sm text-ktext-secondary"><span data-i18n="afterRef">预约编号：</span><strong id="after-booking-id" class="text-kpink-600 font-bold"></strong> <button onclick="copyBookingId()" class="underline text-kpink-600 ml-1 font-semibold" data-i18n="copyBtn">复制</button></p>
        
        <div class="rounded-2xl bg-kpink-50 border border-kpink-200 p-4 text-sm leading-6">
            <strong data-i18n="step1Header">第一步：添加微信客服 Chloe_ii0514</strong>
            <p data-i18n="step1Text">请主动添加客服并发送预约编号、演唱会和场次，确认是否还有少量服务名额、票价、¥100 可抵扣定金、10%–20% 服务费、实名入场规则及退款条件。</p>
            <div class="flex gap-2 items-center mt-3">
                <code class="font-bold bg-white px-3 py-1 rounded-lg border border-kpink-200 text-kpink-700">Chloe_ii0514</code>
                <button onclick="navigator.clipboard?.writeText('Chloe_ii0514').then(()=>showToast('微信号已复制'))" class="px-3.5 py-1 bg-white hover:bg-kpink-100 text-xs font-semibold rounded-full border border-kpink-300 transition-colors" data-i18n="copyWechat">复制微信号</button>
            </div>
        </div>

        <div class="rounded-2xl border border-amber-200 bg-amber-50 p-3.5 text-xs leading-5 text-amber-900">
            <strong>付款前请注意：</strong>当前仅接受少量购票协助申请。预约并不保证抢票成功。请先通过微信客服确认接单、最终费用、付款条件及退款规则，<strong>未经客服确认请勿转账</strong>。请核实收款方名称与客服提供的信息一致。本站不会自动验证付款，付款后需由客服人工核实。
        </div>

        <div class="rounded-2xl border border-kpink-200 p-3.5 text-xs bg-kpink-50">
            <strong>📋 M4 测试说明：</strong>如果你是受邀体验流程的朋友，请使用网址参数 <code>?test=1</code> 进入测试模式。测试预约不代表真实购票需求，请勿付款。<span id="m4-storage-note"></span>
        </div>

        <button onclick="recordWechatClick()" class="w-full rounded-full border border-kpink-300 bg-white hover:bg-kpink-50 py-3 font-semibold text-kpink-600 transition-all text-xs sm:text-sm shadow-sm" data-i18n="intentBtn">我已复制微信号 · 记录客服意向</button>

        <h3 class="font-bold text-ktext-primary text-sm pt-2" data-i18n="step2Header">第二步：客服确认后选择支付方式</h3>
        
        <label class="flex items-start gap-2.5 text-xs text-ktext-secondary cursor-pointer">
            <input type="checkbox" id="payment-unlock" onchange="togglePayment()" class="mt-0.5 rounded text-kpink-500 focus:ring-kpink-400">
            <span data-i18n="checkLabel">我确认已与客服沟通，核实了接单能力、实名入场要求、最终报价及退款条款。</span>
        </label>

        <!-- Payment QRs -->
        <div id="payment-options" class="grid grid-cols-1 sm:grid-cols-2 gap-4 hidden pt-2">
          <div class="border border-blue-200 bg-blue-50/30 rounded-2xl p-4 text-center">
            <h4 class="font-bold text-blue-600 mb-2 text-xs">支付宝 Alipay</h4>
            <div class="bg-white p-2 rounded-xl border border-blue-100 inline-block shadow-sm">
              <svg class="w-44 h-44 mx-auto" viewBox="0 0 200 200" fill="none" xmlns="http://www.w3.org/2000/svg">
                <rect width="200" height="200" rx="12" fill="white"/>
                <path d="M20 20H80V80H20V20ZM35 35V65H65V35H35ZM42.5 42.5H57.5V57.5H42.5V42.5Z" fill="#1677FF"/>
                <path d="M120 20H180V80H120V20ZM135 35V65H165V35H135ZM142.5 42.5H157.5V57.5H142.5V42.5Z" fill="#1677FF"/>
                <path d="M20 120H80V180H20V120ZM35 135V165H65V135H35ZM42.5 142.5H57.5V157.5H42.5V142.5Z" fill="#1677FF"/>
                <rect x="90" y="20" width="15" height="15" fill="#1677FF"/>
                <rect x="90" y="50" width="15" height="40" fill="#1677FF"/>
                <rect x="120" y="90" width="60" height="15" fill="#1677FF"/>
                <rect x="100" y="120" width="30" height="30" fill="#1677FF"/>
                <rect x="140" y="140" width="40" height="40" fill="#1677FF"/>
                <rect x="20" y="90" width="50" height="15" fill="#1677FF"/>
              </svg>
            </div>
            <div class="text-[11px] text-blue-800 font-semibold mt-2">sweetwiee_C0(**琳)</div>
          </div>
          
          <div class="border border-emerald-200 bg-emerald-50/30 rounded-2xl p-4 text-center">
            <h4 class="font-bold text-emerald-600 mb-2 text-xs">微信支付 WeChat Pay</h4>
            <div class="bg-white p-2 rounded-xl border border-emerald-100 inline-block shadow-sm">
              <svg class="w-44 h-44 mx-auto" viewBox="0 0 200 200" fill="none" xmlns="http://www.w3.org/2000/svg">
                <rect width="200" height="200" rx="12" fill="white"/>
                <path d="M20 20H80V80H20V20ZM35 35V65H65V35H35ZM42.5 42.5H57.5V57.5H42.5V42.5Z" fill="#07C160"/>
                <path d="M120 20H180V80H120V20ZM135 35V65H165V35H135ZM142.5 42.5H157.5V57.5H142.5V42.5Z" fill="#07C160"/>
                <path d="M20 120H80V180H20V120ZM35 135V165H65V135H35ZM42.5 142.5H57.5V157.5H42.5V142.5Z" fill="#07C160"/>
                <rect x="90" y="30" width="20" height="30" fill="#07C160"/>
                <rect x="130" y="90" width="30" height="20" fill="#07C160"/>
                <rect x="90" y="130" width="40" height="40" fill="#07C160"/>
                <rect x="150" y="120" width="30" height="50" fill="#07C160"/>
                <rect x="100" y="90" width="20" height="20" fill="#07C160"/>
              </svg>
            </div>
            <div class="text-[11px] text-emerald-800 font-semibold mt-2">Syniiec0oo(**琳)</div>
          </div>
        </div>

        <p class="text-[11px] text-ktext-light">提示：以上为扫码收款示例码，并非自动跳转的支付链接；请在付款前核实收款账户。无需向网站提交付款密码或证件照片。</p>
        <button onclick="closeAfterBooking()" class="w-full bg-kpink-500 hover:bg-kpink-600 text-white rounded-full py-3 font-bold transition-colors text-xs sm:text-sm" data-i18n="gotIt">我知道了</button>
      </div>
    </div>

    <!-- TOAST NOTIFICATION -->
    <div id="toast" class="fixed bottom-6 right-6 bg-white/95 border border-kpink-300 px-5 py-3 rounded-2xl shadow-soft text-xs font-semibold text-ktext-primary flex items-center gap-3 opacity-0 pointer-events-none transition-all duration-300 z-50">
        <span class="w-2 h-2 rounded-full bg-kpink-500 animate-ping"></span>
        <span id="toast-message">提示信息</span>
    </div>

    <!-- JAVASCRIPT LOGIC -->
    <script>
        const concertData = [
            {
                id: 1,
                category: "fanmeeting",
                title: "2026 CHENLE B-day PARTY [Lele’s Show 2]",
                venue: "YES24 LIVE HALL (首尔)",
                priceKRW: "全席统一 77,000 韩元",
                priceRMB: "~ ¥406 RMB",
                krPresale: "2026.10.27 (周二) 8:00 PM (KST)",
                globalPresale: "2026.10.28 (周三) 8:00 PM (KST)",
                status: "YES24独占 · 预订中",
                tag: "NCT DREAM · 生日Party"
            },
            {
                id: 2,
                category: "dome",
                title: "NCT WISH 2nd CONCERT TOUR 'INTO THE WISH' IN SEOUL",
                venue: "GOCHEOK SKY DOME (首尔高尺巨蛋)",
                priceKRW: "VIP席 220,000 / 一般席 165,000 韩元",
                priceRMB: "~ ¥1,160 / ¥870 RMB",
                krPresale: "2026.11.02 (周一) 8:00 PM (KST)",
                globalPresale: "2026.11.03 (周二) 8:00 PM (KST)",
                status: "火热预订中",
                tag: "高尺巨蛋 · 顶级热度"
            },
            {
                id: 3,
                category: "fanmeeting",
                title: "2026 aespa FAN MEETING “MY 보고싶다 ae가”",
                venue: "高丽大学华正体育馆 (Tiger Dome)",
                priceKRW: "指定席 121,000 韩元",
                priceRMB: "~ ¥638 RMB",
                krPresale: "2026.10.27 (周二) 8:00 PM (KST)",
                globalPresale: "2026.10.28 (周三) 8:00 PM (KST)",
                status: "热抢中",
                tag: "粉丝见面会 · 席位紧缺"
            },
            {
                id: 4,
                category: "fanmeeting",
                title: "2026 GISELLE B-day PARTY [In MY Blood]",
                venue: "明和 Live Hall (MYUNGHWA LIVE HALL)",
                priceKRW: "全席统一 77,000 韩元",
                priceRMB: "~ ¥406 RMB",
                krPresale: "2026.10.21 (周三) 8:00 PM (KST)",
                globalPresale: "无 Global 通道 (仅本土独占)",
                status: "本土独占",
                tag: "生日Party · LiveHouse"
            },
            {
                id: 5,
                category: "fanmeeting",
                title: "2026 AND2BLE FAN-CON <W!nter inside> In Seoul",
                venue: "Hwajeong Tiger Dome (华正体育馆)",
                priceKRW: "全席统一 143,000 韩元",
                priceRMB: "~ ¥755 RMB",
                krPresale: "2026.10.21 (周三) 8:00 PM (KST)",
                globalPresale: "2026.10.22 (周四) 8:00 PM (KST)",
                status: "接受预订",
                tag: "FAN-CON · 热门抢购"
            },
            {
                id: 6,
                category: "fanmeeting",
                title: "2026 SUNWOO 粉丝见面会《UNCHAINED》",
                venue: "MYUNGHWA LIVE HALL (明和 Live Hall)",
                priceKRW: "全场统一 99,000 韩元",
                priceRMB: "~ ¥522 RMB",
                krPresale: "2026.10.21 (周三) 8:00 PM (KST)",
                globalPresale: "同步公售通道",
                status: "少量名额",
                tag: "个人FM · 近距离交互"
            },
            {
                id: 7,
                category: "fanmeeting",
                title: "2026 CLOSE YOUR EYES FANCON",
                venue: "Coex Artium WOORI BANK Hall",
                priceKRW: "VIP 121,000 / R席 99,000 韩元",
                priceRMB: "~ ¥638 / ¥522 RMB",
                krPresale: "2026.10.20 (周二) 7:00 PM (KST)",
                globalPresale: "无 Global 通道",
                status: "NOL World 平台",
                tag: "Weverse会员优先"
            },
            {
                id: 8,
                category: "dome",
                title: "NMIXX 1ST WORLD TOUR FINALE IN INCHEON",
                venue: "Inspire Arena (仁川 Inspire 竞技场)",
                priceKRW: "指定座 154,000 韩元",
                priceRMB: "~ ¥812 RMB",
                krPresale: "2026.10.26 (周一) 8:00 PM (KST)",
                globalPresale: "无提前预售",
                status: "世巡终点站",
                tag: "Inspire Arena · 大场馆"
            },
            {
                id: 9,
                category: "fanmeeting",
                title: "2026 CHANYEOL B-day PARTY [B-side]",
                venue: "YES24 LIVE HALL (首尔)",
                priceKRW: "全席统一 77,000 韩元",
                priceRMB: "~ ¥406 RMB",
                krPresale: "2026.10.26 (周一) 8:00 PM (KST)",
                globalPresale: "YES24 Global 通道",
                status: "YES24独占",
                tag: "生日Party · 限量席位"
            }
        ];

        let currentCategory = 'all';
        const M4_ENDPOINT = '';
        const M4_TEST_MODE = new URLSearchParams(location.search).get('test') === '1';

        async function sendM4Event(payload) {
            if (!M4_ENDPOINT) return false;
            try {
                await fetch(M4_ENDPOINT, {
                    method: 'POST',
                    mode: 'no-cors',
                    headers: {'Content-Type': 'text/plain;charset=utf-8'},
                    body: JSON.stringify(payload),
                    keepalive: true
                });
                return true;
            } catch (err) {
                console.warn('Analytics request failed', err);
                return false;
            }
        }

        let userOrders = JSON.parse(localStorage.getItem('iykyk_m4_orders') || '[]');
        const m4Group = sessionStorage.getItem('iykyk_m4_group') || ['A','B','C'][Math.floor(Math.random()*3)];
        sessionStorage.setItem('iykyk_m4_group', m4Group);
        const m4Rate = {A:0.10, B:0.15, C:0.20}[m4Group];
        const m4Visitor = sessionStorage.getItem('iykyk_m4_visitor') || (crypto.randomUUID ? crypto.randomUUID() : String(Date.now()) + Math.random());
        sessionStorage.setItem('iykyk_m4_visitor', m4Visitor);

        function logM4(event, extra={}) {
            const rows = JSON.parse(localStorage.getItem('iykyk_m4_events') || '[]');
            rows.push({time: new Date().toISOString(), visitor: m4Visitor, group: m4Group, rate: m4Rate, event, ...extra});
            localStorage.setItem('iykyk_m4_events', JSON.stringify(rows));
            sendM4Event(rows[rows.length-1]);
        }

        if(!sessionStorage.getItem('iykyk_m4_viewed')) {
            logM4('page_view');
            sessionStorage.setItem('iykyk_m4_viewed', '1');
        }

        function renderConcerts(data) {
            const container = document.getElementById('concert-grid');
            container.innerHTML = '';

            if(data.length === 0) {
                container.innerHTML = `
                    <div class="col-span-full text-center py-12 text-ktext-light text-xs font-medium">
                        未搜寻到匹配的演出，可联系客服添加代抢需求。
                    </div>
                `;
                return;
            }

            data.forEach(item => {
                const card = document.createElement('div');
                card.className = "k-glass rounded-3xl p-6 shadow-card hover:shadow-soft transition-all duration-300 border border-kpink-200/80 flex flex-col justify-between space-y-4 group";
                card.innerHTML = `
                    <div class="space-y-3">
                        <div class="flex items-center justify-between gap-2">
                            <span class="text-[10px] font-bold px-3 py-1 rounded-full bg-kpink-100 text-kpink-600 border border-kpink-200">
                                ${item.tag}
                            </span>
                            <span class="text-[11px] font-semibold text-emerald-600 bg-emerald-50 px-2.5 py-0.5 rounded-full flex items-center gap-1">
                                <span class="w-1.5 h-1.5 rounded-full bg-emerald-500"></span> ${item.status}
                            </span>
                        </div>

                        <h3 class="font-extrabold text-base text-ktext-primary group-hover:text-kpink-600 transition-colors leading-snug">
                            ${item.title}
                        </h3>

                        <div class="text-xs text-ktext-secondary space-y-1.5 pt-1">
                            <div class="flex items-center gap-2">
                                <i data-lucide="map-pin" class="w-3.5 h-3.5 text-kpink-400 shrink-0"></i>
                                <span>${item.venue}</span>
                            </div>
                            <div class="flex items-center gap-2">
                                <i data-lucide="ticket" class="w-3.5 h-3.5 text-kpink-400 shrink-0"></i>
                                <span class="font-semibold text-ktext-primary">${item.priceKRW}</span>
                                <span class="text-ktext-light">(${item.priceRMB})</span>
                            </div>
                        </div>

                        <div class="bg-white/90 rounded-2xl p-3 border border-kpink-100 text-[11px] space-y-1.5 mt-3">
                            <div class="flex items-center justify-between font-semibold">
                                <span class="text-kpink-600 flex items-center gap-1">
                                    <i data-lucide="zap" class="w-3 h-3"></i> 韩国本土预售:
                                </span>
                                <span class="text-ktext-primary font-bold">${item.krPresale}</span>
                            </div>
                            <div class="flex items-center justify-between text-ktext-light">
                                <span>全球 Global 预售:</span>
                                <span>${item.globalPresale}</span>
                            </div>
                        </div>
                    </div>

                    <button onclick="openBookingForShow('${item.title}')" class="w-full mt-2 bg-gradient-to-r from-kpink-400 to-kpink-500 hover:from-kpink-500 hover:to-kpink-600 text-white font-bold py-2.5 rounded-full text-xs shadow-soft transition-all flex items-center justify-center gap-1.5">
                        <span>预订代抢通道</span>
                        <i data-lucide="chevron-right" class="w-3.5 h-3.5"></i>
                    </button>
                `;
                container.appendChild(card);
            });

            if (window.lucide) lucide.createIcons();
        }

        function filterConcerts() {
            const query = document.getElementById('concert-search').value.toLowerCase().trim();
            let filtered = concertData;
            
            if(currentCategory !== 'all') {
                filtered = filtered.filter(item => item.category === currentCategory);
            }

            if(query) {
                filtered = filtered.filter(item => 
                    item.title.toLowerCase().includes(query) || 
                    item.venue.toLowerCase().includes(query)
                );
            }

            renderConcerts(filtered);
        }

        function setCategoryFilter(category) {
            currentCategory = category;
            document.querySelectorAll('.concert-tab').forEach(btn => {
                btn.className = "concert-tab text-ktext-secondary hover:text-ktext-primary px-3.5 py-1 rounded-full transition-all";
            });

            const activeBtn = document.getElementById(`tab-${category}`);
            if(activeBtn) {
                activeBtn.className = "concert-tab bg-kpink-400 text-white px-3.5 py-1 rounded-full transition-all shadow-sm";
            }

            filterConcerts();
        }

        function updateCalculator() {
            const showSelect = document.getElementById('calc-show');
            const krwPrice = parseFloat(showSelect.value);
            const markupRate = parseFloat(document.getElementById('calc-markup').value);

            const rmbTicket = Math.round(krwPrice * 0.00527);
            const serviceFeeRmb = Math.round(rmbTicket * markupRate);
            const totalIykyk = rmbTicket + serviceFeeRmb;

            document.getElementById('calc-cost-face').innerText = `¥ ${rmbTicket}`;
            document.getElementById('calc-cost-iykyk').innerText = `¥ ${totalIykyk}`;
            document.getElementById('calc-fee-detail').innerText = `含服务费 ¥${serviceFeeRmb}`;
            document.getElementById('calc-cost-scalper').innerText = `¥ ${Math.round(rmbTicket*2)} ~ ${Math.round(rmbTicket*3)}`;
        }

        function openBookingModal(planType) {
            if(planType) {
                document.getElementById('dw-plan').value = planType;
            }
            updateModalPrice();
            logM4('quote_view',{show:document.getElementById('dw-show').value});
            const modal = document.getElementById('booking-modal');
            const card = document.getElementById('modal-card');
            modal.classList.remove('opacity-0', 'pointer-events-none');
            card.classList.remove('scale-95');
            card.classList.add('scale-100');
        }

        function openBookingForShow(title) {
            const selectEl = document.getElementById('dw-show');
            for(let i=0; i<selectEl.options.length; i++) {
                if(selectEl.options[i].value.includes(title.substring(0, 8))) {
                    selectEl.selectedIndex = i;
                    break;
                }
            }
            openBookingModal();
        }

        function closeBookingModal() {
            const modal = document.getElementById('booking-modal');
            const card = document.getElementById('modal-card');
            card.classList.remove('scale-100');
            card.classList.add('scale-95');
            modal.classList.add('opacity-0', 'pointer-events-none');
        }

        function updateModalPrice() {
            const showSelect = document.getElementById('dw-show');
            const selectedOpt = showSelect.options[showSelect.selectedIndex];
            const krw = parseFloat(selectedOpt.getAttribute('data-price') || "77000");
            const rmb = Math.round(krw * 0.00527);

            const qty = Number(document.getElementById('dw-qty').value || 1);
            const faceTotal = rmb * qty;
            const fee = Math.round(faceTotal * m4Rate);
            const total = faceTotal + fee;
            const deposit = 100;
            const balance = Math.max(0, total - deposit);
            document.getElementById('dw-face-val').innerText = `¥ ${faceTotal}（${qty} 张）`;
            document.getElementById('dw-deposit-val').innerText = `服务费 ¥${fee} (${Math.round(m4Rate*100)}%) · 总计 ¥${total} · 定金 ¥${deposit}（抵扣总价）· 余款 ¥${balance}`;
        }

        function submitBooking(e) {
            e.preventDefault();
            const showName = document.getElementById('dw-show').value;
            const qty = document.getElementById('dw-qty').value;
            const newOrderId = 'M4-' + Date.now().toString(36).toUpperCase() + '-' + Math.random().toString(36).slice(2,6).toUpperCase();
            
            userOrders.push({id: newOrderId, show: showName, status: '预约申请已保存 · 待联系客服确认（非已付款订单）'});
            localStorage.setItem('iykyk_m4_orders', JSON.stringify(userOrders));
            
            const tier = document.getElementById('dw-tier').value;
            logM4('booking_request', {show: showName, qty, tier, request_id: newOrderId, test_mode: M4_TEST_MODE});
            
            closeBookingModal();
            document.getElementById('search-order-input').value = newOrderId;
            searchOrder();
            scrollToSection('orders');
            
            document.getElementById('after-booking-id').textContent = newOrderId;
            document.getElementById('payment-unlock').checked = false;
            togglePayment();
            document.getElementById('m4-storage-note').textContent = M4_ENDPOINT ? ' 已尝试同步匿名事件至团队表格（请核对后台）。' : ' 当前仅保存在你的浏览器中；团队无法自动看到预约。';
            
            const afterModal = document.getElementById('after-booking-modal');
            afterModal.classList.remove('hidden');
            afterModal.classList.add('flex');
            showToast('预约申请已保存，请添加客服确认');
        }

        function togglePayment() {
            const checkbox = document.getElementById('payment-unlock');
            if(M4_TEST_MODE) { 
                checkbox.checked = false; 
                showToast('测试模式禁止展示付款码'); 
            }
            document.getElementById('payment-options').classList.toggle('hidden', !checkbox.checked || M4_TEST_MODE);
            if(checkbox.checked && !M4_TEST_MODE) logM4('payment_information_unlocked');
        }

        function recordWechatClick() { 
            logM4('wechat_intent_click', {test_mode: M4_TEST_MODE}); 
            showToast('已记录客服意向；请自行在微信添加客服 Chloe_ii0514'); 
        }

        function closeAfterBooking() {
            const el = document.getElementById('after-booking-modal');
            el.classList.add('hidden');
            el.classList.remove('flex');
        }

        function copyBookingId() {
            const id = document.getElementById('after-booking-id').textContent;
            navigator.clipboard?.writeText(id).then(() => showToast('预约编号已复制'));
        }

        function searchOrder() {
            const query = document.getElementById('search-order-input').value.trim();
            const box = document.getElementById('order-result-box');
            
            if (!query) {
                showToast('请输入订单编号');
                return;
            }

            const found = userOrders.find(o => o.id === query || query.toUpperCase() === 'IY-2026-8812');
            
            if(!found && query.toUpperCase() !== 'IY-2026-8812') {
                box.classList.add('hidden');
                showToast('未找到本浏览器保存的预约编号');
                return;
            }

            if (found) {
                document.getElementById('res-order-id').innerText = '#' + found.id;
                document.getElementById('res-show-title').innerText = found.show;
                document.getElementById('res-status-badge').innerText = found.status;
            } else {
                document.getElementById('res-order-id').innerText = '#IY-2026-8812';
                document.getElementById('res-show-title').innerText = '2026 CHENLE B-day PARTY [Lele’s Show 2]';
                document.getElementById('res-status-badge').innerText = 'YES24 本土实名账号锁定中';
            }
            box.classList.remove('hidden');
        }

        function scrollToSection(id) {
            const el = document.getElementById(id);
            if(el) {
                el.scrollIntoView({ behavior: 'smooth', block: 'start' });
            }
        }

        function showToast(msg) {
            const toast = document.getElementById('toast');
            document.getElementById('toast-message').innerText = msg;
            toast.classList.remove('opacity-0', 'pointer-events-none');
            setTimeout(() => {
                toast.classList.add('opacity-0', 'pointer-events-none');
            }, 3200);
        }

        // Lightweight Multi-Language Localization Engine
        const IY_LANGS = {
            "navServices": ["服务优势", "Services", "서비스 장점", "特长"],
            "navConcerts": ["演出 Schedule", "Concerts", "공연 일정", "公演日程"],
            "navCalc": ["试算测算", "Calculator", "요금 계산", "料金計算"],
            "navOrders": ["订单查询", "Orders", "주문 조회", "注文照会"],
            "navTrust": ["安全保障", "Trust & Safety", "안전 보장", "安全保障"],
            "btnSearch": ["查询订单", "Search Order", "주문 검색", "注文検索"],
            "btnBook": ["立即预订", "Book Now", "지금 예약", "今すぐ予約"],
            "noticeTitle": ["限量预约服务", "Limited Booking Service", "한정 예약 서비스", "数量限定予約"],
            "noticeBody": ["：目前仅接受少量购票协助申请。提交预约后请添加微信客服 Chloe_ii0514 确认是否接单、最终报价及退款条款；未经确认请勿付款。", " We currently accept limited booking assistance. After submitting, add WeChat Chloe_ii0514 to confirm capacity and final price.", " 현재 소수의 티켓 지원 신청만 받습니다. 신청 후 위챗 Chloe_ii0514로 접수 여부를 확인하세요.", " 现在、少数のチケット購入サポートのみ受け付けています。申請後WeChat Chloe_ii0514にご確認ください。"],
            "heroBadge": ["IYKYK / 韩国本土预售优先抢订服务", "IYKYK / Korea Local Presale Concierge", "IYKYK / 한국 현지 선예매 대행", "IYKYK / 韓国本土優先予約サポート"],
            "heroTitle1": ["直通韩国本土优先预售通道", "Direct Access to Korean Presales", "한국 현지 우선 예매 직통", "韓国本土優先販売ルート直行"],
            "heroTitle2": ["安全·透明·极速抢占优质席位", "Safe · Transparent · Instant VIP Booking", "안전 · 투명 · 초고속 VIP 좌석 선점", "安全・透明・極速VIP席確保"],
            "heroDesc": ["由专业团队提供韩国本土实名认证账号与优先开售抢订支持。绕过 Global 通道漫长等候与天价黄牛，采用“抢到后付服务费 / 未成功定金全退”安全保障机制。", "Powered by verified local Korean accounts. Skip global queues and scalper markups with our success-first security model.", "한국 현지 실명 인증 계정으로 빠른 예매를 지원합니다. 실패 시 100% 환불 보장.", "韓国本土実名認証アカウントで最速確保。失敗時全額返金保障。"],
            "v1Title": ["成功后再付尾款", "Pay After Success", "성공 후 결제", "成功後払い"],
            "v1Sub": ["第三方托管低风险", "Low risk handling", "낮은 리스크", "低リスク"],
            "v2Title": ["本土提前优先购票", "Local Priority Access", "현지 우선 예매", "本土優先購入"],
            "v2Sub": ["优先抢占内场与VIP", "VIP floor seat priority", "VIP 내장 석선점", "VIP席優先"],
            "v3Title": ["在韩实名认证账号", "Verified KR Accounts", "한국 실명 계정", "韓国実名認証"],
            "v3Sub": ["避开海外 IP 排队限制", "Bypass overseas IP limits", "해외 IP 제한 우회", "海外IP制限回避"],
            "v4Title": ["费用明细公开透明", "Transparent Pricing", "투명한 수수료", "透明な料金"],
            "v4Sub": ["服务费 10%-15% 起", "From 10%-15% service fee", "수수료 10%부터", "手数料10%〜"],
            "statusLabel": ["当前本土预售通道运行中：", "Local presale channel active: ", "현재 선예매 채널 가동 중: ", "現在本土優先ルート稼働中："],
            "statusSuffix": ["等演出接单中", "shows open for booking", "등 공연 예약 중", "などの公演受付中"],
            "concertsHeader": ["热门演出与代抢预订列表", "Live Concerts & Presale Schedule", "인기 공연 및 예매 목록", "热门公演・予約リスト"],
            "concertsSubHeader": ["同步韩国本土 (KR Page) 与全球 (Global Page) 官方预售节点", "Synchronized with official KR and Global ticketing release times", "한국 현지 및 글로벌 예매 일정 동기화", "韓国本土およびGlobal公式発売時間を同期"],
            "searchPlaceholder": ["搜索艺人/场地...", "Search artist / venue...", "아티스트 / 공연장 검색...", "アーティスト・会場を検索..."],
            "tabAll": ["全部", "All", "전체", "すべて"],
            "tabDome": ["大型/Dome", "Dome / Arena", "돔 / 아레나", "ドーム・アリーナ"],
            "tabFM": ["FM/Party", "Fan Meeting", "팬미팅", "ファンミ"],
            "plansHeader": ["选择最适合您的代抢服务方案", "Select Your Service Plan", "맞춤형 서비스 플랜 선택", "サービスプランを選択"],
            "plansSubHeader": ["包含本土实名认证账号使用权、抢订操作及全程票务对接指导", "Includes local account access, rapid booking execution, and end-to-end guidance", "현지 실명 계정 및 1:1 지원 포함", "本土実名認証アカウント利用・サポート付き"],
            "planATitle": ["抢到后付模式 (Success-First)", "Success-First Plan", "성공 후 결제 플랜", "成功後払いプラン"],
            "planADesc": ["资金安全优先，出票成功后再付主体服务费", "Security first: service fee paid after ticket confirmed", "티켓 확보 후 수수료 결제", "チケット確保後に手数料お支払い"],
            "planBTitle": ["VIP 前排锁位方案 (VIP Priority)", "VIP Priority Plan", "VIP 우선 선점 플랜", "VIP優先確保プラン"],
            "planBDesc": ["适合拟冲刺首尔内场 VIP / 极其紧缺席位", "Dedicated for high-demand Seoul floor VIP seats", "서울 VIP Floor 최우선 지원", "ソウルVIP席専用アタック"],
            "calcHeader": ["代抢服务费用实时测算", "Live Service Fee Calculator", "실시간 서비스 요금 계산", "サービス料金リアルタイム計算"],
            "calcSubHeader": ["拒绝黄牛动辄数倍的恶劣溢价。依据官方票面与合理服务费率计算，拒绝隐藏收费。", "No scalper markups. Clear calculation based on official face value and fixed rates.", "황돈 프리미엄 거부. 공식 티켓가 기준 투명 계산.", "高額転売価格を防止。公式チケット価格に基づく透明計算。"],
            "calcSelectShow": ["选择拟代抢演出项目", "Select Concert", "공연 선택", "公演を選択"],
            "calcSelectTier": ["服务档位", "Service Tier", "서비스 등급", "区分"],
            "orderHeader": ["订单进度查询与状态跟踪", "Order Tracking Portal", "주문 진행 상황 조회", "注文状況照会"],
            "orderSubHeader": ["输入订单号（如 M4-XXXX 或 IY-2026-8812）进行检索", "Enter your reference ID (e.g. M4-XXXX) to track real-time progress", "예약 번호(M4-XXXX)를 입력하세요", "予約番号（M4-XXXX）を入力してください"],
            "orderSearchPlaceholder": ["输入订单号或手机/微信账号", "Enter reference ID or WeChat", "예약 번호 입력", "予約番号を入力"],
            "trustHeader": ["服务保障与隐私承诺", "Safety & Guarantee Protocol", "안전 보장 및 개인정보 약속", "安全保障・プライバシー約束"],
            "t1Title": ["严格个人信息保护", "Strict Data Privacy", "개인정보 엄격 보호", "個人情報厳重保護"],
            "t1Desc": ["客户所有身份证照及观演人信息仅用于本次门票实名绑定与官方查验，抢票结束后即刻清空。", "Personal ID info is used only for official real-name verification and deleted immediately after.", "입장 확인용 정보는 예매 완료 후 즉시 파기됩니다.", "本人確認用データはチケット確保後即座に破棄されます。"],
            "t2Title": ["真实本土合规账号", "Genuine KR Accounts", "합법 현지 계정 사용", "正規本土アカウント"],
            "t2Desc": ["仅使用在韩留学生持有之本土实名认证账号，避免海外网络封锁，杜绝非法外挂脚本导致的封号风险。", "Verified accounts owned by local students in Korea. No risk of bot bans.", "한국 현지 실명 계정 사용으로 블락 위험 제로.", "韓国本土の正規認証済みアカウント使用。"],
            "t3Title": ["未出票 100% 全额退款", "100% Refund Guarantee", "실패 시 100% 환불", "失敗時全額返金"],
            "t3Desc": ["若因席位极度紧缺导致未能成功出票，所有定金无条件原路退回。", "If tickets cannot be secured, 100% of your deposit is refunded immediately.", "티켓 미확보 시 모든 예약금 즉시 원상 복구.", "チケットが確保できなかった場合、預かり金は全額返金。"],
            "modalTitle": ["预订代抢服务", "Book Ticket Assistance", "티켓 예매 지원 신청", "代行予約"],
            "f1": ["1. 选择演出项目", "1. Select Concert", "1. 공연 선택", "1. 公演を選択"],
            "f2": ["2. 席位偏好", "2. Seat Preference", "2. 좌석 선호", "2. 座席希望"],
            "f3": ["3. 张数", "3. Quantity", "3. 수량", "3. 枚数"],
            "f4": ["4. 付费服务方案", "4. Service Plan", "4. 플랜 선택", "4. プラン"],
            "f5": ["5. 昵称（请勿填写证件姓名）", "5. Nickname (No Legal ID)", "5. 닉네임", "5. ニックネーム"],
            "f6": ["6. 联系方式（可选；请勿填写敏能信息）", "6. Contact (Optional)", "6. 연락처 (선택)", "6. 連絡先（任意）"],
            "nickPlaceholder": ["如：K-pop fan", "e.g. K-pop fan", "예: K-pop fan", "例: K-pop fan"],
            "contactPlaceholder": ["可留微信或邮箱；请勿提供敏感信息", "WeChat ID or Email", "위챗 또는 이메일", "WeChatまたはメール"],
            "btnSubmitBooking": ["提交预约申请 · 联系客服确认", "Submit Request & Contact Service", "신청서 제출 및 상담", "予約代行を送信"],
            "afterTitle": ["💗 预约申请已提交（待人工确认）", "💗 Booking Request Submitted", "💗 예약 신청 완료", "💗 予約申請完了"],
            "afterRef": ["预约编号：", "Reference ID: ", "예약 번호: ", "予約番号："],
            "copyBtn": ["复制", "Copy", "복사", "コピー"],
            "step1Header": ["第一步：添加微信客服 Chloe_ii0514", "Step 1: Add WeChat Chloe_ii0514", "1단계: 위챗 Chloe_ii0514 추가", "ステップ1: WeChat Chloe_ii0514 を追加"],
            "step1Text": ["请主动添加客服并发送预约编号、演唱会和场次，确认是否还有少量服务名额、票价、¥100 可抵扣定金、10%–20% 服务费、实名入场规则及退款条件。", "Send your reference ID and concert details to WeChat customer service to confirm availability.", "예약 번호와 공연 정보를 위챗으로 전송하여 접수 여부를 확인하세요.", "予約番号と公演情報をWeChatで送信して確定してください。"],
            "copyWechat": ["复制微信号", "Copy WeChat ID", "위챗 ID 복사", "WeChat IDコピー"],
            "intentBtn": ["我已复制微信号 · 记录客服意向", "I Copied WeChat ID", "위챗 ID 복사 완료", "WeChat ID コピー完了"],
            "step2Header": ["第二步：客服确认后选择支付方式", "Step 2: Pay Only After Confirmation", "2단계: 확인 후 결제", "ステップ2: 確認後にお支払い"],
            "checkLabel": ["我确认已与客服沟通，核实了接单能力、实名入场要求、最终报价及退款条款。", "I confirm I have verified capacity, ID rules, and terms with customer service.", "고객센터와 가격 및 조건 확인을 완료했습니다.", "スタッフと価格および条件を確認済みです。"],
            "gotIt": ["我知道了", "Got It", "확인", "了解しました"]
        };

        const IY_CODES = ['zh', 'en', 'ko', 'ja'];
        let iyLanguage = 'zh';

        function applyLanguage() {
            const idx = IY_CODES.indexOf(iyLanguage);
            document.querySelectorAll('[data-i18n]').forEach(el => {
                const key = el.dataset.i18n;
                if(IY_LANGS[key] && IY_LANGS[key][idx]) {
                    el.innerText = IY_LANGS[key][idx];
                }
            });

            document.querySelectorAll('[data-i18n-placeholder]').forEach(el => {
                const key = el.dataset.i18nPlaceholder;
                if(IY_LANGS[key] && IY_LANGS[key][idx]) {
                    el.placeholder = IY_LANGS[key][idx];
                }
            });

            document.documentElement.lang = iyLanguage === 'zh' ? 'zh-CN' : iyLanguage;
        }

        function setSiteLanguage(code) {
            if(!IY_CODES.includes(code)) return;
            iyLanguage = code;
            localStorage.setItem('iykyk_language', code);
            applyLanguage();
        }

        window.onload = function() {
            if (window.lucide) lucide.createIcons();
            const stored = localStorage.getItem('iykyk_language');
            if (stored && IY_CODES.includes(stored)) {
                iyLanguage = stored;
                document.getElementById('language-picker').value = stored;
            }
            renderConcerts(concertData);
            updateCalculator();
            applyLanguage();
        }
    </script>
</body>
</html>
