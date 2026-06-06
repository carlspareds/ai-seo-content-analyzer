# AI SEO Content Analyzer

AI-powered SEO analysis tool that scans web pages and generates technical and content recommendations.

## Why this project exists

This project combines SEO experience with applied AI engineering. The goal is to turn a webpage into a structured SEO audit: metadata, headings, links, image alt text, schema/canonical/robots signals, content gaps, search intent, and a prioritized action plan generated with an LLM.

## Planned MVP

- URL input
- Title, meta description, and H1-H3 extraction
- Word count and basic content structure analysis
- Internal and external link extraction
- Image alt text extraction
- Schema, canonical, and robots checks
- LLM-assisted SEO score
- Search intent analysis
- Content gap recommendations
- Prioritized action plan
- Markdown/PDF export
- Sample reports for at least 2 websites

## Target stack

- Backend: Python, FastAPI
- Scraping/parsing: Requests/HTTPX, BeautifulSoup, optional Playwright for JS-rendered pages
- AI: LLM API with structured JSON output
- Frontend: React or simple HTML interface
- Reports: Markdown first, PDF export later

## Architecture draft

```text
User URL
  ↓
Fetcher / Parser
  ↓
SEO Signal Extractor
  ↓
Structured JSON Report
  ↓
LLM Recommendation Layer
  ↓
Markdown/PDF Output
```

## Example output areas

The analyzer should produce:

- Technical SEO findings
- Content structure findings
- Missing or weak metadata
- Heading hierarchy issues
- Internal linking opportunities
- Image accessibility issues
- Search intent mismatch
- Top prioritized recommendations

## Limitations / What I learned

### Limitations

This project is an MVP/proof-of-work, not a full production SEO platform yet.

Current limitations:

- The SEO score is heuristic and LLM-assisted, not based on proprietary ranking data.
- Recommendations depend on the quality of the extracted page content.
- JavaScript-heavy sites may require improved rendering support.
- The tool analyzes individual pages, not full-site crawl depth yet.
- The LLM output can vary, so structured validation and evaluation examples are needed.
- It does not replace professional SEO judgment; it is designed to speed up analysis and prioritization.

### What I learned

While building this project, I am practicing:

- Extracting SEO-relevant page data such as title, meta description, headings, links, images, canonical tags, robots tags, and schema signals.
- Designing structured prompts for LLM-generated SEO recommendations.
- Turning unstructured webpage content into a clear technical/content audit.
- Combining SEO experience with applied AI engineering.
- Thinking about reliability issues such as hallucinations, inconsistent outputs, blocked pages, and edge cases.
- Communicating limitations honestly instead of presenting the project as a finished commercial product.

### Next improvements

- Add JavaScript rendering for dynamic pages.
- Add batch site crawling.
- Add before/after comparison reports.
- Add evaluation examples to test consistency of LLM recommendations.
- Add export to PDF.
- Add deployed demo and sample reports.

## Roadmap

1. Build page fetcher and parser.
2. Extract SEO signals into structured JSON.
3. Add LLM recommendation generation.
4. Generate Markdown report.
5. Add sample reports.
6. Add screenshots and demo.
7. Deploy a public demo.

## Status

In progress.
