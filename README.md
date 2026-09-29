# AMH Payroll Autobot

Monthly payroll entries, advances and reporting for NSK Hospitals – AMH-Pemba.

**Open the app:** use this repository's GitHub Pages link (see the "About" box), or the Google web app link.

## How it works
- The app runs on **Google Apps Script** inside the admin's NSK Google account.
- **Ground team** (NSK Google login) enters: new joiners, left staff, renewals/increments, bank account changes, leave.
- **Admin** sets pay, reviews checks, manages advances (amount + number of months, tracked until fully recovered) and motivation.
- On the chosen day each month the app **emails the Monthly Report** (same layout as the AMH-Pemba report) and saves it to Drive.
- Every entry updates the **AMH Master Payroll** Google Sheet. Allowances, motivation and bonuses are not taxed (no PAYE / ZHSF / ZSSF); Net = Gross − PAYE − ZHSF − ZSSF + allowances − other deductions.

## Files
| File | Where it goes |
|---|---|
| `apps-script/Code.gs` | Apps Script file `Code.gs` |
| `apps-script/Engine.gs` | Apps Script file `Engine.gs` |
| `apps-script/Index.html` | Apps Script HTML file `Index` |
| `index.html` | GitHub Pages link that opens the app |

`Seed.gs` (staff, salaries and bank details used once at setup) is **deliberately not in this repository**. Never upload it here.

## Updating the app
1. Change the code in Apps Script (Extensions → Apps Script from the data sheet).
2. Deploy → Manage deployments → ✏️ → Version: *New version* → Deploy (the link stays the same).
3. Upload the changed file(s) here so GitHub keeps the latest copy.
