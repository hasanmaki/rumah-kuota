# Tahapan Persiapan Server Otomax

!!! danger "Peringatan"

    Jangan Pernah Menggunakan Jabber untuk koneksi Otomax di lingkungan production, karena rawan pencurian.
    baik sebagai center untuk menerima transaksi, atau sebagai client untuk melakukan koneksi ke server lain.

Asumsi otomax sudah selesai terinstall dengan baik , docs ini hanya memberi panduan untuk melanjutkan dan mengkonfigurasi otomax agar berjalan lebih optimal.

## membuat modul pada otomax

untuk menambahkan modul pada otomax, sangat di sarankan untuk membuat modul based on supplier data, dan jika memungkinkan tidak membuat supplier ganda di module, seperti `h2h-supplier1` isi nya adalah supplier-1, dan semua hal terkait pemetaan product pada supplier tersebut terhitung sebagai satu module

beberapa best practice pada pembuatan module supplier :

1. koneksi kan ke server menggunakan module IP , lebih reliable dan lebih stabil, gunakan jalur back up hanya jika benar benar di butuhkan, seperti jika down dan lain lain ( rekomendasi jalur back up hanya menggunakan OH, tetapi OH agak rumit ketika butuh custom parameter parsing, jadi best option adalah menggunakan IP langsung )
2. jangan pernah hardcode data credentials , pada field paramter parsing, tetapi gunakan paramters parsing2 , agar nilai nya tetap encypted dan tersembunyi.
3. jangan setup auto kirim ulang jika memungkinkan, karena akan membebani thread server.
