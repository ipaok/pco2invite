# PCO2Invite

**Live site: [docs.ipaok.org/pco2invite](https://docs.ipaok.org/pco2invite/)**

> Upload a Planning Center People export, get a guest list ready for Zola, The Knot, or Word mail merge — no account, no server, runs in your browser.

## What it does

Church admins often need to invite congregation members to weddings, graduation parties, and other celebrations. Planning Center has all the contact info, but getting it into an invitation site like Zola or The Knot requires a specific format.

PCO2Invite bridges that gap. Upload your Planning Center CSV export and download a guest list in whatever format you need — all processed locally in your browser. Your church data never leaves your device.

## How to use

1. In Planning Center, go to **People → Export → Export as CSV**
2. Go to the PCO2Invite site and drop the CSV file onto the upload area
3. Choose which membership types to include (Members, Regular Attenders, etc.)
4. Preview the household list and use the search to find specific families
5. Download in your preferred format

## Export formats

| Format | Columns | Best for |
|---|---|---|
| **Household List** | Household Name, People, Address | General reference, spreadsheets |
| **Mail Merge / Labels** | Family Name, Street 1, Street 2, City, State, Zip | Word/Google Docs letters, Avery label printing |
| **Per-Person List** | First Name, Last Name, Household, Email, Phone, Address | Sites that need one row per guest |
| **Zola / The Knot** | First Name, Last Name, Party Name, Email, Phone, Address, City, State, Zip, Country | Direct import into Zola or The Knot guest lists |

## Planning Center export tips

Make sure your export includes these fields:
- First Name, Middle Name, Last Name
- Household ID, Household Name
- Membership
- Home Address (Street Line 1, Street Line 2, City, State, Zip Code)
- Home Email, Mobile Phone Number

## Deployment

This is a static single-page app with no build step. To host on GitHub Pages:

1. Fork or clone this repo
2. Go to **Settings → Pages**
3. Set source to **main branch, / (root)**

Your site will be live at `https://your-username.github.io/pco2invite`.
