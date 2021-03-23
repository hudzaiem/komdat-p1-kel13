# Aplikasi Web Commafeed

<img src="1200px-CommaFeed.svg.png" width="300" height="300" align=center>

### Kelompok 13
| Nama                   | NIM       |
| ---------------------- | --------- |
| Shibgotalloh Sabilana  | G64180002 |
| Hudzaifah Muttaqin     | G64180119 |
| Yudha Berliandi        | G64180110 |
| Muhammad Hafiduddin    | G64180017 |

## sekilas tentang
***Commafeed*** merupakan aplikasi pembaca RSS feed yang terbuka untuk umum dan juga gratis. Dengan aplikasi ini kita dapat mengikuti berbagai jenis feeds xml dan mendapat update terbaru informasi feeds tersebut. Selain itu dengan aplikasi ini juga kita dapat melakukan hosting sendiri melalu server web. Tampilan dari aplikasi ini pun cukup responsif yang mana dapat menyesuaikan dengan ukuran pengguna seperti di laptop, hp ataupun tablet.

## Instalasi
### Kebutuhan sistem
- Dropwizard
- AngularJs
- Java
- Apache

### Proses Instalasi
pada awal instalasi, login kedalam server menggunakan SSH
    
        $ ssh student@localhost -p 2200
  
Setelah itu terdapat 3 Cara / versi :
1. **Versi sangat pendek**

        $ mkdir commafeed && cd commafeed
        $ wget https://github.com/Athou/commafeed/releases/download/2.5.0/commafeed.jar
        $ wget https://raw.githubusercontent.com/Athou/commafeed/2.5.0/config.yml.example -O config.yml
        $ vi config.yml
        $ java -Djava.net.preferIPv4Stack=true -jar commafeed.jar server config.yml

2. **Versi Pendek**

        $ git clone https://github.com/Athou/commafeed.git
        $ cd commafeed
        $ sudo ./mvnw clean package
        $ sudo cp config.yml.example config.yml
        $ cd target
        $ sudo cd wget  https://github.com/Athou/commafeed/releases/download/2.5.0/commafeed.jar
        $ cd ..
        $ sudo vi config.yml
        $ sudo java -Djava.net.preferIPv4Stack=true -jar target/commafeed.jar server config.yml

3. **Versi Panjang**

    a. Langkah pertama install terlebih dahulu required packages ke build CommaFeed pada Ubuntu
        
        # if openjdk-8-jdk is not available on your ubuntu version (14.04 LTS), add the following repo first*
       
        $ sudo add-apt-repository ppa:openjdk-r/ppa
        $ sudo apt-get update
                 
        $ sudo apt-get install g++ build-essential openjdk-8-jdk
                 
        $ Make sure java8 is the selected java version
        $ sudo update-alternatives --config java
        $ sudo update-alternatives --config javac
    
    b. Duplikasi  repositori ini
    
        $ git clone https://github.com/Athou/commafeed.git
        $ cd commafeed
        
    c. Setelah itu lakukan build pada apilkasi
    
        $ ./mvnw clean package
    
    d. salin `config.yml.example` ke `config.yml` lalu edit. Kemudian ikuti langkah untuk menjalankan aplikasi ini. Server yang digunakan di `http://localhost:8082`
    
        $ java -Djava.net.preferIPv4Stack=true -jar target/commafeed.jar server config.yml

    
## Konfigurasi
Disini kelompok kami menggunakan cara versi pendek, berikut prosesnya :

- Pertama kita diharuskan untuk menginstall Java dan Apache terlebih dahulu

        $ sudo apt install apache2
        $ sudo apt-get install default-jre
        
- Lalu dilanjutkan dengan menjalankan proses seperti pada skrip diatas. Pertama mengambil data dari github Commafeed sendiri

        $ Sudo git clone https://github.com/Athou/commafeed.git
        
- Lalu masuk ke direktori Commafeed
        
        $ cd commafeed

