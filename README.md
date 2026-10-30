# DevBoard

**Collaborative Task Management Application**

DevBoard merupakan project pengembangan aplikasi manajemen tugas sederhana yang dibuat sebagai media pembelajaran dan simulasi kolaborasi pengembangan software menggunakan Git dan GitHub.

Project ini dirancang untuk mempraktikkan workflow pengembangan software secara tim, mulai dari pengelolaan repository, branching, remote repository, commit, push, pull, Pull Request, Code Review, Merge, hingga penyelesaian Merge Conflict.

Meskipun dikerjakan menggunakan satu perangkat, project ini mensimulasikan lingkungan kerja dengan tiga developer yang memiliki akun GitHub, identitas Git, dan direktori kerja masing-masing.

---

## 1. Project Overview

### Project Information

| Informasi | Keterangan |
|---|---|
| Project Name | DevBoard |
| Project Type | Task Management Application |
| Repository | `alfrzimhmd/devboard` |
| Platform | Web Application |
| Development | Collaborative Development |
| Version Control | Git |
| Remote Repository | GitHub |
| Main Language | HTML, CSS, JavaScript |
| Repository Visibility | Private |

### Project Description

DevBoard adalah aplikasi sederhana untuk membantu pengguna mengelola pekerjaan dan aktivitas pengembangan software.

Aplikasi ini menyediakan fitur pengelolaan tugas, kategori, status pekerjaan, serta dashboard untuk menampilkan ringkasan aktivitas.

Project dikembangkan secara kolaboratif dengan menerapkan sistem pembagian tugas berdasarkan fitur (*Feature-Based Development*).

### Project Objectives

Tujuan utama project:

1. Memahami konsep Git dan GitHub secara mendalam.
2. Mempelajari pengelolaan repository lokal dan remote.
3. Memahami penggunaan branch dalam pengembangan software.
4. Mempraktikkan kolaborasi menggunakan beberapa akun GitHub.
5. Mempelajari Pull Request dan Code Review.
6. Memahami proses Merge dan penyelesaian Merge Conflict.
7. Menerapkan workflow pengembangan software yang terstruktur.
8. Memahami pengelolaan riwayat perubahan kode menggunakan Git.

---

## 2. Team Members & Responsibilities

Project ini menggunakan tiga akun GitHub dengan peran dan tanggung jawab yang berbeda.

### 2.1 Project Owner

| Informasi | Keterangan |
|---|---|
| GitHub Username | `alfrzimhmd` |
| SSH Alias | `github.com` |
| SSH Key | `id_ed25519` |
| Role | Project Owner / Maintainer |

**Responsibilities:**

- Membuat dan mengelola repository utama.
- Mengatur struktur dan konfigurasi project.
- Mengelola branch utama dan branch integrasi.
- Mengatur akses collaborator.
- Melakukan pemeriksaan terhadap Pull Request.
- Melakukan Code Review.
- Menyetujui dan melakukan Merge.
- Menjaga konsistensi dan kualitas kode.
- Mengelola dokumentasi project.

### 2.2 Developer A

| Informasi | Keterangan |
|---|---|
| GitHub Username | `studymate-dev` |
| SSH Alias | `studymate` |
| SSH Key | `id_ed25519_studymate` |
| Role | Frontend Developer |

**Responsibilities:**

- Mengembangkan halaman Dashboard.
- Membuat komponen navigasi.
- Mengembangkan tampilan antarmuka aplikasi.
- Mengelola stylesheet dan komponen frontend.
- Memastikan tampilan aplikasi konsisten dan responsif.

### 2.3 Developer B

| Informasi | Keterangan |
|---|---|
| GitHub Username | `tekekid` |
| SSH Alias | `tekekid` |
| SSH Key | `id_ed25519_tekekid` |
| Role | Feature Developer |

**Responsibilities:**

- Mengembangkan fitur Task Management.
- Membuat fungsi tambah, edit, dan hapus tugas (CRUD).
- Mengembangkan kategori tugas.
- Mengelola status dan prioritas pekerjaan.
- Mengembangkan logika aplikasi menggunakan JavaScript.

---

## 3. Development Environment

Project dikembangkan menggunakan satu perangkat dengan tiga direktori kerja terpisah.

### Directory Structure

```text
GitHub-Team-Learning/
│
├── owner/
│   └── devboard/
│
├── developer-studymate/
│   └── devboard/
│
└── developer-tekekid/
    └── devboard/
```

### Working Directory

