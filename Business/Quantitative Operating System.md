Cross-functional measurement system for objectively running the business

# Purpose

Turns each strategy module into a measurable operating surface: what to track, which decisions the metric supports, and which analytical tools can be used to improve it.

# Metric design rules

- Tie every metric to a decision, owner, cadence and threshold.
- Separate input metrics from output metrics.
- Track both efficiency and effectiveness.
- Use leading indicators for daily control and lagging indicators for board-level review.
- Segment before averaging: channel, SKU, customer cohort, supplier, region, product line and time period.
- Pair each metric with a counter-metric to prevent local optimization.

# Core business equation

```
Enterprise value improves when the business increases durable revenue, expands contribution margin, shortens the cash conversion cycle, lowers avoidable risk and compounds customer retention.
```

# Module metric map

| Module | Quantitative capability | Useful methods |
| --- | --- | --- |
| [[Product Market Fit]] | Validate whether demand is real and repeatable | Sean Ellis rule, activation rate, retention cohorts, NPS, win/loss rate |
| [[Market]] | Size and prioritize opportunity | TAM/SAM/SOM, segment attractiveness, Pareto opportunity ranking |
| [[Pricing]] | Convert value into margin | Price waterfall, willingness-to-pay, elasticity, breakeven, contribution margin |
| [[Financial Modelling]] | Prove economic viability | Unit economics, runway, burn multiple, cash conversion cycle, scenario and sensitivity analysis |
| [[Demand Generation (Marketing)]] | Allocate growth spend | CAC, ROAS, MER, funnel conversion, payback period, channel Pareto |
| [[Sales and Distribution Channels]] | Compare routes to market | Channel margin, sell-through, take rate, distributor ROI, inventory turns by channel |
| [[Retention and Advocacy]] | Measure customer durability | CLTV, churn, repeat purchase rate, cohort retention, referral rate |
| [[Supply Chain and Sourcing]] | Control supply cost and reliability | Supplier scorecard, spend Pareto, purchase price variance, lead-time variability, OTIF |
| [[Production Planning and Control]] | Convert demand into executable production | MPS/MRP, capacity utilization, schedule adherence, takt time, bottleneck analysis |
| [[Inventory]] | Balance service level, cash and stock risk | EOQ, reorder point, safety stock, ABC/XYZ analysis, inventory turns, days inventory outstanding |
| [[Manufacturing and Assembly]] | Improve production throughput | OEE, cycle time, throughput, WIP, scrap rate, first-pass yield |
| [[Quality Assurance]] | Reduce defects and cost of poor quality | Pareto defects, control charts, AQL, defect density, warranty defect rate |
| [[Yield Management]] | Improve usable output | Yield bridge, scrap Pareto, FPY, rework rate, process capability |
| [[Logistics and Fulfillment]] | Deliver reliably at low cost | OTIF, freight cost per unit, warehouse utilization, pick accuracy, return rate |
| [[Customer Support]] | Control post-sale experience | Ticket rate, first response time, MTTR, escalation rate, CSAT, warranty cost |
| [[Operational Metrics]] | Translate product behavior into measurable performance | SLA, uptime, latency, failure rate, MTBF, MTTR |

# Operating cadences

| Cadence | Review focus |
| --- | --- |
| Daily | Exceptions, blockers, service failures, production misses, stockouts |
| Weekly | Funnel movement, schedule adherence, inventory risk, cash pressure, supplier performance |
| Monthly | Unit economics, margin bridge, channel performance, working capital, cohort retention |
| Quarterly | Strategy bets, capacity plan, market attractiveness, portfolio Pareto, pricing architecture |

# Analytical tool shelf

- Pareto analysis: identify the few customers, SKUs, suppliers, defects, channels or costs that create most of the result.
- EOQ: calculate economic replenishment quantity where demand, ordering cost and holding cost are reasonably estimable.
- ABC/XYZ inventory: classify stock by value and demand variability.
- Cohort analysis: compare behavior by acquisition period, product version, customer segment or channel.
- Funnel analysis: find conversion constraints from awareness to purchase to repeat usage.
- Price waterfall: isolate discounts, channel fees, returns, rebates, freight and net realized price.
- Contribution margin tree: connect price, volume, COGS, variable opex and channel cost.
- Cash conversion cycle: measure how long cash is trapped in inventory and receivables net of payables.
- Control charts: distinguish normal variation from process signals.
- Bottleneck analysis: find the constrained resource limiting system throughput.
- Scenario analysis: model best/base/worst cases for demand, margin, cash and capacity.

# Structure guidance

The current four-domain structure is sound:

- [[Business]] owns economic viability, market truth, pricing, legal structure and financial logic.
- [[Technical]] owns product requirements, performance thresholds and technical constraints.
- [[Operational]] owns making, buying, moving and supporting the product.
- [[Marketing and Sales]] owns demand creation, conversion, channels, retention and advocacy.

[[Production Planning and Control]] is correctly placed under [[Manufacturing and Assembly]] because it governs production execution.

[[Inventory]] is acceptable under [[Manufacturing and Assembly]] for a physical-product skeleton because raw material, WIP and finished-goods stock directly constrain production. If the skeleton becomes a broader enterprise operating model, promote it into a dedicated Operational submodule called Inventory Planning and Control, linked across [[Supply Chain and Sourcing]], [[Manufacturing and Assembly]], [[Logistics and Fulfillment]] and [[Financial Modelling]].

If the operating layer becomes more advanced, add an Operational Planning layer above manufacturing:

- Demand Planning
- S&OP
- Production Planning and Control
- Inventory Planning and Control
- Capacity Planning

# Governance

- Each metric needs an owner, source of truth, refresh cadence, target and escalation trigger.
- Dashboards should show trend, target, variance, segment and next action.
- Do not promote a metric unless it changes a decision or exposes a risk.
