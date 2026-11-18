# Camunda Forms – Use Case 1

Owner: Ogan Bertun Alpaydin (Sprint 2)

| File | Used by | Functionality |
|---|---|---|
| `product-listing.form` | "Submit Product information" and "Correct product details" user tasks | A – Product Listing and Validation |
| `stock-update.form` | "Update stock and seasonal availability" (A); "Update stock and season dates", "Correct quantity" and "Correct season dates" (B) | A and B – Inventory and Seasonal Availability |

All producer user tasks are assigned to the `producers` candidate group.

## Process variables

The form keys become process variables, so they must match the names used in the operational BPMN.

| Key | Type | Rule | Used in |
|---|---|---|---|
| `productName` | text | required, max 100 | A, B |
| `description` | text | required | A |
| `category` | select | required (categories from the case study) | A |
| `price` | number | required, min 0.01 | A |
| `unit` | select | required (kg, each, dozen, bunch, jar) | A |
| `quantity` | number | required, min 0, whole number | A – "Stock quantity = 0?" gateway; B – "Quantity valid?" and "Stock above zero?" gateways |
| `farmOrigin` | text | required | A |
| `availableFrom`, `availableUntil` | date | required | A, B – "Dates valid?" and "Within season?" gateways |
| `harvestDate`, `bestBeforeDate` | date | optional | A |
| `allergens` | text | optional | A |
| `isOrganic` | boolean | – | A – "Organic product?" gateway |
| `certificationNumber` | text | required only when `isOrganic` is ticked | A – certification check |
| `validationMessage` | text | set by the process, not the producer | A – shown at the top when details need correcting |

The same listing form is reused for the correction loop, both when the data is invalid and when the certificate can't be verified. Because the keys stay the same, the producer sees their earlier answers and the reason the listing was rejected.

## AI use

## AI use

I made these forms for Sprint 2 in Camunda. Claude helped me draft the first version of the form files. I then imported and tested them in Camunda, added the `unit` field, linked them to the producer user tasks and assigned the producers group myself.
