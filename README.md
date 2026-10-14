# PRIDE Lead · Jua Kali SACCO

**Ethical multi-agent loan decisioning for Kenya’s informal sector.**

Live prototype: [https://pride-lead.vercel.app](https://pride-lead.vercel.app)

---

## What it is

PRIDE Lead is a live, interactive prototype that demonstrates how a SACCO can make fair, explainable, and regulation-aligned credit decisions for Jua Kali (informal-sector) traders.

Three specialised agents work in sequence, with a licensed human officer always making the final decision:

| Agent | Role | Responsibility |
|-------|------|----------------|
| **Kiburi** | Credit Scout | Scores the member using alternative data (M-Pesa averages, chama membership, trade type). Produces a transparent risk score and breakdown. |
| **Hekima** | Risk Guardian | Checks SASRA capital adequacy, collateral, and Kenya DPA 2019 consent. Detects gender-proxy bias (GUARD rail) and can pause the workflow (PRIDE Loop). |
| **Uamuzi** | Human Liaison | Generates a clear briefing in Swahili, Dholuo or English and delivers it via Dashboard, WhatsApp or USSD. |
| **Officer** | Final Decision | Licensed loan officer reviews the briefing and chooses Approve / Counter-offer / Decline (with appeal pathway). |

---

## Key design principles

- **Explainability** — Every score shows its components. No black box.
- **Human-in-the-loop** — The system never auto-approves or auto-declines.
- **Bias hard-stop** — Gender-proxy signals are blocked at the payload level (GUARD rail). Ethics Committee is notified.
- **Regulatory pause** — SASRA breaches or missing DPA consent trigger a PRIDE Loop pause. Member is notified via USSD.
- **Local language & low-literacy channels** — Swahili / Dholuo / English + USSD codes for consent withdrawal, explanation and appeal.
- **Data residency** — All data conceptualised as stored in AWS af-south-1 (Cape Town). Kenya DPA 2019 aligned.
- **Full audit trail** — Every run, block and officer decision is logged for SASRA reporting.

---

## How to demo (panel-ready)

1. Open [pride-lead.vercel.app](https://pride-lead.vercel.app)
2. Use the one-click scenario buttons:
   - **Happy path — Approve**
   - **GUARD bias block**
   - **PRIDE Loop pause**
   - **Counter-offer**
   - **Decline + appeal**
3. After the briefing appears, click the officer decision buttons (human-in-the-loop step).

A 3–4 minute script covering all three agents, the GUARD rail and the PRIDE Loop is available in the project materials.

---

## Tech

- Single-page HTML/CSS/JS prototype (no backend required for the demo)
- Deployed on Vercel
- Designed as a Zapier/n8n-style workflow with explicit pause points

---

## Regulatory alignment (Kenya)

- Kenya Data Protection Act, 2019 (consent, purpose limitation, data subject rights)
- SASRA capital adequacy and audit requirements for SACCOs
- Emerging national AI ethics guidance (explainability, human oversight, bias testing)

---

## Repository

```
pride-lead/
├── index.html          # Live prototype (open in browser or deploy to Vercel)
└── README.md
```

---

Built for a panel presentation on ethical AI and financial inclusion in Kenya.
