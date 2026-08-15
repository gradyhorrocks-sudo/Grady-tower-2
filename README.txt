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

FIXED PIN v16:
- App PIN is fixed to 159357.
- Each new browser/app session requires the PIN.
- Removed PIN creation/change workflow.
- Existing registry, Scan, quick Cell ID/NCI Lookup, Registry, Add/Edit, Backup,
  GitHub Pages, Safari Home Screen/PWA support remain preserved.
- Important: this is app-level protection, not server-side protection of public GitHub Pages files.

UNIVERSAL SEARCH + CARRIERS v17:
- Lookup searches Cell ID/NCI, LTE eNB, 5G gNB, carrier name, tower/site name, PLMN, and band.
- Searching by carrier returns all towers for that carrier.
- Optional LTE/5G and carrier filters.
- Numeric searches also perform LTE /256 and current 5G /4096 identifier math.
- Add/Edit now accepts any future carrier name instead of a fixed carrier dropdown.
- Entering a new carrier + PLMN adds that carrier mapping to the local registry.
- Existing Scan, Registry, Add/Edit, Backup, fixed PIN, GitHub Pages and PWA support preserved.

TOWER MAP v18:
- Added a Map tab using OpenStreetMap.
- Tower records can store latitude and longitude.
- Add/Edit supports manual coordinates, current-device location, or tapping the map.
- Saved tower locations appear as map pins with carrier/radio/ID details.
- Existing towers without coordinates remain valid and can be mapped later.
- Existing Scan, universal Lookup, future-carrier support, Registry, Add/Edit, Backup,
  fixed PIN 159357, GitHub Pages, and Safari Home Screen/PWA support preserved.

ID AUTOFILL v19:
- In Add/Edit, typing an existing eNB/gNB automatically finds the matching registry record.
- Autofills carrier, PLMN, LTE/5G, site name, status, bands, bandwidth, saved Cell ID/NCI,
  sector/local cell, PCI, TAC, coordinates, and notes.
- Automatically switches the form into Edit mode for the matched record.
- If more than one record shares the same numeric ID, current carrier/radio is preferred.
- Existing Scan, universal Lookup, Map, future-carrier support, Backup, fixed PIN 159357,
  GitHub Pages and Safari Home Screen/PWA support preserved.

UNKNOWN TOWER ADD FLOW v20:
- If Scan & Identify derives an eNB/gNB that is not in the registry, an Add This Tower button appears.
- Add/Edit opens with all scanned values prefilled: PLMN/carrier when known, radio, eNB/gNB,
  Cell ID/NCI, sector/local cell, band, bandwidth, PCI, TAC, and scan signal notes.
- Site name remains blank so the user confirms the real tower name instead of the app inventing one.
- Unknown numeric Lookup results also offer Add as LTE Tower / Add as 5G Tower.
- Existing Scan, universal Lookup, Registry, Map, ID autofill, future-carrier support,
  Backup, fixed PIN 159357, GitHub Pages and Safari Home Screen/PWA support preserved.

SATELLITE MAP v21:
- Map tab now has Street Map and Satellite basemap options.
- Satellite layer uses Esri World Imagery.
- Saved tower pins, map picking, current location, and coordinate editing remain available.
- Existing Scan, universal Lookup, Registry, Add/Edit, unknown-tower add flow, future-carrier support,
  Backup, fixed PIN 159357, GitHub Pages and Safari Home Screen/PWA support preserved.

LOCATION GLOBE v22:
- Registry records with saved latitude/longitude now display a globe symbol (🌐).
- Records without coordinates do not show the globe.
- Globe indicates that the tower has a saved map location.
- Existing satellite/street map, Scan, Lookup, Add/Edit, ID autofill, unknown-tower flow,
  Backup, PIN 159357, GitHub Pages and PWA support preserved.

QUICK MAP LOCATION UPDATE v23:
- Map tab now includes an Update Tower Location panel.
- Enter an eNB/gNB and paste decimal coordinates to update that tower's saved location.
- Example accepted format: 40.455500, -109.528700.
- The registry globe indicator and map pin update immediately.
- If the numeric ID matches multiple records, the app refuses to silently update all of them.
- Existing satellite/street map, Scan, Lookup, Registry, Add/Edit, ID autofill,
  unknown-tower flow, Backup, PIN 159357, GitHub Pages and PWA support preserved.

DRAGGABLE MAP EDIT v24:
- Map tab includes Place / Drag Tower.
- Enter an eNB/gNB and select the matching tower.
- If the tower has a saved location, its marker becomes draggable.
- Dragging the marker saves the new coordinates immediately.
- While a tower is selected for map editing, tapping anywhere on the map moves that tower there and saves immediately.
- Towers without a saved location can be placed by selecting them and tapping the map.
- Stop Editing exits the map-edit mode.
- Existing coordinate-paste updater, satellite/street map, Registry globe indicator,
  Scan, Lookup, Add/Edit, Backup, fixed PIN 159357, GitHub Pages and PWA support preserved.
