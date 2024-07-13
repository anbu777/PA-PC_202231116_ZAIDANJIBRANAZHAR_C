

---

# Segmentasi Gambar Nanas

Program ini melakukan segmentasi pada gambar nanas untuk memisahkan buah nanas dan daunnya berdasarkan rentang warna tertentu. Segmentasi ini dilakukan menggunakan pustaka OpenCV dan matplotlib untuk menampilkan hasilnya.

## Teori Pendukung

Segmentasi citra adalah proses membagi gambar digital menjadi beberapa segmen (kumpulan piksel). Tujuan segmentasi adalah menyederhanakan atau mengubah representasi gambar menjadi sesuatu yang lebih bermakna dan lebih mudah dianalisis. Dalam konteks ini, kita menggunakan segmentasi berbasis warna dalam ruang warna HSV (Hue, Saturation, Value).

- **Hue (Hue)**: Representasi dari jenis warna.
- **Saturation (Kejenuhan)**: Intensitas dari warna.
- **Value (Nilai)**: Kecerahan dari warna.

Menggunakan ruang warna HSV lebih efektif untuk segmentasi berbasis warna dibandingkan dengan ruang warna RGB karena pemisahan warna lebih jelas dalam HSV.

## Tahapan Cara Menyelesaikan Proyek

1. **Membaca dan Mengkonversi Gambar**:
    - Membaca gambar dalam format BGR dan mengkonversinya ke RGB untuk keperluan tampilan.
    - Mengkonversi gambar dari RGB ke HSV untuk segmentasi warna.

2. **Membuat Masker untuk Buah Nanas dan Daun**:
    - Mendefinisikan rentang warna untuk buah nanas (kuning) dan daun (hijau).
    - Menggunakan fungsi `cv2.inRange()` untuk membuat masker berdasarkan rentang warna yang telah ditentukan.

3. **Segmentasi Gambar**:
    - Menerapkan masker pada gambar asli menggunakan fungsi `cv2.bitwise_and()` untuk mendapatkan segmentasi buah nanas dan daun.

4. **Menampilkan Hasil**:
    - Menampilkan gambar asli, masker buah nanas, hasil segmentasi buah nanas, dan hasil segmentasi daun menggunakan `matplotlib` dengan subplot.

## NOTE
Untuk background pada citra ikut tersegmentasi dikarenakan termasuk dalam rentang warna yang saya tentukan untuk buah nanas.

## Kesimpulan

Segmentasi gambar nanas ini menunjukkan bagaimana teknik pemrosesan citra dapat digunakan untuk memisahkan objek berdasarkan warna. Dengan memahami dan menerapkan teknik segmentasi berbasis warna, kita dapat melakukan berbagai analisis dan pemrosesan lebih lanjut pada gambar digital.

---

