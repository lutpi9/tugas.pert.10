# tugas.pert.10
## profil

| Variable       |    DATA DIRI         |
| ---------------| ----------------     |
| Nama           | Lutpiah Ainus Shiddik|                                     
| NIM            | 312310474            |
| Kelas          | TI.23.A.5            |
| Mata Kuliah    |Basis data            |

## *1. Lakukan penambahan data pada table mahasiswa dengan mengisi kd_ds yang belum ada pada data dosen.*
dengan kode sebagai berikut:

```
insert into dosen (kd_ds, nama ) VALUES
('DS001', 'LULU'),
('DS002', 'UPI'),
('DS003', 'LUTPI'),
('DS004', 'SAPA'),
('DS005', 'YUPI'),
('DS006', 'SAYA');

```
![1](https://github.com/lutpi9/tugas.pert.10/assets/147919251/3b51c724-1982-4ea1-89b9-25769bad0f62)
 ## outputnya:
 ![2](https://github.com/lutpi9/tugas.pert.10/assets/147919251/a50149b7-ed40-4b41-adfb-22474fc7d916)

 ## *2. Hapus satu record data pada table dosen yang telah dirujuk pada tabel mahasiswa.*

 ```
DELETE FROM dosen WHERE kd_ds = 'DS005';
```
## outputnya:
![3](https://github.com/lutpi9/tugas.pert.10/assets/147919251/6f24c7eb-79b4-49a1-9cd6-8387be6b9c8d)

## *3. Ubah mode menjadi ON UPDATE CASCADE ON DELETE RESTRICT*
Untuk mengubah CONSTRAINT FOREIGN KEY menjadi ON UPDATE CASCADE dan ON DELETE RESTRICT, perlu menambahkan CONSTRAINT dengan opsi yang diinginkan. Berikut ini adalah langkah-langkahnya:

Tambahkan CONSTRAINT FOREIGN KEY dengan opsi ON UPDATE CASCADE dan ON DELETE RESTRICT:
```
ALTER TABLE mahasiswa
ADD CONSTRAINT fk_dosen
FOREIGN KEY (kd_ds)
REFERENCES dosen (kd_ds)
ON UPDATE CASCADE
ON DELETE RESTRICT;
```
## outputnya:
![4](https://github.com/lutpi9/tugas.pert.10/assets/147919251/1bbe06a9-1744-4b45-bfd1-8018cb7fb95b)

## *4. Lakukan perubahan data pada table dosen (kd_ds)*
Berikut adalah contoh perintah untuk melakukan perubahan data pada tabel "dosen" dengan kolom "kd_ds":
```
UPDATE dosen SET kd_ds = 'DS005' WHERE nama = 'SAYA';
```
Perintah di atas akan mengubah nilai kolom "kd_ds" "SAYA" menjadi "DS005" pada tabel "dosen". anda dapat menyesuaikan nilai yang ingin anda ubah dan kondisi WHERE sesuai dengan kebutuhan Anda.

Pastikan untuk menjalankan perintah dengan hati-hati dan memastikan bahwa perubahan data yang Anda lakukan sesuai dengan kebutuhan dan kebijakan yang berlaku dalam basis data Anda.

## outputnya:
![5](https://github.com/lutpi9/tugas.pert.10/assets/147919251/b9ca5365-2dad-4e6c-8cf3-dbc2ce35b888)

## *5. Lakukan penghapusan data pada table dosen*
Untuk menghapus data dari tabel "dosen" dengan kondisi "kd_ds = 'DS006'", Anda dapat menggunakan perintah DELETE dengan sintaks yang benar. Berikut adalah contoh perintah yang dapat Anda gunakan:
```
DELETE FROM Dosen WHERE kd_ds = 'DS006';
```
## outputnya:
![6](https://github.com/lutpi9/tugas.pert.10/assets/147919251/f436af73-8d8e-45ad-abeb-4cb6d2b619ba)

## *6. Ubah mode menjadi ON UPDATE CASCADE ON DELETE SET NULL*
```
ALTER TABLE mahasiswa
DROP FOREIGN KEY fk_dosen;
```

```
ALTER TABLE mahasiswa
ADD CONSTRAINT fk_dosen
FOREIGN KEY (kd_ds)
REFERENCES dosen (kd_ds)
ON DELETE SET NULL;
```

## outputnya:
![6 2 yg plng baru](https://github.com/lutpi9/tugas.pert.10/assets/147919251/e33b379a-eb4e-4368-973d-c1ec491927c9)








