# FM Pickup Performance Dashboard

### Weight calculation
The raw workbook can contain multiple rows for the same PUR. The dashboard first groups raw rows by **Centre + Pickup Id (PUR)** and calculates:

**PUR Weight (KG) = SUM of every raw `Weight` column value belonging to that PUR.**

The resulting PUR-level weight is then used everywhere:
- Pickup Success total weight
- KG / Tons
- Client-wise weight
- Date-wise weight trend
- Dispatch ID-wise mapped PUR weight

A PUR is counted once in PUR counts. Dispatch IDs contain/club multiple PURs; dispatch-level weight is the sum of the already-calculated PUR weights.

All non-empty Excel worksheets are treated as separate centres.

Failure logic:
1. Status = Not Picked
2. Exclude OTP/Geofence when In Slot = Yes
3. Exclude Shipment not ready for pickup-Multi client Seller Partial handover
4. Exclude Client = FEDEX EXPORT
