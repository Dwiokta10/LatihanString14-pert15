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
_____________________________

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
_____________________________
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
    # Cek apakah nama hanya berisi huruf dan spasi
    if all(x.isalpha() or x.isspace() for x in nama):
        return True, "Nama valid."
    else:
        return False, "Nama hanya boleh berisi huruf dan spasi."

def validasi_nomor_telepon(nomor):
    # Cek apakah nomor hanya berisi angka dan panjang nomor valid
    if nomor.isdigit() and len(nomor) >= 10 and len(nomor) <= 13:
        return True, "Nomor telepon valid."
    else:
        return False, "Nomor telepon harus terdiri dari 10 hingga 13 angka."

def validasi_email(email):
    # Cek apakah email mengandung @ dan .
    if "@" in email and "." in email and email.index("@") < email.index("."):
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
PS C:\Users\acer\Documents\KULIAH\PEMROGRAMAN\Latihan string 14 pert 15> python -u "c:\Users\acer\Documents\KULIAH\PEMROGRAMAN\Latihan string 14 pert 15\LATIHANINPUT.py"
Masukkan nama lengkap: dwi okta ramadhani
Masukkan nomor telepon: 085814233926
Masukkan email: @dwi.okta.ramadhani.005.gmail.com
Data pendaftaran valid.

Masukkan nama lengkap: pramanta pratama putra
Masukkan nomor telepon: 089678453678
Masukkan email: @pratama.pramanta.ptr.gmail.com
Data pendaftaran valid.

Masukkan nama lengkap: munaroh
Masukkan nomor telepon: 08975246617382
Masukkan email: munaerohhabjd
Data pendaftaran tidak valid.
PS C:\Users\acer\Documents\KULIAH\PEMROGRAMAN\Latihan string 14 pert 15> python -u "c:\Users\acer\Documents\KULIAH\PEMROGRAMAN\Latihan string 14 pert 15\LATIHANINPUT.py"
```

# Cara Kerja Program
1. Input Data Pengguna:  
   Pengguna akan diminta memasukkan:  
   - *Nama Lengkap*
   - *Nomor Telepon* 
   - *Email*
2. Program memvalidasi setiap input menggunakan fungsi terpisah.  
3. Hasil validasi dikumpulkan untuk menentukan apakah data valid atau tidak.  
4. Jika valid, menampilkan pesan sukses. Jika tidak, memberikan pesan kesalahan detail untuk input yang salah.