- Lalu kita menginstall package menggunakan maven
        
        $ ./mvnw clean package
        
- Selanjutnya file config.yml.example di copy menjadi config.yml

        $ cp config.yml.example config.yml

- Lalu terakhir kita menjalankan kode :

        $ Sudo java -Djava.net.preferIPv4Stack=true -jar target/commafeed.jar server config.yml

Selama kita menjalankan proses tersebut kita bisa mengakses aplikasi tadi lewat link `http://localhost:8082` di browser maka aplikasi Commafeed akan ditampilkan

## Cara Pemakaian
1. Kita Login terlebih dahulu (untuk setiap pemakai sudah diberi usernama dan password default sehingga tidak perlu melakukan proses SignUp)
<img src="/Foto/1.png" align=center>

2. Setelah berhasil kita akan masuk ke tampilan utama

![2](https://user-images.githubusercontent.com/60167974/112223320-5243ff80-8c5c-11eb-8bd8-db4a23497de6.png = 10x10)


3. Untuk memulai berlangganan dengan website yang akan diambil tekan tombol Subscribe di kiri atas

4. Masukan Link website yang dituju, beri judul dan pilih kategori. Setelah semua selesai tekan tombol Save

5. Proses berhasil dan kita bisa kembali ke halaman utama, maka Website berita yang dituju akan muncul

6. Selain itu semua artikel baerita tersebut akan muncul semua da kita bisa me refresh terus agar berita yang muncul dapat terus terupdate

Selain bisa mengambil berita, fitur lainnya yang dapat digunakan lewat aplikasi Commafeed ini diantaranya :
- Mengganti tema Website
- Mengganti pengaturan bahasa
- Refresh berita terupdate secara terus menerus
- Memberi mark artikel yang sudah dibaca dan yang belum
- Mengurutkan berita sesuai alfabet
- Filtering berita dengan jangkauan waktu (12 jam terakhir, satu hari terakhir, seminggu terakhir)
- Membuat kategori berita
- Mengubah tampilan dari bentuk list ke bentuk per artikel
- Dll


## Pembahasan
***Commafeed*** merupakan aplikasi Google Reader yang simpel. Aplikasi yang nampak seperti “koran online” ini pun tentunya memiliki berbagai kelebihan dan kekurangan . Beberapa Kelebihan dari Commafeed diantaranya :

### Kelebihan dari Commafeed :
- Terintegrasi dengan banyak situs
- Responsif terhadap berbagai macam ukuran
- Simpel dan mudah digunakan
- Bekerja secara real time
- Bersifat lebih pribadi
- Memiliki berbagai miniatur yang sangat membantu

### Kekurangan dari Commafeed ini :
- Banyak aplikasi sejenis yang lebih lengkap fiturnya
- Berita yang terintegrasi terbatas
- Tampilan yang kurang menarik dilihat oleh user
- Proses respon lambat

### Perbandingan dengan aplikasi sejenis (Commafeed & Feedly)
Jika dibandingkan dengan aplikasi sejenis seperti Feedly, Commafeed memiliki beberapa perbedaan :
- Feedly memiliki tampilan aplikasi lebih mengikuti zaman, sedangka Commafeed masih belum terlalu responsif
- Untuk Feedly sendiri memiliki fitur premium yang tentunya memiliki fitur-fitur tambahan lainnnya sedangkan pada Commafeed sendiri tidak ada
- Pada Feedly kita bisa mendapatkan berbagai rekomendasi berita mana yang ingin kita berlangganan, sedangkan pada Commafeed hal itu tidak ada, kita diharuskan mencari sendiri

## Referensi
1. [Source Code CommaFeed](https://github.com/Athou/commafeed)

2. [Tampilan CommaFeed](https://www.commafeed.com/#/feeds/view/category/31654063)

3. [Website RSS Reader](https://www.antaranews.com/rss)
