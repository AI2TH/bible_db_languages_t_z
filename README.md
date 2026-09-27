# AI2TH Bible Database — Languages T to Z

[![License: CC0-1.0](https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg)](http://creativecommons.org/publicdomain/zero/1.0/)
[![Repository Status](https://img.shields.io/badge/Status-Active-brightgreen.svg)]()
[![Target Languages](https://img.shields.io/badge/Languages-~970%20languages-blue.svg)]()

This repository is part of the **AI2TH Global Scripture Multi-Repository Network**, hosting pre-compiled, optimized SQLite (`.db`) databases for all **4,170 language portions** and **800+ complete language Bibles** worldwide.

---

## 📖 Scope
* **Language Alphabetical Range**: **T – Z**
* **Language Portions & Complete Bibles**: **~970 languages**
* **Sample Key Languages**:
  - Tagalog (tgl)
  - Tamil (tam)
  - Telugu (tel)
  - Thai (tha)
  - Turkish (tur)
  - Ukrainian (ukr)
  - Urdu (urd)
  - Vietnamese (vie)
  - Welsh (cym)
  - Yoruba (yor)
  - Zulu (zul)

---

## ⚡ Direct Download & CDN Endpoints

All databases are pre-indexed and formatted for instant SQLite `ATTACH DATABASE` consumption.

### Primary Raw GitHub Endpoint:
```text
https://raw.githubusercontent.com/AI2TH/bible_db_languages_t_z/main/{language_or_version_code}.db
```

### Global jsDelivr High-Speed CDN Mirror:
```text
https://cdn.jsdelivr.net/gh/AI2TH/bible_db_languages_t_z@main/{language_or_version_code}.db
```

---

## 🗄️ Standard SQLite Schema

Every database in this repository follows the strict, lightning-fast Miktam Bible SQLite schema:

```sql
CREATE TABLE books (
    book_number     INTEGER PRIMARY KEY,
    name            TEXT NOT NULL,
    abbreviation    TEXT NOT NULL,
    testament       TEXT NOT NULL CHECK(testament IN ('OT', 'NT')),
    total_chapters  INTEGER NOT NULL
);

CREATE TABLE verses (
    id              INTEGER PRIMARY KEY AUTOINCREMENT,
    book_number     INTEGER NOT NULL,
    chapter         INTEGER NOT NULL,
    verse_number    INTEGER NOT NULL,
    text            TEXT NOT NULL,
    UNIQUE(book_number, chapter, verse_number)
);
```

---

## 🌐 Complete AI2TH Scripture Network

| Repository | Scope | Description |
| :--- | :--- | :--- |
| [AI2TH/bible_db](https://github.com/AI2TH/bible_db) | 140 Major Translations | Primary popular world Bibles (KJV, ASV, BBE, Darby, Vulgate, Luther, etc.) |
| [AI2TH/bible_db_languages_a_f](https://github.com/AI2TH/bible_db_languages_a_f) | Languages A – F | Portions and complete Bibles for ~1,100 languages |
| [AI2TH/bible_db_languages_g_m](https://github.com/AI2TH/bible_db_languages_g_m) | Languages G – M | Portions and complete Bibles for ~1,000 languages |
| [AI2TH/bible_db_languages_n_s](https://github.com/AI2TH/bible_db_languages_n_s) | Languages N – S | Portions and complete Bibles for ~1,100 languages |
| [AI2TH/bible_db_languages_t_z](https://github.com/AI2TH/bible_db_languages_t_z) | Languages T – Z | Portions and complete Bibles for ~970 languages |

---
*Maintained by AI2TH for the [Miktam Bible](https://github.com/AI2TH/miktam_bible) mobile application.*
