# Membuat Proyek Firebase Baru

Pada sesi ini kita akan membuat proyek baru pada firebase, yang nantinya akan
digunakan untuk menyimpan data pada Firebase Realtime Database.

#### Membuat Akun Firebase

1. Buka `firebase.google.com`
2. Pada pojok kanan atas, klik `Sign In`

   <center><img src="assets/images/firebase_setup_1.png" alt="expo client"
   width="800"/></center>

3. **Sign In** menggunakan akun atau email **Google**

   <center><img src="assets/images/firebase_setup_2.png" alt="expo client"
   width="500"/></center>

#### Membuat Proyek Baru

1. Pada laman awal firebase, klik `Get Started` atau pada pojok kanan atas klik
   `Go to console`
2. Pada laman _console_ firebase, pilih `Add Project`
3. Di kolom **Project Name**, masukkan nama aplikasi, misal `AplikasiIoT`, Pada
   kolom **Analytics location** pilih `Indonesia`. Pada kolom **Cloud Firestore location**
   biarkan _default_. Centang kedua _checkbox_ di bawah, kemudian klik
   **Create Project**.

   <center><img src="assets/images/firebase_setup_3.png" alt="expo client"
   width="500"/></center>

4. Tunggu hingga proses selesai. Kemudian klik **Continue**

   <center><img src="assets/images/firebase_setup_4.png" alt="expo client"
   width="500"/></center>

#### Mempersiapkan Realtime Database untuk Android

1. Pada sisi kiri dashboard firebase, klik **Database** di bagian **Develop**

   <center><img src="assets/images/firebase_setup_10.png" alt="expo client"
   width="300"/></center>

2. Scroll ke bawah, pada bagian **Realtime Database**, klik **Create database**

   <center><img src="assets/images/firebase_setup_11.png" alt="expo client"
   width="800"/></center>

3. Pilih `Start in test mode`, lalu tekan **Enable**, nanti dashboard **Realtime Database** akan terbuka.

   <center><img src="assets/images/firebase_setup_12.png" alt="expo client"
   width="500"/></center>

4. Arahkan cursor ke database, lalu klik `add child` dengan icon `+`

   <center><img src="assets/images/firebase_setup_14.png" alt="expo client"
   width="500"/></center>

5. Masukkan `lampu` pada kolom **Name** dan nilai `0` pada kolom **Value**,
   klik **Add**

   <center><img src="assets/images/firebase_setup_15.png" alt="expo client"
   width="500"/></center>

6. Sehingga menjadi seperti ini.

   <center><img src="assets/images/firebase_setup_16.png" alt="expo client"
   width="300"/></center>

---

Dengan dibuatnya database di Firebase Realtime Database, kita sudah bisa
mengggunakan database tersebut untuk menyimpan dan mengolah data.
[Selanjutnya](android_expo_create_project.md)
