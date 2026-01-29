# 🚀 React Native + Expo (No Template)

Dokumentasi ini menjelaskan cara menginstall **React Native menggunakan Expo tanpa template** dan mengaktifkan **Expo Router** dengan dukungan JSX/TSX.

---

## 📦 Prerequisites

Pastikan sudah terinstall:

* **Node.js** (disarankan versi LTS)
* **npm** atau **yarn**
* **Git** (opsional)
* **Expo Go** (di HP, untuk testing)

---

## ⚙️ Instalasi Expo (Blank Template)

Buat project Expo **tanpa template**:

```bash
npx create-expo-app@latest --template blank ./
```

> Perintah ini akan membuat project Expo kosong (blank) di folder saat ini.

---

## 🌐 Alternatif: Install dari Situs React Native

Jika kalian mengikuti dokumentasi React Native / Expo secara manual, jalankan:

```bash
npm install expo
```

---

## 🔄 Mengubah ke JSX / TSX (Expo Router)

### 1️⃣ Hapus File Default

Masuk ke folder `app/`, lalu **hapus kedua file default** (biasanya):

* `index.js`
* `_layout.js`

---

### 2️⃣ Edit `app.json`

Tambahkan `scheme` **di bagian atas** file `app.json`:

```json
{
  "scheme": "nama-project-kalian",
  "expo": {
    ...
  }
}
```

> `scheme` digunakan untuk deep linking & Expo Router.

---

### 3️⃣ Install Expo Router & Dependencies

Jalankan perintah berikut di terminal:

```bash
npx expo install expo-router react-native-safe-area-context react-native-screens expo-linking expo-constants expo-status-bar
```

---

### 4️⃣ Update `package.json`

Ubah bagian `main` menjadi:

```json
"main": "expo-router/entry"
```

Contoh:

```json
{
  "name": "nama-project",
  "version": "1.0.0",
  "main": "expo-router/entry",
  "scripts": {
    "start": "expo start",
    "android": "expo start --android",
    "ios": "expo start --ios",
    "web": "expo start --web"
  }
}
```

---

## 📁 Struktur Folder (Contoh)

```bash
app/
 ├── index.jsx
 ├── _layout.jsx
assets/
app.json
package.json
```

> Kalian bisa pakai `.jsx` atau `.tsx` sesuai kebutuhan.

---

## ▶️ Menjalankan Project

```bash
npm run start
```

atau

```bash
npx expo start
```

Scan QR Code menggunakan **Expo Go** di HP 📱
