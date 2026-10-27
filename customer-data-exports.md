# Customer data exports

The CSV export endpoint was removed in web-app v4.6.0 (WEB-8), so when a customer asks for their data as a
file, an engineer produces it. Customer Success files a CS ticket labelled `data-export`.

1. Hamilton approves the request on the ticket (check the contract allows the data asked for).
2. The web-app owner runs `scripts/usage_export.py --tenant <tenant> --quarter <YYYY-Qn>` from a web-app
   checkout.
3. Upload the file with the Reports API (`POST /api/v2/reports/exports`, WEB-9) so the customer gets a
   signed, expiring link instead of an attachment.
4. Comment the link's expiry on the ticket and close it. Customer Success sends the link.
