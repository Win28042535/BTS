# BTS Group Homepage Redesign — Concept Plan (Working Draft)

> สถานะ: วางแผน/ตกลงแนวทางแล้ว **ยังไม่ลงมือสร้าง mockup**
> อ้างอิงจาก: `BTS_Connected_Future.pdf` (concept doc), เว็บจริง btsgroup.co.th/th/home, blueprintapps.io (hero DNA reference)

## 1. Design DNA

### Typography
- **LINE Seed Sans TH** — ข้อความไทยทั้งหมด (headline/body)
- **LINE Seed Sans (EN)** — headline/ตัวเลขภาษาอังกฤษ
- **มีไฟล์ฟอนต์จริงแล้ว** (ไม่ต้องใช้ fallback อีกต่อไป) — เก็บที่ `C:\Users\pawin.s\Desktop\BTS\LINE_Seed_Sans_TH\LINE_Seed_Sans_TH_V1.003\Web\WOFF2\` ใช้ชุด Web (WOFF2) สำหรับ self-host ผ่าน `@font-face` ในเว็บจริง/mockup: `LINESeedSansTH_W_Th` (Thin), `_Rg` (Regular), `_Bd` (Bold), `_XBd` (ExtraBold), `_He` (Heavy) — ครบ 5 น้ำหนัก
- Section headline ระดับหัวข้อใหญ่ใช้สไตล์ all-caps ช่องไฟกว้างแบบ manifesto (เช่น "MOVE · MIX · MATCH")

### Icon DNA
- **Lucide** (lucide.dev) — เส้น outline, stroke-width 2px สม่ำเสมอ, มุมโค้งมน
- โหลดผ่าน jsdelivr, ใช้แบบ inline SVG
- ไอคอนที่เล็งไว้: `move`, `layers` (MIX), `link`/`handshake` (MATCH), `trending-up` (ตัวเลข), `network`

### Color (sample จริงจาก logo.svg ของเว็บ btsgroup.co.th)
| สี | Hex | บทบาท |
|---|---|---|
| BTS Blue | `#00599B` | Accent หลัก, CTA, ลิงก์ |
| BTS Red | `#ED1D24` | Accent รอง ใช้น้อย/เฉพาะจุด |
| Navy | `#23324E` | หัวข้อ, footer, dark section |
| Charcoal | `#292B2C` | body text |
| White/Cream | `#FFFFFF` + ครีมหินอ่อนอ่อน (จาก concept doc) | พื้นหลังหลัก (section สว่าง) |
| Near-black | `~#1B1B1B` (อ้างอิง blueprintapps.io) | พื้นหลัง section 2 (dark) |
| Silver/metallic gradient | เทาเงิน | กราฟิกเส้น-จุดเชื่อมโยง (node-line motif) ใช้แทน grid ธรรมดา |

## 2. Homepage Structure (7 Sections)

| # | Section | Perception Funnel stage | สถานะ |
|---|---|---|---|
| 1 | เชื่อมต่อความเป็นไปได้ (Hero) | ดึงดูด | วางแผนละเอียดแล้ว (ดูข้อ 16 — hero video concept) |
| 2 | หนึ่งกลุ่มธุรกิจ หลายความเชื่อมโยง | เกริ่น Ecosystem | วางแผนละเอียดแล้ว (ดูข้อ 3) |
| 3 | 3 แพลตฟอร์ม หนึ่งระบบนิเวศ (MOVE·MIX·MATCH) | ให้ความรู้ | วางแผนละเอียดแล้ว (ดูข้อ 4) |
| 4 | เครือข่ายที่ขับเคลื่อนธุรกิจ | ให้ความรู้ (ต่อ MATCH) | วางแผนละเอียดแล้ว (ดูข้อ 5) |
| 5 | การเชื่อมต่อที่สร้างผลกระทบ | พิสูจน์ (Impact) | วางแผนละเอียดแล้ว (ดูข้อ 9) — ไม่มีต้นแบบใน PDF เดิม, ออกแบบใหม่โดยอิง DNA จาก unitedcarriers.com "Why us" |
| 6 | ตัวเลขเบื้องหลังเครือข่าย (IR) | สร้างการมีส่วนร่วม | วางแผนคร่าวๆ (ย้ายจากตำแหน่งบนสุดเดิม → ท้ายหน้า แต่คง quick-access) |
| 7 | เรื่องราวจากเครือข่ายของเรา | สร้างการมีส่วนร่วม | วางแผนคร่าวๆ ปิดท้ายด้วย "Where will we connect next?" |

## 3. Section 2 — รายละเอียดที่ตกลงแล้ว (clone DNA จาก blueprintapps.io hero)

**อ้างอิง DNA จาก blueprintapps.io:**
- พื้นหลังเกือบดำ `rgb(27,27,27)` + grid เส้นบาง
- การ์ดภาพกระจายแบบ scattered mosaic (ขนาด/มุมไม่เท่ากัน มุมโค้งมน)
- Headline หนา 2 บรรทัดกลางจอ + subhead สั้น + CTA pill เดียว
- แต่ละการ์ดมี caption/label กำกับ (proof point)
- Nav แบบ floating pill

**การตัดสินใจสำหรับ BTS (ยืนยันแล้ว):**
1. **โทนพื้นหลัง**: มืดเกือบดำแบบ Blueprint ตรงๆ (ต่อเนื่องจาก Hero video เพื่อ journey ลื่นไหล ก่อนสลับสว่างที่ section 3)
2. **จำนวน/เนื้อหาการ์ด**: ยึด **4 การ์ดหลัก** ตาม diagram เดิมในเอกสาร — **People / Business / Data / Opportunities** โดยใช้ภาพจริงจาก Image DNA (Infrastructure/Human/Business/Future)
3. **Motion**: ใส่ **parallax เบื้องต้น** (การ์ดขยับความเร็วต่างกันตาม scroll/mouse)

**Mapping เพิ่มเติม:**
- Grid เส้นบางของ Blueprint → แทนด้วย motif เส้น-จุดเชื่อมโยงสีเงินของ BTS
- Headline กลางจอ: "ONE GROUP. MANY CONNECTIONS. ENDLESS POSSIBILITIES." + บรรทัดไทยรอง "เว็บไซต์ต้องทำให้ผู้ใช้รู้สึกถึงความเชื่อมต่ออย่างแท้จริง"
- CTA: "Explore BTS Group" / "สำรวจระบบนิเวศ BTS"
- Caption ใต้การ์ด: proof point สั้นๆ ต่อกลุ่ม (เช่น "People — ผู้โดยสารกว่า X ล้านคน/วัน", "Data — แพลตฟอร์มเชื่อมข้อมูล O2O")

> **หมายเหตุ**: Section 2 มี **เวอร์ชัน B และ C แบบคู่ขนาน** — B: clone จาก unitedcarriers.com/services "Our Services" (ดูข้อ 11), C: clone จาก unitedcarriers.com/careers "Why Join Us" (ดูข้อ 13) — ยังไม่ตัดสินใจว่าจะใช้เวอร์ชันไหนสร้างจริง

## 4. Section 3 — รายละเอียดที่ตกลงแล้ว (clone DNA จาก blueprintapps.io "What we do")

**อ้างอิง DNA จาก blueprintapps.io:**
- ไม่ใช่การ์ดนิ่งเรียงต่อกัน แต่เป็น **pinned feature module**: การ์ดเดียวตำแหน่งคงที่กลางจอ (rounded 24px, bg `#242424`, ทรงตั้ง) สลับภาพภายใน 4 สถานะตามจังหวะ scroll (pinned-scroll-crossfade)
- แต่ละสถานะภาพเป็นอุปมาโดยตรงของ claim ที่อยู่ใต้การ์ด (constellation, โปรไฟล์เดี่ยว, orbit rings, stat bubbles)
- Eyebrow label: จุดสี + ข้อความสั้น เหนือ headline
- Headline หนา 2 บรรทัด + subtext เทา 1 บรรทัดใต้การ์ดทุกสถานะ
- Intro paragraph มี highlight-on-scroll (คำค่อยๆ สว่างขึ้นตามการอ่าน) ก่อนเข้าโมดูลการ์ด

**การตัดสินใจสำหรับ BTS (ยืนยันแล้ว):**
1. **โทนพื้นหลัง**: การ์ดเข้ม (`#242424` หรือ navy `#23324E`) เป็น "เกาะ" ลอยบนพื้นครีม/ขาว — section 3 สลับเป็นโทนสว่างตามแผนเดิม (ตัดกับ section 1-2 ที่มืด)
2. **ภาพ MATCH**: ใช้กราฟิก steel-beam ตัด X ของเดิมจากเอกสาร concept ไปก่อน (อาจปรับเปลี่ยนภายหลังให้เข้าชุดเดียวกับ MOVE/MIX)
3. **Motion**: ทำ **pinned-scroll-crossfade แบบเต็ม** (การ์ดค้างตำแหน่งเดิม ภาพสลับตาม scroll progress เหมือนต้นแบบ)

**Mapping 3 สถานะ = 3 แพลตฟอร์ม:**

| Platform | Visual metaphor (แทน constellation/profile/orbit/bubbles) | Headline + Subtext |
|---|---|---|
| **MOVE** | เส้น route/จุด station พร้อม dot เคลื่อนที่ตามเส้นทาง (door-to-door journey) — ต่อยอด Layer 1 motif จากเอกสารเดิม | "MOVE — Transportation solution" / การสัญจร · คมนาคมขนส่ง · โครงสร้างพื้นฐาน · Door-to-door |
| **MIX** | กลุ่มไอคอน Lucide เล็ก (O2O, สื่อ, ดิจิทัล, กระจายสินค้า, ข้อมูล) ลอยรอบ node กลาง สีตาม BTS | "MIX — Connecting data & experience" / O2O · สื่อ · ดิจิทัล · การกระจายสินค้า · ข้อมูล |
| **MATCH** | กราฟิก steel-beam ตัด X ของเดิม | "MATCH — Connecting capability & opportunity" / พันธมิตร · ธุรกิจบริการ · ICT · บริการการเงิน · โอกาสใหม่ |

**องค์ประกอบที่ยืมมาตรงๆ**: eyebrow label แบบจุดสี ("● MOVE" ฯลฯ), headline หนา 2 บรรทัดใต้การ์ด + subtext เทาบรรทัดเดียว, ลิงก์ปลายทางไปหน้าธุรกิจเดิมที่มีอยู่แล้ว (/our-business/move, /mix, /match)

> **หมายเหตุ**: Section 3 มี **เวอร์ชัน B และ C แบบคู่ขนาน** — B: clone จาก unitedcarriers.com/about "Vision/Mission/Strategy" (ดูข้อ 10), C: clone จาก unitedcarriers.com (โฮมเพจ) "Our Services" sticky 2-คอลัมน์ (ดูข้อ 15) — ยังไม่ตัดสินใจว่าจะใช้เวอร์ชันไหนสร้างจริง

## 5. Section 4 (เครือข่ายที่ขับเคลื่อนธุรกิจ) — รายละเอียดที่ตกลงแล้ว (clone DNA จาก blueprintapps.io "The model works")

**อ้างอิง DNA จาก blueprintapps.io:**
- ไม่มีภาพประกอบเลย เน้นตัวพิมพ์ล้วน (ต่างจาก section 2/3 ที่เน้นภาพ) — สร้างจังหวะเปลี่ยนโทนของหน้า
- Eyebrow "● The model works" + headline หนา "Here's the proof."
- รายการตัวเลขใหญ่เรียงแนวตั้ง 4 ตัว (`<5%`, `94%`, `84%`, `86%`) ขนาด **60px น้ำหนัก regular (400)** สีขาวครีม `rgb(247,245,242)`
- แต่ละตัวเลข **เยื้องซ้าย-ขวาเพิ่มขึ้นทีละนิด** (cascade เฉียงลงขวา) — ค่าจริงที่ inspect ได้: left 24px → 24px → 39px → 104px
- คำอธิบาย 1-2 บรรทัดสีเทา `rgb(146,146,146)` ใต้ตัวเลขแต่ละตัว
- **Opacity ผูกกับ scroll**: ตัวเลขตรงจุดโฟกัส = opacity 1, ตัวถัดไปที่ยังไม่ถึง ≈ 0.6, ตัวไกลออกไป ≈ 0.01 — นับหลักฐานทีละตัวขณะเลื่อน

**การตัดสินใจสำหรับ BTS (ยืนยันแล้ว):**
1. **โทนพื้นหลัง**: คงสว่างต่อเนื่องจาก section 3 (ไม่สลับมืดตามต้นแบบ) — ใช้ตัวเลขสีเข้ม/navy (`#23324E`) แทนสีครีมขาวบนพื้นขาว
2. **แหล่งข้อมูลตัวเลข**: ใช้ placeholder ชั่วคราวใน mockup รอบแรก รอข้อมูลจริงจากทีมธุรกิจภายหลัง (จำนวนพันธมิตร, สัดส่วน ICT, ผลิตภัณฑ์การเงิน ฯลฯ)
3. **จำนวนตัวเลข**: ยึด **4 ตัว** ตามต้นแบบ (คัดจาก 5 หมวดของ MATCH เดิม — พันธมิตร/ธุรกิจบริการ/ICT/บริการการเงิน/โอกาสใหม่ เลือก 4 ที่มี impact สุด)
4. **Motion**: ทำ **cascade + opacity-fade แบบเต็ม** ตามต้นแบบ (ผูกกับ scroll progress เหมือน section 3)

**องค์ประกอบที่ยืมมาตรงๆ**: eyebrow + headline พิสูจน์, ตัวเลขใหญ่ 60px regular, cascade เยื้องซ้าย-ขวาทีละนิด, คำอธิบายเทา/navy ใต้ตัวเลข, opacity fade ตาม scroll focus

## 6. Footer — รายละเอียดที่ตกลงแล้ว (clone DNA จาก unitedcarriers.com/industries)

**อ้างอิง DNA จาก unitedcarriers.com/industries (mega-footer, 8 บล็อกคั่นด้วยเส้นแบ่ง):**
1. แถบดำคั่นต่อจาก nav
2. Tagline 2 บรรทัด ("One operator. Every leg of the journey.") ฟอนต์ `BT Steinhart` ตัวหนา
3. Segmented pill toggle ("INDUSTRIES / SERVICES") + marquee ticker เลื่อนแนวนอนอัตโนมัติ
4. Nav 2 คอลัมน์ ใต้ label mono uppercase ("COMPANY")
5. Secure Payments: คำอธิบาย + badge วิธีชำระเงิน
6. Hotline / Email / Office Hours (label mono + ค่าตัวหนา) + Socials (ปุ่มวงกลม outline)
7. Head Office + "Direction on Google" + Operating Across + แผนที่โลก dotted พร้อมจุดไฮไลต์
8. Legal utility grid (QHSE/Privacy/Terms/Payment/Delivery/Refund/Cookie)
9. Wordmark ghost ตัวใหญ่เต็มความกว้าง ("UNITED CARRIERS" ลาย dotted จาง)
10. แถบ copyright เล็กสุดท้าย

Typography เฉพาะ footer: label เล็ก uppercase ใช้ **mono font** (`BT Steinhart Mono`) ให้ความรู้สึก technical/manifest, heading/nav ใช้ `BT Steinhart` sans ตัวหนา

