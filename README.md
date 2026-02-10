# UTIL2000 (COBOL) — Multi-Customer Utility Bill Calculator

This COBOL program is designed to calculate and display utility bills for multiple customers (CUST-ALPHA, CUST-BRAVO, and CUST-CHARLIE). It demonstrates iterative procedural logic by loading specific customer data—including Kilowatt Hours (KWH) used and base service fees—into working storage and performing a standardized billing routine for each.

## What it does

For each customer execution, the program performs the following tiered calculation logic:

1.  **Tier 1 Calculation**: Computes the charge for the first 500 kWh at a rate of **$0.12/kWh**.
2.  **Tier 2 Calculation**: Computes the charge for the next 500 kWh (501–1000) at a rate of **$0.15/kWh**.
3.  **Tier 3 Calculation**: Computes the charge for any usage exceeding 1000 kWh at a rate of **$0.18/kWh**.
4.  **Final Total**: Adds the calculated tier charges to a fixed service fee of **$14.95** to produce the final total bill.

The program utilizes `PERFORM` statements to execute these calculations for all three predefined customers in a single run.

## COBOL Concepts Used

In this assignment, I implemented the following enterprise computing concepts:

* **Program Header Documentation**: Organized the Identification Division with programmer details, date, GitHub URL, and project description.
* **Working-Storage Data Definition**: Defined numeric items using specific `PIC` clauses for raw data and `VALUE` constants for rates and limits.
* **Numeric Editing**: Used `Z,ZZZ,ZZ9` and `$$,$$$,$$9.99` picture strings to format raw computational data into human-readable currency formats.
* **Procedural Logic**: Utilized `PERFORM` and paragraph-based execution to reuse the billing routine across different data sets.
* **Arithmetic Operations**: Used `COMPUTE` with the `ROUNDED` phrase to ensure financial accuracy across three distinct tiers of pricing.

## Program Output

Below is a screenshot of the program execution showing the calculated bills for the three customer phases:

![Program Output](assets/UTIL2000_Output.png) 

---

### Author Profiles
* [Tristan Joubert - GitHub](https://github.com/TJoubert004) 
