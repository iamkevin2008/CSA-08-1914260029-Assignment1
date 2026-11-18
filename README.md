[README_Milk_Cooperative.md](https://github.com/user-attachments/files/35040443/README_Milk_Cooperative.md)
# Milk Cooperative Payment Calculator

## Student details
- Name: Kevin Mathews K
- Register number: 1914260029
- GitHub repository: https://github.com/iamkevin2008/CSA-08-1914260029-Assignment1

## Environment
- Python: [Run `python --version` and enter the result]
- Libraries: Python standard library (`decimal`; tests may use `unittest` or the included custom runner)
- Installed packages and versions: [Record third-party packages, if any]

## Project structure
```text
calculator.py       Interactive/demo payment calculator
milkrate.py         Reusable Decimal-based rate and payout functions
test_milkrate.py    Automated tests for rate and payment calculations
task10.py           Float versus Decimal experiment (if included)
task11.py           Design recommendation/revised requirement notes (if included)
README.md
```
Keep `calculator.py`, `milkrate.py` and `test_milkrate.py` in the same folder so the main program and tests can import the rate module. Add any input data, output screenshots or seasonal implementation files that are actually present in the repository.

## How to run
Run commands from the project folder in a terminal. Confirm the filenames match the committed files.

| Program | Command | Result note |
|---|---|---|
| Rate module demonstration | `python milkrate.py` | Shows rates and payments calculated by the reusable Decimal-based functions. |
| Main calculator | `python calculator.py` | Reads three demonstration entries and prints each payment and the total. The report records a sample total of 917.50. |
| Automated tests | `python test_milkrate.py` | The submitted screenshot reports 6/6 tests passed for standard, boundary and payment cases. |
| Float versus Decimal experiment | `python task10.py` | Compares numerical totals and timing at the tested input sizes, if this file is included. |
| Task 11 / revised design | `python task11.py` | Run only if an executable file with this name is included; otherwise this section is design documentation. |

## Calculation summary
The standard rate uses a base rate of 30.00, a fat adjustment of 0.40 per 0.1 percentage-point step, and an SNF adjustment of 0.30 per 0.1 percentage-point step. Reference values are 3.5% fat and 8.5% SNF. `milkrate.py` uses `Decimal` and rounds money to two decimal places with `ROUND_HALF_UP`.

These values and the nearest-step rule are assumptions recorded in the report. Verify them, any SNF limits, and the official rounding method against the assignment specification before submission.

## Dependencies
The described calculator uses Python's standard library and requires Python 3. No third-party packages are identified in the report. If the repository uses any external packages, record exact versions in `requirements.txt` and list them here.

## Known limitations and next steps
- The executable calculator demonstrates three entries but does not retain a farmer's ten-day history between runs.
- Seasonal rate selection and the bonus rule are described as revised design notes; the supplied `calculator.py` and `milkrate.py` do not implement the complete seasonal workflow.
- Confirm whether the seasonal bonus applies to all litres in the qualifying period or only qualifying litres, and test the 500 L and 501 L boundaries.
- Add any required SNF validation, persistent storage, and tests for malformed input and rounding boundaries.
- Make at least one progressive commit for each assignment task and ensure the repository link is accessible to the course faculty.
