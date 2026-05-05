## Informasi
| Informasi       | Keterangan                          |
|-----------------|-------------------------------------|
| Nama            | Hilman Ihza Amrullah               |
| NIM             | 312210310                          |
| Mata Kuliah     | Pemrograman Web                    |
| Deskripsi Tugas | Eksperimen SQL Injection dan mitigasinya |<br>

# UTS Pemrograman Web 2
Eksperimen SQL Injection pada Sistem Login Berbasis PHP dan Mitigasinya
[Link Artikel](https://medium.com/@hilmanamr22/eksperimen-sql-injection-pada-sistem-login-berbasis-php-dan-upaya-mitigasinya-f93d01dd1eff)

Repositori ini berisi hasil eksperimen terhadap celah keamanan SQL Injection pada sistem login sederhana berbasis PHP dan MySQL. Eksperimen dilakukan untuk memahami cara kerja serangan serta menerapkan teknik mitigasi yang tepat.


---

## Pendahuluan
SQL Injection merupakan celah keamanan pada aplikasi web yang terjadi karena input pengguna tidak divalidasi dengan baik. Hal ini memungkinkan penyerang menyisipkan perintah SQL berbahaya ke dalam query database.

---

## Tujuan
- Memahami SQL Injection  
- Melakukan simulasi serangan  
- Menerapkan mitigasi keamanan  

---

## Struktur Database
```sql
CREATE TABLE user (
  id INT AUTO_INCREMENT PRIMARY KEY,
  username VARCHAR(100),
  password VARCHAR(100)
);

INSERT INTO user (username, password) VALUES ('admin', '12345');
