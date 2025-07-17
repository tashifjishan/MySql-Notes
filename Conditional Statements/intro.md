# Maximum Among Three Numbers: 

```sql
SET @a = 110;
SET @b = 90;
SET @c = 110;

-- Determine which variable has the maximum value
SELECT 
  IF(@a > @b, 
     IF(@a > @c, 'A', 
        IF(@a = @c, 'A and C', 'C')), 
	 IF(@b > @c, 'B', 
        IF(@b = @c, 'B and C', 'C'))
   ) AS maximumOfThree;

```
# Questions
- Find maximum between two number
- Check whether a number is negative positive or 0
- Check whether a number is even or odd
- check whether a number is divisible by 5 and 11 or not
- Calculate percentage and grade according to following:
```sql
    Percentage >= 90% : Grade A
    Percentage >= 80% : Grade B
    Percentage >= 70% : Grade C
    Percentage >= 60% : Grade D
    Percentage >= 40% : Grade E
    Percentage < 40% : Grade F
```

- Calculate Gross salary according to following:
```sql
    Basic Salary <= 10000 : HRA = 20%, DA = 80%
    Basic Salary <= 20000 : HRA = 25%, DA = 90%
    Basic Salary > 20000 : HRA = 30%, DA = 95%
```
- Calculate total electricity bill according to the given condition:

```sql
    For first 50 units Rs. 0.50/unit
    For next 100 units Rs. 0.75/unit
    For next 100 units Rs. 1.20/unit
    For unit above 250 Rs. 1.50/unit

    An additional surcharge of 20% is added to the bill
```