**การตัดสินใจสำหรับ BTS (ยืนยันแล้ว):**
1. **ขอบเขต**: ตัด **บล็อก "Secure Payments"** ออก (ไม่มี e-commerce ตรงๆ ในบริบทนี้) — เหลือ 7 บล็อก: Tagline → Pill toggle+ticker → Nav 2 คอลัมน์ → Contact+Socials → Head Office+Map → Legal grid → Wordmark ghost → Copyright
2. **เนื้อหา ticker/marquee**: รวมทุกอย่างเข้าด้วยกันในเส้นเดียว (ชื่อบริษัทในเครือ + sub-items ของ MOVE/MIX/MATCH + หัวข้อข่าวล่าสุด) จัดองค์ประกอบผสมกันเป็น ticker เดียว
3. **แผนที่**: โฟกัสเฉพาะเครือข่าย **BTS Skytrain ในกรุงเทพฯ** (ไม่รวมธุรกิจ/การลงทุนต่างประเทศ) — จุดไฮไลต์สถานีบนแผนที่ dotted โทนน้ำเงิน BTS
4. **Wordmark ghost**: ใช้ **"BTS GROUP"** ตรงๆ ตามต้นแบบ ตัวใหญ่เต็มความกว้าง ลาย dotted จาง
5. **Typography**: ใช้ **LINE Seed Sans ตัวปกติ** แทนทั้ง `BT Steinhart` และ `BT Steinhart Mono` (LINE Seed ไม่มีตัวแปร mono) — บล็อก label เล็ก uppercase จะจำลองความรู้สึก "technical label" ด้วยขนาดเล็ก + ตัวพิมพ์ใหญ่ + letter-spacing กว้าง + สีจางแทนการใช้ mono font จริง

**Mapping เนื้อหา:**

| บล็อก unitedcarriers | แปลงเป็นของ BTS |
|---|---|
| Tagline 2 บรรทัด | Reprise headline ปิดท้าย เช่น "One Group. Many Connections." หรือ "Connected Future, Today." |
| Pill toggle + ticker | Toggle **"MOVE / MIX / MATCH"** + ticker รวมชื่อบริษัทในเครือ/sub-items/ข่าว ตามข้อ 2 |
| Nav 2 คอลัมน์ | IA เดิม: เกี่ยวกับเรา / ธุรกิจของเรา / นักลงทุนสัมพันธ์ / การกำกับดูแลกิจการ / ความยั่งยืน / ข่าวสาร / สมัครงาน / ติดต่อ |
| Hotline/Email/Office Hours + Socials | คงรูปแบบเดิม ใส่ช่องทางติดต่อ IR/นักลงทุน + social ของ BTS Group |
| Head Office + Operating Across + dotted map | ที่อยู่สำนักงานใหญ่ BTS Group + จุดไฮไลต์เครือข่าย BTS Skytrain ในกรุงเทพฯ |
| Legal utility grid | ตรงกับ footer เดิมของเว็บอยู่แล้ว (Privacy Policy, Cookie Policy, Career, Contact, Sitemap, T&C) — reuse ตรงๆ |
| Wordmark ghost ใหญ่ | "BTS GROUP" |
| Copyright bar | คงข้อมูลลิขสิทธิ์เดิม |

## 7. Header (global component) — รายละเอียดที่ตกลงแล้ว (clone DNA จาก unitedcarriers.com/industries)

**อ้างอิง DNA จาก unitedcarriers.com/industries (inspect DOM/CSS จริง):**
- โครงสร้าง 2 แถว โปร่งใสทับ hero ตอนโหลด:
  - แถว utility บน: "CARBON CALCULATOR | LIVE TRACKING PORTAL" ตัวเล็ก mono uppercase สีขาวโปร่ง 60%
  - แถวหลัก: โลโก้ "UC" (ซ้าย) ... ไอคอน **dot-cluster ไล่ความทึบ** (5 จุด, opacity 0.24/0.5/0.7) + ข้อความ "MENU" (ขวา) — สอดคล้องกับ motif วงกลม/จุดจาก preloader ของแบรนด์
- **Scroll behavior (จาก CSS จริง)**:
  1. `.header.on-scroll` → พื้นหลังเปลี่ยนเป็นขาวทึบ+ตัวอักษรดำ (ปกติโปร่งใส+ขาว) ยกเว้น section ที่ mark เป็น dark จะโปร่งใสต่อ
  2. `.header.on-hide` → header เลื่อนซ่อนขึ้นเมื่อ scroll ลง, โผล่กลับเมื่อ scroll ขึ้น (auto-hide sticky)
  3. โลโก้มี 2 ส่วน (mark + full text) — ส่วน full หดความกว้างเป็น 0 ตอน scroll เหลือแต่ mark ย่อ
  4. Mobile: padding header แน่นขึ้นเมื่อ scroll
- **Full overlay menu**: ไอคอน dot-cluster มอร์ฟเป็น "CLOSE", list เมนูตัวใหญ่ uppercase (หน้าปัจจุบัน = ขาวตัวหนา, อื่นๆ = เทาจาง — ใช้ contrast น้ำหนัก/ความสว่างแทนสี), ปุ่ม CTA pill outline, เส้นคั่น, "CONNECT WITH US:" + อีเมล

**การตัดสินใจสำหรับ BTS (ยืนยันแล้ว):**
1. **แถว utility บน**: ใช้ทั้งหมดตามต้นแบบ — stock ticker ย่อ ("ราคาหุ้น BTS 2.00 ▼0.99%") + ลิงก์ IR ด่วน + ตัวสลับภาษา TH/EN รวมกันในแถวเดียว
2. **โครงสร้างเมนู**: คง **2 ระดับ** ไว้ (ตามเมนูเดิมของเว็บที่มี sub-item เยอะ เช่น นักลงทุนสัมพันธ์มีลิงก์ย่อย 10 รายการ) แต่ปรับสไตล์การแสดงผลตาม DNA นี้ (หน้าปัจจุบัน = ขาวตัวหนา, อื่นๆ = เทาจาง, list ตัวใหญ่ uppercase)
3. **Scroll behavior**: ทำเต็มรูปแบบตามต้นแบบ — transparent→white บน scroll, hide-on-scroll-down/show-on-scroll-up, โลโก้ collapse เหลือ mark ย่อ
4. **Dot-cluster icon**: ใช้แทนไอคอน hamburger เดิมของเว็บทั้งหมด — เชื่อมกับ motif เส้น-จุดเชื่อมโยงสีเงินที่ใช้ทั่วทั้งเว็บ (reuse element เดียวกัน)

**หมายเหตุ**: Header เป็น **global component** ทำงานร่วมกับทุก section (ไม่ใช่ 1 ใน 7 section ของ homepage) — ต้องรองรับทั้งพื้นหลังมืด (section 1-2) และสว่าง (section 3-4) ของหน้า

## 8. Loader (global component, ก่อนเข้าหน้า homepage) — รายละเอียดที่ตกลงแล้ว (clone DNA จาก unitedcarriers.com)

**อ้างอิง DNA จาก unitedcarriers.com (inspect CSS/DOM จริง — มี 2 loader):**

1. **`loader-page`** (ใช้ข้ามหน้า/มือถือ) — วงกลม 4 วงซ้อนศูนย์กลางเดียวกัน (`circ-1..4` ขนาด 30/45/60/75vmax เส้นขอบบาง) fade+ripple stagger แบบ sonar ping + wordmark fade เข้ากลางจอ, header ซ่อนระหว่างโหลด
2. **`loader-home`** (เฉพาะหน้าแรก, desktop, 3 คอลัมน์):
   - ซ้าย: โลโก้ + ลิสต์ประเทศเลื่อนเข้าทีละบรรทัด (stagger opacity)
   - กลาง: แผนที่โลกพร้อมจุด office (สีแบรนด์) / worldwide (สีเทา)
   - ขวา: ตัวนับ % progress + ลิสต์บริการเลื่อนเข้าทีละบรรทัด
3. **กลไก reveal (`loader-bg-mask`)**: circle-wipe 3 ชั้นสี — div วงกลม `width:0;height:0` แต่มี `box-shadow` แผ่ 100vmax (ไล่เฉดสี) บังเต็มจอ, ขยายขนาดวงกลมทำให้เกิด "รูม่านตา" โปร่งใสขยายจากศูนย์กลาง เผยหน้าเว็บจริง ซ้อน 3 ชั้น stagger เวลาต่างกันได้เอฟเฟกต์เปิดม่านตาไล่เฉดสีนุ่มๆ

**การตัดสินใจสำหรับ BTS (ยืนยันแล้ว):**
1. **ความเข้ม**: ทำเวอร์ชัน **rich เต็มรูปแบบแบบ `loader-home`** — 3 คอลัมน์: ซ้าย = ลิสต์บริษัทในเครือ/ธุรกิจ (BTS SkyTrain, VGI, Kerry Express, U City ฯลฯ) เลื่อนเข้าทีละบรรทัด, กลาง = แผนที่เครือข่าย BTS Skytrain กรุงเทพฯ (asset เดียวกับ footer), ขวา = ตัวนับ % + ลิสต์ "MOVE · MIX · MATCH" เลื่อนเข้าทีละบรรทัด
2. **สีของ iris-wipe**: ไล่เฉด **navy → charcoal → ครีม/ขาว** (จบที่โทนพื้นหลัง hero) แทนเฉดเทาของต้นแบบ
3. **ความถี่การแสดง**: **โชว์ทุกครั้งที่เข้าหน้าแรก** (ไม่ gate ด้วย sessionStorage แบบต้นแบบ)
4. **ระยะเวลา**: คุมให้เร็วใกล้เคียงต้นแบบ (~1 วินาที) ไม่ให้กวนใจผู้ใช้

**Synergy กับส่วนอื่นที่วางแผนไว้แล้ว**: วงแหวน sonar ต่อยอด motif เส้น-จุดเชื่อมโยงสีเงิน, แผนที่ BTS Skytrain reuse asset เดียวกับ footer, ลิสต์ขวาใช้ชื่อแพลตฟอร์ม MOVE/MIX/MATCH ที่ปรากฏซ้ำใน section 3 — ทำให้ loader ทำหน้าที่ "teaser" เนื้อหาในหน้าจริงตั้งแต่แรกเห็น

## 9. Section 5 (การเชื่อมต่อที่สร้างผลกระทบ) — รายละเอียดที่ตกลงแล้ว (clone DNA จาก unitedcarriers.com "Why us")

**อ้างอิง DNA จาก unitedcarriers.com (section "Why us" ก่อน testimonials):**
- ไม่มีการ์ดเลย ใช้ **ภาพถ่ายจริงแบบ pinned + parallax ช้า** เป็นฉากหลังตลอด section (ภาพเรือขนส่งสินค้ามุมสูง เลื่อนช้ากว่าหน้าจอ ให้ความรู้สึกภาพ "ปัก" อยู่กับที่)
- Eyebrow "WHY US" + headline ใหญ่กลางจอ ซ้อนทับภาพ
- 5 รายการเรียงต่อกันบนภาพเดียวกันตลอด แต่ละรายการมี: **ไอคอน dot-matrix/halftone เฉพาะตัว** (รูปทรงต่างกันแต่ละข้อ ทำจากจุดขาว) + headline หนา + คำอธิบาย 1-2 บรรทัดสีขาว, crossfade เข้า-ออกตามจังหวะ scroll โดยไม่มีกรอบการ์ด ข้อความลอยตรงบนภาพ
- Feel โดยรวม: cinematic/documentary เน้นภาพจริงเป็นหลักฐาน มากกว่ากราฟิกนามธรรม

**การตัดสินใจสำหรับ BTS (ยืนยันแล้ว):**
1. **ภาพพื้นหลัง**: ใช้ **ภาพเดียวคงที่ตลอด section** (ภาพจริงจาก Image DNA — Human/Future category) พร้อม parallax ช้าตามต้นแบบ + gradient scrim มืดทับภาพเพื่อให้ตัวอักษรขาวอ่านง่าย
2. **จำนวนข้อ**: ปรับเป็น **4 ข้อ** ให้สอดคล้อง pattern เดียวกับ section 4 (เครือข่ายที่ขับเคลื่อนธุรกิจ)
3. **เนื้อหา claim**: ใช้ **placeholder ชั่วคราว** ใน mockup รอบแรก รอข้อมูลจริงจากทีม ESG/Sustainability ภายหลัง (แนวทาง: ผู้โดยสาร/ชุมชน/ESG/พันธมิตร หรือความปลอดภัย — เลือก 4 จาก 5 แนวทางที่เสนอไว้)
4. **ไอคอน dot-matrix**: สร้างชุดไอคอนเฉพาะของ BTS ด้วยเทคนิค halftone dot เดียวกับต้นแบบ — **เชื่อมกับ motif จุดที่ใช้ใน loader (sonar ping rings) และ header (dot-cluster MENU icon) อยู่แล้ว** ทำให้ motif จุด/วงกลมกลายเป็นภาษาภาพร่วม (visual thread) ที่ปรากฏซ้ำตั้งแต่ loader → header → section 5

**Mapping เนื้อหา:**

| unitedcarriers | BTS |
|---|---|
| Eyebrow "WHY US" + headline | Eyebrow "IMPACT" + headline "การเชื่อมต่อที่สร้างผลกระทบจริง" / "CONNECTIONS THAT CREATE REAL IMPACT" |
| 5 รายการ + ไอคอน dot-matrix | 4 ข้อ claim เชิงผลกระทบ (placeholder เช่น ผู้โดยสาร/ชุมชน/ESG/พันธมิตร) แต่ละข้อมีไอคอน dot-matrix เฉพาะตัว |
| Text ลอยตรงบนภาพ | ใช้ตรงๆ พร้อม scrim มืด |

## 10. Section 3 — เวอร์ชัน B (ทางเลือกคู่ขนาน, clone DNA จาก unitedcarriers.com/about "Vision/Mission/Strategy")

**สถานะ**: บันทึกเป็น **ตัวเลือกคู่ขนาน** กับเวอร์ชัน A (Blueprint pinned-card crossfade, ดูข้อ 4) — ยังไม่ฟันธงว่าจะสร้างเวอร์ชันไหนจริง รอตัดสินใจภายหลัง

**อ้างอิง DNA จาก unitedcarriers.com/about (inspect DOM/CSS จริง):**
- กลไก **`position: sticky` แบบซ้อนทับกัน (stacking sticky panels)** — ไม่ใช่ pinned-card หรือ crossfade: panel เต็มจอค้างอยู่กับที่จนกว่า panel ถัดไปจะเลื่อนขึ้นมาคลุมทับไปเลย (เหมือนสไลด์การ์ดซ้อนทีละใบ)
- โครงสร้าง 3 panel เต็มความสูงจอ (VISION / MISSION / STRATEGY) แต่ละ panel มี **ภาพถ่ายเต็มพื้นหลัง (full-bleed) โทนสีเฉพาะตัวตามความหมาย**:
  - VISION: พื้นดำ + ภาพโลกจากอวกาศยามค่ำคืน (สเกลระดับโลก/แรงบันดาลใจ)
  - MISSION: โทนส้ม/อุ่น + ภาพตู้คอนเทนเนอร์สินค้าระยะใกล้ (จับต้องได้จริง)
  - STRATEGY: โทนน้ำเงินเข้ม + ภาพเครื่องบินพุ่งขึ้นพร้อมควันไอพ่น (ทิศทาง/แรงขับเคลื่อน)
- Layout เหมือนกันทุก panel: headline ตัวใหญ่หนาชิดซ้ายบน + พารากราฟคำอธิบายใต้ headline ไม่มี eyebrow label ไม่มีไอคอน ไม่มีกรอบการ์ด

