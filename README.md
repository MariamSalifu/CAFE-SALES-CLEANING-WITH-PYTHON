Café Sales Data Cleaning and Analysis (Python)

Project Overview

This project takes a messy record of 10,000 café sales from 2023 and turns it into data a business can trust. Many entries were missing, or held "ERROR" or "UNKNOWN" instead of real values. I rebuilt the missing figures, worked out which menu items earn the most, and identified the gaps in the café's record-keeping. A business can only make sound decisions when its sales records are complete and accurate.

Executive Summary

Salads, sandwiches and smoothies bring in just over half of the café's $89,042 revenue. Coffee is the most frequent purchase but earns little, because it's cheap. Two in five sales have no recorded location and almost a third have no payment method, so fixing record-keeping matters as much as anything the numbers show.

Methodology

Assessed the damage first. I checked every column for blanks and for "ERROR" or "UNKNOWN" entries. Location was missing or invalid on 40% of sales, payment method on 32%, item on 10%, and quantity, price, total and date on about 5% each. There were no duplicate sales.
Rebuilt missing figures instead of guessing. This is where my accounting background came in. Every sale must satisfy quantity × price = total, and each item has one fixed price.
I used those two rules to recover 527 missing prices, 456 quantities and 479 totals.
I also identified 489 unnamed items from their price.
Only 26 sales (0.3%) were missing too much to rebuild, so I removed them.
Reconciled every sale. After cleaning, all 9,974 remaining sales balance exactly: quantity × price equals the total in every row.
Kept dates honest. I left the 460 sales with no valid date out of the monthly trend, rather than piling them onto one day and creating a false spike.
Analysed and visualised the results. I used Python (pandas, matplotlib and seaborn) to break down revenue by item, location, payment method and month, and to chart how sale values are spread.

Findings

Three items bring in half the revenue. Salads ($19,095), sandwiches ($13,716) and smoothies ($13,344) make up 52% of the total. Salads alone bring in 21%.
Coffee is popular but earns little. It's bought more often than anything else (1,286 sales, 3,904 units) but brings in only $7,808 (9%).
Price, not demand, decides revenue. Each named item sold between 3,336 and 3,904 units, so demand is similar across the menu. The difference is price: an average salad sale is $15.04, and an average cookie sale is $2.97.
Record-keeping gaps hide a large share of sales.
40% of revenue ($35,350) has no recorded location.
31% ($27,789) has no payment method.
Even after recovery, $5,087 (6%) can't be linked to a menu item.
Where data exists, sales are evenly split.
In-store ($27,140) and takeaway ($26,553) are level.
Credit card, digital wallet and cash each take about 23%.
Sales are steady all year. Monthly revenue stayed between $6,644 (February) and $7,353 (June), with no strong seasonal peak.

Recommendations

Make item, payment method and location compulsory at the till. Two in five sales currently can't be traced to in-store or takeaway, so decisions about staffing or packaging rest on guesswork.
Sell coffee with higher-value items. Coffee already draws the most purchases. A coffee-and-sandwich or coffee-and-salad meal deal would raise the value of each sale.
Promote the top earners and review the cheapest items. Feature salads, sandwiches and smoothies prominently. Consider selling cookies and tea as add-ons rather than on their own.

