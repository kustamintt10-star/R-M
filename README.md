```html
<!DOCTYPE html>
<html lang="id" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Undangan Pernikahan Rudi Hartono Sihotang, S.Pd & Masri Br. Simarmata, S.Pd</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts: Cormorant Garamond & Plus Jakarta Sans -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,600;0,700;1,400&family=Plus+Jakarta+Sans:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- AOS Animation Library -->
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        gold: {
                            50: '#fbf8ef',
                            100: '#f5ecd5',
                            200: '#ebd8aa',
                            300: '#dfbe75',
                            400: '#d4a34b',
                            500: '#c59239',
                            600: '#aa7728',
                            700: '#885b20',
                            800: '#6f491e',
                            900: '#5c3d1b',
                        },
                        forest: {
                            800: '#1b3b2b',
                            900: '#12261b'
                        }
                    },
                    fontFamily: {
                        serif: ['"Cormorant Garamond"', 'serif'],
                        sans: ['"Plus Jakarta Sans"', 'sans-serif'],
                    }
                }
            }
        }
    </script>
    <style>
        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            background-color: #faf9f6;
            color: #2c3e35;
            overflow-x: hidden;
        }
        .font-serif {
            font-family: 'Cormorant Garamond', serif;
        }
        .gold-gradient-text {
            background: linear-gradient(135deg, #d4a34b 0%, #aa7728 50%, #f5ecd5 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        .gold-border {
            border-color: #dfbe75;
        }
        /* Custom scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #f1f1f1;
        }
        ::-webkit-scrollbar-thumb {
            background: #d4a34b;
            border-radius: 4px;
        }
    </style>
</head>
<body class="relative selection:bg-gold-200 selection:text-gold-900">

    <!-- AUDIO LATAR (Batak Song) -->
    <audio id="bgMusic" loop>
        <!-- Menggunakan data audio dari file terlampir -->
        <source src="data:audio/mp3;base64,//uQxAAAAAAAAAAAAAAAWGluZm8AAAAZAAAAEAAACb4AEhISEhISEhISEhISEhISEhISEhISEhISEhISEhISEhISEhISEhISEhISEhISEhISEhISEhJSUlJSUlJSUlJSUlJSUlJSUlJSUlJSUlJSUlJSUlJSUlJSUlJSUlJUgAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAD//wAAAP//v7+v7+/v7+/v7+/v7+/v7+/v7+/v7+/v7+/v7+/v7+/v7+/v7+/v7+/v7+/v7+/v7+/v7+/v7+/v7+/v7+/v7+/v7+/v7+/v7+/" type="audio/mp3">
        Your browser does not support the audio element.
    </audio>

    <!-- FLOATING MUSIC PLAYER BUTTON -->
    <div id="musicControl" class="fixed bottom-6 right-6 z-55 hidden animate-bounce">
        <button onclick="toggleMusic()" class="w-12 h-12 bg-gold-600 text-white rounded-full shadow-2xl flex items-center justify-center border-2 border-white hover:bg-gold-700 transition duration-300 focus:outline-none">
            <i id="musicIcon" class="fa-solid fa-music text-lg"></i>
        </button>
    </div>

    <!-- 1. COVER / HALAMAN UTAMA (WELCOME SCREEN) -->
    <section id="coverSection" class="fixed inset-0 z-50 flex items-center justify-center bg-forest-900 text-white px-4 transition-transform duration-1000 ease-in-out">
        <!-- Background Overlay with Image -->
        <div class="absolute inset-0 opacity-30 bg-cover bg-center" style="background-image: url('1000171494.jpg');"></div>
        <div class="absolute inset-0 bg-gradient-to-t from-forest-900 via-forest-900/80 to-black/40"></div>

        <div class="relative z-10 text-center max-w-lg mx-auto py-10" data-aos="zoom-in" data-aos-duration="1200">
            <span class="text-xs uppercase tracking-[0.3em] text-gold-300 font-semibold mb-3 block">Undangan Pernikahan Suci</span>
            <span class="inline-block px-4 py-1 mb-4 text-xs tracking-widest bg-gold-600/30 border border-gold-400/50 rounded-full text-gold-200">
                <i class="fa-solid fa-hands-praying mr-2"></i> Adat Batak Elegance
            </span>
            <h1 class="font-serif text-4xl sm:text-6xl font-bold mb-4 gold-gradient-text tracking-wide">
                Rudi & Masri
            </h1>
            <p class="text-sm sm:text-base text-gray-300 mb-6 font-light">
                Kepada Yth. Bapak/Ibu/Saudara/i,<br>
                <span id="guestName" class="font-semibold text-white text-lg block mt-1">Tamu Undangan</span>
            </p>
            
            <div class="bg-white/10 backdrop-blur-md p-4 rounded-2xl border border-white/10 mb-8 max-w-xs mx-auto">
                <p class="text-xs text-gray-300 mb-1">Hari & Tanggal</p>
                <p class="font-serif text-lg text-gold-200 font-semibold">Sabtu, 14 November 2026</p>
            </div>

            <button onclick="openInvitation()" class="group relative inline-flex items-center gap-3 px-8 py-4 bg-gradient-to-r from-gold-500 to-gold-600 text-white font-medium rounded-full shadow-xl hover:from-gold-600 hover:to-gold-700 transition-all duration-300 transform hover:-translate-y-1">
                <i class="fa-solid fa-envelope-open-text text-lg animate-pulse"></i>
                <span class="tracking-wider uppercase text-sm font-semibold">Buka Undangan</span>
            </button>
        </div>
    </section>

    <!-- MAIN CONTENT WRAPPER (Hidden until opened) -->
    <div id="mainContent" class="opacity-0 transition-opacity duration-1000">

        <!-- HERO SECTION -->
        <header class="relative min-h-screen flex items-center justify-center text-center px-4 py-20 bg-forest-900 text-white overflow-hidden">
            <div class="absolute inset-0 opacity-25 bg-cover bg-center transform scale-105 animate-pulse" style="background-image: url('1000171493.jpg');"></div>
            <div class="absolute inset-0 bg-gradient-to-b from-forest-900/90 via-forest-900/60 to-forest-900"></div>

            <div class="relative z-10 max-w-3xl mx-auto" data-aos="fade-up" data-aos-duration="1000">
                <span class="text-xs uppercase tracking-[0.4em] text-gold-300 block mb-4 font-semibold">The Wedding Of</span>
                <h1 class="font-serif text-5xl sm:text-7xl lg:text-8xl font-bold mb-6 gold-gradient-text">
                    Rudi & Masri
                </h1>
                <p class="font-serif italic text-xl sm:text-2xl text-gold-200 mb-8">
                    "Dan keduanya menjadi satu daging. Demikianlah mereka bukan lagi dua, melainkan satu."
                </p>
                <span class="inline-block px-6 py-2 rounded-full border border-gold-400 text-gold-300 text-sm tracking-widest uppercase bg-black/30">
                    14 . 11 . 2026
                </span>
            </div>
            
            <!-- Scroll Down Indicator -->
            <div class="absolute bottom-6 left-1/2 transform -translate-x-1/2 text-gold-300 animate-bounce">
                <i class="fa-solid fa-chevron-down text-xl"></i>
            </div>
        </header>

        <!-- KUTIPAN AYAT SUCI -->
        <section class="py-20 px-4 bg-stone-100 text-center relative">
            <div class="max-w-2xl mx-auto" data-aos="fade-up">
                <i class="fa-solid fa-quote-left text-4xl text-gold-500 mb-6 block"></i>
                <h2 class="font-serif text-2xl sm:text-3xl text-forest-900 font-semibold mb-4 leading-relaxed">
                    "Demikianlah mereka bukan lagi dua, melainkan satu. Karena itu, apa yang telah dipersatukan Allah, tidak boleh diceraikan manusia."
                </h2>
                <p class="text-gold-700 font-bold uppercase tracking-widest text-sm">— Markus 10:8 —</p>
            </div>
        </section>

        <!-- MEMPELAI / GROOM & BRIDE -->
        <section class="py-24 px-4 bg-white">
            <div class="max-w-5xl mx-auto text-center mb-16" data-aos="fade-up">
                <span class="text-gold-600 font-semibold uppercase tracking-widest text-xs block mb-2">Pasangan Kekasih</span>
                <h2 class="font-serif text-4xl sm:text-5xl font-bold text-forest-900 mb-4">Mempelai Bahagia</h2>
                <p class="text-gray-600 max-w-lg mx-auto text-sm">Dengan memohon rahmat dan kasih karunia Tuhan, kami bermaksud mengundang Bapak/Ibu sekalian dalam pernikahan kami.</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-12 max-w-4xl mx-auto items-center">
                <!-- Groom -->
                <div class="text-center bg-stone-50 p-8 rounded-3xl border border-stone-200 shadow-lg transform hover:-translate-y-2 transition duration-500" data-aos="fade-right">
                    <div class="w-48 h-48 mx-auto mb-6 rounded-full overflow-hidden shadow-xl border-4 border-gold-300">
                        <img src="1000171495.jpg" alt="Rudi Hartono Sihotang" class="w-full h-full object-cover">
                    </div>
                    <h3 class="font-serif text-3xl font-bold text-forest-900 mb-2">Rudi Hartono Sihotang, S.Pd</h3>
                    <p class="text-xs uppercase tracking-widest text-gold-600 font-semibold mb-4">Putra Tercinta</p>
                    <p class="text-sm text-gray-600 leading-relaxed">
                        Anak dari:<br>
                        <span class="font-semibold text-forest-900">Mendiang A. Sihotang</span> & <span class="font-semibold text-forest-900">Rosdiana Sijabat</span>
                    </p>
                </div>

                <!-- Bride -->
                <div class="text-center bg-stone-50 p-8 rounded-3xl border border-stone-200 shadow-lg transform hover:-translate-y-2 transition duration-500" data-aos="fade-left">
                    <div class="w-48 h-48 mx-auto mb-6 rounded-full overflow-hidden shadow-xl border-4 border-gold-300">
                        <img src="1000171496.jpg" alt="Masri Br. Simarmata" class="w-full h-full object-cover">
                    </div>
                    <h3 class="font-serif text-3xl font-bold text-forest-900 mb-2">Masri Br. Simarmata, S.Pd</h3>
                    <p class="text-xs uppercase tracking-widest text-gold-600 font-semibold mb-4">Putri Tercinta</p>
                    <p class="text-sm text-gray-600 leading-relaxed">
                        Anak dari:<br>
                        <span class="font-semibold text-forest-900">Pdt. Dr. Drs. A. Simarmata, S.Th.MIP</span> & <span class="font-semibold text-forest-900">Mendiang M. Br Matondang, Spd</span>
                    </p>
                </div>
            </div>
        </section>

        <!-- KISAH CINTA / LOVE STORY -->
        <section class="py-24 px-4 bg-forest-900 text-white relative overflow-hidden">
            <div class="absolute inset-0 opacity-10 bg-cover bg-center" style="background-image: url('1000171490.jpg');"></div>
            <div class="max-w-3xl mx-auto relative z-10 text-center" data-aos="zoom-in">
                <span class="text-gold-300 font-semibold uppercase tracking-widest text-xs block mb-3">Perjalanan Cinta Kami</span>
                <h2 class="font-serif text-4xl sm:text-5xl font-bold mb-8 gold-gradient-text">Kisah Kasih & Takdir</h2>
                
                <div class="bg-white/10 backdrop-blur-md p-8 sm:p-12 rounded-3xl border border-white/15 shadow-2xl">
                    <i class="fa-solid fa-church text-3xl text-gold-400 mb-6"></i>
                    <p class="font-serif text-lg sm:text-xl leading-relaxed italic text-gray-200">
                        "Satu tempat ibadah dari kecil sampai sekarang, sekian lama mencari ternyata di mana mereka berdoa waktu dan tempat yang sama hingga hati mereka disatukan oleh kehendak Tuhan."
                    </p>
                    <div class="mt-8 inline-flex items-center gap-3 text-gold-300 text-sm font-semibold tracking-wider">
                        <span>Rudi</span>
                        <i class="fa-solid fa-heart text-gold-500"></i>
                        <span>Masri</span>
                    </div>
                </div>
            </div>
        </section>

        <!-- ACARA / EVENT DETAILS -->
        <section class="py-24 px-4 bg-stone-50">
            <div class="max-w-5xl mx-auto text-center mb-16" data-aos="fade-up">
                <span class="text-gold-600 font-semibold uppercase tracking-widest text-xs block mb-2">Rangkaian Acara</span>
                <h2 class="font-serif text-4xl sm:text-5xl font-bold text-forest-900 mb-4">Waktu & Tempat</h2>
                <p class="text-gray-600 max-w-lg mx-auto text-sm">Merupakan suatu kehormatan dan kebahagiaan bagi kami apabila Bapak/Ibu/Saudara/i berkenan hadir memberikan doa restu.</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-8 max-w-4xl mx-auto">
                <!-- Pemberkatan -->
                <div class="bg-white p-8 rounded-3xl shadow-xl border border-stone-200 text-center flex flex-col justify-between transform hover:scale-105 transition duration-300" data-aos="fade-up">
                    <div>
                        <div class="w-16 h-16 mx-auto mb-6 bg-gold-100 text-gold-600 rounded-full flex items-center justify-center text-2xl shadow-inner">
                            <i class="fa-solid fa-ring"></i>
                        </div>
                        <h3 class="font-serif text-2xl font-bold text-forest-900 mb-2">Pemberkatan / Janji Suci</h3>
                        <p class="text-gold-600 font-semibold text-sm mb-4">Sabtu, 14 November 2026</p>
                        <p class="text-gray-600 text-sm mb-6 leading-relaxed">
                            <strong class="text-forest-900 block mb-1">GPI Sidang Lubuk Pakam</strong>
                            Jln. P. Siantar No. 8<br>
                            Pukul 10.00 WIB - Selesai
                        </p>
                    </div>
                    <a href="https://maps.google.com/?q=GPI+Sidang+Lubuk+Pakam+Jln+P+Siantar+No+8" target="_blank" class="inline-flex items-center justify-center gap-2 px-6 py-3 bg-forest-900 text-white text-xs font-semibold uppercase tracking-wider rounded-xl hover:bg-forest-800 transition shadow-md">
                        <i class="fa-solid fa-map-location-dot"></i> Buka Google Maps
                    </a>
                </div>

                <!-- Resepsi -->
                <div class="bg-white p-8 rounded-3xl shadow-xl border border-stone-200 text-center flex flex-col justify-between transform hover:scale-105 transition duration-300" data-aos="fade-up" data-aos-delay="200">
                    <div>
                        <div class="w-16 h-16 mx-auto mb-6 bg-gold-100 text-gold-600 rounded-full flex items-center justify-center text-2xl shadow-inner">
                            <i class="fa-solid fa-glass-cheers"></i>
                        </div>
                        <h3 class="font-serif text-2xl font-bold text-forest-900 mb-2">Resepsi Adat Batak</h3>
                        <p class="text-gold-600 font-semibold text-sm mb-4">Sabtu, 14 November 2026</p>
                        <p class="text-gray-600 text-sm mb-6 leading-relaxed">
                            <strong class="text-forest-900 block mb-1">Wisma Tiberias</strong>
                            Jalan P. Siantar No. 34, Lubuk Pakam<br>
                            Selepas Pemberkatan
                        </p>
                    </div>
                    <a href="https://maps.google.com/?q=Wisma+Tiberias+Jalan+P+Siantar+No+34+Lubuk+Pakam" target="_blank" class="inline-flex items-center justify-center gap-2 px-6 py-3 bg-forest-900 text-white text-xs font-semibold uppercase tracking-wider rounded-xl hover:bg-forest-800 transition shadow-md">
                        <i class="fa-solid fa-map-location-dot"></i> Buka Google Maps
                    </a>
                </div>
            </div>
        </section>

        <!-- COUNTDOWN TIMER -->
        <section class="py-16 px-4 bg-gradient-to-r from-forest-900 to-forest-800 text-white text-center">
            <div class="max-w-3xl mx-auto" data-aos="fade-up">
                <span class="text-gold-300 font-semibold uppercase tracking-widest text-xs block mb-2">Menuju Hari Bahagia</span>
                <h2 class="font-serif text-3xl sm:text-4xl font-bold mb-8">Hitung Mundur Acara</h2>
                
                <div class="grid grid-cols-4 gap-3 sm:gap-6 max-w-lg mx-auto">
                    <div class="bg-white/10 backdrop-blur-md p-4 rounded-2xl border border-white/10">
                        <span id="days" class="font-serif text-3xl sm:text-4xl font-bold text-gold-300 block">00</span>
                        <span class="text-xs uppercase tracking-wider text-gray-300">Hari</span>
                    </div>
                    <div class="bg-white/10 backdrop-blur-md p-4 rounded-2xl border border-white/10">
                        <span id="hours" class="font-serif text-3xl sm:text-4xl font-bold text-gold-300 block">00</span>
                        <span class="text-xs uppercase tracking-wider text-gray-300">Jam</span>
                    </div>
                    <div class="bg-white/10 backdrop-blur-md p-4 rounded-2xl border border-white/10">
                        <span id="minutes" class="font-serif text-3xl sm:text-4xl font-bold text-gold-300 block">00</span>
                        <span class="text-xs uppercase tracking-wider text-gray-300">Menit</span>
                    </div>
                    <div class="bg-white/10 backdrop-blur-md p-4 rounded-2xl border border-white/10">
                        <span id="seconds" class="font-serif text-3xl sm:text-4xl font-bold text-gold-300 block">00</span>
                        <span class="text-xs uppercase tracking-wider text-gray-300">Detik</span>
                    </div>
                </div>
            </div>
        </section>

        <!-- GALERI FOTO PREWEDDING -->
        <section class="py-24 px-4 bg-white">
            <div class="max-w-5xl mx-auto text-center mb-16" data-aos="fade-up">
                <span class="text-gold-600 font-semibold uppercase tracking-widest text-xs block mb-2">Momen Kebersamaan</span>
                <h2 class="font-serif text-4xl sm:text-5xl font-bold text-forest-900 mb-4">Galeri Foto Prewedding</h2>
                <p class="text-gray-600 max-w-lg mx-auto text-sm">Setiap detik bersama adalah anugerah terindah yang dipersiapkan oleh Sang Pencipta.</p>
            </div>

            <div class="grid grid-cols-2 md:grid-cols-4 gap-4 max-w-6xl mx-auto">
                <div class="overflow-hidden rounded-2xl shadow-md group h-72 sm:h-80 cursor-pointer" data-aos="fade-up" onclick="openLightbox('1000171494.jpg')">
                    <img src="1000171494.jpg" alt="Prewedding 1" class="w-full h-full object-cover group-hover:scale-110 transition duration-500">
                </div>
                <div class="overflow-hidden rounded-2xl shadow-md group h-72 sm:h-80 cursor-pointer" data-aos="fade-up" data-aos-delay="100" onclick="openLightbox('1000171493.jpg')">
                    <img s
