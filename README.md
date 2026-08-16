# FM Pickup Operations Dashboard

GitHub Pages dashboard supporting two raw-data sources:

- Live Google Sheets URL
- Local Excel (`.xlsx`, `.xls`) or CSV upload

For Google Sheets, the sheet must be shared as **Anyone with the link → Viewer** (or published to the web). Excel/CSV files are processed locally in the browser.

## Failure logic
Adjusted failures are calculated from `Status = Not Picked`, excluding:
- OTP/Geofence remarks when `In Slot = Yes`
- `Shipment not ready for pickup-Multi client Seller Partial handover`
- `Client = FEDEX EXPORT`

No raw sheet/file rows are uploaded to a server by the dashboard.
