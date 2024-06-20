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
Benjamin Khawarismi Habibi | 5027231031

## Permasalahan

Anda adalah seorang lulusan Teknologi Informasi, sebagai ahli IT, salah satu kemampuan yang harus dimiliki adalah Keampuan merancang, membangun, mengelola aplikasi berbasis komputer menggunakan layanan awan untuk memenuhi kebutuhan organisasi.

Pada suatu saat anda mendapatkan project untuk mendeploy sebuah aplikasi Sentiment Analysis dengan komponen Backend menggunakan python: sentiment-analysis.py dengan spesifikasi sebagai berikut

## Rancangan Arsitektur dan Tabel Harga Spesifikasi VM

Kami memutuskan untuk menggunakan Digital Ocean...

![Arsitektur](images/arsitektur.png)
![Tabel Harga](images/tabel_harga.png)

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
