| Nama        | Hilman Ihza Amrullah |
| NIM         | 312210310            |
| Mata Kuliah | Pemrograman Web 2    |

# UTS Pemrograman Web 2
Eksperimen SQL Injection pada Sistem Login Berbasis PHP dan Mitigasinya
[Link Artikel] (https://medium.com/@hilmanamr22/eksperimen-sql-injection-pada-sistem-login-berbasis-php-dan-upaya-mitigasinya-f93d01dd1eff)

Repositori ini berisi hasil eksperimen terhadap celah keamanan SQL Injection pada sistem login sederhana berbasis PHP dan MySQL. Eksperimen dilakukan untuk memahami cara kerja serangan serta menerapkan teknik mitigasi yang tepat.

'''$username = $_POST['username'];
$password = $_POST['password'];

$query = "SELECT * FROM user WHERE username='$username' AND password='$password'";
$result = mysqli_query($conn, $query);
