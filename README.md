# SA Mark Normalizer

A simple browser-based tool to normalize SA marks from **50 marks to 20 marks** and automatically populate an SA output template.

## Features

- Reads student marks from an Excel file
- Converts marks from 50 to 20 using:

  ```
  Normalized Mark = Original Mark × 0.4
  ```

- Maps marks using Register Number
- Automatically fills:
  - Q1 to Q5 marks
  - Total mark
- Generates a ready-to-upload output Excel file
- Runs completely in the browser (no server required)

---

## Input File Requirements

Upload the **Input Marks File** with the following structure:

| Column | Data |
|----------|----------|
| C | Register Number |
| G | Question 1 Mark |
| H | Question 2 Mark |
| I | Question 3 Mark |
| J | Question 4 Mark |
| K | Question 5 Mark |

### Example

| C | G | H | I | J | K |
|---|---|---|---|---|---|
| 721123104001 | 45 | 40 | 38 | 42 | 48 |

After normalization:

| Q1 | Q2 | Q3 | Q4 | Q5 |
|----|----|----|----|----|
| 18 | 16 | 15.2 | 16.8 | 19.2 |

---

## Output Template Requirements

Upload the official SA output template.

The tool expects:

- Register Numbers in **Column A**
- Student data beginning from **Row 5**
- Marks will be written into:

| Column | Data |
|----------|----------|
| F | Total Mark |
| G | Q1 |
| H | Q2 |
| I | Q3 |
| J | Q4 |
| K | Q5 |

---

## Usage

### Step 1

Upload the **Input Marks File**

### Step 2

Upload the **Output Template**

### Step 3

Click:

```
Generate Output
```

### Step 4

The file:

```
Final_SA_Marks.xlsx
```

will be downloaded automatically.

---

## Calculation Logic

For each student:

```text
Q1 = Column G × 0.4
Q2 = Column H × 0.4
Q3 = Column I × 0.4
Q4 = Column J × 0.4
Q5 = Column K × 0.4
```

Total:

```text
Total = Q1 + Q2 + Q3 + Q4 + Q5
```

All values are rounded to 2 decimal places.

---


## Notes

- Register Numbers are used for mapping.
- Missing students are assigned zero marks.
- The tool runs entirely offline after loading.
- No data is uploaded to any server.

---

## Output File

Generated file name:

```text
Final_SA_Marks.xlsx
```

---

## Disclaimer

This tool is provided for educational and administrative assistance purposes only.

While every effort has been made to ensure accurate mark conversion and template generation, users are strongly advised to randomly verify a sample of student records and calculated marks before final submission or uploading to any official portal.

The author(s) of this tool shall not be responsible for any errors arising from incorrect input files, template modifications, data inconsistencies, or verification omissions. Final responsibility for validating the generated marks rests with the user.
