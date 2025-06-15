# 🚀 Zero-Cost AI-Driven Lead Qualification Pipeline

A fully automated, no-code lead qualification pipeline built with **free tools** for early-stage startups.  
Specifically designed to qualify **B2B hydrogen industry vendors** and pass only the best-fit leads to a sales CRM.

🔗 [Live Portfolio](https://jerryn-joy.github.io)  
📂 [Workflow Diagram](https://miro.com/app/board/uXjVIqjpoh4=/?share_link_id=861433035153)

---

## 📌 What This Project Does

- Captures leads from multiple sources (form, chatbot, business cards, social)
- Scores them using a pre-trained AI model (`facebook/bart-mini`) for **intent**
- Filters for only **hydrogen-related vendors**
- Sends hot leads to **HubSpot** for sales follow-up
- Built 100% with **no-code tools** and **free-tier services**

---

## 🛠️ Tools Used (All Free Tiers)

| Tool            | Purpose                                 |
|------------------|-----------------------------------------|
| **Airtable**     | Central database (CRM for leads)        |
| **Fillout / Tally.so** | Website lead capture forms        |
| **Voiceflow**    | Chatbot that collects data + context    |
| **BizConnect**   | Business card scanner for trade fairs   |
| **HubSpot (Free)** | CRM for sales follow-up               |
| **Make.com**     | Automation between Airtable ↔ HubSpot   |
| **BART-mini**    | Open-source model used for NLP scoring  |

---

## 🧩 End-to-End Flow

1. **Lead Collection**
    - Website form via Fillout or Tally
    - Voiceflow chatbot on homepage
    - BizConnect for event leads
    - Contact form or social outreach

2. **Storage in Airtable**
    - Leads land in a "Raw Leads" table
    - Metadata captured (source, message, company name, etc.)

3. **AI Scoring + Filtering**
    - Pre-trained model (facebook/bart-mini) classifies message intent
    - Firmographic filtering (e.g., hydrogen, electrolyzer, fuel cell)
    - Leads tagged and routed to “Qualified Vendors” view

4. **HubSpot Integration (via Make)**
    - Only hot leads are sent to HubSpot
    - Auto-assign to sales rep
    - Follow-up stages handled inside HubSpot

5. **Outcome Logging**
    - Closed-Won or Lost feedback pushed back to Airtable for review
    - Optionally re-nurture cold leads via MailerLite

---

## 🎯 Why This Is Valuable

| Feature                | Benefit                          |
|------------------------|----------------------------------|
| No-code                | Easy to set up & maintain        |
| Free tools only        | Zero cost to build and run       |
| Industry-specific      | Tailored for hydrogen vendors    |
| Scalable               | Can add LinkedIn/website enrichments later |
| Recruiter-ready        | Professional architecture        |

---

## 🔄 Airtable Views

| View Name         | Purpose                            |
|-------------------|-------------------------------------|
| Raw Leads         | All unprocessed leads               |
| Qualified Vendors | AI-scored and hydrogen-validated    |
| Cold Leads        | No response, for re-nurturing       |
| Closed Deals      | Deal stage synced from HubSpot      |

---

## 📂 Repository Contents

```text
├── assets/
│   ├── lead_workflow_diagram.png     # Visual overview of system
│   ├── screenshot_airtable.png       # (optional) example of Airtable view
│   └── resume.pdf                    # (optional) if you're showcasing this repo
├── docs/
│   └── project_info.md               # Walkthrough of system usage
├── README.md                         # You're reading this!
└── LICENSE                           # Open license (MIT recommended)

```
---

## 📝 Bonus File: `docs/project_info.md`

```markdown
# 🔧 How to Replicate This Project (No Code)

## 🧠 What You Need

- Airtable account
- Make.com account
- HubSpot Free CRM
- Tally.so or Fillout.com (for lead forms)
- Voiceflow (for chatbot)
- BizConnect (optional for events)

## 🪜 Setup Steps

1. Create Airtable base with tables:
    - Raw Leads
    - Qualified Vendors
    - Cold Leads
    - Closed Deals

2. Set up a form in Fillout or Tally → connect to Airtable

3. Deploy chatbot in Voiceflow → connect webhook to Airtable

4. Use Make.com:
    - Scenario 1: Airtable → HubSpot (new lead in Qualified View)
    - Scenario 2: HubSpot → Airtable (update lead status)

5. Use pre-trained BART model on collected messages for intent score (optional if running manually or via external script)

```

---

## 🔄 Data Flow Diagram

📥 Lead Capture → Airtable → AI Scoring → Qualified Leads → HubSpot → Sales → Outcome Sync → Airtable