| Directory | GitHub Account | Role |
|---|---|---|
| `owner/devboard` | alfrzimhmd | Owner |
| `developer-studymate/devboard` | studymate-dev | Developer A |
| `developer-tekekid/devboard` | tekekid | Developer B |

**Important:**

Ketiga direktori merupakan hasil clone dari repository GitHub yang sama.

Setiap direktori mempunyai working tree dan riwayat perubahan lokal sendiri.

Perubahan pada satu direktori tidak otomatis diterapkan pada direktori lainnya. Sinkronisasi dilakukan melalui remote repository menggunakan Git.

---

## 4. Branching Strategy

DevBoard menggunakan pendekatan Feature Branch Workflow dengan dua branch utama dan beberapa branch pengembangan fitur.

### Branch Structure

```text
main
 │
 └── develop
      │
      ├── feature/dashboard
      │
      ├── feature/navigation
      │
      ├── feature/task-management
      │
      └── feature/task-category
```

### 4.1 Main Branch

`main` merupakan branch utama yang berisi kode stabil dan siap digunakan.

Rules:

- Tidak melakukan pengembangan fitur secara langsung.
- Tidak melakukan commit langsung dari developer.
- Perubahan harus melalui Pull Request.
- Hanya perubahan yang sudah diperiksa dan disetujui yang dapat digabungkan.

### 4.2 Develop Branch

`develop` merupakan branch integrasi untuk menggabungkan fitur-fitur yang telah dikembangkan.

Rules:

- Menjadi sumber pembuatan feature branch.
- Menjadi target Pull Request untuk pengembangan fitur.
- Harus diperbarui sebelum memulai pekerjaan baru.
- Perubahan harus melalui proses pemeriksaan.

### 4.3 Feature Branch

Feature branch digunakan untuk mengembangkan fitur tertentu secara terpisah.

Format penamaan:

```text
feature/nama-fitur
```

Contoh:

```text
feature/dashboard
feature/navigation
feature/task-management
feature/task-category
feature/user-profile
```

Rules:

- Setiap fitur harus mempunyai branch sendiri.
- Branch dibuat dari `develop`.
- Tidak mengerjakan fitur berbeda dalam satu branch.
- Setelah selesai, ajukan Pull Request ke `develop`.
- Branch dapat dihapus setelah berhasil di-merge.

### 4.4 Bugfix Branch

Digunakan untuk memperbaiki kesalahan atau bug.

Format:

```text
bugfix/nama-perbaikan
```

Contoh:

```text
bugfix/dashboard-layout
bugfix/task-validation
```

### 4.5 Hotfix Branch

Digunakan untuk memperbaiki masalah penting pada versi stabil yang berada di `main`.

Format:

```text
hotfix/nama-perbaikan
```

Contoh:

```text
hotfix/critical-error
```

---

## 5. Git Collaboration Rules

Seluruh anggota wajib mengikuti aturan kolaborasi berikut.

### 5.1 General Rules

1. Jangan melakukan pengembangan langsung pada branch `main`.
2. Gunakan branch terpisah untuk setiap fitur.
3. Selalu lakukan sinkronisasi sebelum memulai pekerjaan.
4. Gunakan commit message yang jelas dan deskriptif.
5. Jangan mengunggah file yang tidak diperlukan.
6. Jangan menghapus atau mengubah pekerjaan developer lain tanpa koordinasi.
7. Jangan melakukan force push pada branch bersama.
8. Periksa perubahan sebelum melakukan commit.
9. Gunakan Pull Request untuk menggabungkan perubahan.
10. Pastikan kode dapat berjalan sebelum mengajukan Pull Request.

### 5.2 Commit Message Convention

Gunakan format:

```text
<type>: <description>
```

Jenis commit:

| Type | Keterangan |
|---|---|
| `feat` | Menambahkan fitur baru |
| `fix` | Memperbaiki bug |
| `docs` | Mengubah dokumentasi |
| `style` | Perubahan format atau tampilan kode tanpa mengubah fungsi |
| `refactor` | Merapikan struktur kode |
| `test` | Menambahkan atau memperbaiki pengujian |
| `chore` | Pemeliharaan konfigurasi project |

Contoh:

```bash
git commit -m "feat: add dashboard layout"
git commit -m "feat: implement task management"
git commit -m "fix: resolve task validation"
git commit -m "docs: update project README"
git commit -m "refactor: improve navigation component"
```

### 5.3 Pull Request Rules

Setiap Pull Request harus:

