# Problem Thesis Research Prompts

**Project:** CyberShield Rural
**Date Generated:** 2026-01-28
**Capital Thesis Reference:** phases/01-capital/thesis.md

## Context

CyberShield Rural targets **rural hospital cybersecurity** — specifically critical access hospitals and small rural hospitals (under 100 beds) in the United States. The capital thesis identified 12 viable funding paths anchored by the CMS Rural Health Transformation Program ($200M to South Carolina with explicit cybersecurity language) and SCRA/SC Launch Inc. (which invested $250K in a cybersecurity startup in 2025).

The problem hypothesis: **Rural hospitals face cybersecurity threats they cannot adequately defend against due to resource constraints (no dedicated security staff, limited budgets, legacy systems), and no dedicated solution exists for this segment.** This research validates whether that problem is real, documented, and severe enough to build a venture around.

Key constraints from the capital thesis:
- The Change Healthcare breach (192.7M individuals affected, $1.98B+ costs) has elevated cybersecurity to board-level concern
- No VC-backed startup dedicated to rural hospital cybersecurity was identified
- Corporate philanthropic programs (Microsoft: 550+ hospitals; Google: pilots) are the primary current response
- HIPAA Security Rule update proposed with $9B estimated first-year compliance cost
- Healthcare cybersecurity market projected to reach $75-127B by 2032-2034

## Prompts

### Prompt 1: Problem Prevalence and Severity

I am building a problem thesis for a venture addressing **cybersecurity vulnerability in rural hospitals** in the **US healthcare sector**. This research will establish whether the problem is large enough and painful enough to build a business around. The findings will be used in investor materials, so every claim must be defensible.

Research the prevalence and severity of cybersecurity vulnerability in rural hospitals in the United States.

First, establish the scale of the problem:
- How many rural hospitals exist in the US (total count, critical access hospitals vs. other rural designations)
- What percentage have experienced a cyberattack or data breach (absolute numbers and percentages)
- What percentage have no dedicated cybersecurity staff or CISO
- What percentage are running legacy/end-of-life systems
- Geographic distribution (national spread, concentration in certain states — note South Carolina specifically if data exists)
- Segment breakdown by size (under 25 beds, 25-50 beds, 50-100 beds)

Then, quantify the severity:
- Average cost per breach or ransomware incident for rural/small hospitals
- Operational impact (system downtime duration, diversion to other facilities, return to paper processes)
- Patient outcome impact (delayed care, mortality data if available, patient safety incidents during cyber events)
- Frequency of attacks targeting healthcare (daily/weekly/annual rates, trend direction)
- Comparison to urban/large hospital cybersecurity posture (staffing, spending, incident rates)

Finally, establish the trajectory:
- Is the problem getting worse, stable, or improving? Over what timeframe?
- What forces are driving the trend (ransomware-as-a-service, IoT medical devices, workforce shortage)?
- Are rural hospitals closing at higher rates partly due to financial impact of cyber events?
- Projections from credible sources (analyst reports, government data)

Scope:
- United States focus
- Data from 2023 through 2026
- Prioritize government sources (HHS, GAO, CMS, CISA, FBI IC3), peer-reviewed research, and industry associations (AHA, CHIME, HISAC) over vendor-sponsored studies
- Include the Change Healthcare breach (2024) impact on rural hospitals specifically if documented

If statistics conflict across sources, present both figures and note the discrepancy. Do not average or reconcile conflicting data — flag it for human review.

For every claim, provide a citation in this format:
- **Source:** [Publication or organization name]
- **Date:** [Publication date or "Accessed YYYY-MM"]
- **URL:** [Direct link to the source]
- **Relevance:** [One sentence on why this source matters]

If a data point cannot be verified with a credible source, state "Unverified — requires confirmation" rather than omitting it or presenting it as fact.

