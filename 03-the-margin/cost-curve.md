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

**Current pricing:** 
**Proposed AI pricing:**
**Model:** seat-based 

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
