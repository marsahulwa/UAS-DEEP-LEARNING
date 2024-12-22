# **DEEP LEARNING (UAS)**
# **CHAT BOT INFORMASI UNIB**

### Nama Anggota Kelompok

| Nama                                | NPM         |
|-------------------------------------|-------------|
| **PUTRI RAHMAYANI**                 | G1A021030   |
| **MARSA HULWA INDRI MUTHI**         | G1A021058   |
| **TRIANA KESUMANINGRUM**            | G1A021068   |

## **LATAR BELAKANG**
Chatbot adalah perangkat lunak yang dapat berkomunikasi dengan manusia menggunakan bahasa alami. Model percakapan menggunakan teknologi kecerdasan buatan agar mampu memahami ucapan pengguna dan memberi tanggapan yang relevan mengenai pertanyaan dari pengguna. Chatbot Informasi Universitas Bengkulu (UNIB) digunakan untuk meningkatkan efisiensi mahasiswa maupun masyrakat untuk mencari informasi mengenai universitas bengkulu.

## **DATASET**
**Dataset** di buat dengan proses pengumpulan data manual melalui informasi yang tersedia pada laman web universitas bengkulu.

**Dataset** lalu disimpan dengan format JSON.

**Pengolahan data** dilakukan dengan **Tokenizer** untuk tokenisasi teks, menyamakan panjang urutan data dengan **Padding**, **LabelEncoder** untuk Encoding label.

## **MODEL**
Model yang digunakan adalah **LSTM(Long Short-Term Memory)**.

**ARSITEKTUR MODEL:**

| **Lapisan**                   | **Deskripsi**                                                                 | **Value**                                                   | 
|-------------------------------|-------------------------------------------------------------------------------|---------------------------------------------------------------|
| **Input Layer**                | Menerima data input dan memberikan data tersebut ke lapisan berikutnya.      | `shape=(input_shape,)`                                          | 
| **Embedding Layer**            | Mengonversi kata-kata dalam teks menjadi vektor numerik.                     | `vocabulary+1`, `10`. |
| **LSTM Layer**                 | Memproses data urutan dan mengenali pola serta hubungan antar elemen yang berurutan. | `10`, `return_sequences=True`, `recurrent_dropout=0.2`| 
| **Flatten Layer**              | Menyamkan keluaran dari LSTM agar dapat diproses lebih lanjut oleh lapisan berikutnya. | Tidak ada parameter tambahan.|
| **Dense Layer dengan Softmax** | Melakukan klasifikasi dan menghasilkan output probabilitas untuk setiap kelas yang ada. | `output_length`, `activation="softmax"`|


![Arsitektur model](https://github.com/marsahulwa/UAS-DEEP-LEARNING/blob/main/Gambar/Arsitektur%20model.png)

## **Kompilasi Model**

| **Parameter**  | **Value**                             |
|----------------|---------------------------------------|
| **loss**       | `sparse_categorical_crossentropy`     |
| **optimizer**  | `adam` (default: 0.001)                               |
| **metrics**    | `accuracy`                            |

## **Training Model**
Model di train dengan **500 epoch**

**Grafik hasil training (Accuracy dan loss)**

![Grafik Hasil Train](https://github.com/marsahulwa/UAS-DEEP-LEARNING/blob/main/Gambar/Grafik%20Hasil%20Train.png)

## **Hasil Test ChatBot Informasi Unib** 

![hasil1](https://github.com/marsahulwa/UAS-DEEP-LEARNING/blob/main/Gambar/hasil1.png)
![hasil2](https://github.com/marsahulwa/UAS-DEEP-LEARNING/blob/main/Gambar/hasil2.png)

## **Kesimpulan**
Pada pembuatan **ChatBot Informasi Unib** model yang digunakan adalah **LSTM** dengan pengaturan arsitektur dan parameter di dapatkan **akurasi 1.0000** dan **loss 0.0383** dari proses training dengan **500 epoch**, akurasi yang terus meningkat dan sangat tinggi serta loss yang terus menrun dan sangat rendah menunjukkan model telah cukup baik untuk diimplemenetasikan pada pengklasifikasian text seperti chatbot.

## **Analisa bagaimana model dapat dikatakan sebgai deep learning dan bukan shallow learn?**

Model LSTM dalam pembuatan ChatBot mengenai Informasi Unib termasuk dalam kategori Deep learning karena menggunakan arsitektur jaringan saraf dalam, dengan banyak lapisan. Model LSTM memilikki banyak lapisan seperti Input Layer, Embedding Layer, LSTM layer, Flatten, Dense. Sedangkan Shallow learn merupakan model sederhana atau model yang dangkal, biasayanya hanya menggunakan beberapa lapisan tidak sedalam lapian pada deep learning yang membuatnya kurang efektif dalam menangain masalah seperti pembuatan chatbot atau pengklasifikasian teks






