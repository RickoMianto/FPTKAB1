# Final Project

## Teknologi Komputasi Awan

### Kelas B

#### Kelompok B1

Nama | NRP
---- | ----
Daffa Rajendra Priyatama | 5027231009
Muhammad Faqih Husain | 5027231023
Ricko Mianto Jaya Saputra | 5027231031
Nicholas Arya Krisnugroho Rerangin | 5027231058
Benjamin Khawarismi Habibi | 5027231078

## Permasalahan

Anda adalah seorang lulusan Teknologi Informasi, sebagai ahli IT, salah satu kemampuan yang harus dimiliki adalah Keampuan merancang, membangun, mengelola aplikasi berbasis komputer menggunakan layanan awan untuk memenuhi kebutuhan organisasi.

Pada suatu saat anda mendapatkan project untuk mendeploy sebuah aplikasi Sentiment Analysis dengan komponen Backend menggunakan python: sentiment-analysis.py dengan spesifikasi sebagai berikut

## Rancangan Arsitektur dan Tabel Harga Spesifikasi VM

Setelah melakukan analisis secara menyeluruh dan mempertimbangkan aspek harga dan spesifikasi, kami memutuskan untuk mengadopsi Digital Ocean sebagai platform cloud provider pilihan kami. Berikut adalah beberapa pertimbangan yang membuat kami memutuskan untuk menggunakan Digital Ocean:
1. Efisiensi Biaya: Digital Ocean menghadirkan struktur harga yang lebih ekonomis dibandingkan dengan kompetitor seperti Azure, memungkinkan pengoptimalan pengeluaran infrastruktur cloud tanpa mengorbankan performa.
2. Performa Tinggi: Spesifikasi hardware yang ditawarkan Digital Ocean tergolong tangguh dan mampu memenuhi kebutuhan komputasi yang kompleks. Hal ini memungkinkan kami untuk menjalankan aplikasi dan beban kerja dengan lancar tanpa hambatan.
3. Optimalisasi Performa Device: Berbeda dengan VM yang dapat membebani perangkat, Digital Ocean dirancang dengan mempertimbangkan efisiensi penggunaan sumber daya, sehingga meminimalisir dampak negatif terhadap performa device.