**การตัดสินใจสำหรับ BTS (ยืนยันแล้ว):**
1. **สถานะ**: บันทึกเป็นตัวเลือกคู่ขนาน (เวอร์ชัน A/B) — ไม่ replace เวอร์ชัน A
2. **ภาพต่อแพลตฟอร์ม**: MOVE และ MIX ใช้ภาพถ่ายจริงจาก Image DNA, ส่วน **MATCH ยังคง reuse กราฟิก steel-beam ตัด X เดิม** — ผสมภาพถ่าย+กราฟิกในชุดเดียวกัน (ไม่บังคับให้ทั้ง 3 เป็นภาพถ่ายล้วน)
3. **โทนสีต่อ panel**: ให้แต่ละแพลตฟอร์มมีโทนสีเฉพาะตัวแบบต้นแบบ — เสนอ MOVE = น้ำเงิน BTS (`#00599B`), MIX = เทาเงิน/metallic (silver gradient), MATCH = แดง BTS (`#ED1D24`) หรือ navy (`#23324E`)
4. **Motion**: ทำกลไก **sticky-stack เต็มรูปแบบ** ตามต้นแบบ (panel ถัดไปเลื่อนขึ้นคลุมทับ panel ก่อนหน้า)

**Mapping เนื้อหา:**

| unitedcarriers | BTS (เวอร์ชัน B) |
|---|---|
| Headline ใหญ่ชิดซ้ายบน + พารากราฟ | ชื่อแพลตฟอร์ม (MOVE/MIX/MATCH) + นิยามใหม่ที่ร่างไว้แล้วในเวอร์ชัน A (เช่น "MOVE — Transportation solution ที่เน้น door-to-door") |
| ภาพ full-bleed โทนสีเฉพาะตัว | MOVE = ภาพขบวนรถไฟฟ้ากำลังเคลื่อนที่ (โทนน้ำเงิน), MIX = ภาพเมือง/ข้อมูลยามค่ำคืน (โทนเทาเงิน), MATCH = กราฟิก steel-beam เดิม (โทนแดง/navy) |
| ไม่มีการ์ด/กรอบ | ใช้ตรงๆ — เวอร์ชัน B ให้ความรู้สึก cinematic เต็มจอ ต่างจากเวอร์ชัน A ที่มีกรอบการ์ดชัดเจน |

## 11. Section 2 — เวอร์ชัน B (ทางเลือกคู่ขนาน, clone DNA จาก unitedcarriers.com/services "Our Services")

**สถานะ**: บันทึกเป็น **ตัวเลือกคู่ขนาน** กับเวอร์ชัน A (Blueprint photo collage กระจายบนพื้นมืด, ดูข้อ 3) — ยังไม่ฟันธงว่าจะสร้างเวอร์ชันไหนจริง รอตัดสินใจภายหลัง

**อ้างอิง DNA จาก unitedcarriers.com/services (inspect จริง):**
- ไม่มี pinned/parallax/crossfade เลย เป็น **list แบบ editorial เรียบง่าย** อ่านง่ายเหมือน directory
- Intro: "OUR SERVICES" + headline + คำอธิบายสั้น
- แบ่ง 2 กลุ่ม สลับพื้นหลังเข้ม-อ่อนแบบ **ตัดชัด (hard cut ไม่ fade)**: CORE SERVICES (พื้นดำ, 6 รายการ) / INTEGRATED SOLUTIONS (พื้นขาว, 6 รายการ)
- แต่ละแถว: ไอคอน **dot-matrix เฉพาะตัว** (บ้าน, ตะขอเครน, เครื่องหมายถูก ฯลฯ) + headline หนา + tagline 1 บรรทัด + จุดกลมเล็กชิดขวา (ตกแต่ง/ตัวคั่น) + เส้นแบ่งบางระหว่างแถว

**การตัดสินใจสำหรับ BTS (ยืนยันแล้ว):**
1. **สถานะ**: บันทึกเป็นตัวเลือกคู่ขนาน (เวอร์ชัน A/B) — ไม่ replace เวอร์ชัน A
2. **การแบ่งกลุ่ม**: ใช้ 2 กลุ่มจาก 4 node เดิม — **"การเชื่อมโยงหลัก" (People + Business)** และ **"การเชื่อมโยงขยาย" (Data + Opportunities)**
3. **สีพื้นหลังสลับ**: **กลับด้าน** จากที่เสนอไว้ — "การเชื่อมโยงหลัก" (People + Business) = พื้น**อ่อน/ครีม-ขาว**, "การเชื่อมโยงขยาย" (Data + Opportunities) = พื้น**เข้ม/navy**
4. **จุดคั่นขวา**: เป็นแค่ตกแต่งเหมือนต้นแบบ (ไม่ทำเป็นลิงก์คลิกได้)

**Mapping เนื้อหา:**

| unitedcarriers | BTS (เวอร์ชัน B) |
|---|---|
| Intro "OUR SERVICES" + headline | Intro "OUR CONNECTIONS" + headline "ONE GROUP. MANY CONNECTIONS." (ข้อความเดิมจากเวอร์ชัน A) |
| CORE SERVICES (พื้นดำ) / INTEGRATED SOLUTIONS (พื้นขาว) | "การเชื่อมโยงหลัก" People+Business (พื้นอ่อน/ครีม-ขาว) / "การเชื่อมโยงขยาย" Data+Opportunities (พื้นเข้ม/navy) |
| ไอคอน dot-matrix ต่อแถว | ไอคอน dot-matrix เฉพาะตัวต่อ node (คน, ตึก/ธุรกิจ, ข้อมูล/กราฟ, ไอเดีย/โอกาส) — เชื่อมกับ motif จุดที่ใช้ใน loader/header/section 5 อยู่แล้ว |
| Headline + tagline 1 บรรทัด + จุดคั่นขวา (ตกแต่ง) | ชื่อ node + proof point สั้น (เช่น "People — ผู้โดยสารกว่า X ล้านคน/วัน") + จุดคั่นขวาตกแต่งเหมือนต้นแบบ |

## 13. Section 2 — เวอร์ชัน C (ทางเลือกคู่ขนาน, clone DNA จาก unitedcarriers.com/careers "Why Join Us")

**สถานะ**: บันทึกเป็น **เวอร์ชัน C คู่ขนาน** กับเวอร์ชัน A (Blueprint photo collage, ข้อ 3) และเวอร์ชัน B (Our Services 2-กลุ่มสลับสี, ข้อ 11) — ยังไม่ฟันธงว่าจะสร้างเวอร์ชันไหนจริง

**อ้างอิง DNA จาก unitedcarriers.com/careers (section "Why Join Us"):**
- Eyebrow "WHY JOIN US" + headline ใหญ่ + พารากราฟอินโทรสั้น บนพื้นดำล้วน
- List ต่อเนื่อง 9 รายการ **ไม่มีการแบ่งกลุ่ม/สลับสีพื้นหลัง** (ต่างจากเวอร์ชัน B ที่มี 2 กลุ่มสีตัดกัน) — ทั้ง section เป็นพื้นเข้มเดียวตลอด
- แต่ละแถว: ไอคอน **dot-matrix เฉพาะตัว** (กุญแจ, ตึก/สกายไลน์ ฯลฯ) ที่ **ค่อยๆ ก่อตัวจากจุดกระจายเป็นรูปทรงตอน scroll เข้า viewport** + headline หนา + คำอธิบาย 2-3 บรรทัด + เส้นแบ่งบางระหว่างแถว
- สรุป DNA: ภาษาภาพเดียวกับเวอร์ชัน B (ไอคอน dot-matrix + headline + description + divider) แต่เรียบง่ายกว่า ไม่มีการแบ่งกลุ่มสี

**การตัดสินใจสำหรับ BTS (ยืนยันแล้ว):**
1. **สถานะ**: บันทึกเป็นเวอร์ชัน C คู่ขนานกับ A และ B
2. **สีพื้นหลัง**: ใช้ **navy (`#23324E`)** เดียวตลอด section แทนสีดำล้วนของต้นแบบ
3. **จำนวนรายการ**: คงแค่ **4 node เดิม** (People/Business/Data/Opportunities) ไม่ขยายเป็น 9 แบบต้นแบบ
4. **แอนิเมชัน**: ทำ **icon ก่อตัวจากจุดกระจายเต็มรูปแบบ** ตามต้นแบบ (ไอคอนค่อยๆ รวมจากจุดกระจายเป็นรูปทรงตอน scroll เข้า viewport)

**Mapping เนื้อหา:**

| unitedcarriers | BTS (เวอร์ชัน C) |
|---|---|
| Eyebrow "WHY JOIN US" + headline | Eyebrow เดิม + headline "ONE GROUP. MANY CONNECTIONS. ENDLESS POSSIBILITIES." |
| List ต่อเนื่อง พื้นดำเดียวตลอด | List 4 node เดิม เรียงต่อเนื่องบนพื้น navy เดียว ไม่สลับสี |
| ไอคอน dot-matrix ก่อตัวตอน scroll | ไอคอนต่อ node (คน/ตึก/กราฟข้อมูล/ไอเดีย) พร้อมแอนิเมชันก่อตัวจากจุด — เชื่อม motif จุดเดิมที่ใช้ทั่วเว็บ (loader/header/section 5) |
| Headline + description + divider | ชื่อ node + proof point + เส้นแบ่ง |

## 15. Section 3 — เวอร์ชัน C (ทางเลือกคู่ขนาน, clone DNA จาก unitedcarriers.com โฮมเพจ "Our Services")

**สถานะ**: บันทึกเป็น **เวอร์ชัน C คู่ขนาน** กับเวอร์ชัน A (Blueprint pinned-card, ข้อ 4) และเวอร์ชัน B (Vision/Mission/Strategy sticky-stack, ข้อ 10) — ยังไม่ฟันธงว่าจะสร้างเวอร์ชันไหนจริง

**อ้างอิง DNA จาก unitedcarriers.com โฮมเพจ (section "Our Services" — คนละแบบกับ "Our Services" ของหน้า `/services` ที่ clone เป็น Section 2 เวอร์ชัน B):**
- Headline two-tone: "EVERYTHING YOUR FREIGHT NEEDS. **UNDER ONE GROUP.**" (บรรทัดแรกขาวเข้ม บรรทัดหลังเทาจาง) + พารากราฟอินโทร บนพื้นดำล้วน
- เลย์เอาต์ **2 คอลัมน์**: ซ้าย = **ภาพประกอบ flat illustration แบบ sticky** ค้างอยู่กับที่ และ **สลับภาพตามกลุ่มบริการที่ scroll ผ่าน** (รถเทรลเลอร์ตู้คอนเทนเนอร์ → เครนยก reach-stacker), ขวา = list บริการเลื่อนผ่าน (6 รายการ) แต่ละแถวมีไอคอน dot-matrix + headline + คำอธิบาย + เส้นแบ่ง
- ปิดท้าย section ด้วย **ghost wordmark ตัวใหญ่จาง** คล้าย motif เดียวกับ footer

**การตัดสินใจสำหรับ BTS (ยืนยันแล้ว):**
1. **สถานะ**: บันทึกเป็นเวอร์ชัน C คู่ขนานกับ A และ B
2. **จำนวนรายการใน list**: คัดมา**แพลตฟอร์มละ 3-4 รายการเด่น** จาก sub-item เดิม (ไม่ใส่ครบทุกรายการ) — MOVE เลือกจาก การสัญจร/คมนาคมขนส่ง/โครงสร้างพื้นฐาน/Door-to-door, MIX เลือกจาก O2O/สื่อ/ดิจิทัล/กระจายสินค้า/ข้อมูล, MATCH เลือกจาก พันธมิตร/ธุรกิจบริการ/ICT/บริการการเงิน/โอกาสใหม่
3. **โทนพื้นหลัง**: **navy** (`#23324E`) แทนดำล้วนของต้นแบบ ให้เข้าธีม BTS
4. **ภาพประกอบ sticky**: **MOVE และ MIX ใช้ภาพถ่ายจริง** (จาก Image DNA) แทน flat illustration ของต้นแบบ ส่วน **MATCH ยังคงใช้กราฟิก steel-beam เดิม** — ผสมภาพถ่าย+กราฟิกในคอลัมน์ซ้ายเดียวกัน สลับ 3 ช่วงตามกลุ่มที่ scroll ผ่าน

**Mapping เนื้อหา:**

| unitedcarriers | BTS (เวอร์ชัน C) |
|---|---|
| Headline two-tone | "3 แพลตฟอร์ม หนึ่งระบบนิเวศ" (navy เข้ม) / "MOVE · MIX · MATCH" (เทาจาง) |
| ภาพประกอบ sticky สลับตามกลุ่ม | MOVE = ภาพถ่ายขบวนรถไฟฟ้า, MIX = ภาพถ่ายเมือง/ข้อมูลยามค่ำคืน, MATCH = กราฟิก steel-beam เดิม |
| List 6 บริการ + ไอคอน dot-matrix | List คัดสรร 3-4 รายการต่อแพลตฟอร์ม (~10-12 แถวรวม) ไอคอน dot-matrix เฉพาะตัวต่อ item |
| Ghost wordmark ปิดท้าย | "ECOSYSTEM" หรือ "MOVE · MIX · MATCH" ตัวใหญ่จาง |

## 16. Section 1 (เชื่อมต่อความเป็นไปได้ / Hero) — Hero Video Concept

**เป้าหมาย**: ตามเอกสาร concept เดิม วิดีโอต้องสื่อ "WHO WE CONNECT" และ "MANY CONNECTIONS. ONE GROUP." ให้รับรู้ได้ภายใน 15 วินาทีแรก — เปลี่ยนการรับรู้จาก "แค่รถไฟฟ้า" เป็น "เครือข่ายที่เชื่อมโยงทุกมิติของเมือง" (สร้างการรับรู้ใหม่)

**โครงเรื่อง (Shot List) — วนลูป 15-18 วินาที:**

| ช่วงเวลา | ภาพ | Image DNA category | Text overlay |
|---|---|---|---|
| 0-4s | โดรนมุมสูงจับภาพรถไฟฟ้า BTS วิ่งผ่านเมืองยามเช้า/โกลเด้นอาวร์ | Infrastructure | "Moving people." |
| 4-8s | Match-cut ผ่าน motif เส้น-จุดสีเงิน (เส้นทางรถไฟยืดออกกลายเป็นเส้นเชื่อมข้อมูล) → คนหลากหลายบนสถานี/ในเมือง | Human | (เส้นเชื่อมขยับไปภาพถัดไป) |
| 8-12s | เส้นบรรจบเป็นจุด hub (สะท้อน diagram "ONE GROUP") → ตัดเข้าภาพบรรยากาศธุรกิจจริง (ตึกกระจก/ประชุม) | Business | "Connecting businesses." |
| 12-16s | เส้นขยายออกอีกครั้งสู่ภาพเมืองแห่งอนาคต (ตึกสีเขียว/โซลาร์) | Future | "Creating possibilities." |
| 16-18s | วนกลับเข้าภาพแรกด้วย motif เส้นเดิม (loop ไร้รอยต่อ) | — | โลโก้ + CTA "Explore BTS Group" |

**จุดเชื่อมกับสิ่งที่วางแผนไว้แล้ว:**
- motif เส้น-จุดสีเงินเป็นตัวเชื่อมทุกช็อต (transition) — element เดียวกับ loader/header/section 5/6
- สีเปิดวิดีโอต่อเนื่องจาก iris-wipe ของ loader (navy→charcoal→ครีม) ให้ transition จาก loader เข้า hero ไร้รอยต่อ
- Copy ใช้ของเดิมที่ยืนยันแล้ว: "Moving people. Connecting businesses. Creating possibilities." sync กับจังหวะภาพ
- คงปุ่ม "View Full VDO" ไว้เหมือนเว็บปัจจุบัน (ลิงก์ไป YouTube เวอร์ชันเต็ม)