- Memiliki judul yang jelas.
- Menjelaskan perubahan yang dilakukan.
- Menyebutkan fitur atau masalah yang dikerjakan.
- Tidak mengandung perubahan yang tidak berkaitan.
- Memastikan tidak terdapat konflik dengan branch tujuan.

Alur Pull Request:

```text
Feature Branch
      |
      v
Create Pull Request
      |
      v
Code Review
      |
      v
Approval
      |
      v
Merge into Develop
      |
      v
Delete Feature Branch
```

### 5.4 Merge Conflict Rules

Apabila terjadi Merge Conflict:

1. Jangan langsung menghapus perubahan developer lain.
2. Periksa file yang mengalami konflik.
3. Identifikasi perubahan dari masing-masing branch.
4. Diskusikan atau tentukan hasil penggabungan.
5. Selesaikan konflik secara manual.
6. Jalankan pengujian kembali.
7. Lakukan commit setelah konflik terselesaikan.

---

## 6. Standard Development Workflow

Setiap developer wajib mengikuti alur kerja berikut.

### Step 1: Clone Repository

Clone repository menggunakan SSH alias masing-masing.

**Owner:**

```bash
git clone git@github.com:alfrzimhmd/devboard.git
```

**Developer A:**

```bash
git clone git@studymate:alfrzimhmd/devboard.git
```

**Developer B:**

```bash
git clone git@tekekid:alfrzimhmd/devboard.git
```

### Step 2: Configure Git Identity

Atur identitas Git secara lokal pada setiap repository.

**Owner:**

```bash
git config user.name "alfrzimhmd"
git config user.email "mhmdalfrzi.03@gmail.com"
```

**Developer A:**

```bash
git config user.name "studymate-dev"
git config user.email "studymate@gmail.com"
```

**Developer B:**

```bash
git config user.name "tekekid"
git config user.email "tekekid22@gmail.com"
```

Pengaturan ini berlaku hanya untuk repository yang sedang digunakan dan tidak mengubah konfigurasi Git global.

### Step 3: Synchronize Repository

Sebelum mengembangkan fitur:

```bash
git switch develop
git pull origin develop
```

### Step 4: Create Feature Branch

Contoh Developer A:

```bash
git switch -c feature/dashboard
```

Contoh Developer B:

```bash
git switch -c feature/task-management
```

### Step 5: Develop and Commit

Setelah melakukan perubahan:

```bash
git status
git add .
git commit -m "feat: add dashboard layout"
```

### Step 6: Push Feature Branch

```bash
git push -u origin feature/dashboard
```

Sesuaikan nama branch dengan fitur yang dikerjakan.

### Step 7: Create Pull Request

Buat Pull Request melalui GitHub dengan ketentuan:

```text
Base Branch: develop
Compare Branch: feature/dashboard
```

### Step 8: Review and Merge

Owner melakukan pemeriksaan kode, memberikan masukan jika diperlukan, kemudian melakukan Merge apabila perubahan sudah sesuai.

### Step 9: Update Local Repository

Setelah Pull Request berhasil di-merge:

```bash
git switch develop
git pull origin develop
```

Developer dapat menghapus branch lokal yang sudah tidak diperlukan:

```bash
git branch -d feature/dashboard
```

---

## 7. Git Commands Reference

Bagian ini berisi perintah Git yang umum digunakan selama pengembangan project.

### 7.1 Repository Initialization

| Command | Function |
|---|---|
| `git init` | Membuat repository Git lokal |
| `git clone <url>` | Mengunduh repository remote ke lokal |
| `git status` | Melihat status perubahan file |
| `git log` | Melihat riwayat commit |
| `git log --oneline` | Melihat riwayat commit secara ringkas |

### 7.2 Git Configuration

| Command | Function |
|---|---|
| `git config --global user.name "Name"` | Mengatur nama global |
| `git config --global user.email "Email"` | Mengatur email global |
| `git config user.name "Name"` | Mengatur nama lokal repository |
| `git config user.email "Email"` | Mengatur email lokal repository |
| `git config --list` | Melihat konfigurasi Git |

### 7.3 Staging and Commit

| Command | Function |
|---|---|
| `git add <file>` | Menambahkan file tertentu ke staging |
| `git add .` | Menambahkan perubahan di direktori kerja ke staging |
| `git commit -m "message"` | Menyimpan perubahan sebagai commit |
| `git commit --amend` | Mengubah commit terakhir |
| `git diff` | Melihat perubahan yang belum di-stage |
| `git diff --staged` | Melihat perubahan yang sudah di-stage |

