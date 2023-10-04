# Patient_Timeline_Visualization
This project has been created using Python language. This project uses Dash Library. It gives summary of the patient when they enter their patient Id
generate_table Function:

This function takes two arguments: a DataFrame (dataframe) and an optional max_rows parameter (defaulting to 10).
It defines styles for the table, table header (th_style), and table data (td_style) using dictionaries.
It creates an HTML table structure using Dash's html.Table component.
Inside the table, it defines the table header (html.Thead) with table header cells (html.Th) for each column in the DataFrame.
It also creates the table body (html.Tbody) by iterating over rows in the DataFrame and generating table rows (html.Tr) with table data cells (html.Td).
The style parameter is used to apply the table_style to the entire table
DataFrame Manipulation:

Before defining the Dash layout,  some modifications to  DataFrame d have been made:
Removing the 'SNo' and 'Unnamed: 0' columns using d.drop('SNo', axis=1) and d.drop('Unnamed: 0', axis=1)
Dash Layout:

The Dash layout is defined as a hierarchy of components.
It starts with an html.Div containing several child components:
An html.H1 element for the main heading ("Timeline").
An html.H4 element for the subheading ("Summary").
The generate_table function is called to create and display the HTML table for the DataFrame d.
Running the Dash App:

Finally, the app is run using app.run_server() and the result is assigned to the variable b.
The print(b) statement is used to print the result of running the Dash app.
Overall, this code sets up a Dash web application with a table that displays data from the DataFrame d. The table is styled using CSS, and the layout includes headings and the table itself.
