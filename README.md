# 🏃 RunMore

**RunMore** adalah aplikasi Android untuk membantu pelari dalam **mencatat aktivitas latihan lari, mengelola jadwal latihan, melihat riwayat latihan, dan memantau statistik perkembangan lari**.

Aplikasi ini dikembangkan menggunakan **Kotlin** dan **Jetpack Compose** dengan penyimpanan data lokal menggunakan **Room Database**.

---

## 📱 Tentang Aplikasi

RunMore dirancang sebagai aplikasi sederhana untuk membantu pengguna mengelola aktivitas latihan lari secara terstruktur.

Dengan RunMore, pengguna dapat:

* Membuat akun dan melakukan login.
* Mencatat aktivitas latihan lari.
* Menyimpan jarak tempuh.
* Mencatat durasi latihan.
* Mencatat pace.
* Mencatat kalori yang terbakar.
* Menambahkan catatan latihan.
* Membuat jadwal latihan.
* Menentukan target jarak dan durasi latihan.
* Melihat riwayat latihan.
* Menghapus data latihan.
* Melihat statistik perkembangan latihan.
* Melihat grafik jarak lari selama 7 hari terakhir.
* Melihat total jarak dan jumlah latihan.
* Melihat pace rata-rata.
* Melihat pace terbaik.
* Melihat jarak lari terjauh.
* Melihat total kalori yang terbakar.

---

## 🎯 Tujuan

Tujuan pengembangan RunMore adalah menyediakan aplikasi pencatatan latihan lari yang sederhana dan mudah digunakan sehingga pengguna dapat:

1. Mencatat aktivitas lari secara terorganisir.
2. Merencanakan latihan melalui jadwal latihan.
3. Mengetahui perkembangan performa lari.
4. Mengevaluasi hasil latihan berdasarkan statistik.
5. Menyimpan data latihan secara lokal pada perangkat Android.

---

## ✨ Fitur Utama

### 🔐 1. Login dan Registrasi

Pengguna dapat membuat akun dan melakukan login untuk mengakses aplikasi.

Data pengguna disimpan menggunakan Room Database.

Informasi pengguna meliputi:

* Nama
* Email
* Password

---

### 🏠 2. Dashboard / Home

Halaman utama menampilkan ringkasan aktivitas pengguna.

Informasi yang ditampilkan:

* Total jarak lari.
* Jumlah latihan.
* Pace rata-rata.
* Tombol untuk mencatat latihan.
* Tombol untuk melihat riwayat latihan.

Contoh informasi:

```text
Halo, User 👋

Tetap konsisten dan terus berlari!

Jarak       Latihan
25.5 KM     5

Pace rata-rata
6.20 min/km

[ + Catat Latihan ]

[ Lihat Riwayat ]
```

---

### 📝 3. Catat Latihan

Pengguna dapat mencatat hasil latihan lari secara manual.

Data yang dapat dimasukkan:

* Tanggal latihan
* Jarak tempuh
* Durasi
* Pace
* Kalori
* Catatan

Data latihan kemudian disimpan ke database lokal.

---

### 📅 4. Jadwal Latihan

Pengguna dapat membuat jadwal latihan lari.

Informasi jadwal meliputi:

* Tanggal latihan
* Jenis latihan
* Target jarak
* Target durasi
* Deskripsi latihan

Jenis latihan yang tersedia:

* Easy Run
* Long Run
* Tempo Run
* Interval
* Recovery Run
* Race

---

### 📚 5. Riwayat Latihan

Halaman riwayat menampilkan daftar aktivitas lari yang telah dicatat.

Informasi setiap latihan meliputi:

* Tanggal
* Jarak
* Durasi
* Pace
* Kalori
* Catatan

Pengguna juga dapat menghapus data latihan.

---

### 📊 6. Statistik

RunMore menyediakan halaman statistik untuk membantu pengguna mengevaluasi perkembangan latihan.

Statistik yang tersedia:

| Statistik      | Keterangan                           |
| -------------- | ------------------------------------ |
| Total Jarak    | Total seluruh jarak latihan          |
| Total Latihan  | Jumlah latihan yang telah dilakukan  |
| Pace Rata-rata | Rata-rata pace seluruh latihan       |
| Pace Terbaik   | Pace tercepat                        |
| Lari Terjauh   | Jarak terjauh dalam satu latihan     |
| Total Kalori   | Total kalori yang tercatat           |
| Jarak 7 Hari   | Grafik jarak latihan 7 hari terakhir |

---

## 🛠️ Teknologi yang Digunakan

RunMore dikembangkan menggunakan teknologi berikut:

| Teknologi          | Penggunaan                     |
| ------------------ | ------------------------------ |
| Kotlin             | Bahasa pemrograman utama       |
| Jetpack Compose    | Pengembangan antarmuka         |
| Material 3         | Komponen UI                    |
| Navigation Compose | Navigasi antarhalaman          |
| Room Database      | Penyimpanan data lokal         |
| KSP                | Room annotation processing     |
| ViewModel          | Pengelolaan state dan logic UI |
| Kotlin Coroutines  | Operasi asynchronous           |
| Flow               | Pengamatan perubahan data      |
| Gradle Kotlin DSL  | Konfigurasi build              |

