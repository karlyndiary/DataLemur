Assume you're given the table on user viewership categorised by device type where the three types are laptop, tablet, and phone.

Write a query that calculates the total viewership for laptops and mobile devices where mobile is defined as the sum of tablet and phone viewership. Output the total viewership for laptops as laptop_reviews and the total viewership for mobile devices as mobile_views.

Effective 15 April 2023, the solution has been updated with a more concise and easy-to-understand approach.

```
SELECT 
  SUM(CASE WHEN device_type = 'laptop' then 1 else 0 end) as laptop_views,
  SUM(CASE WHEN device_type IN ('phone', 'tablet') then 1 else 0 end) as mobile_views
FROM viewership;
```
