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

---

## Praktikum: Manajemen Nilai Mahasiswa
```data_mahasiswa = {}
```

### FUNGSI PERHITUNGAN NILAI AKHIR
```def hitung_nilai_akhir(tugas, uts, uas):
    """Menghitung Nilai Akhir dengan bobot Tugas: 30%, UTS: 35%, UAS: 35%."""
    # [span_0](start_span)Nilai Akhir diambil dari perhitungan 3 komponen nilai (tugas: 30%, uts: 35%, uas: 35%)[span_0](end_span)
    akhir = (tugas * 0.30) + (uts * 0.35) + (uas * 0.35)
    return round(akhir, 2)  # Dibulatkan 2 angka di belakang koma
```

### FUNGSI MENU UTAMA
```def tampilkan_menu():
    """Menampilkan pilihan menu utama."""
    print("\n==================================")
    print("| PROGRAM INPUT NILAI MAHASISWA |")
    print("==================================")
    # [span_1](start_span)Tampilkan menu pilihan: (Tambah Data, Ubah Data, Hapus Data, Tampilkan Data, Cari Data)[span_1](end_span)
    print("[(L)ihat, (T)ambah, (U)bah, (H)apus, (C)ari, (K)eluar]: ", end="")
    pilihan = input().upper()
    return pilihan
```

### FUNGSI TAMPILKAN DATA (LIHAT)
```def tampilkan_data():
    """Menampilkan seluruh data mahasiswa dalam bentuk tabel."""

    if not data_mahasiswa:
        print("\n[INFO]: TIDAK ADA DATA")
        return

    print("\n" + "=" * 70)
    print(f"| {'NO':<3} | {'NIM':<10} | {'NAMA':<20} | {'TUGAS':<5} | {'UTS':<5} | {'UAS':<5} | {'AKHIR':<6} |")
    print("=" * 70)

    no = 1
    for nim, data in data_mahasiswa.items():
        print(
            f"| {no:<3} | {nim:<10} | {data['Nama']:<20} | {data['Tugas']:<5} | {data['UTS']:<5} | {data['UAS']:<5} | {data['Akhir']:<6.2f} |")
        no += 1
    print("=" * 70)
```

### FUNGSI TAMBAH DATA
```def tambah_data():
    """Menambah data mahasiswa baru."""
    print("\n--- TAMBAH DATA ---")
    nim = input("NIM : ")

    if nim in data_mahasiswa:
        print(f"[ERROR]: NIM {nim} sudah ada!")
        return

    nama = input("Nama : ")
    # Input nilai dipastikan berupa angka
    try:
        tugas = float(input("Nilai Tugas : "))
        uts = float(input("Nilai UTS : "))
        uas = float(input("Nilai UAS : "))
    except ValueError:
        print("[ERROR]: Input nilai harus berupa angka.")
        return

    akhir = hitung_nilai_akhir(tugas, uts, uas)

    # Tambahkan data ke dictionary, dengan NIM sebagai key
    data_mahasiswa[nim] = {
        'Nama': nama,
        'Tugas': tugas,
        'UTS': uts,
        'UAS': uas,
        'Akhir': akhir
    }
    print(f"\n[SUKSES]: Data {nama} ({nim}) berhasil ditambahkan dengan Nilai Akhir {akhir:.2f}.")
```

### FUNGSI UBAH DATA 
```def ubah_data():
    """Mengubah data mahasiswa yang sudah ada."""
    print("\n--- UBAH DATA ---")
    nim_cari = input("Masukkan NIM mahasiswa yang ingin diubah: ")

    if nim_cari not in data_mahasiswa:
        print(f"[ERROR]: NIM {nim_cari} tidak ditemukan.")
        return

    data = data_mahasiswa[nim_cari]
    print(f"\nData saat ini untuk {data['Nama']} ({nim_cari}):")
    print(f"Tugas: {data['Tugas']}, UTS: {data['UTS']}, UAS: {data['UAS']}")

    try:
        data['Nama'] = input(f"Nama baru ({data['Nama']}): ") or data['Nama']
        data['Tugas'] = float(input(f"Nilai Tugas baru ({data['Tugas']}): ") or data['Tugas'])
        data['UTS'] = float(input(f"Nilai UTS baru ({data['UTS']}): ") or data['UTS'])
        data['UAS'] = float(input(f"Nilai UAS baru ({data['UAS']}): ") or data['UAS'])
    except ValueError:
        print("[ERROR]: Input nilai harus berupa angka.")
        return

    # Hitung ulang nilai akhir setelah perubahan
    data['Akhir'] = hitung_nilai_akhir(data['Tugas'], data['UTS'], data['UAS'])

    print(f"\n[SUKSES]: Data {nim_cari} berhasil diubah. Nilai Akhir baru: {data['Akhir']:.2f}.")
```

### FUNGSI HAPUS DATA
```def hapus_data():
    """Menghapus data mahasiswa berdasarkan NIM."""
    print("\n--- HAPUS DATA ---")
    nim_hapus = input("Masukkan NIM mahasiswa yang ingin dihapus: ")

    if nim_hapus not in data_mahasiswa:
        print(f"[ERROR]: NIM {nim_hapus} tidak ditemukan.")
        return

    nama = data_mahasiswa[nim_hapus]['Nama']
    del data_mahasiswa[nim_hapus]
    print(f"\n[SUKSES]: Data {nama} ({nim_hapus}) berhasil dihapus.")
```

### FUNGSI CARI DATA
```def cari_data():
    """Mencari dan menampilkan data satu mahasiswa."""
    print("\n--- CARI DATA ---")
    nim_cari = input("Masukkan NIM mahasiswa yang ingin dicari: ")

    if nim_cari not in data_mahasiswa:
        print(f"[ERROR]: NIM {nim_cari} tidak ditemukan.")
        return

    data = data_mahasiswa[nim_cari]
    print("\n--- DATA DITEMUKAN ---")
    print(f"NIM   : {nim_cari}")
    print(f"Nama  : {data['Nama']}")
    print(f"Tugas : {data['Tugas']}")
    print(f"UTS   : {data['UTS']}")
    print(f"UAS   : {data['UAS']}")
    print(f"AKHIR : {data['Akhir']:.2f}")
    print("----------------------")
```

### MAIN LOOP PROGRAM
```def main():
    while True:
        pilihan = tampilkan_menu()

        if pilihan == 'L':
            tampilkan_data()
        elif pilihan == 'T':
            tambah_data()
        elif pilihan == 'U':
            ubah_data()
        elif pilihan == 'H':
            hapus_data()
        elif pilihan == 'C':
            cari_data()
        elif pilihan == 'K':
            print("\nProgram dihentikan. Sampai jumpa!")
            break
        else:
            print("\n[ERROR]: Pilihan tidak valid. Silakan coba lagi.")


if __name__ == "__main__":
    main()
```

#### Hasilnya
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/145af7a9-0b88-4a8a-954a-be2110039b36" />


#### Berikut flowchart nya
<img width="1177" height="594" alt="image" src="https://github.com/user-attachments/assets/97151a99-b390-4731-9573-54b3e2c49e19" />
