# ข้าวแกงกะหรี่ยายใจ 🍛
### ใบงานที่ 7 — ฝึกสร้าง UI Components (Card, Menu, Modal) ด้วย Tailwind CSS

---

## โครงสร้างโปรเจ็กต์

```
curry-shop/
├── package.json          ← ไฟล์ตั้งค่าโปรเจ็กต์ Node.js
├── src/
│   ├── input.css         ← ไฟล์ CSS ต้นฉบับ (Tailwind v4)
│   ├── index.html        ← หน้าหลัก (Home)
│   ├── menu.html         ← หน้าเมนูอาหาร (Menu + Filter + Cards)
│   ├── about.html        ← หน้าเกี่ยวกับร้าน (About)
│   └── contact.html      ← หน้าติดต่อ (Contact + Form)
└── dist/
    └── output.css        ← ไฟล์ CSS ที่ Tailwind CLI สร้างให้ (หลัง build)
```

---

## วิธีติดตั้งและรัน (ใบงานที่ 6)

### ขั้นตอนที่ 1 — ติดตั้ง dependencies
```bash
npm install
```

### ขั้นตอนที่ 2 — Build CSS (ครั้งเดียว)
```bash
npm run build
```

### ขั้นตอนที่ 3 — Watch Mode (auto-compile เมื่อ save)
```bash
npm run watch
```

> หลัง build แล้ว ให้เปิดไฟล์ HTML แต่ละหน้าด้วย Browser  
> หรือใช้ Live Server Extension ใน VS Code

---

## หน้าเว็บทั้ง 4 หน้า

| หน้า | ไฟล์ | คำอธิบาย |
|------|------|----------|
| 1 | `index.html` | หน้าหลัก Hero + Featured Cards + Reviews |
| 2 | `menu.html` | เมนูอาหารครบ + Filter Pills + Modal รายละเอียด |
| 3 | `about.html` | ประวัติร้าน + Timeline + ปรัชญา |
| 4 | `contact.html` | ข้อมูลร้าน + ฟอร์มติดต่อ |

---

## Components ที่ใช้ (ตามใบงานที่ 7)

- ✅ **Card** — dish-card บนหน้าเมนูและหน้าหลัก (hover animation)
- ✅ **Menu** — Navbar responsive + Mobile hamburger + Filter pills
- ✅ **Modal** — Modal สั่งอาหาร, Modal รายละเอียดเมนู, Modal ขอบคุณ
- ✅ **Mobile-First** — Responsive ทุกหน้า (sm / md / lg breakpoints)
- ✅ **Flexbox + Grid** — ใช้ทั้งสองในการจัด Layout
- ✅ **ชื่อระบบ + โลโก้ + เมนู** — ครบทุกหน้า

---

## หมายเหตุ
- ไฟล์ HTML ปัจจุบันใช้ **CDN** (`cdn.tailwindcss.com`) เพื่อพรีวิวได้ทันที
- เมื่อต้องการ **Production** ให้รัน `npm run build` แล้วเปลี่ยน tag ใน `<head>` ทุกไฟล์เป็น:
  ```html
  <link href="../dist/output.css" rel="stylesheet"/>
  ```
  และลบ `<script src="https://cdn.tailwindcss.com">` ออก
