<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Koneksi Wi-Fi Otomatis</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f4f7f6;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
        }
        .card {
            background-color: #ffffff;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
            text-align: center;
            max-width: 380px;
            width: 100%;
        }
        h2 {
            color: #333;
            margin-bottom: 5px;
        }
        p.subtitle {
            color: #666;
            font-size: 14px;
            margin-top: 0;
            margin-bottom: 25px;
        }
        .info-box {
            background-color: #f9f9f9;
            border: 1px solid #e0e0e0;
            border-radius: 8px;
            padding: 15px;
            margin-bottom: 20px;
            text-align: left;
        }
        .info-item {
            margin-bottom: 10px;
        }
        .info-item:last-child {
            margin-bottom: 0;
        }
        .label {
            font-size: 12px;
            color: #888;
            text-transform: uppercase;
            font-weight: bold;
            display: block;
        }
        .value {
            font-size: 18px;
            color: #222;
            font-weight: 600;
        }
        .btn-copy {
            background-color: #007bff;
            color: white;
            border: none;
            padding: 12px;
            width: 100%;
            border-radius: 8px;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer;
            transition: background 0.2s;
        }
        .btn-copy:hover {
            background-color: #0056b3;
        }
        .footer {
            margin-top: 20px;
            font-size: 12px;
            color: #aaa;
        }
    </style>
</head>
<body>

<div class="card">
    <h2>Detail Jaringan Wi-Fi</h2>
    <p class="subtitle">Gunakan informasi di bawah untuk terhubung</p>
    
    <div class="info-box">
        <div class="info-item">
            <span class="label">Nama Wi-Fi (SSID)</span>
            <span class="value">NASI UDUK FR_4G</span>
        </div>
        <hr style="border: 0; border-top: 1px solid #eee; margin: 12px 0;">
        <div class="info-item">
            <span class="label">Kata Sandi</span>
            <span class="value" id="password">2U346J2J88</span>
        </div>
        <hr style="border: 0; border-top: 1px solid #eee; margin: 12px 0;">
        <div class="info-item">
            <span class="label">Jenis Keamanan</span>
            <span class="value">WPA/WPA2</span>
        </div>
    </div>

    <button class="btn-copy" onclick="copyPassword()">Salin Kata Sandi</button>
    
    <div class="footer">
        Pindai kode QR langsung dari kamera HP untuk masuk otomatis.
    </div>
</div>

<script>
function copyPassword() {
    const passwordText = document.getElementById("password").innerText;
    navigator.clipboard.writeText(passwordText).then(() => {
        alert("Kata sandi berhasil disalin ke papan klip!");
    }).catch(err => {
        alert("Gagal menyalin kata sandi otomatis.");
    });
}
</script>

</body>
</html>            cursor: pointer;
            text-decoration: none;
            display: inline-block;
            transition: background-color 0.3s;
        }
        .btn:hover {
            background-color: #1d4ed8;
        }
        .footer {
            margin-top: 25px;
            font-size: 12px;
            color: #94a3b8;
        }
    </style>
</head>
<body>

<div class="container">
    <h1>Koneksi Wi-Fi Cepat</h1>
    <p>Silakan gunakan informasi di bawah ini untuk terhubung ke jaringan Wi-Fi secara manual atau gunakan tombol akses.</p>
    
    <div class="info-box">
        <div class="info-item"><span class="label">Nama Wi-Fi (SSID):</span> NASI UDUK FR_4G</div>
        <div class="info-item"><span class="label">Kata Sandi:</span> 2U346J2J88</div>
        <div class="info-item"><span class="label">Keamanan:</span> WPA/WPA2</div>
    </div>
    
    <a href="WIFI:S:NASI UDUK FR_4G;T:WPA;P:2U346J2J88;;" class="btn">Hubungkan Otomatis</a>
    
    <div class="footer">
        Dibuat berdasarkan informasi QR code jaringan Anda.
    </div>
</div>

</body>
</html>
