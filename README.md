# SEO Checklist สำหรับเว็บไซต์ไทย 2026 ✅

> เช็คลิสต์ SEO ฉบับสมบูรณ์สำหรับเว็บไซต์ภาษาไทย — ใช้ได้ทั้ง Next.js, WordPress, และทุก Framework

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

## ทำไมต้องมี SEO Checklist?

เว็บไซต์ไทยกว่า 80% มีปัญหา SEO พื้นฐานที่ทำให้ไม่ติดอันดับ Google — title ยาวเกิน, ไม่มี Schema, Core Web Vitals ไม่ผ่าน เช็คลิสต์นี้ช่วยให้คุณตรวจสอบได้ครบทุกจุดก่อน launch

---

## 📋 Technical SEO

### Crawlability & Indexability
- [ ] `robots.txt` — อนุญาต Googlebot, บล็อกหน้าที่ไม่ต้องการ index
- [ ] `sitemap.xml` — มี URL ครบ, submit ใน Search Console
- [ ] ไม่มี `noindex` ในหน้าที่ต้องการให้ index
- [ ] Canonical URL ถูกต้องทุกหน้า (self-referencing)
- [ ] ไม่มี redirect chain (redirect ไม่เกิน 1 hop)
- [ ] ไม่มีหน้า orphan (ทุกหน้ามี internal link เข้าถึง)

### HTTPS & Security
- [ ] SSL Certificate ถูกต้อง (HTTPS ทุกหน้า)
- [ ] HTTP → HTTPS redirect อัตโนมัติ
- [ ] HSTS header เปิดใช้งาน
- [ ] Security headers: `X-Frame-Options`, `X-Content-Type-Options`, `Referrer-Policy`

