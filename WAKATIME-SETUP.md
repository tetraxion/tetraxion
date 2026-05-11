# ⏱️ WakaTime Setup Guide

Panduan lengkap untuk setup WakaTime coding stats di GitHub profile Anda.

## 🎯 Apa itu WakaTime?

WakaTime adalah tool untuk tracking coding activity Anda secara otomatis. Menampilkan:
- ⏰ Total coding time
- 💻 Bahasa pemrograman yang paling sering digunakan
- 📁 Project yang sedang dikerjakan
- 🔧 Editor/IDE yang digunakan
- 📊 Daily/Weekly statistics

---

## 🚀 Setup Steps

### Step 1: Daftar WakaTime (GRATIS)

1. Buka [wakatime.com](https://wakatime.com/)
2. Klik **"Sign Up"**
3. Daftar dengan GitHub account (recommended) atau email
4. Verifikasi email jika perlu

---

### Step 2: Install WakaTime Plugin

#### VS Code (Recommended)
1. Buka VS Code
2. Tekan `Ctrl + Shift + X` (Extensions)
3. Search: **"WakaTime"**
4. Install plugin by **WakaTime**
5. Restart VS Code

#### JetBrains IDEs (IntelliJ, Android Studio, dll)
1. File → Settings → Plugins
2. Search: **"WakaTime"**
3. Install & Restart

#### Sublime Text
1. Install Package Control
2. `Ctrl + Shift + P` → Install Package
3. Search: **"WakaTime"**

#### Vim/Neovim
```bash
# Vim-Plug
Plug 'wakatime/vim-wakatime'

# Vundle
Plugin 'wakatime/vim-wakatime'
```

**Lebih banyak editors**: [WakaTime Plugins](https://wakatime.com/plugins)

---

### Step 3: Get API Key

1. Login ke [wakatime.com](https://wakatime.com/)
2. Klik profile Anda (kanan atas)
3. Pilih **"Settings"**
4. Scroll ke **"API Key"** section
5. Copy API Key Anda (format: `waka_xxxxx...`)

**PENTING**: Jangan share API key ini ke siapapun!

---

### Step 4: Configure Plugin

Setelah install plugin, VS Code akan otomatis minta API key:
1. Paste API key yang sudah di-copy
2. Tekan Enter
3. Plugin akan mulai tracking otomatis

**Manual Configuration**:
- File location: `~/.wakatime.cfg`
- Add:
  ```ini
  [settings]
  api_key = waka_xxxxx...
  ```

---

### Step 5: Add API Key ke GitHub Secrets

1. Buka repository GitHub Anda: `https://github.com/tetraxion/tetraxion`
2. Klik **Settings** (tab paling kanan)
3. Sidebar kiri → **Secrets and variables** → **Actions**
4. Klik **"New repository secret"**
5. Isi:
   - **Name**: `WAKATIME_API_KEY`
   - **Secret**: Paste API key Anda
6. Klik **"Add secret"**

---

### Step 6: Verify Workflow

Workflow sudah dibuat di `.github/workflows/waka-readme.yml`

**Manual Trigger untuk Test**:
1. Buka tab **Actions** di GitHub
2. Pilih **"Waka Readme"** workflow
3. Klik **"Run workflow"** → **"Run workflow"**
4. Tunggu selesai (~1-2 menit)

---

### Step 7: Check Results

Setelah workflow selesai:
1. Buka profile GitHub Anda
2. Scroll ke section **"📈 Coding Activity"**
3. Stats akan muncul di antara comment tags:
   ```markdown
   <!--START_SECTION:waka-->
   [Stats akan muncul di sini]
   <!--END_SECTION:waka-->
   ```

---

## 📊 Contoh Output

```
📊 This Week I Spent My Time On:

💬 Programming Languages:
Dart         12 hrs 30 mins  ████████████░░░░░░░░░  55.2%
TypeScript   5 hrs 15 mins   ██████░░░░░░░░░░░░░░░  23.1%
Python       3 hrs 20 mins   ████░░░░░░░░░░░░░░░░░  14.7%
Markdown     1 hr 5 mins     █░░░░░░░░░░░░░░░░░░░░   4.8%
YAML         30 mins         ░░░░░░░░░░░░░░░░░░░░░   2.2%

🔥 Editors:
VS Code      20 hrs 45 mins  ███████████████████░░  91.5%
Android St.  1 hr 55 mins    ██░░░░░░░░░░░░░░░░░░░   8.5%

💻 Operating Systems:
Windows      22 hrs 40 mins  █████████████████████ 100.0%
```

---

## ⚙️ Customization

Edit `.github/workflows/waka-readme.yml` untuk customize:

```yaml
- uses: athul/waka-readme@master
  with:
    WAKATIME_API_KEY: ${{ secrets.WAKATIME_API_KEY }}
    SHOW_TITLE: true              # Show/hide title
    BLOCKS: ->                    # Progress bar style
    TIME_RANGE: last_7_days       # last_7_days, last_30_days, last_6_months, last_year
    SHOW_TIME: true               # Show time spent
    SHOW_MASKED_TIME: true        # Show total time
    SHOW_TOTAL: true              # Show total time
    SHOW_PROJECTS: true           # Show projects
    SHOW_EDITORS: true            # Show editors
    SHOW_OS: true                 # Show OS
    SHOW_LANGUAGE: true           # Show languages
    SHOW_TIMEZONE: false          # Show timezone
```

---

## 🔄 Update Schedule

Workflow berjalan otomatis:
- ⏰ Setiap 2 jam
- 🔄 Atau manual trigger via Actions tab

Edit schedule di `waka-readme.yml`:
```yaml
schedule:
  - cron: "0 */2 * * *"  # Setiap 2 jam
  # - cron: "0 */6 * * *"  # Setiap 6 jam
  # - cron: "0 0 * * *"    # Setiap hari jam 00:00
```

---

## 🐛 Troubleshooting

### Stats tidak muncul?
1. ✅ Pastikan API key sudah ditambahkan di GitHub Secrets
2. ✅ Pastikan nama secret: `WAKATIME_API_KEY` (exact match)
3. ✅ Pastikan WakaTime plugin aktif di IDE
4. ✅ Pastikan sudah ada coding activity (minimal 1 hari)
5. ✅ Check workflow logs di Actions tab

### Workflow gagal?
1. Check error message di Actions tab
2. Verify API key masih valid
3. Re-run workflow

### Plugin tidak tracking?
1. Check status bar (bottom right VS Code)
2. Restart IDE
3. Re-enter API key: `Ctrl + Shift + P` → "WakaTime: API Key"

---

## 💡 Pro Tips

1. **Privacy**: Set project visibility di WakaTime settings
2. **Exclude Files**: Add `.wakatime-project` file untuk exclude folders
3. **Multiple Machines**: Install plugin di semua devices untuk complete tracking
4. **Dashboard**: Check detailed stats di [wakatime.com/dashboard](https://wakatime.com/dashboard)
5. **Goals**: Set coding goals di WakaTime dashboard

---

## 🔗 Resources

- [WakaTime Website](https://wakatime.com/)
- [WakaTime Plugins](https://wakatime.com/plugins)
- [WakaTime Readme Action](https://github.com/athul/waka-readme)
- [WakaTime Documentation](https://wakatime.com/help)

---

## 🎯 Alternative: GitHub Stats

Jika tidak ingin setup WakaTime, Anda bisa disable workflow:
1. Rename file: `waka-readme.yml.disabled`
2. Atau delete file tersebut

Stats lain sudah otomatis muncul tanpa setup:
- GitHub contribution graph
- Language stats
- Commit streak
- Activity graph

---

**Happy Tracking! ⏱️**
