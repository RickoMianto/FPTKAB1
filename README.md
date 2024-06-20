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

![fptka](https://github.com/RickoMianto/FPTKAB1/assets/150517828/55c5569d-756e-4557-a1ae-88b45a9e8686)



## Langkah Implementasi dan Konfigurasi Teknologi

1. Buat database dan copy connection string...
2. Create new connection dengan string database yang sudah di-copy sebelumnya...
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

1. Get All Orders
2. Get a Specific Orders by ID
3. Create a New Order
4. Update an Order by ID
5. Delete an Order by ID

## Hasil Pengujian dan Analisis Loadtesting Locust

- RPS Maksimum...
- Peak Concurrency Maksimum...

## Kesimpulan dan Saran

- Setelah percobaan yang kami lakukan...
- Harga yang ditawarkan Digital Ocean lebih murah...
- Terdapat banyak variabel yang berpengaruh dalam skenario pengujian Locust...
- Kuantitas database juga dapat mempengaruhi performa...

## About

No description, website, or topics provided.
