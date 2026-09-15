[index.html](https://github.com/user-attachments/files/32224748/index.html)
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>空谷设计 | 酒店·康养·休闲空间设计</title>
    <!-- 微信 / 社交平台链接卡片 -->
    <meta property="og:type" content="website">
    <meta property="og:url" content="https://y123-h-spec.github.io/kongg/">
    <meta property="og:title" content="空谷设计 KONGGU DESIGN | 酒店·康养·休闲空间设计">
    <meta property="og:description" content="居于空谷 · 心在云际 —— 以东方意境，筑当代空间。酒店、康养与休闲空间设计。">
    <meta property="og:image" content="https://y123-h-spec.github.io/kongg/images/og-cover.jpg">
    <meta property="og:site_name" content="空谷设计">
    <meta name="twitter:card" content="summary_large_image">
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600&family=Noto+Sans+SC:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        ink: '#F2EDE3',
                        paper: '#0C0C0C',
                        gold: '#D4AF6A',
                        muted: '#A39D92',
                        card: '#171717'
                    },
                    fontFamily: {
                        sans: ['Noto Sans SC', 'Inter', 'system-ui', 'sans-serif'],
                        en: ['Inter', 'sans-serif']
                    },
                    boxShadow: {
                        'card': '0 4px 24px rgba(0, 0, 0, 0.45)',
                        'card-hover': '0 20px 60px rgba(0, 0, 0, 0.65), 0 0 40px rgba(212, 175, 106, 0.08)',
                        'glow': '0 0 40px rgba(212, 175, 106, 0.25)'
                    },
                    borderRadius: {
                        '2xl': '20px',
                        '3xl': '28px'
                    }
                }
            }
        }
    </script>
    <style type="text/tailwindcss">
        @layer utilities {
            .text-balance { text-wrap: balance; }
            .bg-blur {
                backdrop-filter: saturate(180%) blur(24px);
                -webkit-backdrop-filter: saturate(180%) blur(24px);
            }
            .fade-in {
                opacity: 0;
                transform: translateY(40px);
                transition: opacity 0.9s cubic-bezier(0.22, 1, 0.36, 1), transform 0.9s cubic-bezier(0.22, 1, 0.36, 1);
            }
            .fade-in.visible { opacity: 1; transform: translateY(0); }
            .card-3d { transform-style: preserve-3d; border: 1px solid rgba(255,255,255,0.06); transition: transform 0.6s cubic-bezier(0.22, 1, 0.36, 1), box-shadow 0.6s ease, border-color 0.6s ease; }
            .card-3d:hover { transform: translateY(-8px) rotateX(2deg); box-shadow: 0 24px 70px rgba(0, 0, 0, 0.6), 0 0 50px rgba(212, 175, 106, 0.16); border-color: rgba(212, 175, 106, 0.45); }
            .lightbox {
                opacity: 0;
                visibility: hidden;
                transition: opacity 0.3s ease, visibility 0.3s ease;
            }
            .lightbox.active { opacity: 1; visibility: visible; }
            .watermark {
                position: fixed;
                width: 200%;
                height: 200%;
                top: -50%;
                left: -50%;
                transform: rotate(-30deg);
                pointer-events: none;
                z-index: 9999;
                opacity: 0.03;
                font-size: 26px;
                line-height: 200px;
                color: #F2EDE3;
                white-space: nowrap;
                user-select: none;
            }
            .img-fade {
                opacity: 0;
                transition: opacity 0.8s ease;
            }
            .img-fade.loaded { opacity: 1; }
            .filter-btn.active {
                background-color: #D4AF6A;
                color: #0C0C0C;
                box-shadow: 0 4px 22px rgba(212, 175, 106, 0.35);
            }
            .filter-btn:hover:not(.active) {
                color: #D4AF6A;
                border-color: rgba(212, 175, 106, 0.5);
            }
            .hero-overlay {
                background: linear-gradient(180deg, rgba(0,0,0,0.25) 0%, rgba(0,0,0,0.55) 100%);
            }
            .section-hero {
                background-size: cover;
                background-position: center;
                position: relative;
            }
            .section-hero::before {
                content: '';
                position: absolute;
                inset: 0;
                background: linear-gradient(135deg, rgba(10,10,10,0.92) 0%, rgba(10,10,10,0.85) 100%);
            }
            .section-hero > * {
                position: relative;
                z-index: 1;
            }
        }
            /* ===== 黑金主题 · 交互增强 ===== */
            .progress-bar {
                position: fixed;
                top: 0; left: 0;
                height: 2px; width: 0;
                background: linear-gradient(90deg, #D4AF6A, #F1DCA8);
                box-shadow: 0 0 12px rgba(212, 175, 106, 0.6);
                z-index: 100;
                transition: width 0.15s linear;
            }
            .shine { position: relative; overflow: hidden; }
            .shine::after {
                content: '';
                position: absolute;
                top: 0; left: -130%;
                width: 55%; height: 100%;
                background: linear-gradient(105deg, transparent, rgba(255,255,255,0.10), transparent);
                transform: skewX(-20deg);
                transition: left 0.75s ease;
            }
            .shine:hover::after { left: 170%; }
            .nav-link { position: relative; }
            .nav-link::after {
                content: '';
                position: absolute;
                left: 0; bottom: -4px;
                width: 0; height: 1px;
                background: #D4AF6A;
                transition: width 0.35s ease;
            }
            .nav-link:hover::after { width: 100%; }
    </style>
</head>
<body class="bg-paper text-ink antialiased selection:bg-gold/20 overflow-x-hidden">
    <!-- 防截图水印层 -->
    <div class="watermark">
        空谷设计 KONGGU DESIGN · 仅供客户阅览 · 版权所有
        &nbsp;&nbsp;&nbsp;&nbsp;空谷设计 KONGGU DESIGN · 仅供客户阅览 · 版权所有
        &nbsp;&nbsp;&nbsp;&nbsp;空谷设计 KONGGU DESIGN · 仅供客户阅览 · 版权所有
        &nbsp;&nbsp;&nbsp;&nbsp;空谷设计 KONGGU DESIGN · 仅供客户阅览 · 版权所有
        <br>
        空谷设计 KONGGU DESIGN · 仅供客户阅览 · 版权所有
        &nbsp;&nbsp;&nbsp;&nbsp;空谷设计 KONGGU DESIGN · 仅供客户阅览 · 版权所有
        &nbsp;&nbsp;&nbsp;&nbsp;空谷设计 KONGGU DESIGN · 仅供客户阅览 · 版权所有
        &nbsp;&nbsp;&nbsp;&nbsp;空谷设计 KONGGU DESIGN · 仅供客户阅览 · 版权所有
    </div>

    <!-- 图片灯箱 -->
    <div id="lightbox" class="lightbox fixed inset-0 z-[100] bg-black/90 flex items-center justify-center p-6">
        <button id="closeLightbox" class="absolute top-6 right-6 text-white/70 hover:text-white text-3xl w-12 h-12 flex items-center justify-center rounded-full bg-white/10 hover:bg-white/20 transition-all">
            ×
        </button>
        <img id="lightboxImg" src="" alt="" class="max-w-full max-h-[90vh] object-contain rounded-2xl shadow-2xl">
        <div id="lightboxText" class="absolute bottom-8 left-1/2 -translate-x-1/2 text-white text-center">
            <h3 class="text-xl font-medium mb-1"></h3>
            <p class="text-white/60 text-sm"></p>
        </div>
    </div>

    <!-- 回到顶部按钮 -->
    <button id="backToTop" class="fixed bottom-8 right-8 z-40 w-12 h-12 bg-card rounded-full shadow-card flex items-center justify-center opacity-0 invisible transition-all duration-300 hover:shadow-card-hover hover:-translate-y-1">
        <svg class="w-5 h-5 text-ink/70" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 15l7-7 7 7"></path>
        </svg>
    </button>

    <!-- 导航栏 -->
    <nav id="navbar" class="fixed top-0 left-0 right-0 z-50 transition-all duration-500 py-6">
        <div class="max-w-7xl mx-auto px-6 md:px-10 flex items-center justify-between">
            <a href="#top" class="flex items-center gap-3">
                <img src="images/footer-logo.png" alt="空谷设计" class="h-6 object-contain" onerror="this.style.display='none'">
                <span class="text-lg font-semibold tracking-wide">空谷设计</span>
                <span class="text-xs text-muted font-en tracking-widest uppercase">Konggu Design</span>
            </a>
            <div class="hidden md:flex items-center gap-8 text-sm text-muted">
                <a href="#prologue" class="nav-link hover:text-ink transition-colors">品牌序言</a>
                <a href="#profile" class="nav-link hover:text-ink transition-colors">公司概况</a>
                <a href="#capability" class="nav-link hover:text-ink transition-colors">核心能力</a>
                <a href="#hotel" class="nav-link hover:text-ink transition-colors">酒店案例</a>
                <a href="#wellness" class="nav-link hover:text-ink transition-colors">康养案例</a>
                <a href="#contact" class="nav-link hover:text-ink transition-colors">联系我们</a>
            </div>
        </div>
    </nav>

    <!-- Hero 首屏 -->
    <section id="top" class="min-h-screen flex flex-col justify-center items-center relative px-6 overflow-hidden">
        <div class="absolute inset-0 z-0">
            <img src="images/hero-bg.png" alt="" class="w-full h-full object-cover opacity-30">
            <div class="absolute inset-0 bg-gradient-to-b from-black/70 via-black/45 to-black"></div>
        </div>
        <div class="text-center fade-in relative z-10">
            <p class="text-gold text-sm tracking-[0.3em] uppercase mb-6 font-en">Hotel & Wellness Space</p>
            <h1 class="text-[clamp(2.5rem,8vw,5.5rem)] font-light tracking-wider mb-4">空谷设计</h1>
            <p class="text-muted text-lg md:text-xl font-light mb-12 tracking-wide">居于空谷 · 心在云际</p>
            <p class="text-muted/80 max-w-xl mx-auto text-balance leading-relaxed text-lg">
                以东方意境，筑当代空间<br>
                让每一处抵达，都成为归心之旅
            </p>
        </div>
        <div class="absolute bottom-12 left-1/2 -translate-x-1/2 text-muted text-xs tracking-widest animate-bounce z-10">
            向下滚动探索
        </div>
    </section>

    <!-- 01 品牌序言 -->
    <section id="prologue" class="py-28 md:py-36 px-6 section-hero" style="background-image: url('images/prologue-bg.jpg')">
        <div class="max-w-4xl mx-auto fade-in">
            <div class="flex items-center gap-4 mb-16">
                <span class="text-gold text-xs font-en tracking-widest">01 / PROLOGUE</span>
                <div class="h-px bg-ink/10 flex-1 max-w-[100px]"></div>
            </div>
            <h2 class="text-3xl md:text-5xl font-light mb-10 tracking-wide">品牌序言</h2>
            <p class="text-xl text-muted leading-loose max-w-2xl">
                以东方意境，筑当代空间；让每一处抵达，都成为归心之旅。
            </p>
        </div>
    </section>

    <!-- 02 公司概况 -->
    <section id="profile" class="py-28 md:py-36 px-6 bg-[#101010]">
        <div class="max-w-6xl mx-auto fade-in">
            <div class="flex items-center gap-4 mb-16">
                <span class="text-gold text-xs font-en tracking-widest">02 / PROFILE</span>
                <div class="h-px bg-ink/10 flex-1 max-w-[100px]"></div>
            </div>
            
            <div class="grid md:grid-cols-2 gap-20 items-start mb-24">
                <div>
                    <h2 class="text-3xl md:text-5xl font-light mb-10 tracking-wide">关于我们</h2>
                    <div class="space-y-6 text-muted leading-relaxed text-lg">
                        <p>空谷设计创立于成都，深耕酒店与康养休闲空间设计十余年，是一家集前期策划、空间设计、软装陈设与落地运营支持于一体的专业设计公司。</p>
                        <p>公司以「空谷云际」专注酒店及商业空间，以「空谷设计」深耕足浴健康与休闲空间，双线并进、互为印证。</p>
                        <p>以「商业价值导向」为设计原点，提供从选址分析到运营支持的全链条服务。截至2026年，已累计落地400+酒店、康养与休闲空间项目。</p>
                    </div>
                </div>
                
                <div class="grid grid-cols-3 gap-6">
                    <div class="bg-card rounded-3xl p-8 shadow-card text-center card-3d">
                        <div class="text-5xl font-light text-gold mb-3 counter" data-target="10">0</div>
                        <div class="text-sm text-muted">年行业深耕</div>
                        <div class="text-xs text-gold/60 mt-1 font-en">+</div>
                    </div>
                    <div class="bg-card rounded-3xl p-8 shadow-card text-center card-3d">
                        <div class="text-5xl font-light text-gold mb-3 counter" data-target="200">0</div>
                        <div class="text-sm text-muted">酒店项目落地</div>
                        <div class="text-xs text-gold/60 mt-1 font-en">+</div>
                    </div>
                    <div class="bg-card rounded-3xl p-8 shadow-card text-center card-3d">
                        <div class="text-5xl font-light text-gold mb-3 counter" data-target="200">0</div>
                        <div class="text-sm text-muted">康养休闲项目</div>
                        <div class="text-xs text-gold/60 mt-1 font-en">+</div>
                    </div>
                </div>
            </div>

            <!-- 资质认证 -->
            <div class="bg-card rounded-3xl p-10 shadow-card card-3d">
                <h3 class="text-xl font-medium mb-8">资质认证</h3>
                <div class="grid md:grid-cols-2 gap-10">
                    <div class="space-y-4">
                        <div class="aspect-[3/4] bg-paper rounded-2xl overflow-hidden flex items-center justify-center">
                            <img src="images/cert-license.png" alt="营业执照" class="w-full h-full object-contain p-4">
                        </div>
                        <p class="text-center text-sm text-muted">营业执照</p>
                    </div>
                    <div class="space-y-4">
                        <div class="aspect-[3/2] bg-paper rounded-2xl overflow-hidden flex items-center justify-center">
                            <img src="images/cert-qualification.jpg" alt="工程设计资质证书" class="w-full h-full object-contain p-4">
                        </div>
                        <p class="text-center text-sm text-muted">建筑装饰设计专项乙级资质</p>
                    </div>
                </div>
                <div class="mt-8 pt-8 border-t border-ink/5 grid md:grid-cols-2 gap-6 text-sm text-muted">
                    <div class="space-y-2">
                        <p><span class="text-ink/70 font-medium">企业名称：</span>四川空谷云际建筑设计有限公司</p>
                        <p><span class="text-ink/70 font-medium">详细地址：</span>四川省成都市成华区龙潭工业园航天路5号1栋15楼1502号</p>
                        <p><span class="text-ink/70 font-medium">统一社会信用代码：</span>91510100MACEEB8J48</p>
                    </div>
                    <div class="space-y-2">
                        <p><span class="text-ink/70 font-medium">资质等级：</span>建筑装饰设计专项乙级</p>
                        <p><span class="text-ink/70 font-medium">证书编号：</span>A251040044</p>
                        <p><span class="text-ink/70 font-medium">有效期至：</span>2028年09月06日</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 03 核心能力 -->
    <section id="capability" class="py-28 md:py-36 px-6">
        <div class="max-w-6xl mx-auto fade-in">
            <div class="flex items-center gap-4 mb-16">
                <span class="text-gold text-xs font-en tracking-widest">03 / CAPABILITY</span>
                <div class="h-px bg-ink/10 flex-1 max-w-[100px]"></div>
            </div>
            
            <h2 class="text-3xl md:text-5xl font-light mb-6 tracking-wide">核心能力</h2>
            <p class="text-muted mb-16 max-w-xl text-lg">全链条设计服务，一站式覆盖酒店、康养与休闲空间全生命周期</p>
            
            <div class="grid grid-cols-2 md:grid-cols-5 gap-6">
                <div class="bg-card rounded-2xl p-8 shadow-card card-3d cursor-pointer group shine">
                    <div class="text-gold font-en text-lg mb-4">01</div>
                    <div class="font-medium text-lg group-hover:text-gold transition-colors">选址分析</div>
                </div>
                <div class="bg-card rounded-2xl p-8 shadow-card card-3d cursor-pointer group shine">
                    <div class="text-gold font-en text-lg mb-4">02</div>
                    <div class="font-medium text-lg group-hover:text-gold transition-colors">商业规划</div>
                </div>
                <div class="bg-card rounded-2xl p-8 shadow-card card-3d cursor-pointer group shine">
                    <div class="text-gold font-en text-lg mb-4">03</div>
                    <div class="font-medium text-lg group-hover:text-gold transition-colors">品牌定位</div>
                </div>
                <div class="bg-card rounded-2xl p-8 shadow-card card-3d cursor-pointer group shine">
                    <div class="text-gold font-en text-lg mb-4">04</div>
                    <div class="font-medium text-lg group-hover:text-gold transition-colors">室内设计</div>
                </div>
                <div class="bg-card rounded-2xl p-8 shadow-card card-3d cursor-pointer group shine">
                    <div class="text-gold font-en text-lg mb-4">05</div>
                    <div class="font-medium text-lg group-hover:text-gold transition-colors">软装搭配</div>
                </div>
                <div class="bg-card rounded-2xl p-8 shadow-card card-3d cursor-pointer group shine">
                    <div class="text-gold font-en text-lg mb-4">06</div>
                    <div class="font-medium text-lg group-hover:text-gold transition-colors">VI 导视</div>
                </div>
                <div class="bg-card rounded-2xl p-8 shadow-card card-3d cursor-pointer group shine">
                    <div class="text-gold font-en text-lg mb-4">07</div>
                    <div class="font-medium text-lg group-hover:text-gold transition-colors">成本控制</div>
                </div>
                <div class="bg-card rounded-2xl p-8 shadow-card card-3d cursor-pointer group shine">
                    <div class="text-gold font-en text-lg mb-4">08</div>
                    <div class="font-medium text-lg group-hover:text-gold transition-colors">施工支持</div>
                </div>
                <div class="bg-card rounded-2xl p-8 shadow-card card-3d cursor-pointer group shine">
                    <div class="text-gold font-en text-lg mb-4">09</div>
                    <div class="font-medium text-lg group-hover:text-gold transition-colors">家具软装</div>
                </div>
                <div class="bg-card rounded-2xl p-8 shadow-card card-3d cursor-pointer group shine">
                    <div class="text-gold font-en text-lg mb-4">10</div>
                    <div class="font-medium text-lg group-hover:text-gold transition-colors">运营支持</div>
                </div>
            </div>
        </div>
    </section>

    <!-- 04 酒店代表案例 -->
    <section id="hotel" class="py-28 md:py-36 px-6 section-hero" style="background-image: url('images/hotel-section-bg.jpg')">
        <div class="max-w-6xl mx-auto fade-in">
            <div class="flex items-center gap-4 mb-16">
                <span class="text-gold text-xs font-en tracking-widest">04 / HOTEL PORTFOLIO</span>
                <div class="h-px bg-ink/10 flex-1 max-w-[100px]"></div>
            </div>
            
            <div class="flex flex-col md:flex-row md:items-end justify-between mb-12 gap-6">
                <div>
                    <h2 class="text-3xl md:text-5xl font-light mb-4 tracking-wide">酒店代表案例</h2>
                    <p class="text-muted max-w-xl text-lg">7个代表性酒店与商业空间项目，覆盖会议中心、中高端酒店、度假酒店等多元业态</p>
                </div>
                <div class="flex gap-2 flex-wrap">
                    <button class="filter-btn shine active px-5 py-2 rounded-full text-sm bg-card border border-white/10 shadow-sm transition-all" data-filter="all">全部</button>
                    <button class="filter-btn shine px-5 py-2 rounded-full text-sm bg-card border border-white/10 shadow-sm transition-all" data-filter="conference">会议中心</button>
                    <button class="filter-btn shine px-5 py-2 rounded-full text-sm bg-card border border-white/10 shadow-sm transition-all" data-filter="hotel">精品酒店</button>
                    <button class="filter-btn shine px-5 py-2 rounded-full text-sm bg-card border border-white/10 shadow-sm transition-all" data-filter="resort">度假酒店</button>
                </div>
            </div>
            
            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8" id="hotelGrid">
                <!-- 案例1 绵阳云帆 -->
                <div class="hotel-item bg-card rounded-3xl overflow-hidden shadow-card card-3d cursor-pointer" data-category="conference" data-img="images/hotel-1-yunfan.jpg" data-title="绵阳云帆国际会议中心" data-desc="2021 · 绵阳江油 · 40000㎡">
                    <div class="aspect-[4/3] overflow-hidden relative group bg-[#201D18]">
                        <img src="images/hotel-1-yunfan.jpg" alt="绵阳云帆国际会议中心" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-700">
                        <div class="absolute inset-0 bg-black/0 group-hover:bg-black/20 transition-all duration-500 flex items-center justify-center">
                            <div class="w-12 h-12 rounded-full bg-gold/95 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-all duration-500 translate-y-4 group-hover:translate-y-0">
                                <svg class="w-5 h-5 text-black" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0zM10 7v3m0 0v3m0-3h3m-3 0H7"></path>
                                </svg>
                            </div>
                        </div>
                    </div>
                    <div class="p-8">
                        <h3 class="text-xl font-medium mb-4">绵阳云帆国际会议中心</h3>
                        <div class="grid grid-cols-2 gap-3 text-sm text-muted">
                            <div>时间 · 2021</div>
                            <div>地点 · 绵阳江油</div>
                            <div>面积 · 40000㎡</div>
                            <div>服务 · 空间设计</div>
                        </div>
                    </div>
                </div>
                
                <!-- 案例2 成都科创 -->
                <div class="hotel-item bg-card rounded-3xl overflow-hidden shadow-card card-3d cursor-pointer" data-category="hotel" data-img="images/hotel-2-kechuang.jpg" data-title="成都科创宿泊码头酒店" data-desc="2021 · 四川成都 · 10000㎡">
                    <div class="aspect-[4/3] overflow-hidden relative group bg-[#201D18]">
                        <img src="images/hotel-2-kechuang.jpg" alt="成都科创宿泊码头酒店" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-700">
                        <div class="absolute inset-0 bg-black/0 group-hover:bg-black/20 transition-all duration-500 flex items-center justify-center">
                            <div class="w-12 h-12 rounded-full bg-gold/95 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-all duration-500 translate-y-4 group-hover:translate-y-0">
                                <svg class="w-5 h-5 text-black" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0zM10 7v3m0 0v3m0-3h3m-3 0H7"></path>
                                </svg>
                            </div>
                        </div>
                    </div>
                    <div class="p-8">
                        <h3 class="text-xl font-medium mb-4">成都科创宿泊码头酒店</h3>
                        <div class="grid grid-cols-2 gap-3 text-sm text-muted">
                            <div>时间 · 2021</div>
                            <div>地点 · 四川成都</div>
                            <div>面积 · 10000㎡</div>
                            <div>服务 · 空间设计</div>
                        </div>
                    </div>
                </div>
                
                <!-- 案例3 岳池钻石 -->
                <div class="hotel-item bg-card rounded-3xl overflow-hidden shadow-card card-3d cursor-pointer" data-category="hotel" data-img="images/hotel-3-diamond.jpg" data-title="四川岳池钻石酒店" data-desc="2022 · 四川岳池 · 10000㎡">
                    <div class="aspect-[4/3] overflow-hidden relative group bg-[#201D18]">
                        <img src="images/hotel-3-diamond.jpg" alt="四川岳池钻石酒店" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-700">
                        <div class="absolute inset-0 bg-black/0 group-hover:bg-black/20 transition-all duration-500 flex items-center justify-center">
                            <div class="w-12 h-12 rounded-full bg-gold/95 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-all duration-500 translate-y-4 group-hover:translate-y-0">
                                <svg class="w-5 h-5 text-black" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0zM10 7v3m0 0v3m0-3h3m-3 0H7"></path>
                                </svg>
                            </div>
                        </div>
                    </div>
                    <div class="p-8">
                        <h3 class="text-xl font-medium mb-4">四川岳池钻石酒店</h3>
                        <div class="grid grid-cols-2 gap-3 text-sm text-muted">
                            <div>时间 · 2022</div>
                            <div>地点 · 四川岳池</div>
                            <div>面积 · 10000㎡</div>
                            <div>服务 · 空间设计</div>
                        </div>
                    </div>
                </div>
                
                <!-- 案例4 西安盛铂 -->
                <div class="hotel-item bg-card rounded-3xl overflow-hidden shadow-card card-3d cursor-pointer" data-category="hotel" data-img="images/hotel-4-shengbo.jpg" data-title="西安盛铂清居酒店" data-desc="2023 · 陕西西安 · 7000㎡">
                    <div class="aspect-[4/3] overflow-hidden relative group bg-[#201D18]">
                        <img src="images/hotel-4-shengbo.jpg" alt="西安盛铂清居酒店" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-700">
                        <div class="absolute inset-0 bg-black/0 group-hover:bg-black/20 transition-all duration-500 flex items-center justify-center">
                            <div class="w-12 h-12 rounded-full bg-gold/95 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-all duration-500 translate-y-4 group-hover:translate-y-0">
                                <svg class="w-5 h-5 text-black" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0zM10 7v3m0 0v3m0-3h3m-3 0H7"></path>
                                </svg>
                            </div>
                        </div>
                    </div>
                    <div class="p-8">
                        <h3 class="text-xl font-medium mb-4">西安盛铂清居酒店</h3>
                        <div class="grid grid-cols-2 gap-3 text-sm text-muted">
                            <div>时间 · 2023</div>
                            <div>地点 · 陕西西安</div>
                            <div>面积 · 7000㎡</div>
                            <div>服务 · 空间设计</div>
                        </div>
                    </div>
                </div>
                
                <!-- 案例5 新都豪生 -->
                <div class="hotel-item bg-card rounded-3xl overflow-hidden shadow-card card-3d cursor-pointer" data-category="hotel" data-img="images/hotel-5-howard.jpg" data-title="成都新都豪生Life酒店" data-desc="2023 · 四川成都 · 12000㎡">
                    <div class="aspect-[4/3] overflow-hidden relative group bg-[#201D18]">
                        <img src="images/hotel-5-howard.jpg" alt="成都新都豪生Life酒店" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-700">
                        <div class="absolute inset-0 bg-black/0 group-hover:bg-black/20 transition-all duration-500 flex items-center justify-center">
                            <div class="w-12 h-12 rounded-full bg-gold/95 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-all duration-500 translate-y-4 group-hover:translate-y-0">
                                <svg class="w-5 h-5 text-black" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0zM10 7v3m0 0v3m0-3h3m-3 0H7"></path>
                                </svg>
                            </div>
                        </div>
                    </div>
                    <div class="p-8">
                        <h3 class="text-xl font-medium mb-4">成都新都豪生Life酒店</h3>
                        <div class="grid grid-cols-2 gap-3 text-sm text-muted">
                            <div>时间 · 2023</div>
                            <div>地点 · 四川成都</div>
                            <div>面积 · 12000㎡</div>
                            <div>服务 · 空间设计</div>
                        </div>
                    </div>
                </div>
                
                <!-- 案例6 凯莱希 -->
                <div class="hotel-item bg-card rounded-3xl overflow-hidden shadow-card card-3d cursor-pointer" data-category="hotel" data-img="images/hotel-6-kalasi.jpg" data-title="凯莱希假日酒店" data-desc="2022 · 四川成都 · 4000㎡">
                    <div class="aspect-[4/3] overflow-hidden relative group bg-[#201D18]">
                        <img src="images/hotel-6-kalasi.jpg" alt="凯莱希假日酒店" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-700">
                        <div class="absolute inset-0 bg-black/0 group-hover:bg-black/20 transition-all duration-500 flex items-center justify-center">
                            <div class="w-12 h-12 rounded-full bg-gold/95 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-all duration-500 translate-y-4 group-hover:translate-y-0">
                                <svg class="w-5 h-5 text-black" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0zM10 7v3m0 0v3m0-3h3m-3 0H7"></path>
                                </svg>
                            </div>
                        </div>
                    </div>
                    <div class="p-8">
                        <h3 class="text-xl font-medium mb-4">凯莱希假日酒店</h3>
                        <div class="grid grid-cols-2 gap-3 text-sm text-muted">
                            <div>时间 · 2022</div>
                            <div>地点 · 四川成都</div>
                            <div>面积 · 4000㎡</div>
                            <div>服务 · 空间设计</div>
                        </div>
                    </div>
                </div>
                
                <!-- 案例7 廷泊 -->
                <div class="hotel-item bg-card rounded-3xl overflow-hidden shadow-card card-3d cursor-pointer md:col-span-2 lg:col-span-1" data-category="resort" data-img="images/hotel-7-tingbo.jpg" data-title="廷泊酒店" data-desc="2026 · 四川康定 · 6000㎡">
                    <div class="aspect-[4/3] overflow-hidden relative group bg-[#201D18]">
                        <img src="images/hotel-7-tingbo.jpg" alt="廷泊酒店" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-700">
                        <div class="absolute top-4 right-4 bg-gold text-black text-xs px-3 py-1 rounded-full z-10">NEW · 2026新作</div>
                        <div class="absolute inset-0 bg-black/0 group-hover:bg-black/20 transition-all duration-500 flex items-center justify-center">
                            <div class="w-12 h-12 rounded-full bg-gold/95 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-all duration-500 translate-y-4 group-hover:translate-y-0">
                                <svg class="w-5 h-5 text-black" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0zM10 7v3m0 0v3m0-3h3m-3 0H7"></path>
                                </svg>
                            </div>
                        </div>
                    </div>
                    <div class="p-8">
                        <h3 class="text-xl font-medium mb-4">廷泊酒店</h3>
                        <div class="grid grid-cols-2 gap-3 text-sm text-muted">
                            <div>时间 · 2026</div>
                            <div>地点 · 四川康定</div>
                            <div>面积 · 6000㎡</div>
                            <div>服务 · 空间设计</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 05 康养休闲案例 -->
    <section id="wellness" class="py-28 md:py-36 px-6 section-hero" style="background-image: url('images/wellness-section-bg.jpg')">
        <div class="max-w-6xl mx-auto fade-in">
            <div class="flex items-center gap-4 mb-16">
                <span class="text-gold text-xs font-en tracking-widest">05 / WELLNESS & LEISURE</span>
                <div class="h-px bg-ink/10 flex-1 max-w-[100px]"></div>
            </div>
            
            <h2 class="text-3xl md:text-5xl font-light mb-6 tracking-wide">康养休闲案例</h2>
            <p class="text-muted mb-16 max-w-xl text-lg">十余年深耕足浴健康与休闲空间设计，累计落地200+项目</p>
            
            <div class="grid grid-cols-2 md:grid-cols-4 gap-6 mb-12">
                <!-- 克拉拉 -->
                <div class="bg-card rounded-3xl shadow-card card-3d cursor-pointer overflow-hidden group" onclick="openLightbox('images/wellness-1-kelala.jpg','克拉拉','精品足道 · KELALA')">
                    <div class="aspect-[4/5] overflow-hidden bg-[#201D18]">
                        <img src="images/wellness-1-kelala.jpg" alt="克拉拉" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-700">
                    </div>
                    <div class="p-5 text-center">
                        <div class="font-medium text-lg mb-1 group-hover:text-gold transition-colors">克拉拉</div>
                        <div class="text-sm text-muted">精品足道</div>
                    </div>
                </div>
                <!-- 朋乐迹 -->
                <div class="bg-card rounded-3xl shadow-card card-3d cursor-pointer overflow-hidden group" onclick="openLightbox('images/wellness-2-pengleji.jpg','朋乐迹','休闲空间 · PENGLEJI')">
                    <div class="aspect-[4/5] overflow-hidden bg-[#201D18]">
                        <img src="images/wellness-2-pengleji.jpg" alt="朋乐迹" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-700">
                    </div>
                    <div class="p-5 text-center">
                        <div class="font-medium text-lg mb-1 group-hover:text-gold transition-colors">朋乐迹</div>
                        <div class="text-sm text-muted">休闲空间</div>
                    </div>
                </div>
                <!-- 莲足纪 -->
                <div class="bg-card rounded-3xl shadow-card card-3d cursor-pointer overflow-hidden group" onclick="openLightbox('images/wellness-3-lianzuji.jpg','莲足纪','中式足道 · LIANZUJI')">
                    <div class="aspect-[4/5] overflow-hidden bg-[#201D18]">
                        <img src="images/wellness-3-lianzuji.jpg" alt="莲足纪" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-700">
                    </div>
                    <div class="p-5 text-center">
                        <div class="font-medium text-lg mb-1 group-hover:text-gold transition-colors">莲足纪</div>
                        <div class="text-sm text-muted">中式足道</div>
                    </div>
                </div>
                <!-- 臻享足道 -->
                <div class="bg-card rounded-3xl shadow-card card-3d cursor-pointer overflow-hidden group" onclick="openLightbox('images/wellness-4-zhenxiang.jpg','臻享足道','健康足道 · ZHENXIANG')">
                    <div class="aspect-[4/5] overflow-hidden bg-[#201D18]">
                        <img src="images/wellness-4-zhenxiang.jpg" alt="臻享足道" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-700">
                    </div>
                    <div class="p-5 text-center">
                        <div class="font-medium text-lg mb-1 group-hover:text-gold transition-colors">臻享足道</div>
                        <div class="text-sm text-muted">健康足道</div>
                    </div>
                </div>
                <!-- 朋悦·泰 -->
                <div class="bg-card rounded-3xl shadow-card card-3d cursor-pointer overflow-hidden group" onclick="openLightbox('images/wellness-5-pengyue.jpg','朋悦·泰','养生SPA · PENGYUE')">
                    <div class="aspect-[4/5] overflow-hidden bg-[#201D18]">
                        <img src="images/wellness-5-pengyue.jpg" alt="朋悦·泰" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-700">
                    </div>
                    <div class="p-5 text-center">
                        <div class="font-medium text-lg mb-1 group-hover:text-gold transition-colors">朋悦·泰</div>
                        <div class="text-sm text-muted">养生SPA</div>
                    </div>
                </div>
                <!-- 楠锦荟 -->
                <div class="bg-card rounded-3xl shadow-card card-3d cursor-pointer overflow-hidden group" onclick="openLightbox('images/wellness-6-nanjinhui.jpg','楠锦荟','水汇休闲 · NANJINHUI')">
                    <div class="aspect-[4/5] overflow-hidden bg-[#201D18]">
                        <img src="images/wellness-6-nanjinhui.jpg" alt="楠锦荟" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-700">
                    </div>
                    <div class="p-5 text-center">
                        <div class="font-medium text-lg mb-1 group-hover:text-gold transition-colors">楠锦荟</div>
                        <div class="text-sm text-muted">水汇休闲</div>
                    </div>
                </div>
                <!-- 美足时光 -->
                <div class="bg-card rounded-3xl shadow-card card-3d cursor-pointer overflow-hidden group" onclick="openLightbox('images/wellness-7-meizu.jpg','美足时光','休闲足道 · MEIZU')">
                    <div class="aspect-[4/5] overflow-hidden bg-[#201D18]">
                        <img src="images/wellness-7-meizu.jpg" alt="美足时光" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-700">
                    </div>
                    <div class="p-5 text-center">
                        <div class="font-medium text-lg mb-1 group-hover:text-gold transition-colors">美足时光</div>
                        <div class="text-sm text-muted">休闲足道</div>
                    </div>
                </div>
                <!-- 栖隐 -->
                <div class="bg-card rounded-3xl shadow-card card-3d cursor-pointer overflow-hidden group" onclick="openLightbox('images/wellness-8-qiyin.jpg','栖隐','禅意养生 · QIYIN')">
                    <div class="aspect-[4/5] overflow-hidden bg-[#201D18]">
                        <img src="images/wellness-8-qiyin.jpg" alt="栖隐" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-700">
                    </div>
                    <div class="p-5 text-center">
                        <div class="font-medium text-lg mb-1 group-hover:text-gold transition-colors">栖隐</div>
                        <div class="text-sm text-muted">禅意养生</div>
                    </div>
                </div>
            </div>
            
            <p class="text-muted text-center text-lg">
                更多项目：春天印象 · 沐芳华 · 云足道 · 观澜境会馆 · 涪江月 · 寻境K歌沐足 · 飞花令
            </p>
        </div>
    </section>

    <!-- 06 品牌理念 -->
    <section class="py-28 md:py-36 px-6 bg-[#0A0A0A] text-white relative overflow-hidden">
        <div class="absolute inset-0 opacity-20">
            <img src="images/philosophy-bg.jpg" alt="" class="w-full h-full object-cover">
        </div>
        <div class="max-w-5xl mx-auto text-center fade-in relative z-10">
            <span class="text-gold/80 text-xs font-en tracking-widest">06 / PHILOSOPHY</span>
            <h2 class="text-3xl md:text-5xl font-light mt-8 mb-20 tracking-wide">品牌理念</h2>
            
            <div class="grid md:grid-cols-3 gap-16 mb-20">
                <div class="group">
                    <div class="text-gold text-3xl mb-6 group-hover:scale-110 transition-transform duration-500">执专业之尺</div>
                    <p class="text-white/60 leading-relaxed">以专业为根基，严谨对待每一个项目细节</p>
                </div>
                <div class="group">
                    <div class="text-gold text-3xl mb-6 group-hover:scale-110 transition-transform duration-500">怀敬畏之心</div>
                    <p class="text-white/60 leading-relaxed">敬畏空间、敬畏客户、敬畏每一份信任</p>
                </div>
                <div class="group">
                    <div class="text-gold text-3xl mb-6 group-hover:scale-110 transition-transform duration-500">筑有温度的空间</div>
                    <p class="text-white/60 leading-relaxed">让空间不止于设计，更成为值得回味的场域</p>
                </div>
            </div>
            
            <p class="text-white/50 max-w-2xl mx-auto leading-relaxed text-lg">
                以专业为尺、以敬畏为心、以温度为魂——让空间不止于设计，更成为值得回味的场域。
            </p>
        </div>
    </section>

    <!-- 07 联系我们 -->
    <section id="contact" class="py-28 md:py-36 px-6">
        <div class="max-w-5xl mx-auto fade-in">
            <div class="flex items-center gap-4 mb-16">
                <span class="text-gold text-xs font-en tracking-widest">07 / CONTACT</span>
                <div class="h-px bg-ink/10 flex-1 max-w-[100px]"></div>
            </div>
            
            <div class="grid md:grid-cols-2 gap-20 items-center">
                <div>
                    <h2 class="text-3xl md:text-5xl font-light mb-8 tracking-wide">联系我们</h2>
                    <p class="text-muted mb-12 text-xl">期待与您同行</p>
                    
                    <div class="space-y-8">
                        <div>
                            <div class="text-sm text-muted mb-2">联系电话</div>
                            <a href="tel:13678080880" class="text-2xl tracking-wide font-light inline-block transition-colors hover:text-gold">136 7808 0880</a>
                        </div>
                        <div>
                            <div class="text-sm text-muted mb-2">公司地址</div>
                            <div class="leading-relaxed text-lg">
                                四川成都 · 利星行广场<br>
                                <span class="text-muted">成华区龙潭工业园航天路5号</span>
                            </div>
                        </div>
                    </div>
                    
                    <!-- 区位地图 -->
                    <div class="mt-10 rounded-2xl overflow-hidden shadow-card">
                        <img src="images/contact-map.png" alt="公司区位图" class="w-full h-auto">
                    </div>
                </div>
                
                <div class="bg-card rounded-3xl p-10 shadow-card card-3d">
                    <div class="aspect-square bg-paper rounded-2xl flex items-center justify-center mb-6 overflow-hidden">
                        <img src="images/contact-qrcode.png" alt="微信咨询二维码" class="w-3/4 h-3/4 object-contain">
                    </div>
                    <p class="text-center text-muted">扫码咨询 · 期待与您同行</p>
                    <div class="mt-6 pt-6 border-t border-ink/5 text-center">
                        <img src="images/contact-icon.png" alt="" class="h-8 mx-auto object-contain opacity-60" onerror="this.style.display='none'">
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 页脚 -->
    <footer class="py-12 px-6 border-t border-ink/5 relative overflow-hidden">
        <div class="absolute inset-0 opacity-5">
            <img src="images/footer-bg.png" alt="" class="w-full h-full object-cover">
        </div>
        <div class="max-w-6xl mx-auto flex flex-col md:flex-row justify-between items-center gap-4 text-sm text-muted relative z-10">
            <div class="flex items-center gap-3">
                <img src="images/footer-logo.png" alt="空谷设计" class="h-5 object-contain" onerror="this.style.display='none'">
                <span>© 2026 空谷设计 KONGGU DESIGN. All Rights Reserved.</span>
            </div>
            <div class="font-en tracking-wider">CHENGDU · CHINA · EST. 2010S</div>
        </div>
    </footer>

    <script>
        // ========== 隐私保护 ==========
        document.addEventListener('contextmenu', e => e.preventDefault());
        document.addEventListener('selectstart', e => e.preventDefault());
        document.addEventListener('dragstart', e => e.preventDefault());
        
        document.addEventListener('keydown', function(e) {
            if ((e.ctrlKey || e.metaKey) && e.key === 's') { e.preventDefault(); return false; }
            if ((e.ctrlKey || e.metaKey) && e.key === 'p') { e.preventDefault(); return false; }
            if (e.key === 'F12' || ((e.ctrlKey || e.metaKey) && e.shiftKey && e.key === 'i')) { e.preventDefault(); return false; }
            if ((e.ctrlKey || e.metaKey) && e.key === 'u') { e.preventDefault(); return false; }
            if (e.key === 'PrintScreen') { e.preventDefault(); return false; }
        });

        // ========== 导航栏滚动效果 ==========
        const navbar = document.getElementById('navbar');
        const backToTop = document.getElementById('backToTop');
        const sections = document.querySelectorAll('section[id]');
        const navLinks = document.querySelectorAll('.nav-link');

        window.addEventListener('scroll', () => {
            if (window.scrollY > 80) {
                navbar.classList.add('bg-black/85', 'bg-blur', 'shadow-sm', 'py-3');
                navbar.classList.remove('py-6');
            } else {
                navbar.classList.remove('bg-black/85', 'bg-blur', 'shadow-sm', 'py-3');
                navbar.classList.add('py-6');
            }

            if (window.scrollY > 500) {
                backToTop.classList.remove('opacity-0', 'invisible');
                backToTop.classList.add('opacity-100', 'visible');
            } else {
                backToTop.classList.add('opacity-0', 'invisible');
                backToTop.classList.remove('opacity-100', 'visible');
            }

            let current = '';
            sections.forEach(section => {
                const sectionTop = section.offsetTop - 150;
                if (window.scrollY >= sectionTop) {
                    current = section.getAttribute('id');
                }
            });

            navLinks.forEach(link => {
                link.classList.remove('text-ink', 'font-medium');
                if (link.getAttribute('href') === '#' + current) {
                    link.classList.add('text-ink', 'font-medium');
                }
            });
        });

        backToTop.addEventListener('click', () => {
            window.scrollTo({ top: 0, behavior: 'smooth' });
        });

        // ========== 平滑滚动 ==========
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({ behavior: 'smooth', block: 'start' });
                }
            });
        });

        // ========== 滚动渐入动画 ==========
        const observerOptions = { threshold: 0.1, rootMargin: '0px 0px -100px 0px' };
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                    if (entry.target.querySelector('.counter')) {
                        startCounters();
                    }
                }
            });
        }, observerOptions);

        document.querySelectorAll('.fade-in').forEach(el => observer.observe(el));

        // ========== 数字滚动动画 ==========
        let countersStarted = false;
        function startCounters() {
            if (countersStarted) return;
            countersStarted = true;
            
            document.querySelectorAll('.counter').forEach(counter => {
                const target = +counter.getAttribute('data-target');
                const duration = 2000;
                const step = target / (duration / 16);
                let current = 0;

                const updateCounter = () => {
                    current += step;
                    if (current < target) {
                        counter.innerText = Math.floor(current);
                        requestAnimationFrame(updateCounter);
                    } else {
                        counter.innerText = target;
                    }
                };
                updateCounter();
            });
        }

        // ========== 案例筛选 ==========
        const filterBtns = document.querySelectorAll('.filter-btn');
        const hotelItems = document.querySelectorAll('.hotel-item');

        filterBtns.forEach(btn => {
            btn.addEventListener('click', () => {
                filterBtns.forEach(b => b.classList.remove('active'));
                btn.classList.add('active');

                const filter = btn.getAttribute('data-filter');
                
                hotelItems.forEach(item => {
                    const category = item.getAttribute('data-category');
                    if (filter === 'all' || category === filter) {
                        item.style.display = 'block';
                        setTimeout(() => {
                            item.style.opacity = '1';
                            item.style.transform = 'translateY(0)';
                        }, 50);
                    } else {
                        item.style.opacity = '0';
                        item.style.transform = 'translateY(20px)';
                        setTimeout(() => {
                            item.style.display = 'none';
                        }, 300);
                    }
                });
            });
        });

        // ========== 图片灯箱 ==========
        const lightbox = document.getElementById('lightbox');
        const lightboxImg = document.getElementById('lightboxImg');
        const lightboxText = document.querySelector('#lightboxText h3');
        const lightboxDesc = document.querySelector('#lightboxText p');
        const closeLightbox = document.getElementById('closeLightbox');

        function openLightbox(imgSrc, title, desc) {
            lightboxImg.src = imgSrc;
            lightboxText.textContent = title;
            lightboxDesc.textContent = desc;
            lightbox.classList.add('active');
            document.body.style.overflow = 'hidden';
        }

        hotelItems.forEach(item => {
            item.addEventListener('click', () => {
                const imgSrc = item.getAttribute('data-img');
                const title = item.getAttribute('data-title');
                const desc = item.getAttribute('data-desc');
                openLightbox(imgSrc, title, desc);
            });
        });

        function closeLightboxFunc() {
            lightbox.classList.remove('active');
            document.body.style.overflow = '';
        }

        closeLightbox.addEventListener('click', closeLightboxFunc);
        lightbox.addEventListener('click', (e) => {
            if (e.target === lightbox) closeLightboxFunc();
        });
        document.addEventListener('keydown', (e) => {
            if (e.key === 'Escape' && lightbox.classList.contains('active')) {
                closeLightboxFunc();
            }
        });

        // ========== 页面加载触发首屏动画 ==========
        window.addEventListener('load', () => {
            document.querySelector('.fade-in').classList.add('visible');
        });
        // ========== 黑金主题 · 增强交互 ==========

        // 顶部金色滚动进度条
        const progressBar = document.createElement('div');
        progressBar.className = 'progress-bar';
        document.body.appendChild(progressBar);
        let scrollTicking = false;
        window.addEventListener('scroll', () => {
            if (!scrollTicking) {
                scrollTicking = true;
                requestAnimationFrame(() => {
                    const h = document.documentElement;
                    const max = h.scrollHeight - h.clientHeight;
                    progressBar.style.width = (max > 0 ? (h.scrollTop / max) * 100 : 0) + '%';
                    scrollTicking = false;
                });
            }
        }, { passive: true });

        // 卡片 3D 跟随鼠标倾斜（触屏设备自动跳过）
        if (window.matchMedia('(hover: hover)').matches) {
            document.querySelectorAll('.card-3d').forEach(card => {
                card.addEventListener('mousemove', (e) => {
                    const r = card.getBoundingClientRect();
                    const px = (e.clientX - r.left) / r.width - 0.5;
                    const py = (e.clientY - r.top) / r.height - 0.5;
                    card.style.transform = 'translateY(-6px) rotateX(' + (-py * 6).toFixed(2) + 'deg) rotateY(' + (px * 6).toFixed(2) + 'deg)';
                });
                card.addEventListener('mouseleave', () => {
                    card.style.transform = '';
                });
            });
        }

        // 首屏背景微视差
        const heroBgImg = document.querySelector('#top .absolute.inset-0 img');
        if (heroBgImg) {
            window.addEventListener('scroll', () => {
                if (window.scrollY < window.innerHeight * 1.2) {
                    heroBgImg.style.transform = 'translateY(' + (window.scrollY * 0.22).toFixed(1) + 'px) scale(1.06)';
                }
            }, { passive: true });
        }
    </script>
</body>
</html>
