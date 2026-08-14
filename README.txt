Master Cellular Tower Registry - Editable Home Screen App

This is an installable Progressive Web App (PWA).

NEW:
- Add towers
- Edit towers
- Delete towers
- Duplicate protection by carrier + radio + eNB/gNB
- Local on-device persistence
- Import/export JSON backups
- Registry counts
- LTE eNB/sector math both ways
- 5G /4096 calculation with provisional ? labeling
- PLMN carrier lookup
- Roaming detection
- Signal rating fields
- STRATA unmapped handling

iPhone/iPad:
1. Host the unzipped folder on any HTTPS static host.
2. Open index.html in Safari.
3. Share > Add to Home Screen.
4. Tap Add.

IMPORTANT:
Browser storage can be cleared by the OS/user, so use the Backup tab to export your registry after making changes.

NEW SCREENSHOT SCANNER:
- Upload a cellular screenshot from Photos/Files
- OCR attempts to extract PLMN, Cell ID/NCI, PCI, TAC, band, bandwidth, RSRP, RSRQ and SNR/SINR
- LTE or 5G ID math is calculated from the extracted Cell ID/NCI
- Review/edit OCR results before sending them into Tower Lookup
- OCR requires internet access when its OCR engine is loaded from the CDN

SCAN-BASED IDENTIFICATION UPDATE:
- Scan & Identify now uses the values extracted from the screenshot itself.
- It automatically matches PLMN + derived eNB/gNB against the Master Registry.
- The connection summary appears directly in the Scan tab.
- Open in Lookup remains available only as a secondary manual review path.

SPATIAL OCR v8:
- Scanner now uses OCR word bounding boxes instead of plain text order.
- Labels on the left are paired with values horizontally across from them on the same row.
- Cell ID/NCI, TAC, PCI, band, bandwidth, RSRP, RSRQ and SNR/SINR are extracted from their own rows.
- The app refuses to identify a tower unless PLMN + Cell ID/NCI are present.

PLMN SPATIAL UPDATE v9:
- PLMN is explicitly read from the value directly across from the PLMN label.
- If a screen uses separate MCC and MNC rows, their across-row values are combined into the PLMN.
- Known-registry PLMN text remains a safe fallback.

DIAGNOSTIC LAYOUT v10:
- Optimized for the supplied diagnostic screenshot layout.
- Reads top summary rows including TAC and PLMN.
- Supports spaced PLMN values such as "310 260" and normalizes to "310260".
- Reads "Cell Id" exactly as displayed by the diagnostic UI.
- Reads far-right values for Band, Bandwidth, Cell Id, PCI, RSRP and SNR.
- Detects the 5G section header and applies /4096 provisional gNB/local-cell math.

CELL ID FIX v11:
- More tolerant recognition of "Cell Id" including OCR mistakes such as Cell 1d / Cell ld.
- Constrained fallback searches only immediately after the Cell Id label, never arbitrary numbers.
- 5G detection improved from the 5G section header and n25/n41/n71 bands.
- n41 forces the scanned radio type to 5G in Auto mode.

LINE BAND SCANNER v12:
- Diagnostic fields are grouped by horizontal line band.
- A label and its value are matched only when they occupy the same visual row.
- The value to the right of the label is extracted, even when it is far across the screen.
- Cell Id also has a same-OCR-line fallback.
- Designed around the supplied diagnostic screen with separator lines.

AUTOFILL FIX v13:
- Runs enhanced + original OCR passes and merges the best field values.
- Uses both spatial row extraction and same-line diagnostic parsing.
- Explicitly autofills all Scan result fields after OCR.
- Manual corrections instantly recalculate eNB/gNB/local cell and re-identify the registry match.

SIMPLIFIED AUTO SCAN v15:
- Removed Home Carrier selector from Scan.
- Removed Radio Type selector from Scan.
- Screenshot automatically determines PLMN and LTE/5G.
- Scan & Identify automatically fills/identifies from the picture.
- Lookup is now a simple Cell ID/NCI box.
- Quick Lookup automatically tests LTE /256 and current 5G /4096 registry matches.
- Existing Registry, Add/Edit, Backup, PIN lock, GitHub Pages and PWA support preserved.
