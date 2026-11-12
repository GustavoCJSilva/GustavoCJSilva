<p align="center">
  <img src="assets/gustavo.jpg" alt="Gustavo César" width="200" />
</p>

<h1 align="center">Hi, I'm Gustavo César 👋</h1>

<p align="center">
  <b>Full-Stack Developer</b> · PHP · React · TypeScript · Node.js · Python · MySQL/PostgreSQL · AWS
</p>

<p align="center">
  <a href="https://github.com/GustavoCJSilva">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=20&duration=3200&pause=900&color=2F81F7&center=true&vCenter=true&width=640&lines=I+build+business+software+end-to-end;From+database+schema+to+production+deploy;APIs%2C+integrations+and+workflow+automation;Open+to+remote+contract+work" alt="I build business software end-to-end" />
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Open%20to-Remote%20Contract%20(B2B)-2ea44f?style=for-the-badge" alt="Open to remote contract work" />
  <img src="https://img.shields.io/badge/Timezone-UTC%E2%88%923%20(BRT)-555?style=for-the-badge" alt="Timezone UTC-3" />
  <img src="https://img.shields.io/badge/English-Intermediate%20(B1)-1f6feb?style=for-the-badge" alt="English: Intermediate" />
</p>

<p align="center">
  <a href="https://zenitetechnology.com.br/en/"><img src="https://img.shields.io/badge/Portfolio-zenitetechnology.com.br-1d1b17?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Portfolio" /></a>`n  <a href="https://www.linkedin.com/in/gustavo-c%C3%A9sar-526791311/"><img src="https://img.shields.io/badge/LinkedIn-Gustavo%20C%C3%A9sar-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="mailto:gustavocjsilva@outlook.com"><img src="https://img.shields.io/badge/Email-gustavocjsilva%40outlook.com-D14836?style=for-the-badge&logo=maildotru&logoColor=white" alt="Email" /></a>
</p>

---

## 👨‍💻 About me

I'm a full-stack developer from Brazil who builds and ships **complete web systems**: UI, REST API, database, security and deploy. My most recent work is a **production platform that replaced a company's spreadsheet-driven operations** with three integrated systems (finance, import costing and returns) behind a single sign-on portal. I designed, built and maintain all of it.

What I bring to a team:

- **End-to-end ownership.** I take a feature from a vague business problem to a deployed, monitored solution, without hand-offs.
- **Business-domain fluency.** Cash flow, P&L, accounts payable/receivable, import taxes, marketplace returns. I talk to the people who use the software and turn their process into code.
- **Security by default.** HMAC-signed SSO, CSRF protection, AES-256-GCM encrypted secrets, rate limiting, optimistic locking.
- **Integrations.** REST APIs, OAuth 2.0, signed webhooks, and connectors for marketplaces (Mercado Livre, Shopee, Amazon, Shopify, TikTok Shop and others).
- **AI-assisted workflow.** I use AI tools daily to ship faster while keeping code reviewed, tested and maintainable.

---

## 🧰 Tech stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=php,nodejs,python,java,cs,dotnet&perline=6" alt="Backend" /><br/>
  <img src="https://skillicons.dev/icons?i=react,ts,js,vite,html,css&perline=6" alt="Frontend" /><br/>
  <img src="https://skillicons.dev/icons?i=mysql,postgres,aws,git,github,linux&perline=6" alt="Data, cloud and tools" />
</p>

| Area | Technologies |
|---|---|
| **Backend** | PHP 8 (main) · Node.js · Python · Java · C# / .NET |
| **Frontend** | React · TypeScript · Vite · JavaScript · HTML5 · CSS3 |
| **Databases** | MySQL / MariaDB · PostgreSQL · relational modeling, migrations, JSON columns |
| **Cloud & DevOps** | AWS (EC2, deploys) · Linux · Apache / LiteSpeed · cron jobs · Git / GitHub |
| **Integrations & Security** | REST · OAuth 2.0 · HMAC-signed webhooks · SSO · AES-256-GCM |
| **Enterprise platforms** | ![Salesforce](https://img.shields.io/badge/Salesforce-00A1E0?style=flat-square&logo=salesforce&logoColor=white) support and customization |

---

## 🚀 Featured project: Feheros Platform

> **Problem:** a Brazilian e-commerce/import company ran finance, import costing and product returns on shared spreadsheets, with no access control, no audit trail and constant overwrite conflicts.
>
> **Solution:** a web platform, **in production and used daily**, with a central access portal and **single sign-on** into three systems. Each team member only sees the systems their department is allowed to use.
>
> **My role:** sole developer. Architecture, backend, frontend, database design, security, deploy and ongoing maintenance.

```mermaid
flowchart TB
    U["👤 Staff<br/>(browser)"] -->|HTTPS| P["🏠 Access portal<br/>login · departments · permissions"]

    P -->|"signed ticket (HMAC, 60 s, single-use)"| GF
    P -->|"signed ticket"| IMP
    P -->|"signed ticket"| DEV

    subgraph GF["💰 Finance"]
        GF_SPA["React + TS SPA"] -->|JSON| GF_API["REST API · PHP 8.3"]
    end
    subgraph IMP["🚢 Import Costing"]
        IMP_SPA["React + TS SPA"] -->|JSON| IMP_API["REST API · PHP 8.3"]
    end
    subgraph DEV["↩️ Returns"]
        DEV_SPA["React + TS SPA"] -->|JSON| DEV_API["REST API · PHP 8.3"]
    end

    GF_API --> DBF[("MySQL<br/>finance")]
    IMP_API --> DBF
    DEV_API --> DBD[("MySQL<br/>returns")]
    IMP_API -. "creates payables,<br/>import loans and product costs" .-> GF_API

    MP["🛒 Marketplaces<br/>Mercado Livre · Shopee · Amazon<br/>Magalu · Shein · TikTok Shop · Shopify"] -->|Webhooks| DEV_API
    MP -->|payouts| GF_API
    CRON["⏱️ Cron"] -->|sync and scheduled jobs| GF_API
    CRON --> DEV_API
