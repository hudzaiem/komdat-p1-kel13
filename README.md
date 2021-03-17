# Aplikasi Web Commafeed



## sekilas tentang
Commafeed merupakan aplikasi pembaca feed yang terbuka untuk umum dan juga gratis. Dengan aplikasi ini kita dapat membuka berbagai bacaan dalam format apapun bahkan dalam bentuk url juga. Selain itu dengan aplikasi ini juga kita dapat melakukan hosting sendiri melalu server web. Tampilan dari aplikasi ini pun cukup responsif yang mana dapat menyesuaikan dengan ukura pengguna seperti di laptop, hp ataupun tablet.

## Instalasi
### Kebutuhan sistem
- Dropwizard
- AngularJs
- Java

### Proses Instalasi
pada awal instalasi, login kedalam server menggunakan SSH
    
    $ ssh student@localhost -p 2200
  
Setelah itu terdapat 3 Cara / versi :
1. **Versi sangat pendek**

    ```
 $ mkdir commafeed && cd commafeed
 $ wget https://github.com/Athou/commafeed/releases/download/2.5.0/commafeed.jar
 $ wget https://raw.githubusercontent.com/Athou/commafeed/2.5.0/config.yml.example -O config.yml
 $ vi config.yml
 $ java -Djava.net.preferIPv4Stack=true -jar commafeed.jar server config.yml

2. **Versi Pendek**
    ```
$ git clone https://github.com/Athou/commafeed.git
$ cd commafeed
$ ./mvnw clean package
$ cp config.yml.example config.yml
$ vi config.yml
$ java -Djava.net.preferIPv4Stack=true -jar target/commafeed.jar server config.yml

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
        ./mvnw clean package
    
    d. salin `config.yml.example` ke `config.yml` lalu edit. Kemudian ikuti langkah untuk menjalankan aplikasi ini. Server yang digunakan di `http://localhost:8082`
        java -Djava.net.preferIPv4Stack=true -jar target/commafeed.jar server config.yml

    
## Konfigurasi
Setting server tambahan yang diperlukan untuk meningkatkan fungsi dan kinerja aplikasi, misalnya:
- batas upload file
- batas memori
- dll

Plugin untuk fungsi tambahan : 
- login dengan Google/Facebook
- editor Markdown
- dll


## Maintenance (Optional)
Setting tambahan untuk maintenance secara periodik, misalnya:
- buat backup database tiap pekan
- hapus direktori sampah tiap hari
- dll


## Otomatisasi (Optional)
Skrip shell untuk otomatisasi instalasi, konfigurasi, dan maintenance.

## Cara Pemakaian
-Tampilan aplikasi web
-Fungsi-fungsi utama
-Isi dengan data real/dummy (jangan kosongan) dan sertakan beberapa screenshot


## Pembahasan
Aplikasi Commafeed ini memiliki berbagai kelebihan dan kekurangan . Kelebihan dari Commafeed diantaranya :
-Terintegrasi dengan banyak situs
-Responsif terhadap berbagai macam ukuran
 
Sementara itu kekurangan dari Commafeed ini adalah :
-Fitur yang cukup rumit
-Banyak aplikasi sejenis yang lebih lengkap fiturnya


## Referensi
1. [Source Code CommaFeed](https://github.com/Athou/commafeed)

2. [Tampilan CommaFeed](https://www.commafeed.com/#/feeds/view/category/31654063)

