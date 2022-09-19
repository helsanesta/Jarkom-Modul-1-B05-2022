# Jarkom-Modul-1-B05-2022

## Anggota 
<p>Helsa Nesta Dhaifullah - 5025201005</p>
<p>Achmad Nashruddin Riskynanda  - 5025201021</p>
<p>Haniif Ahmad Jauhari - 5025201224</p>

### No 1
Sebutkan web server yang digunakan pada "monta.if.its.ac.id"! </br>
**Jawaban**: nginx/1.10.3 </br>
Langkah-langkah :
- apply display filter `http contains "monta"`
![gambar1](https://user-images.githubusercontent.com/70515589/191040421-450e0761-91e9-45a2-93b1-a82c0610eb1f.png)
- Klik kanan, lalu klik follow TCP Stream
![gambar2](https://user-images.githubusercontent.com/70515589/191040603-b8d0173c-3e45-4ca0-b7fc-8e51c214e680.png)
- Dapat dilihat servernya di dalamnya
![gambar3](https://user-images.githubusercontent.com/70515589/191040610-e1233765-31d7-4167-b095-8f7ead5d58e7.png)

### No 2
Ishaq sedang bingung mencari topik ta untuk semester ini , lalu ia datang ke website monta dan menemukan detail topik pada website “monta.if.its.ac.id” , judul TA apa yang dibuka oleh ishaq ? </br>
**Jawaban**: Evaluasi unjuk Kerja User Space FileSystem </br>
Langkah-langkah :
- apply display filter `http`
![image](https://user-images.githubusercontent.com/70515589/191042533-b796d7b2-0804-4c79-91c0-60953156f304.png)
- Paket 599 terletak merupakan lanjutan dari paket 576 yang menuju link detail topik (klik kanan dan follow tcp stream)
![image](https://user-images.githubusercontent.com/70515589/191043039-7fd89d2f-451a-4107-9a75-232e6e4a9e9b.png)
-  Dari sana dapat ditemukan jawaban judul topik yang dilihat

### No 3
Filter sehingga wireshark hanya menampilkan paket yang menuju port 80!</br>

