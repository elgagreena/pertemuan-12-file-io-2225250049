# Pertemuan 12 - File I/O dan Error Handling

Nama: Elga Greena Rahma Tazkia
NIM: 2225250049
Kelas: 3B

## Tujuan

Membaca, memvalidasi, mengolah, dan menulis data file dengan Python.

## Format File Input

Data nilai disimpan dalam file `data/nilai.txt` dengan format:

NIM,nilai

Contoh:

```text
A001,85
A002,78
A003,92
```

## Cara Menjalankan

Jalankan perintah berikut melalui terminal pada folder utama proyek:

```bash
python tugas/rekap_nilai_file.py
```

## Error yang Ditangani

* `FileNotFoundError`: menangani kondisi ketika file input tidak ditemukan.
* `ValueError`: menangani data nilai yang tidak dapat dikonversi menjadi angka.

## Test Case

| No. | Kondisi Pengujian     | Hasil Aktual                                          | Status   |
| --- | --------------------- | ----------------------------------------------------- | -------- |
| 1   | Data normal           | Data valid berhasil direkap                           | Berhasil |
| 2   | File tidak ditemukan  | Pesan file tidak ditemukan ditampilkan                | Berhasil |
| 3   | Nilai tidak valid     | Baris dengan nilai tidak valid dilewati               | Berhasil |
| 4   | Terdapat baris kosong | Baris kosong dilewati dan data lainnya tetap diproses | Berhasil |
| 5   | Nilai tepat 60        | Nilai 60 tetap dihitung lulus                         | Berhasil |

## Refleksi

Salah satu error yang ditemukan adalah `ValueError` ketika program membaca nilai yang berisi teks, seperti `abc`. Error tersebut ditangani menggunakan `try-except`, sehingga baris yang tidak valid dapat dilewati dan data lainnya tetap diproses.