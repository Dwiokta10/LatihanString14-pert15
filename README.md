# Dwi Okta Ramadhani
# TI.24.A.1
# Latihan STRING 1
```python 
# Definisi string
txt = 'Hello World'

# Hitung jumlah karakter
print("Jumlah karakter:", len(txt))
```
# Output
Jumlah karakter: 11

```python
# Ambil karakter terakhir
print("Karakter terakhir:", txt[-1])
```
# Output
Karakter terakhir: d
```python
# Ambil karakter index ke-2 sampai index ke-4
print("Karakter index 2 sampai 4:", txt[2:5])
```
# Output
Karakter index 2 sampai 4: llo
```python
# Hilangkan spasi pada teks tersebut
print("Teks tanpa spasi:", txt.replace(" ", ""))
```
# Output
Teks tanpa spasi: HelloWorld
```python
# Ubah teks menjadi huruf besar
print("Huruf besar:", txt.upper())
```
# Output
Huruf besar: HELLO WORLD
```python
# Ubah teks menjadi huruf kecil
print("Huruf kecil:", txt.lower())
```
# Output
Huruf kecil: hello world
```python
# Ganti karakter H dengan karakter J
print("Ganti H dengan J:", txt.replace("H", "J"))
```
# Output
Ganti H dengan J: Jello World
```
```
# Latihan STRING 2
```python
# Definisi variabel
umur = 23
txt = 'Hello, nama saya john, dan umur saya adalah {} tahun'

# Format string
print(txt.format(umur))
```
# Output
Hello, nama saya john, dan umur saya adalah 23 tahun

# Latihan Program Studi Kasus Validasi Form Input
Selamat datang di Program Validasi Formulir Pendaftaran, sebuah solusi sederhana namun canggih untuk memastikan bahwa data input dalam formulir pendaftaran online sesuai dengan format yang diharapkan. Program ini memvalidasi input pengguna, termasuk **nama lengkap** , **nomor telepon** , dan **email** , guna memastikan data yang diterima bersih dan valid.
# Deskripsi Program
Program ini dibuat menggunakan *Fitur*
1. *Validasi Nama Lengkap*:  
   - Memastikan hanya huruf yang diterima (tanpa angka atau karakter khusus)
2. *Validasi Nomor Telepon*:  
   - Memastikan hanya angka yang diterima sebagai nomor telepon
3. *Validasi Email*:  
   - Memastikan format email benar, yaitu mengandung karakter @ dan . 
4. *Pesan Kesalahan Spesifik*:  
   - Memberikan notifikasi jelas tentang data yang tidak valid agar pengguna dapat memperbaikinya dengan mudah  
5. *Antarmuka Sederhana*:  
   - Menggunakan input berbasis teks dengan instruksi yang mudah dipahami
