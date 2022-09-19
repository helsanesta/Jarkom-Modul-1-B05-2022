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
![Screenshot_2022-09-19_22_09_44](https://user-images.githubusercontent.com/91010605/191050757-9bcc8103-61c6-411e-a0c7-c931e280168e.png)


