# 🎨 Customization Guide

Panduan untuk meng-customize README profile GitHub Anda.

## 🎯 Quick Customization Checklist

- [ ] Update email address
- [ ] Update social media links
- [ ] Add project demo links
- [ ] Setup WakaTime (opsional)
- [ ] Setup blog RSS feed (opsional)
- [ ] Customize color theme
- [ ] Add more badges
- [ ] Update project descriptions

---

## 📧 Update Email Address

Cari dan ganti `your.email@gmail.com` dengan email Anda yang sebenarnya di:
- Badge di header
- Badge di section "Let's Connect"

```markdown
[![Email](https://img.shields.io/badge/Email-youremail@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:youremail@gmail.com)
```

---

## 🔗 Add Social Media Links

### Instagram
```markdown
[![Instagram](https://img.shields.io/badge/Instagram-Follow-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://instagram.com/yourusername)
```

### Twitter/X
```markdown
[![Twitter](https://img.shields.io/badge/Twitter-Follow-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/yourusername)
```

### YouTube
```markdown
[![YouTube](https://img.shields.io/badge/YouTube-Subscribe-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://youtube.com/@yourchannel)
```

### Discord
```markdown
[![Discord](https://img.shields.io/badge/Discord-Join-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/yourinvite)
```

### Telegram
```markdown
[![Telegram](https://img.shields.io/badge/Telegram-Contact-26A5E4?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/yourusername)
```

---

## 🎨 Change Color Theme

### Available Themes for GitHub Stats

Ganti `theme=tokyonight` dengan salah satu dari:

- `dark`, `radical`, `merko`, `gruvbox`, `tokyonight`
- `onedark`, `cobalt`, `synthwave`, `highcontrast`, `dracula`
- `prussian`, `monokai`, `vue`, `vue-dark`, `shades-of-purple`
- `nightowl`, `buefy`, `blue-green`, `algolia`, `great-gatsby`
- `darcula`, `bear`, `solarized-dark`, `solarized-light`, `chartreuse-dark`
- `nord`, `gotham`, `material-palenight`, `graywhite`, `vision-friendly-dark`
- `ayu-mirage`, `midnight-purple`, `calm`, `flag-india`, `omni`
- `react`, `jolly`, `maroongold`, `yeblu`, `blueberry`
- `slateorange`, `kacho_ga`, `outrun`, `ocean_dark`, `city_lights`
- `github_dark`, `discord_old_blurple`, `aura_dark`, `panda`, `noctis_minimus`
- `cobalt2`, `swift`, `aura`, `apprentice`, `moltack`
- `codeSTACKr`, `rose_pine`

**Contoh**:
```markdown
![GitHub Stats](https://github-readme-stats.vercel.app/api?username=tetraxion&show_icons=true&theme=dracula&include_all_commits=true&count_private=true&hide_border=true)
```

---

## 🚀 Add Project Demo Links

Update tabel project dengan link demo yang sebenarnya:

```markdown
| 🚀 Project | 📝 Description | 🛠️ Tech Stack | 🔗 Links |
|-----------|---------------|---------------|----------|
| **SpeechDelay-AI** | AI-powered mobile app | `Flutter` `Python` | [Demo](https://your-demo-link.com) [GitHub](https://github.com/yourusername/repo) |
```

---

## 📊 Customize GitHub Stats

### Hide Specific Stats
```markdown
![GitHub Stats](https://github-readme-stats.vercel.app/api?username=tetraxion&hide=issues,contribs)
```

### Show Private Contributions
```markdown
![GitHub Stats](https://github-readme-stats.vercel.app/api?username=tetraxion&count_private=true)
```

### Show Icons
```markdown
![GitHub Stats](https://github-readme-stats.vercel.app/api?username=tetraxion&show_icons=true)
```

### Custom Colors
```markdown
![GitHub Stats](https://github-readme-stats.vercel.app/api?username=tetraxion&bg_color=0D1117&title_color=F7941D&icon_color=F7941D&text_color=FFFFFF)
```

