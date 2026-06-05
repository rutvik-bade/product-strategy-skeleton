Stock planning and control across raw materials, WIP and finished goods

# Categorization

Inventory is correctly connected to [[Manufacturing and Assembly]] because production depends on raw material availability, WIP control and finished-goods readiness.

It should also be treated as a cross-operational control point linked to [[Supply Chain and Sourcing]], [[Production Planning and Control]], [[Logistics and Fulfillment]] and [[Financial Modelling]] because inventory affects supplier lead times, warehouse execution, customer service levels and working capital.

# EOQ

Economic Order Quantity belongs here.

Use EOQ to estimate the replenishment quantity that minimizes ordering or setup cost plus holding cost.

```
EOQ = sqrt((2 * annual demand * order or setup cost) / annual holding cost per unit)
```

Use it when demand is reasonably stable, replenishment costs are measurable and holding cost is meaningful. Do not use it blindly for highly volatile, perishable, constrained-capacity or strategic-scarcity items.

# Replenishment controls

- Reorder point: demand during lead time plus safety stock.
- Safety stock: buffer against demand variability, supply variability and service-level targets.
- Minimum order quantity: supplier or production constraint that may override EOQ.
- Lot size: production batch size, packaging size or transport unit size.
- Lead-time variance: actual supplier or production lead time compared with planned lead time.

# Inventory segmentation

- ABC analysis: classify SKUs by consumption value or revenue impact.
- XYZ analysis: classify SKUs by demand variability.
- Pareto analysis: identify the SKUs causing most stock value, stockouts, obsolete stock or warehouse effort.
- Criticality: tag parts that can stop production or customer delivery even if their value is low.

# Metrics

- Inventory turns
- Days inventory outstanding
- Stockout rate
- Fill rate
- Service level
- Excess and obsolete inventory
- Inventory carrying cost
- Gross margin return on inventory investment
- Forecast accuracy by SKU
- Cycle count accuracy

# Operating questions

- Which SKUs tie up the most cash?
- Which SKUs cause the most missed orders or production stoppages?
- Which items should be made to stock, made to order or discontinued?
- Which reorder policies should differ by ABC/XYZ class?
