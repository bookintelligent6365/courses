# BookIntelligent Learning Platform — Plan

## Vision
เปลี่ยน bookintelligent.com จาก blog ธรรมดา เป็น Learning Hub ที่มีรายได้ โดยใช้ asset ที่มีอยู่แล้ว (YouTube + Facebook + WordPress + Templates) ให้คุ้มค่าสูงสุด โดยไม่เสียค่าใช้จ่ายเพิ่ม

---

## Asset ที่มีอยู่แล้ว

| Asset | รายละเอียด |
|---|---|
| Website | bookintelligent.com (WordPress) |
| YouTube | @bookintelligent6509 — สอน Excel, GSheets, PowerBI, WebApp, สรุปหนังสือ |
| Facebook | BookIntelligent Page |
| Content | บทความ 34+ หน้า, templates หลายตัว |
| Templates ฟรี | Calendar, Tracker, Dashboard, Planner, Attendance, Inventory ฯลฯ |
| Skills | Google Sheets, Excel, Power BI, Web App, Dashboard |

---

## Tech Stack (Separated Course Site Version)

| ส่วน | เครื่องมือ | ค่าใช้จ่าย |
|---|---|---|
| เว็บหลัก / Blog / SEO | WordPress (bookintelligent.com) | มีอยู่แล้ว |
| เว็บคอร์ส / Landing Page | Static site บน GitHub Pages | ฟรี |
| โดเมนเว็บคอร์ส | เริ่มด้วย GitHub URL, ต่อไปใช้ learn.bookintelligent.com | ฟรีถ้าใช้ subdomain เดิม |
| รับชำระเงิน | WooCommerce บน WordPress หรือเริ่มด้วยโอนตรง/LINE | ฟรี / มีค่าธรรมเนียมตาม gateway |
| Payment ไทย | Omise หรือโอนตรงช่วง MVP | % ต่อ transaction / ฟรีถ้าโอนตรง |
| เนื้อหา video | YouTube Unlisted | ฟรี |
| ไฟล์ template | Google Drive | ฟรี |
| Email / ส่งมอบหลังซื้อ | WooCommerce email หรือ manual LINE ช่วงแรก | ฟรี |

---

## Architecture ใหม่

```
bookintelligent.com
├── หน้าแรก          → แนะนำคอร์ส + ปุ่มไปเว็บคอร์ส
├── Shop / Product   → WooCommerce product / checkout
├── Free Library     → Templates ฟรี / lead magnet
├── Blog             → บทความเดิมที่มีอยู่ (SEO)
└── Community        → link ไป Facebook Group

GitHub Pages / learn.bookintelligent.com
├── /                → หน้ารวมคอร์สทั้งหมด
├── /google-sheets-dashboard.html
├── /excel-dashboard.html
├── /apps-script-webapp.html
└── /power-bi-dashboard.html
```

**Flow หลัก:**
```
WordPress / YouTube / Facebook
        ↓
เว็บคอร์สแยกบน GitHub Pages หรือ learn.bookintelligent.com
        ↓
หน้ารายละเอียดคอร์ส + ปุ่มซื้อ
        ↓
กลับไป WooCommerce product / checkout บน bookintelligent.com
        ↓
จ่ายเงิน
        ↓
ได้รับ email พร้อมลิงก์ YouTube Unlisted + Google Drive
```

**เหตุผลที่ใช้เว็บคอร์สแยก:**
- ดีไซน์หน้า course catalog / landing page ได้อิสระกว่า WordPress
- ไม่เสี่ยง CSS ชนกับ theme/plugin เดิม
- Deploy ฟรีและเร็วผ่าน GitHub Pages
- WordPress ยังทำหน้าที่รับเงิน, เก็บ order, blog SEO และ customer account
- ต่อไปสามารถผูก subdomain `learn.bookintelligent.com` เพื่อให้ดูเป็นระบบเดียวกัน

---

## Course ที่วางแผนจะสร้าง

> Course series: BookIntelligent Dashboard & Automation Series
>
> แนวคิดหลัก: ใช้เนื้อหาฟรีบน YouTube เป็นบทนำ/ตัวอย่าง แล้วให้คอร์สเสียเงินเป็น project แบบ end-to-end พร้อมไฟล์ฝึกทำ, template, checklist และวิธีนำไปใช้กับงานจริง

### Course 1 — Google Sheets Dashboard Bootcamp (เริ่มก่อน)
> เหมาะสุดเพราะมี content และ template อยู่แล้วเยอะ ใช้เป็นคอร์สเปิดตัวเพื่อพิสูจน์ระบบขาย

