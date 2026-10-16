# Jawaban Praktikum: 
# Nama : Elia Nurlatipah
# NIM : 10224149

## Bagian 1: Pemanasan
1. Pada aturan `nav a.active:hover { color: red; }`:
   - Selector: `nav a.active:hover`
   - Property: `color`
   - Value: `red`
   - Declaration: `color: red;`
   - Pseudo-class: `:hover`
2. Default Display:
   - Inline: `span`, `a`, `strong`
   - Block: `p`, `li`, `h2`
3. Paragraf A dan B akan berwarna hijau (`.box p` menargetkan semua paragraf turunan `.box`).
4. Berwarna **merah (red)**. ID Selector (`#title`) memiliki spesifisitas tertinggi (1-0-0) dibanding Class `.heading` (0-1-0) dan Tag `h1` (0-0-1).
5. Penutupan tag salah (*overlapping*). Tag `<strong>` harus ditutup sebelum `</p>`. Perbaikan: `<p>Hello <strong>world</strong></p>`.

## Bagian 3: Prediksi Selector Golf
P1.
(a) "Weekly hack nights.": green
(b) "Bring your own laptop.": orange
(c) "© 2026 Student Affairs": blue

P2. Urutan specificity (tertinggi ke terendah):
1. `#tech p` (1-0-1)
2. `.club p` (0-1-1)
3. `main section p` (0-0-3)
4. `p` (0-0-1)

Setelah diuji (hasil sebenarnya):
Semua hasil pengujian di browser sesuai dengan prediksi P1 dan P2.

## Bagian 4: Box model
Q1 (content-box):
Lebar tampak = width + padding left/right + border left/right
= 300px + 16px + 16px + 1px + 1px = **334px**.
Penjelasan: Pada `content-box`, padding dan border ditambahkan di luar nilai `width`.

Q2 (border-box):
Lebar tampak tetap **300px**.
Penjelasan: Pada `border-box`, padding dan border dihitung di dalam total `width` 300px.

Pengecekan DevTools:
Content: 300px, Padding: 16px, Border: 1px, Margin: 24px.

## Bagian 5: Tabel debug
| # | Baris | Bug | Perbaikan | Cara menemukannya |
|---|-------|-----|-----------|-------------------|
| 1 | 9 | `colour: #333;` | `color: #333;` | DevTools (property tidak dikenal) |
| 2 | 12 | Kurang titik koma pada `background: #dbe7f3` | Tambahkan `;` | Membaca kode |
| 3 | 16 | Nama class `.Card` kapital | Ubah ke `.card` | Membaca kode |
| 4 | 20 | Spasi pada nilai `font-size: 18 px;` | Ubah ke `18px;` | DevTools (invalid value) |
| 5 | 23 | Ejaan value `text-align: centre;` | Ubah ke `text-align: center;` | DevTools (invalid value) |
| 6 | 28 | Mismatch tag penutup `<h1>...</h2>` | Ubah penutup ke `</h1>` | W3C Validator |
| 7 | 31 | Kurang tanda kutip penutup `href="about.html>` | Ubah ke `href="about.html"` | W3C Validator |
| 8 | 36 | Gambar `<img>` tanpa atribut `alt` | Tambahkan `alt="News"` | W3C Validator |
| 9 | 20 & 37 | Mismatch ID `#news-list` dan `id="newsList"` | Ubah HTML ke `id="news-list"` | Membaca kode |

## Bagian 6: Tabel Code Review
| # | Baris | Masalah | Mengapa penting | Perbaikan saya |
|---|-------|---------|-----------------|----------------|
| 1 | 1 | Kurang `<!DOCTYPE html>` dan `lang="id"` | Memicu Quirks Mode di browser | Tambahkan `<!DOCTYPE html>` dan `<html lang="id">` |
| 2 | 6 | Penggunaan `!important` | Merusak hirarki spesifisitas | Hapus `!important` |
| 3 | 12 | Penggunaan `<div>` tanpa tag semantik | Buruk untuk SEO dan screen reader | Gunakan `<header>`, `<nav>`, `<main>`, `<footer>` |
| 4 | 13 | Judul utama menggunakan `<div class="title">` | Mengganggu hirarki dokumen | Ganti dengan `<h1>` |
| 5 | 21 | Menggunakan inline style `style="..."` | Mencampur struktur dan tampilan | Pindahkan ke CSS terpisah/class |
| 6 | 22 | Menggunakan tag `<br>` untuk mengatur jarak | Jarak elemen seharusnya menggunakan margin CSS | Gunakan properti `margin` pada CSS |
| 7 | 26 | Elemen `<input>` tidak memiliki `<label>` | Pengguna screen reader tidak tahu fungsi input | Tambahkan tag `<label for="...">` |
| 8 | 28 | Menggunakan atribut event inline `onclick="..."` | Mencampur HTML dan JavaScript | Pisahkan logika ke file JS |

Refleksi:
1. Penggunaan `<div>` non-semantik paling sulit disadari dari visual browser karena kelihatannya baik-baik saja padahal kodenya buruk.
2. Masalah ini penting karena memengaruhi SEO, performa, dan aksesibilitas bagi pengguna penyandang disabilitas.
3. Kebiasaan yang akan saya lakukan adalah memvalidasi file HTML lewat W3C Validator sebelum mengumpulkan.

## Bagian 7: Exit ticket
1. Aturan CSS terdiri dari **Selector** dan **Declaration Block** `{}` yang berisi pasangan **Property** dan **Value** yang diakhiri titik koma `;`.
2. Kalkulasi poin spesifisitas pada kombinasi selector yang kompleks.
3. Membuat struktur HTML5 semantik lengkap beserta formulir dan tabel.