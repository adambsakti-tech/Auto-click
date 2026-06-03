# Canton AutoClick — Auto-clicker Android (build dari HP)

Auto-clicker berbasis koordinat: tambah/rekam titik tap, atur interval, play/loop.
Bekerja lintas-aplikasi pakai **AccessibilityService** + overlay. Native Kotlin.

## Build APK tanpa PC (via GitHub Actions)
1. Login github.com di browser HP → **New repository** (mis. `canton-autoclick`).
2. Upload SEMUA isi folder ini (struktur folder dipertahankan: `app/`, `.github/`,
   `build.gradle`, `settings.gradle`, `gradle.properties`).
   - Paling gampang: buka github.com mode desktop di Chrome → **Add file → Upload files** → drag folder.
3. Tab **Actions** jalan otomatis ("Build AutoClick APK"). Kalau tidak, klik **Run workflow**.
4. Tunggu centang hijau (~3–6 mnt) → buka run → **Artifacts** → download `canton-autoclick-apk`.
5. Install `app-debug.apk` (izinkan Install unknown apps).

## Cara pakai di HP
1. Buka app → tombol **1) Izinkan Overlay** → aktifkan izin.
2. **2) Aktifkan Accessibility** → cari "Canton AutoClick" → ON.
3. **3) Mulai Panel** → panel mengambang muncul.
4. **➕ Titik** lalu tap lokasi (layar bertint merah = mode tangkap), atau **⏺ Rec**
   untuk merekam urutan tap (tekan Rec lagi untuk stop — jeda antar tap ikut terekam).
5. Set **ms** (jeda antar klik untuk titik manual), pilih **🔁** loop, lalu **▶ Play**.
   **⏹ Stop** untuk berhenti. **✕** tutup panel.

## Catatan
- Hanya untuk perangkat sendiri (sideload debug APK).
- Berbasis koordinat layar — kalau resolusi/orientasi berubah, titik perlu diset ulang.
- Sebagian game/app punya deteksi anti-automation; auto-click bisa tidak berfungsi/ditolak di app tsb.
