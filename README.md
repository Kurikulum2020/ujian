<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Masuk Ujian</title>
  <style>
    body { font-family: Arial, sans-serif; padding: 20px; text-align: center; }
    .warning { color: red; font-weight: bold; }
  </style>
</head>
<body>
  <h2>Memeriksa Aplikasi Ujian...</h2>
  <p id="status">Tunggu sebentar...</p>

  <script>
    const userAgent = navigator.userAgent.toLowerCase();
    const statusEl = document.getElementById('status');

    // Ganti ini dengan URL ujian Google Site kamu
    const ujianURL = "https://sites.google.com/view/asat-genap-daring-2025/juknis";

    if (userAgent.includes("exam") || userAgent.includes("cbt")) {
      statusEl.textContent = "Ditemukan aplikasi CBT ExamBrowser. Mengarahkan...";
      setTimeout(() => {
        window.location.href = ujianURL;
      }, 2000);
    } else {
      statusEl.innerHTML = `<span class="warning">⚠️ Anda tidak menggunakan aplikasi CBT ExamBrowser.<br>Silakan tutup browser ini dan buka menggunakan aplikasi ujian yang sesuai.</span>`;
    }
  </script>
</body>
</html>
