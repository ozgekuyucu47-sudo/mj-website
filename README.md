# mj-website
first version
[Uploading ai_studio_code.html…]()
<!DOCTYPE html>
<html lang="tr" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MJ: Moonwalk Efsanesi & Neverland Merch</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        mjGold: '#f59e0b',
                        mjRed: '#dc2626',
                        mjDark: '#0f172a',
                    },
                    animation: {
                        'float': 'float 4s ease-in-out infinite',
                        'pulse-glow': 'pulseGlow 2s ease-in-out infinite',
                    },
                    keyframes: {
                        float: {
                            '0%, 100%': { transform: 'translateY(0)' },
                            '50%': { transform: 'translateY(-12px)' },
                        },
                        pulseGlow: {
                            '0%, 100%': { opacity: '0.4' },
                            '50%': { opacity: '0.9' },
                        }
                    }
                }
            }
        }
    </script>
    <style>
        .fedora-shadow {
            filter: drop-shadow(0 15px 25px rgba(220, 38, 38, 0.35));
        }
    </style>
</head>
<body class="bg-slate-950 text-slate-100 font-sans selection:bg-amber-400 selection:text-black">

    <!-- ÜST MENÜ & SEPET SAYAÇ -->
    <header class="fixed top-0 left-0 w-full bg-slate-900/80 backdrop-blur-md border-b border-slate-800 z-50">
        <div class="max-w-6xl mx-auto px-4 h-16 flex items-center justify-between">
            <a href="#hero" class="flex items-center gap-2 font-black tracking-wider text-xl text-amber-400 hover:text-amber-300">
                <span>✦ MJ ARCHIVE</span>
            </a>
            <nav class="hidden md:flex gap-6 text-sm font-medium">
                <a href="#gecmis" class="hover:text-amber-400 transition">Erken Dönem</a>
                <a href="#populer" class="hover:text-amber-400 transition">King of Pop</a>
                <a href="#hayvanlar" class="hover:text-amber-400 transition">Neverland Sakinleri</a>
                <a href="#magaza" class="hover:text-amber-400 transition">Peluş Merch</a>
            </nav>
            <div class="flex items-center gap-3">
                <a href="#magaza" class="relative bg-amber-500 hover:bg-amber-400 text-slate-950 font-bold px-4 py-2 rounded-full text-xs transition flex items-center gap-2">
                    <span>🛒 Peluş Sepeti</span>
                    <span id="cart-count" class="bg-slate-950 text-white rounded-full w-5 h-5 flex items-center justify-center text-[10px]">0</span>
                </a>
            </div>
        </div>
    </header>

    <!-- BÖLÜM 1: GİRİŞ (HERO & GEOMETRİK ÖZGÜN MJ KARİKATÜRÜ) -->
    <section id="hero" class="min-h-screen pt-24 pb-16 flex items-center justify-center relative overflow-hidden bg-gradient-to-b from-slate-950 via-slate-900 to-slate-950">
        <div class="absolute inset-0 bg-[radial-gradient(circle_at_center,_var(--tw-gradient-stops))] from-amber-500/10 via-transparent to-transparent"></div>
        
        <div class="max-w-5xl mx-auto px-4 flex flex-col md:flex-row items-center gap-12 relative z-10">
            <!-- Karikatür İllüstrasyonu (Geometrik SVG: Emojisiz, özgün, gözlüklü, gülümseyen MJ portresi) -->
            <div class="w-64 h-64 md:w-80 md:h-80 relative animate-float fedora-shadow flex-shrink-0">
                <svg viewBox="0 0 200 200" class="w-full h-full" xmlns="http://www.w3.org/2000/svg">
                    <!-- Arka Parlama -->
                    <circle cx="100" cy="100" r="92" fill="#1e293b" stroke="#f59e0b" stroke-width="3" stroke-dasharray="6 4"/>
                    <!-- Saç Bukleleri (Geometrik daireler ve yaylar) -->
                    <path d="M 50 110 Q 30 80 60 50 Q 100 20 150 50 Q 175 85 150 120" fill="#09090b" />
                    <circle cx="48" cy="105" r="14" fill="#09090b"/>
                    <circle cx="45" cy="125" r="12" fill="#09090b"/>
                    <circle cx="155" cy="105" r="14" fill="#09090b"/>
                    <circle cx="155" cy="125" r="12" fill="#09090b"/>
                    <!-- Yüz Geometrisi -->
                    <path d="M 65 75 Q 100 85 135 75 L 130 130 Q 100 160 70 130 Z" fill="#fde68a"/>
                    <!-- Çene gamzesi (İmzası) -->
                    <circle cx="100" cy="142" r="2.5" fill="#d97706"/>
                    <!-- Ünlü Geniş Gülümseme -->
                    <path d="M 78 118 Q 100 135 122 118 Z" fill="#ffffff" stroke="#b45309" stroke-width="1.5"/>
                    <line x1="78" y1="118" x2="122" y2="118" stroke="#cbd5e1" stroke-width="1.5"/>
                    <path d="M 75 116 Q 100 144 125 116" fill="none" stroke="#d97706" stroke-width="2"/>
                    <!-- Güneş Gözlüğü (Aviator Tarzı Geometrik Lensler) -->
                    <polygon points="62,80 96,80 92,105 68,105" fill="#020617" stroke="#f59e0b" stroke-width="2.5" rx="3"/>
                    <polygon points="104,80 138,80 132,105 108,105" fill="#020617" stroke="#f59e0b" stroke-width="2.5" rx="3"/>
                    <line x1="96" y1="83" x2="104" y2="83" stroke="#f59e0b" stroke-width="3"/>
                    <!-- Cam Üzeri Işık Yansıması -->
                    <line x1="68" y1="84" x2="82" y2="101" stroke="#38bdf8" stroke-width="2" stroke-linecap="round"/>
                    <line x1="110" y1="84" x2="124" y2="101" stroke="#38bdf8" stroke-width="2" stroke-linecap="round"/>
                    <!-- Şapka (Fedora) -->
                    <path d="M 35 68 Q 100 58 165 68 L 155 60 Q 100 52 45 60 Z" fill="#18181b"/>
                    <path d="M 60 62 L 68 28 Q 100 35 132 28 L 140 62 Z" fill="#18181b"/>
                    <!-- Şapka Beyaz Kurdelesi -->
                    <path d="M 61 58 L 63 50 Q 100 57 137 50 L 139 58 Z" fill="#ffffff"/>
                    <!-- Kırmızı Sahne Ceketi Yakası -->
                    <polygon points="60,150 100,185 140,150 150,195 50,195" fill="#dc2626"/>
                    <polygon points="85,160 100,180 115,160 100,195" fill="#f8fafc"/>
                    <!-- İkonik Alından Düşen Tek Bukle -->
                    <path d="M 98 48 Q 90 70 99 80" fill="none" stroke="#09090b" stroke-width="3" stroke-linecap="round"/>
                </svg>
            </div>

            <div class="text-center md:text-left">
                <div class="inline-block px-3 py-1 bg-red-900/40 border border-red-500/30 text-red-300 rounded-full text-xs font-semibold mb-4 tracking-wider uppercase">
                    Yapay Zeka & Efsaneler Dersi Özel Projesi
                </div>
                <h1 class="text-4xl md:text-6xl font-extrabold tracking-tight text-white mb-4">
                    Hee-Hee! <br><span class="text-transparent bg-clip-text bg-gradient-to-r from-amber-400 to-red-500">Popun Kralı</span> Aramızda!
                </h1>
                <p class="text-slate-300 text-base md:text-lg max-w-xl leading-relaxed mb-6">
                    Yer çekimine meydan okuyan ayakkabılar, Neverland'in çay içen şempanzeleri ve 70 milyondan fazla satan albümler... Ay yürüyüşü hızında hazırlanmış en gerçekçi ve mizahi MJ rehberine hoş geldin!
                </p>
                <div class="flex flex-wrap gap-4 justify-center md:justify-start">
                    <a href="#gecmis" class="bg-amber-500 hover:bg-amber-400 text-slate-950 font-bold px-6 py-3 rounded-xl transition duration-200">
                        Keşfe Başla ↓
                    </a>
                    <a href="#magaza" class="bg-slate-800 hover:bg-slate-700 text-white font-semibold px-6 py-3 rounded-xl border border-slate-700 transition duration-200">
                        Neverland Merch Dükkanı 🛒
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- BÖLÜM 2: GEÇMİŞ (WIKIPEDIA DOĞRULANMIŞ - CİDDİ & BİLGİLENDİRİCİ TON) -->
    <section id="gecmis" class="py-20 bg-slate-900/90 border-t border-b border-slate-800">
        <div class="max-w-4xl mx-auto px-4">
            <div class="border-l-4 border-amber-500 pl-4 mb-10">
                <span class="text-xs font-semibold uppercase tracking-widest text-slate-400">Tarihsel Biyografi (1958 – 1979)</span>
                <h2 class="text-3xl font-bold text-white mt-1">Gary'den Sahnelere: Bir Müzik Dehasının İlk Yılları</h2>
            </div>
            
            <div class="space-y-6 text-slate-300 leading-relaxed text-sm md:text-base">
                <p>
                    Michael Joseph Jackson, <strong>29 Ağustos 1958</strong> tarihinde Amerika Birleşik Devletleri'nin Indiana eyaletine bağlı Gary kentinde, işçi sınıfı bir Afro-Amerikan ailenin sekizinci çocuğu olarak dünyaya geldi. Annesi Katherine Esther Scruse dindar bir Yehova Şahidi, babası Joseph Walter "Joe" Jackson ise vinç operatörlüğü yapan ve eski bir blues gitaristi olan katı bir aile reisiydi.
                </p>
                <div class="grid md:grid-cols-2 gap-4 my-6">
                    <div class="bg-slate-950/60 p-5 rounded-xl border border-slate-800">
                        <h3 class="text-amber-400 font-semibold mb-2">The Jackson 5 ve Motown Efsanesi</h3>
                        <p class="text-xs text-slate-400 leading-normal">
                            1964 yılında kardeşleri Jackie, Tito, Jermaine ve Marlon ile kurulan gruba katıldı. 1968'de efsanevi Motown Records ile imzaladıkları sözleşmenin ardından yayımlanan ilk 4 single'ı (<em>"I Want You Back"</em>, <em>"ABC"</em>, <em>"The Love You Save"</em> ve <em>"I'll Be There"</em>) Billboard Hot 100 listesinde arka arkaya 1 numaraya yerleşerek müzik tarihine geçti.
                        </p>
                    </div>
                    <div class="bg-slate-950/60 p-5 rounded-xl border border-slate-800">
                        <h3 class="text-amber-400 font-semibold mb-2">İlk Solo Adımlar ve Özgürleşme</h3>
                        <p class="text-xs text-slate-400 leading-normal">
                            Grup çalışmalarının yanı sıra Motown etiketiyle <em>Got to Be There</em> (1972) ve bir fareye ithafen yazılan şarkıyla liste başı olan <em>Ben</em> (1972) gibi ilk solo albümlerini çıkardı. 1979 yılında prodüktör Quincy Jones ile kaydettiği <em>Off the Wall</em> albümü, çocuk yıldız kimliğini geride bırakıp yetişkin bir süperstara dönüşmesinin kesin dönüm noktası oldu.
                        </p>
                    </div>
                </div>
                <p>
                    Jackson ailesinin yoğun ve disiplinli prova süreçleri, Michael'ın genç yaşta olağanüstü bir vokal tekniği ve ritim kabiliyeti geliştirmesini sağladı. 1970'lerin sonuna gelindiğinde, kendi bestelerini yazan, grubun yaratıcı kontrolünü eline alan ve tek başına bir pop devrimi başlatmaya hazır bir figür haline gelmişti.
                </p>
            </div>
        </div>
    </section>

    <!-- BÖLÜM 3: POPÜLER DÖNEM (ALBÜMLER, ŞARKILAR, ÖDÜLLER, BAĞIŞLAR - MİZAHİ & ENERJİK TON) -->
    <section id="populer" class="py-20 bg-slate-950 relative">
        <div class="max-w-6xl mx-auto px-4">
            <div class="text-center max-w-2xl mx-auto mb-16">
                <span class="text-red-400 font-bold uppercase tracking-wider text-xs">Rekorlar Kitabı Çaresiz Kaldı</span>
                <h2 class="text-3xl md:text-5xl font-black text-white mt-2">Gezegeni Titreten Dönem: Thriller ve Ötesi</h2>
                <p class="text-slate-400 mt-3 text-sm">Dünyanın "Bu kadar da satamazsın artık" deyip Michael'ın "Dur daha yeni başladım" dediği o yıllar...</p>
            </div>

            <!-- Albümler & Hit Şarkılar Izgarası -->
            <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mb-12">
                <div class="bg-gradient-to-b from-slate-900 to-slate-950 p-6 rounded-2xl border border-red-500/20 hover:border-red-500/60 transition group">
                    <div class="w-12 h-12 bg-red-600/20 text-red-500 rounded-lg flex items-center justify-center font-black text-xl mb-4 group-hover:scale-110 transition">
                        70M+
                    </div>
                    <h3 class="text-xl font-bold text-white">Thriller (1982)</h3>
                    <p class="text-xs text-amber-400 font-semibold mb-2">Tüm Zamanların En Çok Satan Albümü</p>
                    <p class="text-xs text-slate-400 leading-relaxed">
                        Zombilere dans etmeyi öğreten albüm. <em>Billie Jean</em>, <em>Beat It</em> ve <em>Thriller</em> klipleriyle MTV'nin yayın akışını tek başına baştan yarattı.
                    </p>
                </div>

                <div class="bg-gradient-to-b from-slate-900 to-slate-950 p-6 rounded-2xl border border-amber-500/20 hover:border-amber-500/60 transition group">
                    <div class="w-12 h-12 bg-amber-600/20 text-amber-500 rounded-lg flex items-center justify-center font-black text-xl mb-4 group-hover:scale-110 transition">
                        5 #1
                    </div>
                    <h3 class="text-xl font-bold text-white">Bad (1987)</h3>
                    <p class="text-xs text-amber-400 font-semibold mb-2">Tarihte Tek Albümden 5 Tane 1 Numara</p>
                    <p class="text-xs text-slate-400 leading-relaxed">
                        <em>Smooth Criminal</em> ile yerçekimine "sen biraz bekle" dedi. Kemerler, tokalar ve meşhur 45 derecelik eğilme büyüsü bu döneme aittir.
                    </p>
                </div>

                <div class="bg-gradient-to-b from-slate-900 to-slate-950 p-6 rounded-2xl border border-blue-500/20 hover:border-blue-500/60 transition group">
                    <div class="w-12 h-12 bg-blue-600/20 text-blue-500 rounded-lg flex items-center justify-center font-black text-xl mb-4 group-hover:scale-110 transition">
                        90'lar
                    </div>
                    <h3 class="text-xl font-bold text-white">Dangerous & HIStory</h3>
                    <p class="text-xs text-amber-400 font-semibold mb-2">Black or White & Scream Çağı</p>
                    <p class="text-xs text-slate-400 leading-relaxed">
                        Macaulay Culkin ile kapı çalma şakaları, devasa stadyum konserleri ve pop müzik kliplerine Hollywood bütçeleri ayırma dönemi!
                    </p>
                </div>
            </div>

            <!-- Ödüller ve Bağışlar Şeridi -->
            <div class="bg-slate-900 border border-slate-800 rounded-2xl p-6 md:p-8 flex flex-col md:flex-row gap-8 items-center justify-between">
                <div>
                    <h4 class="text-lg font-bold text-white mb-2">🏆 Ödül Rafı Çöken Adam</h4>
                    <p class="text-xs text-slate-300 max-w-xl">
                        13 Grammy Ödülü, Grammy Yaşam Boyu Başarı Ödülü ve 26 American Music Awards. Bir gecede 8 Grammy kazanıp kucaklayamadığı için görevlilere taşıttığı 1984 töreni halen efsanedir.
                    </p>
                </div>
                <div class="md:border-l md:border-slate-800 md:pl-8">
                    <h4 class="text-lg font-bold text-amber-400 mb-2">🌍 Rekor Bağışlar & Heal the World</h4>
                    <p class="text-xs text-slate-300 max-w-xl">
                        1985'te Afrika'daki açlık için yazılan <em>We Are the World</em> ile 60 milyon dolardan fazla gelir. Guinness Rekorlar Kitabı'na <strong>en çok hayır kurumunu destekleyen pop yıldızı</strong> (39 kurum ve 300+ milyon dolar) olarak adını yazdırdı.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- BÖLÜM 4: EVCİL HAYVANLAR & FUN FACTS (EĞLENCELİ GEOMETRİK ÇİZİMLERLE) -->
    <section id="hayvanlar" class="py-20 bg-slate-900/50 border-t border-slate-800">
        <div class="max-w-6xl mx-auto px-4">
            <div class="text-center max-w-2xl mx-auto mb-16">
                <span class="text-amber-400 font-bold uppercase tracking-wider text-xs">Neverland Hayvanat Bahçesi</span>
                <h2 class="text-3xl md:text-5xl font-black text-white mt-2">Normal İnsan Köpek Besler, MJ İse...</h2>
                <p class="text-slate-400 mt-2 text-sm">Michael'ın Neverland çiftliğinde yaşayan ve muhtemelen çoğumuzdan daha lüks hayat süren dostları:</p>
            </div>

            <!-- Hayvan Kartları (Özgün Geometrik Vektör Çizimler) -->
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-16">
                <!-- 1. Bubbles (Şempanze) -->
                <div class="bg-slate-950 p-6 rounded-2xl border border-slate-800 text-center flex flex-col items-center">
                    <div class="w-36 h-36 mb-4">
                        <svg viewBox="0 0 100 100" class="w-full h-full">
                            <!-- Kulaklar -->
                            <circle cx="20" cy="50" r="14" fill="#a16207"/>
                            <circle cx="20" cy="50" r="8" fill="#fde047"/>
                            <circle cx="80" cy="50" r="14" fill="#a16207"/>
                            <circle cx="80" cy="50" r="8" fill="#fde047"/>
                            <!-- Kafa -->
                            <circle cx="50" cy="50" r="32" fill="#78350f"/>
                            <!-- Yüz maskesi -->
                            <ellipse cx="50" cy="58" rx="22" ry="16" fill="#fef08a"/>
                            <circle cx="40" cy="45" r="4" fill="#000"/>
                            <circle cx="60" cy="45" r="4" fill="#000"/>
                            <!-- Sevimli Burun ve Ağız -->
                            <circle cx="47" cy="54" r="1.5" fill="#78350f"/>
                            <circle cx="53" cy="54" r="1.5" fill="#78350f"/>
                            <path d="M 44 63 Q 50 68 56 63" stroke="#78350f" stroke-width="2" fill="none"/>
                            <!-- Kırmızı Papyon -->
                            <polygon points="40,82 60,82 50,75" fill="#dc2626"/>
                        </svg>
                    </div>
                    <h3 class="text-xl font-bold text-white">Bubbles (Şempanze)</h3>
                    <p class="text-xs text-amber-400 font-semibold mb-2">Çay Saati Müdavimi</p>
                    <p class="text-xs text-slate-400 leading-normal">
                        Michael ile birlikte dünya turnesine çıkan, smokin giyen ve Japonya Belediye Başkanı ile resmi fincanlarda yeşil çay yudumlayan tarihteki tek maymun.
                    </p>
                </div>

                <!-- 2. Louie (Lama) -->
                <div class="bg-slate-950 p-6 rounded-2xl border border-slate-800 text-center flex flex-col items-center">
                    <div class="w-36 h-36 mb-4">
                        <svg viewBox="0 0 100 100" class="w-full h-full">
                            <!-- Uzun Boyun -->
                            <rect x="42" y="45" width="16" height="40" rx="8" fill="#f8fafc"/>
                            <!-- Kafa -->
                            <ellipse cx="50" cy="38" rx="18" ry="14" fill="#f8fafc"/>
                            <!-- Kulaklar -->
                            <polygon points="38,28 42,12 46,28" fill="#cbd5e1"/>
                            <polygon points="54,28 58,12 62,28" fill="#cbd5e1"/>
                            <!-- Gözler & Havalı Gözlük -->
                            <circle cx="43" cy="36" r="3" fill="#000"/>
                            <circle cx="57" cy="36" r="3" fill="#000"/>
                            <!-- Ağız Geometrisi -->
                            <ellipse cx="50" cy="44" rx="8" ry="5" fill="#f1f5f9"/>
                            <line x1="50" y1="42" x2="50" y2="45" stroke="#94a3b8" stroke-width="2"/>
                            <!-- Etnik Boyunluk -->
                            <rect x="42" y="60" width="16" height="5" fill="#dc2626"/>
                            <rect x="42" y="65" width="16" height="5" fill="#f59e0b"/>
                        </svg>
                    </div>
                    <h3 class="text-xl font-bold text-white">Louie (Lama)</h3>
                    <p class="text-xs text-amber-400 font-semibold mb-2">Queen'i Dağıtan Tehdit</p>
                    <p class="text-xs text-slate-400 leading-normal">
                        Freddie Mercury ile MJ düet yaparken Michael laması Louie'yi stüdyoya soktu. Freddie, "Bir lamayla aynı mikrofona şarkı söyleyemem" diyerek kaydı terk etti!
                    </p>
                </div>

                <!-- 3. Crusher (Dev Boa Yılanı) -->
                <div class="bg-slate-950 p-6 rounded-2xl border border-slate-800 text-center flex flex-col items-center">
                    <div class="w-36 h-36 mb-4">
                        <svg viewBox="0 0 100 100" class="w-full h-full">
                            <!-- Kıvrımlı Yılan Gövdesi -->
                            <path d="M 25 75 Q 35 45 50 65 T 75 45 Q 85 55 75 75" fill="none" stroke="#22c55e" stroke-width="14" stroke-linecap="round"/>
                            <!-- Yılan Kafası -->
                            <circle cx="28" cy="42" r="14" fill="#16a34a"/>
                            <circle cx="24" cy="38" r="3" fill="#fef08a"/>
                            <circle cx="24" cy="38" r="1.5" fill="#000"/>
                            <!-- Çatallı Dil -->
                            <path d="M 16 44 L 8 46 M 8 46 L 4 42 M 8 46 L 4 50" stroke="#ef4444" stroke-width="2" fill="none"/>
                            <!-- MJ Şapkası Minyatür -->
                            <polygon points="20,32 36,32 33,22 23,22" fill="#09090b"/>
                        </svg>
                    </div>
                    <h3 class="text-xl font-bold text-white">Crusher (Boa Yılanı)</h3>
                    <p class="text-xs text-amber-400 font-semibold mb-2">Misafir Kaçıran</p>
                    <p class="text-xs text-slate-400 leading-normal">
                        Michael'ın stüdyo kayıtlarında omuzlarına doladığı, röportaja gelen gazetecilerin panikle odadan fırlamasına sebep olan devasa tatlı boa yılanı.
                    </p>
                </div>
            </div>

            <!-- Fun Facts Şeridi -->
            <div class="bg-gradient-to-r from-amber-500/10 via-red-500/10 to-transparent p-6 rounded-2xl border border-slate-800">
                <h4 class="text-white font-bold mb-4 flex items-center gap-2">
                    <span>⚡ Biliyor muydunuz? (Akıl Almaz MJ Gerçekleri)</span>
                </h4>
                <div class="grid md:grid-cols-3 gap-4 text-xs text-slate-300">
                    <div class="bg-slate-900/80 p-3 rounded-lg border border-slate-800">
                        <strong>👟 Patentli Ayakkabı:</strong> Sahnedeki 45 derecelik eğilme hilesi için zemine kenetlenen özel kancalı ayakkabıların bizzat mucidiydi (US Patent #5,255,452).
                    </div>
                    <div class="bg-slate-900/80 p-3 rounded-lg border border-slate-800">
                        <strong>🎮 Sonic the Hedgehog:</strong> Sega'nın efsanevi Sonic 3 oyununun müziklerini gizlice bestelemiş, fakat ses kalitesini beğenmediği için jeneriğe adını yazdırmamıştı.
                    </div>
                    <div class="bg-slate-900/80 p-3 rounded-lg border border-slate-800">
                        <strong>🎈 Su Balonu Terörü:</strong> Neverland'e gelen ünlü misafirleri (Elizabeth Taylor dahil) pusuya düşürüp devasa su balonu savaşları düzenlemeye bayılırdı.
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- BÖLÜM 5: MERCH / PELUŞ MAĞAZASI (DEMO - GERÇEK PARA GEÇMEZ) -->
    <section id="magaza" class="py-20 bg-slate-950 border-t border-slate-800">
        <div class="max-w-6xl mx-auto px-4">
            <div class="flex flex-col md:flex-row md:items-end justify-between mb-12">
                <div>
                    <span class="text-amber-400 font-bold uppercase tracking-wider text-xs">Neverland Demo Koleksiyonu</span>
                    <h2 class="text-3xl md:text-5xl font-black text-white mt-1">Evcil Hayvan Peluş Merch Pazarı</h2>
                    <p class="text-slate-400 text-xs mt-1">Uyarı: Bu dükkan demo amaçlıdır. Kredi kartınızı rahat bırakın, sadece hayal gücünüzü harcıyoruz!</p>
                </div>
                <div class="mt-4 md:mt-0 bg-slate-900 px-4 py-2 rounded-xl border border-slate-800 text-xs text-amber-400 font-mono">
                    Kargo: Moonwalk Express (3 saniye)
                </div>
            </div>

            <!-- Ürün Kartları -->
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Ürün 1 -->
                <div class="bg-slate-900 border border-slate-800 rounded-2xl overflow-hidden hover:border-amber-400/50 transition group flex flex-col justify-between p-6">
                    <div>
                        <div class="bg-slate-950 rounded-xl p-6 flex justify-center items-center h-48 mb-6 group-hover:scale-105 transition">
                            <!-- Peluş Bubbles İllüstrasyonu -->
                            <svg viewBox="0 0 100 100" class="w-32 h-32">
                                <circle cx="50" cy="50" r="38" fill="#d97706" stroke="#b45309" stroke-width="3"/>
                                <circle cx="50" cy="56" r="22" fill="#fef08a"/>
                                <circle cx="42" cy="48" r="5" fill="#000"/>
                                <circle cx="58" cy="48" r="5" fill="#000"/>
                                <circle cx="43" cy="46" r="1.5" fill="#fff"/>
                                <circle cx="59" cy="46" r="1.5" fill="#fff"/>
                                <path d="M 44 62 Q 50 68 56 62" stroke="#b45309" stroke-width="2.5" fill="none" stroke-linecap="round"/>
                                <rect x="35" y="80" width="30" height="15" rx="4" fill="#020617"/>
                                <polygon points="45,86 55,86 50,81" fill="#dc2626"/>
                            </svg>
                        </div>
                        <div class="flex justify-between items-start mb-2">
                            <h3 class="text-lg font-bold text-white">Smokinli Peluş Bubbles</h3>
                            <span class="text-amber-400 font-mono font-bold">$49.99</span>
                        </div>
                        <p class="text-xs text-slate-400 mb-6">
                            Özel dikim smokini ve elinde porselen çay fincanıyla gelen %100 sarılmalık şempanze peluşu. Moonwalk yapamaz ama dert dinler.
                        </p>
                    </div>
                    <button onclick="addToCart('Smokinli Peluş Bubbles')" class="w-full bg-amber-500 hover:bg-amber-400 text-slate-950 font-bold py-2.5 rounded-xl text-xs transition duration-150">
                        Demo Sepete Ekle
                    </button>
                </div>

                <!-- Ürün 2 -->
                <div class="bg-slate-900 border border-slate-800 rounded-2xl overflow-hidden hover:border-amber-400/50 transition group flex flex-col justify-between p-6">
                    <div>
                        <div class="bg-slate-950 rounded-xl p-6 flex justify-center items-center h-48 mb-6 group-hover:scale-105 transition">
                            <!-- Peluş Louie İllüstrasyonu -->
                            <svg viewBox="0 0 100 100" class="w-32 h-32">
                                <rect x="42" y="30" width="16" height="50" rx="8" fill="#f1f5f9" stroke="#cbd5e1" stroke-width="3"/>
                                <ellipse cx="50" cy="30" rx="20" ry="15" fill="#f8fafc"/>
                                <polygon points="36,18 42,4 46,20" fill="#e2e8f0"/>
                                <polygon points="54,20 58,4 64,18" fill="#e2e8f0"/>
                                <!-- Güneş Gözlüğü -->
                                <rect x="36" y="24" width="12" height="8" rx="2" fill="#0f172a"/>
                                <rect x="52" y="24" width="12" height="8" rx="2" fill="#0f172a"/>
                                <line x1="48" y1="28" x2="52" y2="28" stroke="#0f172a" stroke-width="2"/>
                                <ellipse cx="50" cy="37" rx="6" ry="4" fill="#fee2e2"/>
                            </svg>
                        </div>
                        <div class="flex justify-between items-start mb-2">
                            <h3 class="text-lg font-bold text-white">Stüdyo Kaçkını Peluş Lama</h3>
                            <span class="text-amber-400 font-mono font-bold">$39.99</span>
                        </div>
                        <p class="text-xs text-slate-400 mb-6">
                            Freddie Mercury'nin stüdyoyu terk etmesine yol açan o asil duruş! Üzerinde mini güneş gözlüğüyle birlikte teslim edilir.
                        </p>
                    </div>
                    <button onclick="addToCart('Stüdyo Kaçkını Peluş Lama')" class="w-full bg-amber-500 hover:bg-amber-400 text-slate-950 font-bold py-2.5 rounded-xl text-xs transition duration-150">
                        Demo Sepete Ekle
                    </button>
                </div>

                <!-- Ürün 3 -->
                <div class="bg-slate-900 border border-slate-800 rounded-2xl overflow-hidden hover:border-amber-400/50 transition group flex flex-col justify-between p-6">
                    <div>
                        <div class="bg-slate-950 rounded-xl p-6 flex justify-center items-center h-48 mb-6 group-hover:scale-105 transition">
                            <!-- Peluş Crusher İllüstrasyonu -->
                            <svg viewBox="0 0 100 100" class="w-32 h-32">
                                <circle cx="50" cy="50" r="34" fill="none" stroke="#4ade80" stroke-width="14" stroke-dasharray="160 50"/>
                                <circle cx="35" cy="40" r="14" fill="#22c55e"/>
                                <circle cx="30" cy="36" r="3" fill="#fff"/>
                                <circle cx="30" cy="36" r="1.5" fill="#000"/>
                                <polygon points="26,24 44,24 40,16 30,16" fill="#0f172a"/>
                                <path d="M 22 42 L 14 44" stroke="#ef4444" stroke-width="2"/>
                            </svg>
                        </div>
                        <div class="flex justify-between items-start mb-2">
                            <h3 class="text-lg font-bold text-white">Fedoraplı Peluş Boa Crusher</h3>
                            <span class="text-amber-400 font-mono font-bold">$29.99</span>
                        </div>
                        <p class="text-xs text-slate-400 mb-6">
                            Boynunuza sarıp şarkı söyleyebileceğiniz 1.5 metre boyunda yumuşacık peluş yılan. Kafasında minyatür fedora şapkası hediyeli!
                        </p>
                    </div>
                    <button onclick="addToCart('Fedoraplı Peluş Boa Crusher')" class="w-full bg-amber-500 hover:bg-amber-400 text-slate-950 font-bold py-2.5 rounded-xl text-xs transition duration-150">
                        Demo Sepete Ekle
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- BİLDİRİM TOAST KUTUSU -->
    <div id="toast" class="fixed bottom-6 right-6 bg-amber-400 text-slate-950 px-5 py-3 rounded-xl font-bold text-xs shadow-2xl flex items-center gap-3 transform translate-y-32 transition duration-300 z-50">
        <span id="toast-icon">✨</span>
        <span id="toast-msg">Ürün sepete eklendi!</span>
    </div>

    <!-- FOOTER -->
    <footer class="bg-slate-950 border-t border-slate-900 py-8 text-center text-xs text-slate-500">
        <p>Yapay Zeka Araçları Kullanımı Dersi için Bilgilendirme ve Demo Portalı olarak geliştirilmiştir.</p>
        <p class="mt-1">Tüm bilgiler Wikipedia kaynaklıdır. Görseller telif içermeyen özgün SVG vektörleridir. 🎩✨</p>
    </footer>

    <!-- ETKİLEŞİM VE SEPET SCRIPTI -->
    <script>
        let cart = 0;
        const cartCountEl = document.getElementById('cart-count');
        const toast = document.getElementById('toast');
        const toastMsg = document.getElementById('toast-msg');

        function addToCart(productName) {
            cart++;
            cartCountEl.innerText = cart;
            cartCountEl.classList.add('scale-125', 'bg-amber-400', 'text-slate-950');
            setTimeout(() => {
                cartCountEl.classList.remove('scale-125', 'bg-amber-400', 'text-slate-950');
            }, 200);

            // Bildirim göster
            toastMsg.innerText = `Hee-Hee! ${productName} sanal sepete eklendi!`;
            toast.classList.remove('translate-y-32');
            
            setTimeout(() => {
                toast.classList.add('translate-y-32');
            }, 3000);
        }
    </script>
</body>
</html>
