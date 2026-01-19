# Backorder-Early-Warning-Classifier-Supply-Chain
## Author: Ishika Narang
Given what we know about a part at planning time, predicting whether it is at high risk of going on backorder soon, so planners can intervene before customers are impacted.
n supply chain management, "backorders" occur when an order cannot be completed at the point of sale due to the item not being in the seller's inventory, even though it is still being produced or accessible from the distributor. Backorders indicate to the seller that anticipated demand has surpassed expectations, whether due to inadequate planning, supply chain problems, excessively rigid safety stock policies, or an unexpected surge in demand for a product (Jenkins, 2025).

From a business perspective, backorders damage a company's performance on several fronts, such as:

- **Customer dissatisfaction** - late or incomplete deliveries erode customer trust and encourage customers to switch to competitors.

- **Revenue delays** - and opportunity lost from unfulfilled orders.

- **Operational chaos** - supply managers and staff are forced to switch to reactive mode to expedite shipments, re-allocate scarce stock, renegotiate with suppliers, or even find alternative sources.

- **Hidden cost and risk** - frequent backorders indicate deeper structural issues such as chronic under-forecasting of products, over-reliance on a single or a few suppliers, insufficient safety stock, and stress on staff.

- **Damaged service-level agreements (SLAs)** - An SLA is a formal documented agreement between a service provider (for example, a supplier) and a customer that outlines the specific level and logistics of the service expected (Hand, 2025). SLA violations cause backorders and increase the risk of inventory issues.

For a company managing thousands of stock-keeping units (SKUs) across a complex supply network, the question becomes: Can we identify which parts are at high risk of going on backorder before it actually happens? This is the motivation behind my project.

A good early warning system does not eliminate all the backorders uncertainty but it can give the supply chain managers a critical advantage, which would be the time to intervene. When informed of all the high-risk SKUs at regular frequent intervals, they can take targeted actions such as increase safety stock for certain parts, negotiate better deals with suppliers ahead of time, diversify their suppliers, and even do more accurate contingency planning. This transforms reactive responses to proactive risk management.

### Framing as a machine learning problem
Data sourcing: For this project, I am using the Backorder Prediction Dataset from Kaggle (https://www.kaggle.com/datasets/gowthammiryala/back-order-prediction-dataset/data), which is already split into 2 files - Training_BOP.csv and Testing_BOP.csv. The data is tabular and concerns spare parts in a supply chain. Each row is a snapshot of an SKU with features describing its inventory, demand and supplier performance (explored in detail below). The datacard on Kaggle does not describe the dataset or the units of the features included, so I will explore the data in detail and clearly state the assumptions I would make to use the data.

**Overall Goal:** Considering the business value of the early-warning system, I will treat this as a classification task where my model is less about being perfectly “right” on every SKU, and more about surfacing a set of high-risk parts where early intervention has the biggest impact.

### Goal of the project
Design a computational essay that:

- Frames the business problem as an ML problem clearly

- Builds a reproducible and transparent ML pipeline

- Compares multiple ML algorithms and evaluates them with the appropriate data considerations

- Integrates explainable AI to understand feature contributions to backorder risk

- Translates model results into business recommendations

By the end of the pipeline, a supply chain manager should be able to identify which and what kind of SKUs are systematically at risk of a backorder and what levers drive the risk.
