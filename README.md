# Prakrikum 5 Latihan Dictionary Python

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

# 2. Tampilkan kontaknya Ari
```print("====================================")
print("2. Nomor Kontak Ari:")
print(daftar_kontak["Ari"])
```

# 3. Tambah kontak baru dengan nama Riko, nomor 087654544
daftar_kontak["Riko"] = "087654544"
print("====================================")
print("3. Kontak setelah menambah Riko:")
print(daftar_kontak)


# 4. Ubah kontak Dina dengan nomor baru 088999776
daftar_kontak["Dina"] = "088999776"
print("====================================")
print("4. Kontak setelah mengubah nomor Dina:")
print(daftar_kontak)


# 5. Tampilkan semua Nama (Keys)
print("====================================")
print("5. Semua Nama (Keys):")
# Mengubah keys() ke list agar mudah dibaca saat dicetak
print(list(daftar_kontak.keys()))


# 6. Tampilkan semua Nomor (Values)
print("====================================")
print("6. Semua Nomor (Values):")
# Mengubah values() ke list agar mudah dibaca saat dicetak
print(list(daftar_kontak.values()))


# 7. Tampilkan daftar Nama dan nomornya (Items)
print("====================================")
print("7. Daftar Nama dan Nomor (Items):")
for nama, nomor in daftar_kontak.items():
    print(f"- {nama}: {nomor}")


# 8. Hapus kontak Dina
del daftar_kontak["Dina"]
print("====================================")
print("8. Kontak setelah menghapus Dina:")
print(daftar_kontak)
print("====================================")