| รายละเอียด | ข้อมูล |
|---|---|
| Positioning | จากข้อมูลดิบสู่ Dashboard พร้อมใช้ในงานจริง |
| กลุ่มเป้าหมาย | มนุษย์ออฟฟิศ, เจ้าของธุรกิจ SME, ฟรีแลนซ์, คนทำรายงาน |
| ราคา | Early bird 590 บาท / ปกติ 990 บาท |
| จำนวนบทเรียน | 24–26 ตอน |
| ความยาวต่อบท | 6–12 นาที |
| ความยาวรวม | 3.5–4.5 ชั่วโมง |
| Delivery | หน้า Course Site + YouTube Unlisted + Google Drive + WooCommerce email |
| สิ่งที่แถม | Practice file, final dashboard template, raw data 3 ชุด, PDF สูตรสำคัญ, dashboard checklist |

**โครงสร้าง:**
```
Module 1: เตรียมพื้นฐานและเป้าหมาย Dashboard
Module 2: เตรียมข้อมูลให้พร้อมวิเคราะห์
Module 3: สูตรสำคัญสำหรับ Dashboard (SUMIFS, COUNTIFS, FILTER, QUERY, IF/IFS)
Module 4: สร้าง Dashboard ตัวแรก (KPI, chart, filter, layout)
Module 5: Dashboard จากเคสจริง 3 แบบ (Sales / Expense / Task)
Module 6: ส่งมอบ แชร์ไฟล์ ป้องกันสูตรพัง และนำไปใช้ต่อ
```

### Course 2 — Excel Dashboard สำหรับงานออฟฟิศ

| รายละเอียด | ข้อมูล |
|---|---|
| Positioning | ทำรายงาน Excel ให้เป็น Dashboard ที่อัปเดตง่ายและใช้ประชุมได้จริง |
| กลุ่มเป้าหมาย | พนักงานออฟฟิศ, Sales Admin, HR, Accounting, Analyst beginner |
| ราคา | 790–1,290 บาท |
| จำนวนบทเรียน | 24–30 ตอน |
| ความยาวต่อบท | 6–12 นาที |
| ความยาวรวม | 4–5 ชั่วโมง |
| Delivery | หน้า Course Site + YouTube Unlisted + Excel practice files + WooCommerce email |
| สิ่งที่แถม | Excel dashboard template, raw data, Pivot checklist, report design checklist |

**โครงสร้าง:**
```
Module 1: เตรียมข้อมูลด้วย Excel Table
Module 2: สูตรสำคัญสำหรับรายงาน (XLOOKUP, SUMIFS, COUNTIFS, IF)
Module 3: PivotTable / PivotChart
Module 4: Slicer, Timeline และ interactive report
Module 5: Dashboard layout และ Conditional Formatting
Module 6: เคสจริง (Sales / HR Attendance / Inventory)
Module 7: เทคนิคทำไฟล์ให้ update ง่ายและไม่พัง
```

### Course 3 — Web App ด้วย Google Sheets + Apps Script

| รายละเอียด | ข้อมูล |
|---|---|
| Positioning | สร้าง Web App ใช้งานเอง โดยใช้ Google Sheets เป็นฐานข้อมูล |
| กลุ่มเป้าหมาย | เจ้าของธุรกิจ, admin, ฟรีแลนซ์, คนที่อยากสร้างระบบใช้เอง |
| ราคา | 1,490–2,490 บาท |
| จำนวนบทเรียน | 28–36 ตอน |
| ความยาวต่อบท | 8–15 นาที |
| ความยาวรวม | 5–7 ชั่วโมง |
| Delivery | หน้า Course Site + YouTube Unlisted + Google Drive + Apps Script source code |
| สิ่งที่แถม | Source code, starter template, deployment checklist, debugging checklist |

**โครงสร้าง:**
```
Module 1: Google Sheets เป็น database เบื้องต้น
Module 2: พื้นฐาน Google Apps Script
Module 3: สร้าง HTML Form และรับข้อมูลเข้า Sheet
Module 4: Auto ID, Timestamp, Validation และ Search
Module 5: ระบบ Lead Form / Booking / PO Request
Module 6: ส่ง email อัตโนมัติ
Module 7: Deploy เป็น Web App และตั้งค่าสิทธิ์
Module 8: ใช้ AI/Gemini ช่วยเขียนและแก้โค้ด
```

### Course 4 — Power BI Dashboard สำหรับธุรกิจ

