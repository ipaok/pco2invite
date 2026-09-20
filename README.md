# PCO2Invite

**Live site: [docs.ipaok.org/pco2invite](https://docs.ipaok.org/pco2invite/)**

> Upload a Planning Center People export, get a guest list ready for Zola, The Knot, or Word mail merge — or build a printable photo directory — no account, no server, runs in your browser.

## What it does

Church admins often need to invite congregation members to weddings, graduation parties, and other celebrations, or put together a printed photo directory for the congregation. Planning Center has all the contact info, but getting it into an invitation site like Zola or The Knot — or laying it out as a directory — requires a specific format and some manual work.

PCO2Invite bridges that gap. Upload your Planning Center CSV export and either download a guest list in whatever format you need, or design and export a print-ready PDF directory — all processed locally in your browser. Your church data never leaves your device.

## Privacy

**Your data never leaves your device — there's nothing to worry about.** PCO2Invite has no backend and makes no network calls with your data:

- The CSV is read and parsed entirely in your browser (via [PapaParse](https://www.papaparse.com/)); it is never uploaded anywhere
- Household photos you add are held in the browser tab's memory only, and are gone as soon as you close or refresh the tab
- The PDF directory is generated client-side (via [jsPDF](https://github.com/parallax/jsPDF)) and saved straight to your downloads — it never touches a server
- Closing the tab clears everything; nothing is stored, logged, or synced anywhere

This means it's safe to use with real names, addresses, and photos for your congregation — the same names/addresses/photos in your Planning Center export never leave your computer.

## How to use

1. In Planning Center, go to **People → Export → Export as CSV**
2. Go to the PCO2Invite site and drop the CSV file onto the upload area
3. Choose which membership types to include (Members, Regular Attenders, etc.) and a minimum household size
4. Preview the household list and use the search to find specific families
5. Download a guest list in your preferred format, and/or click **Printable Directory** to design and export a photo directory

## Export formats

| Format | Columns | Best for |
|---|---|---|
| **Household List** | Household Name, People, Address | General reference, spreadsheets |
| **Mail Merge / Labels** | Family Name, Street 1, Street 2, City, State, Zip | Word/Google Docs letters, Avery label printing |
| **Per-Person List** | First Name, Last Name, Household, Email, Phone, Address | Sites that need one row per guest |
| **Zola / The Knot** | First Name, Last Name, Party Name, Email, Phone, Address, City, State, Zip, Country | Direct import into Zola or The Knot guest lists |

Every format respects the current search filter, so you can export a subset of households (e.g. just one campus or group) without changing your membership filters.

## Printable directory

Click **Printable Directory** under the export buttons to open the directory designer:

- **Photos** — click any card to upload a household photo (stored only in your browser tab, never uploaded anywhere); toggle photos off entirely for a text-only directory
- **Layout** — 2 or 3 households per row
- **Title** — customize the heading (defaults to "Church Directory")
- **Export PDF** — generates a print-ready, letter-sized PDF directly in the browser (vector text and embedded photos, not a screenshot), with a title page, page numbers, and households grouped by family — ready to print or share as-is

You can also use your browser's own Print (`Cmd/Ctrl+P`) on the directory view if you'd rather print straight from the page.

## Planning Center export tips

Make sure your export includes these fields:
- First Name, Middle Name, Last Name
- Household ID, Household Name
- Membership
- Home Address (Street Line 1, Street Line 2, City, State, Zip Code)
- Home Email, Mobile Phone Number

Planning Center doesn't export photos, so directory photos are added manually, one household at a time, after uploading the CSV.

## Deployment

This is a static single-page app with no build step. To host on GitHub Pages:

1. Fork or clone this repo
2. Go to **Settings → Pages**
3. Set source to **main branch, / (root)**

Your site will be live at `https://your-username.github.io/pco2invite`.
