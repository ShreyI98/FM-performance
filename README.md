# FM Pickup Performance Dashboard

## Tabs
### Failure Analysis
- All failure reasons
- Client-wise failure list with failure count and % contribution
- FE-wise failure analysis shown on demand with: total mapped pickup, failed pickup, success pickup and failure %
- No failure-by-centre chart

### Pickup Success Analysis
Uses only `Status = Picked Up` from the raw data and includes:
- Client-wise success view
- Weight
- PUR count / PUR ID trend
- Weight trend
- Dispatch ID-wise PUR mapping with PUR IDs

### Filters
- Centre selector (worksheet name = centre)
- Multi-date selector

### Data loading
- Excel: every non-empty worksheet is loaded and treated as a separate centre.
- CSV: treated as a single `CSV` centre.
- After first load, the upload panel is hidden.
- `↻ Re-upload Raw Data` replaces the dataset and resets date filters.
- The last processed dataset is stored locally in the browser for convenience.

### Failure logic
1. Status = Not Picked
2. Exclude OTP/Geofence when In Slot = Yes
3. Exclude Shipment not ready for pickup-Multi client Seller Partial handover
4. Exclude Client = FEDEX EXPORT
