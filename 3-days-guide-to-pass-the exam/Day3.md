## EC2 Instance Pricing Models

|                      |               **On-Demand**               |                         **Spot**                          |             **Reserved**             |                                **Savings Plan**                                 |
|:--------------------:|:-----------------------------------------:|:---------------------------------------------------------:|:------------------------------------:|:-------------------------------------------------------------------------------:|
|   **WHAT IS IT?**    | Pay as you use it, No up-front commitment |                Bid on AWS's spare capacity                |       Commitment of 1-3 years        | Commitment of 1-3 years, Saving on the commitment; on-demand pricing after that |
|       **COST**       |           Most expensive option           | Least expensive option , Up to 90% savings over on-demand |    30%-60% savings over on-demand    |                          Less expensive than on-demand                          |
|  **BEST USED FOR**   |      General use , Trying things out      |                  Interruptible workloads                  |       Steady, Known workloads        |            Steady, Known workloads but with more flexibility than RI            |
| **IMPORTANT POINTS** |      Flexible and easy to work with       |          Instance can be terminated at any time           | Pay for capacity regardless of usage |                 Introduced 2019, Flexible and easy to work with                 |

---

## AWS Organizations

- Centrally manage multiple accounts, including permissions

- Consolidated billing
	1. Receive a single bill for all account in the organization
	2. Track combined costs, but can itemize account.
	3. Can share discount pricing (Reserved Instances, Saving Plans) across accounts.

---

## Cost Allocation Tags

- Once activated, can be used to group and filter charges (such as "createdBy")

---

## Billing DashBoard

- Providing a snapshot of costs by service, forcasted costs, etc...

---

## Cost Explorer

- Provides a way to drill into specific charges and group/filter by service, region, tags, etc...
- Can provide a forecast of charges based on existing usage.

---

## AWS Pricing Calculator

- Prior iterations were called "Total Cost of Ownership" (**TCO**) Calculator and the "Simple Monthly Calculator".
- Publicly available at calculator.aws
- Provides an estimated of costs based on the services chosen (useful for existing customers, as well as those who are evaluating AWS).

---

## AWS Budgets vs. CloudWatch Billing Alerts/Alarms

|                        **AWS Budgets**                         |               **CloudWatch Billing**                |
|:--------------------------------------------------------------:|:---------------------------------------------------:|
|        Used to create and track budgets and send alerts        | More limited than budgets; only used to send alerts |
| Can receive alerts based on actual spend AND forecasted spend  |    Can receive alerts based on actual spend only    |
|            Can filter alarms by region and service             |         Filtering by region is not possible         |
| Create budgets for cost, usage, Savings Plans and Reservations |                                                     |
|                         Newer Service                          |                                                     |
