<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Website Alqudwah - Tahap Pengembangan</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome Icons -->
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <!-- Google Fonts Inter -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800;900&display=swap" rel="stylesheet">
    <!-- Tag untuk memunculkan logo favicon -->
    <link rel="icon" type="image/png" href="logo.png">

    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    },
                    colors: {
                        'brand-orange': '#f3a953',
                        'brand-dark': '#3c2a2a',
                        'brand-light': '#fbeed9',
                        'brand-tan': '#d1b199',
                    },
                    animation: {
                        blob: "blob 7s infinite",
                        'fade-in': "fadeIn 0.5s ease-out forwards",
                        'fade-out': "fadeOut 0.5s ease-in forwards",
                        'pop-in': "popIn 0.5s cubic-bezier(0.16, 1, 0.3, 1) forwards",
                        'pop-out': "popOut 0.4s ease-in forwards",
                    },
                    keyframes: {
                        blob: {
                            "0%": { transform: "translate(0px, 0px) scale(1)" },
                            "33%": { transform: "translate(30px, -50px) scale(1.1)" },
                            "66%": { transform: "translate(-20px, 20px) scale(0.9)" },
                            "100%": { transform: "translate(0px, 0px) scale(1)" },
                        },
                        /* Keyframes Animasi Masuk (Entry) */
                        fadeIn: {
                            '0%': { opacity: '0' },
                            '100%': { opacity: '1' }
                        },
                        popIn: {
                            '0%': { opacity: '0', transform: 'scale(0.9) translateY(15px)' },
                            '100%': { opacity: '1', transform: 'scale(1) translateY(0)' }
                        },
                        /* Keyframes Animasi Keluar (Exit) */
                        fadeOut: {
                            '0%': { opacity: '1' },
                            '100%': { opacity: '0' }
                        },
                        popOut: {
                            '0%': { opacity: '1', transform: 'scale(1) translateY(0)' },
                            '100%': { opacity: '0', transform: 'scale(0.95) translateY(10px)' }
                        }
                    }
                }
            }
        }
    </script>
    <style>
        .animation-delay-2000 { animation-delay: 2s; }
        .animation-delay-4000 { animation-delay: 4s; }
    </style>
</head>
<body class="bg-gray-100 min-h-screen font-sans">

    <!-- Overlay Pembangunan Alqudwah -->
    <div id="alqudwah-construction-overlay" class="fixed inset-0 z-[100] flex items-center justify-center bg-white/70 backdrop-blur-md overflow-hidden animate-fade-in">
        
        <!-- Animasi Background Blobs -->
        <div class="absolute inset-0 w-full h-full pointer-events-none overflow-hidden z-0">
            <div class="absolute top-[5%] left-[5%] w-[450px] h-[450px] bg-brand-orange/30 rounded-full mix-blend-multiply filter blur-3xl animate-blob"></div>
            <div class="absolute top-[20%] left-[25%] w-[400px] h-[400px] bg-brand-tan/40 rounded-full mix-blend-multiply filter blur-3xl animate-blob animation-delay-2000"></div>
            <div class="absolute bottom-[5%] left-[10%] w-[500px] h-[500px] bg-orange-300/30 rounded-full mix-blend-multiply filter blur-3xl animate-blob animation-delay-4000"></div>
        </div>

        <!-- Main Card Popup (Diberi ID 'alqudwah-card' agar bisa diberi animasi keluar secara terpisah) -->
        <div id="alqudwah-card" class="bg-white/90 backdrop-blur-xl rounded-[2.5rem] p-8 md:p-10 shadow-[0_20px_50px_rgba(0,0,0,0.08)] max-w-md w-[90%] mx-auto text-center relative z-10 border border-white animate-pop-in">
            
            <!-- Ikon Pembangunan -->
            <div class="w-[70px] h-[70px] mx-auto rounded-full bg-brand-light flex items-center justify-center mb-6 text-brand-orange text-2xl shadow-sm">
                                    <img 
  src="logo.png" 
  alt="Pemandangan gunung saat matahari terbit" 
  width="70" 
  loading="lazy" 
  title="Gunung Bromo"
></i>
</i>
            </div>
            
            <!-- Badge Update -->
            <div class="inline-flex items-center gap-2 bg-orange-100/80 text-brand-orange text-[10px] font-extrabold px-3 py-1 rounded-full mb-4 w-max mx-auto">
                <span class="relative flex h-2 w-2">
                    <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-brand-orange opacity-75"></span>
                    <span class="relative inline-flex rounded-full h-2 w-2 bg-brand-orange"></span>
                </span>
                Tahap Pengembangan
            </div>

            <!-- Judul -->
            <h2 class="text-2xl md:text-[26px] font-black text-black mb-3 tracking-tight leading-tight">
                Website <span class="text-brand-orange">Alqudwah</span><br>Sedang Dibangun
            </h2>

            <!-- Penjelasan -->
            <p class="text-black font-medium text-[13px] md:text-[14.5px] mb-8 leading-[1.6] opacity-80">
                Kami sedang merangkai dan menyempurnakan inovasi digital ini. Beberapa fitur mungkin belum maksimal, namun Anda tetap dapat menjelajahi halaman yang tersedia.
            </p>

            <!-- Tombol Masuk -->
            <button onclick="closeAlqudwahOverlay()" class="w-full bg-brand-orange text-white px-7 py-3.5 rounded-full text-sm font-bold hover:bg-orange-500 hover:-translate-y-0.5 transition-all duration-300 shadow-[0_5px_15px_rgba(243,169,83,0.3)] flex items-center justify-center gap-2 group">
                Masuk ke Website
                <i class="fa-solid fa-arrow-right transform group-hover:translate-x-1 transition-transform"></i>
            </button>
        </div>
    </div>

<!-- Script Penutup Overlay Beranimasi & Perpindahan Halaman -->
    <script>
        function closeAlqudwahOverlay() {
            const overlay = document.getElementById('alqudwah-construction-overlay');
            const card = document.getElementById('alqudwah-card');
            
            // Ganti animasi masuk dengan animasi keluar
            overlay.classList.remove('animate-fade-in');
            overlay.classList.add('animate-fade-out');
            
            if (card) {
                card.classList.remove('animate-pop-in');
                card.classList.add('animate-pop-out');
            }
            
            // Tunggu durasi animasi keluar (500ms) sebelum berpindah ke index.html
            setTimeout(() => {
                window.location.href = 'home.html';
            }, 500);
        }
    </script></body>
</html>
