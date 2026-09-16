<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Detail Jaringan Wi-Fi</title>
    <!-- QRCode.js Library CDN untuk generate QR otomatis -->
    <script src="https://cloudflare.com"></script>
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
            width: 100%;
            max-width: 480px;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        /* Card Utama untuk Detail Jaringan */
        .info-card {
            background-color: #ffffff;
            border-radius: 20px;
            padding: 30px 24px;
            text-align: center;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.03);
        }

        .title {
            font-size: 20px;
            font-weight: 600;
            color: #1a1a1a;
            margin-bottom: 8px;
        }

        .subtitle {
            font-size: 14px;
            color: #666666;
            margin-bottom: 28px;
        }

        .label {
            font-size: 11px;
            text-transform: uppercase;
            color: #999999;
            letter-spacing: 0.5px;
            margin-bottom: 4px;
            font-weight: 500;
        }

        .value {
            font-size: 16px;
            font-weight: 600;
            color: #000000;
            line-height: 1.4;
            margin-bottom: 24px;
        }

        .btn-copy {
            width: 100%;
            background-color: #007aff;
            color: #ffffff;
            border: none;
            border-radius: 12px;
            padding: 14px;
            font-size: 15px;
            font-weight: 500;
            cursor: pointer;
            transition: background-color 0.2s;
        }

        .btn-copy:hover {
            background-color: #0062cc;
        }

        /* Container untuk Barcode / QR Code bawah */
        .qr-section {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 16px;
        }

        .qr-card {
            background-color: #ffffff;
            border-radius: 20px;
            padding: 20px 16px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.03);
        }

        .qr-container {
            width: 130px;
            height: 130px;
            display: flex;
            justify-content: center;
            align-items: center;
            margin-bottom: 16px;
        }

        .qr-container img {
            width: 100% !important;
            height: 100% !important;
        }

        .qr-desc {
            font-size: 11px;
            color: #666666;
            text-align: center;
            font-weight: 400;
        }
    </style>
</head>
<body>

    <div class="container">
        <!-- Bagian Atas: Detail Informasi -->
        <div class="info-card">
            <h2 class="title">Detail Jaringan Wi-Fi</h2>
            <p class="subtitle">Gunakan informasi di bawah untuk terhubung</p>

            <div class="label">Nama Wi-Fi (SSID)</div>
            <div class="value">
                NASI UDUK FR<br>
                NASI UDUK FR_4G
            </div>

            <div class="label">Kata Sandi</div>
            <div class="value" id="password">2U346J2J88</div>

            <button class="btn-copy" onclick="copyPassword()">Salin Kata Sandi</button>
        </div>

        <!-- Bagian Bawah: QR Code Dua Frekuensi -->
        <div class="qr-section">
            <div class="qr-card">
                <div class="qr-container" id="qr-24ghz"></div>
                <p class="qr-desc">NASI UDUK FR</p>
            </div>

            <div class="qr-card">
                <div class="qr-container" id="qr-5ghz"></div>
                <p class="qr-desc">NASI UDUK FR_4G</p>
            </div>
        </div>
    </div>

    <script>
        // Data Wi-Fi untuk dibuat jadi QR Code standar Android/iOS
        // Format: WIFI:S:[SSID];T:[WPA/WEP];P:[PASSWORD];;
        const wifi24 = "WIFI:S:NASI UDUK FR;T:WPA;P:2U346J2J88;;";
        const wifi5 = "WIFI:S:NASI UDUK FR_4G;T:WPA;P:2U346J2J88;;";

        // Generate QR Code untuk 2.4GHz
        new QRCode(document.getElementById("qr-24ghz"), {
            text: wifi24,
            width: 130,
            height: 130,
            colorDark : "#000000",
            colorLight : "#ffffff",
            correctLevel : QRCode.CorrectLevel.H
        });

        // Generate QR Code untuk 5GHz
        new QRCode(document.getElementById("qr-5ghz"), {
            text: wifi5,
            width: 130,
            height: 130,
            colorDark : "#000000",
            colorLight : "#ffffff",
            correctLevel : QRCode.CorrectLevel.H
        });

        // Fungsi Tombol Salin Kata Sandi
        function copyPassword() {
            const passwordText = document.getElementById("password").innerText;
            navigator.clipboard.writeText(passwordText).then(() => {
                alert("Kata sandi berhasil disalin ke clipboard!");
            }).catch(err => {
                console.error("Gagal menyalin kata sandi: ", err);
            });
        }
    </script>

</body>
</html>
