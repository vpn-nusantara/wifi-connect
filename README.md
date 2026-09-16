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
            background-color: #f7f9fa;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 20px;
        }

        /* Container Utama dengan flex agar card dan info kanan sejajar */
        .wrapper {
            display: flex;
            align-items: center;
            gap: 20px;
            max-width: 600px;
            width: 100%;
        }

        /* Card Putih Utama (Kiri) */
        .card {
            background: #ffffff;
            border-radius: 16px;
            padding: 24px;
            width: 280px;
            box-shadow: 0 4px 24px rgba(0, 0, 0, 0.04);
            text-align: center;
            flex-shrink: 0;
        }

        .title {
            font-size: 20px;
            font-weight: 600;
            color: #1a1a1a;
            line-height: 1.3;
            margin-bottom: 8px;
        }

        .subtitle {
            font-size: 12px;
            color: #8c8c8c;
            line-height: 1.4;
            margin-bottom: 24px;
        }

        /* Grup Informasi Jaringan */
        .info-group {
            text-align: left;
            margin-bottom: 16px;
        }

        .label {
            font-size: 10px;
            font-weight: 600;
            color: #a0a0a0;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            margin-bottom: 4px;
        }

        .value {
            font-size: 15px;
            font-weight: 600;
            color: #262626;
            line-height: 1.4;
            word-break: break-all;
        }

        /* Bagian Kanan (Tombol Salin & Keterangan QR) */
        .action-area {
            display: flex;
            align-items: center;
            gap: 12px;
            flex-grow: 1;
        }

        .btn-copy {
            background-color: #007aff;
            color: #ffffff;
            border: none;
            border-radius: 8px;
            padding: 12px 20px;
            font-size: 14px;
            font-weight: 500;
            cursor: pointer;
            white-space: nowrap;
            transition: background-color 0.2s;
        }

        .btn-copy:hover {
            background-color: #0062cc;
        }

        .qr-hint {
            font-size: 11px;
            color: #a6a6a6;
            line-height: 1.3;
            max-width: 140px;
        }

        /* Responsif untuk layar hp portrait kecil jika area tidak muat */
        @media (max-width: 480px) {
            .wrapper {
                flex-direction: column;
                align-items: center;
            }
            .action-area {
                flex-direction: column;
                text-align: center;
                align-items: center;
            }
        }
    </style>
</head>
<body>

    <div class="wrapper">
        <!-- Card Detail Wi-Fi -->
        <div class="card">
            <h1 class="title">Detail<br>Jaringan Wi-Fi</h1>
            <p class="subtitle">Gunakan informasi di bawah untuk terhubung</p>

            <div class="info-group">
                <div class="label">Nama Wi-Fi (SSID)</div>
                <div class="value">NASI UDUK FR</div>
                <div class="value">NASI UDUK FR_4G</div>
            </div>

            <div class="info-group">
                <div class="label">Kata Sandi</div>
                <div class="value">2U346J2J88</div>
            </div>

            <div class="info-group" style="margin-bottom: 0;">
                <div class="label">Jenis Keamanan</div>
                <div class="value">WPA/WPA2</div>
            </div>
        </div>

        <!-- Tombol Aksi di Luar Card -->
        <div class="action-area">
            <button class="btn-copy" onclick="copyPassword()">Salin Kata Sandi</button>
            <p class="qr-hint">Pindai kode QR langsung dari kamera HP untuk masuk otomatis.</p>
        </div>
    </div>

    <script>
        // Fungsi opsional untuk menyalin kata sandi ketika tombol diklik
        function copyPassword() {
            const password = "2U346J2J88";
            navigator.clipboard.writeText(password).then(() => {
                alert("Kata sandi berhasil disalin!");
            }).catch(err => {
                console.error("Gagal menyalin: ", err);
            });
        }
    </script>

</body>
</html>
