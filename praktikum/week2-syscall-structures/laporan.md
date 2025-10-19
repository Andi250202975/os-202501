
# Laporan Praktikum Minggu [X]
Topik: syscall-structures

---

## Identitas
- **Nama**  : Andi pratama   
- **NIM**   : 250202975  
- **Kelas** : 1IKRA

---

## Tujuan
Tuliskan tujuan praktikum minggu ini.  
Contoh:  
> Tujuan dari praktikum untuk mempelajari mekanisme system call dan struktur sistem operasi adalah untuk memahami bagaimana sebuah program dapat berkomunikasi dengan kernel dan perangkat keras. Dengan memahami konsep ini, kita dapat mengetahui alur kerja sistem dari saat perintah dijalankan hingga perangkat keras meresponsnya. Pengetahuan ini sangat penting karena system call menjadi jembatan antara ruang pengguna (user space) dan ruang kernel (kernel space), sehingga proses eksekusi dapat berjalan dengan aman dan terkontrol. 

---

## Dasar Teori
1. Pemisahan antara User Space dan Kernel Space
Dalam sistem operasi modern, terdapat dua ruang utama, yaitu user space dan kernel space. User space adalah tempat program atau aplikasi dijalankan oleh pengguna, sedangkan kernel space merupakan area khusus yang digunakan oleh kernel untuk mengelola seluruh sumber daya sistem. Pemisahan ini bertujuan untuk menjaga keamanan dan stabilitas sistem, sehingga aplikasi tidak dapat langsung mengakses perangkat keras atau sumber daya penting tanpa melalui mekanisme resmi.

2. Peran System Call sebagai Jembatan Komunikasi
System call berfungsi sebagai pintu gerbang yang menghubungkan user space dengan kernel space. Ketika program ingin melakukan operasi penting seperti membaca file, mengirim data, atau mengakses perangkat keras, ia tidak melakukannya secara langsung, tetapi melalui system call. Dengan cara ini, sistem operasi dapat mengontrol setiap permintaan yang masuk sehingga tidak merusak sistem dan dapat dijalankan dengan aman.

3. Struktur Sistem Operasi yang Berlapis
Sistem operasi memiliki struktur berlapis yang terdiri dari kernel, file system, device driver, dan user interface. Kernel menjadi inti yang mengatur semua proses dan sumber daya. File system mengatur penyimpanan data, sedangkan device driver menerjemahkan perintah kernel ke dalam bahasa yang dapat dipahami perangkat keras. Lapisan terluar adalah user interface, yang memungkinkan pengguna berinteraksi dengan sistem melalui perintah teks atau tampilan grafis.

5. Pengelolaan Sumber Daya Secara Terpusat
Salah satu fungsi utama sistem operasi adalah mengatur dan membagi sumber daya seperti CPU, memori, penyimpanan, dan perangkat input/output. Dengan adanya mekanisme system call, pengelolaan ini dapat dilakukan secara terpusat dan efisien. Hal ini memastikan bahwa setiap proses mendapat giliran yang adil dan tidak terjadi konflik dalam penggunaan sumber daya.

5. Landasan Keamanan dan Stabilitas Sistem
Mekanisme system call dan struktur sistem operasi dirancang untuk menjaga keamanan serta mencegah kerusakan sistem. Karena semua akses terhadap sumber daya penting harus melalui kernel, maka sistem dapat memfilter, mengatur izin, serta mencegah tindakan yang berbahaya. Inilah yang menjadikan sistem operasi mampu berjalan secara stabil meskipun digunakan oleh banyak program secara bersamaan.

---

## Langkah Praktikum
1. Langkah-langkah yang dilakukan.  
2. Perintah yang dijalankan.  
3. File dan kode yang dibuat.  
4. Commit message yang digunakan.

---

## Kode / Perintah
Tuliskan potongan kode atau perintah utama:
```bash
strace ls
strace -e trace=open,read,write,close cat /etc/paswwd
dmesg | tail -n10
```

---

## Hasil Eksekusi
Sertakan screenshot hasil percobaan atau diagram:
![alt text](screenshots/screenshotssyscall_ls.png)
![alt text](screenshots/screenshotssyscall2_ls.png)
![alt text](screenshots/screenshotssyscall3_ls.png)


---

## Analisis
- Jelaskan makna hasil percobaan.  
- Hubungkan hasil dengan teori (fungsi kernel, system call, arsitektur OS).  
- Apa perbedaan hasil di lingkungan OS berbeda (Linux vs Windows)?  

---

## Kesimpulan
Tuliskan 2–3 poin kesimpulan dari praktikum ini.

---

## Quiz
1. Apa fungsi utama system call dalam sistem operasi?  
   **Jawaban:
   1.manajemen proses
   2.manajemen file
   3.komunikasi
   4.manajemen sistem & proteksi**  
3. Sebutkan 4 kategori system call yang umum digunakan. 
   **Jawaban:
   1.proses control
   2.file manajer
   3.Devive management
   4.information maintance & commmuniacation**  
5. Mengapa system call tidak bisa dipanggil langsung oleh user program? 
   **Jawaban:
    karena hanya dapat dijalankan di mode kernel,sedangkan program berjalan di mode user**  

---

## Refleksi Diri
Tuliskan secara singkat:
- Apa bagian yang paling menantang minggu ini?  
- Bagaimana cara Anda mengatasinya?  

---

**Credit:**  
_Template laporan praktikum Sistem Operasi (SO-202501) – Universitas Putra Bangsa_
