Rangkuman Modul Praktikum Basis Data - HTML/CSS dengan Animasi

<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rangkuman Praktikum Basis Data</title>
    <style>
         {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background: linear-gradient(135deg, #1a2a6c, #b21f1f, #fdbb2d);
            background-size: 400% 400%;
            animation: gradientBG 15s ease infinite;
            color: #333;
            line-height: 1.6;
            padding: 20px;
            min-height: 100vh;
        }

        @keyframes gradientBG {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        header {
            text-align: center;
            margin-bottom: 40px;
            padding: 30px;
            background: rgba(255, 255, 255, 0.9);
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            animation: fadeIn 1s ease-out;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(-20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        h1 {
            color: #1a2a6c;
            font-size: 2.5rem;
            margin-bottom: 10px;
        }

        .subtitle {
            color: #b21f1f;
            font-size: 1.2rem;
        }

        .bab-container {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
            margin-bottom: 40px;
        }

        .bab {
            flex: 1;
            min-width: 300px;
            background: rgba(255, 255, 255, 0.9);
            border-radius: 15px;
            padding: 25px;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.15);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            animation: slideUp 0.8s ease-out;
            animation-fill-mode: both;
        }

        .bab:nth-child(1) { animation-delay: 0.2s; }
        .bab:nth-child(2) { animation-delay: 0.4s; }

        @keyframes slideUp {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .bab:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.25);
        }

        h2 {
            color: #1a2a6c;
            border-bottom: 3px solid #fdbb2d;
            padding-bottom: 10px;
            margin-bottom: 20px;
            font-size: 1.8rem;
        }

        h3 {
            color: #b21f1f;
            margin: 20px 0 10px;
            font-size: 1.4rem;
        }

        .highlight {
            background: #fff9c4;
            padding: 15px;
            border-radius: 10px;
            margin: 15px 0;
            border-left: 5px solid #fdbb2d;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% { box-shadow: 0 0 0 0 rgba(253, 187, 45, 0.4); }
            70% { box-shadow: 0 0 0 10px rgba(253, 187, 45, 0); }
            100% { box-shadow: 0 0 0 0 rgba(253, 187, 45, 0); }
        }

        ul, ol {
            margin-left: 20px;
            margin-bottom: 15px;
        }

        li {
            margin-bottom: 8px;
            position: relative;
            padding-left: 10px;
        }

        li:before {
            content: "▸";
            color: #fdbb2d;
            font-weight: bold;
            position: absolute;
            left: -15px;
        }

        .code-block {
            background: #2d2d2d;
            color: #f8f8f2;
            padding: 15px;
            border-radius: 8px;
            margin: 15px 0;
            font-family: 'Courier New', monospace;
            overflow-x: auto;
            border-left: 5px solid #b21f1f;
            animation: typewriter 1.5s steps(40) 1s both;
        }

        @keyframes typewriter {
            from { width: 0; }
            to { width: 100%; }
        }

        .conversion-table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            animation: fadeIn 1.5s ease-out;
        }

        .conversion-table th {
            background: #1a2a6c;
            color: white;
            padding: 12px;
            text-align: left;
        }

        .conversion-table td {
            padding: 12px;
            border-bottom: 1px solid #eee;
        }

        .conversion-table tr:nth-child(even) {
            background: #f9f9f9;
        }

        .conversion-table tr:hover {
            background: #fff9c4;
            transition: background 0.3s;
        }

        .important {
            background: #ffebee;
            border-left: 5px solid #b21f1f;
            padding: 15px;
            border-radius: 8px;
            margin: 15px 0;
            animation: shake 0.5s ease-in-out;
        }

        @keyframes shake {
            0%, 100% { transform: translateX(0); }
            25% { transform: translateX(-5px); }
            75% { transform: translateX(5px); }
        }

        footer {
            text-align: center;
            margin-top: 40px;
            padding: 20px;
            background: rgba(255, 255, 255, 0.9);
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            animation: fadeIn 2s ease-out;
        }

        .btn {
            display: inline-block;
            background: #1a2a6c;
            color: white;
            padding: 12px 25px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            margin: 10px;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }

        .btn:hover {
            background: #b21f1f;
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
        }

        @media (max-width: 768px) {
            .bab-container {
                flex-direction: column;
            }
            
            h1 {
                font-size: 2rem;
            }
            
            h2 {
                font-size: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>📚 Rangkuman Praktikum Basis Data</h1>
            <p class="subtitle">Bab 1 & 2 - Universitas Mercu Buana Yogyakarta</p>
        </header>

        <div class="bab-container">
            <div class="bab">
                <h2>📖 BAB 1: Cara Ubah Diagram ER Jadi Tabel Database</h2>
                
                <div class="highlight">
                    <h3>🎯 Tujuannya Apa Sih?</h3>
                    <p>Biar kamu paham gimana cara ngubah gambar diagram ER yang abstrak itu jadi tabel-tabel database yang bener dan bisa jalan di komputer.</p>
                </div>
                
                <h3>📋 Yang Dipelajari:</h3>
                <ul>
                    <li>Cara ngubah diagram ER jadi diagram relationship</li>
                    <li>Contoh nyata sistem pembayaran di apotik</li>
                </ul>
                
                <h3>🔧 Aturan Main Ngubah Diagram ER:</h3>
                
                <table class="conversion-table">
                    <thead>
                        <tr>
                            <th>Komponen ERD</th>
                            <th>Hasil Konversi</th>
                            <th>Contoh</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td><strong>Entitas/Kotak</strong></td>
                            <td>1 Tabel</td>
                            <td>Entitas "Mahasiswa" → tabel "mahasiswa"</td>
                        </tr>
                        <tr>
                            <td><strong>Atribut Kompleks</strong></td>
                            <td>Dipecah jadi beberapa kolom</td>
                            <td>"Alamat" → "jalan", "kota", "provinsi"</td>
                        </tr>
                        <tr>
                            <td><strong>Atribut Multinilai</strong></td>
                            <td>Tabel terpisah</td>
                            <td>1 mahasiswa punya banyak no telepon</td>
                        </tr>
                        <tr>
                            <td><strong>Relasi 1 ke Banyak</strong></td>
                            <td>Foreign Key di sisi 'banyak'</td>
                            <td>Tabel mahasiswa tambah kolom "id_dosen"</td>
                        </tr>
                        <tr>
                            <td><strong>Relasi Banyak ke Banyak</strong></td>
                            <td>Tabel penghubung</td>
                            <td>Tabel "krs" yang nyambungin mahasiswa & matkul</td>
                        </tr>
                    </tbody>
                </table>
                
                <div class="important">
                    <h3>⚠️ Yang Paling Penting Diinget:</h3>
                    <p>Kalo ada hubungan banyak ke banyak, HARUS bikin tabel baru buat nyambungin keduanya!</p>
                </div>
                
                <h3>📝 Evaluasi:</h3>
                <ul>
                    <li><strong>Test Awal:</strong> Suruh kenalin bagian-bagian diagram ER</li>
                    <li><strong>Test Akhir:</strong> Suruh ubah diagram ER yang ribet jadi kumpulan tabel</li>
                </ul>
            </div>

            <div class="bab">
                <h2>💻 BAB 2: Pengenalan Database & Perintah Dasar</h2>
                
                <div class="highlight">
                    <h3>🎯 Tujuannya:</h3>
                    <p>Biar bisa pake MySQL, ngerti perintah-perintah dasar, dan bisa bikin database sendiri.</p>
                </div>
                
                <h3>🔍 MySQL Itu Apa?</h3>
                <ul>
                    <li>Software buat manage database (tempenya data)</li>
                    <li>Gratis, cepat, bisa dipake di Windows/Linux/Mac</li>
                    <li>Biasanya dipake bareng XAMPP biar gampang instalasinya</li>
                </ul>
                
                <h3>⌨️ Cara Pake MySQL:</h3>
                <div class="code-block">
                    # Login ke MySQL lewat Command Prompt<br>
                    mysql -u root -p<br>
                    # Terus enter aja kalo passwordnya kosong<br><br>
                    
                    # Tempat file database disimpen:<br>
                    Windows: C:\xampp\mysql\data<br>
                    Linux: /opt/lampp/var/mysql/
                </div>
                
                <h3>📊 Jenis-jenis Data di MySQL:</h3>
                <ul>
                    <li><strong>INT:</strong> buat angka kayak 1, 2, 3, 100</li>
                    <li><strong>FLOAT:</strong> buat angka koma kayak 3.14, 2.5</li>
                    <li><strong>DATE:</strong> buat tanggal kayak 2024-01-15</li>
                    <li><strong>VARCHAR:</strong> buat teks kayak nama, alamat</li>
                </ul>
                
                <h3>🛠️ Perintah Dasar Yang Harus Dikuasain:</h3>
                <div class="code-block">
                    -- Bikin database baru<br>
                    CREATE DATABASE praktikum;<br><br>
                    
                    -- Liat database yang ada<br>
                    SHOW DATABASES;<br><br>
                    
                    -- Pilih database yang mau dipake<br>
                    USE praktikum;<br><br>
                    
                    -- Hapus database<br>
                    DROP DATABASE praktikum;
                </div>
                
                <div class="important">
                    <h3>💡 Tips Praktikum:</h3>
                    <p>Jangan takut nyoba dan salah! Database yang udah kehapus bisa dibikin lagi kok. Yang penting paham konsepnya dulu.</p>
                </div>
                
                <h3>📋 Yang Harus Dilakuin:</h3>
                <ol>
                    <li>Coba login ke MySQL di komputermu</li>
                    <li>Bikin database dengan nama "Prak_NIM" (ganti NIM dengan nim asli)</li>
                    <li>Praktekin semua perintah dasar</li>
                    <li>Bikin laporan yang isinya screenshot dan kode SQL</li>
                </ol>
            </div>
        </div>

        <footer>
            <h3>📁 Ketentuan Laporan Praktikum</h3>
            <p><strong>Format file:</strong> PrakDB_Bab[NoBab]-NIM.odt</p>
            <p><strong>Simpan di folder:</strong> PrakDB-NIM</p>
            <p><strong>Isi laporan:</strong> Source SQL + Screenshot CMD + Tema yang ditentukan</p>
            
            <div style="margin-top: 20px;">
                <a href="#" class="btn">📥 Download Modul Lengkap</a>
                <a href="#" class="btn">👨‍🏫 Kontak Asisten</a>
            </div>
            
            <p style="margin-top: 20px; font-style: italic;">Modul Praktikum Basis Data - Universitas Mercu Buana Yogyakarta</p>
        </footer>
    </div>

    <script>
        // Animasi tambahan saat scroll
        document.addEventListener('DOMContentLoaded', function() {
            const items = document.querySelectorAll('.bab, .highlight, .important');
            
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.animation = 'slideUp 0.8s ease-out forwards';
                        observer.unobserve(entry.target);
                    }
                });
            }, { threshold: 0.1 });
            
            items.forEach(item => {
                observer.observe(item);
            });
            
            // Efek ketik untuk code blocks
            const codeBlocks = document.querySelectorAll('.code-block');
            codeBlocks.forEach(block => {
                const originalText = block.innerHTML;
                block.innerHTML = '';
                let i = 0;
                const typeWriter = () => {
                    if (i < originalText.length) {
                        block.innerHTML += originalText.charAt(i);
                        i++;
                        setTimeout(typeWriter, 10);
                    }
                };
                setTimeout(typeWriter, 1000);
            });
        });
    </script>
</body>
</html>
