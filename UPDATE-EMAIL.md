# 📧 Update Email Address

Panduan cepat untuk update email address di README.

## 🎯 Lokasi Email di README

Email Anda muncul di **2 tempat** di README.md:

### 1️⃣ Header Section (Baris ~10)
```markdown
[![Email](https://img.shields.io/badge/Email-Contact-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:your.email@gmail.com)
```

### 2️⃣ Let's Connect Section (Baris ~250+)
```markdown
[![Email](https://img.shields.io/badge/Email-your.email@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:your.email@gmail.com)
```

---

## ✏️ Cara Update

### Option 1: Find & Replace (Recommended)
1. Buka README.md
2. Tekan `Ctrl + H` (Find & Replace)
3. Find: `your.email@gmail.com`
4. Replace: `youremail@gmail.com` (email Anda yang sebenarnya)
5. Replace All

### Option 2: Manual Edit
Edit kedua lokasi di atas dengan email Anda.

---

## 💡 Format Email Badge

### Gmail
```markdown
[![Email](https://img.shields.io/badge/Email-youremail@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:youremail@gmail.com)
```

### Outlook
```markdown
[![Email](https://img.shields.io/badge/Email-youremail@outlook.com-0078D4?style=for-the-badge&logo=microsoft-outlook&logoColor=white)](mailto:youremail@outlook.com)
```

### Yahoo
```markdown
[![Email](https://img.shields.io/badge/Email-youremail@yahoo.com-6001D2?style=for-the-badge&logo=yahoo&logoColor=white)](mailto:youremail@yahoo.com)
```

### Custom Domain
```markdown
[![Email](https://img.shields.io/badge/Email-you@yourdomain.com-00C4CC?style=for-the-badge&logo=maildotru&logoColor=white)](mailto:you@yourdomain.com)
```

---

## 🚀 Setelah Update

```bash
git add README.md
git commit -m "📧 Update email address"
git push origin main
```

---

**Done! ✅**