```

### 🏠 Access portal (SSO)

| Feature | How it works |
|---|---|
| 🔑 **Single sign-on** | Users log in once. The portal issues an HMAC-SHA256 signed ticket valid for 60 seconds and one use; each system verifies signature, audience and replay |
| 🏢 **Department-based access** | Each department unlocks a set of systems, with per-user overrides. Direct URL access is blocked without permission |
| 🛡️ **Security** | CSRF protection, forced password change on first login, lockout after 5 failed attempts, sessions revoked when permissions change |
| 🚪 **Break-glass access** | If the portal is down, an admin can still log in to each system with a local credential |

### 💰 Finance

| Feature | How it works |
|---|---|
| 📒 **Accounts payable & receivable** | Installments, recurring entries, settlement, reversal, inter-account transfers and attachments |
| 📊 **P&L and cash flow statements** | Custom chart of accounts with monthly results, balance sheet and KPIs |
| 🔮 **Cash flow forecasting** | Yearly, monthly and daily (calendar) views, custom ranges, and past months showing actuals vs. forecast |
| 🏦 **Loans** | Loan contracts with installments, auto-linked to payables, outstanding balance chart per bank |
| 🛒 **Purchasing & reconciliation** | Purchase plans and orders with approval flow, bank reconciliation from statements |
| 📥 **Spreadsheet import** | `.xlsx` and XML parsing directly in the browser, with no third-party library |

### 🚢 Import Costing

| Feature | How it works |
|---|---|
| 📂 **Document ingestion** | Reads every file of an import process at once (electronic invoice XML, closing spreadsheets, customs declaration, reconciliation) and fills the whole form |
| 🧮 **Landed cost per unit** | Computes Brazilian import taxes (II, IPI, PIS, COFINS, ICMS), allocates costs across items by CIF value and calculates the real unit cost |
| 🔗 **Finance integration** | On save, creates the payables, registers import financing as a loan and updates product costs |
| 📈 **Payback simulation** | Month-by-month projection over 24 months, including financing installments |
| 📤 **Export / re-import** | Generates `.xlsx` in the browser (zip + XML written by hand) with a hidden sheet that allows re-importing the process |

### ↩️ Returns management

| Feature | How it works |
|---|---|
| 👥 **Granular permissions** | Admin and user roles with fine-grained permissions (create, edit, attach, delete, backup) |
| ⚔️ **Optimistic concurrency** | Detects concurrent edits to the same record (HTTP 409) and prevents silent overwrites |
| 🖼️ **Photos & videos** | Chunked uploads up to 200 MB, client-side image compression, gallery and video player |
| 🔄 **Real-time updates** | Every user sees changes without reloading the page |
| 🗄️ **Archiving & audit** | Completed records are archived after 60 days (with prior notice), full change history and daily backups |
| 🔌 **Integration layer** | Pluggable connector per marketplace, encrypted credentials (AES-256-GCM), webhooks and idempotent upserts |

`PHP 8.3` `MySQL` `React` `TypeScript` `Vite` `Python` `Node.js` `REST` `SSO` `HMAC` `OAuth 2.0` `AES-GCM`

> 🔒 The source code is private (client work). I'm happy to walk through the architecture and code in a call or a screen-share.

---

## 💼 What I can help you with

| | |
|---|---|
| **Build** | New web apps, internal tools, admin dashboards and REST APIs |
| **Maintain** | Bug fixes, feature work and gradual modernization of legacy systems |
| **Integrate** | Third-party APIs, payment and marketplace platforms, webhooks, SSO |
| **Data** | Schema design, query optimization, data migrations |
| **Deploy** | Cloud setup, server configuration and production releases |

---

## 🎯 Currently

- ✅ Running a multi-system platform in production with SSO and a marketplace integration layer
- 🔄 Connecting live APIs for Mercado Livre, Shopee, Amazon and other marketplaces
- 📚 Deepening software architecture, automated testing and CI/CD
- 🌎 **Looking for remote contract roles with international teams**

---

## 🎸 Beyond code

<table>
  <tr>
    <td width="35%" align="center">
      <img src="assets/gustavo-anime.jpg" alt="Anime-style portrait of Gustavo: coding setup, guitar, martial arts gear" width="100%" />
    </td>
<td width="65%">

🎸 **Guitar**: how I switch off after a day of coding.

🔥 **RPGs and Souls-likes**: die, learn the pattern, try again. Pretty much debugging.

🥋 **Martial arts**: discipline, consistency and respect.

📚 **Always learning**: there's always a book or a course in progress.

</td>
  </tr>
</table>

---

<p align="center">
  <b>Let's build something together.</b><br/><br/>
  <a href="mailto:gustavocjsilva@outlook.com">📧 gustavocjsilva@outlook.com</a> ·
  <a href="https://www.linkedin.com/in/gustavo-c%C3%A9sar-526791311/">💼 LinkedIn</a>
</p>
