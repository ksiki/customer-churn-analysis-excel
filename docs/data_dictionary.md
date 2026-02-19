# Data Dictionary

## customers_raw.csv
- CustomerID: unique customer key
- Age: customer age
- Gender: category
- Country: ISO-ish country code
- AcquisitionChannel: acquisition source 
- SignupDate: date the customer signed up 

## subscriptions_raw.csv
- CustomerID: key
- PlanType: Basic/Standard/Pro/Enterprise 
- MonthlyFee: monthly subscription price 
- ContractType: Month-to-Month/Annual/Quarterly 
- StartDate: subscription start 
- EndDate: subscription end 

## activity_raw.csv
- CustomerID: key
- LastLoginDate: last login 
- SupportTickets: count 
- UsageHoursLast30Days: usage hours in last 30 days 
