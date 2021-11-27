# Jarkom Modul 4 A08 - 2021

Anggota:
-   05111940000030 - Bunga Fairuz Wijdan
-   05111940000062 - Thomas Felix Brilliant
-   05111940000145 - Ikhlasul Amal Rivel

## Narasi Soal

<img src="https://lh5.googleusercontent.com/0IOaR7ZqbM_H8M800OlsO1WCFDM_xrhOcm5QMxacXDO6aJNIwZ9qhqixeiuxImnkNSCUZ7K6g-NS8p041lnuxwKK4UUHQQ_y9f2Yehwyh_S2TaY9qvUHbQv0ABazS5mJDA" width=600>

1. Soal *shift* dikerjakan pada **Cisco Packet Tracer** dan **GNS3** menggunakan metode perhitungan **CLASSLESS** yang berbeda.  
   Keterangan: Bila di **CPT** menggunakan **VLSM**, maka di **GNS3** menggunakan **CIDR** atau sebaliknya.
    
2. Jika tidak ada pemberitahuan revisi soal dari asisten, berarti semua soal **BERSIFAT BENAR** dan **DAPAT DIKERJAKAN**.
    
3. Untuk di GNS3, **CLOUD** merupakan **NAT1** jadi jangan sampai salah agar bisa terkoneksi internet.
    
4. Pembagian IP menggunakan *prefix* IP yang telah ditentukan pada modul pengenalan.
    
5. Pembagian IP dan routing harus **SEEFISIEN MUNGKIN**.
    
6. Pastikan semua *node* pada GNS3 dapat melakukan ping ke [its.ac.id](https://its.ac.id/).

## Jawaban

## VLSM (*Variable Length Subnet Masking*)
   - Pembagian *subnet* (*subnetting*) terhadap topologi
   
     <img src="https://user-images.githubusercontent.com/37539546/143672703-dbf1b3bb-e751-4f41-9968-23b8c2f0fe2e.jpg" width=600>
     
   - Penentuan jumlah alamat IP yang dibutuhkan tiap *subnet* dan ***labelling netmask*** berdasarkan jumlah IP. Berdasarkan hasil perhitungan, maka menggunakan *length* **/19** untuk *netmask*-nya.

     <img src="https://user-images.githubusercontent.com/37539546/143673581-c3b71258-157c-497f-9240-83a9872f2b0b.JPG" width=400>
     
   - Pembuatan ***tree subnet*** untuk nantinya membagi IP berdasarkan **NID** dan ***netmask***-nya.

     <img src="https://user-images.githubusercontent.com/37539546/143674197-342c0c60-1672-4f81-b63f-11221ed02bce.jpg" width=600>
     
   - Pembagian IP dan *netmask* dengan tabel berdasarkan ***tree subnet*** yang sudah dibuat.

     <img src="https://user-images.githubusercontent.com/37539546/143675108-0302f015-fb50-4034-9625-eecda124599e.png" width=550>

## CIDR (*Classless Inter Domain Routing*)
   - Pembagian *subnet* (*subnetting*) terhadap topologi
 
     <img src="https://user-images.githubusercontent.com/37539546/143672768-fb805831-4b2d-4d52-9e17-f7b4471d7eb6.jpg" width=600>

   - Penggabungan *subnet* paling bawah dalam topologi. Paling bawah di sini berarti paling jauh dari **internet** (*cloud*). Sebagai contoh di bawah **A7 dan A3** digabungkan menjadi **B1**, **A8 dan A1** digabungkan menjadi **B2**, **A6 dan A9** digabungkan menjadi **B3**. *Subnet* yang digabung tersebut akan membentuk sebuah *subnet* lebih besar dari *subnet*-*subnet* kecil yang ada di dalamnya. Penggabungan dilakukan terus sampai mencakup 1 topologi yang dimiliki.
   - Untuk penentuan *netmask* per *subnet*, didapat dari *netmask* yang 1 tingkat di atas *subnet* **terbesar** yang digabungkan. Sebagai contoh **A8 dan A1** jika digabung, *netmask* terbesarnya adalah **/21**, maka *netmask* untuk *subnet* **B2** adalah **/20** karena setingkat di atasnya.
   
     <img src="https://user-images.githubusercontent.com/37539546/143674871-b4465431-406f-4736-b1f4-20c3633906aa.jpg" width=600>
     
     <img src="https://user-images.githubusercontent.com/37539546/143674897-b0859820-a632-451b-9289-c37b8bf9c73b.jpg" width=600>
     
     <img src="https://user-images.githubusercontent.com/37539546/143674900-a0d88644-a3f8-480c-87b4-8414e273c8bd.jpg" width=600>
     
     <img src="https://user-images.githubusercontent.com/37539546/143674903-05c738e9-d1cf-40ee-9409-2c8eaf3b5003.jpg" width=600>
     
     <img src="https://user-images.githubusercontent.com/37539546/143674904-7deac825-a224-4a75-8a5f-5fb61c71e08d.jpg" width=600>
     
     <img src="https://user-images.githubusercontent.com/37539546/143674906-f40dddb9-fb1c-44af-a0a8-56bafc2b839d.jpg" width=600>
     
     <img src="https://user-images.githubusercontent.com/37539546/143674908-d65b21e7-53b2-4eef-b61b-ade55721a5fe.jpg" width=600>
     
   - Pembuatan ***tree subnet*** untuk nantinya membagi IP berdasarkan **NID** dan ***netmask***-nya.

     <img src="https://user-images.githubusercontent.com/37539546/143674982-a00981c2-938e-4d03-85ed-2b15fbe09d14.jpg" width=600>

   - Pembagian IP dan *netmask* dengan tabel berdasarkan ***tree subnet*** yang sudah dibuat.

     <img src="https://user-images.githubusercontent.com/37539546/143675114-055a2367-1895-4862-9d34-88bbeb95a3de.png" width=550>

## Kendala
