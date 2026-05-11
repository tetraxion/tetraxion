# 📝 Blog RSS Feed Setup Guide

Panduan untuk menampilkan blog posts terbaru di GitHub profile Anda.

## 🎯 Apa itu Blog RSS Workflow?

Workflow ini akan otomatis menampilkan 5 blog posts terbaru Anda di README profile. Update otomatis setiap jam!

---

## 🚀 Setup Steps

### Step 1: Dapatkan RSS Feed URL

Tergantung platform blog Anda:

#### Dev.to
```
https://dev.to/feed/yourusername
```
**Cara dapat username**:
- Buka profile Dev.to Anda
- URL: `https://dev.to/yourusername`
- Copy `yourusername`

#### Medium
```
https://medium.com/feed/@yourusername
```
**Cara dapat username**:
- Buka profile Medium Anda
- URL: `https://medium.com/@yourusername`
- Copy `@yourusername` (dengan @)

#### Hashnode
```
https://yourusername.hashnode.dev/rss.xml
```
**Cara dapat**:
- Buka blog Hashnode Anda
- URL biasanya: `https://yourusername.hashnode.dev`
- Tambahkan `/rss.xml` di akhir

#### WordPress
```
https://yourblog.com/feed/
```
atau
```
https://yourblog.com/feed.xml
```

#### Ghost
```
https://yourblog.com/rss/
```

#### Blogger
```
https://yourblog.blogspot.com/feeds/posts/default
```

#### Custom Blog (Hugo, Jekyll, Gatsby, dll)
Biasanya:
```
https://yourblog.com/index.xml
https://yourblog.com/feed.xml
https://yourblog.com/rss.xml
```

---

### Step 2: Test RSS Feed

Sebelum setup, test dulu RSS feed Anda:
1. Buka RSS URL di browser
2. Pastikan muncul XML content
3. Pastikan ada list artikel