---

## 🏆 Customize GitHub Trophies

### Change Theme
```markdown
![Trophies](https://github-profile-trophy.vercel.app/?username=tetraxion&theme=radical)
```

### Change Layout
```markdown
![Trophies](https://github-profile-trophy.vercel.app/?username=tetraxion&row=2&column=3)
```

### Hide Specific Trophies
```markdown
![Trophies](https://github-profile-trophy.vercel.app/?username=tetraxion&no-frame=true&no-bg=true)
```

---

## 📈 Add More Badges

### Skills Badges

**Programming Languages**:
```markdown
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white)
```

**Frameworks**:
```markdown
![Vue.js](https://img.shields.io/badge/Vue.js-4FC08D?style=for-the-badge&logo=vue.js&logoColor=white)
![Angular](https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white)
![Spring](https://img.shields.io/badge/Spring-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
```

**Cloud Platforms**:
```markdown
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Google Cloud](https://img.shields.io/badge/Google_Cloud-4285F4?style=for-the-badge&logo=google-cloud&logoColor=white)
![Azure](https://img.shields.io/badge/Azure-0078D4?style=for-the-badge&logo=microsoft-azure&logoColor=white)
![Heroku](https://img.shields.io/badge/Heroku-430098?style=for-the-badge&logo=heroku&logoColor=white)
```

**Testing**:
```markdown
![Jest](https://img.shields.io/badge/Jest-C21325?style=for-the-badge&logo=jest&logoColor=white)
![Pytest](https://img.shields.io/badge/Pytest-0A9EDC?style=for-the-badge&logo=pytest&logoColor=white)
![Cypress](https://img.shields.io/badge/Cypress-17202C?style=for-the-badge&logo=cypress&logoColor=white)
```

---

## 🎭 Add Animated Elements

### Typing SVG Customization

```markdown
![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&duration=3000&pause=1000&color=F7941D&center=true&vCenter=true&width=600&lines=Your+First+Line;Your+Second+Line;Your+Third+Line)
```

**Parameters**:
- `font`: Font family
- `size`: Font size
- `duration`: Duration of typing animation
- `pause`: Pause between lines
- `color`: Text color (hex without #)
- `width`: Width of the SVG
- `lines`: Text lines separated by semicolon

---

## 📝 Add Custom Sections

### Certifications
```markdown
## 🎓 Certifications

- 🏅 **AWS Certified Developer** - Amazon Web Services (2024)
- 🏅 **Google Cloud Professional** - Google (2024)
- 🏅 **Flutter Development Bootcamp** - Udemy (2023)
```

### Achievements
```markdown
## 🏆 Achievements

- 🥇 Winner of Hackathon XYZ 2024
- 🥈 2nd Place in Mobile App Competition
- 🎖️ Open Source Contributor of the Month
```

### Currently Working On
```markdown
## 🔨 Currently Working On

- 🚀 Building an AI-powered mobile app
- 📚 Learning microservices architecture
- 🌟 Contributing to open source projects
```

---

## 🎯 Pro Tips

1. **Keep it Updated**: Update your README regularly with new projects and skills
2. **Be Authentic**: Show your personality and unique style
3. **Use Emojis Wisely**: Don't overuse, keep it professional
4. **Test Links**: Make sure all links work before committing
5. **Mobile Friendly**: Check how it looks on mobile devices
6. **Performance**: Don't add too many heavy images/GIFs
7. **Accessibility**: Use alt text for images

---

## 🔍 Resources

- [Shields.io](https://shields.io/) - Custom badges
- [Simple Icons](https://simpleicons.org/) - Brand icons
- [GitHub Readme Stats](https://github.com/anuraghazra/github-readme-stats)
- [Typing SVG](https://github.com/DenverCoder1/readme-typing-svg)
- [Skill Icons](https://github.com/tandpfun/skill-icons)

---

**Need help? Feel free to customize and experiment! 🎨**
