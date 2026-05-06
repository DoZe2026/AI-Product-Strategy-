# Cost Curve & Pricing Strategy

Leader: Copilot/ClodeCode embedded into EDI format creation
Filler: EDI format templates ready to reuse
Killer: deep, terminal-native integration coupled with agentic hooks, which allows it to act as an autonomous, customized partner directly in your development environment rather than just a chatbot

## Cost Model

| Cost Category | Per-User/Month | Notes |
|--------------|----------------|-------|
| Inference (primary model) |$5.00 – $15.00 |High-end model (e.g., GPT-5/Claude Code) using ~1M–3M tokens/mo for complex tasks. |
| Inference (cascading/triage) |$1.00 – $3.00 |Smaller, faster models (e.g., GPT-5-mini) for routing, filtering, or quick classification. |
| Infrastructure |$2.00 – $5.00 |GPU hosting, vector database (RAG), vector similarity search, monitoring, and API gateway overhead. |
| Data/storage |$0.50 – $2.00 | Embedding storage, vector index updates, log storage (GDPR/EU AI Act auditing).|
| Human-in-the-loop |$0.50 – $1.50 |Quality assurance, RLHF labeling, or compliance review for high-stakes AI outputs. |
| **Total AI COGS** |$9.00 – $26.50 |Expected range for active users. Rises to 60%+ of revenue if usage is not capped. |

## Cascading Strategy
<!-- Cheap model → frontier model routing logic -->

**Triage model:** Specialized Small Language Model
**Frontier model:** Clode Code 
**Routing rule:**  Example Rule: "If user_type == 'developer' and format_complexity == 'high', route directly to Frontier Model, otherwise route to Triage Model"
**Expected cascade ratio:**  Vast majority of simple queries (approx. 70–90%) to be kept within the smaller, specialized and cost-effective models.

## Pricing Model

**Current pricing:** $5.00 - $15.00
**Proposed AI pricing:** $9.00 – $26.50
**Model:** hybrid

Pricing Strategy Block — Module 3

Pricing Strategy
- Strategy posture: Maximize
- Pricing model: Hybrid (base + usage)
- Unit of work metered: new EDI formats created 
- Base fee ($/month): $15.00
- Price per unit: $0.50
- Estimated units/user/month: 10
- Implied revenue/user/month: $20.00



## Stress Tests

| Scenario | Impact on Margin | Response |
|----------|-----------------|----------|
| Inference costs 3x | | |
| Heaviest segment doubles | | |
| Model provider raises prices 50% | | |

## Board One-Pager
<!-- Before/After: Old SaaS revenue vs. AI usage revenue for your product -->

**Before (traditional SaaS):**
**After (AI-enabled):**
**Net margin shift:**


Before (traditional SaaS):
- Current pricing: $5.00 - $15.00
- Current gross margin:75–90%


After (AI-enabled): 
- Proposed pricing: $20.00
- AI COGS per user/month:$9.00 – $26.50
- Expected gross margin:50–60%


Net margin shift:
- Margin moves from 75–90% % to 50–60%.
- Explain why the margin changes: The Data IntegrationPlatform as is an already built software, the cost to serve an additional user is negligible. Making it AI-powered at the early stage generates high variable costs, known as inference costs, etc. 


Why this is still a good business:
The shift is not entirely negative. While gross margin decreases, empowering Data Integration Platform with AI can help us achieve higher Average Revenue per Account (ARPA) because we could charge for replacing high-cost human labour needed to created new EDI formats. With optimized infrastructure over time (model routing, caching), we can expect to stabilize at around 60–65% gross margin.

Board-ready narrative:

" CFO, we are currently spending too much time creating EDI formats manually from scratch for every bespoke integration instead of leveraging on AI-powered code generating solutions. By enriching our data integration platform with AI, we can transform our manual and time consuming process of new formats creation into a real-time 'integration factory'.This isn’t about just 'doing AI'; it’s about tangible ROI.Speed: We can cut our integration time to market by up to 40%. Accuracy: AI will automate new EDI formats creation, reducing human error and development lifecycle.Strategic Impact: Instead of being reactive scorekeepers, we move to proactive engineering, allowing us to gain a competitive advantage in contract negotiations this customer and partners awaiting systems to be integrated. By investing here, we turn our fragmented integration ecosystem  into a trusted, strategic asset that drives efficiency and competitive advantage."
