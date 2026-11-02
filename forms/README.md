# Camunda Forms – Use Case 1

Owner: Ogan Bertun Alpaydin (Sprint 2)

| File | Used by | Functionality |
|---|---|---|
| `product-listing.form` | "Submit product details" and "Correct product details" user tasks | A – Product Listing and Validation |
| `stock-update.form` | "Update stock and availability" user task | B – Inventory and Seasonal Availability |

## Process variables

The form keys become process variables, so they must match the names used in the operational BPMN.

| Key | Type | Rule | Used in |
|---|---|---|---|
| `productName` | text | required, max 100 | A, B |
| `description` | text | required | A |
| `category` | select | required (categories from the case study) | A |
| `price` | number | required, min 0.01 | A |
| `unit` | select | required (kg, each, dozen, bunch, jar) | A |
| `quantity` | number | required, min 0, whole number | A, B – "stock = 0?" gateway |
| `farmOrigin` | text | required | A |
| `availableFrom`, `availableUntil` | date | required | A, B – "within season?" gateway |
| `harvestDate`, `bestBeforeDate` | date | optional | A |
| `allergens` | text | optional | A |
| `isOrganic` | boolean | – | A – "organic claimed?" gateway |
| `certificationNumber` | text | required only when `isOrganic` is ticked | A – certification check |
| `validationMessage` | text | set by the process, not the producer | A – shown at the top when details need correcting |

The same listing form is reused for the correction loop. Because the keys stay the same, the producer sees their earlier answers and the reason the listing was rejected.

## AI use

These form files were drafted with help from Claude (Anthropic). I imported them into Camunda, tested them there (required fields, the organic condition and the correction message) and added the `unit` field myself, because the price needs a unit. Field names and rules are taken from Use Case 1 and the case study.
