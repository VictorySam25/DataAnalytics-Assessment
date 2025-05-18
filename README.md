# DataAnalytics-Assessment
rephrase "SQL Analysis Methodology
This document explains the methodology used to solve each of the four SQL analysis questions for the financial services dataset.

# 1. Customers with Funded Savings and Investment Plans
Methodology:
Objective: Identify customers actively using both savings and investment products

Approach:

Joined user data with account information

Created separate joins for savings plans (types 1 and 4) and investment plans (mutual funds, managed portfolios, fixed investments)

Filtered for active, funded accounts (non-zero amounts, not deleted)

Calculated total deposits across all account types

Key Insights:

Reveals customers engaged with multiple product offerings

Helps identify cross-selling opportunities

Sorted by total deposits to prioritize high-value customers

# 2. Transaction Frequency Categorization
Methodology:
Objective: Analyze customer transaction patterns and categorize by frequency

Approach:

Created CTE to count transactions per customer per month

Calculated monthly averages for each customer

Applied business-defined thresholds:

High: ≥10 transactions/month

Medium: 3-9 transactions/month

Low: ≤2 transactions/month

Added visual indicators (star ratings) for quick analysis

Key Insights:

Identifies highly engaged vs. dormant customers

Helps tailor communication strategies

Provides basis for customer segmentation

# 3. Dormant Account Identification
Methodology:
Objective: Find active accounts with no recent activity

Approach:

Joined account data with transaction records

Calculated days since last transaction

Filtered for:

Active accounts (not deleted/archived, status=1)

No transactions in past 365 days (or ever)

Categorized account types for context

Key Insights:

Identifies accounts needing re-engagement

Helps with account cleanup decisions

Shows potential revenue leakage from inactive funds

# 4. Customer Lifetime Value Calculation
Methodology:
Objective: Estimate customer profitability and long-term value

Approach:

Calculated key metrics:

Account tenure (months since signup)

Total transaction count and value

Profit (0.1% of transaction value)

Developed CLV formula:

(transactions/tenure) * 12 * avg_profit_per_transaction

Protected against division by zero

Key Insights:

Quantifies customer value

Identifies most profitable relationships

Enables data-driven retention strategies

Provides basis for customer tiering"