# Kode Program
```python
def validasi_nama(nama):
    # Cek apakah nama hanya berisi huruf
    if nama.isalpha():
        return True, "Nama valid."
    else:
        return False, "Nama hanya boleh berisi huruf."

def validasi_nomor_telepon(nomor):
    # Cek apakah nomor hanya berisi angka
    if nomor.isdigit():
        return True, "Nomor telepon valid."
    else:
        return False, "Nomor telepon hanya boleh berisi angka."

def validasi_email(email):
    # Cek apakah email mengandung @ dan .
    if "@" in email and "." in email:
        return True, "Email valid."
    else:
        return False, "Email harus mengandung karakter '@' dan '.'."

# Input dari pengguna
nama = input("Masukkan nama lengkap: ")
nomor_telepon = input("Masukkan nomor telepon: ")
email = input("Masukkan email: ")

# Validasi setiap input
validasi_nama_result, pesan_nama = validasi_nama(nama)
validasi_nomor_result, pesan_nomor = validasi_nomor_telepon(nomor_telepon)
validasi_email_result, pesan_email = validasi_email(email)

# Tampilkan hasil validasi
if validasi_nama_result and validasi_nomor_result and validasi_email_result:
    print("Data pendaftaran valid.")
else:
    print("Data pendaftaran tidak valid.")
    if not validasi_nama_result:
        print("Error pada Nama:", pesan_nama)
    if not validasi_nomor_result:
        print("Error pada Nomor Telepon:", pesan_nomor)
    if not validasi_email_result:
        print("Error pada Email:", pesan_email)
```
# Output Program
```
PS C:\Users\acer\Documents\KULIAH\PEMROGRAMAN\Pratikum 6 Bahasa Pemrograman> python -u "c:\Users\acer\Documents\KULIAH\PEMROGRAMAN\Pratikum 6 Bahasa Pemrograman\Daftar nilai mhs dictionary.py"

Menu Utama:
(T)ambah Data
(U)bah Data
(H)apus Data
(L)ihat Data
(C)ari Data
(K)eluar
Pilih menu: T

Tambah Data Mahasiswa
NIM: 312410068
Nama: Kenzi
Nilai Tugas: 98
Nilai UTS: 96
Nilai UAS: 99
Data berhasil ditambahkan!

Menu Utama:
(T)ambah Data
(U)bah Data
(H)apus Data
(L)ihat Data
(C)ari Data
(K)eluar
Pilih menu: T

Tambah Data Mahasiswa
NIM: 312410098
Nama: Ayen
Nilai Tugas: 97
Nilai UTS: 98
Nilai UAS: 99
Data berhasil ditambahkan!

Menu Utama:
(T)ambah Data
(U)bah Data
(H)apus Data
(L)ihat Data
(C)ari Data
(K)eluar
Pilih menu: T

Tambah Data Mahasiswa
NIM: 312410053
Nama: Marseal
Nilai Tugas: 98
Nilai UTS: 96
Nilai UAS: 90
Data berhasil ditambahkan!

Menu Utama:
(T)ambah Data
(U)bah Data
(H)apus Data
(L)ihat Data
(C)ari Data
(K)eluar
Pilih menu: T

Tambah Data Mahasiswa
NIM: 312410045
Nama: Budi
Nilai Tugas: 98
Nilai UTS: 96
Nilai UAS: 99
Data berhasil ditambahkan!

Menu Utama:
(T)ambah Data
(U)bah Data
(H)apus Data
(L)ihat Data
(C)ari Data
(K)eluar
Pilih menu: T

Tambah Data Mahasiswa
NIM: 312410042
Nama: Loriska
Nilai Tugas: 87
Nilai UTS: 99
Nilai UAS: 94
Data berhasil ditambahkan!

Menu Utama:
(T)ambah Data
(U)bah Data
(H)apus Data
(L)ihat Data
(C)ari Data
(K)eluar
Pilih menu: T

Tambah Data Mahasiswa
NIM: 312410056
Nama: Dwi
Nilai Tugas: 100
Nilai UTS: 100
Nilai UAS: 100
Data berhasil ditambahkan!

Menu Utama:
(T)ambah Data
(U)bah Data
(H)apus Data
(L)ihat Data
(C)ari Data
(K)eluar
Pilih menu: L

Daftar Nilai Mahasiswa
============================================================
| NO |    NIM    |    NAMA    | TUGAS | UTS | UAS | AKHIR |
============================================================
| 1  | 312410068 | Kenzi      | 98.0  | 96.0 | 99.0 | 97.65 |
| 2  | 312410098 | Ayen       | 97.0  | 98.0 | 99.0 | 98.05 |
| 3  | 312410053 | Marseal    | 98.0  | 96.0 | 90.0 | 94.50 |
| 4  | 312410045 | Budi       | 98.0  | 96.0 | 99.0 | 97.65 |
| 5  | 312410042 | Loriska    | 87.0  | 99.0 | 94.0 | 93.65 |
| 6  | 312410056 | Dwi        | 100.0 | 100.0 | 100.0 | 100.00 |
============================================================

Menu Utama:
(T)ambah Data
(U)bah Data
(H)apus Data
(L)ihat Data
(C)ari Data
(K)eluar
Pilih menu: K
Keluar dari program. Terima kasih!
PS C:\Users\acer\Documents\KULIAH\PEMROGRAMAN\Pratikum 6 Bahasa Pemrograman> 
```
# Cara Kerja Program
Program sederhana ini menggunakan tipe data dictionary dalam Python untuk menyimpan data mahasiswa. Setiap kunci dalam dictionary adalah NIM mahasiswa, dan nilainya adalah dictionary lain yang berisi informasi lengkap tentang mahasiswa tersebut (nama, nilai tugas, UTS, UAS, dan nilai akhir).
1. Menu Utama akan ditampilkan setiap kali program dijalankan.
2. Pengguna dapat memilih salah satu opsi menu:
    - Tambah Data Fungsi ini menambahkan data mahasiswa baru ke dalam dictionary.
    - Ubah Data Fungsi ini mengubah data mahasiswa yang sudah ada.
    - Hapus Data Fungsi ini menghapus data mahasiswa.
    - Tampilkan Data Fungsi ini menampilkan semua data mahasiswa yang tersimpan dalam format tabel.
    - Cari Data Fungsi ini mencari data mahasiswa berdasarkan NIM.
    - Keluar
   Program akan menjalankan fungsi yang sesuai dengan pilihan pengguna.

   Setelah selesai, program akan kembali ke Menu Utama.
   Jika pengguna memilih Keluar, program akan berhenti berjalan.