---

## 🏗️ Arsitektur Aplikasi

Aplikasi menggunakan pendekatan pemisahan antara UI, ViewModel, Repository, dan Database.

```text
┌─────────────────────────────┐
│        Jetpack Compose      │
│             UI              │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│          ViewModel          │
│     State & Business Logic  │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│         Repository          │
│      Data Management        │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│       Room Database         │
│                             │
│ User                        │
│ RunResult                   │
│ TrainingSchedule            │
└─────────────────────────────┘
```

---

## 📂 Struktur Proyek

Struktur utama proyek RunMore:

```text
RunMore/
│
├── app/
│   └── src/
│       └── main/
│           ├── java/
│           │   └── com/
│           │       └── example/
│           │           └── runmore/
│           │               │
│           │               ├── MainActivity.kt
│           │               │
│           │               ├── data/
│           │               │   ├── AppDatabase.kt
│           │               │   ├── User.kt
│           │               │   ├── UserDao.kt
│           │               │   ├── RunResult.kt
│           │               │   ├── RunResultDao.kt
│           │               │   ├── TrainingSchedule.kt
│           │               │   ├── TrainingScheduleDao.kt
│           │               │   ├── TrainingType.kt
│           │               │   └── RunningStatistic.kt
│           │               │
│           │               ├── navigation/
│           │               │   ├── NavGraph.kt
│           │               │   └── Screen.kt
│           │               │
│           │               ├── repository/
│           │               │   └── RunMoreRepository.kt
│           │               │
│           │               ├── ui/
│           │               │   ├── AddRunScreen.kt
│           │               │   ├── AddScheduleScreen.kt
│           │               │   ├── HomeScreen.kt
│           │               │   ├── LoginScreen.kt
│           │               │   ├── MainAppScreen.kt
│           │               │   ├── ProfileScreen.kt
│           │               │   ├── RegisterScreen.kt
│           │               │   ├── RunHistoryScreen.kt
│           │               │   ├── ScheduleScreen.kt
│           │               │   ├── StatisticsScreen.kt
│           │               │   │
│           │               │   ├── components/
│           │               │   │   ├── BottomBar.kt
│           │               │   │   ├── RunningChart.kt
│           │               │   │   ├── StatisticCard.kt
│           │               │   │   └── WeeklyDistanceChart.kt
│           │               │   │
│           │               │   └── theme/
│           │               │       ├── Color.kt
│           │               │       ├── Theme.kt
│           │               │       └── Type.kt
│           │               │
│           │               ├── util/
│           │               │   ├── DateUtils.kt
│           │               │   ├── PaceUtils.kt
│           │               │   ├── ProgressUtils.kt
│           │               │   ├── StatisticsUtils.kt
│           │               │   └── WeeklyStatistics.kt
│           │               │
│           │               └── viewmodel/
│           │                   ├── AuthViewModel.kt
│           │                   ├── RunMoreViewModelFactory.kt
│           │                   ├── StatisticsViewModel.kt
│           │                   └── TrainingViewModel.kt
│           │
│           └── AndroidManifest.xml
│
├── build.gradle.kts
├── settings.gradle.kts
└── gradle/
```

---

## 🗄️ Database

RunMore menggunakan **Room Database** sebagai database lokal.

### User

Digunakan untuk menyimpan data akun pengguna.

```text
User
├── id
├── name
├── email
└── password
```

### RunResult

Digunakan untuk menyimpan hasil latihan lari.

```text
RunResult
├── id
├── userId
├── date
├── distance
├── duration
├── pace
├── calories
└── notes
```

### TrainingSchedule

Digunakan untuk menyimpan jadwal latihan.

```text
TrainingSchedule
├── id
├── userId
├── date
├── type
├── targetDistance
├── targetDuration
├── description
└── completed
```

---

## 📋 Persyaratan Sistem

Untuk menjalankan proyek ini diperlukan:

* Android Studio versi terbaru yang mendukung konfigurasi proyek.
* JDK 11 atau kompatibel dengan konfigurasi proyek.
* Android SDK.
* Android SDK Platform 37.
* Gradle.
* Emulator Android atau perangkat Android fisik.

Konfigurasi utama aplikasi:

```text
compileSdk = 37
minSdk = 24
targetSdk = 37
```

---

## 🚀 Cara Menjalankan Project

### 1. Clone atau Extract Project

Jika menggunakan file ZIP, ekstrak project:

```text
RunMore/
```

Jika menggunakan Git:

```bash
git clone <repository-url>
```

---

### 2. Buka Android Studio

Buka:

```text
Android Studio
→ Open
→ Pilih folder RunMore
```

Tunggu sampai proses **Gradle Sync** selesai.

---

### 3. Pastikan SDK Terpasang

Buka:

```text
Tools
→ SDK Manager
```

Pastikan Android SDK yang diperlukan telah tersedia.

---

### 4. Pilih Device

Gunakan:

* Android Emulator, atau
* Smartphone Android fisik.

Untuk smartphone fisik, aktifkan:

```text
Developer Options
→ USB Debugging
```

---

### 5. Jalankan Aplikasi

Klik tombol:

```text
▶ Run
```

atau gunakan:

```text
Run → Run 'app'
```

---

## 🔄 Alur Penggunaan

Alur penggunaan aplikasi:

```text
Register
   ↓
Login
   ↓
Home
   ├── Catat Latihan
   │      ↓
   │   Simpan
   │      ↓
   │   Riwayat
   │
   ├── Jadwal Latihan
   │      ↓
   │   Tambah Jadwal
   │
   ├── Statistik
   │      ↓
   │   Analisis Performa
   │
   └── Profile
          ↓
        Logout
```

---

## 🏃 Jenis Latihan

RunMore menyediakan beberapa jenis latihan:

### Easy Run

Latihan dengan intensitas ringan untuk membangun aerobic base.

### Long Run

Latihan dengan jarak lebih panjang untuk meningkatkan daya tahan.

### Tempo Run

Latihan dengan intensitas sedang hingga tinggi untuk meningkatkan kemampuan mempertahankan pace.

### Interval

Latihan dengan kombinasi lari cepat dan recovery.

### Recovery Run

Latihan ringan untuk membantu pemulihan setelah latihan berat.

### Race

Digunakan untuk mencatat atau merencanakan aktivitas perlombaan.

---

## 📈 Perhitungan Statistik

Aplikasi menggunakan data latihan yang tersimpan untuk menghitung beberapa statistik.

### Total Jarak

```text
Total Jarak = Σ Jarak setiap latihan
```

### Jumlah Latihan

```text
Total Latihan = Jumlah seluruh data latihan
```

### Pace Rata-rata

Pace dihitung berdasarkan data pace dari latihan yang telah dicatat.

### Lari Terjauh

```text
Lari Terjauh = MAX(Jarak latihan)
```

### Total Kalori

```text
Total Kalori = Σ Kalori setiap latihan
```

---

## 🎨 User Interface

Antarmuka RunMore dibuat menggunakan **Jetpack Compose** dan **Material 3**.

Halaman utama aplikasi terdiri dari:

* Login
* Register
* Home
* Jadwal Latihan
* Tambah Jadwal
* Catat Latihan
* Riwayat Latihan
* Statistik
* Profile

Navigasi utama menggunakan **Bottom Navigation**.

---

## 🔒 Penyimpanan Data

RunMore menggunakan database lokal sehingga data latihan dapat disimpan pada perangkat.

Data utama yang disimpan:

```text
User
RunResult
TrainingSchedule
```

Repository bertanggung jawab mengatur akses data antara ViewModel dan Room Database.

---

## 🧪 Pengujian

Pengujian aplikasi dapat dilakukan dengan:

### Manual Testing

Memastikan setiap fitur berjalan sesuai kebutuhan:

* Registrasi pengguna.
* Login.
* Menambahkan latihan.
* Menghapus latihan.
* Menambahkan jadwal.
* Menghapus jadwal.
* Menampilkan statistik.
* Logout.

### Build Testing

Gunakan:

```bash
./gradlew build
```

Pada Windows:

```bash
gradlew.bat build
```

Untuk membersihkan hasil build:

```bash
gradlew.bat clean
```

---

## ⚠️ Catatan

RunMore merupakan aplikasi pencatatan dan perencanaan latihan lari berbasis lokal.

Aplikasi ini **tidak menggantikan perangkat GPS atau running tracker profesional**. Data latihan dimasukkan oleh pengguna secara manual berdasarkan hasil aktivitas lari.

---

## 🔮 Pengembangan Selanjutnya

Fitur yang dapat dikembangkan pada versi berikutnya:

* GPS real-time tracking.
* Pedometer menggunakan sensor perangkat.
* Integrasi Google Maps.
* Integrasi Google Fit / Health Connect.
* Sinkronisasi cloud.
* Backup dan restore data.
* Notifikasi jadwal latihan.
* Target latihan mingguan.
* Program latihan 5K, 10K, Half Marathon, dan Marathon.
* Grafik perkembangan pace.
* Grafik perkembangan jarak.
* Heart rate tracking.
* Dark mode.
* Export data ke CSV/PDF.
* Integrasi smartwatch.

---

## 👨‍💻 Pengembang

**RunMore**

Aplikasi ini dikembangkan sebagai proyek aplikasi Android untuk pembelajaran dan pengembangan sistem pencatatan serta perencanaan latihan lari.

### Teknologi

```text
Kotlin
Jetpack Compose
Material 3
Room Database
Navigation Compose
ViewModel
Kotlin Coroutines
KSP
```

---

## 📄 Lisensi

Project ini dibuat untuk tujuan **pembelajaran, pengembangan, dan Final Project**.

---

## ⭐ RunMore

> **RunMore — Track Your Run, Plan Your Progress.**

**Catat latihan. Atur jadwal. Pantau perkembangan. Terus berlari. 🏃**