### 7.4 Branch Management

| Command | Function |
|---|---|
| `git branch` | Melihat daftar branch lokal |
| `git branch -a` | Melihat seluruh branch lokal dan remote-tracking |
| `git branch <name>` | Membuat branch baru |
| `git switch <branch>` | Berpindah branch |
| `git switch -c <branch>` | Membuat sekaligus berpindah branch |
| `git branch -d <branch>` | Menghapus branch lokal yang sudah ter-merge |
| `git branch -m <new-name>` | Mengganti nama branch |

### 7.5 Remote Repository Commands

Remote merupakan referensi menuju repository yang berada di server seperti GitHub.

| Command | Function |
|---|---|
| `git remote` | Melihat nama remote |
| `git remote -v` | Melihat nama remote beserta URL fetch dan push |
| `git remote add origin <url>` | Menambahkan remote bernama origin |
| `git remote remove origin` | Menghapus konfigurasi remote origin lokal |
| `git remote rename origin upstream` | Mengganti nama remote |
| `git remote set-url origin <url>` | Mengubah URL remote |
| `git remote show origin` | Melihat informasi remote secara detail |
| `git ls-remote origin` | Melihat referensi branch dan tag pada remote |
| `git remote prune origin` | Membersihkan remote-tracking branch yang sudah tidak ada di remote |

**Important:** Menghapus remote menggunakan `git remote remove` tidak menghapus repository di GitHub. Perintah tersebut hanya menghapus referensi remote dari konfigurasi repository lokal.

### 7.6 Push and Pull

| Command | Function |
|---|---|
| `git push` | Mengirim commit ke remote |
| `git push origin <branch>` | Mengirim branch tertentu ke remote |
| `git push -u origin <branch>` | Push sekaligus mengatur upstream |
| `git pull` | Mengambil dan mengintegrasikan perubahan dari remote |
| `git pull origin <branch>` | Mengambil perubahan dari branch remote tertentu |
| `git fetch` | Mengambil informasi dan commit terbaru tanpa mengintegrasikannya ke branch aktif |
| `git fetch origin` | Mengambil pembaruan dari remote origin |
| `git fetch --all` | Mengambil pembaruan dari seluruh remote |

### 7.7 Merge and Rebase

| Command | Function |
|---|---|
| `git merge <branch>` | Menggabungkan branch ke branch aktif |
| `git merge --abort` | Membatalkan proses merge yang sedang mengalami konflik |
| `git rebase <branch>` | Memindahkan basis commit branch aktif ke branch lain |
| `git rebase --abort` | Membatalkan proses rebase |
| `git cherry-pick <commit>` | Mengambil commit tertentu ke branch aktif |

### 7.8 Stash and Reset

| Command | Function |
|---|---|
| `git stash` | Menyimpan sementara perubahan lokal |
| `git stash list` | Melihat daftar stash |
| `git stash pop` | Mengembalikan perubahan dan menghapus stash terkait |
| `git stash apply` | Mengembalikan perubahan tanpa menghapus stash |
| `git reset --soft HEAD~1` | Membatalkan commit terakhir tetapi mempertahankan staging |
| `git reset --mixed HEAD~1` | Membatalkan commit terakhir dan mengembalikan perubahan ke working tree |
| `git revert <commit>` | Membuat commit baru untuk membatalkan perubahan commit tertentu |

**Caution:** Hindari `git reset --hard` dan `git push --force` pada pekerjaan bersama karena dapat menghilangkan atau menimpa perubahan.

---

## 8. Understanding Origin and Upstream

Dalam Git, `origin` dan `upstream` merupakan nama remote yang umum digunakan.

### Origin

`origin` biasanya merupakan nama default untuk repository tempat developer melakukan clone.

Contoh:

```bash
git remote -v
```

Output:

```text
origin  git@github.com:alfrzimhmd/devboard.git (fetch)
origin  git@github.com:alfrzimhmd/devboard.git (push)
```

### Upstream

`upstream` biasanya digunakan untuk menunjuk repository sumber atau repository utama ketika developer bekerja menggunakan fork.

Contoh:

```bash
git remote add upstream git@github.com:ORIGINAL-OWNER/devboard.git
```

Melihat remote:

```bash
git remote -v
```

Mengambil pembaruan:

```bash
git fetch upstream
```

Mengintegrasikan perubahan:

```bash
git merge upstream/develop
```

