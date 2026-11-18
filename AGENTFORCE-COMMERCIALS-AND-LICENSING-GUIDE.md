# 💼 Salesforce Agentforce Commercials, Pricing & Licensing Guide
## From "$2 per Conversation" to Flex Credits & Agentforce Coworker Licensing
**Trainer & Trainee Reference Manual — Enterprise AI FinOps & Licensing Architecture**

---

> [!IMPORTANT]
> **Why Every Salesforce Engineer & Architect Must Understand Agentforce Pricing:**
> In the Agentforce era, **architecture directly equals cost**. A poorly designed agent that makes 5 separate Flow calls instead of 1 consolidated Apex Invocable Action costs a business **5x more money per user interaction**. Understanding licensing models empowers you to architect cost-efficient, high-ROI AI solutions.

---

## 📋 Table of Contents
1. [The Pricing Evolution: "Earlier" vs. "Nowadays"](#1-the-pricing-evolution-earlier-vs-nowadays)
2. [Current Pricing Models Breakdown (Nowadays)](#2-current-pricing-models-breakdown-nowadays)
3. [Agentforce Coworker (Employee Agent) Licensing & Technical Entitlements](#3-agentforce-coworker-employee-agent-licensing--technical-entitlements)
4. [Real-World Cost Math & Break-Even Analysis](#4-real-world-cost-math--break-even-analysis)
5. [Hidden & Prerequisite Costs to Budget For](#5-hidden--prerequisite-costs-to-budget-for)
6. [Agentforce FinOps: How Developers Save Businesses Money](#6-agentforce-finops-how-developers-save-businesses-money)
7. [Live Session Q&A Cheat Sheet (Top Trainee Questions)](#7-live-session-qa-cheat-sheet-top-trainee-questions)

---

## 1. The Pricing Evolution: "Earlier" vs. "Nowadays"

Salesforce fundamentally evolved how businesses pay for AI agents between the initial launch (late 2024) and the modern consumption era (2025–2026).

### 🕰️ EARLIER (2023 – Late 2024): Rigid Per-Seat & "$2 Per Conversation"

When Salesforce first introduced generative AI and Agentforce at Dreamforce 2024, pricing followed two early structures:

1. **Einstein Copilot Add-On (Pre-Agentforce):**
   * Priced strictly **per seat** (~USD 50–75 / user / month) or bundled inside **Einstein 1 Edition** (~USD 500 / user / month).
   * *Problem:* Businesses had to pay for every employee license upfront, even for casual users who barely touched AI.
2. **The Launch "$2 per Conversation" Model (Late 2024):**
   * Salesforce famously launched Agentforce at a flat **USD 2.00 per conversation** (starting from the first user prompt until the session timed out or ended after 24 hours).
   * **Why Businesses Pushed Back on "$2 per Conversation":**
     * **Unfair for Simple Queries:** A customer typing *"What are your store hours?"* (1 quick lookup) cost the exact same **USD 2.00** as a complex 10-step order cancellation and refund workflow.
     * **Unworkable for Internal Employees (Coworker):** If an internal sales rep asked Agentforce Coworker 15 quick questions a day across separate sessions, the "$2/conversation" model made internal employee adoption financially unpredictable.
     * **Hard to Forecast:** Businesses hesitated to deploy agents on public websites where anonymous traffic or bots could trigger thousands of expensive USD 2.00 conversations overnight.

---

### 🚀 NOWADAYS (2025 – 2026): Flex Credits, Unmetered Employee Add-Ons & Flex Agreements

To solve those pain points, Salesforce shifted to a **hybrid value-based model** built around **Flex Credits** (pay-per-action), **Unmetered Employee Add-ons**, and **Flex Agreements**:

| Dimension | 🕰️ Earlier (Late 2024 Launch) | 🚀 Nowadays (Current Model) |
| :--- | :--- | :--- |
| **Primary Billing Metric** | Per Conversation (Flat session rate) | **Flex Credits (Per Action)** + **Per-User Add-ons** |
| **Base Unit Cost** | USD 2.00 per conversation | **USD 500 per 100,000 Flex Credits** (USD 0.005/credit) |
| **Cost per Standard Action** | Bundled inside USD 2.00 session | **20 Flex Credits = USD 0.10 per action** |
| **Cost per Voice Action** | N/A | **30 Flex Credits = USD 0.15 per action** |
| **Simple 1-Step Lookup Cost** | USD 2.00 | **USD 0.10** *(95% cost reduction!)* |
| **Complex 5-Step Resolution** | USD 2.00 | **USD 0.50** *(75% cost reduction!)* |
| **Employee / Coworker Option** | Expensive under per-conversation | **Unmetered Employee Add-ons** (USD 125–150/user/mo) OR Flex Credits |
| **Contract Flexibility** | Rigid annual license lock-in | **Flex Agreements** (swap unused human seats ⇄ Flex Credits) |
| **Starter / PoC Entry Cost** | Paid add-on required | **Salesforce Foundations** (Free starter credits on Enterprise+ orgs) |

> [!NOTE]
> **Important Org Rule:** Organizations generally standardize on **either** Flex Credits **or** legacy Per-Conversation buckets within an org (they are not typically mixed in the same consumption pool). New deployments overwhelmingly adopt **Flex Credits + Employee Add-ons**.

---

## 2. Current Pricing Models Breakdown (Nowadays)

Today, a business purchasing Agentforce chooses from **four commercial pillars** (often combining them):

### Pillar 1: Flex Credits (Consumption / Pay-Per-Action)
* **List Price:** **USD 500 per pack of 100,000 Flex Credits**.
* **How Actions Are Metered:**
  * **1 Standard Agent Action** (calling a Flow, running an Apex Invocable Method, invoking a Prompt Template, updating a CRM record, querying Data Cloud) = **20 Flex Credits (USD 0.10)**.
  * **1 Voice Action** (Agentforce Voice telephony turn) = **30 Flex Credits (USD 0.15)**.
  * *Note:* Simple greeting messages or conversational clarifications that do **not** execute an underlying tool/action generally do not burn action credits at the same rate as full tool executions.
* **Best For:** Customer-facing Service Agents, SDR Agents, Commerce Agents, and occasional internal employee workflows.

### Pillar 2: Agentforce Per-User Add-Ons (Unmetered Employee Usage)
* **Standard Cloud Add-On (Sales, Service, Field Service):** **USD 125 / user / month** (billed annually).
* **Industry Cloud Add-On (Financial Services, Health, Manufacturing, etc.):** **USD 150 / user / month**.
* **What It Includes:** **Unmetered (unlimited) employee-facing Agentforce usage** directly inside the user's daily CRM workspace (including Agentforce Coworker / Employee Agent workflows, Prompt Builder, and embedded AI insights).
* **Best For:** Heavy daily internal users (Sales Reps, Service Agents, Account Managers) who rely on AI all day long and want predictable fixed budgeting.

### Pillar 3: Agentforce 1 Editions (All-in-One Enterprise Bundle)
* **List Price:** Starting at **USD 550 / user / month** (e.g., *Agentforce 1 Sales Edition*, *Agentforce 1 Service Edition*).
* **What It Includes:**
  * Full Unlimited Edition CRM capabilities.
  * Unmetered employee-facing Agentforce Add-on included.
  * Massive pooled enterprise allocations of **Flex Credits** (millions per year) and **Data Cloud Credits** bundled right into the org.
  * Slack Enterprise integration & Tableau/Analytics capabilities.
* **Best For:** Large enterprises rolling out CRM + Data Cloud + Customer Agents + Employee Coworkers company-wide.

### Pillar 4: Flex Agreements & Payment Flexibility
* **Pay-As-You-Go (PayGo):** No upfront credit commitment; billed monthly in arrears for exact consumption.
* **Pre-Commit:** Commit to an annual credit pool for volume discounting, billed monthly with end-of-term true-up.
* **License-to-Credit Swapping:** Under a **Flex Agreement**, if a business automates 20% of its call center volume and needs fewer human seat licenses, it can **reallocate those unused human license dollars directly into Agentforce Flex Credits** (and vice versa if hiring scales up!).

---

## 3. Agentforce Coworker (Employee Agent) Licensing & Technical Entitlements

Since today's session focuses on **Agentforce Coworker**, here is how businesses buy and provision it:

### Commercial Buying Paths for Coworker
1. **Path A — Unmetered Employee Add-On (USD 125/user/mo):** Best when reps use **Find**, **Catch Up**, and **Plan & Act** heavily every single day. Zero fear of credit overages.
2. **Path B — Pure Flex Credits (USD 0.10/action):** Best for light/moderate internal users (e.g., executives, HR, IT staff) who run 5–15 actions per week (~USD 2–6/month per employee instead of USD 125!).
3. **Path C — Agentforce 1 Edition (USD 550/user/mo):** Already included out-of-the-box with enterprise Data Cloud & Flex Credit pools.

### Technical Licenses (Permission Set Licenses Visible in Salesforce Setup)
When a business purchases the commercial SKU, Salesforce provisions the following **Permission Set Licenses (PSLs)** inside `Setup ➔ Company Information`:

| Entitlement Name | API DeveloperName | Purpose in Coworker Architecture |
| :--- | :--- | :--- |
| **Agentforce Coworker** | `AISearchUserPsl` | Grants employees access to the AI Search bar & Coworker panel |
| **Agentforce Coworker Setup** | `AISearchAdminPsl` | Grants admins access to configure Coworker in Setup |
| **Data Cloud (Data 360)** | `GenieDataPlatformStarterPsl` | Powers sub-second indexing, vector search (RAG), and DMO grounding |
| **Agentforce (Default)** | `EinsteinGPTCopilotPsl` | Enables the core Atlas Reasoning Engine & agent execution |
| **Einstein Prompt Templates** | `EinsteinGPTPromptTemplatesPsl` | Enables authoring & grounding custom Prompt Templates |

---

## 4. Real-World Cost Math & Break-Even Analysis

Walk your trainees through these **3 real-world financial calculations** on screen—this makes licensing immediately click!

### 📊 Scenario A: Simple Customer Inquiry (1 Action)
* **Use Case:** Customer asks *"What is the status of Case #10029?"* (Agent triggers 1 Lookup Action).
* **Earlier Cost ($2/conv):** `USD 2.00`
* **Nowadays Cost (Flex Credits):** `1 action × 20 credits × USD 0.005` = **`USD 0.10`**
* **Savings:** **95% cheaper** under Flex Credits!

---

### 📊 Scenario B: Complex Customer Service Resolution (5 Actions)
* **Use Case:** Customer wants to cancel an order, verify eligibility, issue a refund, update Case, and send confirmation email (5 Actions total).
* **Earlier Cost ($2/conv):** `USD 2.00`
* **Nowadays Cost (Flex Credits):** `5 actions × 20 credits × USD 0.005` = **`USD 0.50`**
* **Savings:** **75% cheaper** than the old flat model!
* *Note:* Even if a single complex conversation runs **20 actions**, `20 × USD 0.10 = USD 2.00` (just matching the old flat rate). Most real conversations average 2–4 actions (`USD 0.20 – USD 0.40`).

---

### 📊 Scenario C: The Architect's Break-Even Formula (Coworker Add-On vs. Flex Credits)
Suppose a company has **100 Sales Reps** using **Agentforce Coworker**:

* **Unmetered Add-on Cost:** `100 reps × USD 125/mo` = **USD 12,500 / month**
* **Break-Even Point per Rep:**
  $$\frac{\text{USD } 125}{\text{USD } 0.10 \text{ per action}} = \mathbf{1,250 \text{ actions / user / month}}$$
  *(Roughly **60+ automated actions per working day** per employee!)*

* **Takeaway for Clients:**
  * If employees trigger **< 1,250 actions/month** (e.g. 15 actions/day = 300 actions/month = **USD 30/user/month**), **Flex Credits** is dramatically cheaper than buying USD 125/user seats!
  * If employees are power users triggering **> 1,250 actions/month** (or also need bundled Sales/Service AI features like Conversation Insights, Forecasting AI, and Case Summaries), the **USD 125/user/month Unmetered Add-On** wins!

---

## 5. Hidden & Prerequisite Costs to Budget For

Businesses often forget these **3 companion line items** when budgeting an Agentforce project:

1. **Base CRM Edition Prerequisite:**
   * Agentforce requires **Enterprise Edition**, **Unlimited Edition**, or **Performance Edition** (it is not available on Starter or Professional Editions).
2. **Data Cloud (Data 360) Consumption Credits:**
   * Grounding agents on unstructured PDFs/Knowledge (RAG Vector Search), Zero Copy federation (Snowflake/BigQuery), and storing **Einstein Trust Layer Audit Trails** consume **Data Services Credits** and **Data Storage**.
   * *Good News:* Eligible Enterprise+ orgs get **Salesforce Foundations** at **USD 0**, which includes a starter allocation of Data Cloud credits to build and pilot before purchasing paid credit packs.
3. **Monitoring Spend via Digital Wallet:**
   * Admins monitor real-time Flex Credits and Data Cloud credit burn inside **`Setup ➔ Digital Wallet`**.
   * Best practice: Configure **75% and 90% usage threshold email alerts** so there are never surprise overage invoices!

---

## 6. Agentforce FinOps: How Developers Save Businesses Money

Teach your trainees these **4 golden engineering rules** that directly reduce a client's monthly bill:

| Anti-Pattern (Expensive 💸) | Best Practice (Cost-Optimized 💰) | Cost Impact |
| :--- | :--- | :--- |
| Chaining 4 separate Flows (Get Account ➔ Get Opps ➔ Calculate ARR ➔ Format SLA) = **4 Actions** | Build 1 composite **Apex `@InvocableMethod`** (like our Day 5 `GetAccountMetricsAction`) = **1 Action** | **75% cost drop** (USD 0.10 vs USD 0.40) |
| Vague Topic/Action descriptions causing Atlas to pick the wrong tool and retry | Crisp, mutually exclusive semantic descriptions with explicit negative boundaries ("Do not use for...") | Eliminates wasted retry credits |
| Calling an LLM action for simple deterministic field validation | Use standard Lightning Validation Rules / Screen Flows before invoking Agentforce | Zero credits burned on static rules |
| Letting public web agents answer out-of-scope chitchat with RAG lookups | Add strict Guardrails & Off-Topic rejection instructions | Blocks spam/bot credit drain |

---

## 7. Live Session Q&A Cheat Sheet (Top Trainee Questions)

* **Q1: "Do we pay Flex Credits when testing in Agentforce Builder Simulator?"**
  * **A:** In **Simulate Mode**, actions are mocked/dry-run and do not burn live production Flex Credits. In **Live Test Mode** or in production orgs executing real LLM/Data Cloud calls, consumption meters against your org's credit pool (Developer/Scratch orgs have free developer allocations for learning).
* **Q2: "Does Salesforce charge extra for the LLM tokens (OpenAI / Anthropic / Gemini)?"**
  * **A:** No separate OpenAI/Anthropic invoice is required! Salesforce bundles the managed LLM inference, Einstein Trust Layer (PII masking & Zero Data Retention), and Atlas Reasoning Engine directly inside the **Flex Credits** or **Add-on** price. *(If you use Bring Your Own Model / BYOLLM via Amazon Bedrock or Azure OpenAI, you pay your cloud provider separately for inference).*
* **Q3: "Can a small business try Agentforce without spending thousands upfront?"**
  * **A:** Yes! Any Enterprise Edition+ org can activate **Salesforce Foundations** for **USD 0**, which unlocks Agentforce Builder, Prompt Builder, and starter Data Cloud/Agentforce credits to test a live pilot before committing to Flex Credits or Add-ons.
* **Q4: "Is the old '$2 per conversation' model completely dead?"**
  * **A:** Legacy contracts signed in late 2024 may still run on the USD 2/conversation model until renewal, and some high-complexity service use cases still evaluate it, but **Flex Credits (USD 0.10/action)** and **Unmetered Employee Add-ons (USD 125/user/mo)** are now Salesforce's primary recommended commercial standard.
