# 🚀 GitHub Actions Setup Guide

Panduan lengkap untuk mengaktifkan semua fitur dinamis di README profile GitHub Anda.

## 📋 Daftar Workflows

### 1. ✅ Snake Animation (Sudah Aktif)
**File**: `.github/workflows/snake.yml`

Workflow ini akan otomatis berjalan dan tidak memerlukan setup tambahan!

**Cara Kerja**:
- Berjalan otomatis setiap 24 jam
- Generate snake animation dari contribution graph Anda
- Menyimpan hasil di branch `output`

**Status**: ✅ Siap digunakan setelah push pertama

---

### 2. 📝 Blog Post Workflow (Perlu Setup)
**File**: `.github/workflows/blog-post-workflow.yml`

**Setup**:
1. Edit file `.github/workflows/blog-post-workflow.yml`
2. Ganti `feed_list` dengan RSS feed blog Anda:
   ```yaml
   feed_list: "https://dev.to/feed/yourusername,https://medium.com/feed/@yourusername"
   ```

**Contoh RSS Feeds**:
- Dev.to: `https://dev.to/feed/yourusername`
- Medium: `https://medium.com/feed/@yourusername`
- Hashnode: `https://yourusername.hashnode.dev/rss.xml`
- Personal Blog: `https://yourblog.com/feed.xml`

**Status**: ⚠️ Perlu update RSS feed URL

---

### 3. ⏱️ WakaTime Stats (Opsional)
**File**: `.github/workflows/waka-readme.yml`

**Setup**:
1. Daftar di [WakaTime](https://wakatime.com/)
2. Install WakaTime plugin di VS Code/IDE Anda
3. Dapatkan API Key dari [WakaTime Settings](https://wakatime.com/settings/account)
4. Tambahkan secret di GitHub:
   - Buka repository Settings → Secrets and variables → Actions
   - Klik "New repository secret"
   - Name: `WAKATIME_API_KEY`
   - Value: [Your WakaTime API Key]

**Status**: ⚠️ Perlu WakaTime API Key

---

### 4. 📊 Update Stats (Sudah Aktif)
**File**: `.github/workflows/update-stats.yml`

Workflow ini akan otomatis berjalan dan tidak memerlukan setup tambahan!

**Status**: ✅ Siap digunakan

---

## 🔧 Cara Mengaktifkan

### Step 1: Push ke GitHub
```bash
git add .
git commit -m "Add GitHub Actions workflows"
git push origin main
```

### Step 2: Enable GitHub Actions
1. Buka repository di GitHub
2. Klik tab **Actions**
3. Jika diminta, klik **"I understand my workflows, go ahead and enable them"**

### Step 3: Set Permissions
1. Buka **Settings** → **Actions** → **General**
2. Scroll ke **Workflow permissions**
3. Pilih **"Read and write permissions"**
4. Centang **"Allow GitHub Actions to create and approve pull requests"**
5. Klik **Save**

### Step 4: Manual Trigger (Opsional)
Untuk test workflow:
1. Buka tab **Actions**
2. Pilih workflow yang ingin dijalankan
3. Klik **"Run workflow"**

---

## 🎯 Hasil yang Diharapkan

### Snake Animation
Setelah workflow berjalan, Anda akan melihat:
- Branch baru bernama `output`
- File `github-contribution-grid-snake.svg` dan `github-contribution-grid-snake-dark.svg`
- Snake animation muncul di README

### Blog Posts
Setelah setup RSS feed:
- 5 blog post terbaru akan muncul di section "Latest Blog Posts"
- Update otomatis setiap jam

### WakaTime Stats
Setelah setup API key:
- Coding activity 7 hari terakhir
- Bahasa pemrograman yang paling banyak digunakan
- Update setiap 2 jam

---

## 🐛 Troubleshooting

### Snake Animation tidak muncul?
1. Pastikan workflow sudah berjalan (cek tab Actions)
2. Pastikan branch `output` sudah dibuat
3. Tunggu beberapa menit setelah workflow selesai
4. Coba manual trigger workflow

### Blog Posts tidak update?
1. Pastikan RSS feed URL benar
2. Test RSS feed di browser
3. Pastikan format RSS valid

### WakaTime tidak muncul?
1. Pastikan API key sudah ditambahkan di Secrets
2. Pastikan WakaTime plugin aktif di IDE
3. Pastikan sudah ada data coding activity

---

## 📚 Resources

- [GitHub Actions Documentation](https://docs.github.com/en/actions)
- [Snake Animation Repo](https://github.com/Platane/snk)
- [Blog Post Workflow](https://github.com/gautamkrishnar/blog-post-workflow)
- [WakaTime Readme](https://github.com/athul/waka-readme)

---

## 💡 Tips

1. **Test Locally**: Gunakan [act](https://github.com/nektos/act) untuk test workflows secara lokal
2. **Monitor**: Cek tab Actions secara berkala untuk memastikan workflows berjalan
3. **Optimize**: Sesuaikan cron schedule sesuai kebutuhan
4. **Backup**: Simpan backup workflows sebelum melakukan perubahan besar

---

**Happy Coding! 🚀**
