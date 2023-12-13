
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