* Berikut adalah rancangan arsitektur yang telah kami buat untuk final project kami
![fptka2](https://github.com/RickoMianto/FPTKAB1/assets/150517828/5ce41cbb-397c-4c22-9ca4-b8950c3c077e)

* Berikut adalah tabel harga dan spesifikasi VM yang kami gunakan
![fptka](https://github.com/RickoMianto/FPTKAB1/assets/150517828/55c5569d-756e-4557-a1ae-88b45a9e8686)



## Langkah Implementasi dan Konfigurasi Teknologi

1. Buat database dan copy connection string.
   ![Database](https://github.com/RickoMianto/FPTKAB1/assets/149749135/0addc857-9d2f-47d3-8aaf-77814b5d5f62)
2. Create new connection dengan string database yang sudah di-copy sebelumnya
3. Buat database sesuai dengan variabel yang sudah dibuat di dalam `app.py`...
4. Create database baru dengan collection order...
5. Run `app.py` hingga muncul url-nya...
6. Untuk mengecek database bisa menggunakan Postman...
7. Deploy VM untuk worker dengan installasi requirement...
8. Buat Load Balancer dan pilih droplet worker...
9. Jika tidak ada error, lakukan load testing menggunakan Locust...

## Endpoints
1. **Analyze Text**
   - **Endpoint:** `POST /analyze`
   - **Description:** This endpoint accepts a text input and returns the sentiment score of the text.
   - **Request:**
     ```json
     {
        "text": "Your text here"
     }
     ```
    - **Response:**
      ```json
      {
        "sentiment": <sentiment_score>
      }
      ```

2. **Retrieve History**
   - **Endpoint:** `GET /history`
   - **Description:** This endpoint retrieves the history of previously analyzed texts along with their sentiment scores.
   - **Response:**
     ```json
     {
      {
        "text": "Your previous text here",
        "sentiment": <sentiment_score>
      },
      ...
     }
     ```
---

Kemudian juga disediakan sebuah Frontend sederhana menggunakan [index.html](/Resources/FE/index.html) dan [styles.css](/Resources/FE/styles.css) dengan tampilan antarmuka sebagai berikut

<img width="892" alt="Sentiment_analysis" src="https://github.com/RickoMianto/FPTKAB1/assets/149749135/a8b64d7a-db2e-4a15-8ff4-5be2649798e2">

Kemudian anda diminta untuk mendesain arsitektur cloud yang sesuai dengan kebutuhan aplikasi tersebut. Apabila dana maksimal yang diberikan adalah **1 juta rupiah per bulan (65 US$)**
konfigurasi cloud terbaik seperti apa yang bisa dibuat?

## Hasil Pengujian Setiap Endpoint

1. Get History

![Test End Point](https://github.com/RickoMianto/FPTKAB1/assets/149749135/d4de08da-2435-4bd8-a536-4fc6281ec49a)

## Hasil Pengujian dan analisis Loadtesting menggunakan Locust

- RPS Maksimum...

- Peak Concurrency Maksimum ***700*** dengan Spawn Rate ***50***
![Peak 700, Spawn rate 50](https://github.com/RickoMianto/FPTKAB1/assets/149749135/4587fe1c-76e2-461e-8eae-54d81c46e32c)


## Kesimpulan dan Saran

- Setelah percobaan yang kami lakukan dengan menggunakan tiga worker, berupa satu backend dan dua frontend, dikarenakan kami hanya menggunakan dua node balancer supaya bisa seimbang dan bebannya merata.

<img width="975" alt="Load balancingnya " src="https://github.com/RickoMianto/FPTKAB1/assets/149749135/f1968bd9-11af-4280-a6fa-6bffa8ea7a8c">

Untuk Load balancer ini memang idealnya hanya 2 kapasitas droplet saja sehingga tidak mudah unutk down

![Load Balancer](https://github.com/RickoMianto/FPTKAB1/assets/149749135/765fc2e4-a173-486f-8f4c-edde0fc18755)

- Harga yang ditawarkan Digital Ocean lebih murah, namun perlu juga ditekankan bahwa kualitas dari digital ocean ini kurang fleksibel untuk skala yang sangat besar dibandingkan dengan penyedia besar lainnya. Oleh karena itu, penting melihat skala mana yang akan dibuat sesuai kebutuhan yang ada. 
***Microsoft Azure*** opsi yang cukup baik untuk penggunaan banyak produk Microsoft dan memerlukan integrasi yang kuat, serta Cocok untuk aplikasi skala besar dan bisnis.
***Google Cloud Platform (GCP)*** untuk memanfaatkan infrastruktur jaringan Google yang kuat.
***Amazon Web Services (AWS)*** Idealnya untuk aplikasi skala besar dan kompleks.

- Terdapat banyak variabel yang berpengaruh dalam skenario pengujian Locustb seperti : 
Jumlah Users (Simulated Users)
   - Spawn Rate
   - Request Rate (RPS - Requests per Second)
   - Durasi Pengujian
   - Concurrency Level
   - Endpoint yang Diuji
   - Response Time
   - Failure Rate
   = Resource Utilization
   - Network Latency/Jaringan Internet

Jadi, perlu diketahui kebutuhan yang tepat agar penggunaan bisa dilakukan secara efisien dan tidak membuang budget yang sia-sia, serta bisa meminimalisir failure rate yang ada. Selain itu, jaringan internet perlu kualitas yang tinggi agar bisa dimanfaatkan secara maksimal.

 - Kuantitas database juga dapat mempengaruhi performa server/droplet yang kami buat karena beban worker VM untuk melakukan GET /history dan POST /anlayze juga semakin berat.


## Terakhir 
Terima kasih, sudah membaca
