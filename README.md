# **DEEP LEARNING (UAS)**
# **CHAT BOT INFORMASI UNIB**

### Nama Anggota Kelompok

| Nama                                | NPM         |
|-------------------------------------|-------------|
| **PUTRI RAHMAYANI**                 | G1A021030   |
| **MARSA HULWA INDRI MUTHI**         | G1A021058   |
| **TRIANA KESUMANINGRUM**            | G1A021068   |

### **LATAR BELAKANG**
Chatbot adalah perangkat lunak yang dapat berkomunikasi dengan manusia menggunakan bahasa alami. Model percakapan menggunakan teknologi kecerdeasan buatan agar mampu memahami ucapan pengguna dan memberi tanggapan yang relevan mengenai pertanyaan dari pengguna. Chatbot Informasi Universitas Bengkulu (UNIB) digunakan untuk meningkatkan efisiensi mahasiswa maupun masyrakat untuk mencari informasi mengenai universitas bengkulu.

## **DATASET**
**Dataset** di buat dengan proses pengumpulan data manual melalui informasi yang tersedia pada laman web universitas bengkulu.
**Dataset** berformat JSON.
**Pengolahan data** dilakukan dengan **Tokenizer** untuk tokenisasi teks, menyamakan anjang urutan data dengan **Padding**, **LabelEncoder** untuk Encoding label.

## **MODEL**
Model yang digunakan adalah **LSTM**.

**ARSITEKTUR MODEL:**
| **Lapisan**                   | **Deskripsi**                                                                 |
|-------------------------------|-------------------------------------------------------------------------------|
| **Embedding Layer**            | Mengonversi kata-kata dalam teks menjadi vektor numerik . |
| **LSTM Layer**                 | Memproses data urutan dan mengenali pola serta hubungan antar elemen yang berurutan untuk memahami data. |
| **Flatten Layer**              | Menyamkan keluaran dari LSTM agar dapat diproses lebih lanjut oleh lapisan berikutnya. |
| **Dense Layer dengan Softmax** | Melakukan klasifikasi dan menghasilkan output probabilitas untuk setiap kelas yang ada. |



