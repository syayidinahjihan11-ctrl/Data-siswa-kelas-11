<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Data Siswa Kelas 11</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body {
            box-sizing: border-box;
        }
        .gradient-bg {
            background: linear-gradient(-45deg, #fef7ff, #f0f9ff, #f0fdf4, #fffbeb, #fef2f2, #f3e8ff, #ecfdf5, #fef3c7, #ddd6fe, #fce7f3, #e0f2fe, #f0fdfa);
            background-size: 600% 600%;
            animation: gradientShift 10s ease infinite;
        }
        @keyframes gradientShift {
            0% { background-position: 0% 50%; }
            25% { background-position: 100% 0%; }
            50% { background-position: 100% 100%; }
            75% { background-position: 0% 100%; }
            100% { background-position: 0% 50%; }
        }
        .card-shadow {
            box-shadow: 0 25px 50px rgba(255,0,128,0.3), 0 15px 35px rgba(0,255,128,0.2), 0 5px 15px rgba(128,0,255,0.4);
        }
        .btn-hover:hover {
            transform: translateY(-5px) scale(1.1) rotateZ(2deg);
            transition: all 0.4s cubic-bezier(0.68, -0.55, 0.265, 1.55);
            box-shadow: 0 20px 40px rgba(255,0,128,0.4), 0 10px 20px rgba(0,255,128,0.3);
        }
        .fade-in {
            animation: fadeInUp 0.8s ease-out;
        }
        @keyframes fadeInUp {
            from { 
                opacity: 0; 
                transform: translateY(30px) scale(0.95); 
            }
            to { 
                opacity: 1; 
                transform: translateY(0) scale(1); 
            }
        }
        .bounce {
            animation: bounce 2s infinite;
        }
        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
            40% { transform: translateY(-10px); }
            60% { transform: translateY(-5px); }
        }
        .pulse {
            animation: pulse 2s infinite;
        }
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        .rotate {
            animation: rotate 3s linear infinite;
        }
        @keyframes rotate {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }
        .slide-in-left {
            animation: slideInLeft 0.6s ease-out;
        }
        @keyframes slideInLeft {
            from { 
                opacity: 0; 
                transform: translateX(-50px); 
            }
            to { 
                opacity: 1; 
                transform: translateX(0); 
            }
        }
        .slide-in-right {
            animation: slideInRight 0.6s ease-out;
        }
        @keyframes slideInRight {
            from { 
                opacity: 0; 
                transform: translateX(50px); 
            }
            to { 
                opacity: 1; 
                transform: translateX(0); 
            }
        }
        .rainbow-text {
            background: linear-gradient(45deg, #6366f1, #8b5cf6, #06b6d4, #10b981, #f59e0b, #ef4444, #ec4899, #84cc16, #3b82f6, #a855f7, #14b8a6, #f97316);
            background-size: 600% 600%;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: rainbowText 4s ease infinite;
        }
        @keyframes rainbowText {
            0% { background-position: 0% 50%; }
            25% { background-position: 100% 0%; }
            50% { background-position: 100% 100%; }
            75% { background-position: 0% 100%; }
            100% { background-position: 0% 50%; }
        }
        .neon-glow {
            text-shadow: 1px 1px 2px rgba(0,0,0,0.3), 0 0 4px rgba(74,144,226,0.4);
            color: #2c3e50;
            font-weight: 800;
        }
        .floating {
            animation: floating 3s ease-in-out infinite;
        }
        @keyframes floating {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
        }
        .wiggle:hover {
            animation: wiggle 0.5s ease-in-out;
        }
        @keyframes wiggle {
            0%, 100% { transform: rotate(0deg); }
            25% { transform: rotate(-3deg); }
            75% { transform: rotate(3deg); }
        }
        .glow {
            box-shadow: 0 0 20px rgba(139,92,246,0.3), 0 0 40px rgba(16,185,129,0.2), 0 0 60px rgba(245,158,11,0.15);
            animation: superGlow 3s ease-in-out infinite alternate;
        }
        @keyframes superGlow {
            0% { box-shadow: 0 0 20px rgba(139,92,246,0.3), 0 0 40px rgba(16,185,129,0.2), 0 0 60px rgba(245,158,11,0.15); }
            25% { box-shadow: 0 0 25px rgba(16,185,129,0.35), 0 0 50px rgba(245,158,11,0.25), 0 0 75px rgba(236,72,153,0.2); }
            50% { box-shadow: 0 0 30px rgba(245,158,11,0.4), 0 0 60px rgba(236,72,153,0.3), 0 0 90px rgba(6,182,212,0.25); }
            75% { box-shadow: 0 0 25px rgba(236,72,153,0.35), 0 0 50px rgba(6,182,212,0.25), 0 0 75px rgba(139,92,246,0.2); }
            100% { box-shadow: 0 0 20px rgba(6,182,212,0.3), 0 0 40px rgba(139,92,246,0.2), 0 0 60px rgba(16,185,129,0.15); }
        }
        .sparkle {
            position: relative;
            overflow: hidden;
        }
        .sparkle::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(45deg, transparent, rgba(255,255,255,0.8), transparent);
            animation: sparkleMove 3s linear infinite;
        }
        @keyframes sparkleMove {
            0% { transform: translateX(-100%) translateY(-100%) rotate(45deg); }
            100% { transform: translateX(100%) translateY(100%) rotate(45deg); }
        }
        .card-hover:hover {
            transform: translateY(-5px) rotateX(5deg);
            transition: all 0.3s ease;
        }
        .input-focus:focus {
            transform: scale(1.02);
            box-shadow: 0 0 15px rgba(79, 172, 254, 0.4);
            transition: all 0.3s ease;
        }
        .colorful-border {
            border: 3px solid;
            border-image: linear-gradient(45deg, #6366f1, #8b5cf6, #06b6d4, #10b981, #f59e0b, #ef4444, #ec4899, #84cc16, #3b82f6, #a855f7, #14b8a6, #f97316) 1;
            animation: borderShift 4s linear infinite;
            position: relative;
        }
        @keyframes borderShift {
            0% { border-image-source: linear-gradient(45deg, #6366f1, #8b5cf6, #06b6d4, #10b981, #f59e0b, #ef4444, #ec4899, #84cc16, #3b82f6, #a855f7, #14b8a6, #f97316); }
            16.67% { border-image-source: linear-gradient(45deg, #8b5cf6, #06b6d4, #10b981, #f59e0b, #ef4444, #ec4899, #84cc16, #3b82f6, #a855f7, #14b8a6, #f97316, #6366f1); }
            33.33% { border-image-source: linear-gradient(45deg, #06b6d4, #10b981, #f59e0b, #ef4444, #ec4899, #84cc16, #3b82f6, #a855f7, #14b8a6, #f97316, #6366f1, #8b5cf6); }
            50% { border-image-source: linear-gradient(45deg, #10b981, #f59e0b, #ef4444, #ec4899, #84cc16, #3b82f6, #a855f7, #14b8a6, #f97316, #6366f1, #8b5cf6, #06b6d4); }
            66.67% { border-image-source: linear-gradient(45deg, #f59e0b, #ef4444, #ec4899, #84cc16, #3b82f6, #a855f7, #14b8a6, #f97316, #6366f1, #8b5cf6, #06b6d4, #10b981); }
            83.33% { border-image-source: linear-gradient(45deg, #ef4444, #ec4899, #84cc16, #3b82f6, #a855f7, #14b8a6, #f97316, #6366f1, #8b5cf6, #06b6d4, #10b981, #f59e0b); }
            100% { border-image-source: linear-gradient(45deg, #6366f1, #8b5cf6, #06b6d4, #10b981, #f59e0b, #ef4444, #ec4899, #84cc16, #3b82f6, #a855f7, #14b8a6, #f97316); }
        }
        @keyframes fadeOut {
            from { 
                opacity: 1; 
                transform: translateY(0) scale(1); 
            }
            to { 
                opacity: 0; 
                transform: translateY(-20px) scale(0.9); 
            }
        }
    </style>
</head>
<body class="gradient-bg min-h-screen">
    <div class="container mx-auto px-4 py-8">
        <!-- Header -->
        <header class="text-center mb-8 fade-in">
            <div class="bounce mb-4 sparkle">
                <span class="text-8xl neon-glow">🎓✨🌟</span>
            </div>
            <h1 class="text-4xl md:text-6xl font-bold rainbow-text mb-4 pulse neon-glow">🌈 DATA SISWA KELAS 11 🌈</h1>
            <h2 class="text-2xl md:text-3xl text-gray-800 mb-2 slide-in-left glow sparkle font-bold bg-white px-4 py-2 rounded-xl shadow-lg">🏫 SMAS ISLAM MIFTAAHUSSURUR 🏫</h2>
            <p class="text-xl md:text-2xl text-yellow-200 slide-in-right floating neon-glow font-bold">✨🎊 TAHUN AJARAN 2025/2026 🎊✨</p>
            <div class="mt-4 flex justify-center space-x-4">
                <span class="text-3xl bounce" style="animation-delay: 0.1s">🌟</span>
                <span class="text-3xl bounce" style="animation-delay: 0.2s">⭐</span>
                <span class="text-3xl bounce" style="animation-delay: 0.3s">💫</span>
                <span class="text-3xl bounce" style="animation-delay: 0.4s">🌟</span>
                <span class="text-3xl bounce" style="animation-delay: 0.5s">⭐</span>
            </div>
        </header>

        <!-- Main Content -->
        <div class="max-w-4xl mx-auto">
            <!-- Form Section -->
            <div id="formSection" class="bg-gradient-to-br from-rose-50 via-violet-50 via-sky-50 to-emerald-50 rounded-3xl card-shadow p-8 md:p-12 mb-8 fade-in card-hover glow colorful-border sparkle">
                <div class="flex items-center justify-center mb-8">
                    <span class="text-5xl mr-4 wiggle rotate">👨‍🎓</span>
                    <h3 class="text-3xl md:text-4xl font-bold rainbow-text pulse neon-glow">🌟 ISI DATA DIRI KAMU 🌟</h3>
                    <span class="text-5xl ml-4 wiggle rotate">👩‍🎓</span>
                </div>
                
                <form id="studentForm" class="space-y-6">
                    <div class="grid md:grid-cols-2 gap-8">
                        <div class="sparkle">
                            <label for="nama" class="block text-lg font-black text-gray-800 mb-3 bg-white px-3 py-1 rounded-lg shadow-lg">👤 Nama Lengkap</label>
                            <input type="text" id="nama" name="nama" required 
                                   class="w-full px-6 py-4 border-4 border-pink-300 rounded-2xl focus:border-purple-500 focus:outline-none transition-all input-focus bg-white text-lg font-bold text-gray-800">
                        </div>
                        
                        <div class="sparkle">
                            <label for="ttl" class="block text-lg font-black text-gray-800 mb-3 bg-white px-3 py-1 rounded-lg shadow-lg">📅 Tempat, Tanggal Lahir</label>
                            <input type="text" id="ttl" name="ttl" required placeholder="Jakarta, 15 Januari 2008"
                                   class="w-full px-6 py-4 border-4 border-blue-300 rounded-2xl focus:border-cyan-500 focus:outline-none transition-all input-focus bg-white text-lg font-bold text-gray-800">
                        </div>
                    </div>
                    
                    <div class="grid md:grid-cols-2 gap-8">
                        <div class="sparkle">
                            <label for="hobi" class="block text-lg font-black text-gray-800 mb-3 bg-white px-3 py-1 rounded-lg shadow-lg">🎨 Hobi Favorit</label>
                            <input type="text" id="hobi" name="hobi" required placeholder="Membaca, Olahraga, Musik"
                                   class="w-full px-6 py-4 border-4 border-green-300 rounded-2xl focus:border-lime-500 focus:outline-none transition-all input-focus bg-white text-lg font-bold text-gray-800">
                        </div>
                        
                        <div class="sparkle">
                            <label for="noHp" class="block text-lg font-black text-gray-800 mb-3 bg-white px-3 py-1 rounded-lg shadow-lg">📱 Nomor HP</label>
                            <input type="tel" id="noHp" name="noHp" required placeholder="08123456789"
                                   class="w-full px-6 py-4 border-4 border-orange-300 rounded-2xl focus:border-yellow-500 focus:outline-none transition-all input-focus bg-white text-lg font-bold text-gray-800">
                        </div>
                    </div>
                    
                    <div class="sparkle">
                        <label for="alamat" class="block text-lg font-black text-gray-800 mb-3 bg-white px-3 py-1 rounded-lg shadow-lg">🏠 Alamat Lengkap</label>
                        <textarea id="alamat" name="alamat" required rows="4" placeholder="Jl. Contoh No. 123, Kelurahan, Kecamatan, Kota"
                                  class="w-full px-6 py-4 border-4 border-pink-300 rounded-2xl focus:border-rose-500 focus:outline-none transition-all resize-none input-focus bg-white text-lg font-bold text-gray-800"></textarea>
                    </div>
                    
                    <div class="flex flex-col sm:flex-row gap-6 pt-8">
                        <button type="submit" class="flex-1 bg-gradient-to-r from-violet-400 via-purple-400 to-fuchsia-400 hover:from-violet-500 hover:via-purple-500 hover:to-fuchsia-500 text-white font-bold py-4 px-8 rounded-2xl btn-hover transition-all duration-300 pulse wiggle sparkle text-xl neon-glow">
                            💾✨ SIMPAN DATA KU ✨💾
                        </button>
                        <button type="button" id="viewAllBtn" class="flex-1 bg-gradient-to-r from-emerald-400 via-teal-400 to-cyan-400 hover:from-emerald-500 hover:via-teal-500 hover:to-cyan-500 text-white font-bold py-4 px-8 rounded-2xl btn-hover transition-all duration-300 pulse wiggle sparkle text-xl neon-glow">
                            📋🌟 LIHAT SEMUA DATA 🌟📋
                        </button>
                    </div>
                </form>
            </div>

            <!-- Data List Section -->
            <div id="dataSection" class="bg-gradient-to-br from-amber-50 via-lime-50 via-cyan-50 to-indigo-50 rounded-3xl card-shadow p-8 md:p-12 hidden fade-in card-hover glow colorful-border sparkle">
                <div class="flex items-center justify-between mb-8">
                    <div class="flex items-center">
                        <span class="text-5xl mr-4 rotate floating">📊</span>
                        <h3 class="text-3xl md:text-4xl font-bold rainbow-text pulse neon-glow">🌟 DATA SEMUA SISWA 🌟</h3>
                        <span class="text-5xl ml-4 rotate floating">📈</span>
                    </div>
                    <button id="backToFormBtn" class="bg-gradient-to-r from-rose-400 via-pink-400 to-purple-400 hover:from-rose-500 hover:via-pink-500 hover:to-purple-500 text-white font-bold py-3 px-6 rounded-2xl btn-hover transition-all duration-300 wiggle sparkle text-lg neon-glow">
                        ← 🏠 KEMBALI 🏠
                    </button>
                </div>
                
                <div id="studentList" class="space-y-4">
                    <!-- Data akan ditampilkan di sini -->
                </div>
                
                <div id="emptyState" class="text-center py-16 hidden fade-in">
                    <div class="mb-6">
                        <span class="text-8xl block bounce">📝</span>
                        <span class="text-4xl block bounce" style="animation-delay: 0.2s">💫</span>
                    </div>
                    <p class="text-purple-600 text-2xl font-bold floating neon-glow mb-4">🌈 Belum ada data siswa yang tersimpan 🌈</p>
                    <div class="flex justify-center space-x-4 mt-6">
                        <span class="text-3xl pulse" style="animation-delay: 0.1s">✨</span>
                        <span class="text-3xl pulse" style="animation-delay: 0.3s">🌟</span>
                        <span class="text-3xl pulse" style="animation-delay: 0.5s">⭐</span>
                        <span class="text-3xl pulse" style="animation-delay: 0.7s">💫</span>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Edit Modal -->
    <div id="editModal" class="fixed inset-0 bg-black bg-opacity-50 hidden items-center justify-center z-50 p-4">
        <div class="bg-gradient-to-br from-orange-100 via-yellow-100 to-red-100 rounded-3xl card-shadow p-8 md:p-12 w-full max-w-3xl max-h-screen overflow-y-auto glow colorful-border sparkle">
            <div class="flex items-center justify-between mb-8">
                <h3 class="text-3xl md:text-4xl font-bold rainbow-text pulse neon-glow">✏️🌟 EDIT DATA SISWA 🌟✏️</h3>
                <button id="closeModalBtn" class="text-red-500 hover:text-red-700 text-4xl wiggle neon-glow">❌</button>
            </div>
            
            <form id="editForm" class="space-y-6">
                <input type="hidden" id="editIndex">
                
                <div class="grid md:grid-cols-2 gap-6">
                    <div>
                        <label for="editNama" class="block text-lg font-black text-gray-800 mb-3 bg-white px-3 py-1 rounded-lg shadow-lg">👤 Nama Lengkap</label>
                        <input type="text" id="editNama" name="nama" required 
                               class="w-full px-6 py-4 border-4 border-purple-300 rounded-2xl focus:border-purple-500 focus:outline-none transition-all input-focus bg-white text-lg font-bold text-gray-800">
                    </div>
                    
                    <div>
                        <label for="editTtl" class="block text-lg font-black text-gray-800 mb-3 bg-white px-3 py-1 rounded-lg shadow-lg">📅 Tempat, Tanggal Lahir</label>
                        <input type="text" id="editTtl" name="ttl" required 
                               class="w-full px-6 py-4 border-4 border-blue-300 rounded-2xl focus:border-blue-500 focus:outline-none transition-all input-focus bg-white text-lg font-bold text-gray-800">
                    </div>
                </div>
                
                <div class="grid md:grid-cols-2 gap-6">
                    <div>
                        <label for="editHobi" class="block text-lg font-black text-gray-800 mb-3 bg-white px-3 py-1 rounded-lg shadow-lg">🎨 Hobi</label>
                        <input type="text" id="editHobi" name="hobi" required 
                               class="w-full px-6 py-4 border-4 border-green-300 rounded-2xl focus:border-green-500 focus:outline-none transition-all input-focus bg-white text-lg font-bold text-gray-800">
                    </div>
                    
                    <div>
                        <label for="editNoHp" class="block text-lg font-black text-gray-800 mb-3 bg-white px-3 py-1 rounded-lg shadow-lg">📱 No. HP</label>
                        <input type="tel" id="editNoHp" name="noHp" required 
                               class="w-full px-6 py-4 border-4 border-orange-300 rounded-2xl focus:border-orange-500 focus:outline-none transition-all input-focus bg-white text-lg font-bold text-gray-800">
                    </div>
                </div>
                
                <div>
                    <label for="editAlamat" class="block text-lg font-black text-gray-800 mb-3 bg-white px-3 py-1 rounded-lg shadow-lg">🏠 Alamat Lengkap</label>
                    <textarea id="editAlamat" name="alamat" required rows="4"
                              class="w-full px-6 py-4 border-4 border-pink-300 rounded-2xl focus:border-pink-500 focus:outline-none transition-all resize-none input-focus bg-white text-lg font-bold text-gray-800"></textarea>
                </div>
                
                <div class="flex gap-6 pt-8">
                    <button type="submit" class="flex-1 bg-gradient-to-r from-blue-400 via-indigo-400 to-purple-400 hover:from-blue-500 hover:via-indigo-500 hover:to-purple-500 text-white font-bold py-4 px-8 rounded-2xl btn-hover transition-all duration-300 pulse wiggle sparkle text-xl neon-glow">
                        💾✨ SIMPAN PERUBAHAN ✨💾
                    </button>
                    <button type="button" id="cancelEditBtn" class="flex-1 bg-gradient-to-r from-gray-400 via-slate-400 to-zinc-400 hover:from-gray-500 hover:via-slate-500 hover:to-zinc-500 text-white font-bold py-4 px-8 rounded-2xl btn-hover transition-all duration-300 wiggle sparkle text-xl neon-glow">
                        ❌🔥 BATAL 🔥❌
                    </button>
                </div>
            </form>
        </div>
    </div>

    <script>
        let students = JSON.parse(localStorage.getItem('studentsData')) || [];
        let editingIndex = -1;

        // Form submission
        document.getElementById('studentForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const formData = new FormData(e.target);
            const student = {
                nama: formData.get('nama'),
                ttl: formData.get('ttl'),
                hobi: formData.get('hobi'),
                alamat: formData.get('alamat'),
                noHp: formData.get('noHp'),
                id: Date.now()
            };
            
            students.push(student);
            localStorage.setItem('studentsData', JSON.stringify(students));
            
            // Reset form
            e.target.reset();
            
            // Show success message
            showNotification('✅ Data berhasil disimpan!', 'success');
        });

        // View all data
        document.getElementById('viewAllBtn').addEventListener('click', function() {
            document.getElementById('formSection').classList.add('hidden');
            document.getElementById('dataSection').classList.remove('hidden');
            renderStudentList();
        });

        // Back to form
        document.getElementById('backToFormBtn').addEventListener('click', function() {
            document.getElementById('dataSection').classList.add('hidden');
            document.getElementById('formSection').classList.remove('hidden');
        });

        // Render student list
        function renderStudentList() {
            const listContainer = document.getElementById('studentList');
            const emptyState = document.getElementById('emptyState');
            
            if (students.length === 0) {
                listContainer.innerHTML = '';
                emptyState.classList.remove('hidden');
                return;
            }
            
            emptyState.classList.add('hidden');
            
            listContainer.innerHTML = students.map((student, index) => `
                <div class="bg-gradient-to-br from-pink-100 via-purple-100 via-blue-100 to-green-100 rounded-3xl p-8 border-4 border-transparent card-hover glow fade-in sparkle colorful-border" style="animation-delay: ${index * 0.1}s">
                    <div class="flex flex-col lg:flex-row lg:items-center justify-between">
                        <div class="flex-1 grid md:grid-cols-2 gap-6 mb-6 lg:mb-0">
                            <div class="slide-in-left sparkle">
                                <p class="text-lg font-black text-gray-800 mb-2 bg-purple-200 px-3 py-1 rounded-lg">👤 Nama:</p>
                                <p class="text-xl font-black text-gray-900 bg-white px-3 py-2 rounded-lg shadow-md">${student.nama}</p>
                            </div>
                            <div class="slide-in-right sparkle">
                                <p class="text-lg font-black text-gray-800 mb-2 bg-blue-200 px-3 py-1 rounded-lg">📅 TTL:</p>
                                <p class="text-lg font-bold text-gray-900 bg-white px-3 py-2 rounded-lg shadow-md">${student.ttl}</p>
                            </div>
                            <div class="slide-in-left sparkle">
                                <p class="text-lg font-black text-gray-800 mb-2 bg-green-200 px-3 py-1 rounded-lg">🎨 Hobi:</p>
                                <p class="text-lg font-bold text-gray-900 bg-white px-3 py-2 rounded-lg shadow-md">${student.hobi}</p>
                            </div>
                            <div class="slide-in-right sparkle">
                                <p class="text-lg font-black text-gray-800 mb-2 bg-orange-200 px-3 py-1 rounded-lg">📱 No. HP:</p>
                                <p class="text-lg font-bold text-gray-900 bg-white px-3 py-2 rounded-lg shadow-md">${student.noHp}</p>
                            </div>
                            <div class="md:col-span-2 slide-in-left sparkle">
                                <p class="text-lg font-black text-gray-800 mb-2 bg-pink-200 px-3 py-1 rounded-lg">🏠 Alamat:</p>
                                <p class="text-lg font-bold text-gray-900 bg-white px-3 py-2 rounded-lg shadow-md">${student.alamat}</p>
                            </div>
                        </div>
                        <div class="flex gap-4 lg:ml-8">
                            <button onclick="editStudent(${index})" class="bg-gradient-to-r from-amber-400 via-orange-400 to-yellow-400 hover:from-amber-500 hover:via-orange-500 hover:to-yellow-500 text-white font-bold py-3 px-6 rounded-2xl btn-hover transition-all duration-300 wiggle pulse sparkle text-lg neon-glow">
                                ✏️🌟 EDIT 🌟✏️
                            </button>
                            <button onclick="deleteStudent(${index})" class="bg-gradient-to-r from-rose-400 via-pink-400 to-red-400 hover:from-rose-500 hover:via-pink-500 hover:to-red-500 text-white font-bold py-3 px-6 rounded-2xl btn-hover transition-all duration-300 wiggle pulse sparkle text-lg neon-glow">
                                🗑️💥 HAPUS 💥🗑️
                            </button>
                        </div>
                    </div>
                </div>
            `).join('');
        }

        // Edit student
        function editStudent(index) {
            editingIndex = index;
            const student = students[index];
            
            document.getElementById('editIndex').value = index;
            document.getElementById('editNama').value = student.nama;
            document.getElementById('editTtl').value = student.ttl;
            document.getElementById('editHobi').value = student.hobi;
            document.getElementById('editAlamat').value = student.alamat;
            document.getElementById('editNoHp').value = student.noHp;
            
            document.getElementById('editModal').classList.remove('hidden');
            document.getElementById('editModal').classList.add('flex');
        }

        // Delete student with confirmation
        function deleteStudent(index) {
            const student = students[index];
            const confirmDiv = document.createElement('div');
            confirmDiv.className = 'fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50 p-4';
            confirmDiv.innerHTML = `
                <div class="bg-gradient-to-br from-red-100 via-pink-100 to-orange-100 rounded-3xl p-8 max-w-lg w-full glow colorful-border fade-in sparkle">
                    <div class="text-center">
                        <div class="mb-6">
                            <span class="text-6xl block bounce">⚠️</span>
                            <span class="text-4xl block bounce" style="animation-delay: 0.2s">💥</span>
                        </div>
                        <h3 class="text-2xl md:text-3xl font-bold rainbow-text mb-4 pulse neon-glow">🚨 KONFIRMASI HAPUS 🚨</h3>
                        <p class="text-gray-700 text-lg mb-8 floating font-semibold">Apakah kamu yakin ingin menghapus data <strong class="text-red-600 text-xl neon-glow">${student.nama}</strong>?</p>
                        <div class="flex gap-6">
                            <button onclick="confirmDelete(${index})" class="flex-1 bg-gradient-to-r from-red-400 via-rose-400 to-pink-400 hover:from-red-500 hover:via-rose-500 hover:to-pink-500 text-white font-bold py-3 px-6 rounded-2xl btn-hover wiggle sparkle text-lg neon-glow">
                                💥 YA, HAPUS! 💥
                            </button>
                            <button onclick="cancelDelete()" class="flex-1 bg-gradient-to-r from-slate-400 via-gray-400 to-zinc-400 hover:from-slate-500 hover:via-gray-500 hover:to-zinc-500 text-white font-bold py-3 px-6 rounded-2xl btn-hover wiggle sparkle text-lg neon-glow">
                                🛡️ BATAL 🛡️
                            </button>
                        </div>
                    </div>
                </div>
            `;
            document.body.appendChild(confirmDiv);
        }

        function confirmDelete(index) {
            students.splice(index, 1);
            localStorage.setItem('studentsData', JSON.stringify(students));
            renderStudentList();
            cancelDelete();
            showNotification('🗑️ Data berhasil dihapus!', 'success');
        }

        function cancelDelete() {
            const confirmDiv = document.querySelector('.fixed.inset-0.bg-black.bg-opacity-50');
            if (confirmDiv) {
                confirmDiv.remove();
            }
        }

        // Edit form submission
        document.getElementById('editForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const formData = new FormData(e.target);
            const index = parseInt(document.getElementById('editIndex').value);
            
            students[index] = {
                ...students[index],
                nama: formData.get('nama'),
                ttl: formData.get('ttl'),
                hobi: formData.get('hobi'),
                alamat: formData.get('alamat'),
                noHp: formData.get('noHp')
            };
            
            localStorage.setItem('studentsData', JSON.stringify(students));
            renderStudentList();
            closeModal();
            showNotification('✅ Data berhasil diperbarui!', 'success');
        });

        // Close modal
        function closeModal() {
            document.getElementById('editModal').classList.add('hidden');
            document.getElementById('editModal').classList.remove('flex');
        }

        document.getElementById('closeModalBtn').addEventListener('click', closeModal);
        document.getElementById('cancelEditBtn').addEventListener('click', closeModal);

        // Show notification
        function showNotification(message, type) {
            const notification = document.createElement('div');
            notification.className = `fixed top-4 right-4 z-50 px-6 py-3 rounded-lg text-white font-bold ${type === 'success' ? 'bg-gradient-to-r from-green-500 to-teal-600' : 'bg-gradient-to-r from-red-500 to-pink-600'} fade-in bounce glow`;
            notification.textContent = message;
            
            document.body.appendChild(notification);
            
            setTimeout(() => {
                notification.style.animation = 'fadeOut 0.5s ease-out forwards';
                setTimeout(() => {
                    notification.remove();
                }, 500);
            }, 2500);
        }

        // Close modal when clicking outside
        document.getElementById('editModal').addEventListener('click', function(e) {
            if (e.target === this) {
                closeModal();
            }
        });
    </script>
<script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'98f5352cf1de3e49',t:'MTc2MDU5MzA4Mi4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
