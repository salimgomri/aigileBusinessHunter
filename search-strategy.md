# SEARCH STRATEGY — WEBSEARCH ONLY
Version: 1.0
Purpose: shared search protocol for Career Hunter and Business Hunter in Claude Cloud.

## 1. ENVIRONMENT RULE

The Claude Cloud environment used by these routines does not provide reliable direct HTTP access to external websites.
WebSearch is the primary available discovery mechanism.

Therefore:
- Never claim to have opened or directly consulted a website unless its content was actually retrieved directly.
- A result returned by WebSearch is an indexed search result, not proof that the current page is accessible.
- A URL listed in a source file is not proof that the source was consulted.
- Never invent missing dates, contacts, emails, job status, company facts or signals.

## 2. SEARCH HIERARCHY

Use searches in this order:

### Level 1 — exact domain targeting
Use:
site:domain "exact phrase"

Examples:
site:eib.org/en/about/careers "Agile"
site:malt.fr "Agile Coach" Luxembourg
site:paperjam.lu "digital transformation" Luxembourg

### Level 2 — targeted combinations
Use combinations of:
- role
- skill
- geography
- business context
- year/current period

Examples:
"Senior Agile Coach" Luxembourg
"SAFe" Luxembourg consultant
"Agile Transformation" Luxembourg
"Transformation Manager" Luxembourg
"Agile Coach" Brussels freelance

### Level 3 — buying / hiring signals
Search for concrete triggers:
- new CIO
- new CTO
- new CPO
- new COO
- agile transformation
- digital transformation
- transformation programme
- transformation program
- operating model
- Target Operating Model
- Agile at Scale
- SAFe
- Scrum
- change programme
- organisational change
- organizational change
- delivery transformation
- PMO transformation
- technology transformation
- recruitment / hiring of transformation leaders

### Level 4 — freshness
Where supported by the search engine, use recent/current wording and current-year terms.
Never manufacture a publication date.

## 3. EVIDENCE LEVELS

For every important result classify evidence:

A — DIRECT CONTENT
The actual page content was retrieved by the available tool.

B — SEARCH-INDEXED
The information is visible in WebSearch results/excerpts and points to the source domain.

C — SECONDARY REPORT
The information is reported by another source.

D — UNSUPPORTED
No usable evidence. Do not use for qualification.

## 4. FRESHNESS

Classify each result:

CONFIRMED RECENT
A recent explicit date is available.

RECENTLY INDEXED
The search result appears recent, but the original publication/update date is not fully confirmed.

DATE UNKNOWN
No reliable date is available.

OLD
The available evidence clearly points to an old publication.

Rules:
- DATE UNKNOWN or OLD cannot be HOT.
- An old job offer cannot be presented as currently open.
- A current search-result timestamp must not be confused with the original publication date.
- When freshness is uncertain, use À VÉRIFIER.

## 5. SEARCH LOG

For each run internally record:
- query
- source/domain targeted
- number of useful results
- evidence level
- freshness
- selected result URL
- reason for rejection where applicable

The final report should summarize search coverage without pretending to be exhaustive.

## 6. NO EXHAUSTIVENESS CLAIM

WebSearch is not an exhaustive database.
Do not write:
- "all available jobs"
- "all freelance missions"
- "complete market scan"

Use:
- "recherche ciblée"
- "résultats identifiés"
- "sources interrogées"
- "opportunités détectées"

## 7. ZERO-SOURCE SAFETY

If no usable WebSearch result is obtained:
- do not fabricate opportunities
- do not reuse examples from prompts
- do not reuse old search results as today's discoveries
- report that no exploitable source was obtained during the run

## 8. CONTACT DATA

Never guess an email address.
Use only a publicly verified professional email found in the current research or an approved connected source.
A person's name found in an article does not automatically mean they are the hiring/business decision maker.

## 9. OUTPUT PRINCIPLE

Every qualified result must be traceable:

FACT → SOURCE → EVIDENCE → ANALYSIS → ACTION

If the FACT cannot be traced to evidence, do not qualify it.
