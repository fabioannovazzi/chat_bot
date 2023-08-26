##### Choose Column Separator and Load File

Your uploaded file (max 200 MB) needs be either an Excel file or a CSV file with UTF 8 encoding. 

The file name should not contain the "." (dot) character. For instance, if you file is called "test_07.01.2021.xlsx", rename it as something like "test_07_01_2021.xlsx.

 If it is an  Excel file, the sheet with your data must be the first sheet of the Excel workbook. If it is a  CSV file, the column separator must be either comma or semicolon. You need to specify the separator.

An Excel file is more straightforward to load compared to a CSV file. You do not have to worry about the UFT-8 encoding and, often, about the "number" encoding of the metric columns. However, very large datasets seem to take more time to load if they are in Excel format, and it might make sense to convert them into CSV format. 

There are three ways to save your Excel file as a CSV with UTF-8 encoding .

With Excel:

- Open your file in Excel and save as "CSV UTF-8 (Comma or Semicolon delimited)".

If this option is not available, still with Excel:

- Open your file in Excel and save as CSV (Comma or Semicolon delimited).
- Scroll down and choose **Tools**.
- Choose **Web Options** from the **Tools** drop-down menu.
- Select the **Encoding** tab
- Choose UTF-8 from the **Save this document as**: drop down menu
- Select **OK**.

if the above does not work, with Notepad:

- Open the file with Notepad
- File => Save As
- Encoding choose "UTF-8"
- Save

Now your file is saved as a UTF-8 encoded CSV file.