**Tools untuk test**:
- [RSS Feed Validator](https://validator.w3.org/feed/)
- [RSS Reader](https://feedly.com/)

---

### Step 3: Update Workflow File

Edit file `.github/workflows/blog-post-workflow.yml`:

**Sebelum**:
```yaml
feed_list: "https://dev.to/feed/yourusername,https://medium.com/feed/@yourusername"
```

**Sesudah** (contoh untuk Dev.to):
```yaml
feed_list: "https://dev.to/feed/dwilutfi"
```

**Multiple Blogs** (pisahkan dengan koma):
```yaml
feed_list: "https://dev.to/feed/dwilutfi,https://medium.com/feed/@dwilutfi,https://dwilutfi.hashnode.dev/rss.xml"
```

---

### Step 4: Customize Output (Opsional)

Edit workflow untuk customize tampilan:

```yaml
- name: Pull in blog posts
  uses: gautamkrishnar/blog-post-workflow@v1
  with:
    comment_tag_name: "BLOG-POST-LIST"
    feed_list: "YOUR_RSS_FEED_URL"
    max_post_count: 5                    # Jumlah posts (default: 5)
    template: "- [$title]($url)"         # Format output
    commit_message: "Updated blog posts" # Commit message
    committer_username: "blog-bot"       # Bot username
    committer_email: "blog-bot@example.com"
```

---

### Step 5: Customize Template

**Default Template**:
```yaml
template: "- [$title]($url)"
```
Output:
```markdown
- [My Blog Post Title](https://blog.com/post)
```

**With Date**:
```yaml
template: "- [$title]($url) - $newline  📅 $date"
```
Output:
```markdown
- [My Blog Post Title](https://blog.com/post)
  📅 Jan 15, 2024
```

**With Description**:
```yaml
template: "- [$title]($url)$newline  > $description"
```
Output:
```markdown
- [My Blog Post Title](https://blog.com/post)
  > This is the post description...
```

**Fancy Format**:
```yaml
template: "### [$title]($url)$newline📅 $date | ⏱️ $readTime$newline$newline$description$newline"
```

**Available Variables**:
- `$title` - Post title
- `$url` - Post URL
- `$description` - Post description
- `$date` - Publication date
- `$readTime` - Reading time
- `$newline` - New line

---

### Step 6: Commit & Push

```bash
git add .github/workflows/blog-post-workflow.yml
git commit -m "⚙️ Configure blog RSS feed"
git push origin main
```

---

### Step 7: Manual Trigger (Test)

1. Buka repository di GitHub
2. Tab **Actions**
3. Pilih **"Latest Blog Post Workflow"**
4. Klik **"Run workflow"** → **"Run workflow"**
5. Tunggu selesai (~30 detik)

---

### Step 8: Check Results

Setelah workflow selesai:
1. Buka README.md di GitHub
2. Scroll ke section **"📝 Latest Blog Posts"**
3. Blog posts akan muncul di antara:
   ```markdown
   <!-- BLOG-POST-LIST:START -->
   [Posts akan muncul di sini]
   <!-- BLOG-POST-LIST:END -->
   ```

---

## 📊 Contoh Output

### Simple List
```markdown
<!-- BLOG-POST-LIST:START -->
- [Building AI Apps with Flutter](https://dev.to/dwilutfi/building-ai-apps)
- [Next.js 14 Best Practices](https://dev.to/dwilutfi/nextjs-14-best-practices)
- [Clean Architecture in Mobile Apps](https://dev.to/dwilutfi/clean-architecture)
- [Getting Started with LangChain](https://dev.to/dwilutfi/langchain-intro)
- [Docker for Developers](https://dev.to/dwilutfi/docker-guide)
<!-- BLOG-POST-LIST:END -->
```

### With Dates
```markdown
<!-- BLOG-POST-LIST:START -->
- [Building AI Apps with Flutter](https://dev.to/dwilutfi/building-ai-apps)
  📅 May 10, 2026
- [Next.js 14 Best Practices](https://dev.to/dwilutfi/nextjs-14-best-practices)
  📅 May 8, 2026
<!-- BLOG-POST-LIST:END -->
```

---

## 🔄 Update Schedule

Workflow berjalan otomatis:
- ⏰ Setiap 1 jam
- 🔄 Atau manual trigger via Actions tab

Edit schedule di `blog-post-workflow.yml`:
```yaml
schedule:
  - cron: '0 * * * *'    # Setiap jam
  # - cron: '0 */6 * * *'  # Setiap 6 jam
  # - cron: '0 0 * * *'    # Setiap hari jam 00:00
```

---

## 🐛 Troubleshooting

### Posts tidak muncul?
1. ✅ Pastikan RSS feed URL benar
2. ✅ Test RSS feed di browser
3. ✅ Pastikan ada artikel di blog
4. ✅ Check workflow logs di Actions tab
5. ✅ Pastikan comment tags ada di README:
   ```markdown
   <!-- BLOG-POST-LIST:START -->
   <!-- BLOG-POST-LIST:END -->
   ```

### Workflow gagal?
1. Check error message di Actions tab
2. Verify RSS feed format valid
3. Try different RSS URL format

### RSS feed tidak valid?
1. Test di [RSS Validator](https://validator.w3.org/feed/)
2. Check blog platform documentation
3. Try alternative RSS URL

---

## 💡 Pro Tips

1. **Multiple Blogs**: Combine feeds dari berbagai platform
2. **Custom Domain**: Jika punya custom domain, gunakan RSS dari sana
3. **SEO**: Blog posts di GitHub profile = extra visibility
4. **Consistency**: Post regularly untuk keep profile fresh
5. **Quality**: Feature your best posts

---

## 🎯 Alternative: Manual List

Jika tidak punya blog atau tidak ingin auto-update, bisa manual:

```markdown
## 📝 Latest Blog Posts

- [Building AI Apps with Flutter](https://dev.to/dwilutfi/building-ai-apps)
- [Next.js 14 Best Practices](https://dev.to/dwilutfi/nextjs-14-best-practices)
- [Clean Architecture in Mobile Apps](https://dev.to/dwilutfi/clean-architecture)
```

Atau disable workflow:
```bash
# Rename file
mv .github/workflows/blog-post-workflow.yml .github/workflows/blog-post-workflow.yml.disabled

# Atau delete
rm .github/workflows/blog-post-workflow.yml
```

---

## 🔗 Resources

- [Blog Post Workflow](https://github.com/gautamkrishnar/blog-post-workflow)
- [RSS Feed Validator](https://validator.w3.org/feed/)
- [Dev.to](https://dev.to/)
- [Medium](https://medium.com/)
- [Hashnode](https://hashnode.com/)

---

## 📚 Popular Blog Platforms for Developers

1. **Dev.to** - Free, developer-focused, great community
2. **Hashnode** - Free, custom domain, developer-friendly
3. **Medium** - Large audience, paywall option
4. **Ghost** - Self-hosted, professional
5. **Hugo/Jekyll/Gatsby** - Static site generators

---

**Happy Blogging! 📝**
