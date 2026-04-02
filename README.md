# DataCite DOI Search

Look up dataset metadata and discover journal citations for any DOI registered with DataCite.

**Live tool:** [bvkay.github.io/DataCite_Search](https://bvkay.github.io/DataCite_Search/)

## What it does

- **Browse seismic networks** by institution (AusPass, ANU, UTas, UoA) with network codes pulled live from FDSN
- **Search any DataCite DOI** to retrieve dataset metadata (title, authors, publisher, year, rights)
- **List journal articles** that formally cite the dataset, filtered from all DataCite-registered citations
- **Export results** as CSV or BibTeX

## Why

Citation tracking systems only count references from formal reference lists. This tool lets data providers and researchers quickly check whether a dataset DOI has been cited, and by whom. It supports AuScope's effort to demonstrate the impact of Australian research infrastructure to funders (NCRIS, ARC).

## APIs

| API | Purpose |
|-----|---------|
| [DataCite GraphQL](https://api.datacite.org/graphql) | Dataset metadata and citation graph |
| [FDSN Web Services](https://www.fdsn.org/ws/networks/) | Seismic network registry (codes, DOIs, dates) |
| [AusPass FDSNWS](https://auspass.edu.au/fdsnws/) | AusPass network listings |
| [Crossref](https://api.crossref.org/) | Metadata enrichment for citations with encoding issues |

## Tech

Single static HTML page, no build tools or dependencies. Vanilla JavaScript with `fetch` and `Promise.all`. Hosted via GitHub Pages.