# Monthly Financial Reconciliation Dashboard

A 6-page Power BI dashboard for an e-commerce business that tracks revenue, payments, order status, and delivery performance, and reconciles what customers paid against what orders were worth.

<img width="1445" height="858" alt="Screenshot 2026-06-16 143156" src="https://github.com/user-attachments/assets/e0f7469b-1cea-4b99-b546-cea2041f47fa" />
<img width="1442" height="866" alt="Screenshot 2026-06-16 143713" src="https://github.com/user-attachments/assets/51b79ea8-fc9d-4e46-aec6-991b37cb7004" />
<img width="1438" height="866" alt="Screenshot 2026-06-16 143813" src="https://github.com/user-attachments/assets/cdc7b2f1-ad66-4440-9523-5b7f44b23920" />
<img width="1445" height="862" alt="Screenshot 2026-06-16 143929" src="https://github.com/user-attachments/assets/69099692-9b49-4587-bacc-03e3d078d56c" />
<img width="1441" height="857" alt="Screenshot 2026-06-16 144052" src="https://github.com/user-attachments/assets/905194c5-99b4-4400-970c-fcc0d6830ba3" />



**Demo video:** [https://drive.google.com/file/d/1__aRwrKi3HUL5IhS1FAqpO1xdl9qEN2S/view?usp=drive_link)]


## Dataset

The [Olist Brazilian E-Commerce Public Dataset](https://www.kaggle.com/) (public data on Kaggle, orders from September 2016 to October 2018). Amounts are in the dataset's currency (Brazilian Real). I used three tables:

| Table | Content | Rows |
|---|---|---|
| `olist_orders_dataset` | One row per order with status and purchase, approval, delivery, and estimated delivery dates | 99,441 orders |
| `olist_order_items_dataset` | Products in each order with price and freight value | about 98.7K distinct orders |
| `olist_order_payments_dataset` | Payments per order with payment type and value | about 99.4K distinct orders |

## Dashboard Pages

| Page | What it shows |
|---|---|
| **Home** | Navigation buttons and global slicers (date range, order status, payment type) |
| **Executive Financial Overview** | Total revenue, total payments, and reconciliation KPIs, with revenue and payments trends over time |
| **Order Analysis** | Total, delivered, pending, and canceled orders, orders by month, order status distribution, and orders by payment type |
| **Delivery Performance** | Late deliveries, average delay, late deliveries over time, months with the highest delays, and order-level delivery details |
| **Payment Reconciliation** | Total payments, matched, underpaid, and overpaid orders, payments versus revenue over time, and payments by type |
| **Revenue Forecasting** | Net sales over time and a revenue forecast |

## Notes and Limitations

- The dataset contains no cost of goods, so the dashboard reports **net sales (price minus freight)**, not profit or margin.
- Revenue is calculated on **delivered orders only**, and payment reconciliation is done on the same set of orders so the comparison is consistent.
- Order volume in late 2016 is very small and the data thins out after August 2018, so the report is limited to **January 2017 to August 2018** to avoid misleading drops at the edges.
- The forecast is Power BI's built-in forecasting on this period and should be read as an estimate.
