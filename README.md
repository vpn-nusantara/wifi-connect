<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Detail Jaringan Wi-Fi</title>
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            background-color: #f9f9f9;
            margin: 0;
            padding: 20px;
            display: flex;
            justify-content: center;
        }

        .container {
            background-color: #ffffff;
            border: 1px solid #e0e0e0;
            border-radius: 16px;
            max-width: 500px;
            width: 100%;
            padding: 24px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.05);
        }

        h2 {
            text-align: center;
            margin: 0 0 4px 0;
            font-size: 22px;
            color: #000000;
            font-weight: 600;
        }

        .subtitle {
            text-align: center;
            color: #666666;
            font-size: 14px;
            margin-bottom: 24px;
        }

        .card {
            border: 1px solid #cccccc;
            border-radius: 12px;
            padding: 20px;
            margin-bottom: 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .info-section {
            flex: 1;
            padding-right: 15px;
        }

        .network-title {
            font-size: 20px;
            font-weight: bold;
            margin-bottom: 16px;
            color: #000000;
        }

        .label {
            font-size: 11px;
            color: #666666;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            margin-bottom: 2px;
        }

        .value {
            font-size: 18px;
            font-weight: bold;
            color: #000000;
            margin-bottom: 16px;
        }

        .btn-copy {
            background-color: #0066cc;
            color: white;
            border: none;
            border-radius: 8px;
            padding: 10px 24px;
            font-size: 14px;
            font-weight: 500;
            cursor: pointer;
            width: 85%;
            text-align: center;
        }

        .btn-copy:hover {
            background-color: #0052a3;
        }

        .qr-section {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }

        .qr-border {
            border: 3px solid #000000;
            border-radius: 12px;
            padding: 6px;
            background: white;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .qr-image {
            width: 110px;
            height: 110px;
            display: block;
        }

        .scan-me-container {
            display: flex;
            align-items: center;
            background-color: #000000;
            color: white;
            border-radius: 20px;
            padding: 4px 16px;
            margin-top: 10px;
            font-size: 14px;
            font-weight: bold;
        }

        /* Ikon Wi-Fi minimalis menggunakan CSS */
        .wifi-icon {
            width: 16px;
            height: 16px;
            margin-right: 6px;
            background: radial-gradient(circle at 50% 100%, transparent 60%, white 60%, white 70%, transparent 70%);
            position: relative;
        }
    </style>
</head>
<body>

<div class="container">
    <h2>Detail Jaringan Wi-Fi</h2>
    <div class="subtitle">Gunakan informasi di bawah untuk terhubung</div>

    <!-- Jaringan 1 -->
    <div class="card">
        <div class="info-section">
            <div class="network-title">Jaringan 1</div>
            
            <div class="label">Nama Wi-Fi (SSID)</div>
            <div class="value">NASI UDUK FR</div>
            
            <div class="label">Kata Sandi</div>
            <div class="value">2U346J2J88</div>
            
            <button class="btn-copy">Salin Kata Sandi</button>
        </div>
        <div class="qr-section">
            <div class="qr-border">
                <!-- Ganti URL gambar di bawah ini dengan file QR code asli Anda -->
                <img src="https://github.com/vpn-nusantara/wifi-connect/blob/main/NASI_UDUK_FR.png" alt="QR Code Jaringan 1" class="qr-image">
            </div>
            <div class="scan-me-container">
                <div class="wifi-icon"></div>
                Scan Me
            </div>
        </div>
    </div>

    <!-- Jaringan 2 -->
    <div class="card">
        <div class="info-section">
            <div class="network-title">Jaringan 2</div>
            
            <div class="label">Nama Wi-Fi (SSID)</div>
            <div class="value">NASI UDUK FR_4G</div>
            
            <div class="label">Kata Sandi</div>
            <div class="value">2U346J2J88</div>
            
            <button class="btn-copy">Salin</button>
        </div>
        <div class="qr-section">
            <div class="qr-border">
                <!-- Ganti URL gambar di bawah ini dengan file QR code asli Anda -->
                <img src="https://github.com/vpn-nusantara/wifi-connect/blob/main/NASI%20UDUK%20FR_4G.png" alt="QR Code Jaringan 2" class="qr-image">
            </div>
            <div class="scan-me-container">
                <div class="wifi-icon"></div>
                Scan Me
            </div>
        </div>
    </div>
</div>

</body>
</html>
