# Golden Dataset & Reliability Contract

## Golden Dataset Spec
Golden Dataset — Module 4

Test cases:
  1. Edge: N · Judge: both — IN: Raw or Segmented Data:(e.g., ISA*00*...*GS*...) → OUT: Parsed/Structured Response:(e.g., JSON representation of the \(\text{EDI}\) document structure)
  2. Edge: Y · Judge: both — IN: Business Logic Instruction:(e.g., "Convert Odoo Order into an 850 Purchase Order") → OUT: Formatted Outbound EDI String:(e.g., ST*850*0001 with correct data element lengths)
  3. Edge: N · Judge: rule — IN: 810 Invoice:Raw segments: BIG*20240501*INV99*... → OUT: JSON Representation:{ "invoice_no": "INV99", "date": "2024-05-01" }
  4. Edge: N · Judge: rule — IN: 856 ASN:Physical hierarchy: Ship > Order > Item → OUT: Physical hierarchy: Ship > Order > ItemHierarchical Level (HL) Segments:HL*1**S, HL*2*1*O, HL*3*2*I
  5. Edge: N · Judge: both — IN: InputExpected OutputEdge Case?Judge Type810 Invoice:Raw segments: BIG*20240501*INV99*...JSON Representation:{ "invoice_no": "INV99", "date": "2024-05-01" }Multi-tax handling:Multiple TXI segments for state/local taxes.Currency Validator:Check CUR segment against ISO codes IBM 810 Specs.856 ASN:Physical hierarchy: Ship > Order > ItemHierarchical Level (HL) Segments:HL*1**S, HL*2*1*O, HL*3*2*ISplit Shipments:One PO split across multiple boxes with distinct MAN tags.Loop Auditor:Ensures HL parent IDs correctly reference prior IDs Comparatio 856 Guide.214 Status:Event: "Arrived at Warehouse Z" → OUT: Status Code (AT7):AT7*AR*NS***20240510*1645
  6. Edge: Y · Judge: LLM — IN: 997 Acknowledgment:Received invalid 850 PO → OUT: Error Report:AK3*BEG*3**8 (Segment error at position 3)
  7. Edge: N · Judge: both — IN: 315 Status (Ocean): Container "Gate In" event at a port. → OUT: Status Segment: B4***R*20240520*1030*PORTL (Event code 'R' for Arrival).
  8. Edge: N · Judge: LLM — IN: 860 PO Change: Request to cancel 2 lines and add 1 new line. → OUT: POC Segments: POC*1*DI (Delete) and POC*3*AI (Add) with updated totals.
  9. Edge: N · Judge: rule — IN: 820 Payment Order: Payment for 50 invoices with various discounts. → OUT: RMR Segments: Multiple RMR*IV*INV123**450.00 blocks showing net paid amounts.
  10. Edge: N · Judge: LLM — IN: EDI Functional Acknowledgment (997): Reporting a "Mandatory Segment Missing" error. → OUT: Human-Readable Alert: "Error: The mandatory 'BEG' segment is missing at line 4."

Dataset health
- Total: 10
- Edge cases: 2 (20.0%)
- Judge mix: 30% rule / 30% LLM / 40% both

## Confidence UX Design

**Approach:** Tiered confidence with human in the loop

**Confident (>90%):** Claude is highly certain of the EDI Standard, transaction set, segments, and data mappings. Claude auto-executes the file generation and formatting. Publishes directly to the output directory or staging environment.

**Uncertain (50-90%):** Claude understands the base EDI requirements but encounters ambiguities (e.g., custom segment definitions, overlapping code lists, or missing validation references).
Halt-and-Prompt. Claude stages the EDI file and pauses for human review. It explains the ambiguities in the chat interface Claude Code overview.  Requires explicit approve or clarify from the human developer before saving or transmitting.

**Not confident (<50%):** Claude lacks context on the trading partner requirements, struggles to interpret the input data structure, or hits potential schema validation failures. Claude stops, aborts the file generation, and enters Plan Mode Claude Code Best Practices.   Provides a diagnostic breakdown to the developer and requests additional context or documents (e.g., specific Implementation Guides).

**User control surface:** 

Correction/feedback loop is enabled

- Users see AI reasoning / drivers
- Users correct & override outputs
- Corrections feed back into the model / dataset
- Users adjust the confidence threshold _(not yet)_

## Reliability Contract



| Metric | Target | Measurement | Alert Threshold |
|--------|--------|-------------|-----------------|
| Accuracy | | | |
| Hallucination rate | | | |
| Latency (p95) | | | |
| Drift velocity | | | |

## HITL Architecture
<!-- When does a human step in? What's the escalation path? -->

## Red-Team Findings
*What failure mode did your partner find that you missed?*

## Red-Team Findings

My partner ran a **🎯 Confident Hallucination** attack: _(not set)_

**Worst miss they found that I'd missed:** _(not set)_

**Severity:** High

**New gold row I'm adding to close the gap:** _(not set)_
