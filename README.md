# Latihan 1: Manajemen Kontak dengan Python Dictionary

Proyek ini adalah latihan dasar untuk memahami cara kerja struktur data **Dictionary** pada Python. Kode ini mensimulasikan aplikasi daftar kontak sederhana dimana kita bisa menyimpan nama (sebagai *Key*) dan nomor telepon (sebagai *Value*).

## Deskripsi Tugas & Penjelasan Kode

Berikut adalah penjelasan langkah demi langkah dari 8 poin tugas yang dikerjakan dalam kode:

1. Membuat Dictionary Daftar Kontak
Kita menginisialisasi dictionary bernama `daftar_kontak` dengan dua data awal.
* **Sintaks:** Menggunakan kurung kurawal `{}`.
* **Format:** `"Key": "Value"`.

```python
daftar_kontak = {
    "Ari": "081267888",
    "Dina": "087677777"
}
https://1drv.ms/i/c/89a1a1c1454ac923/EVkdgXCp82hJutLESbkwxsoBAD_l7saZqEYJ_BVTU3i3Ig?e=IoLelW

2. Menampilkan Kontak Ari
Mengambil dan menampilkan nomor telepon (value) berdasarkan nama (key) "Ari".
 * Sintaks: dictionary["Key"].
<!-- end list -->
print(daftar_kontak["Ari"])

3. Menambah Kontak Baru
Menambahkan data baru dengan nama "Riko". Karena key "Riko" belum ada sebelumnya, Python akan menambahkannya sebagai entri baru.
daftar_kontak["Riko"] = "087654544"

4. Mengubah Kontak Dina
Mengganti nomor telepon milik "Dina". Karena key "Dina" sudah ada di dalam dictionary, Python akan menimpa (overwrite) nomor lama dengan nomor baru.
daftar_kontak["Dina"] = "088999776"

5. Menampilkan Semua Nama (Keys)
Menampilkan daftar semua nama yang ada di kontak menggunakan method .keys().
# Mengembalikan view object berisi semua key
print(list(daftar_kontak.keys()))

6. Menampilkan Semua Nomor (Values)
Menampilkan daftar semua nomor telepon yang tersimpan menggunakan method .values().
# Mengembalikan view object berisi semua value
print(list(daftar_kontak.values()))

7. Menampilkan Daftar Nama dan Nomor
Menggunakan perulangan (loop) untuk menampilkan nama dan nomor secara berpasangan agar lebih rapi. Kita menggunakan method .items() yang mengembalikan pasangan (key, value).
for nama, nomor in daftar_kontak.items():
    print(f"- {nama}: {nomor}")

8. Menghapus Kontak Dina
Menghapus data "Dina" dari dictionary secara permanen menggunakan kata kunci del.
del daftar_kontak["Dina"]

Cara Menjalankan
Pastikan Python sudah terinstal, lalu jalankan perintah berikut di terminal:
python latihan1.py
