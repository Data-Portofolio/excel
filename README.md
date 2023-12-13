
# Text Manipulation Fuction 

### 1. Concatenation
   - **Example:**
     - Assuming A1 contains "Hello" and B1 contains "World"
     - Formula:
       ```excel
       =A1 & " " & B1
       ```
      **Output:**
     >`Hello World`

### 2. Substring Extraction
   - **Example:**
     - Assuming A1 contains "Excel is powerful"
     - Formula: `=LEFT(A1, 5)`
     - Output: `Excel`

### 3. **Text to Upper/Lower Case**
   - **Example:**
     - Assuming A1 contains "Hello"
     - Formula: `=UPPER(A1)`
     - Output: `HELLO`

### 4. **Find and Replace**
   - **Example:**
     - Assuming A1 contains "apple orange apple"
     - Formula: `=REPLACE(A1, 7, 6, "banana")`
     - Output: `apple banana apple`

### 5. **Text Length**
   - **Example:**
     - Assuming A1 contains "Excel"
     - Formula: `=LEN(A1)`
     - Output: `5`

### 6. **Trimming Spaces**
   - **Example:**
     - Assuming A1 contains "   Trim   "
     - Formula: `=TRIM(A1)`
     - Output: `Trim`

### 7. **Splitting Text**
   - **Example:**
     - Assuming A1 contains "First Last"
     - Formula: `=LEFT(A1, FIND(" ", A1) - 1)`
     - Output: `First`
     - Formula: `=MID(A1, FIND(" ", A1) + 1, LEN(A1))`
     - Output: `Last`

### 8. **Text to Columns**
   - **Example:**
     - Assuming A1 contains "John,Doe"
     - Method: Data tab -> Text to Columns (using comma as a delimiter)
     - Output (two separate columns): 
       - Column A: `John`
       - Column B: `Doe`

# Functional Condition

In Excel, the `IF` function is used for conditional statements. The basic syntax of the `IF` function is:

```excel
=IF(logical_test, value_if_true, value_if_false)
```

- `logical_test`: This is the condition you want to check.
- `value_if_true`: If the logical test is true, this is the value that will be returned.
- `value_if_false`: If the logical test is false, this is the value that will be returned.

Here are a few examples:

1. **Basic IF Statement:**
   - If the value in A1 is greater than 10, return "Yes"; otherwise, return "No".
     ```excel
     =IF(A1>10, "Yes", "No")
     ```

2. **Nested IF Statements:**
   - If A1 is greater than 10, return "High"; if A1 is between 5 and 10 (inclusive), return "Medium"; otherwise, return "Low".
     ```excel
     =IF(A1>10, "High", IF(A1>=5, "Medium", "Low"))
     ```

3. **Text-based Condition:**
   - If the text in A1 is "Done", return "Complete"; otherwise, return "Incomplete".
     ```excel
     =IF(A1="Done", "Complete", "Incomplete")
     ```

4. **Using Functions in Conditions:**
   - If the sum of B1 and C1 is greater than 100, return "Over Budget"; otherwise, return "Within Budget".
     ```excel
     =IF(SUM(B1, C1) > 100, "Over Budget", "Within Budget")
     ```

5. **Checking for Blank Cells:**
   - If A1 is not blank, return the value in A1; otherwise, return "No Data".
     ```excel
     =IF(ISBLANK(A1), "No Data", A1)
     ```

6. **Date-based Condition:**
   - If the date in A1 is today or later, return "Upcoming"; otherwise, return "Past".
     ```excel
     =IF(A1>=TODAY(), "Upcoming", "Past")
     ```
<details>
   <summary>the `AND` and `OR` functions
   </summary>
<br>
   
1. **Using `AND` Function:**
   - If both A1 is greater than 10 and B1 is not blank, return "Valid"; otherwise, return "Invalid".
     ```excel
     =IF(AND(A1>10, NOT(ISBLANK(B1))), "Valid", "Invalid")
     ```

2. **Using `OR` Function:**
   - If either A1 is greater than 10 or B1 is "Complete", return "OK"; otherwise, return "Not OK".
     ```excel
     =IF(OR(A1>10, B1="Complete"), "OK", "Not OK")
     ```

3. **Combining `AND` and `OR`:**
   - If A1 is between 5 and 10 (inclusive) and B1 is "High" or "Medium", return "Good"; otherwise, return "Not Good".
     ```excel
     =IF(AND(A1>=5, A1<=10, OR(B1="High", B1="Medium")), "Good", "Not Good")
     ```

These examples showcase how you can use `AND` and `OR` functions to create more sophisticated conditions in your `IF` statements. Adjust the conditions based on your specific requirements and the data in your Excel sheet.
</details>

