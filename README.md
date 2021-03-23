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
- Tampilan aplikasi web
- Fungsi-fungsi utama
- Isi dengan data real/dummy (jangan kosongan) dan sertakan beberapa screenshot

<img src="/Foto/1.png" align=center>

## Pembahasan
Aplikasi Commafeed ini memiliki berbagai kelebihan dan kekurangan

### Kelebihan dari Commafeed :
- Terintegrasi dengan banyak situs
- Responsif terhadap berbagai macam ukuran
 
### kekurangan dari Commafeed ini :
- Fitur yang cukup rumit
- Banyak aplikasi sejenis yang lebih lengkap fiturnya


## Referensi
1. [Source Code CommaFeed](https://github.com/Athou/commafeed)

2. [Tampilan CommaFeed](https://www.commafeed.com/#/feeds/view/category/31654063)

