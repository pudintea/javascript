Mantap! Kita masuk ke materi penting dan keren dari JavaScript: **`localStorage`** — ini sangat berguna untuk menyimpan data di browser tanpa server.

---

## 📦 **1. Menyimpan Data ke `localStorage`**

```javascript
localStorage.setItem("kunci", "isi data");
```

Contoh:

```javascript
localStorage.setItem("nama", "Nama Saya Dong");
```

---

## 📥 **2. Mengambil Data dari `localStorage`**

```javascript
let data = localStorage.getItem("kunci");
```

Contoh:

```javascript
let nama = localStorage.getItem("nama");
console.log(nama); // Output: Nama Saya Dong
```

Kalau belum ada datanya, hasilnya `null`.

---

## 🗑️ **3. Menghapus Data dari `localStorage`**

```javascript
localStorage.removeItem("kunci");
```

Contoh:

```javascript
localStorage.removeItem("nama");
```

---

## 🔄 **4. Menghapus Semua Data di `localStorage`**

```javascript
localStorage.clear();
```

⚠️ Hati-hati ya, ini akan menghapus semua data yang disimpan di `localStorage` oleh situs kamu.

---

## 📚 **Bonus: Menyimpan Data Berbentuk Objek atau Array**

Karena `localStorage` hanya bisa simpan **string**, kamu harus pakai `JSON.stringify()` dan `JSON.parse()`:

### ✅ Simpan:
```javascript
const siswa = { nama: "Budi", umur: 17 };
localStorage.setItem("dataSiswa", JSON.stringify(siswa));
```

### ✅ Ambil:
```javascript
const ambilSiswa = JSON.parse(localStorage.getItem("dataSiswa"));
console.log(ambilSiswa.nama); // Output: Budi
```

---

Kalau kamu kasih tahu use case kamu, aku bisa bantu buatkan contoh real-nya langsung 👌  
Misalnya: simpan nama dari form input, terus tampilkan di halaman, dan bisa dihapus juga. Mau?
