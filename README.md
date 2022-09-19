# Jarkom-Modul-1-B05-2022

## Anggota 
<p>Helsa Nesta Dhaifullah - 5025201005</p>
<p>Achmad Nashruddin Riskynanda  - 5025201021</p>
<p>Haniif Ahmad Jauhari - 5025201224</p>

### No 1
Sebutkan web server yang digunakan pada "monta.if.its.ac.id"! </br>
**Jawaban**: nginx/1.10.3 </br>
Langkah-langkah :
- apply wireshark filter expression `http contains "monta"`
![gambar1](https://user-images.githubusercontent.com/70515589/191040421-450e0761-91e9-45a2-93b1-a82c0610eb1f.png)
- Klik kanan, lalu klik follow TCP Stream
![gambar2](https://user-images.githubusercontent.com/70515589/191040603-b8d0173c-3e45-4ca0-b7fc-8e51c214e680.png)
- Dapat dilihat servernya di dalamnya
![gambar3](https://user-images.githubusercontent.com/70515589/191040610-e1233765-31d7-4167-b095-8f7ead5d58e7.png)

### No 2
Ishaq sedang bingung mencari topik ta untuk semester ini , lalu ia datang ke website monta dan menemukan detail topik pada website “monta.if.its.ac.id” , judul TA apa yang dibuka oleh ishaq ? </br>
**Jawaban**: Evaluasi unjuk Kerja User Space FileSystem </br>
Langkah-langkah :
- apply wireshark filter expression `http`
![image](https://user-images.githubusercontent.com/70515589/191042533-b796d7b2-0804-4c79-91c0-60953156f304.png)
- Paket 599 terletak merupakan lanjutan dari paket 576 yang menuju link detail topik (klik kanan dan follow tcp stream)
![image](https://user-images.githubusercontent.com/70515589/191043039-7fd89d2f-451a-4107-9a75-232e6e4a9e9b.png)
-  Dari sana dapat ditemukan jawaban judul topik yang dilihat

### No 3
Filter sehingga wireshark hanya menampilkan paket yang menuju port 80!</br>
**Jawaban**: tcp.dstport == 80
![Screenshot_2022-09-19_20_10_39](https://user-images.githubusercontent.com/91010605/191045857-47788df2-27c9-41ae-b4fd-a4ecf223ec66.png)
### No 4
Filter sehingga wireshark hanya mengambil paket yang berasal dari port 21!</br>
**Jawaban**: tcp.srcport == 21
![Screenshot_2022-09-19_20_12_51](https://user-images.githubusercontent.com/91010605/191047001-accbdc45-4529-4475-85d9-0927d3d5e8b8.png)
### No 5
Filter sehingga wireshark hanya mengambil paket yang berasal dari port 443!</br>
**Jawaban**: tcp.srcport == 443
![Screenshot_2022-09-19_20_15_48](https://user-images.githubusercontent.com/91010605/191048767-d4a57e90-46c1-4662-b795-69667437597c.png)
### No 6
Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!</br>
**Jawaban**: Cara:
- Gunakan filter `http contains "lipi.go.id"` maka akan didapatkan ip dari dns tersebut yaitu 203.160.128.158
![Screenshot_2022-09-19_22_02_59](https://user-images.githubusercontent.com/91010605/191049310-059736a7-81e2-4c3f-8322-a0ab52ebd547.png)
- Selanjutnya gunakan filter `ip.dst == 203.160.128.158`
![Screenshot_2022-09-19_22_05_01](https://user-images.githubusercontent.com/91010605/191049664-2fbb07bc-b2d8-4973-aa1f-291987968912.png)
### No 7
Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!</br>
**Jawaban**: Cara:
- untuk linux gunakan command 'ifconfig' atau 'ip addr' untuk mendapatkan ip komputer kita.
![Screenshot_2022-09-19_22_08_42](https://user-images.githubusercontent.com/91010605/191050519-fb9990ab-e03b-4f21-8c9c-b8b6a7bbc90c.png)
- gunakan capture filter `src <ip komputer>` lalu eksekusi
![Screenshot_2022-09-19_22_19_14](https://user-images.githubusercontent.com/91010605/191052887-b1ba1faa-5c85-4f75-9204-017ff35b87ff.png)

### No. 8
Telusuri aliran paket dalam file .pcap yang diberikan, cari informasi berguna berupa percakapan antara dua mahasiswa terkait tindakan kecurangan pada kegiatan praktikum. Percakapan tersebut dilaporkan menggunakan protokol jaringan dengan tingkat keandalan yang tinggi dalam pertukaran datanya sehingga kalian perlu menerapkan filter dengan protokol yang tersebut.<br>
**Jawaban**: Cara:
- Gunakan display filter: `tcp`
![image](https://user-images.githubusercontent.com/100585249/191056255-1ada60d6-bdf0-471c-a287-4e1bd848c3f3.png)
- Cari paket yang berisi percakapan kecurangan mahasiswa lalu klik kanan > Follow > TCP Stream
![image](https://user-images.githubusercontent.com/100585249/191056792-d4396ced-ee30-46d3-9b9f-0c15ff63c4c2.png)
- Didapatkan teks percakapan seperti berikut.
![Screenshot (11)](https://user-images.githubusercontent.com/100585249/191056925-3e6cba8e-3988-49f0-ad54-59941f0e0f0f.png)
- Diatas kita sudah temukan bahwa percakapan terjadi antara 127.0.0.1 dan 127.0.1.1. Sehingga untuk mendapatkan semua paket percakapan mereka, kita bisa display filter: `(ip.src == 127.0.0.1 && ip.dst == 127.0.1.1) || (ip.src == 127.0.1.1 && ip.dst == 127.0.0.1)`. Kemudian, dapat kita temukan percakapan berikut.
![Screenshot (12)](https://user-images.githubusercontent.com/100585249/191057177-86454ea1-f804-4c25-ab4d-d3c61f1f201f.png)
![Screenshot (13)](https://user-images.githubusercontent.com/100585249/191057195-8b1b9190-0055-4d67-8164-1e3733a6daf1.png)

### No. 9
Terdapat laporan adanya pertukaran file yang dilakukan oleh kedua mahasiswa dalam percakapan yang diperoleh, carilah file yang dimaksud! Untuk memudahkan laporan kepada atasan, beri nama file yang ditemukan dengan format [nama_kelompok].des3 dan simpan output file dengan nama “flag.txt”.</br>
**Jawaban**: Cara:
- Dari percakapan kedua mahasiswa, didapatkan bahwa mereka akan mengirim file lewat port 9002. Kita gunakan display filter:
`tcp.port == 9002`
![Screenshot (16)](https://user-images.githubusercontent.com/100585249/191057508-8e9dd31f-c13c-45b7-8f6d-dd455bd85bf1.png)
- Lalu kita pilih paket yang berisi file salt nya > klik kanan > Follow > TCP Stream
![Screenshot (17)](https://user-images.githubusercontent.com/100585249/191057686-d22b0811-ba52-4edf-b57c-403a2c5a0dc7.png)
- Didapatkan text berikut.
![Screenshot (18)](https://user-images.githubusercontent.com/100585249/191057729-63760c11-b7e6-4f64-8b33-17f0ea2c8231.png)
- Kemudian, kita ubah Show data as dari ASCII menjadi RAW.
![Screenshot (19)](https://user-images.githubusercontent.com/100585249/191057758-aae4ced4-6893-499c-88e3-094e273620bc.png)
- Lalu kita Save As dan beri nama “B05.des3”
![Screenshot (22)](https://user-images.githubusercontent.com/100585249/191057895-186c8794-5318-4ca6-9e78-9c15939b5ebf.png)
- Kemudian kita decrypt menggunakan OpenSSL dengan method des3 menggunakan password “nakano” yang kita dapatkan dari clue percakapan mahasiswa.
![Screenshot (24)](https://user-images.githubusercontent.com/100585249/191057910-8233ee3a-7f2e-4ee6-a7c7-8182cc30e2ca.png)
- Didapatkan file output hasil dekripsi flag.txt sebagai berikut.
![Screenshot (25)](https://user-images.githubusercontent.com/100585249/191057970-898ee3c1-5222-4736-9155-b870854e3366.png)
![Screenshot (26)](https://user-images.githubusercontent.com/100585249/191057992-eec5418e-6b0a-407f-956b-dfd9cbaffcf0.png)

### No. 10
Temukan password rahasia (flag) dari organisasi bawah tanah yang disebutkan di atas!</br>
**Jawaban**: Cara:
- Password rahasia adalah `JaRkOm2022{8uK4N_CtF_k0k_h3h3h3}` dimana password ini berada di dalam file flag.txt sebagai berikut.
![Screenshot (26)](https://user-images.githubusercontent.com/100585249/191058247-25b8465f-0039-40bb-b9af-335135162de4.png)
