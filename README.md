<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Detail Jaringan Wi-Fi</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
        }

        body {
            background-color: #f8f9fa;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 20px;
        }

        .container {
            background-color: #ffffff;
            width: 100%;
            max-width: 500px;
            border: 1px solid #e0e0e0;
            border-radius: 16px;
            padding: 24px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
            text-align: center;
        }

        .header h1 {
            font-size: 22px;
            color: #1a1a1a;
            font-weight: 600;
            margin-bottom: 6px;
        }

        .header p {
            font-size: 14px;
            color: #666666;
            margin-bottom: 24px;
        }

        .card {
            border: 1px solid #cccccc;
            border-radius: 12px;
            padding: 16px;
            margin-bottom: 16px;
            display: flex;
            align-items: stretch;
            justify-content: space-between;
        }

        .info-section {
            width: 55%;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            text-align: left;
        }

        .info-group {
            margin-bottom: 12px;
        }

        .card h2 {
            font-size: 20px;
            color: #1a1a1a;
            margin-bottom: 14px;
        }

        .label {
            font-size: 11px;
            color: #444444;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            font-weight: 500;
            margin-bottom: 2px;
        }

        .value {
            font-size: 18px;
            font-weight: bold;
            color: #111111;
            word-break: break-all;
        }

        .btn-copy {
            background-color: #0066cc;
            color: white;
            border: none;
            border-radius: 8px;
            padding: 10px 16px;
            font-size: 14px;
            font-weight: 500;
            cursor: pointer;
            width: 100%;
            transition: background-color 0.2s;
            text-align: center;
        }

        .btn-copy:hover {
            background-color: #0052a3;
        }

        .btn-copy:active {
            background-color: #004080;
        }

        .qr-section {
            width: 40%;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            border: 2px solid #000000;
            border-radius: 16px;
            padding: 10px;
            background-color: #ffffff;
        }

        .qr-code {
            width: 100%;
            max-width: 120px;
            height: auto;
            aspect-ratio: 1/1;
            margin-bottom: 8px;
        }

        .scan-me-container {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 6px;
            border-top: 1px solid #e0e0e0;
            width: 100%;
            padding-top: 8px;
        }

        .wifi-icon {
            width: 16px;
            height: 16px;
        }

        .scan-text {
            font-size: 14px;
            font-weight: bold;
            color: #000000;
        }

        /* Notifikasi Toast */
        .toast {
            position: fixed;
            bottom: 20px;
            left: 50%;
            transform: translateX(-50%) translateY(100px);
            background-color: #333333;
            color: white;
            padding: 12px 24px;
            border-radius: 30px;
            font-size: 14px;
            opacity: 0;
            transition: transform 0.3s, opacity 0.3s;
            z-index: 999;
        }

        .toast.show {
            transform: translateX(-50%) translateY(0);
            opacity: 1;
        }
    </style>
</head>
<body>

    <div class="container">
        <div class="header">
            <h1>Detail Jaringan Wi-Fi</h1>
            <p>Gunakan informasi di bawah untuk terhubung</p>
        </div>

        <!-- Jaringan 1 -->
        <div class="card">
            <div class="info-section">
                <h2>Jaringan 1</h2>
                <div class="info-group">
                    <div class="label">Nama Wi-Fi (SSID)</div>
                    <div class="value">NASI UDUK FR</div>
                </div>
                <div class="info-group" style="margin-bottom: 16px;">
                    <div class="label">Kata Sandi</div>
                    <div class="value" id="pass1">2U346J2J88</div>
                </div>
                <button class="btn-copy" onclick="copyPassword('pass1')">Salin Kata Sandi</button>
            </div>
            <div class="qr-section">
                <!-- Anda bisa mengganti URL src gambar ini dengan file gambar QR code asli Anda nanti -->
                <img class="qr-code" <img src="images/NASI_UDUK_FR.png" alt="QR Jaringan 1" style="max-width: 100%; height: auto;">
                <div class=>
                </div>
            </div>
        </div>

        <!-- Jaringan 2 -->
        <div class="card">
            <div class="info-section">
                <h2>Jaringan 2</h2>
                <div class="info-group">
                    <div class="label">Nama Wi-Fi (SSID)</div>
                    <div class="value">NASI UDUK FR_4G</div>
                </div>
                <div class="info-group" style="margin-bottom: 16px;">
                    <div class="label">Kata Sandi</div>
                    <div class="value" id="pass2">2U346J2J88</div>
                </div>
                <button class="btn-copy" onclick="copyPassword('pass2')">Salin Kata Sandi</button>
            </div>
            <div class="qr-section">
                <!-- Anda bisa mengganti URL src gambar ini dengan file gambar QR code asli Anda nanti -->
                <img class="qr-code" <img src="images/NASI UDUK FR_4G.png" alt="QR Jaringan 2 "style="max-width: 100%; height: auto;">
                <div class=>
                </div>
            </div>
        </div>
    </div>

    <!-- Elemen Toast untuk pesan berhasil salin -->
    <div id="toast" class="toast">Kata sandi berhasil disalin!</div>

    <script>
        function copyPassword(elementId) {
            // Mengambil teks dari elemen kata sandi yang sesuai
            const passwordText = document.getElementById(elementId).innerText;

            // Menggunakan API modern Clipboard untuk menyalin teks
            navigator.clipboard.writeText(passwordText).then(() => {
                showToast();
            }).catch(err => {
                console.error('Gagal menyalin teks: ', err);
            });
        }

        function showToast() {
            const toast = document.getElementById('toast');
            toast.classList.add('show');
            
            // Menghilangkan pesan toast setelah 2 detik
            setTimeout(() => {
                toast.classList.remove('show');
            }, 2000);
        }
    </script>
</body>
</html>