**การตัดสินใจสำหรับ BTS (ยืนยันแล้ว):**
1. **แหล่งภาพ**: ใช้ฟุตเทจจริงของ BTS (จากคลังที่มีอยู่) ไปก่อน — ไม่ถ่ายทำ/หา stock ใหม่ในรอบนี้
2. **ความยาว loop**: **15-18 วินาที** ตามที่ร่าง
3. **เสียง**: **ไม่ต้องคิดเรื่องเสียง** ในรอบนี้ (mute-by-default ตาม pattern ปกติของ hero video)
4. **"Full VDO" เวอร์ชันยาว**: **นอก scope รอบนี้** — โฟกัสแค่ loop สั้นสำหรับ hero background เท่านั้น ปุ่ม "View Full VDO" คงไว้แต่ไม่ต้อง storyboard เวอร์ชันยาวตอนนี้

## 17. Next Step (ยังไม่ลงมือ)

- ใช้ token ชุดนี้เป็นฐาน: สีจาก logo.svg จริง + ฟอนต์ LINE Seed Sans TH จริง (self-host WOFF2) + ไอคอน Lucide
- Section อื่นที่ยังไม่ลงรายละเอียดระดับ section 2 (6, 7) จะออกแบบเพิ่มเติมระหว่าง build หรือรอ brief เพิ่มจากผู้ใช้

## 18. Build Kickoff — เริ่มสร้าง Mockup จริง (ทีละ Section)

**สถานะ**: เริ่มลงมือ build แล้ว (ไม่ใช่แค่วางแผน)

**Tech stack ที่ยืนยัน:**
- Artifact เดียว (HTML) publish ซ้ำ URL เดิมทุกครั้งที่เพิ่ม section
- ฟอนต์ LINE Seed Sans TH จริง (self-host WOFF2 จาก path ข้างบน) แทน fallback เดิม
- Lucide icon ผ่าน jsdelivr, dot-matrix icon วาดมือเป็น SVG
- Motion: vanilla JS + IntersectionObserver/scroll listener
- ภาพ/วิดีโอจริงยังไม่มีให้ใช้ — ใช้ placeholder คั่นตำแหน่งไว้ก่อน

**ลำดับ build**: Foundation+Header → Section 1 (Hero) → Section 2 → Section 3 → Section 4 → Section 5 → Section 6+7 → Footer → Loader → Polish

**การตัดสินใจสำหรับรอบ build นี้ (ยืนยันแล้ว):**
1. **Section 2**: build **เวอร์ชัน A** ก่อน (Blueprint photo collage) — B และ C เก็บไว้เป็นทางเลือกทีหลัง
2. **Section 3**: build **เวอร์ชัน A** ก่อน (Blueprint pinned-card crossfade) — B และ C เก็บไว้เป็นทางเลือกทีหลัง
3. **ฟอนต์**: ใช้ไฟล์จริงจาก `C:\Users\pawin.s\Desktop\BTS\LINE_Seed_Sans_TH\` (self-host ผ่าน Artifact `files`)
4. **Responsive**: ช่วงเริ่ม build **ยังไม่ต้องคำนึงถึง** — เน้นเลย์เอาต์ PC/desktop ก่อน ค่อยทำ responsive ทีหลังเป็น pass แยก (จะไม่เสียเวลาไปกับ media query ระหว่างต่อ section ใหม่แต่ละรอบ)

**Build log:**
- **รอบ 1 (เสร็จแล้ว)**: Foundation (design tokens, @font-face 5 น้ำหนัก) + Header (global, scroll behavior เต็มรูปแบบ, full overlay menu 2 ระดับ, dot-cluster icon) + Section 1 Hero (static shell: headline/subcopy/CTA/motif เส้น-จุด ตามที่ตกลง — วิดีโอจริงยังไม่ใส่ เพราะยังไม่มีฟุตเทจ ใช้ gradient+motif แทนตำแหน่งไปก่อน)
  - Artifact: https://claude.ai/artifact/SA1qEi8p8yaPUeQeXmham7
  - โลโก้ใช้ SVG จริงจาก btsgroup.co.th/storage/logo.svg (ไม่ใช่ของจำลอง)
  - ข้อจำกัดที่รู้ตัว: หน้ายังสูงแค่ 100vh (มีแค่ hero) จึงยังทดสอบ header hide-on-scroll ไม่ได้เต็มที่ รอ section 2 เข้ามาต่อ
- **รอบ 2 (เสร็จแล้ว)**: Section 2 เวอร์ชัน A — headline "ONE GROUP. MANY CONNECTIONS. ENDLESS POSSIBILITIES." กลางจอ, การ์ด 4 ใบ (People/Business/Data/Opportunities) กระจายรอบ motif เส้น-จุดเชื่อมสู่ศูนย์กลาง, parallax ตาม scroll (ความเร็วต่างกันต่อการ์ด), ใช้ icon-tile ไล่สี BTS blue/red/silver แทนภาพถ่ายจริง (ยังไม่มีคลังภาพให้ใช้)
  - Focus **PC/desktop ก่อนตามที่ตกลง** — ยังไม่ทำ responsive breakpoint ละเอียด
  - Artifact เดิม อัปเดตแล้ว (Version 2): https://claude.ai/artifact/SA1qEi8p8yaPUeQeXmham7
- **รอบ 3 (เสร็จแล้ว)**: Section 3 เวอร์ชัน A — พื้นครีม (สลับสว่างจาก section 1-2), intro 2 คอลัมน์: headline "3 แพลตฟอร์ม หนึ่งระบบนิเวศ" + พารากราฟ highlight-on-scroll (คำสว่างขึ้นทีละวลี, MOVE/MIX/MATCH เป็นสีน้ำเงิน), ตามด้วย pinned module (สูง 390vh, sticky 100vh) 3 คอลัมน์:
  - ซ้าย: rail MOVE/MIX/MATCH พร้อมแถบ progress ตาม scroll (คลิกเพื่อข้ามไปแต่ละแพลตฟอร์มได้)
  - กลาง: การ์ด navy rounded 24px (dot-grid จาง) crossfade 3 ฉาก — MOVE = เส้นทาง metro-style HOME→DESTINATION + dot วิ่งตามเส้น (เดิน/รถไฟฟ้า BTS/ฟีดเดอร์/ส่งถึงที่), MIX = hub "MIX" + ไอคอน Lucide 5 ตัวโคจรรอบ (O2O/สื่อ/ดิจิทัล/กระจายสินค้า/ข้อมูล), MATCH = คาน steel-beam 2 ท่อนเลื่อนเข้ามาตัดกันเป็น X + แผ่นเพลทจุดแดงตรงกลาง + chip 4 หมวด; ใต้การ์ด eyebrow จุดสี + headline 2 บรรทัด + subtext เทา + ลิงก์ /our-business/move|mix|match
  - ขวา: ตัวนับ 01/02/03 ตัวบาง (Thin) ขนาดใหญ่
  - MATCH วาดกราฟิก steel-beam ขึ้นใหม่เป็น SVG (ยังไม่มีไฟล์ต้นฉบับจากเอกสาร concept) — เปลี่ยนเป็นภาพจริงได้ภายหลัง
  - ไฟล์ต้นฉบับหน้าเว็บ: scratchpad ของ session นี้ `bts-mockup/index.html` (fonts อยู่ใน Artifact แล้ว ไม่ต้องอัปซ้ำ)
  - Artifact เดิม อัปเดตแล้ว (Version 3): https://claude.ai/artifact/SA1qEi8p8yaPUeQeXmham7
- **รอบ 4 (เสร็จแล้ว)**: Section 4 เครือข่ายที่ขับเคลื่อนธุรกิจ — พื้นครีมต่อจาก section 3 (คั่นด้วยเส้นบาง), 2 คอลัมน์: ซ้าย sticky = eyebrow จุดแดง + headline "เครือข่ายที่ทำงานได้จริง / นี่คือหลักฐาน" + lede + ป้าย "ตัวเลขตัวอย่าง · รอข้อมูลจริงจากทีมธุรกิจ", ขวา = ตัวเลข 4 ตัว 60px/400 สี navy เยื้อง cascade 24→24→39→104px ตามต้นแบบ, label หมวดสีน้ำเงินเหนือตัวเลข + คำอธิบายเทาใต้ตัวเลข
  - 4 หมวดที่เลือก (ตัด "โอกาสใหม่"): พันธมิตร 200+ / ธุรกิจบริการ 40 บริษัท / ICT 98% / บริการการเงิน 1.2 ล้านราย — **ทั้งหมดเป็น placeholder**
  - Opacity ตาม scroll: ตัวที่ใกล้กึ่งกลางจอ = 1, ตัวถัดไป = 0.6, ตัวที่ผ่านไปแล้ว = 0.18, ตัวไกลออกไป = 0.01 (prefers-reduced-motion = แสดงทึบทั้งหมด)
  - Artifact เดิม อัปเดตแล้ว (Version 4): https://claude.ai/artifact/SA1qEi8p8yaPUeQeXmham7
- **รอบ 5 (เสร็จแล้ว)**: Section 5 การเชื่อมต่อที่สร้างผลกระทบ — pinned stage (สูง 440vh, sticky 100vh) ภาพเดียวค้างเป็นฉากหลังพร้อม parallax ช้า (-18vh ตลอด section) + scrim มืดซ้าย→ขวาและล่าง
  - ภาพพื้นหลัง: ยังไม่มีภาพจริง → วาด placeholder ด้วย canvas (เมืองยามเย็น + รางยกระดับ + ขบวนรถไฟฟ้า) พร้อมป้าย "ภาพตัวอย่าง · แทนที่ด้วยภาพจริงหมวด Human / Future"
  - ซ้าย: eyebrow "IMPACT" จุดแดง + headline "การเชื่อมต่อที่สร้างผลกระทบจริง" + "CONNECTIONS THAT CREATE REAL IMPACT"; ขวา: 4 claim crossfade ตาม scroll ไม่มีกรอบการ์ด; ล่าง: แถบขั้น 4 ข้อ
  - 4 claim (placeholder ทั้งหมด): ผู้โดยสาร / ชุมชน / ESG / พันธมิตร
  - ไอคอน dot-matrix halftone สร้างด้วย JS (grid 15×15, ขนาดจุดตาม coverage ขอบ): คน / บ้าน / ใบไม้ / วงแหวนคล้องกัน — จุดค่อยๆ ขยายจากศูนย์กลางออกตอน claim เข้ามา
  - **แก้ Header (global)**: ตอน scroll บน section สว่าง = พื้นครีมทึบ+ตัว navy, บน section มืด (hero / section 2 / section 5 ที่ mark `data-header="dark"`) = โปร่งใส+ตัวขาว ตามข้อ 7
  - Artifact เดิม อัปเดตแล้ว (Version 5): https://claude.ai/artifact/SA1qEi8p8yaPUeQeXmham7
- **รอบ 6 (เสร็จแล้ว)**: Section 6 ตัวเลขเบื้องหลังเครือข่าย (IR) — ไม่มีต้นแบบ clone เฉพาะ ออกแบบจาก DNA ที่ใช้อยู่แล้ว: พื้นครีม, หัว section = eyebrow "นักลงทุนสัมพันธ์" + headline "ตัวเลขเบื้องหลังเครือข่าย" / "THE NUMBERS BEHIND THE NETWORK" + ป้าย placeholder + ลิงก์ไปหน้า IR
  - ซ้าย (7/12): การ์ด navy แบบ "เกาะ" (ตระกูลเดียวกับการ์ด section 3) — ราคาหุ้น BTS 2.00 ▼−0.99% (ตรงกับ ticker ใน header), กราฟเส้น+area ราคาปิด ปุ่มช่วง 1M/3M/6M/1Y, hover crosshair+tooltip, แถวสถิติ ราคาเปิด/ต่ำสุด–สูงสุด/ปริมาณ/มูลค่าตลาด
  - ขวา (5/12): การ์ดขาว "ข้อมูลทางการเงินโดยสรุป" 2×2 (รายได้รวม/EBITDA/กำไรสุทธิ/เงินปันผล) + list ทางลัด IR 5 รายการ (งบการเงิน, One Report, เอกสารนำเสนอ, ปฏิทินนักลงทุน, ข่าวแจ้งตลาด)
  - **ตัวเลข/กราฟทั้งหมดเป็นข้อมูลตัวอย่าง** (กราฟสร้างจาก random walk แบบ fix seed) — รอเชื่อมข้อมูลจริงจาก SET/ทีม IR
  - Artifact เดิม อัปเดตแล้ว (Version 6): https://claude.ai/artifact/SA1qEi8p8yaPUeQeXmham7
- **รอบ 7 (เสร็จแล้ว)**: Section 7 เรื่องราวจากเครือข่ายของเรา — ไม่มีต้นแบบ clone เฉพาะ ออกแบบจาก DNA เดิม
  - พื้นครีม, eyebrow "ข่าวสารและเรื่องราว" + headline, ปุ่มกรอง pill (ทั้งหมด / MOVE / MIX / MATCH / ความยั่งยืน) ใช้จุดสีแพลตฟอร์มเดียวกับ section 3
  - Grid 3 คอลัมน์ editorial (ไม่มีกรอบการ์ด): เรื่องเด่น 1 เรื่อง (2×2) + 5 เรื่อง — ภาพเป็น placeholder ไล่สีตามแพลตฟอร์ม (MOVE น้ำเงิน / MIX เงิน / MATCH แดง / ความยั่งยืน navy) + ลาย dot-grid + ไอคอน Lucide, แต่ละเรื่องมี หมวด+วันที่ / หัวข้อ
  - ท้าย section: ป้าย "เนื้อหาตัวอย่าง" + ลิงก์ "ดูข่าวสารองค์กรทั้งหมด"
  - **ปิดท้าย "Where will we connect next?"**: แถบมืด (`data-header="dark"`) + motif เส้น-จุด (reuse จาก hero) + headline ใหญ่ + 3 เส้นทางต่อ: ร่วมเป็นพันธมิตร / ร่วมงานกับเรา / ติดต่อ BTS Group — ส่งต่อเข้า footer
  - **ข่าวทั้งหมดเป็นเนื้อหาตัวอย่าง** ลิงก์ยังเป็น `#`
  - Artifact เดิม อัปเดตแล้ว (Version 7): https://claude.ai/artifact/SA1qEi8p8yaPUeQeXmham7
- **รอบ 8 (เสร็จแล้ว)**: Footer (global) ตามข้อ 6 — พื้น near-black `#0C1018` + แถบดำคั่นบน, `data-header="dark"`
  - Tagline "One Group. Many Connections. / Connected Future, Today." (บรรทัดสองสีจาง)
  - Pill toggle MOVE / MIX / MATCH + marquee วิ่งอัตโนมัติ (หยุดเมื่อ hover) — แต่ละแพลตฟอร์มรวมชื่อบริษัท (ตัวหนาขาว) + sub-items + หัวข้อข่าว (สีฟ้า) ไว้ในเส้นเดียว; toggle สลับชุดข้อความ
  - แถวหลัก 3 ช่องคั่นเส้น: Nav 2 คอลัมน์ (8 เมนู IA เดิม) / Hotline + Email + เวลาทำการ + social 4 ปุ่มวงกลม / Head Office (TST Tower) + ปุ่ม "เส้นทางบน Google Maps" + Operating across (สายสุขุมวิท/สายสีลม) + **แผนที่ dotted** (JS สร้างจุดพื้นหลัง เว้นแนวแม่น้ำเจ้าพระยา, เส้นสุขุมวิท/สีลมเป็นจุดน้ำเงิน, สถานีหลัก + Siam interchange + จุด Head Office สีแดง) — เป็นแผนผังโดยประมาณ ไม่ใช่พิกัดจริง
  - Legal grid 6 ช่อง, wordmark ghost "BTS GROUP" เต็มความกว้างลายจุดจาง (SVG pattern), แถบ copyright
  - ใช้ LINE Seed Sans ทั้งหมด (label เล็ก uppercase + letter-spacing กว้าง + สีจาง แทน mono)
  - Artifact เดิม อัปเดตแล้ว (Version 8): https://claude.ai/artifact/SA1qEi8p8yaPUeQeXmham7
