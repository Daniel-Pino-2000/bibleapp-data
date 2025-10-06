# BibleApp Data Repository

This repository hosts prebuilt Bible databases (`.db` files) for use in the **BibleApp** Android application.  
It allows the app to download multiple Bible versions in different languages and display them to the user.

---

## **Description**

The repository contains:

- Multiple Bible versions in SQLite database format (`.db`).
- A metadata JSON file (`bible_versions.json`) listing all available versions, including:
  - Internal version ID (`versionId`)
  - Display name (`name`)
  - Language code (`language`)
  - Direct download URL (`url`)

The databases are structured to be **compatible with the BibleApp**, using a standardized schema:

**Table `words`**
| Column   | Type    | Description                  |
|----------|---------|------------------------------|
| wordId   | INTEGER | Unique ID for each word      |
| word     | TEXT    | The text of the word         |
| bookNum  | INTEGER | Book number (e.g., Genesis=1) |
| chNum    | INTEGER | Chapter number               |
| verseNum | INTEGER | Verse number                 |

All database versions follow this schema to allow **consistent querying** and **search functionality** in the app.

---

## **Folder Structure**
bibleapp-data/
│
├─ bible_versions.json      <- metadata file describing available versions
└─ versions/
   ├─ en/
   │  ├─ kjv.db
   │  └─ esv.db
   ├─ es/
   │  ├─ rvr1960.db
   │  └─ nvi.db
   └─ fr/
      └─ lsg.db