### Core Web Vitals (2026)
- [ ] **LCP** (Largest Contentful Paint) < 2.5 วินาที
- [ ] **INP** (Interaction to Next Paint) < 200ms *(แทนที่ FID ตั้งแต่ 2024)*
- [ ] **CLS** (Cumulative Layout Shift) < 0.1
- [ ] ทดสอบด้วย [PageSpeed Insights](https://pagespeed.web.dev/)
- [ ] ทดสอบด้วย [Lighthouse](https://developer.chrome.com/docs/lighthouse/) — เป้า 90+ ทุก category

### Mobile
- [ ] Responsive design — ทดสอบ 5+ ขนาดหน้าจอ
- [ ] Font size อ่านได้บนมือถือ (ไม่ต่ำกว่า 16px)
- [ ] ปุ่ม/ลิงก์ กดง่าย (tap target ≥ 48x48px)
- [ ] ไม่มี horizontal scroll บนมือถือ
- [ ] Viewport meta tag: `<meta name="viewport" content="width=device-width, initial-scale=1">`

---

## 📝 On-Page SEO

### Title Tag
- [ ] มี Title ทุกหน้า — ไม่ซ้ำกัน
- [ ] ความยาว 50-60 ตัวอักษร
- [ ] มี Primary keyword อยู่ข้างหน้า
- [ ] มีชื่อ Brand ต่อท้าย (เช่น `| CherCode`)
- [ ] ไม่ใช้ตัวพิมพ์ใหญ่ทั้งหมด

### Meta Description
- [ ] มี Description ทุกหน้า — ไม่ซ้ำกัน
- [ ] ความยาว 120-155 ตัวอักษร
- [ ] มี keyword + call-to-action
- [ ] มีราคาหรือ USP (ถ้าเป็น service page)

### Heading Structure
- [ ] มี `<h1>` เพียง 1 ตัวต่อหน้า
- [ ] H1 มี primary keyword
- [ ] Heading hierarchy ถูกต้อง (H1 → H2 → H3 ไม่ข้าม)
- [ ] ไม่ใช้ heading เป็น styling (ใช้ CSS แทน)

### URL Structure
- [ ] URL สั้น อ่านเข้าใจ (`/website/clinic` ไม่ใช่ `/page?id=123`)
- [ ] ใช้ hyphen `-` คั่นคำ (ไม่ใช่ underscore `_`)
- [ ] ไม่มี parameter ที่ไม่จำเป็น
- [ ] Lowercase ทั้งหมด

### Content
- [ ] เนื้อหาไม่ซ้ำกับหน้าอื่น (unique content)
- [ ] Word count เพียงพอ (blog ≥ 1,500 คำ, service page ≥ 800 คำ)
- [ ] Primary keyword อยู่ใน 100 คำแรก
- [ ] มี keyword variation ตามธรรมชาติ (ไม่ยัด keyword)
- [ ] มี internal links 3-5 ลิงก์ต่อ 1,000 คำ
- [ ] มี external links อ้างอิงแหล่งข้อมูลที่น่าเชื่อถือ

---

## 🖼️ Images

- [ ] ทุกรูปมี `alt` text ที่อธิบายภาพ (ภาษาไทยได้)
- [ ] ขนาดไฟล์ optimize แล้ว (ใช้ WebP หรือ AVIF)
- [ ] มี `width` และ `height` attribute (ป้องกัน CLS)
- [ ] รูปสำคัญมี `loading="eager"` หรือ `fetchpriority="high"`
- [ ] รูปที่ไม่สำคัญมี `loading="lazy"`
- [ ] ใช้ `<picture>` หรือ `srcset` สำหรับ responsive images
- [ ] ชื่อไฟล์มี keyword (`clinic-booking-system.webp` ไม่ใช่ `IMG_001.jpg`)

---

## 🔗 Structured Data (Schema Markup)

### ทุกเว็บไซต์ควรมี
- [ ] `Organization` — ชื่อ, logo, เบอร์, email, ที่อยู่, social links
- [ ] `WebSite` — ชื่อเว็บ, URL, ภาษา
- [ ] `BreadcrumbList` — navigation path ทุก inner page

### เว็บไซต์ธุรกิจ/บริการ
- [ ] `LocalBusiness` หรือ `ProfessionalService` — ข้อมูลธุรกิจ, เวลาเปิด-ปิด
- [ ] `Service` — รายการบริการ, ราคา
- [ ] `FAQPage` — คำถามที่พบบ่อย (ช่วยได้ rich results)

### Blog
- [ ] `BlogPosting` — title, author, datePublished, dateModified, image
- [ ] `Person` (author) — name, url, image

### E-commerce
- [ ] `Product` — name, price, availability, review
- [ ] `Review` / `AggregateRating`
- [ ] `Offer` — price, currency, availability

### ตรวจสอบ
- [ ] ทดสอบด้วย [Rich Results Test](https://search.google.com/test/rich-results)
- [ ] ไม่มี error ใน [Schema Markup Validator](https://validator.schema.org/)

---

## 🌐 International SEO (สำหรับเว็บสองภาษา TH/EN)

- [ ] `hreflang` tag ครบทุกหน้า: `th`, `en`, `x-default`
- [ ] hreflang อยู่ทั้งใน HTML `<head>` **และ** sitemap
- [ ] แต่ละภาษามี URL แยก (`/en/...` ไม่ใช่ query `?lang=en`)
- [ ] Canonical URL ชี้ไปเวอร์ชันภาษาของตัวเอง
- [ ] `og:locale` และ `og:locale:alternate` ตั้งค่าถูก
- [ ] เนื้อหาแปลจริง ไม่ใช่ Google Translate

---

## 📱 Social Media / Open Graph

- [ ] `og:title` — ทุกหน้า
- [ ] `og:description` — ทุกหน้า
- [ ] `og:image` — รูป 1200x630px ทุกหน้า
- [ ] `og:url` — canonical URL
- [ ] `og:type` — `website` (หน้าแรก) หรือ `article` (blog)
- [ ] `twitter:card` — `summary_large_image`
- [ ] `twitter:image` — เหมือน og:image
- [ ] ทดสอบด้วย [Facebook Sharing Debugger](https://developers.facebook.com/tools/debug/)

---

## 🤖 AI Search Readiness (GEO — 2026)

> Google AI Overviews, ChatGPT, Perplexity จะอ้างอิงเว็บที่มีโครงสร้างดี

- [ ] มี `/llms.txt` — อธิบายเว็บให้ AI อ่านเข้าใจ
- [ ] เนื้อหาตอบคำถามชัดเจน (answer-first format)
- [ ] มีสถิติ/ตัวเลข ที่ AI สามารถ quote ได้
- [ ] มีตาราง/ลิสต์สำหรับการเปรียบเทียบ
- [ ] FAQ schema ที่มีคำตอบละเอียด
- [ ] robots.txt อนุญาต GPTBot, ClaudeBot (ถ้าต้องการให้ AI อ้างอิง)

---

## 🇹🇭 เฉพาะเว็บไซต์ไทย

### ฟอนต์ภาษาไทย
- [ ] ใช้ Google Fonts ภาษาไทย (Noto Sans Thai, Sarabun, Prompt, etc.)
- [ ] Subset เฉพาะภาษาไทย (ลดขนาดไฟล์ 60-80%)
- [ ] `font-display: swap` ป้องกันข้อความหายขณะโหลด
- [ ] ใช้ไม่เกิน 2 ฟอนต์ (heading + body)

### PDPA (พ.ร.บ.คุ้มครองข้อมูลส่วนบุคคล)
- [ ] Cookie consent banner
- [ ] Privacy policy page
- [ ] ฟอร์มที่เก็บข้อมูลมี consent checkbox
- [ ] ข้อมูลสุขภาพ (คลินิก) ต้องมี explicit consent ตาม มาตรา 26

### Local SEO (ธุรกิจมีหน้าร้าน)
- [ ] Google Business Profile สร้างและ verify แล้ว
- [ ] NAP (ชื่อ, ที่อยู่, เบอร์) ตรงกันทุกที่
- [ ] Google Maps embed บนเว็บไซต์
- [ ] ขอ Google Review จากลูกค้า
- [ ] ลงทะเบียนใน directories ไทย (Wongnai, ThaiSME, Yellowpages.co.th)

---

## 🔧 เครื่องมือที่แนะนำ (ฟรี)

| เครื่องมือ | ใช้ทำอะไร |
|-----------|----------|
| [Google Search Console](https://search.google.com/search-console) | ติดตาม indexing, impressions, clicks |
| [Google Analytics 4](https://analytics.google.com/) | Traffic, behavior, conversions |
| [PageSpeed Insights](https://pagespeed.web.dev/) | Core Web Vitals |
| [Rich Results Test](https://search.google.com/test/rich-results) | ตรวจ Schema markup |
| [Schema Validator](https://validator.schema.org/) | Validate JSON-LD |
| [Lighthouse](https://developer.chrome.com/docs/lighthouse/) | Performance, A11y, SEO audit |
| [Ahrefs Webmaster Tools](https://ahrefs.com/webmaster-tools) | Backlinks, keywords (ฟรี) |
| [Screaming Frog](https://www.screamingfrog.co.uk/seo-spider/) | Crawl เว็บ (ฟรี 500 URLs) |

---

## วิธีใช้

1. Fork หรือ clone repo นี้
2. สร้าง issue ใน project ของคุณ แล้ว copy checklist ไปใช้
3. เช็คทีละหมวด ก่อน launch เว็บไซต์
4. ทำซ้ำทุก 3-6 เดือน เพื่ออัปเดตตาม algorithm ใหม่

```bash
# Clone
git clone https://github.com/chercode-dev/thai-seo-checklist.git
```

---

## Contributing

พบข้อผิดพลาด หรืออยากเพิ่มรายการ? ยินดีรับ PR ครับ!

1. Fork repo
2. สร้าง branch: `git checkout -b feature/add-new-item`
3. Commit: `git commit -m "add: new checklist item"`
4. Push: `git push origin feature/add-new-item`
5. สร้าง Pull Request

---

## Author

**Cher** — Full-Stack Developer & Founder of [CherCode](https://chercode.com)

บริการ[รับทำเว็บไซต์](https://chercode.com/website) AI และ Automation สำหรับธุรกิจไทย

- [chercode.com](https://chercode.com) — บริการเว็บไซต์ AI Automation
- [เว็บไซต์คลินิก](https://chercode.com/website/clinic) — ระบบนัดหมาย PDPA-ready
- [เว็บไซต์ร้านอาหาร](https://chercode.com/website/restaurant) — เมนูออนไลน์ จองโต๊ะ
- [AI Chatbot](https://chercode.com/ai/chatbot) — ตอบลูกค้า 24 ชม.
- [n8n Automation](https://chercode.com/automation/n8n) — ลดงานซ้ำ 60-80%

### บทความที่เกี่ยวข้อง
- [เว็บไซต์คลินิกที่ดี เช็คลิสต์ 15 ข้อ](https://chercode.com/blog/clinic-website-checklist)
- [PDPA กับเว็บไซต์คลินิก](https://chercode.com/blog/pdpa-clinic-website-guide)
- [เลือกฟอนต์ไทยสำหรับเว็บไซต์](https://chercode.com/blog/thai-web-font-guide)
- [ทำเว็บไซต์ราคาเท่าไหร่ 2026](https://chercode.com/blog/website-pricing-guide-2026)

---

## License

MIT License — ใช้ได้ฟรีทั้งส่วนตัวและเชิงพาณิชย์

---

*อัปเดตล่าสุด: มีนาคม 2026*
