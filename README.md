# FM Pickup Performance Dashboard

## Data loading
- First opening: upload the raw Excel/CSV file.
- Every worksheet in an Excel workbook is loaded; each worksheet name is treated as a centre.
- After loading, the upload panel is hidden.
- A small **↻ Re-upload Raw Data** button appears beside the dashboard title.
- Clicking it opens the file picker and replaces the current dataset.
- Re-upload resets the selected centre/date filters and refreshes the dashboard.
- The last processed dataset is retained in the browser so the dashboard can reopen without the large upload screen; use **Re-upload Raw Data** whenever the source file changes.

## Filters
- Centre selector: select one or more centre sheets.
- Date selector: add multiple dates and remove selected dates individually.

## Failure logic
1. Start with `Status = Not Picked`.
2. Exclude OTP/Geofence when `In Slot = Yes`.
3. Exclude `Shipment not ready for pickup-Multi client Seller Partial handover`.
4. Exclude `Client = FEDEX EXPORT`.

## GitHub Pages
Upload `index.html` and `README.md` to the repository root and deploy `main` / root through GitHub Pages.
