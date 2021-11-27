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

## VLSM dengan CPT (Cisco Packet Tracer)

   - Pembuatan topologi baru
   
     <img src="https://user-images.githubusercontent.com/37539546/143675534-6799685d-091e-4f80-8778-8ba6d0306f7b.PNG" width="600">

   - ***Subnetting*** dan ***routing***
   
     ### A2
     
     - Atur IP pada *interface* **FOOSHA** yang mengarah ke *client* **BLUENO** dengan `10.3.8.1` dan *subnet mask* `255.255.252.0`.
     
       <img src="https://user-images.githubusercontent.com/37539546/143676218-8bebdc9d-07a9-4688-a5f7-179aae1b5124.JPG" width="600">
     
     - Atur IP pada *client* **BLUENO** yang mengarah ke **FOOSHA** dengan `10.3.8.2` dan *subnet mask* `255.255.252.0` serta *default gateway* `10.3.8.1`.

       <img src="https://user-images.githubusercontent.com/37539546/143676410-6de5336b-9b03-4044-aa40-fef1ddbae61d.JPG" width="600">
       
     ### A14
     
     - Atur IP pada *interface* **FOOSHA** yang mengarah ke *client* **DORIKI** dengan `10.3.27.161` dan *subnet mask* `255.255.255.252`.

       <img src="https://user-images.githubusercontent.com/37539546/143676488-d7aa10c3-f7d3-4e5d-bebe-3d7b08d458fe.JPG" width="600">
     
     - Atur IP pada *client* **DORIKI** yang mengarah ke **FOOSHA** dengan `10.3.27.162` dan *subnet mask* `255.255.255.252` serta *default gateway* `10.3.27.161`.

       <img src="https://user-images.githubusercontent.com/37539546/143676531-30c8fb9e-1dd1-4604-b814-77552bb3360b.JPG" width="600">
   
     ### A12
     
     - Atur IP pada *interface* **FOOSHA** yang mengarah ke *router* **GUANHAO** dengan `10.3.27.153` dan *subnet mask* `255.255.255.252`.

       <img src="https://user-images.githubusercontent.com/37539546/143676650-3f2da1c2-43f5-4ee5-913b-1f909a76bcd2.JPG" width="600">
     
     - Atur IP pada *interface* **GUANHAO** yang mengarah ke *router* **FOOSHA** dengan `10.3.27.154` dan *subnet mask* `255.255.255.252`.

       <img src="https://user-images.githubusercontent.com/37539546/143676700-325bb260-2466-4519-92e9-fad63d304343.JPG" width="600">
       
     - Tambahkan *default routing* yang mengarah ke **FOOSHA** pada *client* **GUANHAO**.

       <img src="https://user-images.githubusercontent.com/37539546/143676835-d2e747ce-1212-4da1-bb5c-adb382cbe5c6.JPG" width="600">
       
     ### A5
     
     - Atur IP pada *interface* **GUANHAO** yang mengarah ke *client* **JABRA** dengan `10.3.16.1` dan *subnet mask* `255.255.252.0`.

       <img src="https://user-images.githubusercontent.com/37539546/143676964-fdf8eae9-ac50-4faf-8650-309725d7f5b2.JPG" width="600">
     
     - Atur IP pada *client* **JABRA** yang mengarah ke **GUANHAO** dengan `10.3.16.2` dan *subnet mask* `255.255.252.0` serta *default gateway* `10.3.16.1`.

       <img src="https://user-images.githubusercontent.com/37539546/143677001-9502419b-18e1-41b4-9434-7ffa113e45f3.JPG" width="600">
       
     - Tambahkan *static routing* yang menuju jaringan yang digunakan *client* **JABRA** melalui *router* **GUANHAO** pada **FOOSHA**.

       <img src="https://user-images.githubusercontent.com/37539546/143677127-95f3a0d1-5ec7-4b94-b089-271509878c38.JPG" width="600">
       
     ### A6
     
     - Atur IP pada *interface* **GUANHAO** yang mengarah ke *client* **MAINGATE** dengan `10.3.24.1` dan *subnet mask* `255.255.254.0`.

       <img src="https://user-images.githubusercontent.com/37539546/143677174-6008dc8e-c89d-4b92-8674-b64fbd2096b3.JPG" width="600">

     - Atur IP pada *client* **MAINGATE** yang mengarah ke **GUANHAO** dengan `10.3.24.2` dan *subnet mask* `255.255.254.0` serta *default gateway* `10.3.24.1`.

       <img src="https://user-images.githubusercontent.com/37539546/143677213-2e98e1fe-f977-4c0b-9cf5-3c1fe767dc10.JPG" width="600">
       
     - Tambahkan *static routing* yang menuju jaringan yang digunakan *client* **MAINGATE** melalui *router* **GUANHAO** pada **FOOSHA**.

       <img src="https://user-images.githubusercontent.com/37539546/143677269-678625ff-0697-4884-8737-abd7e889c040.JPG" width="600">
       
     - Atur IP pada *interface* **ALABASTA** yang mengarah ke *router* **GUANHAO** dengan `10.3.24.3` dan *subnet mask* `255.255.254.0`.

       <img src="https://user-images.githubusercontent.com/37539546/143677321-cf2e0fb3-e912-4de0-9a44-3f002b9b1a48.JPG" width="600">
     
     - Tambahkan *default routing* yang mengarah ke **GUANHAO** pada *router* **ALABASTA**.

       <img src="https://user-images.githubusercontent.com/37539546/143677363-d6258334-e439-4f18-92e9-4e7f4fb03f89.JPG" width="600">
       
     ### A9
     
     - Atur IP pada *interface* **ALABASTA** yang mengarah ke *client* **JORGE** dengan `10.3.27.129` dan *subnet mask* `255.255.255.240`.

       <img src="https://user-images.githubusercontent.com/37539546/143677413-ea09f100-1fd9-4009-ab31-5833cc16b25e.JPG" width="600">

     - Atur IP pada *client* **JORGE** yang mengarah ke **ALABASTA** dengan `10.3.27.130` dan *subnet mask* `255.255.255.240` serta *default gateway* `10.3.27.129`.

       <img src="https://user-images.githubusercontent.com/37539546/143677458-7815aa2a-9af1-4ded-bc67-b9ca7a6a20df.JPG" width="600">

     - Tambahkan *static routing* yang menuju jaringan yang digunakan *client* **JORGE** melalui *router* **ALABASTA** pada **GUANHAO**.

       <img src="https://user-images.githubusercontent.com/37539546/143677499-9dfcd99a-d6da-4f68-8138-f4f97774a2df.JPG" width="600">

     - Tambahkan *static routing* yang menuju jaringan yang digunakan *client* **JORGE** melalui *router* **GUANHAO** pada **FOOSHA**.

       <img src="https://user-images.githubusercontent.com/37539546/143677562-82797495-aff0-496f-a7ad-d1d62f5491ec.JPG" width="600">

     ### A13
     
     - Atur IP pada *interface* **GUANHAO** yang mengarah ke *router* **OIMO** dengan `10.3.27.157` dan *subnet mask* `255.255.255.252`.

       <img src="https://user-images.githubusercontent.com/37539546/143677590-3c4f1c6c-30c4-4318-b422-f57efb546a2e.JPG" width="600">

     - Atur IP pada *interface* **OIMO** yang mengarah ke *router* **GUANHAO** dengan `10.3.27.158` dan *subnet mask* `255.255.255.252`.

       <img src="https://user-images.githubusercontent.com/37539546/143677624-ea5bdeec-9b92-45da-91b2-6b30eb3aba65.JPG" width="600">

     - Tambahkan *static routing* yang menuju jaringan yang digunakan **OIMO** melalui *router* **GUANHAO** pada **FOOSHA**.

       <img src="https://user-images.githubusercontent.com/37539546/143677758-02b24649-8f94-4483-8f06-16ac3e77eafa.JPG" width="600">
     
     - Tambahkan *default routing* yang mengarah ke **GUANHAO** pada *router* **OIMO**.

       <img src="https://user-images.githubusercontent.com/37539546/143677698-6dcbc073-34f3-4f03-b1d2-e2dddcfc8485.JPG" width="600">

## Kendala