| รายละเอียด | ข้อมูล |
|---|---|
| Positioning | สร้าง Dashboard ธุรกิจด้วย Power BI ตั้งแต่ข้อมูลดิบจนพร้อมนำเสนอ |
| กลุ่มเป้าหมาย | Analyst, Manager, เจ้าของธุรกิจ, คนทำรายงานองค์กร |
| ราคา | 1,490–2,990 บาท |
| จำนวนบทเรียน | 30–36 ตอน |
| ความยาวต่อบท | 8–15 นาที |
| ความยาวรวม | 5–7 ชั่วโมง |
| Delivery | หน้า Course Site + YouTube Unlisted + Power BI files + sample datasets |
| สิ่งที่แถม | PBIX template, sample data, DAX cheat sheet, dashboard UX checklist |

**โครงสร้าง:**
```
Module 1: เตรียมข้อมูลจาก Excel/CSV
Module 2: Power Query สำหรับ cleaning data
Module 3: Data model และ relationship
Module 4: DAX พื้นฐานและ measure สำคัญ
Module 5: KPI, Card, Chart, Matrix, Slicer
Module 6: Sales Dashboard / Market Share Dashboard / Executive Dashboard
Module 7: Dashboard UX สำหรับผู้บริหาร
Module 8: Publish, Export, Refresh และการนำไปใช้จริง
```

### Bundle / Learning Path

| Package | คอร์สที่รวม | ราคาแนะนำ |
|---|---|---|
| Dashboard Starter Bundle | Google Sheets Dashboard + Excel Dashboard | 1,790 บาท |
| Business Data Bundle | Excel Dashboard + Power BI Dashboard | 2,990 บาท |
| Automation Bundle | Google Sheets Dashboard + Web App Apps Script | 2,990 บาท |
| Full Dashboard & Automation Bundle | ทั้ง 4 คอร์ส | 5,900–6,900 บาท |

**ลำดับผลิตที่แนะนำ:**
```
1. Google Sheets Dashboard
2. Excel Dashboard
3. Power BI Dashboard
4. Web App + Apps Script
```

---

## Marketing Funnel

```
YouTube / Facebook (ฟรี — top of funnel)
        ↓
คลิกลิงก์ในคำบรรยาย → เว็บคอร์สแยก / หน้ารายละเอียดคอร์ส
        ↓
ลูกค้าสนใจ กดปุ่ม "ซื้อคอร์สนี้"
        ↓
กลับไป WooCommerce product / checkout บน WordPress
        ↓
จ่ายเงิน → ได้ email พร้อมลิงก์ YouTube Unlisted + Google Drive
        ↓
ดึงเข้า Facebook Group (community)
```

---

## Phases

### Phase 1 — Course Site Setup (1 สัปดาห์)
- สร้าง static course site สำหรับ 4 คอร์ส
- จัดไฟล์สำหรับ GitHub Pages (`index.html`, หน้ารายละเอียดแต่ละคอร์ส, `styles.css`, `assets/`)
- Deploy ขึ้น GitHub Pages
- เพิ่มเมนู/ปุ่มใน WordPress ให้ลิงก์ไปเว็บคอร์ส
- เตรียมแผนเปลี่ยนเป็น subdomain `learn.bookintelligent.com`

### Phase 2 — Payment & Delivery Setup (1 สัปดาห์)
- สร้าง WooCommerce product สำหรับ Google Sheets Dashboard
- ตั้งราคา Early bird / ราคาปกติ
- ตั้ง email หลังซื้อให้ส่งลิงก์ YouTube Unlisted + Google Drive
- เปลี่ยนปุ่มซื้อในเว็บคอร์สให้ลิงก์กลับไป WooCommerce product / checkout
- ทดสอบ flow: Course site → WooCommerce → จ่ายเงิน → รับลิงก์เรียน

### Phase 3 — Course Creation & Launch (2-3 สัปดาห์)
- อัด/จัด video บน YouTube Unlisted จนครบ
- เตรียมไฟล์ template / practice file บน Google Drive
- โปรโมทใน YouTube + Facebook
- รับนักเรียนรุ่นแรก (Early bird pricing) เพื่อทดสอบตลาด
- เปิด Facebook Group

### Phase 4 — Launch Optimization (1–2 สัปดาห์)
- โปรโมทใน YouTube + Facebook
- Early bird pricing
- เก็บ feedback นักเรียนรุ่นแรก
- ปรับหน้าเว็บคอร์สจากคำถามและ feedback จริง

### Phase 5 — Scale (ต่อเนื่อง)
- สร้าง Course 2: Excel Dashboard
- สร้าง Course 3: Power BI Dashboard
- สร้าง Course 4: Web App + Apps Script
- ทำ Bundle / Learning Path สำหรับขายหลายคอร์ส
- Email marketing สม่ำเสมอ
- YouTube SEO เพื่อดึง traffic ต่อเนื่อง