- **รอบ 9 (เสร็จแล้ว)**: Loader (global, หน้าแรก) ตามข้อ 8 — เวอร์ชัน rich 3 คอลัมน์บนพื้น navy
  - ซ้าย: wordmark "BTS GROUP / Connected Future" + label "Our network" + รายชื่อ BTS SkyTrain / สายสีชมพู / สายสีเหลือง / VGI / Kerry Express / U City เลื่อนเข้าทีละบรรทัดตาม progress
  - กลาง: แผนที่ dotted BTS Skytrain (**asset เดียวกับ footer** — refactor เป็นฟังก์ชัน `drawBtsMap()` ใช้ร่วมกัน) + วงแหวน sonar 4 วง (30/45/60/75vmax) ping แบบ stagger
  - ขวา: ตัวนับ 0→100% (ตัวบาง 112px) + MOVE / MIX / MATCH เลื่อนเข้าทีละบรรทัด
  - Reveal: iris-wipe 3 ชั้น (วงกลม 0×0 + box-shadow 150vmax ขยายเป็น 300vmax) ไล่ navy → charcoal → ครีม stagger 0.12s — ตัวนับ ~0.85s + iris ~0.9s
  - โชว์ทุกครั้งที่เข้าหน้า (ไม่ gate), ล็อก scroll + ซ่อน header ระหว่างโหลด, prefers-reduced-motion = ข้ามแอนิเมชัน, มี failsafe ถอด loader อัตโนมัติใน 4 วินาทีถ้าสคริปต์หลักพัง
  - Artifact เดิม อัปเดตแล้ว (Version 9): https://claude.ai/artifact/SA1qEi8p8yaPUeQeXmham7
- **รอบ 10 (เสร็จแล้ว)**: Section 2 เวอร์ชัน B + C พร้อมตัวสลับ A/B/C ในหน้าเดียวกัน (ตัดสินใจ 2026-09-25: แทรกในไฟล์หลักแบบ toggle, ทำ Section 2 ก่อน แล้วค่อย Section 3 B/C)
  - **ตัวสลับเวอร์ชัน**: แถบ pill ลอยกลางล่างจอ ("Section 2 · เวอร์ชัน" A Collage / B 2 กลุ่ม / C List) แสดงเฉพาะตอน scroll อยู่ใน section 2 (sticky dock ท้าย wrapper), จำเวอร์ชันที่เลือกไว้ต่อผู้ชม (localStorage), สลับแล้วดึงกลับมาต้น section อัตโนมัติ
  - **เวอร์ชัน B** (ตามข้อ 11): intro "OUR CONNECTIONS" + "ONE GROUP. / MANY CONNECTIONS." บนพื้นครีม → กลุ่ม "การเชื่อมโยงหลัก" (People + Business) พื้นครีม / ตัดแข็งเป็น "การเชื่อมโยงขยาย" (Data + Opportunities) พื้น navy; เลย์เอาต์ 2 คอลัมน์ (หัวกลุ่มซ้าย, แถวรายการขวา) แต่ละแถว = ไอคอน dot-matrix + เลข + ชื่อ node + proof point + จุดกลมตกแต่งขวา + เส้นแบ่ง, ไม่มี motion
  - **เวอร์ชัน C** (ตามข้อ 13): พื้น navy เดียวตลอด, eyebrow "หนึ่งกลุ่มธุรกิจ หลายความเชื่อมโยง" + headline 3 บรรทัด + lede, list 4 แถว (ไอคอน | ชื่อ node EN+TH | คำอธิบาย 2-3 บรรทัด) — ไอคอน **ก่อตัวจากจุดกระจาย** เมื่อแถวเข้า viewport 60% (เล่นซ้ำเมื่อ scroll ออกแล้วกลับมา), prefers-reduced-motion = แสดงรูปทรงเต็มทันที
  - ไอคอน dot-matrix ชุดใหม่ 4 แบบ (คนสองคน / ตึก / กราฟแท่ง / หลอดไฟ) ใช้ฟังก์ชัน halftone ตัวเดียวกับ section 5 (refactor เป็น `drawHalftone()` ใช้ร่วมกัน)
  - ตัวเลข (700,000 คน/วัน, 200+ พันธมิตร) เป็น **placeholder** — มีป้ายกำกับในทั้ง B และ C
  - Artifact เดิม อัปเดตแล้ว (Version 10): https://claude.ai/artifact/SA1qEi8p8yaPUeQeXmham7
- **รอบ 11 (เสร็จแล้ว)**: Section 3 เวอร์ชัน B + C พร้อมตัวสลับ A/B/C (แถบ "Section 3 · เวอร์ชัน": A Pinned card / B Sticky stack / C 2 คอลัมน์ — ใช้ฟังก์ชันตัวสลับตัวเดียวกับ Section 2, จำเวอร์ชันแยกกันต่อ section)
  - **เวอร์ชัน B** (ตามข้อ 10): intro สั้นบนพื้นครีม ("3 แพลตฟอร์ม หนึ่งระบบนิเวศ") → 3 panel เต็มจอแบบ sticky-stack (panel ถัดไปเลื่อนขึ้นคลุมทับ) แต่ละ panel = count 01/03 + ชื่อแพลตฟอร์มตัวใหญ่มาก (~168px) + นิยาม + พารากราฟ + sub-items + ลิงก์ /our-business, ไม่มี eyebrow/ไอคอน/การ์ด
    - โทนสีที่เลือก: MOVE = น้ำเงิน BTS, MIX = เทาเงิน, **MATCH = แดง BTS** (เลือกแดงแทน navy เพื่อให้ 3 panel ต่างกันชัด)
  - **เวอร์ชัน C** (ตามข้อ 15): พื้น navy, headline two-tone "3 แพลตฟอร์ม หนึ่งระบบนิเวศ" / "MOVE · MIX · MATCH" (จาง) + lede → 2 คอลัมน์: ซ้าย = การ์ดภาพ sticky (4:5, มุม 24px) crossfade ตามกลุ่มที่ scroll ผ่าน + caption "MOVE · 01 / 03", ขวา = list 3 กลุ่ม × 3 รายการ (ไอคอน dot-matrix ก่อตัวจากจุดกระจายแบบเดียวกับ S2-C) → ปิดท้าย ghost wordmark "MOVE · MIX · MATCH" ลายจุดจาง
    - รายการที่คัด: MOVE = คมนาคมขนส่ง / โครงสร้างพื้นฐาน / Door-to-door; MIX = O2O / สื่อ / ข้อมูล; MATCH = พันธมิตร / บริการการเงิน / โอกาสใหม่ (ตัด การสัญจร, ดิจิทัล, การกระจายสินค้า, ธุรกิจบริการ, ICT ออก เพื่อให้ได้ 3 ต่อแพลตฟอร์ม)
  - **ภาพ placeholder** (ใช้ร่วม B และ C) วาดเป็น SVG ด้วย JS: MOVE = ขบวนรถไฟฟ้าบนรางยกระดับ + เส้นความเร็ว (โทนน้ำเงิน), MIX = เมืองยามค่ำ + เส้นเชื่อมจุดข้อมูล (โทนเทาเงิน), MATCH = คาน steel-beam ตัด X บนพื้นแดง — มีป้าย "ภาพตัวอย่าง" กำกับ รอเปลี่ยนเป็นภาพจริง
  - ไอคอน dot-matrix เพิ่ม 5 แบบ: รถไฟ / สะพาน-ทางยกระดับ / ถุงช้อปปิ้ง / จอ / เหรียญ
  - Artifact เดิม อัปเดตแล้ว (Version 11): https://claude.ai/artifact/SA1qEi8p8yaPUeQeXmham7
- **รอบ 12 (เสร็จแล้ว)**: แก้ข้อมูลบริษัทในเครือ + เปลี่ยนรูปแบบตัวสลับเวอร์ชัน + ปุ่ม Back to Top (ตัดสินใจ 2026-09-25)
  - **บริษัทในเครือ (ข้อมูลจริงที่ยืนยันแล้ว)**: BTSG ถือหุ้นใน VGI, Super Turtle (STL), ROCTEC Global, Thanulux (TNL), Rabbit Holdings (RBH) — ลบชื่อ placeholder ที่ผิด (`Kerry Express`, `U City`) ออกจากทุกจุดในหน้าเว็บ
    - Footer ticker: จัดกลุ่มใหม่ VGI → MIX, ROCTEC Global (ICT) + Rabbit Holdings (บริการการเงิน) → MATCH, **เพิ่ม toggle ที่ 4 "อื่นๆ"** สำหรับ Super Turtle + Thanulux (ยังไม่ทราบหมวดธุรกิจชัดเจน จึงแยกไว้ต่างหากตามที่ตกลง)
    - Loader ซ้าย ("Our network"): เปลี่ยนจาก 6 เป็น 8 รายการ — BTS SkyTrain, สายสีชมพู, สายสีเหลือง, VGI, Super Turtle, ROCTEC Global, Thanulux, Rabbit Holdings (ปรับจังหวะ stagger ใหม่ให้พอดีกับ 8 รายการ)
    - ลิงก์เว็บบริษัทในเครือ (vgi.co.th, superturtle.co.th, roctecglobal.co.th, tnl.co.th, rabbitholdings.co.th) **ยังไม่ได้ใช้จริง** ในหน้าเว็บ — รอบริบทว่าจะใส่ตรงไหน (footer nav / ส่วนใหม่ "บริษัทในเครือ")
  - **ตัวสลับเวอร์ชัน (redesign)**: เปลี่ยนจากแถบ pill ลอยที่โผล่เฉพาะตอน scroll อยู่ใน section เดิม → เป็น **แผงตั้งค่าเดโม** (การ์ดลอยมุมขวาล่าง, สไตล์ segmented control ตามภาพอ้างอิงที่ผู้ใช้ส่งมา) เปิด/ปิดด้วยปุ่มกลม (ไอคอน sliders) มุมขวาล่าง
    - แผงมีหัวข้อ + ปุ่มปิด (X), 2 กลุ่ม (Section 2 / Section 3) แต่ละกลุ่ม = label + segmented control 3 ตัวเลือก (A/B/C, ปุ่มที่เลือกพื้นน้ำเงิน BTS ตัวหนังสือขาว)
    - ปิดได้ด้วยปุ่ม X, กด Esc, หรือคลิกนอกแผง; เลือกเวอร์ชันแล้ว smooth-scroll ไปยัง section นั้นให้อัตโนมัติ (เผื่อเปิดแผงจากที่อื่นของหน้า ไม่ใช่แค่ตอนอยู่ใน section แล้ว); จำค่าที่เลือกไว้ต่อ section แยกกันใน localStorage เหมือนเดิม
  - **ปุ่ม Back to Top**: ปุ่มกลมลอยมุมขวาล่าง (เหนือปุ่มเปิดแผงเดโม) โผล่หลัง scroll ผ่าน ~80% ของความสูงจอแรก, กด smooth-scroll กลับบนสุด
  - Artifact เดิม อัปเดตแล้ว (Version 12): https://claude.ai/artifact/SA1qEi8p8yaPUeQeXmham7
