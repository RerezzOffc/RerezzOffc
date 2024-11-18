# Project Name

Deskripsi singkat tentang proyek Anda, termasuk tujuan dan fungsinya.

## Fitur

- **Deteksi Bahasa Pemrograman**: Fitur ini memungkinkan untuk mendeteksi bahasa pemrograman yang digunakan dalam repositori ini.
- **Deteksi Bahasa**: Fitur ini memungkinkan aplikasi untuk mendeteksi bahasa yang digunakan dalam teks atau input pengguna.
- **Pengikut**: Menampilkan jumlah pengikut dan memberikan informasi seputar pengikut.
- **Sosial Media**: Tautan ke berbagai platform sosial media dengan ikon untuk memudahkan pengunjung menghubungi atau mengikuti proyek di media sosial.

## Teknologi yang Digunakan

- **HTML/CSS/JS**: Untuk membangun halaman web yang responsif.
- **Font Awesome**: Untuk menampilkan ikon sosial media.
- **GitHub API**: Untuk mendeteksi bahasa pemrograman di repositori ini.

## Demo

Tampilkan demo atau tangkapan layar proyek Anda di sini.

## Deteksi Bahasa Pemrograman

Repositori ini menggunakan berbagai bahasa pemrograman. Dengan memanfaatkan **GitHub API**, Anda dapat melihat bahasa yang digunakan dalam repositori ini.

### Cara Mendapatkan Bahasa dari Repositori

Fitur ini menggunakan **GitHub API** untuk mengambil informasi tentang repositori dan mendeteksi bahasa yang digunakan dalam kode. Berikut adalah contoh implementasi menggunakan JavaScript untuk mengambil data bahasa pemrograman dari repositori.

```javascript
// Fungsi untuk mendapatkan bahasa dari repositori GitHub
function getLanguages() {
  const repoUrl = 'https://api.github.com/repos/username/repository-name/languages';
  
  fetch(repoUrl)
    .then(response => response.json())
    .then(data => {
      // Menampilkan bahasa pemrograman yang digunakan
      const languages = Object.keys(data);
      console.log('Bahasa pemrograman yang digunakan:');
      languages.forEach(language => {
        console.log(language);
      });
    })
    .catch(error => {
      console.error('Error fetching language data:', error);
    });
}

// Memanggil fungsi untuk mendeteksi bahasa pemrograman
getLanguages();
