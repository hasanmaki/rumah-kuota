# Dokumentasi Kas Digital

Project ini di dedikasikan untuk melakukan konfigurasi server pulsa otomax dan beberapa common best pratice dalam meneglola server otomax.
Project ini bukan Unofficial Guide dari Otomax, melainkan dokumentasi yang di buat berdasarkan pengalaman pribadi dan beberapa common use case yang sering di temui dalam mengelola server otomax.
untuk dokumentasi resmi dari otomax silahkan kunjungi [Otomax Documentation](https://otomax.id/docs/)

## Brief

komponen dalam distribusi server pulsa secara umum terbagi menjadi 2 bagian utama :

1. server ( engine proses transaksi )
2. client ( aplikasi user interface )
3. network ( konektivitas antar komponen )

### Server

server adalah engine utama yang memproses transaski, cakupan server adalah segala hal yg terkait dengan pemeroses transaksi, cakupan pembahasan nya adalah :

1. server : dalam hal ini menggunakan software `otomax`
2. database : dalam hal ini menggunakan `sqlserver`
3. Addon Pendukung : `aplikasi third party` untuk mendukung proses transaksi, seperti aplikasi sms gateway, aplikasi monitoring, aplikasi backup dll.

### Client

client adalah aplikasi user interface yang di gunakan untuk mengakses engine, cakupan client adalah segala hal yg terkait dengan aplikasi user interface, cakupan pembahasan nya adalah :

1. aplikasi web admin panel
2. aplikasi android client untuk bertransaksi

### network

Jaringan adalah konektivitas antar komponen, cakupan jaringan adalah segala hal yg terkait dengan konektivitas antar komponen, cakupan pembahasan nya adalah :

1. setup IP static
2. konfigurasi firewall
3. konfigurasi router

dalam hal jaringan kita akan menggunakan winbox sebagai alat bantu untuk konfigurasi router.

### Struktur Dokumentasi

dokumentasi akan kita pecah menjadi setiap langkah kecil dan segmented sesuai dengan area pembahasan, sehingga memudahkan pembaca untuk mencari topik yang ingin di pelajari.
urutan konfigurasi yg akan di bahas akan di mulai dari konfigurasi backend terlebih dahulu, baru kemudian di lanjutkan ke konfigurasi client.
