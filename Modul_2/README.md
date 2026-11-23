# Laporan Praktikum Pemrograman Web 1 - Modul 2

## Identitas Mahasiswa
* **Nama** : Auliya Nur Anisa
* **NIM** : 20250910045
* **Kelas** : SINFC-04 2025
* **Dosen Pengampu** : Dede Irawan
* **Institusi** : Fakultas Ilmu Komputer, Universitas Kuningan (2025)

---

## KATA PENGANTAR
Puji syukur kehadirat Allah SWT atas rahmat dan karunia-Nya, sehingga laporan praktikum mata kuliah Pemrograman Web 1 dengan judul "Modul 2: Git dan GitHub" ini dapat diselesaikan dengan baik dan tepat waktu.

Laporan ini disusun untuk memenuhi tugas praktikum serta sebagai sarana penyampaian pemahaman mengenai konsep dasar version control system, alur kerja Git, hingga integrasi repository lokal dengan platform GitHub. Melalui praktikum ini, penyusun dapat memahami secara langsung perintah-perintah dasar Git, pengelolaan branching, penggabungan kode (merge), serta cara berkolaborasi dan mendokumentasikan proyek perangkat lunak secara terstruktur.

Penyusun mengucapkan terima kasih kepada dosen pengampu mata kuliah serta asisten praktikum yang telah memberikan bimbingan, arahan, dan penyampaian materi selama proses kegiatan pembelajaran praktikum berlangsung. Tidak lupa ucapan terima kasih disampaikan kepada rekan-rekan mahasiswa yang telah saling mendukung dan berdiskusi selama penyusunan laporan ini.

Penyusun menyadari bahwa dalam penyusunan laporan praktikum ini masih terdapat kekurangan. Oleh karena itu, kritik dan saran yang membangun sangat diharapkan demi perbaikan dan pengembangan penyusunan laporan di masa yang akan datang. Semoga laporan ini dapat memberikan manfaat dan menambah wawasan bagi pembaca.

Kuningan, 4 November 2026

---

