# Power Query Transformations

## Customers 
1. Remove duplicate CustomerID rows
2. Trim text columns (Country, Gender, AcquisitionChannel)
3. Standardize Country values
4. Standardize Gender values
5. Fix/flag invalid ages
6. Parse SignupDate from mixed formats; set type = Date

## Subscriptions
1. Remove duplicates by CustomerID 
2. Standardize PlanType values 
3. Standardize ContractType values 
4. Parse StartDate/EndDate from mixed formats; set type = Date
5. Fix MonthlyFee:
   - convert blanks to null
   - flag negative/zero/extreme values as anomalies
6. Create:
   - IsChurned (EndDate not null)
   - TenureDays (EndDate - StartDate; if active, Today - StartDate)
   - TenureMonths = Number.RoundDown(TenureDays / 30)

## Activity 
1. Remove duplicates by CustomerID
2. Parse LastLoginDate from mixed formats
3. Convert SupportTickets and UsageHoursLast30Days to numeric
4. Flag outliers:
   - SupportTickets < 0 or > 20
   - UsageHours < 0 or absurdly high
