<div align="center">

# 🎵 NexusMusic

**Free Music Streaming App for Android**

[![Android](https://img.shields.io/badge/Platform-Android-3DDC84?logo=android&logoColor=white)](https://developer.android.com)
[![API](https://img.shields.io/badge/API-24%2B-brightgreen)](https://developer.android.com/about/versions/nougat)
[![Kotlin](https://img.shields.io/badge/Kotlin-1.9.22-7F52FF?logo=kotlin&logoColor=white)](https://kotlinlang.org)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

Stream musik favorit kamu secara gratis, kapan saja, di mana saja.<br>
Dengerin bareng teman? Bisa juga!

[Download APK](https://github.com/user/nexusmusic/releases) · [Report Bug](https://github.com/user/nexusmusic/issues) · [Request Feature](https://github.com/user/nexusmusic/issues)

</div>

---

## 📸 Screenshots

<div align="center">
<table>
  <tr>
    <td><img src="screenshots/home.png" width="200" alt="Home"/></td>
    <td><img src="screenshots/search.png" width="200" alt="Search"/></td>
    <td><img src="screenshots/player.png" width="200" alt="Player"/></td>
    <td><img src="screenshots/lyrics.png" width="200" alt="Lyrics"/></td>
  </tr>
  <tr>
    <td align="center">Home</td>
    <td align="center">Search</td>
    <td align="center">Player</td>
    <td align="center">Lyrics</td>
  </tr>
  <tr>
    <td><img src="screenshots/library.png" width="200" alt="Library"/></td>
    <td><img src="screenshots/profile.png" width="200" alt="Profile"/></td>
    <td><img src="screenshots/party.png" width="200" alt="Party Mode"/></td>
    <td><img src="screenshots/settings.png" width="200" alt="Settings"/></td>
  </tr>
  <tr>
    <td align="center">Library</td>
    <td align="center">Profile</td>
    <td align="center">Party Mode</td>
    <td align="center">Settings</td>
  </tr>
</table>
</div>

> ⚠️ Ganti path screenshot di atas dengan gambar asli kamu di folder `screenshots/`

---

## ✨ Features

### 🎵 Core Music
- **Smart Search** — Cari lagu, artis, atau album dengan real-time suggestion
- **Stream Tanpa Batas** — Putar musik sepuasnya tanpa iklan dan tanpa biaya langganan
- **Download Offline** — Simpan lagu ke perangkat untuk didengarkan tanpa internet
- **Live Lyrics** — Tampilkan lirik secara real-time saat musik diputar
- **Background Playback** — Musik tetap jalan meski layar mati, lengkap dengan notifikasi media

### 📚 Library Management
- **Liked Songs** — Tandai lagu favorit dengan satu ketukan
- **Custom Playlist** — Buat dan kelola playlist sesuka hati
- **Recently Played** — Akses cepat ke lagu yang baru diputar
- **Downloaded Songs** — Kelola semua lagu offline dalam satu tempat

### 🎤 Discovery
- **Home Feed** — Rekomendasi musik yang selalu fresh
- **Artist Page** — Jelajahi diskografi lengkap: top songs, album, singles
- **Album Page** — Lihat daftar lagu dalam album dan langsung putar
- **Playlist Page** — Temukan playlist publik dari berbagai genre

### 🎧 Party Mode (NEW!)
- **Create Room** — Buat ruangan dan jadi Host
- **Invite via Link** — Bagikan link `nexusmusic://party?room=XXX` ke teman
- **Real-time Sync** — Musik tersinkronisasi secara real-time antar perangkat
- **Up to 4 Users** — Dengerin bareng hingga 4 orang sekaligus
- **Avatar Slots** — Lihat siapa saja yang ada di room lewat foto profil

### 🎨 UI/UX
- **Dark Mode** — Tampilan gelap yang elegan dan nyaman di mata
- **Dynamic Colors** — Warna player berubah otomatis sesuai artwork album
- **Mini Player** — Kontrol musik tanpa harus membuka full player
- **Smooth Animations** — Transisi halus antar halaman

---

## 🛠️ Tech Stack

| Component | Technology |
|-----------|-----------|
| **Language** | Kotlin |
| **UI** | XML + View Binding |
| **Networking** | Retrofit + OkHttp |
| **Serialization** | Kotlinx Serialization |
| **Image Loading** | Coil |
| **Media Player** | AndroidX Media3 (ExoPlayer) |
| **Auth** | Firebase Auth (Google Sign-In) |
| **Realtime DB** | Firebase Realtime Database |
| **Architecture** | Fragment-based Navigation |
| **Async** | Kotlin Coroutines + Flow |

---

## 📦 Installation

### Prerequisites
- Android Studio Hedgehog (2023.1.1) atau lebih baru
- JDK 17
- Android SDK API 36

### Steps

1. **Clone repository**
   ```bash
   git clone https://github.com/user/nexusmusic.git
   cd nexusmusic
   ```

2. **Setup Firebase**
   - Buat project baru di [Firebase Console](https://console.firebase.google.com)
   - Aktifkan **Authentication** (Google Sign-In)
   - Aktifkan **Realtime Database**
   - Download `google-services.json` dan taruh di folder `app/`

3. **Setup Firebase Realtime Database Rules**
   ```json
   {
     "rules": {
       "rooms": {
         "$roomId": {
           ".read": true,
           ".write": "auth != null"
         }
       }
     }
   }
   ```

4. **Build & Run**
   ```bash
   ./gradlew assembleDebug
   ```

---

## 📁 Project Structure

```
app/src/main/java/com/zedx/nexusmusic/
├── data/
│   ├── local/          # LibraryManager (SharedPreferences)
│   ├── model/          # Data classes (Song, Album, Artist, etc.)
│   └── remote/         # Retrofit API Service & FirebaseManager
├── service/            # PlaybackService (Media3)
├── ui/
│   ├── fragments/      # Home, Search, Library, Profile
│   └── SongAdapter.kt  # RecyclerView Adapters
├── util/               # QueueManager, LyricsCache
├── MainActivity.kt
├── PlayerActivity.kt
├── AlbumDetailActivity.kt
├── ArtistDetailActivity.kt
├── PlaylistDetailActivity.kt
├── SettingsActivity.kt
└── LeaderboardActivity.kt
```

---

## 🤝 Contributing

Kontribusi sangat diterima! Silakan:

1. Fork repository ini
2. Buat branch fitur (`git checkout -b feature/fitur-keren`)
3. Commit perubahan (`git commit -m 'Tambah fitur keren'`)
4. Push ke branch (`git push origin feature/fitur-keren`)
5. Buka Pull Request

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

---

## 💖 Support

Suka NexusMusic? Dukung developer!

[![Trakteer](https://img.shields.io/badge/Trakteer-Donate-red)](https://trakteer.id/xvce/gift)

---

<div align="center">

**Made with ❤️ by ikyy**

</div>
