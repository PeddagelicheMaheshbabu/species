# SpiceCost Pro — Full React UI

## Single-file application: SpiceCostPro.jsx

All 8 pages in one file. No external dependencies beyond chart.js.

## Install & Run

```bash
npm install
npm start
# Opens at http://localhost:3000
```

## Pages included
| Page | Description |
|---|---|
| Dashboard | KPI cards, donut chart, product summary table |
| SKU Explorer | Filter/search 300K SKUs with live card grid |
| Cost Breakdown | Line + bar charts, QoQ comparison, full register |
| Cost Simulator | 8 sliders → live cost/price/export calculation + save scenarios |
| Region Pricing | Per-region price matrix + FX converter |
| Freight Matrix | Zone × mode rates + inline calculator |
| Audit Log | Filterable change history with impact tracking |
| Bulk Import | Drag-drop CSV/Excel upload with animated progress |

## Cost Formula
```
Total Cost  = (PR × batch_yield) + (PM × units_per_kg) + (PR × OH%) + Freight
List Price  = Total Cost / (1 − margin%)
Export Price = List Price / FX Rate
```

## To connect to backend
Replace static PRODUCTS / REGIONS / AUDIT_EVENTS data at the top of
SpiceCostPro.jsx with API calls using the axios clients from the backend
project (see costApi.js, regionApi.js, auditApi.js).
