# catatan.md 

## Perintah Dasar Git
`git init`   :  Membuat repository Git baru                        
`git status` : Melihat status perubahan file                      
`git add`    : Memasukkan perubahan ke Staging Area               
`git commit` : Menyimpan perubahan ke repository lokal            
`git push`   : Mengirim perubahan ke repository remote            
`git pull`   : Mengambil perubahan terbaru dari repository remote 
`git branch` : Melihat atau mengelola branch                      
`git switch` : Berpindah ke branch lain                           
`git merge`  : Menggabungkan perubahan dari branch lain           
`git log`    : Melihat riwayat commit                             

## Cara menggunakannya dengan tugas ini
- Buat folder lokal git-learning-journal, kemudian buka folder dan terminal di vsc
- Atur dulu identitas Git dengan git config --global user.name "nama" dan git config -- global user.email "email@gmail.com"
- Jika sudah selesai cek dengan git config --global --list
- Jadikan folder lokal sebagai Repository Git dengan git init
- Buat file readme.md di vsc, lalu save
- Cek filenya menggunakan git status
- Menambahkan file ke staging area menggunakan git add readme.md (readme ini filenya ya)
- Cek lagi dengan git status
- Membuat commit pertama menggunakan git commit -m "pesan commit"
- Ganti ke branch menggunakan git branch -M main
- Kemudian cek menggunakan git branch
- Buat branch baru menggunakan git switch -c feature/catatan-git
- Cek lagi menggunakan git branch
- Buat file catatan.md di vsc seperti tadi membuat readme.md
- Cek dengan git status
- Tambahkan catatan.md ke staging area dengan git add catatan.md
- Kemudian cek lagi dengan git status
- Buat commit kedua dengan git commit -m "docs: add basic Git commands notes"
- Kemudian cek lagi dengan git status
- Push branch dengan git push -u origin feature/catatan-git
- Switch ke main dulu dengan git switch main
- Tadi lupa harusnya push branch main juga dengan git push -u origin main
- Habis tu gunain fitur GitHub yg pull request, main <- feature/catatan git
- Dan Pull Request deh
- Kalau udah done scroll kebawah cari merge pull request dan pencet itu
- Pull Request dan Merge udah selesai

UNTUK HANDLING SIMULATION -- Simulasi merge conflict terjadi kalau dua branch mengubah bagian/baris yang sama dengan isi yang berbeda.
- Cek statusnya dengan git status, klo working tree clean gas ae
- Buat branch baru dengan git switch -c conflict-test
- Ubah line 9 yg git pull misalnya di catatan.md lalu jalankan git add catatan.md
- Terus commit dengan git commit -m "docs: update git pull description"
- Switch ke main dengan git switch main karena branch kedua harus dibuat dari kondisi main yang belum memiliki perubahan dari branch conflict-test.
- Buat branch kedua dengan git switch -c conflict-test-2
- Ubah line 9 yg git pull misalnya di catatan.md lalu jalankan git add catatan.md
- Terus commit dengan git commit -m "docs: update git pull note"
- Switch Kembali branch ke conflict-test dengan git switch conflict-test
- Dan switch ke git merge conflict-test-2 sekarang.
- Nah, muncul errornya kan jadi hapus tanda <<< === >>> dan hapus baris yg double sisakan satu saja yang benar-benar ingin dipakai.
- Nah setelah ubah file terus jalankan git add catatan.md
- Lalu selesaikan dengan commit dengan git commit -m "fix: resolve merge conflict in catatan.md"
- Cek Kembali dengan git status jika muncul working tree clean, berarti resolve conflict berhasil.
