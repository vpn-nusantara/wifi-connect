<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Detail Jaringan Wi-Fi</title>
    <!-- Menggunakan font modern dari Google Fonts -->
    <link href="https://googleapis.com" rel="stylesheet">
    
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Inter', sans-serif;
        }

        body {
            background-color: #f8fafc;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 20px;
        }

        /* Container Utama */
        .main-card {
            background: #ffffff;
            border-radius: 20px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.05);
            width: 100%;
            max-width: 450px;
            padding: 30px 24px;
            border: 1px solid #e2e8f0;
        }

        .header {
            text-align: center;
            margin-bottom: 28px;
        }

        .header h1 {
            font-size: 22px;
            color: #1e293b;
            font-weight: 700;
            margin-bottom: 6px;
        }

        .header p {
            font-size: 14px;
            color: #64748b;
        }

        /* Kartu Setiap Jaringan */
        .network-card {
            background: #ffffff;
            border: 1px solid #e2e8f0;
            border-radius: 16px;
            padding: 24px;
            margin-bottom: 20px;
            transition: transform 0.2s, box-shadow 0.2s;
        }

        .network-card:last-child {
            margin-bottom: 0;
        }

        .network-title {
            font-size: 18px;
            font-weight: 700;
            color: #0f172a;
            margin-bottom: 16px;
            border-bottom: 2px solid #f1f5f9;
            padding-bottom: 8px;
        }

        /* Info Teks */
        .info-group {
            margin-bottom: 14px;
        }

        .info-label {
            font-size: 11px;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            color: #94a3b8;
            font-weight: 600;
            margin-bottom: 4px;
        }

        .info-value {
            font-size: 16px;
            color: #334155;
            font-weight: 600;
            word-break: break-all;
        }

        /* Seksi Barcode (Di bawah teks) */
        .barcode-section {
            display: flex;
            flex-direction: column;
            align-items: center;
            margin-top: 20px;
            padding-top: 16px;
            border-top: 1px dashed #e2e8f0;
        }

        /* Ukuran barcode diperbesar & terlihat jelas */
        .barcode-wrapper {
            background: #ffffff;
            border: 1px solid #cbd5e1;
            padding: 12px;
            border-radius: 12px;
            display: inline-block;
            margin-bottom: 8px;
        }

        .barcode-wrapper img {
            display: block;
            width: 160px; /* Ukuran gambar barcode */
            height: 160px;
            object-fit: contain;
        }

        .scan-text {
            font-size: 12px;
            color: #64748b;
            font-weight: 500;
            margin-bottom: 16px;
        }

        /* Tombol Salin Kata Sandi */
        .btn-copy {
            width: 100%;
            background-color: #0284c7;
            color: white;
            border: none;
            padding: 12px;
            font-size: 14px;
            font-weight: 600;
            border-radius: 10px;
            cursor: pointer;
            transition: background-color 0.2s, transform 0.1s;
        }

        .btn-copy:hover {
            background-color: #0369a1;
        }

        .btn-copy:active {
            transform: scale(0.98);
        }
    </style>
</head>
<body>

    <div class="main-card">
        <div class="header">
            <h1>Detail Jaringan Wi-Fi</h1>
            <p>Gunakan informasi di bawah untuk terhubung</p>
        </div>

        <!-- Jaringan 1 -->
        <div class="network-card">
            <div class="network-title">Jaringan 1</div>
            
            <div class="info-group">
                <div class="info-label">Nama Wi-Fi (SSID)</div>
                <div class="info-value">NASI UDUK FR</div>
            </div>
            
            <div class="info-group">
                <div class="info-label">Kata Sandi</div>
                <div class="info-value" id="pass1">2U346J2J88</div>
            </div>

            <!-- Barcode berada di bawah teks -->
            <div class="barcode-section">
                <div class="barcode-wrapper">
                    <!-- Ganti src dengan link/path gambar barcodemu -->
                    <img src="images/NASI_UDUK_FR.png" alt="QR Code Jaringan 1">
                </div>
                <div class="scan-text">Scan Me</div>
                <button class="btn-copy" onclick="copyText('pass1', this)">Salin Kata Sandi</button>
            </div>
        </div>

        <!-- Jaringan 2 -->
        <div class="network-card">
            <div class="network-title">Jaringan 2</div>
            
            <div class="info-group">
                <div class="info-label">Nama Wi-Fi (SSID)</div>
                <div class="info-value">NASI UDUK FR_4G</div>
            </div>
            
            <div class="info-group">
                <div class="info-label">Kata Sandi</div>
                <div class="info-value" id="pass2">2U346J2J88</div>
            </div>

            <!-- Barcode berada di bawah teks -->
            <div class="barcode-section">
                <div class="barcode-wrapper">
                    <!-- Ganti src dengan link/path gambar barcodemu -->
                    <img src="images/NASI_UDUK_FR_4G.png" alt="QR Code Jaringan 2">
                </div>
                <div class="scan-text">Scan Me</div>
                <button class="btn-copy" onclick="copyText('pass2', this)">Salin Kata Sandi</button>
            </div>
        </div>
    </div>

    <!-- Script Salin Teks Otomatis -->
    <script>
        function copyText(elementId, button) {
            // Mengambil teks dari elemen kata sandi
            const textToCopy = document.getElementById(elementId).innerText;
            
            // Menggunakan Clipboard API untuk menyalin
            navigator.clipboard.writeText(textToCopy).then(() => {
                // Mengubah teks tombol sementara waktu untuk memberi tahu user
                const originalText = button.innerText;
                button.innerText = "✓ Tersalin!";
                button.style.backgroundColor = "#22c55e"; // Berubah warna menjadi hijau
                
                setTimeout(() => {
                    button.innerText = originalText;
                    button.style.backgroundColor = "#0284c7"; // Kembali ke warna semula
                }, 2000);
            }).catch(err => {
                console.error("Gagal menyalin teks: ", err);
            });
        }
    </script>
</body>
</html>
