<details>
   <summary>Shortcurt</summary>
   <br>
   
![image](https://github.com/Data-Portofolio/excel/assets/133883292/244f86f5-e157-40e2-8bb2-438ca6ada80c)

<br>

1. **Pintasan Navigasi:**
   - **Tombol Panah:** Pindah satu sel ke arah panah.
   - **Ctrl + Tombol Panah:** Pindah ke tepi wilayah data.
   - **Ctrl + Beranda:** Pindah ke awal lembar kerja.
   - **Ctrl + Akhir:** Pindah ke sel terakhir dengan data.
   - **Ctrl + Page Up/Page Down:** Beralih antara tab lembar kerja.

2. **Pintasan Seleksi:**
   - **Shift + Tombol Panah:** Perluas seleksi ke arah panah.
   - **Ctrl + Spasi:** Pilih seluruh kolom.
   - **Shift + Spasi:** Pilih seluruh baris.
   - **Ctrl + A:** Pilih seluruh lembar kerja.

3. **Pintasan Pengeditan:**
   - **F2:** Edit sel aktif.
   - **Ctrl + C:** Salin sel yang dipilih.
   - **Ctrl + X:** Potong sel yang dipilih.
   - **Ctrl + V:** Tempel sel yang disalin/dipotong.
   - **Ctrl + Z:** Batalkan tindakan terakhir.
   - **Ctrl + Y:** Ulangi tindakan yang terakhir dibatalkan.

4. **Pintasan Format:**
   - **Ctrl + B:** Tebal.
   - **Ctrl + I:** Miring.
   - **Ctrl + U:** Garis bawah.
   - **Ctrl + 1:** Dialog format sel.
   - **Ctrl + Shift + $:** Terapkan format mata uang.
   - **Ctrl + Shift + %:** Terapkan format persentase.

5. **Pintasan Fungsi:**
   - **Alt + =:** AutoJumlah.
   - **Ctrl + Shift + L:** Alih filter.
   - **Ctrl + `:** Tampilkan rumus.
   - **Ctrl + Shift + (+):** Sisipkan sel baru.
   - **Ctrl + (-):** Hapus sel.

6. **Pintasan Lain-lain:**
   - **Ctrl + S:** Simpan.
   - **F12:** Simpan Sebagai.
   - **Ctrl + P:** Cetak.
   - **Ctrl + F:** Cari.
   - **Ctrl + H:** Ganti.

</details>

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

# Lookup

Lookup functions in Excel are powerful tools for searching and retrieving information from a table or range of data. Here are some common lookup functions in Excel:

1. **VLOOKUP (Vertical Lookup):**
   - Searches for a value in the first column of a table and returns a value in the same row from another column.
     ```excel
     =VLOOKUP(lookup_value, table_array, col_index_num, [range_lookup])
     ```
     Example:
     ```excel
     =VLOOKUP(A1, $B$2:$D$10, 3, FALSE)
     ```

2. **HLOOKUP (Horizontal Lookup):**
   - Searches for a value in the first row of a table and returns a value in the same column from another row.
     ```excel
     =HLOOKUP(lookup_value, table_array, row_index_num, [range_lookup])
     ```
     Example:
     ```excel
     =HLOOKUP(A1, $B$2:$D$10, 2, FALSE)
     ```

3. **LOOKUP:**
   - Searches for a value in a range or array and returns a corresponding value from the same position in another range or array.
     ```excel
     =LOOKUP(lookup_value, lookup_vector, result_vector)
     ```
     Example:
     ```excel
     =LOOKUP(A1, $B$2:$B$10, $C$2:$C$10)
     ```

4. **INDEX and MATCH (Dynamic Lookup):**
   - Uses the combination of the INDEX and MATCH functions to perform flexible lookups.
     ```excel
     =INDEX(return_range, MATCH(lookup_value, lookup_range, 0))
     ```
     Example:
     ```excel
     =INDEX($C$2:$C$10, MATCH(A1, $B$2:$B$10, 0))
     ```

5. **XLOOKUP (Modern Lookup):**
   - Searches a range or array, and returns an item corresponding to the first match it finds.
     ```excel
     =XLOOKUP(lookup_value, lookup_array, return_array, [if_not_found], [match_mode], [search_mode])
     ```
     Example:
     ```excel
     =XLOOKUP(A1, $B$2:$B$10, $C$2:$C$10, "Not Found", 0, 1)
     ```