**Note:** Dalam project ini, ketiga developer melakukan clone langsung dari repository utama yang sama. Oleh karena itu, mereka cukup menggunakan `origin` terlebih dahulu. Kita tidak membutuhkan `upstream` untuk workflow awal.

---

## 9. GitHub Collaboration Features

Selain Git, project ini juga menggunakan beberapa fitur GitHub.

| Feature | Function |
|---|---|
| Repository | Menyimpan source code project |
| Branches | Memisahkan jalur pengembangan |
| Pull Requests | Mengajukan perubahan kode |
| Code Review | Memeriksa perubahan kode |
| Issues | Mencatat bug dan pekerjaan |
| Discussions | Berdiskusi mengenai project |
| Projects | Mengelola tugas dan progres |
| Releases | Mengelola versi aplikasi |
| Actions | Mengotomatisasi proses pengembangan |
| Collaborators | Mengatur akses anggota project |

---

## 10. Project Directory Structure

Struktur project yang direncanakan:

```text
devboard/
│
├── index.html
│
├── assets/
│   ├── css/
│   │   └── style.css
│   │
│   ├── js/
│   │   └── app.js
│   │
│   └── images/
│
├── docs/
│   └── CONTRIBUTING.md
│
├── .gitignore
└── README.md
```

### Feature Ownership

| File / Component | Responsible Developer |
|---|---|
| Dashboard | Developer A |
| Navigation | Developer A |
| Main Stylesheet | Developer A |
| Task Management | Developer B |
| Task CRUD | Developer B |
| Task Category | Developer B |
| Project Configuration | Owner |
| README Documentation | Owner |

Perubahan pada file yang digunakan bersama harus dikoordinasikan untuk menghindari Merge Conflict.

---

## 11. Important Notes

Beberapa hal yang wajib dipahami seluruh anggota:

1. Git merupakan version control system yang digunakan untuk mengelola perubahan kode.
2. GitHub merupakan platform hosting repository Git dan menyediakan fasilitas kolaborasi.
3. Commit merupakan catatan perubahan yang tersimpan dalam riwayat Git.
4. Push mengirimkan commit lokal ke remote repository.
5. Pull mengambil dan mengintegrasikan perubahan dari remote repository.
6. Fetch mengambil pembaruan remote tanpa langsung menggabungkannya.
7. Branch digunakan untuk memisahkan pengembangan fitur.
8. Merge menggabungkan perubahan dari satu branch ke branch lainnya.
9. Pull Request merupakan mekanisme pengajuan perubahan untuk ditinjau dan digabungkan.
10. SSH digunakan untuk melakukan autentikasi dengan GitHub tanpa harus memasukkan username dan password setiap kali melakukan operasi Git.

**Security Rules:**

- Jangan membagikan SSH private key.
- Jangan mengunggah file konfigurasi rahasia.
- Jangan menyimpan token atau password dalam source code.
- Jangan melakukan commit terhadap file sensitif.
- Gunakan `.gitignore` untuk mengecualikan file yang tidak diperlukan.

---

## 12. Project Development Philosophy

DevBoard dikembangkan dengan prinsip:

- **Collaboration:** setiap developer mempunyai tanggung jawab yang jelas.
- **Consistency:** mengikuti standar penamaan branch dan commit.
- **Code Quality:** memastikan perubahan kode dapat dipahami dan dipelihara.
- **Transparency:** seluruh perubahan tercatat dalam riwayat Git.
- **Review Before Merge:** setiap perubahan diperiksa sebelum digabungkan.
- **Continuous Learning:** setiap anggota mempelajari dan memahami proses kolaborasi.

---

## 13. Learning Roadmap

Project ini juga digunakan sebagai media pembelajaran Git dan GitHub secara bertahap.

| Stage | Learning Topics | Status |
|---|---|---|
| 01 | Git Installation & Configuration | Completed |
| 02 | Multiple GitHub Accounts | Completed |
| 03 | SSH Authentication | Completed |
| 04 | Repository Setup & Clone | In Progress |
| 05 | Git Identity Management | Planned |
| 06 | Branch Management | Planned |
| 07 | Remote Repository Management | Planned |
| 08 | Push, Pull & Fetch | Planned |
| 09 | Pull Request & Code Review | Planned |
| 10 | Merge & Merge Conflict | Planned |
| 11 | Rebase & Cherry-pick | Planned |
| 12 | Advanced Git Workflow | Planned |
| 13 | GitHub Actions & Automation | Planned |

---

**DevBoard — Learn, Build, Collaborate.**

*This project is created for educational purposes and collaborative Git/GitHub workflow practice.*