# Project Overview

This script is used to update and format financial data, and it saves the updated data to an Excel file.
The script is designed to be run daily, as it sets the ‘Snapshot Date’ to the current date.
The ‘Client Type’ and ‘Company Name’ are set to ‘A’ and ‘AS’ respectively.
The script also handles data type conversions and formatting for specific columns. The final output is saved to Daily_Payment_Information_06112023.xlsx.
The script confirms the successful operation by printing a message.

## Steps

1. Reads data from three CSV files: Dataset_Batch 2.csv, Daily Payment Information Leo.csv, and Penda_balances.csv.
2. Converts the ‘Account Number’ column in the main and info dataframes to the same data type.
3. Maps the columns from the main file to the info file using a predefined dictionary.
4. Iterates through the rows of the main dataframe, finds the corresponding rows in the info dataframe, and updates the info dataframe with data from the main dataframe.
5. Sets the ‘Snapshot Date’, ‘Client Type’, and ‘Company Name’ columns to the desired values.
6. Converts the ‘loan_mifos_id’ column in ‘Penda_balances_df’ to the same data type as ‘Account Number’.
7. Merges the info dataframe with the ‘Penda_balances_df’ dataframe based on ‘Account Number’.
8. Multiplies the ‘Original Amount’, ‘Payment Amount’, and ‘Penda_loan_balance’ columns by 100.
9. Formats the ‘Current Balance’ column with leading zeros and the ‘Payment Date’ column to YYYYMMDD format.
10. Saves the updated data to an XLSX file, keeping only the original columns from the info file.
11. Displays a confirmation message after saving the updated data.
