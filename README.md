# Pustaka Terbuka — MYTO (Malaysian Theses Online (PNM / PERPUN))

> **Pustaka Terbuka: Katalog Induk Terbuka untuk Perpustakaan dan Sekolah Malaysia.**  
> *Official Malaysian Theses Online (PNM / PERPUN) (MYTO) Bibliographic Dataset & Standalone Harvester.*

This repository contains the harvested open MARCXML collection and harvester pipeline for **Malaysian Theses Online (PNM / PERPUN)** (`MYTO`), contributing to the national Malaysian union catalog at [pustaka-terbuka/opac](https://github.com/pustaka-terbuka/opac).

---

## Institutional Metadata

| Attribute | Value |
| :--- | :--- |
| **Institution Code** | `myto` |
| **Agency Code** | `MYTO` |
| **Official Name** | Malaysian Theses Online (PNM / PERPUN) |
| **Institution Type** | `special` |
| **State / Territory** | Kuala Lumpur |
| **Target End Bib** | 300,000 |
| **OPAC Base URL** | [https://myto.pnm.gov.my/](https://myto.pnm.gov.my/) |
| **Subject Focus** | Malaysian doctoral dissertations and master theses across all Malaysian universities |

---

## Directory Structure

```text
myto/
├── README.md                      # Institutional repository documentation
├── package.json                   # Node.js project specification & scripts
├── harvest/
│   └── inbox/myto/             # Sealed MARCXML batch chunks and manifests
│       └── <run-id>-chunk-001/
│           ├── manifest.json      # Chunk SHA-256 manifest & metadata
│           ├── provenance.jsonl   # Record-level attribution and fetch logs
│           └── records/           # Batched MARC21 slim XML files
├── tools/
│   ├── harvesters/myto/        # Automated OPAC crawler & XML converter
│   └── lib/                       # Supporting MARCXML and validation utilities
└── tests/
    └── harvester-myto.test.js  # Autonomous test suite
```

---

## Usage

```bash
# Install dependencies
npm install

# Test run harvester (10 sample records)
npm run harvest:sample

# Run full collection sweep
npm run harvest:full

# Validate dataset integrity
npm run validate-inbox harvest/inbox/myto/<chunk-directory>
```

---

## Attribution & License

Dataset harvested and preserved under open library metadata standards for educational, civic, and cooperative indexing. Attribution: **Malaysian Theses Online (PNM / PERPUN) (MYTO)** & **Pustaka Terbuka**.
