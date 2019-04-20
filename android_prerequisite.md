# Android

Pada modul ini akan dijelaskan pembuatan aplikasi mobile khususnya Android menggunakan _framework cross-platform_ dari Google, yaitu **Flutter**. Modul atau dokumentasi ini seluruhnya di dapat dari [sumber asli](https://flutter.dev/docs/get-started/install/windows)

# Persyaratan Sistem

- **Sistem Operasi**: Windows 7 SP1 atau terbaru (64-bit)
- **Media Penyimpanan**: Setidaknya tersedia 400MB
- **Alat yang diperlukan** :
  - Windows Command Propmt (CMD) atau Windows PowerShell, pastinya sudah terinstall secara default.
  - Git untuk Windows, Download [disini](https://git-scm.com/download/win).

# Permulaan

#### Instalasi Chocolatey

1. Buka CMD as Administrator
2. Copy Paste kode di bawah
```
@"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command "iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"
```
3. Enter, kemudian tunggu hingga proses instalasi selesai.
4. Close CMD
5. Untuk memastikan instalasi chocolatey berhasil, buka CMD baru kemudian
   ketikan `choco --version` jika muncul versi dari chocolatey maka chocolatey
   sudah dapat digunakan.

#### Instalasi JDK

1. Buka CMD as Administrator
2. Install open JDK dengan kode di bawah
```
choco install -y jdk8
```
3. Tunggu proses instalasi selesai

#### Instalasi Flutter

1. Download Flutter [disini](https://storage.googleapis.com/flutter_infra/releases/stable/windows/flutter_windows_v1.2.1-stable.zip)
2. Ekstrak Flutter yang telah di Download ke dalam folder `C:\src\flutter` (Buat folder jika belum ada).
3. Buka folder `C:\src\flutter` yang telah berisikan berkas Flutter, lalu jalankan file `flutter_console.nat`

#### Tambah atau Perbarui Path Environment

1. Di start menu cari/ketik `env`, lalu pilih **Edit Environment variables for your account**
2. Pada bagian **User variables** cek jika disitu terdapat entry dengan nama `Path`
  - Jika ada, Tambah path ke `flutter\bin` dengan tanda `;` sebagai pemisah dari path sebelumnya.
  - Jika tidak ada, Buat **User variables** baru dengan nama `Path` dan tambahkan path ke `flutter\bin`.

#### Jalankan `Flutter Doctor`

1. Dari CMD, masuk ke folder `C:\src\Flutter`

```
C:\Users\User> cd C:\src\Flutter
```

2. Dari situ jalankan perintah

```
C:\src\Flutter> flutter doctor
```

Perintah ini dipanggil untuk melakukan tes terhadap windows dan menampilkan laporan dari status instalasi Flutter. Perhatikan secara seksama keluarannya.
contoh:

```
C:\src\Flutter> flutter doctor
[-] Android toolchain - develop for Android devices
  • Android SDK at D:\Android\sdk
  ✗ Android SDK is missing command line tools; download from https://goo.gl/XxQghQ
  • Try re-installing or updating your Android SDK,
    visit https://flutter.dev/setup/#android-setup for detailed instructions.
```

> jika terdapat silang, maka poin tersebut masih perlu diperbaiki. Misalnya pada contoh di atas menampilkan bahwa Android SDK kekurangan **Command Line Tools** 
> dan perlu didownload di link tersebut.

## Android Setup

Untuk mempermudah setup android, Flutter menyarankan untuk menginstall **Android Studio** sebagai IDE dalam pembuatan aplikasi android. Perlu diingat, bahwa 
penggunaan **Android Studio** ini opsional, namun kami menyarankan untuk mennggunakannya. Untuk penggunaan IDE lain dapat dilihat di [link berikut](https://flutter.dev/docs/get-started/editor?tab=androidstudio)

#### Install Android Studio
1. Download dan Install Android Studio [disini](https://developer.android.com/studio)
2. Jika sudah, buka Android Studio dan install beberapa tools berikut:
  - Android SDK
  - Android SDK Platform-Tools
  - Android SDK Build-Tools

#### Setup Perangkat Android
> Smartphone android yang digunakan harus diatas versi 4.1

1. Aktifkan **Developer Options** dan **USB Debugging** di Smartphone anda, untuk intruksi lebih lanjut dapat dilihat [disini](https://developer.android.com/studio/debug/dev-options).
2. Download dan Install Google USB Driver [disini](https://developer.android.com/studio/run/win-usb).
3. Menggunakan kabel USB, colokkan antara komputer dengan Smartphone, jika muncul peringatan di Smartphone tekan saja `allow`.
4. Pada terminal, seperti langkah [ini](http://localhost:3000/#/android_prerequisite?id=jalankan-flutter-doctor) jalankan perintah
```
C:\src\Flutter> flutter devices
```

#### Setup Emulator Android
> Jika tidak memungkinkan menggunakan Smartphone, pada **Android Studio** terdapat emulator sebagai pengganti Smartphone.

1. Jalankan Android Studio, **Tools>Android>AVD Manager>** pilih **Create Virtual Device**
2. Pilih definisi Android yang diinginkan, kemudian **next**
3. Pilih jenis Android yang diinginkan, kemudian **next**, direkomendasikan memilih __x86__ atau __x86_64__
4. Pada bagian Emulated Performance, pilih **Hardware - GLES 2.0**
5. Pastikan seluruh konfigurasi benar, kemudian klik **finish**
6. Untuk menjalankan **Android Emulator**, Klik **RUN** pada toolbar Android Studio

#### Install Flutter dan Dart Plugin

1. Jalankan Android Studio
2. Buka Preferences (**File > Settings > Plugins**)
3. Pilih **Browse Repositories**, pilih `Flutter` plugin dan tekan **install**
4. Tekan **Yes** untuk menginstall plugin
5. Tekan **Accept** jika muncul peringatan instalasi plugin `Dart`
6. Tekan **Restart** jika muncul


## Membuat Proyek Flutter

Untuk memulai kita akan mencoba membuat aplikasi starter dari Flutter, menggunakan **Android Studio**
1. Pilih **File > New Flutter Project**
2. Pilih **Flutter Application** sebagai tipe proyek, tekan **Next**
3. Pastikan **Flutter SDK Path** sesuai dengan direktori instalasi flutter
4. Masukkan nama proyek/aplikasi yang akan dibuat (contoh `IoTFirebaseApp`), tekan **Next**
5. Tekan **Finish**
6. Tunggu hingga proses selesai

## Menjalankan Aplikasi

1. Pada toolbar,

![toolbar-android](https://flutter.dev/assets/tools/android-studio/main-toolbar-857fe8c36d38020e27b502ec643ea8b1716edbe150cc6e39e3560f8fb7bda5b2.png)
2. Pada **target selector**, pilih perangkat android untuk menjalankan aplikasi. 
3. Tekan icon RUN di toolbar atau pada menu **Run > Run**
4. Setelah Build selesai maka pada perangkat akan terinstall aplikasi ini.

![starter-flutter](https://flutter.dev/assets/get-started/ios/starter-app-5e284e57b8dce587ea1dfdac7da616e6ec9dc263a409a9a8f99cf836340f47b8.png)

---

Dengan terinstallnya aplikasi starter di perangkat android, maka pembuatan aplikasi android untuk Internet of Things dapat dilanjutkan di halaman [ini](http://localhost:3000/#/android_coding)
