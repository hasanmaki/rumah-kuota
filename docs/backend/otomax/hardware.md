# rekomendasi pemetaan hardware

untuk menjalankan otomax , sebenar nya sangat memungkinkan semua software software pendukung di install pada satu perangkat, tetapi jika memungkinkan , akan sangat baik jika di pisah sesuai dengan domain nya masing masing, agar lebih optimal dan lebih mudah di maintenance.

## perbandingan

Tabler perbandingan ini akan memberi wawasan lebih luas, mengenai kelebihan dan kekurangan dari masing masing hardware yang di rekomendasikan.

| Keterangan    | Single PC | Multi PC |
| ------------- | :-------: | :------: |
| Biaya awal    |   Murah   |  Mahal   |
| Performa      |  Sedang   |  Tinggi  |
| Maintenance   |   Sulit   |  Mudah   |
| Skalabilitas  |  Rendah   |  Tinggi  |
| Auditabilitas |   Sulit   |  Mudah   |

sample pada case kerugian single pc:

terjadi selisih saldo pada account chip provider, dan karena PC nya single PC, maka untuk tracking activity dan browser history akan menjadi sulit, karena semua activity di jalankan pada satu perangkat.
sehingga ketika ada audit dan pemrikasaan data , kita harus turn off internet untuk sementara waktu, agar tidak ada activity baru yang masuk, sehingga kita bisa fokus untuk menelusuri activity yang sudah ada. dan ini akan menganggu otomax yang wajib online 24/7.

apalagi ketika addon tiket banking menggunakan chrome yang sama , maka history nya akan bercampur, sehingga akan menyulitkan untuk tracking.

sample pada case keuntungan single pc:

ketika ada update software, kita hanya perlu mengupdate pada satu perangkat saja, sehingga lebih mudah dan cepat.

koneksi cenderung lebih cepat , karena hanya perlu koneksi lokal saja, tanpa perlu melalui jaringan internet.

!!! warning

    untuk costomer service / operator yang akan bertugas untuk memantau otomax, maka multi pc sudah menjadi hal yang wajib, dan tidak dapat di kompromikan.

recomendasi software yang lebih baik terinstall dalam 1 pc yang sama dengan otomax:

1. database server tanpa ssms ( sql server saja , tanpa sql server management studio )
2. webreport everluck: karena sifat nya yang long running polling, sehingga lebih baik di jalankan pada pc yang sama dengan otomax. agar tidak ada delay pada saat pengambilan data.
3. addon tiketing banking: meskipun menggunakan automamation browser dan cenderung memakan resource yang cukup besar, tetapi lebih baik di jalankan pada pc yang sama dengan otomax, agar tidak ada delay pada saat melakukan insert data mutasi bank dan cek saldo bank.
4. addon provider: optional terpisah , jika hanya ada di bawah 10 chip, maka instalsi cukup pusatkan di satu pc saja. tetapi jika lebih dari 10 chip, maka lebih baik di pisah pada pc tersendiri. agar lebih optimal dan tidak menganggu performa otomax utama.