Example of a well-documented statistic:
---
**Rural hospital cybersecurity staffing:**
- 67% of rural hospitals have no dedicated cybersecurity staff
- Source: American Hospital Association Rural Health Survey, March 2024
- URL: [direct link]
- Relevance: Establishes the resource gap that makes rural hospitals uniquely vulnerable
---

---

### Prompt 2: Customer Voice and Pain Points

I need to understand how **rural hospital IT administrators, CISOs (where they exist), hospital CEOs, and compliance officers** experience and describe **cybersecurity challenges** in their own words. This research will inform our messaging, product design, and investor narrative. Authentic customer language is more convincing than statistics alone.

Search these sources for firsthand accounts:
- Industry forums: CHIME (College of Healthcare Information Management Executives), HIMSS community boards
- Product reviews on G2, Capterra, or TrustRadius for healthcare cybersecurity tools (filter for small/rural hospital reviewers)
- Reddit discussions in r/healthIT, r/sysadmin, r/cybersecurity, r/netsec, r/ruralhealth
- Support forums and help desk discussions related to healthcare IT security
- LinkedIn posts and articles from rural hospital IT directors, CIOs, and compliance officers
- Twitter/X threads from healthcare cybersecurity professionals discussing rural challenges
- Conference presentations from HIMSS, CHIME, AHA Rural Health Conference, National Rural Health Association events
- Public testimony to Congress or HHS about rural hospital cybersecurity challenges
- News interviews with rural hospital administrators following cyber incidents

For each source, capture:
1. Direct quotes (exact language, not paraphrased)
2. The context (what prompted the comment, what role the person holds, hospital size/type)
3. The emotional register (frustration, resignation, urgency, fear, helplessness)
4. Any workarounds or coping mechanisms described
5. What they wish existed or what they've asked for

Then, synthesize patterns:
- Most common complaints (ranked by frequency across sources)
- Language patterns (what words and phrases recur — "we're a sitting duck," "it's not if but when," etc.)
- Unmet needs that multiple people express independently
- Differences in pain by segment (critical access vs. larger rural, with-IT-staff vs. without)
- The "do nothing" voice — what do administrators say when asked why they haven't addressed cybersecurity?

Scope:
- Posts, reviews, and statements from 2023 through 2026
- Focus on rural hospital staff specifically, not large health system IT teams
- Minimum 10 distinct voices from at least 3 different source types
- Include any firsthand accounts of the Change Healthcare breach impact on rural hospitals

If you cannot find sufficient firsthand accounts (fewer than 5 distinct voices), state this explicitly. A thin customer voice finding is more useful than padded results.

For every claim, provide a citation in this format:
- **Source:** [Publication or organization name]
- **Date:** [Publication date or "Accessed YYYY-MM"]
- **URL:** [Direct link to the source]
- **Relevance:** [One sentence on why this source matters]

If a data point cannot be verified with a credible source, state "Unverified — requires confirmation" rather than omitting it or presenting it as fact.

For quotes, use this format:
---
**Source:** Reddit r/healthIT, user [anonymized role description]
**Date:** September 2024
**Quote:** "We got hit with ransomware last year and had to go back to paper for three weeks. We're a 40-bed hospital — we don't have an IT security team. It's just me and I also do the phones."
**Context:** Thread about hospital cybersecurity challenges
**Emotional register:** Resignation, overwhelm
**Workaround mentioned:** Manual/paper fallback processes
---

---

### Prompt 3: Current Solutions and Their Shortcomings

I need to understand what **rural hospitals** currently use to address **cybersecurity**, and where those solutions fall short. This research will define our competitive positioning and validate that a gap exists for our solution. The capital thesis identified that no VC-backed startup is dedicated to rural hospital cybersecurity — this research should validate whether that gap extends to available solutions.

Research current approaches in this order:

