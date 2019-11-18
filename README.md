# Praktikum 4
### Program Data Mahasiswa

Pada praktikum 4, kita akan membuat program sederhana untuk menginput data ke dalam sebuah list.

#### Berikut Codingnya:
```python
nama = []
nim = []
tugas = []
uts = []
uas = []
akhir = []
mhsw = []
a = 0

while True:
    s_nama = input("Nama :")
    nama.append(s_nama)
    i_nim = int(input("NIM :"))
    nim.append(i_nim)
    i_tugas = int(input("Nilai Tugas :"))
    tugas.append(i_tugas)
    i_uts = int(input("Nilai UTS :"))
    uts.append(i_uts)
    i_uas = int(input("Nilai UAS :"))
    uas.append(i_uas)
    i_akhir = (i_tugas * 30/100) + (i_uts * 35/100) + (i_uas * 35/100)
    akhir.append(i_akhir)

    mhsw.append(nama)
    mhsw.append(nim)
    mhsw.append(tugas)
    mhsw.append(uts)
    mhsw.append(uas)
    mhsw.append(akhir)

    jawab = input("Tambah data (y/t)?")
    if jawab == 't':
        break

print("========================================================================")
print("|No.|       Nama       |    NIM    |  Tugas  |  UTS  |  UAS  |  Akhir  |")
print("========================================================================")
for a in range(0, len(mhsw[a])):
    print('|',a+1,'|       ',nama[a],'       |  ',nim[a],'  |  ',tugas[a],'  |  ',uts[a],'  |  ',uas[a],'  |  ',akhir[a],'  |')
print("========================================================================")
```

#### Penjelasan:
1.) Pertama kita membuat berbagai variable list kosong yang nantinya akan diinputkan dengan data - data yang diminta.
```python
nama = []
nim = []
tugas = []
uts = []
uas = []
akhir = []
mhsw = []
a = 0
```
Variable 'a' sebagai penghitung nomor.

2.) Lalu kita membuat kondisi perulangan dan statement yang akan dijalankan ketika perulangan terjadi.
```python
while True:
    s_nama = input("Nama :")
    nama.append(s_nama)
    i_nim = int(input("NIM :"))
    nim.append(i_nim)
    i_tugas = int(input("Nilai Tugas :"))
    tugas.append(i_tugas)
    i_uts = int(input("Nilai UTS :"))
    uts.append(i_uts)
    i_uas = int(input("Nilai UAS :"))
    uas.append(i_uas)
    i_akhir = (i_tugas * 30/100) + (i_uts * 35/100) + (i_uas * 35/100)
    akhir.append(i_akhir)

    mhsw.append(nama)
    mhsw.append(nim)
    mhsw.append(tugas)
    mhsw.append(uts)
    mhsw.append(uas)
    mhsw.append(akhir)
```
Disini, data yg diinputkan akan masuk ke dalam setiap list kosong yang telah dibuat seperti, ```inputan Nama akan masuk ke dalam list 'nama', Nilai tugas akan masuk ke dalam list 'tugas'``` dan seterusnya sampai nilai akhir yang merupakan perhitungan dari setiap nilai.
Setelah itu, setiap data list tersebut akan masuk ke dalam sebuah list lagi yang bernama 'mhsw'.

3.) Setelah membuat perulangan, kita membuat statement untuk menghentikan atau keluar dari perulangan yang terjadi.
```python
    jawab = input("Tambah data (y/t)?")
    if jawab == 't':
        break
```
Untuk keluar dari perulangan kita hanya perlu menginputkan 't' apabila diminta pada saat program dijalankan.

4.) Terakhir kita akan mencetak hasil dari program yang telah dibuat.
```python
print("========================================================================")
print("|No.|       Nama       |    NIM    |  Tugas  |  UTS  |  UAS  |  Akhir  |")
print("========================================================================")
for a in range(0, len(mhsw[a])):
    print('|',a+1,'|       ',nama[a],'       |  ',nim[a],'  |  ',tugas[a],'  |  ',uts[a],'  |  ',uas[a],'  |  ',akhir[a],'  |')
print("========================================================================")
```
```len(mhsw[a]))``` berfungsi untuk mengambil hasil dari setiap inputan data yang telah masuk ke dalam list 'mhsw' secara menurun.