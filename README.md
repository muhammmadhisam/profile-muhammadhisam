<div align="center">

# มูฮัมหมัดฮีซาม ปาล๊ะ (ซัง)

### Mid-level Backend Developer
**System Architecture · Scalable & Secure APIs · End-to-End Ownership**

ออกแบบสถาปัตยกรรมและพัฒนา RESTful API สำหรับระบบระดับ Production ข้าม 4 อุตสาหกรรม —
HealthTech · Energy · Enterprise · Digital Platform

<br/>

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=node.js&logoColor=white)
![Bun](https://img.shields.io/badge/Bun-000000?style=flat&logo=bun&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat&logo=nestjs&logoColor=white)
![Hono](https://img.shields.io/badge/Hono-E36002?style=flat&logo=hono&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat&logo=prisma&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=redis&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)

[![Portfolio](https://img.shields.io/badge/Portfolio-hisam.dev-2563EB?style=flat&logo=vercel&logoColor=white)](https://github.com/muhammmadhisam/profile-muhammadhisam)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/muhammadhisam-pala-45b83825a)
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:muhammadhisam.pala@gmail.com)

</div>

---

## 👋 เกี่ยวกับผม

ผมเป็น Backend Developer ที่ทำงานครบตั้งแต่เก็บ requirement, ออกแบบระบบและฐานข้อมูล, เขียน API ไปจนถึง deploy และดูแลระบบบน production

ตลอด 5+ ปีที่ผ่านมา ทำงานข้ามหลายอุตสาหกรรม และได้ลองใช้สถาปัตยกรรมหลายแบบ —
Microservices, Multi-tenant SaaS, Event-driven, Queue และ AI/RAG — กับโจทย์ธุรกิจ SME ไทยจริง

| | |
|---|---|
| 🗓️ **5+ ปี** ในสายพัฒนา | 🚀 **10+ ระบบ** ขึ้น Production |
| 🏭 **4 อุตสาหกรรม** ที่เคยส่งมอบ | 🔁 **End-to-End** Requirement → Deploy |

---

## 🏗️ แนวทางการออกแบบระบบ (Production Blueprint)

สถาปัตยกรรมที่ผมใช้ซ้ำในหลายโปรเจกต์ — Monorepo แยก App ชัดเจน, API แบบ type-safe,
งานหนักโยนเข้า Queue, และรองรับ Real-time / AI ในเลเยอร์เดียวกัน

```mermaid
flowchart TD
    subgraph Clients["🖥️ Clients"]
        W["Web · Next.js"]
        A["Admin Console"]
        L["LINE LIFF / Mini App"]
    end

    W --> API
    A --> API
    L --> API

    API["⚙️ API Gateway · Hono / NestJS<br/>Type-safe · JWT + RBAC · OpenAPI"]

    API --> DB[("🐘 PostgreSQL · Prisma")]
    API --> Q["📨 Queue · BullMQ + Redis"]
    Q --> WK["🔧 Worker · Background Jobs"]
    API --> ST[("🗄️ Object Storage · R2 / S3")]
    API --> AI["🤖 AI Layer · RAG / Vector<br/>OpenAI · pgvector · Voyage"]
    API -. "SSE · Real-time" .-> W

    classDef api fill:#eff6ff,stroke:#3b82f6,color:#1e40af;
    classDef ai fill:#f5f3ff,stroke:#8b5cf6,color:#5b21b6;
    class API api;
    class AI ai;
```

---

## 💼 ผลงานเด่น (Work)

| Project | สรุป | Stack |
|---------|------|-------|
| **ERC — Centralized Energy Data Platform** | รวมข้อมูลไฟฟ้าระดับประเทศจากหลายแหล่งเข้าสู่ dashboard เดียว ประมวลผลแบบ near real-time | `NestJS` `Microservices` `PostgreSQL` |
| **Pool Manager — Gas Pool Management** | คำนวณต้นทุนก๊าซจากหลายแหล่งจัดหา (LNG/Gulf/Myanmar) พร้อม Cost Allocation & Pricing Workflow | `Cost Engine` `Audit Trail` |
| **Verso PO/PR — Procurement Workflow** | จัดซื้อครบวงจร Multi-Level Approval + Budget Validation ตามหลัก Internal Control | `Approval Flow` `Budget Control` |
| **[Prolab — Health Service Platform](https://ai.prolab.co.th/th)** 🔗 | AI Health Analytics ช่วยแพทย์ประเมินความเสี่ยง + ปรับ Lab Result System (ลดเวลารอผล 3–7 → 1–3 วัน) | `AI Analytics` `HL7` `LAB System` |
| **ICMT — Device Registration** | ลงทะเบียน/ยืนยันอุปกรณ์โทรศัพท์ด้วย IMEI แยก Web/Admin/Storage/Worker | `Turborepo` `Next.js 14` `Hono` `Prisma` `Redis` |

---

## 🧪 Side Projects — *Currently Building* 🟢

โปรเจกต์ที่พัฒนานอกเวลางาน เพื่อแก้ปัญหาธุรกิจ SME ไทยจริง และทดลองสถาปัตยกรรมระดับ Production

| Project | Highlight | Stack |
|---------|-----------|-------|
| **[StockSook](https://stocksook.pixelranklab.com/)** 🔗 | SaaS ERP + POS สำหรับ SME ไทย เข้าใช้ผ่าน LINE Mini App ไม่ต้องติดตั้ง | `Turborepo` `Next.js 15` `Hono` `PostgreSQL` `LINE LIFF` |
| **[Clinic ERP](https://erp-clinic.pixelranklab.com/)** 🔗 | Multi-tenant B2B SaaS 6 Microservices · fp-ts · SuperTokens | `Hono 4` `fp-ts` `BullMQ` `Cloudflare R2` |
| **M-MERT** | ระบบสั่งการกู้ภัยการแพทย์ฉุกเฉิน Real-time (SSE) · response < 10ms | `Bun` `Hono 4` `Effect` `SSE` `JWT+RBAC` |
| **[MeawSook](https://meawsook.com/)** 🔗 | แมวหาย + บริจาคอาหารโปร่งใส · AI จับคู่ใบหน้าแมวด้วย Vector Search | `Voyage MM-3` `pgvector` `LINE LIFF` |
| **[MoveSook](https://movesook.com/)** 🔗 | Two-sided marketplace เรียกคนขับขนย้าย On-demand · end-to-end type-safe RPC | `Next.js` `Hono` `Prisma` `Zod` `Turborepo` |
| **Clinic Booking + AI Chatbot** | จองคิวคลินิก + ผู้ช่วย AI แบบ RAG ตอบจากฐานข้อมูลจริง | `OpenAI` `Milvus` `LINE LIFF` `MinIO` |
| **SE Ranking Scraper API** | ดึงข้อมูล SEO อัตโนมัติด้วย Stealth Browser + Job Queue | `Bun` `Playwright Stealth` `BullMQ` `ExcelJS` |
| **EMS-ECI** | ระบบบันทึกผู้ป่วย & Checklist สำหรับพยาบาล ทดแทนกระดาษ | `Next.js 16` `Prisma 7` `better-auth` `ExcelJS` |

---

## 🧰 Tech Stack

**Backend**
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=node.js&logoColor=white)
![Bun](https://img.shields.io/badge/Bun-000000?style=flat&logo=bun&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat&logo=nestjs&logoColor=white)
![Hono](https://img.shields.io/badge/Hono-E36002?style=flat&logo=hono&logoColor=white)
![Elysia](https://img.shields.io/badge/ElysiaJS-0F172A?style=flat&logoColor=white)
![Fastify](https://img.shields.io/badge/Fastify-000000?style=flat&logo=fastify&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat&logo=go&logoColor=white)

**Frontend**
![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat&logo=next.js&logoColor=white)
![Angular](https://img.shields.io/badge/Angular-DD0031?style=flat&logo=angular&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind-06B6D4?style=flat&logo=tailwindcss&logoColor=white)

**Database & ORM**
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=mysql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=redis&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat&logo=prisma&logoColor=white)
![Milvus](https://img.shields.io/badge/Milvus_(Vector)-00A1EA?style=flat&logoColor=white)

**DevOps & AI**
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=githubactions&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat&logo=nginx&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonwebservices&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat&logo=openai&logoColor=white)
![Turborepo](https://img.shields.io/badge/Turborepo-EF4444?style=flat&logo=turborepo&logoColor=white)

**Architecture & Concepts** · System Design · Microservices · Multi-tenant SaaS · Event-driven · RAG / Vector Search · API Security · RBAC

---

## 📫 ติดต่อ

- 📧 **Email** — [muhammadhisam.pala@gmail.com](mailto:muhammadhisam.pala@gmail.com)
- 💼 **LinkedIn** — [muhammadhisam-pala](https://linkedin.com/in/muhammadhisam-pala-45b83825a)
- 💬 **Line** — hisam023
- 📱 **Phone** — 090-163-0867

---

<details>
<summary>📄 <b>เกี่ยวกับ Repo นี้</b> — Source ของหน้า Portfolio</summary>

<br/>

Repo นี้คือ source code ของหน้าเว็บ Resume / Portfolio แบบ Single Page —
สร้างด้วย **Tailwind CSS** สไตล์ [shadcn/ui](https://ui.shadcn.com/) โทนน้ำเงิน สะอาด และ responsive ทุกหน้าจอ
รวมถึง **inline SVG architecture diagram** ของโปรเจกต์เด่น (Clinic ERP · M-MERT · MeawSook)

**Tech:** HTML5 · Tailwind CSS (CDN) · Vanilla JS · Google Fonts (Sarabun + Inter)

```bash
# Clone & run
git clone https://github.com/muhammmadhisam/profile-muhammadhisam.git
cd profile-muhammadhisam

open index.html            # เปิดตรง ๆ
# หรือรันผ่าน local server
python3 -m http.server 8000
npx serve .
```

**Deploy** เป็น static site ได้กับ GitHub Pages · Netlify · Vercel · Cloudflare Pages (build command ว่าง)

</details>

<div align="center">

<sub>Built with ♥ in Thailand</sub>

</div>
