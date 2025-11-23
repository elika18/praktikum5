# PRAKTIKUM 5
## Latihan 1: Manajemen Kontak dengan Python Dictionary

Praktikum ini adalah latihan dasar untuk memahami cara kerja struktur data *Dictionary* pada Python. Kode ini mensimulasikan aplikasi daftar kontak sederhana dimana kita bisa menyimpan nama (sebagai Key) dan nomor telepon (sebagai Value).

### Deskripsi Tugas & Penjelasan Kode

Berikut adalah penjelasan langkah demi langkah dari 8 poin tugas yang dikerjakan dalam kode:

#### 1. Buat Dictionary daftar kontak
Nama sebagai key, dan nomor sebagai value
```daftar_kontak = {
    "Ari": "081267888",
    "Dina": "087677777"
}

print("====================================")
print("1. Dictionary Kontak Awal:")
print(daftar_kontak)
```
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/b7ae6f75-a753-4225-9b32-3a8c961f61f0" />

#### 2. Tampilkan kontaknya Ari
```print("====================================")
print("2. Nomor Kontak Ari:")
print(daftar_kontak["Ari"])
```
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/9f47cb67-5013-4409-85c2-8e97da4655af" />

#### 3. Tambah kontak baru dengan nama Riko, nomor 087654544
```daftar_kontak["Riko"] = "087654544"
print("====================================")
print("3. Kontak setelah menambah Riko:")
print(daftar_kontak)
```
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/fed89397-9eab-4241-bb5e-612a9406b6df" />

#### 4. Ubah kontak Dina dengan nomor baru 088999776
```daftar_kontak["Dina"] = "088999776"
print("====================================")
print("4. Kontak setelah mengubah nomor Dina:")
print(daftar_kontak)
```
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/5a19531a-fa0c-4f37-81e7-1561c7aea608" />

#### 5. Tampilkan semua Nama (Keys)
```print("====================================")
print("5. Semua Nama (Keys):")
print(list(daftar_kontak.keys()))
```
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/c34803f7-d2fd-4cf0-888f-ec040450b475" />

#### 6. Tampilkan semua Nomor (Values)
```print("====================================")
print("6. Semua Nomor (Values):")
print(list(daftar_kontak.values()))
```
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/a67c757d-8d52-4feb-9e87-d5d66b513357" />

#### 7. Tampilkan daftar Nama dan nomornya (Items)
```print("====================================")
print("7. Daftar Nama dan Nomor (Items):")
for nama, nomor in daftar_kontak.items():
    print(f"- {nama}: {nomor}")
```
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/b604b922-f752-4f16-a41b-6da331f507d7" />

#### 8. Hapus kontak Dina
```del daftar_kontak["Dina"]
print("====================================")
print("8. Kontak setelah menghapus Dina:")
print(daftar_kontak)
print("====================================")
```
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/7381a184-6399-493b-b709-b8b1bddd92b6" />
