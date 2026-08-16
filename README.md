# FM Pickup Performance Dashboard

- Failure Analysis and Pickup Success Analysis tabs.
- All Excel worksheets are loaded and each worksheet name is treated as a centre.
- Centre selection and a smooth From/To date-range selection are applied to both tabs.
- Filters are applied only after clicking **Refresh Dashboard**.
- Failure tab:
  - Failure reason list with count, contribution %, and sorting.
  - Client-wise failure list with count, contribution %, and sorting.
  - FE-wise failure analysis with failed pickups out of total mapped pickups and sorting; displayed on click.
  - KPI labels: Not picked and Failure.
- Success tab:
  - Uses only Status = Picked Up.
  - Client-wise pickup list.
  - PUR ID trend.
  - Weight trend.
  - Weight shown in KG and Tons.
  - Dispatch ID-wise PUR mapping.
- Re-upload Raw Data replaces the current dataset.
- Confirmed failure logic:
  1. Status = Not Picked.
  2. Exclude OTP/Geofence when In Slot = Yes.
  3. Exclude Shipment not ready for pickup-Multi client Seller Partial handover.
  4. Exclude Client = FEDEX EXPORT.


## Counting and weight rules
- Total PUR is counted using unique `Pickup Id` values; blank IDs are counted by source row.
- Picked Up PUR uses unique PURs with `Status = Picked Up`.
- Weight is read from the raw `Weight` column as kilograms, summed once per unique PUR.
- Tons = KG / 1000.
- Weight parsing accepts numeric Excel values and text values containing commas or KG.
