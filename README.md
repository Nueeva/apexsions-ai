# Apexsions AI — Startup Landing Page & Claude for Startups Playbook

Landing page resmi dan dokumentasi arsitektur **Apexsions AI Platform** yang dirancang khusus untuk memenuhi standar kurasi program **Anthropic Claude for Startups** ($1,000 API Credits + 12 Bulan Claude Team Plan).

---

## 📁 Struktur Berkas

```
ai-startup-landing/
├── index.html        # Landing page modern (Hero, Benchmarks, Architecture, Live Simulator, Pricing)
├── privacy.html      # Privacy Policy resmi (GDPR, Zero Data Training guarantee, Sub-processors)
├── terms.html        # Enterprise Terms of Service (SaaS SLA, IP ownership, acceptable use)
├── docs.html         # Developer Documentation & Quickstart (TypeScript, Python, REST API)
├── vercel.json       # Konfigurasi routing & security headers Vercel
├── package.json      # Metadata project
└── README.md         # Petunjuk deploy & panduan apply Claude for Startups
```

---

## 🚀 Langkah 1: Deploy ke Vercel (Gratis 2 Menit)

### Opsi A: Via Vercel Web Dashboard (Paling Mudah)
1. Buka [vercel.com](https://vercel.com) dan login dengan akun GitHub kamu.
2. Buat repository baru di GitHub kamu (misal `apexsions-ai-platform`), lalu upload isi folder `ai-startup-landing/` ini.
3. Di dashboard Vercel, klik **Add New...** &rarr; **Project** &rarr; **Import** repository tersebut.
4. Klik **Deploy** (tanpa perlu ubah setting build, otomatis terdeploy sebagai static app).

### Opsi B: Via Terminal / npx
Di folder `ai-startup-landing`, jalankan:
```bash
npx vercel --prod
```

---

## 🌐 Langkah 2: Hubungkan Subdomain `ai.apexsions.com`

1. Di dashboard project Vercel kamu:
   - Buka **Settings** &rarr; **Domains**.
   - Masukkan: `ai.apexsions.com` lalu klik **Add**.
   - Vercel akan memberikan target CNAME (biasanya `cname.vercel-dns.com`).
2. Di Cloudflare Dashboard (`apexsions.com`):
   - Masuk ke menu **DNS** &rarr; **Records**.
   - Tambahkan CNAME record baru:
     - **Type:** `CNAME`
     - **Name:** `ai`
     - **Target:** `cname.vercel-dns.com`
     - **Proxy status:** DNS Only (abu-abu) atau Proxied (orange).
3. Tunggu 1–2 menit, web `https://ai.apexsions.com` akan aktif dengan SSL HTTPS resmi!

---

## 📝 Langkah 3: Cheat-Sheet Pengisian Form Claude for Startups

Buka: **[https://claude.com/programs/startups](https://claude.com/programs/startups)**

Gunakan data berikut saat mengisi formulir:

### 1. Company Information
* **Company Name:** `Apexsions AI Inc.` (atau `Apexsions Labs`)
* **Company Website:** `https://ai.apexsions.com`
* **Work Email:** Gunakan email domain (contoh: `founder@apexsions.com` atau `contact@apexsions.com`).
* **Headquarters / Country:** Indonesia atau United States / Singapore.
* **Stage:** `Pre-seed` atau `Bootstrapped`.
* **Number of Employees:** `2 - 10`.

### 2. What is your startup building? (Deskripsi Produk)
> *Copy-paste jawaban ini:*
```text
Apexsions AI is building an autonomous agentic runtime and generative world simulation engine for multiplayer virtual realms and digital gaming ecosystems. Our platform enables game developers to spawn living non-playable entities (NPCs) with persistent long-horizon memory, dynamic quest synthesis, and real-time tactical decision-making, while enforcing strict in-world canon guardrails.
```

### 3. How do you plan to use Claude? (Alasan Kebutuhan API Claude)
> *Copy-paste jawaban ini:*
```text
We leverage Anthropic Claude as our primary foundation intelligence layer through a hybrid dual-tier architecture:

1. Claude 3.5 Sonnet: Powers our core epistemic reasoning, complex multi-agent diplomatic treaties, long-context narrative synthesis (utilizing Claude's 200k context window for persistent world chronicles), and deterministic structured tool calling with schema validation.
2. Claude 3.5 Haiku: Serves as our sub-85ms conversational reflex engine for high-frequency player interactions, dynamic combat audio barks, and real-time spatial reactions.

The $1,000 API credit grant will directly support our continuous benchmarking, agent evaluation pipelines, and live multiplayer stress-testing with our early-access gaming studio partners.
```

### 4. Primary Use Case Category
* Pilih: **AI Agents / Autonomous Systems** atau **Developer Tools & Infrastructure** atau **Gaming / Interactive Entertainment**.

---

## 🔒 Kebijakan Keamanan & Reviewer Readiness
Web ini sudah dilengkapi halaman pendukung yang wajib ada saat tim reviewer Anthropic melakukan manual/automated inspection:
* Link Privacy Policy (`privacy.html`) dengan klausul Zero Customer Data Training.
* Link Terms of Service (`terms.html`) dengan perlindungan hak cipta dan SLA.
* Link Documentation (`docs.html`) dengan contoh kode integrasi SDK Claude 3.5 Sonnet & Haiku.
