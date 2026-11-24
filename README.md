# GeoField Mobile (GitHub Pages Bundle)

ชุดไฟล์สำหรับอัปโหลดขึ้น GitHub Pages เพื่อใช้งานแอปพลิเคชัน **GeoField Mobile** แบบออนไลน์และติดตั้งเป็น PWA บนมือถือ

## ไฟล์ในชุดนี้
- `index.html` — ตัวแอปพลิเคชัน GeoField Mobile ฉบับล่าสุด
- `manifest.json` — ค่ากำหนด PWA สำหรับติดตั้งลงหน้าจอมือถือ (iOS / Android)
- `sw.js` — Service Worker สำหรับแคชไฟล์และใช้งานภาคสนามแบบออฟไลน์
- `.nojekyll` — ป้องกัน GitHub Pages ประมวลผลไฟล์ด้วย Jekyll
- `icons/` — ไอคอนแอป (`apple-touch-icon.png`, `icon-192.png`, `icon-512.png`)

## ขั้นตอนการอัปโหลดขึ้น GitHub Pages
1. แตกไฟล์ `.zip` นี้ลงในเครื่อง
2. สร้าง Repository ใหม่บน GitHub (เช่น `geofield-mobile`) แบบ Public
3. อัปโหลดไฟล์ทั้งหมดในโฟลเดอร์นี้ (`index.html`, `manifest.json`, `sw.js`, `.nojekyll`, และโฟลเดอร์ `icons/`) ไปไว้ที่ **Root** ของ Branch `main`
4. ไปที่ **Settings > Pages** ของ Repository
5. ที่หัวข้อ **Build and deployment > Source** เลือก **Deploy from a branch** แล้วเลือก Branch `main` และโฟลเดอร์ `/ (root)` จากนั้นกด **Save**
6. รอประมาณ 1–2 นาที เว็บไซต์จะพร้อมใช้งานที่ `https://<username>.github.io/<repo-name>/`

## หมายเหตุสำหรับ Google Sign-In
หากเปิดใช้ระบบเข้าสู่ระบบด้วย Google (OAuth2) ให้นำโดเมน `https://<username>.github.io` ไปเพิ่มใน **Authorized JavaScript origins** ที่หน้า Google Cloud Console และใส่ `GOOGLE_CLIENT_ID` ในไฟล์ `index.html`