1. First, map the solution landscape:
   - Commercial cybersecurity products marketed to healthcare (CrowdStrike, Palo Alto, Fortinet, Claroty/Medigate, Cynerio, Armis — note which ones target or are accessible to small/rural hospitals)
   - Managed security service providers (MSSPs) serving healthcare (CyberMaxx, Fortified Health Security, Clearwater, Nordic Consulting)
   - Government programs providing cybersecurity assistance to hospitals (CISA services, HHS 405(d), state-level programs)
   - Corporate philanthropic programs (Microsoft Cybersecurity Program for Rural Hospitals — 550+ enrolled; Google pilot programs)
   - Manual processes and workarounds commonly used by rural hospitals
   - "Do nothing" prevalence — what percentage of rural hospitals have no formal cybersecurity program?

2. Then, for each major solution category, document:
   - Key vendors/providers and their market position
   - Pricing model and typical cost (annual contract value where available)
   - What it covers and what it doesn't
   - Target customer profile (designed for enterprise vs. SMB vs. rural)
   - Known limitations based on reviews, case studies, or analyst reports
   - Staffing requirements to operate the solution (does it require a dedicated security team?)

3. Finally, identify the gaps:
   - What makes enterprise cybersecurity solutions impractical for rural hospitals (cost, complexity, staffing requirements)?
   - Common complaints about existing solutions from small hospital users
   - What Microsoft's philanthropic program covers and what it doesn't (is it a complete solution or a stopgap?)
   - Features or capabilities missing for the rural context specifically
   - Barriers to adoption (cost, complexity, staffing, integration with legacy systems, bandwidth limitations)

Scope:
- Focus on solutions accessible to hospitals under 100 beds with 0-1 IT security staff
- Include both technology solutions and service-based approaches
- Current market (products available now, not announced/upcoming)
- United States market

Distinguish between "no solution exists" and "solutions exist but aren't adopted." These are different problems requiring different responses. If adoption data is available, include it.

For every claim, provide a citation in this format:
- **Source:** [Publication or organization name]
- **Date:** [Publication date or "Accessed YYYY-MM"]
- **URL:** [Direct link to the source]
- **Relevance:** [One sentence on why this source matters]

If a data point cannot be verified with a credible source, state "Unverified — requires confirmation" rather than omitting it or presenting it as fact.

---

### Prompt 4: Cost of the Status Quo

I need to quantify what **inadequate cybersecurity** costs **rural hospitals** today, both in direct expenses and hidden costs. This research provides the economic justification for our venture — if we can't show the cost of the problem exceeds the cost of a solution, the business case fails.

Research costs in this order:

1. First, document direct financial costs:
   - Average cost per data breach for healthcare organizations (and specifically for small/rural hospitals if segmented data exists)
   - Average ransomware payment demanded from and paid by hospitals
   - Average system downtime cost per day for a rural hospital
   - Annual spending on current (inadequate) cybersecurity measures by small hospitals
   - Insurance premium impacts — cyber insurance cost trends for healthcare, denial rates, coverage gaps
   - HIPAA penalty amounts imposed on small/rural hospitals (OCR enforcement data)
   - Cost of breach notification, credit monitoring, legal fees