## DAFTAR ISI
1. [BAB I - PRETEST](#bab-i---pretest)
2. [BAB II - PEMBAHASAN](#bab-ii---pembahasan)
3. [BAB III - POSTEST](#bab-iii---postest)
4. [BAB IV - TUGAS](#bab-iv---tugas)
5. [BAB V - KESIMPULAN](#bab-v---kesimpulan)

---

## BAB I - PRETEST

**1. Apa tujuan dari menggunakan version control dalam pengembangan perangkat lunak?**  
*Jawab:* Tujuan utama penggunaan version control dalam pengembangan perangkat lunak adalah untuk melacak, mencatat, dan mengelola setiap perubahan kode sumber yang terjadi dari waktu ke waktu sehingga pengembang dapat dengan mudah kembali ke versi sebelumnya apabila terjadi kesalahan atau kegagalan sistem. Selain itu, sistem kontrol versi memfasilitasi kolaborasi tim secara simultan tanpa risiko penimpaan file yang tidak disengaja, menyediakan riwayat perubahan yang transparan, serta mengamankan dokumentasi proyek secara terstruktur.

**2. Jelaskan perbedaan antara git add dan git commit!**  
*Jawab:* Perbedaan mendasar antara git add dan git commit terletak pada tahapan alur kerja penyimpanan file di dalam Git. Perintah `git add` berfungsi untuk mendaftarkan atau memindahkan file baru maupun file yang telah dimodifikasi dari working directory ke dalam staging area sebagai persiapan sebelum direkam. Sementara itu, perintah `git commit` berfungsi untuk mengambil seluruh perubahan yang saat ini berada di dalam staging area dan menyimpannya secara permanen ke dalam riwayat repository lokal dengan menyertakan pesan deskriptif mengenai perubahan tersebut.

**3. Bagaimana cara membuat branch baru di Git?**  
*Jawab:* Cara membuat branch baru di Git dapat dilakukan dengan menggunakan perintah `git branch <nama-branch>` untuk membuat cabang baru tanpa berpindah ke sana, atau menggunakan perintah `git checkout -b <nama-branch>` maupun `git switch -c <nama-branch>` yang tidak hanya membuat cabang baru tetapi sekaligus memindahkan posisi kerja aktif langsung ke dalam cabang tersebut.

---

## BAB II - PEMBAHASAN

Pada bagian praktikum modul ini, kegiatan diawali dengan pembuatan akun GitHub secara mandiri melalui situs resmi mereka dengan melengkapi alamat email, kata sandi, nama pengguna, serta memasukkan kode verifikasi yang dikirimkan ke email untuk memastikan akun aktif dan siap digunakan dengan paket gratis. Selanjutnya, dilakukan proses instalasi perangkat lunak Git pada sistem operasi Windows dan verifikasi keberhasilannya melalui terminal Visual Studio Code menggunakan perintah `git --version`. Setelah Git terpasang, konfigurasi identitas dasar berupa nama pengguna dan alamat email diatur ke dalam sistem Git lokal. Tahap berikutnya adalah pengelolaan proyek secara lokal di mana sebuah direktori diinisialisasi sebagai repository Git menggunakan perintah `git init`, lalu file latihan dari modul sebelumnya dimasukkan ke dalam staging area menggunakan perintah `git add`, diperiksa statusnya dengan `git status`, dan direkam secara permanen ke dalam riwayat repository menggunakan perintah `git commit`. Terakhir, repository lokal tersebut dihubungkan ke remote repository di GitHub menggunakan perintah `git remote add origin`, diubah nama branch utamanya menjadi `main` dengan perintah `git branch -M main`, dan diunggah seluruh perubahannya ke server cloud GitHub menggunakan perintah `git push -u origin main` agar proyek dapat diakses secara daring dari mana saja.

---

## BAB III - POSTEST

**1. Apa fungsi dari git merge dalam workflow Git?**  
*Jawab:* Fungsi dari `git merge` dalam workflow Git adalah untuk menggabungkan riwayat perubahan atau cabang (`branch`) yang terpisah kembali ke dalam cabang utama (seperti `master` atau `main`) atau cabang target lainnya. Perintah ini memungkinkan integrasi fitur baru atau perbaikan bug yang dikerjakan secara terisolasi pada cabang berbeda agar dapat disatukan menjadi satu kesatuan proyek yang utuh.

**2. Jelaskan cara mengatasi konflik saat melakukan merge!**  
*Jawab:* Cara mengatasi konflik saat melakukan `merge` diawali dengan membuka file yang mengalami konflik untuk mengidentifikasi bagian baris kode yang bermasalah, di mana Git biasanya menandai konflik tersebut dengan teks khusus seperti tanda panah dan garis persamaan. Pengembang harus menghapus tanda penanda konflik tersebut, menentukan kode final mana yang ingin dipertahankan atau menggabungkannya secara manual, lalu menambahkan file yang telah diperbaiki tersebut kembali ke staging area menggunakan `git add`, dan terakhir menyelesaikan proses penggabungan dengan melakukan `git commit`.

**3. Tulis langkah-langkah untuk menambahkan file baru ke repository Git dan melakukan commit.**  
*Jawab:* Langkah-langkah untuk menambahkan file baru ke repository Git dan melakukan commit dimulai dengan menempatkan file baru di dalam direktori proyek lokal. Selanjutnya, buka terminal di Visual Studio Code, lalu jalankan perintah `git add <nama-file>` untuk mendaftarkan file tersebut ke dalam staging area. Setelah itu, periksa status perubahan menggunakan `git status` untuk memastikan file sudah siap, lalu akhiri dengan mengetikkan perintah `git commit -m "Pesan commit"` guna merekam perubahan tersebut secara resmi ke dalam riwayat repository lokal.

---

## BAB IV - TUGAS

**1. Buatlah repository Git untuk proyek web dan dokumentasikan proses pembuatan, commit, dan push ke GitHub.**  
*Jawab:* Pembuatan repository Git untuk proyek web dimulai dengan menginisialisasi folder proyek menggunakan perintah `git init` di terminal Visual Studio Code. Seluruh file HTML, CSS, maupun aset web yang telah dikerjakan ditambahkan ke staging area menggunakan perintah `git add .` dan direkam riwayat perubahannya melalui perintah `git commit -m "Inisialisasi dan penambahan file proyek web"`. Setelah repository lokal siap, sebuah repository kosong dibuat di akun GitHub, kemudian dihubungkan menggunakan perintah `git remote add origin <url-repository>`, diatur branch utamanya menjadi `main` dengan perintah `git branch -M main`, dan dikirimkan seluruh datanya secara daring menggunakan perintah `git push -u origin main`.

**2. Rancanglah workflow Git yang melibatkan branch untuk fitur baru dan integrasi dengan branch utama.**  
*Jawab:* Perancangan workflow Git yang melibatkan branch untuk fitur baru dimulai dari cabang utama (`main`) yang bertindak sebagai fondasi stabil proyek. Ketika pengembang ingin menambahkan fitur baru, mereka wajib membuat dan berpindah ke branch terpisah menggunakan perintah `git checkout -b feature/<nama-fitur>`, sehingga seluruh proses penulisan kode, pengujian, dan perbaikan dilakukan secara terisolasi tanpa mengganggu stabilitas kode di cabang utama. Setelah fitur selesai dikerjakan, diuji, dan di-commit, pengembang kembali ke cabang `main`, memperbarui repositorinya dengan `git pull`, lalu menjalankan perintah `git merge feature/<nama-fitur>` untuk mengintegrasikan seluruh fitur baru tersebut ke dalam cabang utama sebelum akhirnya di-push kembali ke GitHub.

**3. Simpan seluruh praktikum pada modul sebelumnya kedalam repository Git yang sudah Anda buat.**  
*Jawab:* Seluruh praktikum dan latihan dari modul-modul sebelumnya sudah disimpan ke dalam repository Git yang telah dibuat dengan cara memindahkan atau menyalin seluruh folder modul tersebut ke dalam direktori utama proyek Git lokal.

---

## BAB V - KESIMPULAN

Modul ini memberikan pemahaman mendasar mengenai pentingnya version control dalam pengembangan perangkat lunak menggunakan Git dan GitHub, mulai dari tahap instalasi perangkat lunak, konfigurasi identitas, hingga pengelolaan proyek secara lokal dan berbasis cloud. Melalui praktik yang telah dilakukan, pengembang dapat melacak setiap perubahan riwayat kode, memanfaatkan mekanisme staging area dan commit, serta mengelola percabangan (`branching`) dan penggabungan (`merge`) secara sistematis. Dengan menerapkan workflow kolaboratif ini, seluruh dokumentasi serta rangkaian file praktikum dari modul-modul sebelumnya dapat terorganisasi dengan aman, rapi, dan mudah diakses dari mana saja secara daring.