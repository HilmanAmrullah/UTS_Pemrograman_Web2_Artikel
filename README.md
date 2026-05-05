| Informasi       | Keterangan                          |
|-----------------|-------------------------------------|
| Nama            | Hilman Ihza Amrullah               |
| NIM             | 312210310                          |
| Mata Kuliah     | Pemrograman Web                    |
| Deskripsi Tugas | Eksperimen SQL Injection dan mitigasinya |<br>

# UTS Pemrograman Web 2
Eksperimen SQL Injection pada Sistem Login Berbasis PHP dan Mitigasinya
[Link Artikel](https://medium.com/@hilmanamr22/eksperimen-sql-injection-pada-sistem-login-berbasis-php-dan-upaya-mitigasinya-f93d01dd1eff)

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


<?php
$conn = mysqli_connect("localhost", "root", "", "test");

$username = $_POST['username'];
$password = $_POST['password'];

$query = "SELECT * FROM user WHERE username='$username' AND password='$password'";
$result = mysqli_query($conn, $query);

if(mysqli_num_rows($result) > 0){
    echo "Login berhasil";
}else{
    echo "Login gagal";
}
?>