- **รอบ 13 (เสร็จแล้ว)**: Hero ใหม่ — ฉากเปิดประตูรถไฟฟ้า BTS แบบ scroll-locked (clone DNA จาก 21st.dev "Scroll-Locked Video Hero" by Guglielmo Giannattasio — ดูจาก live preview เพราะโค้ดต้นฉบับถูกล็อก)
  - **DNA ต้นแบบ**: ภาพประตูรถไฟปิดเต็มจอ + headline กลางจอ + "SCROLL ↓" → section ปักหน้าจอไว้ขณะเลื่อน: headline เบลอหาย, ประตู 2 บานเลื่อนแยกออกตาม scroll progress, เส้นแสง lens-flare พาดกลาง, แถบ progress บางที่ขอบล่าง → หลังประตูคือวิดีโอเมืองกลางคืนที่เล่นวนอยู่แล้ว (ไม่ได้ scrub ตาม scroll) เผยจนเต็มจอแล้วค่อยปลด scroll
  - **การตัดสินใจ (2026-09-25)**: (1) ประตูเป็นภาพประกอบ SVG ชั่วคราว (2) วิดีโอเป็น canvas animation ชั่วคราวแบบเดียวกับ section 5 (3) ความยาวโมเมนต์สั้นกระชับ (4) มือถือไม่ scroll-jack
  - **Closed state**: ประตู BTS 2 บาน (น้ำเงิน BTS, หน้าต่างกระจกมีหยดน้ำฝน/รอยไหล, ขอบยาง, ป้าย "ระวังประตูหนีบ · MIND THE DOOR", สติกเกอร์ BTS, ช่องมือจับ, แถบแดง livery, ยางกลางรอยต่อ) — กระจกโปร่งแสง เห็นเมืองขยับอยู่ด้านหลังผ่านหน้าต่าง + ชื่อ "THE CONNECTED FUTURE" / "ก้าวผ่านประตู สู่เมืองที่ทุกอย่างเชื่อมถึงกัน" + ปุ่ม pill "เลื่อนเพื่อเปิดประตู ↓"
  - **กลไก**: hero สูง 190vh (เลื่อน ~90vh เพื่อเปิด), ชั้นใน sticky 100vh — ชื่อเบลอ+จางใน 20% แรก, ประตูเปิด (ease-in-out) ช่วง 8–88%, flare เข้มสุดกลางทาง, "วิดีโอ" ซูมจาก 1.14 → 1.0, เนื้อหา hero (h1 + CTA) เลื่อนขึ้นมาช่วง 78–100%
  - **"วิดีโอ" placeholder = เล่าเรื่อง 3 จังหวะ วนทุก ~12.6 วิ** ซิงก์กับบรรทัด "Moving people. / Connecting businesses. / Creating possibilities." (คำที่ตรงจังหวะสว่างขึ้น):
    1. Moving people — ขบวนรถไฟฟ้า BTS วิ่งผ่านทางยกระดับ + ไฟรถบนถนนเป็นเส้นแสง (วิ่งตลอดทั้งลูป)
    2. Connecting businesses — ดาดฟ้าตึกเชื่อมกันด้วยเส้น-จุดสีเงิน (motif เดียวกับทั้งเว็บ) ค่อยๆ ลากเส้นทีละเส้น
    3. Creating possibilities — ฟ้าเริ่มสาง แสงอุ่นที่ขอบฟ้า + วงแหวนขยายจากทุก node
  - CTA "สำรวจ BTS Group" เปลี่ยนลิงก์ไป Section 2 (เดิมชี้ #hero ซึ่งจะพากลับไปประตูปิด)
  - **มือถือ (≤720px) และ prefers-reduced-motion**: hero สูง 100vh ไม่ปักจอ ไม่มีประตู — เห็นเนื้อหาบน "วิดีโอ" ทันที (reduced motion = เฟรมนิ่ง + ทุกวลีสว่าง)
  - ป้าย placeholder ในหน้าเว็บ (Section 3B / 5 / hero) ขยับไป right:92px เพื่อไม่ทับปุ่ม Back to Top
  - Artifact เดิม อัปเดตแล้ว (Version 13): https://claude.ai/artifact/SA1qEi8p8yaPUeQeXmham7
  - **ถัดไป**: เลือกเวอร์ชันจริงของ Section 2 และ 3 → ถอดเวอร์ชันที่ไม่ใช้ + แผงเดโมออก → Polish / responsive pass; เปลี่ยนประตูเป็นภาพถ่ายจริง + canvas เป็นฟุตเทจจริงเมื่อได้ไฟล์
- **รอบ 14 (เสร็จแล้ว)**: Section 2 เวอร์ชัน D — photo/colour mosaic (clone DNA จาก cpgroupglobal.com/th/home banner section — inspect DOM/animation จริงจากเว็บ)
  - **DNA ต้นแบบ**: กริด 8 คอลัมน์ × 4 แถว เต็มกรอบมนไม่มีช่องว่าง ผสมภาพถ่าย (ขนาด 1×1 ถึง 2×2) กับ "การ์ดสี" (คำโปรย 1 บรรทัด) — การ์ดสีมีสองสถานะ: ข้อความ ↔ ไอคอน สลับกันเป็นสองกลุ่มสลับเฟส (checkerboard) ทุก 3 วินาที แบบ crossfade 1s; ก่อนกริดโชว์มี motto เต็มจอทับอยู่ก่อนแล้วค่อยหด/จางออก เผยกริดซูมเข้า stagger ตามระยะจากมุมซ้ายบน
  - **Map เข้า BTS**: 21 ช่อง (13 รูปภาพ placeholder + 8 การ์ดสี) วางตำแหน่ง/ขนาดตรงกับต้นแบบเป๊ะ (รวมถึงตำแหน่งการ์ดสีที่ตรงกับ index เดิมของ CP โดยบังเอิญจากการ map shape) — รูปภาพใช้ icon-tile ไล่สีน้ำเงิน/แดง/เงิน/navy (จำกัดอยู่ในโทนที่กำหนดไว้แล้วในเอกสารข้อ 1 ไม่ใช้สีสันหลากหลายแบบต้นแบบ CP เพราะ brand DNA ของ BTS ใช้สีจำกัด) แต่ละช่องมี caption มุมซ้ายล่าง (PEOPLE/BUSINESS/DATA/MOVE/MIX/MATCH ฯลฯ), การ์ดสีมีคำโปรย 8 อัน: Moving People / Connecting Business / Data-Driven City / Endless Opportunity / One Ecosystem / Sustainable Future / Trusted Network / Driving Growth
  - **มือถือ**: กริดเล็กเกินอ่านไม่ออกถ้าบีบ 8 คอลัมน์ในจอแคบ จึงคง min-width ไว้ (920px) แล้วให้ scroll แนวนอนแทน — เป็นข้อยกเว้นเดียวที่ใส่ mobile fallback ให้ (ปกติ section อื่นยังไม่ทำ responsive ตามแผน)
  - Artifact เดิม อัปเดตแล้ว (Version 14): https://claude.ai/artifact/SA1qEi8p8yaPUeQeXmham7
  - **ถัดไป**: เลือกเวอร์ชันจริงของ Section 2 (ตอนนี้มี A/B/C/D) และ Section 3 → ถอดเวอร์ชันที่ไม่ใช้ + แผงเดโมออก → Polish / responsive pass
- **รอบ 15 (เสร็จแล้ว)**: เพิ่มความ "lifestyle" ให้ Section 2 และ 3 ทุกเวอร์ชัน (ตัดสินใจ 2026-09-25: ปรับพร้อมกันทั้งหมด — สื่อ "Human" ใน Image DNA ที่ระบุไว้ตั้งแต่ข้อ 1 แต่ยังไม่เคยถูกใช้จริงใน section เหล่านี้ เอียงไปทาง Infrastructure/abstract diagram มาตลอด)
  - **เทคนิคใหม่**: ฟังก์ชัน `crowdFigure`/`crowdRow`/`lifeSceneSVG` วาดกลุ่มคนซิลูเอตแบบ flat (หัว+ลำตัว+ขา ด้วย path/circle ล้วน) หลากท่าทาง (ยืน/เดิน/ถือมือถือ/ถือกระเป๋า/ใช้ไม้เท้า/เข็นรถเข็นเด็ก/เด็ก/สะพายเป้) สื่อความหลากหลายผ่าน **ท่าทาง/ความสูง ไม่ใช่สี** (คงโทนน้ำเงิน/เงิน/ขาวจำกัดตามแบรนด์) — มี 3 ฉากพื้นหลัง: `platform` (ชานชาลารอรถไฟฟ้า), `street` (ทางเท้า/สี่แยกในเมือง), `market` (พื้นที่ค้าปลีก/ชุมชน) แต่ละฉากมีคนสองแถว (หลัง=เล็ก/จาง, หน้า=ใหญ่/ชัด) ขยับสวนทางกันช้าๆ (`ls-drift`/`ls-drift-r`) ให้ความรู้สึกคนกำลังเดินผ่าน
  - **Section 2**: A — การ์ด People/Business มีฉากคนลอยด้านบน (icon-tile กลายเป็น badge ทับขอบล่างฉาก) ส่วน Data/Opportunities คงไอคอนเดิม (เป็นแนวคิดนามธรรมที่เหมาะสมอยู่แล้ว); B — แถว People/Business (กลุ่มอ่อน) เปลี่ยนไอคอน dot-matrix เป็น thumbnail ฉากคนสี่เหลี่ยม 96px; C — เพิ่มฉากคนแบบพาโนรามาคั่นระหว่าง intro กับ list; D (mosaic) — เปลี่ยน 3 ใน 13 ช่องภาพ (People/Business/Community) จาก icon-tile เป็นฉากคนเต็มช่อง ที่เหลือ (Data/Opportunities/MOVE/MIX/MATCH/Network/Growth/Future City/Finance/ICT) คงไอคอนเดิมเพราะเป็นแนวคิดนามธรรม
  - **Section 3**: A — เพิ่มไอคอนคนเดิน/คนคู่ในวง node "รถไฟฟ้า BTS" และ "ฟีดเดอร์" ของฉาก MOVE (ขยายวงจาก r=6 เป็น r=13) ส่วน MIX/MATCH คงเป็นแนวคิดนามธรรมตามเดิม (ยืนยันจากแผนเดิมว่า A เป็นแนว infographic ตั้งใจให้ต่างจาก B/C); B และ C (ใช้ `pfSceneSVG` ร่วมกัน) — ฉาก MOVE เพิ่มคนยืนรอที่ชานชาลา, ฉาก MIX เพิ่มคนเดินถนนระดับพื้น, ฉาก MATCH คงกราฟิกคานเหล็กเดิม (เป็นสัญลักษณ์เชิงแนวคิด)
  - **บั๊กที่เจอระหว่างทำและแก้แล้ว**: (1) ส่ง `x` เป็น string (`.toFixed(1)`) เข้า `crowdFigure` แล้วใช้ `x + hw` ในฟังก์ชัน — บวกเลขกับ string กลายเป็นต่อ string แทนบวกจริง ทำให้พิกัด SVG เพี้ยน (เช่น `"1526.8" + 8.3` → `"1526.88.3"`) เกิด parse error หลักพันจุดทั่วหน้า แก้ด้วยการบังคับแปลงเป็นตัวเลขที่ต้นฟังก์ชัน (2) `.life-fill{position:relative}` มาทีหลัง `.dt-p{position:absolute}` ใน stylesheet ทำให้ช่อง mosaic ที่เปลี่ยนเป็นฉากคนเสีย layout (คลาสหลังชนะ) แก้ด้วยการย้าย `position` ไปกำหนดต่อจุดใช้งานแทนที่ฐาน `.life-fill` (3) เดิมมี `document.querySelectorAll('[data-scene]')` (ไม่ scope class) ซึ่งจะดึงฉากคนใหม่ไปวาดทับด้วยกราฟิก MOVE/MIX/MATCH ผิดฉาก — แก้ด้วยการ scope เป็น `.pf-photo[data-scene]`
  - Artifact เดิม อัปเดตแล้ว (Version 15): https://claude.ai/artifact/SA1qEi8p8yaPUeQeXmham7
- **รอบ 16 (เสร็จแล้ว)**: Section 4 เวอร์ชัน B — dark stats grid + count-up + ภาพ mask ทรงโค้งคู่ (clone DNA จาก motionsites.ai "Arceage Stats" — ดูจาก animated preview เพราะเป็น prompt marketplace ไม่มีโค้ดให้ inspect ตรงๆ, ต้องรอแท็บ focus ถึงจะเห็นแอนิเมชันเล่นจริง)
  - **DNA ต้นแบบ**: พื้นดำสนิท 2 คอลัมน์ — ซ้าย headline serif หรู + กริดตัวเลข 2×3 (5 ค่า) นับขึ้น (count-up) จาก 0 ตอน fade-in, ขวา = ภาพ/วิดีโอถูก mask เป็นรูปทรงโลโก้แบรนด์ตัวเอง วนลูป fade ดำ→เผย→ดำ
  - **การตัดสินใจ (2026-09-25)**: ใช้ canvas placeholder (ไม่ใช่ภาพจริง) แต่ให้สื่อ "ขนาด/ความน่าเชื่อถือ" แทนแค่ภาพเมืองทั่วไป → ออกแบบเป็นภาพมุมสูงเห็นแถวหลังคาตึกหนาแน่นนับพันหลัง (ให้ความรู้สึกสเกลใหญ่) + เส้นทางรถไฟฟ้า 2 เส้นตัดกันพร้อมสถานีเรืองแสงและจุดตัดกระพริบสีแดง (สื่อโครงข่ายซับซ้อน น่าเชื่อถือ) แทนที่จะเป็นแค่รถไฟฟ้าวิ่งเฉยๆ แบบ Hero/Section 5
  - **เนื้อหา**: headline "เครือข่ายที่ใหญ่พอ ให้ทั้งเมืองไว้วางใจ" + ตัวเลข 5 ค่า (26+ ปี, 200+ พันธมิตร, 98% ICT, 40 บริษัท, 1.2 ล้านราย บริการการเงิน) นับขึ้นด้วย easing (cubic ease-out) ทีละตัวสลับจังหวะ 140ms
  - **ภาพ mask**: ใช้ SVG shape โค้งคู่ (double-arch) แทนโลโก้ BTS จริง (ยังไม่มีไฟล์ vector โลโก้ที่ตัดเป็น mask ได้) — ให้ความรู้สึก "ประตู/ทางเชื่อม" ใกล้เคียงธีมเว็บ ไม่ใช่โลโก้จริง 100%
  - **แอนิเมชัน**: ภาพซูมเข้า-ออกช้าๆ ต่อเนื่อง (breathing zoom), จุดตัดสถานีกระพริบ, ขบวนรถไฟฟ้าเรืองแสงวิ่งตามเส้นทางวนลูป, วงแหวนสีแดงขยายจากจุดตัดเป็นจังหวะ — ทั้งหมดใช้ IntersectionObserver trigger เข้า/ออกจอ (หยุด loop เมื่อเลื่อนผ่านไปเพื่อประหยัด CPU, เล่นซ้ำเมื่อกลับเข้ามา เหมือน pattern อื่นๆ ในเว็บ)
  - **มือถือ**: ใส่ breakpoint ยุบเป็น 1 คอลัมน์ + กริดตัวเลข 2 คอลัมน์คงเดิม + ภาพ mask ย่อขนาดกึ่งกลาง (พบว่าพังหนักบนจอแคบก่อนแก้ — ล้นขอบจอเพราะกริด 2 คอลัมน์ไม่ยุบ)
  - เพิ่มกลุ่ม "Section 4" ในแผงเดโมแล้ว (A · Cascade / B · Stats grid)
  - Artifact เดิม อัปเดตแล้ว (Version 16): https://claude.ai/artifact/SA1qEi8p8yaPUeQeXmham7

## 19. Motion & Interaction Audit (2026-09-25)

**เหตุผล**: ผู้ใช้แจ้งว่าเจอ section 2 และ 3 บางเวอร์ชัน "ไม่ทำงาน" ระหว่างทดสอบเอง ไล่ตรวจทุกกลไก motion/interaction ในหน้าเว็บอย่างเป็นระบบ

**ข้อจำกัดของการตรวจครั้งนี้**: หน้าต่างพรีวิวของเครื่องมือระหว่าง audit อยู่ในสถานะไม่ focus (`document.hidden = true`) ซึ่งเบราว์เซอร์จะ**หยุดยิง `requestAnimationFrame` และ `IntersectionObserver` ทั้งหมดโดยสมบูรณ์** (ยืนยันแล้วด้วยการสร้าง IntersectionObserver ทดสอบตรงๆ บน element ที่อยู่ในจอจริง แต่ callback ไม่ยิงเลย) — กลไก scroll-driven ส่วนใหญ่ในเว็บนี้ (parallax, pinned crossfade, icon-forming, mosaic reveal) พึ่งสองตัวนี้ จึงตรวจสดผ่าน real scroll ไม่ได้ในรอบนี้ ใช้วิธีเลี่ยง 3 ทาง:
1. ทดสอบ interaction ที่เป็น click handler ตรงๆ (ไม่ผ่าน rAF/IO) ได้ปกติ
2. บางฟังก์ชัน (`onHeroScroll`, `onPinScroll`) ผูกกับ `resize` event ควบคู่กับ `scroll` อยู่แล้ว (ไว้รองรับ viewport เปลี่ยนขนาด) — ใช้ `dispatchEvent(new Event('resize'))` เรียกโดยตรงได้ ไม่ผ่าน rAF
3. `position:sticky` เป็นกลไก CSS layout ล้วนๆ ไม่ต้องพึ่ง JS/rAF — ตรวจได้ตรงๆ ผ่าน `getBoundingClientRect()` ที่ scrollY ต่างๆ

**ผลตรวจ — ยืนยันว่าทำงานถูกต้อง:**
- Header: เปิด/ปิดเมนู overlay, ขยาย submenu ✅ (click handler)
- **Section 3 ทั้ง 3 เวอร์ชัน — กลไก `position:sticky` ทำงานถูกต้องหมด** (ตรวจผ่าน getBoundingClientRect ที่จุด start/mid/end ของแต่ละเวอร์ชัน): A (pinned card ค้างที่ top:0 ตลอด pin range), B (sticky-stack — panel ถัดไปเลื่อนขึ้นทับ panel ก่อนหน้าได้ถูกต้อง เห็น top ของแต่ละ panel เปลี่ยนตามลำดับ), C (การ์ดภาพซ้าย sticky นิ่งขณะ list ขวาเลื่อนผ่าน)
- Section 3-A: pinned crossfade + rail active state (ตรวจผ่าน resize-bypass ที่ scroll 3 จุด — active scene และ rail ตรงกันทุกจุด) ✅
- Hero: กลไกประตูเปิด (ตรวจผ่าน resize-bypass ที่ปิด/กลางทาง/เปิดสุด — gate opacity, door transform, content opacity เปลี่ยนถูกต้องตามลำดับ) ✅
- Section 6: ปุ่มช่วงเวลากราฟหุ้น (1M/3M/6M/1Y) เปลี่ยนกราฟจริง ✅
- Section 7: ปุ่มกรองเรื่องราวตาม MOVE/MIX/MATCH ✅
- Footer: toggle MOVE/MIX/MATCH เปลี่ยน ticker จริง ✅
- แผงเดโม + ตัวสลับเวอร์ชัน: เปิด/ปิดแผง, สลับได้ครบทุกปุ่ม — Section 2 A/B/C/D และ Section 3 A/B/C (แสดง/ซ่อน section ถูกต้องทุกตัว) ✅
- Section 2-A บนจอแคบ (375px จำลอง): การ์ดไม่ล้นขอบจอ ✅ (แต่ยังไม่ได้ปรับ layout ให้เหมาะกับจอเล็กจริงจัง ตามที่ตกลงว่า responsive เป็น pass แยก)

**สิ่งที่พบระหว่างตรวจ (เป็นพฤติกรรมที่ตั้งใจ แต่ทำให้เข้าใจผิดว่า "พัง" ได้ง่าย):**
- ระบบจำเวอร์ชันที่เลือกไว้ผ่าน `localStorage` แยกต่อ Section 2/3 — ถ้าเคยสลับไปเวอร์ชันอื่นไว้ (เช่นระหว่างทดสอบ) แล้วโหลดหน้าใหม่ จะข้ามเวอร์ชัน A ไปโชว์เวอร์ชันที่จำไว้ทันที ไม่ใช่บั๊ก แต่ถ้าไม่รู้กลไกนี้จะดูเหมือนหน้าเว็บ "เพี้ยน" หรือ section หายไป — **ควรพิจารณา**: เพิ่มปุ่ม/ทางรีเซ็ตกลับเวอร์ชัน A ให้ชัดเจนขึ้นในแผงเดโม

**ยังตรวจสดไม่ได้ในรอบนี้ (ต้องมีหน้าต่างพรีวิว focus จริงถึงจะ rAF/IO ทำงาน):**
- Header hide-on-scroll-down / scrolled-state (โค้ดไม่เปลี่ยนตั้งแต่รอบแรกๆ ของ build)
- ปุ่ม Back to Top โผล่ตาม scroll position
- Section 2-A parallax cards, Section 2-C icon ก่อตัวตอน scroll เข้าจอ, Section 2-D mosaic reveal + flip ทุก 3 วิ
- Section 3-C sticky visual สลับภาพตามกลุ่มที่ scroll ผ่าน
- Section 4 proof opacity ตาม scroll focus, Section 5 pinned claims + parallax
- Loader (ตอน pane ไม่ focus จะไปเข้า failsafe 4 วินาทีแทน flow ปกติ — พฤติกรรมนี้เกิดเฉพาะตอน tab ไม่ active ซึ่งผู้ใช้จริงจะไม่เจอ เพราะ tab ที่กำลังโหลดหน้าเว็บจะ active อยู่เสมอ)

**ขั้นต่อไป**: รอผู้ใช้ระบุให้ชัดว่าเจอปัญหาที่ section/เวอร์ชันไหนกับขนาดจอ/เบราว์เซอร์ใด เพื่อ reproduce และแก้ตรงจุด — หรือถ้าเป็นไปได้ ให้เปิดหน้าต่างพรีวิวไว้ (focus) ระหว่างตรวจรอบหน้าเพื่อยืนยัน scroll-driven effect ที่เหลือได้ครบ

## 20. Section 4.5 — เครือข่ายที่เชื่อมทั้งเมือง (Network Map) — clone DNA จาก 21st.dev "Map"

**คำขอผู้ใช้ (2026-09-25)**: อยากได้ 1 section ที่บอกภาพรวมโครงข่ายการเดินทาง/เส้นทางรถไฟฟ้า BTS สื่อความครอบคลุม เชื่อมต่อ วงกว้าง และ impact ต่อเมือง โดย clone DNA จาก https://21st.dev/@shailendrakumar19999/components/map

**DNA ต้นแบบ**: แพทเทิร์น "World Map" (Aceternity/Magic UI style) — แผนที่โลกแบบจุด (dotted-map) พื้นเข้ม + เส้นโค้ง (arc) ที่ animate ลากจากจุดหนึ่งไปอีกจุด (framer-motion) พร้อม pulse วงแหวนที่ปลายจุดเชื่อมต่อ สื่อธีม "เชื่อมทีม/ลูกค้าทั่วโลก"

**การตัดสินใจสำหรับ BTS (ยืนยันแล้ว)**:
1. **ตำแหน่ง**: section ใหม่แทรกระหว่าง Section 4 (ตัวเลขเบื้องหลังเครือข่าย) กับ Section 5 (การเชื่อมต่อที่สร้างผลกระทบ) — ต่อเนื่อง narrative จากพิสูจน์ด้วยตัวเลขธุรกิจ → พิสูจน์ด้วยภาพโครงข่ายจริง → ผลกระทบต่อคน/เมือง
2. **แผนที่**: ขยาย asset `drawBtsMap()` เดิม (ใช้ร่วมกับ footer/loader อยู่แล้ว) เป็นเวอร์ชันใหญ่เฉพาะของ section นี้ — คง coordinate/motif เดิมทั้งหมด (จุดพื้นหลัง, เส้นทางสุขุมวิท/สีลมแบบจุดสี, สถานีหลัก, hub สยาม) เพื่อให้เป็น "asset เดียวกันทั้งเว็บ" ตามที่ตั้งใจไว้ตั้งแต่ข้อ 1
3. **เพิ่มจากต้นแบบ 21st.dev**: schematic spur เส้นประไปยัง "เชื่อมต่อสายสีชมพู" (เหนือ Khu Khot) และ "เชื่อมต่อสายสีเหลือง" (ใต้ Kheha), ป้ายจุดเชื่อมต่อ MRT ที่หมอชิตและอโศก (จุดใหม่ interpolate บนเส้นสุขุมวิท), หมายเหตุเชื่อมเรือด่วนเจ้าพระยาที่สะพานตากสิน (สถานีเดิม), pulse วงแหวนสีแดงที่สยาม (จุดเชื่อมต่อหลัก BTS) — ทั้งหมดเป็นแผนผังโดยประมาณ ไม่ใช่พิกัดจริง (ป้ายกำกับไว้)
4. **Motion**: route dots (เฉพาะเส้นทาง ไม่รวมจุดพื้นหลัง) fade-in แบบ stagger ตอน scroll เข้าจอ (คล้าย "เส้นค่อยๆ ลาก" ของต้นแบบ) + "รถไฟ" แบบ comet-trail 2 ขบวน วิ่งวนตามเส้นทางสุขุมวิท/สีลมต่อเนื่อง (rAF, cumulative-length interpolation) + ring pulse ที่ Siam/Mo Chit/Asok — ใช้ IntersectionObserver enter/leave pattern เดียวกับ proofB (เล่น/หยุดตาม visibility, prefers-reduced-motion = แสดงนิ่ง)
5. **สถิติร่วม section**: stat strip 4 ค่าใต้แผนที่ (60+ สถานี, 70+ กม., 13 เขต, 700,000+ คน/วัน) — คนละชุดกับ Section 4 ที่เน้นสถิติธุรกิจ, เน้นสถิติ "ขนาดโครงข่ายการเดินทาง" โดยเฉพาะ — **ตัวเลขตัวอย่างทั้งหมด** (ป้ายกำกับไว้)
6. **โทนสี**: พื้น `var(--dark)` ต่อเนื่องธีมเข้มของ hero/section 2/5, การ์ดแผนที่ไล่เฉด navy-black, เส้นทางสีน้ำเงิน/ฟ้าเดิม (`#3FA3EC`/`#8FD0FF`), จุดเชื่อมต่อระบบอื่นสีเงิน (`#7C8CA6`), hub หลักสีแดง BTS

**หมายเหตุ**: มี HTML `<rect>` width ติดลบ (console error) อยู่ก่อนแล้วในโค้ด hero door SVG (`winW - 22` ตอน resize จอแคบมาก) — ไม่เกี่ยวกับ section ใหม่นี้ ยังไม่ได้แก้ (นอก scope รอบนี้)

- Artifact เดิม อัปเดตแล้ว (Version 17): https://claude.ai/artifact/SA1qEi8p8yaPUeQeXmham7

## 21. Closing CTA "Where will we connect next?" — clone DNA จาก 21st.dev "cta69" + ลดทอน Footer (2026-09-25)

**DNA ต้นแบบ**: closing CTA แบบ full-bleed — พื้นหลังเป็น marquee ข้อความใหญ่มากโทนเดียววิ่งวนต่อเนื่อง, เนื้อหากลางจอ: badge → headline → note → "seal button" (ปุ่มวงกลมแบบตราประทับ มีข้อความวิ่งรอบวง)

**สิ่งที่ทำ**:
1. **ไม่สร้าง section ใหม่** — reskin section "Where will we connect next?" เดิม (ทำหน้าที่ Future/Closing CTA อยู่แล้ว) ถอด motif เส้น-จุด (hero-net) เดิมออก
2. **Marquee พื้นหลัง**: 2 แถววิ่งสวนทางกัน — แถวบน "CONNECT ·" ตัวโปร่งเส้นขอบเงินจาง, แถวล่าง "MOVE · MIX · MATCH ·" ตัวทึบขาวจางมาก, ตัวใหญ่ ~15vw, ขอบซ้าย-ขวาจางด้วย mask
3. **เนื้อหากลางจอ**: badge pill "Connected Future" (จุดแดง) → headline "Where will we connect next?" + บรรทัดไทย "เราจะเชื่อมต่ออะไรต่อไป?" → คำโปรยเดิม → **seal button** 176px: วงข้อความ "สำรวจการเชื่อมต่อ · EXPLORE CONNECTIONS ·" หมุนช้าๆ (22 วิ/รอบ) รอบแกนวงกลมน้ำเงิน BTS + ลูกศร (hover = แกนขยาย + ลูกศรเอียงขึ้น 45°) → ลิงก์ไปยัง footer (ช่องทางติดต่อ/เมนู) ในรอบนี้
4. **3 ลิงก์เดิม** (ร่วมเป็นพันธมิตร / ร่วมงานกับเรา / ติดต่อ BTS Group) ลดเป็น pill เล็กเรียงใต้ seal button (ลิงก์ยังเป็น `#`)
5. **Footer ลดทอน**: ถอดบล็อก pill toggle MOVE/MIX/MATCH + ticker marquee (รวม JS `ftLines`/`renderTicker`) และ ghost wordmark "BTS GROUP" ท้ายสุดออกทั้งหมด — footer เหลือ tagline → nav/contact/head office+map → legal → copyright (สูงราว 830px บนจอ 1440px, ลดลง ~280px)
6. prefers-reduced-motion = marquee และวงข้อความหยุดนิ่ง

- Artifact เดิม อัปเดตแล้ว (Version 18): https://claude.ai/artifact/SA1qEi8p8yaPUeQeXmham7

## 22. Section 5 · เวอร์ชัน B — Tabs (clone DNA จาก 21st.dev shadcnblocks "feature108") (2026-09-25)

**DNA ต้นแบบ**: "3 features inside a tabs component" (Radix Tabs + Lucide) — แถบ tab เป็นการ์ดคลิกได้ (ไอคอน + หัวข้อ + คำอธิบายสั้น) และ content stage ที่สลับตาม tab: ภาพ + headline + พารากราฟ + checklist, ขับเคลื่อนด้วยการคลิก ไม่ใช่ scroll

**การตัดสินใจ**:
1. เพิ่มเป็น **ตัวเลือกคู่ขนาน** — Section 5 ได้ตัวสลับเวอร์ชันครั้งแรก (A · Pinned photo = ของเดิม ไม่แตะ / B · Tabs = ใหม่) ในแผงเดโม, ห่อด้วย `s5-wrap`, localStorage key `bts-s5-variant`
2. ใช้ **4 หมวดเดิม** (ผู้โดยสาร / ชุมชน / ESG / พันธมิตร) แทน 3 ของต้นแบบ — headline/พารากราฟเดิมจากเวอร์ชัน A, ไอคอน dot-matrix ชุดเดิม (คน/บ้าน/ใบไม้/วงแหวน) บน tab
3. **พื้นเข้ม** `var(--dark)` ต่อเนื่องแบบเวอร์ชัน A — section สูงปกติ ไม่ปักจอ/ไม่ parallax (ต่างจาก A ที่สูง 440vh)
4. **Checklist ใหม่ 3 ข้อต่อหมวด** (placeholder ไม่ใส่ตัวเลข รอทีม ESG): เช่น ESG = ขับเคลื่อนด้วยไฟฟ้า / ระบบเบรกนำพลังงานกลับมาใช้ / พลังงานแสงอาทิตย์บนศูนย์ซ่อมบำรุง
5. **ภาพ placeholder** reuse ฉากเดิม: ผู้โดยสาร = ชานชาลา (platform), ชุมชน = ทางเท้า (street), ESG = ขบวนรถไฟฟ้าโทนน้ำเงิน (pf-photo move), พันธมิตร = พื้นที่ค้าปลีก (market)
6. **Interaction**: tab ใช้ role tablist/tab/tabpanel, คลิกหรือลูกศร ←→ / Home / End (roving tabindex), panel crossfade ในช่อง grid เดียวกัน (ความสูงไม่กระโดด), ≤960px tab เรียง 2×2 และ panel เป็น 1 คอลัมน์

- Artifact เดิม อัปเดตแล้ว (Version 19): https://claude.ai/artifact/SA1qEi8p8yaPUeQeXmham7

## 23. ปรับแก้ย่อย + Section 2-A scroll convergence (2026-09-25)

- **Hero**: ถอดป้าย "ระวังประตูหนีบ · MIND THE DOOR" ออกจากประตูทั้งสองบาน (Version 20)
- **ตัวสลับเวอร์ชัน**: เลิกจำค่าใน localStorage — ทุก section (2/3/4/5) เปิดที่เวอร์ชัน A เสมอ, สลับได้เฉพาะระหว่างเปิดหน้าอยู่ (Version 21)
- **Section 4-A**: "บริการการเงิน" (รายการที่ 4) เยื้องซ้าย 39px เท่ากับ "ICT" แทน 104px (Version 22)
- **Section 2-A — การ์ดรวมเข้ากลางแล้วนำสายตาลงสู่ Section 3** (Version 23):
  - เวทีการ์ด (สูง 960px) ปักจอ (sticky) เมื่อขอบล่างชนขอบล่างจอ ค้างไว้ระยะ scroll 110vh แล้วค่อยปล่อย — section ยาวขึ้นเท่านี้ (ถอด `min-height:132vh` ออก, `overflow:hidden` → `overflow:clip` เพื่อไม่ให้ sticky พัง)
  - ขาเข้า: parallax แนวตั้งแบบเดิม (ความเร็วต่อใบเท่าเดิม) และจบที่ตำแหน่ง CSS พอดีตอนเริ่มปักจอ
  - ระหว่างปักจอ: การ์ดทั้ง 4 เคลื่อนเข้าหาจุดกลางใต้ hub (ทั้งแกน X และ Y) ใน 80% แรก + ย่อเหลือ 55% + จางจนหาย (opacity 0) ช่วง 45–85%; เส้นเชื่อมทั้ง 4 วิ่งตามการ์ดและสว่างขึ้น; hub ขยาย + วงแหวนฟ้ารอบ hub; **เส้นฟ้าพุ่งจาก hub ลงถึงขอบล่างจอ** (ช่วง 30–100%) มีจุดขาวนำหน้า เป็นตัวชี้ทางไป Section 3
  - มือถือ (≤720px) และ prefers-reduced-motion: ไม่ปักจอ ไม่มี convergence, การ์ดอยู่ตำแหน่งเดิม

- Artifact เดิม อัปเดตแล้ว (Version 23): https://claude.ai/artifact/SA1qEi8p8yaPUeQeXmham7

## 24. Section 2→3 transition — เร็วขึ้น + เชื่อมนุ่มนวลขึ้น (2026-09-25)

1. **ลดระยะปักจอ**: `.eco-track` จาก `960px + 110vh` เหลือ `960px + 55vh` — สัดส่วนจังหวะเดิมทั้งหมด (การ์ดเริ่มยุบที่ c=0, จางหมดที่ c=0.85, เส้นฟ้าเริ่มไหลที่ c=0.3 ถึงพื้นที่ c=1) ยังคงเดิม แค่ระยะ scroll จริงสั้นลงครึ่งหนึ่ง — Section 3 โผล่มาเร็วขึ้นชัดเจน
2. **โซนเบลนด์สี**: เพิ่ม `.eco-inner::after` เป็น gradient จากโปร่งใสไปสีครีม สูง 42% ของกล่อง, opacity ผูกกับตัวแปร CSS `--seam` ที่ตั้งค่าจาก JS ให้ตรงกับความคืบหน้าของเส้นฟ้าที่หย่อนลง (`drop`) — ครีม "ไล่ขึ้น" มาบังส่วนล่างจอพอดีตอนเส้นฟ้าถึงพื้น แล้วพอปล่อยปักจอ ตัด hard-cut เข้าสีครีมจริงของ Section 3 จะรู้สึกต่อเนื่องแทนที่จะกระโดด
3. **Section 3 intro โผล่ขึ้นมาหา**: `.pf-intro` (ใช้ร่วมกันทั้งเวอร์ชัน A และ B) เพิ่ม fade+translateY เข้า (40px, .6s) ตอนเลื่อนเข้า viewport ผ่าน IntersectionObserver (threshold .2) — headline ไม่โผล่นิ่งๆ อีกต่อไป แต่ "เคลื่อนขึ้นมา" ตามที่ขอ, prefers-reduced-motion แสดงทึบทันที
4. **ตรวจแล้ว** (bypass rAF ผ่าน resize event เพราะพรีวิวพักอยู่เบื้องหลังทำให้ rAF/IntersectionObserver ไม่ยิง — ปัญหาเดิมที่เจอในรอบ audit ข้อ 19): ระยะปักจอใหม่ = 495px ที่ vh 900 (≈55vh) ตรงตามตั้งใจ, `--seam` และ `dropY2` ไล่ 0→1 / 480→960 สอดคล้องกันพอดีตอน c เข้าใกล้ 1 — ส่วน IntersectionObserver ของ `.pf-intro` ยืนยันด้วยโค้ด (pattern เดียวกับ `proofB`/`ecoD` ที่ทำงานถูกต้องอยู่แล้ว) ยังไม่ได้เห็นด้วยตาเพราะพรีวิวไม่ focus จริง

- Artifact เดิม อัปเดตแล้ว (Version 24): https://claude.ai/artifact/SA1qEi8p8yaPUeQeXmham7

## 25. ภาพจริงชุดแรก — จากโฟลเดอร์ `Image` (2026-09-25)

**วิเคราะห์ภาพทั้ง 10 ไฟล์ใน `C:\Users\pawin.s\Desktop\BTS\Image\`**: Banner (CGI monorail+ป้าย BTS เรืองแสง), Icons (เอกสาร/กราฟหุ้น 2 ไฟล์), Logo (ตรงกับที่ inline ในโค้ดอยู่แล้ว), News ×2 (แบนเนอร์หุ้นกู้ + ภาพกิจกรรมปลูกต้นไม้), Popup ×2 (แบนเนอร์หุ้นกู้เวอร์ชันใหญ่ + **ภาพไว้อาลัยพระราชวงศ์ — ไม่ใช้เด็ดขาด เนื้อหาละเอียดอ่อนเฉพาะกิจ**), Reports ×2 (ปกรายงานประจำปี/ความยั่งยืนจริง)

**ผู้ใช้เลือกใช้ 5 ไฟล์** (ไม่รวม hero banner — Hero section ยังไม่แตะ): `news-2026-09-07.webp`, `annual-report-2025-cover.jpg`, `sustainability-report-2025-26-cover.jpg`, `news-2026-08-28.webp`, `popup-2026-08-31.webp`

**ที่เก็บไฟล์**: คัดลอกเข้าโฟลเดอร์ใหม่ `img/` ในโปรเจกต์ (ตั้งชื่อสื่อความหมาย) แล้วอ้างอิงแบบ relative path เหมือน `fonts/` เดิม — อัปโหลดเข้า Artifact ผ่านพารามิเตอร์ `files` แล้ว (ยืนยันด้วย `list scope:files`: ทั้ง 5 ไฟล์ขนาดตรงกับต้นฉบับ)

**จุดที่ใช้**:
1. **Section 7 (เรื่องราว) — การ์ด ESG**: `story-esg-treeplanting.webp` (ภาพพนักงานถือต้นกล้าในสถานี มีป้าย Net Zero) แทนที่ placeholder ไล่สี — เปลี่ยนพาดหัวจากเดิม (พลังงานแสงอาทิตย์) เป็น "พนักงานบีทีเอสร่วมกิจกรรมปลูกต้นไม้ เดินหน้าสู่เป้าหมาย Net Zero 2050" ให้ตรงกับภาพจริง
2. **Section 7 — การ์ด MATCH**: `story-debenture-offering.webp` (แบนเนอร์หุ้นกู้เวอร์ชันใหญ่) แทนที่การ์ด "จับมือพันธมิตรใหม่..." เดิม — เปลี่ยนพาดหัวเป็น "เตรียมเสนอขายหุ้นกู้ 3 ชุดแก่ผู้ลงทุนทั่วไป ระดับ Investment Grade BBB+" วันที่ 24 ส.ค. 2569 (วันที่ TRIS จัดอันดับตามที่ระบุในภาพจริง)
3. **Section 6 (IR) — ลิสต์เอกสาร**: เพิ่ม thumbnail ภาพปกจริง (40×52px มุมโค้ง) แทนไอคอนวงกลมเดิมในแถว "รายงานประจำปี" (`report-annual-2025.jpg`) และ "ข่าวแจ้งตลาดหลักทรัพย์" (`ir-debenture-notice.webp`, ปรับคำอธิบายเป็นข่าวจัดอันดับหุ้นกู้จริง) + **เพิ่มแถวใหม่ที่ 6** "รายงานความยั่งยืน" (`report-sustainability-2025-26.jpg`) ต่อจากแถวรายงานประจำปี
4. **ไม่ใช้**: ไอคอน PNG 2 ไฟล์ (ขัดกับ Icon DNA แบบ Lucide outline ที่ยึดมาตั้งแต่ต้น), โลโก้ svg (ซ้ำกับที่มีอยู่แล้ว), ภาพไว้อาลัย (ห้ามใช้), hero banner poster (ผู้ใช้ยังไม่ให้ใช้รอบนี้)

**Technical**: เพิ่ม CSS `.st-img img{position:absolute;inset:0;width:100%;height:100%;object-fit:cover}` (คลุม gradient placeholder เดิมและลาย dot ::before ที่ยังไม่ได้ถอด), `.ir-links .thumb{width:40px;height:52px;border-radius:6px;object-fit:cover;box-shadow:...}` — โครงสร้าง `.st-img`/`.ir-links a` เดิมไม่ต้องแก้

- Artifact เดิม อัปเดตแล้ว (Version 26): https://claude.ai/artifact/SA1qEi8p8yaPUeQeXmham7

## 26. Typography/Spacing DNA overhaul — ยุบเหลือ 2 น้ำหนัก, สเกลใหม่, letter-spacing/line-height เดียวทั้งเว็บ (2026-09-25)

**เหตุผล**: ผู้ใช้ขอให้ลดความซับซ้อนของระบบตัวอักษร/spacing ที่สะสมมาหลายรอบ build ให้เป็นกฎที่จำง่ายและสม่ำเสมอกว่าเดิม

**น้ำหนักตัวอักษร — เหลือ 2 น้ำหนักจริงในเว็บ**:
- ตัดสินใจ: `500` ไม่มีไฟล์ฟอนต์จริง (Thin/Regular/Bold/ExtraBold/Heavy เท่านั้น) → ใช้ `400` แทนทั้งจุดที่ตั้งใจเป็น "500" และจุดที่เดิมตั้งใจเป็น "300" (ผู้ใช้ยืนยันให้รวมเป็นก้อนเดียว)
- **ถอด `@font-face` ที่ไม่ใช้แล้วทิ้ง 3 รายการ**: Thin(300), ExtraBold(800), Heavy(900) — เหลือแค่ Regular(400) และ Bold(700) 2 ไฟล์ (ลดข้อมูลที่ต้องโหลด ~92KB)
- Mapping ตรงไปตรงมา: เดิม 900→700, 800→700, 700→400, 600→400 (เจอ 2 จุดหลุด), 400→400 (คงเดิม), 300→400
- ผลลัพธ์: **700 = หัวข้อ/ตัวหนาทั้งหมด, 400 = ทุกอย่างอื่น** (eyebrow, label, ปุ่ม, body, ตัวเลขสถิติ)

**สเกลขนาด (clamp) — ปรับทุก headline/subhead ตาม role**:
| กลุ่ม | ใหม่ | ตัวอย่าง |
|---|---|---|
| Hero H1 | `40→80px` | .hero-h1 |
| Headline ใหญ่สุด | `40→84px` (pfB-h ตัวเลขยักษ์ 01/03 คงสัดส่วนพิเศษที่ `64→140px`) | hero-gate h2, ecoB-h2, next-h2, pfB-h |
| Headline มาตรฐาน | `32→58px` | ทุกหัว section 3-7 (pf-h2, proof-h2, im-h2, imB-h2, ir-h2, st-h2, netmap-h2, proofB-h2, pfC-h2, ecoC-h2, ft-tagline, ecoD-motto) |
| หัวข้อการ์ด/รอง | `24→36px` | เกือบทุกหัวข้อย่อยในการ์ด (ecoB/C/D, pf-cap, pfB-def, pfC-row, im-claim, imB-panel, st-item.feature, menu-row .label) |
| Label/eyebrow | `10→12px` | .eyebrow, dt-text, ทุก label ตัวเล็ก uppercase |
| Body ทั่วไป | รวมเป็น `16px` คงที่ | ข้อความในการ์ด/ลิสต์ที่กระจัดกระจาย 13.5-17px เดิม |
| Intro/lede | `18-20px` (pf-read พิเศษ `24→32px` เพราะมี highlight-on-scroll) | eco-sub, proof-lede, pfB-lede ฯลฯ |
| ตัวเลขสถิติใหญ่ | คงเดิมถ้าอยู่ในกรอบ `40→56-116px` อยู่แล้ว (proof-num, ir-price, proofB-stat b, ld-pct ไม่ต้องแก้) — เกินกรอบตัดลง (pf-count-num 128→116px) | |
| **ไม่แตะ** | marquee ghost text พื้นหลัง (next-row 96-236px, pfC-ghost wordmark 128px), netmap-stat/ir-fin dd (KPI ขนาดกะทัดรัดในกริด ไม่ใช่ headline hierarchy) | เหตุผล: เป็นข้อความตกแต่ง/สถิติย่อยขนาดกะทัดรัด ไม่ใช่ลำดับชั้น headline ที่ตารางนี้ควบคุม |

**Letter-spacing**: ทุกจุด (85 จุด) → `0em` เดียวกันหมด (เดิมมี 2 กลุ่มคือ headline แคบ vs label กว้าง .12-.26em)

**Line-height**: ทุกจุด (67 จุด) → `1.5` เดียวกันหมด (เดิม headline แน่น 0.86-1.15, body หลวม 1.55-1.7, label 1)

**Spacing (gap)**: ปรับ 3 ระดับล่างด้วยการ clamp ค่าเดิมเข้ากรอบใหม่ (ค่าที่อยู่ในกรอบอยู่แล้วไม่แตะ, ค่าที่เกินกรอบตัดเข้าขอบบน/ล่าง) — จิ๋ว `4-8px`, เล็ก `12-16px`, กลาง `24-32px` — **ระดับใหญ่ (64px) และกว้างพิเศษ (80px) คงเดิมตามที่ตกลง** ไม่อยู่ในสโคปนี้

**Technical**: ทำผ่านสคริปต์ Node.js ชั่วคราว (sweep แบบ mechanical สำหรับ weight/letter-spacing/line-height/gap ที่เป็น flat value ทั้งไฟล์ โดยป้องกัน `font-weight:700` ของ @font-face Bold ไม่ให้โดน sweep ผิด) ตามด้วยแก้ `clamp()` ของ headline ทีละจุดด้วยมือ (~30 selector) เพราะต้องใช้ role-based judgment — ตรวจสอบหลัง sweep แล้วว่า: มี `@font-face` เหลือ 2 รายการพอดี, ไม่มี font-weight 300/600/800/900 หลงเหลือ, letter-spacing/line-height เหลือค่าเดียว, HTML/CSS/JS ยังสมดุล (brace/tag count ตรง), โหลดในเบราว์เซอร์ไม่มี console error, คอมพิวเต็ดสไตล์ของ .hero-h1/.eyebrow/.eco-sub ตรงตามสเปกใหม่ทุกจุด

- Artifact เดิม อัปเดตแล้ว (Version 27): https://claude.ai/artifact/SA1qEi8p8yaPUeQeXmham7

## 27. Border-radius DNA — ปรับ 2 ระดับ (2026-09-25)

- **การ์ดพิเศษ/เวทีใหญ่**: `28px → 32px` (imB-stage, netmap-stage ที่ใช้ 28 เดิม)
- **องค์ประกอบเล็ก**: clamp ค่าเดิมที่กระจาย `2–18px` เข้ากรอบใหม่ `8–16px` — ค่าที่อยู่ในกรอบอยู่แล้ว (10, 14, 16) ไม่แตะ, ค่าต่ำกว่าขอบล่างดันขึ้น (2,4,6 → 8: pf-rail .bar, focus outline, ft-lines i, ir-links .thumb), ค่าเกินขอบบนตัดลง (18 → 16: ecoB-scene, imB-tab)
- **ไม่แตะ**: Pill (999px) และ การ์ด/บล็อกใหญ่ (20–24px) — ผู้ใช้ไม่ได้ระบุให้เปลี่ยน 2 ระดับนี้
- ตรวจแล้ว: กระจายค่าหลัง sweep = `8,10,14,16,20,24,32,999` ตรงตามแผน, brace/tag ยังสมดุล, ไม่มี console error

- Artifact เดิม อัปเดตแล้ว (Version 28): https://claude.ai/artifact/SA1qEi8p8yaPUeQeXmham7

## 28. Loader — ถอดคอลัมน์ซ้าย + MOVE/MIX/MATCH ทิ้ง (2026-09-25)

ถอด `.ld-col.ld-left` ทั้งก้อน (wordmark "BTS GROUP" + label "Our network" + ลิสต์ 8 บริษัทในเครือ) และถอดลิสต์ MOVE/MIX/MATCH + label "Platforms" ออกจาก `.ld-col.ld-right` — เหลือแค่ **แผนที่ dotted กลางจอ + ตัวนับ % progress ใต้แผนที่** (จัดกึ่งกลางแนวตั้งแทน grid 3 คอลัมน์เดิม)

**Technical**: เปลี่ยน `.ld-inner` จาก `display:grid` 3 คอลัมน์ เป็น `display:flex; flex-direction:column; align-items:center` แคบลงเหลือ `max-width:640px`, ลบ CSS ที่ไม่ใช้แล้วทั้งหมด (`.ld-brand`, `.ld-label`, `.ld-list` และลูก, `.ld-right`) และลบ JS ส่วน stagger-list (`items`/`forEach` ที่ toggle class `.in` ตาม `data-at`) ออกจากฟังก์ชัน loader เพราะไม่มี list เหลือให้ stagger แล้ว — ตรวจแล้วว่า brace/tag ยังสมดุล ไม่มี reference ค้างถึง class ที่ลบไป และโหลดในเบราว์เซอร์ไม่มี console error

- Artifact เดิม อัปเดตแล้ว (Version 29): https://claude.ai/artifact/SA1qEi8p8yaPUeQeXmham7
