# Sistem Manajemen Wahana Dududu World

## Penjelasan sistem

Sistem Manajemen Wahana menyediakan tampilan data wahana yang tersedia di taman Bermain Dududu World. Sistem Wahana ini menyediakan fitur rating untuk user memberikan penilaian atas wahana yang sudah dimainkan. Fitur rating ini menyediakan penilaiaan dari angka 1-5 yang mana 5 artinya asyik dan 1 artinya tidak asyik. Selain itu, juga terdapat fitur tampilan data chart dan tabel wahana yang dapat dilihat oleh user secara langsung pada homepage sistem ini.

## Fitur utama Sistem Wahana Dududu World

Sistem wahana dududu world juga menyediakan **Chart Wahana Terfavorit** dan **Chart Domisili Kota Pengunjung Terbanyak** yang didapat dari sistem reservasi Takut.com

### Cara menjalankan sistem

 1. Clone repository berikut dengan link berikut ini
    ```sh
    git clone (https://github.com/victoria-angelique/Tugas-Besar-TST-II3160---K01--Kelompok-08.git)
    ```
2. Pastikan **xampp** atau **manager osx** sudah berjalan dan terlampir gambar seperti berikut
   <img width="673" alt="Screenshot 2023-12-18 at 20 27 33" src="https://github.com/victoria-angelique/Tugas-Besar-TST-II3160---K01--Kelompok-08/assets/91114869/65be6ac8-9e93-4538-a8e1-1b4fc83ac20b">
3. Buka link **php myadmin** http://localhost/phpmyadmin/ dengan web browser, kemudian buatlah database baru dengan nama wahanaku dengan click new sehingga terbuat database seperti berikut
   <img width="1105" alt="Screenshot 2023-12-18 at 20 32 26" src="https://github.com/victoria-angelique/Tugas-Besar-TST-II3160---K01--Kelompok-08/assets/91114869/58e43150-7483-482f-8d1f-019de510307f">
5. Selanjutnya, fetch data dengan command berikut untuk memasukkan data seeder ke dalam database di php my admin tadi
   ```sh
   php spark migrate:refresh
   ```
   ```sh
   php spark db:seed AllSeeder
   ```
5. Jalankan command berikut juga untuk menjalankan sistem di link localhost kalian menggunakan link berikut (http://localhost:8080/)
   ```sh
   npx tailwindcss -i ./public/css/input.css -o ./public/css/styles.css --watch
   ```
   ```sh
   php spark serve
   ```
6. Selamat, kalian berhasil masuk ke dalam sistem wahana apabila di layar kalian sudah tertampil interface berikut
   ![messageImage_1702401691414](https://github.com/victoria-angelique/Tugas-Besar-TST-II3160---K01--Kelompok-08/assets/91114869/f2c15850-70dc-4b62-a8a9-01630351b68d)

### Cara menjalankan sistem dengan deployment docker

 1. Clone repository berikut dengan link berikut ini
    ```sh
    git clone (https://github.com/victoria-angelique/Tugas-Besar-TST-II3160---K01--Kelompok-08.git)
    ```
2. Buka command terminal anda dan tuliskan command berikut
   ```sh
   make setup
   ```
   Apabila make setup anda belum berjalan bisa melakukan instalasi GNU terlebih dahulu dengan panduan link berikut (https://leangaurav.medium.com/how-to-setup-install-gnu-make-on-windows-324480f1da69)
5. Jalankan command berikutnya untuk menjalankan sistem 
   ```sh
   make migrate
   ```
   ```sh
   make run
   ```
6. Selamat, anda bisa menjalankan sistem kami di link (http://localhost:8080/) dan apabila kalian berhasil masuk ke dalam sistem wahana apabila di layar kalian sudah tertampil interface berikut
   ![messageImage_1702401691414](https://github.com/victoria-angelique/Tugas-Besar-TST-II3160---K01--Kelompok-08/assets/91114869/f2c15850-70dc-4b62-a8a9-01630351b68d)