2. Then, quantify indirect costs:
   - Staff time spent on manual workarounds during and after incidents
   - Patient diversion costs (ambulance rerouting, lost revenue during downtime)
   - Opportunity costs (what can't be done while dealing with a cyber event — delayed care, cancelled procedures)
   - Reputational damage in small communities (quantified where possible — patient volume changes post-breach)
   - Impact on hospital financial viability (are breaches contributing to rural hospital closures?)
   - Staff burnout and turnover attributable to cybersecurity burden on non-security IT staff

3. Finally, aggregate to market level:
   - Total estimated annual cybersecurity cost across all rural hospitals (build from per-hospital to market)
   - Cost trajectory (growing, stable, declining) with projection
   - Industry benchmarks: what do adequately-secured hospitals spend vs. what rural hospitals spend?
   - The "gap cost" — difference between current spend and adequate spend per rural hospital

Scope:
- United States market
- Focus on rural hospitals (critical access and under 100 beds) specifically, not the broader healthcare market
- Use the most recent data available; flag anything older than 3 years
- Include the Change Healthcare breach as a case study for downstream costs to rural hospitals (were rural hospitals disproportionately affected?)

Where exact figures aren't available, provide ranges and explain the methodology. For example: "Based on [X rural hospitals] × [average cost per incident] × [incident rate], the estimated annual cost is $Y-Z." Show your work so it can be validated.

For every claim, provide a citation in this format:
- **Source:** [Publication or organization name]
- **Date:** [Publication date or "Accessed YYYY-MM"]
- **URL:** [Direct link to the source]
- **Relevance:** [One sentence on why this source matters]

If a data point cannot be verified with a credible source, state "Unverified — requires confirmation" rather than omitting it or presenting it as fact.

---

### Prompt 5: Regulatory and Compliance Context

I need to understand the regulatory environment surrounding **cybersecurity in healthcare** with specific attention to how regulations impact **rural hospitals**. Regulatory pressure is often a key buying trigger — organizations buy compliance solutions when penalties become real. This research will determine if regulation is a tailwind for our venture.

Research in this order:

1. First, identify the regulatory framework:
   - **HIPAA Security Rule** — current requirements and the proposed January 2025 update (estimated $9B first-year compliance cost per AHA). What specifically changes for small hospitals?
   - **HITECH Act** — enforcement provisions relevant to cybersecurity
   - **CMS Conditions of Participation** — are cybersecurity requirements being added as conditions for Medicare reimbursement?
   - **State-level regulations** — Focus on South Carolina first, then states with strictest healthcare cybersecurity requirements. Does SC have any state-specific healthcare cybersecurity mandates?
   - **CISA CPGs (Cybersecurity Performance Goals)** — voluntary but increasingly referenced. Are they becoming de facto requirements?
   - **Upcoming or proposed regulations** — HHS cybersecurity mandates in the pipeline, any proposed legislation
   - **NIST Cybersecurity Framework** — healthcare sector guidance, voluntary vs. mandated adoption

2. Then, document enforcement activity:
   - Recent HIPAA enforcement actions related to cybersecurity failures (last 3 years)
   - Penalty amounts imposed — any against small or rural hospitals specifically?
   - Trends in enforcement (is OCR increasing cybersecurity-specific actions?)
   - High-profile cases that changed industry behavior
   - Have any hospitals lost Medicare certification or reimbursement due to cybersecurity failures?

3. Finally, assess the compliance landscape:
   - Current HIPAA Security Rule compliance rates among rural hospitals (if data exists)
   - Common compliance gaps specific to small/rural hospitals
   - Cost of achieving compliance with proposed HIPAA update for a rural hospital
   - Cost of non-compliance (penalties + breach costs + reputational)
   - Whether compliance requirements are expected to tighten — what's the regulatory trajectory?
   - Do rural hospitals get any exemptions, extended timelines, or size-based accommodations?

Scope:
- US federal regulations and South Carolina state regulations
- Current enforcement environment (2023 through 2026)
- Focus on regulations that specifically affect rural and critical access hospitals
- Include any provisions in the CMS Rural Health Transformation Program that relate to cybersecurity compliance requirements

If enforcement data is not publicly available for rural hospitals specifically, note this gap. General enforcement trends are useful but should be labeled as such, not presented as segment-specific data.

For every claim, provide a citation in this format:
- **Source:** [Publication or organization name]
- **Date:** [Publication date or "Accessed YYYY-MM"]
- **URL:** [Direct link to the source]
- **Relevance:** [One sentence on why this source matters]

If a data point cannot be verified with a credible source, state "Unverified — requires confirmation" rather than omitting it or presenting it as fact.

## Instructions for Research

1. Run each prompt in Claude Deep Research
2. Save each research result as a separate file in `research/02-problem/`
3. Name files: `01-prevalence.md`, `02-customer-voice.md`, `03-current-solutions.md`, `04-cost.md`, `05-regulatory.md`
4. Once all research is complete, notify for processing
