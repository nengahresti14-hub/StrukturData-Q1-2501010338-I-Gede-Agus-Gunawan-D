# StrukturData-Q1-2501010338-I-Gede-Agus-Gunawan-D
1. Karakteristik Memori dan Akses Data

Array dapat mengakses elemen dalam waktu konstan O(1) karena data disimpan secara berurutan (kontinu) di memori. Setiap elemen memiliki indeks yang langsung dihitung menggunakan alamat dasar array ditambah offset indeks. Oleh karena itu, komputer dapat langsung menuju lokasi data tanpa harus memeriksa elemen lain terlebih dahulu.

Sedangkan pada Singly Linked List, data disimpan secara tidak berurutan (non-kontinu). Setiap node hanya menyimpan data dan pointer menuju node berikutnya. Untuk mengakses elemen tertentu, sistem harus menelusuri node satu per satu dari awal hingga posisi yang dicari. Karena proses traversal dilakukan secara berurutan, waktu akses menjadi O(n).

2. Analisis Efisiensi Operasi Manipulasi

Linked List lebih unggul dibandingkan Array ketika sering terjadi operasi penyisipan (insertion) dan penghapusan (deletion) data, terutama di bagian awal atau tengah struktur data.

Pada Array, insertion atau deletion memerlukan pergeseran elemen-elemen lain agar susunan indeks tetap rapi. Proses shifting ini membutuhkan waktu O(n).

Sedangkan pada Linked List, insertion dan deletion cukup dilakukan dengan mengubah pointer antar node tanpa memindahkan data lain. Jika posisi node sudah diketahui, operasi dapat dilakukan dalam waktu O(1).

Karena itu, Linked List lebih cocok digunakan pada kondisi data yang ukurannya sering berubah secara dinamis.

3. Konsep Doubly Linked List

Pada Doubly Linked List, setiap node memiliki tiga bagian utama:

Data
Pointer ke node berikutnya (next)
Pointer ke node sebelumnya (prev)

Struktur ini berbeda dengan Singly Linked List yang hanya memiliki satu pointer next.

Keberadaan pointer tambahan menyebabkan penggunaan memori menjadi lebih besar karena setiap node menyimpan dua alamat pointer. Namun, keuntungan utamanya adalah penelusuran data menjadi lebih fleksibel karena traversal dapat dilakukan ke dua arah, yaitu maju dan mundur.

Doubly Linked List juga mempermudah operasi penghapusan node karena tidak perlu selalu mencari node sebelumnya terlebih dahulu.

4. Mekanisme Circular Linked List

Circular Linked List memiliki struktur melingkar, di mana node terakhir tidak menunjuk ke NULL, melainkan kembali menunjuk ke node pertama.

Sedangkan pada Linked List biasa, node terakhir selalu menunjuk ke NULL sebagai penanda akhir data.

Karena bersifat melingkar, traversal pada Circular Linked List dapat dilakukan terus-menerus tanpa harus kembali ke awal secara manual.

Salah satu contoh penggunaan yang efektif adalah sistem Round Robin Scheduling pada sistem operasi. Pada metode ini, proses CPU dijalankan secara bergantian dan berulang secara siklus sehingga struktur melingkar lebih efisien digunakan.

5. Array Dinamis di Python

Python list menggunakan konsep Dynamic Array. Ketika operasi append dilakukan dan kapasitas array sudah penuh, Python akan membuat blok memori baru dengan kapasitas yang lebih besar.

Setelah itu, seluruh elemen lama akan disalin (copy) ke lokasi memori baru tersebut. Setelah proses penyalinan selesai, array lama akan dilepas dan sistem mulai menggunakan array baru.

Mekanisme ini memungkinkan Python list dapat bertambah ukuran secara otomatis tanpa pengguna perlu menentukan ukuran awal secara manual.

Walaupun proses resize membutuhkan waktu O(n) karena harus menyalin data, operasi append secara umum tetap dianggap efisien dengan kompleksitas amortized O(1).
