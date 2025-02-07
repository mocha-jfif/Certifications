Send custom and detailed reports in a few easy steps to summarize health, performance, resource utilization, and much more.

1. Select a scope for the report.
2. Email it to the desired client.
3. Download the report at any time if required.

## Report Templates

VSA 10 offers out-of-the-box templates for you to get started with the reporting functionality.

These templates can be found by navigating to the **Reporting** modules and selecting **Templates**.

Review the table below to learn how templates can help to gain visibility on health, performance, resource utilization, and more.

| **Template**          | **Description**                                                                |
| --------------------- | ------------------------------------------------------------------------------ |
| Applications          | A report that displays all the applications installed on the selected systems. |
| Assets                | A report that displays all the assets for the selected systems.                |
| Assets Overview       | A report that displays an overview of all assets.                              |
| CPU Usage             | A report that displays CPU usage for all selected systems.                     |
| Custom Fields         | A report that displays user-selected custom field values.                      |
| Drive Usage           | A report that displays the drive usage for all selected systems.               |
| Executive             | A report that displays a detailed overall status of all selected systems.      |
| Executive Summary     | A report that displays the overall status of all selected systems.             |
| IP Summary            | A report that displays the IPs for all selected systems.                       |
| Memory Usage          | A report that displays the memory usage for all selected systems.              |
| Network Usage         | A report that displays network usage for the selected systems.                 |
| Patching              | A report that displays information about patching.                             |
| Task Execution Output | A report that displays the task execution output.                              |
| VSA X Antivirus       | A report that displays a detailed antivirus status of all selected systems.    |

### How to Create a Report
Login to the VSA 10 WebApp and under the **Reporting** section, select the **Templates** menu entry.

Select a template from the list and then click on the **Create Report** button.

Enter a report name, select a system scope, and configure the notification options.


### Scheduling Report Execution
To schedule the report execution, click on **Enable Scheduling** to open the **Schedule** dialog, 

Select the occurrence, days of the week, and start time then select the **Save** button to save the schedule.

## Advanced Reporting

**Categories**: Help organize reports and dashboards and make navigation easier. You can assign a category to a report. You can add a personal category and use it along with the built-in categories.

**Documents**: Documents are report templates with predefined page layouts, styles, and fonts. They are used to avoid the repetitive recreation of reports having the same structure or format.

**Actions**: You can perform the typical actions on a template. For instance, you can duplicate an existing built-in template and edit the duplicate.

**Favorites**: This tab contains all your favorite marked templates in one place. You can add a template to your Favorites by selecting any template, then clicking on the star.

## Report Viewer

The **Report Viewer** has numerous built-in features to help you get the most out of this advanced reporting functionality.

The Report Viewer has numerous built-in features that enable you to:

- Print or export a report
- Zoom in or out of a report
- Search for any text or numbers
- Navigate between the report pages 

The report viewing experience has been pleasing as you can add parameters, filters, and prompts to the reports. 

It allows you to select data from a pre-defined list so that you can view the relevant details at a time.

Suiting your requirements, Advanced Reporting offers you plenty of export formats for your reports:

- PDF
- Excel
- Word
- CSV
- HTML
- Image
- JSON

**Schedule**: Once you create a task, the result of the report is automatically generated at the specified time or interval in the chosen file format. You can share the result by sending an email to the designated email address, storing it on the system server, or keeping the result at a shared location.

**New Templates**: You can quickly create meaningful reports with a lot of ease.  The existing report templates can be used to build these. Once a new **Document** (template) is created and saved, it is displayed in the **Categories** tab.

## Connect a Report and a Dataset

With the help of the Data panel, you can connect your report to the desired dataset. 

The Data panel categorizes the data sources into:

- Server
- New Based on Model Entity
- New Based on server Data Source

![[Pasted image 20250109124059.png]]

### To Bind a Dataset to a Report

Method 1: Using Server
- Consider a scenario where you want to use a dataset already available in VSA 10. Such a dataset type is extremely useful for non-technical users since configuring the dataset requires no SQL queries, parameters, or other related data options.
	- In the Report Designer, go to the Data panel and click Add.
	- Select a suitable dataset listed under the Server category such as 'Customer Orders', and then click the Add button.
	- The 'CustomerOrders' dataset is now added to your report.

Method 2: Using New Based on Model Entity
- Let's suppose, you want to create an ad hoc report for real-time data visualization and exploration. This is only possible when you bind a report to a model entity. A data model helps to transform the technical data structures from database tables and views into real-world entities, attributes, and relationships. It also helps to improve the readability of the data. 
	- In the Report Designer, go to the Data panel and click Add.
	- Select a suitable model listed under the New Based on Model Entity category such as 'ActiveTunes'. A list of available entities in the model is displayed on selection.
	- From the list, choose a model entity, say 'Customer', and then click the Add button to proceed further.
	- You can duplicate the datasets which are based on the Semantic model.

Method 3: Using New Based on Server Data Source
- Let's say, you want to fetch data from a data source to be used only in one report.  Apart from this, you want to configure its related data options such as fields, parameters, and filters to display only the required information in the report. 
	- In the Report Designer, go to the Data panel and click Add.
	- Select a suitable dataset listed under the New Based on Server Data Source category such as 'Customer Orders', and then click the Add button.
	- In the Edit Data Set dialog that appears, provide the query, field, and other settings for the chosen dataset as shown in the next steps.
	- Enter the name of the dataset in the Name field such as 'CustomerOrdersDataset'. By default, this field is set to 'Dataset1'. Note that the dataset name should not contain any empty spaces or special characters ('-', '/', '@', etc).
	- In the Query field, write an SQL query to extract the data from the data source.
	- Click the Validate button to verify the SQL statement.
	- If the SQL query is successfully validated, you will see a count of queried fields against the Bound Fields field.
	- Click the Show Items button to view the entire list of bound fields in the dataset. Here, field names are the names given to the fields in a dataset, while the data fields are the original names of the fields in the database, which should not be modified or renamed.
	- By default, field names show the same names as the data fields. You can modify a field name by simply replacing its old name with the new name as shown below. 
	- To delete a field, click the Delete icon adjacent to the field name in the list. Note that, deleting a field here will not affect the actual data stored in the data source.
	- Add a calculated field in the dataset to create a new field by applying some calculations to the existing data. You can add a calculated field using the Add button. For example, in the below dialog, we have created a new calculated field 'Total Price' to determine the total product cost for a customer.
	- In the Parameters field, you can add report parameters and then use the 'where' clause in the SQL query to filter the data. For example, create a parameter namely 'Country' and set its value to 'Canada', and then update the SQL statement accordingly to filter the data based on the parameter value as shown.
	- To display only relevant data in the report, use filtering in the dataset. The Filters field is especially useful when you have a data source like XML that does not support query parameters.
	- Finally, click the Validate button to verify the dataset definition, and then the OK button to proceed further. The dataset is now added to the report.
	- You can duplicate the datasets which are based on the embedded data source. Below is an example of the dataset based on the embedded data source. Click the duplicate option to duplicate the datasets.

**Edit a Dataset**: Modify the existing details for a dataset by changing its name, parameter, value(s), field name(s), filter value(s), and so on.

**Delete a Dataset**: Removes the bound dataset from the report.


## The Report Designer

The report designer gives users the ability to create a new report or edit an existing report, without writing any code. 

The designed reports can then be exported to any format or printed from the preview window.

**Report Toolbox**: Contains report explorer, group editor, and report controls that assist in designing reports.
- Report Explorer: Provides an overview of the hierarchy of added report items. It displays the current selection and allows the selection of other report items.
- Group Editor: Shows Column and Row hierarchies of Tablix members for currently selected Tablix or Table data region.
- Report Controls: Includes all the available controls for designing a report, such as textbox, container, line, shape, table of contents, image, list, table, chart, barcode, etc.

**Menu Bar**: Contains options to undo or redo an action, save a report, preview a report, format a report, and design a custom parameter panel.
- Undo: Undo an action in the designer.
- Redo: Redo an action in the designer.
- Save: Save a report in the designer.
- Preview: Preview a report in the designer.
- Home: Consists of commonly used report editing and text formatting operations such as cut, copy, paste, font, font size, font color, and horizontal and vertical text alignments. Note that these operations are specific to a report control.
- Report: Contains options to add, delete, or move pages (in Page Report), add or remove header and footer (RDL report), and change report themes.
- Parameters: Contains the design area for designing a custom parameter panel. The controls make the panel have default properties set like name, label, default value, etc.

**Properties and Data Panels**: Access and modify the properties of a report or manage data connection using these panels
- Properties: Displays the properties of the selected report control in the design area. If more than one control is selected, the panel displays their common properties.
- Data: Contains options to add datasets, parameters, and common values.
    - Data sets: Displays the datasets available for designing a report. See Data Binding topic for more information.
    - Parameters: Allows you to add and modify report parameters.
    - Common Values: Displays common values such as current date and time, page number, total pages, page N of M, report name, user ID, and user language, to use in your reports.

**Design Area**: Create and edit reports by simply dragging and dropping the report controls from the toolbox into the design area.

**Other Settings**: Set zoom percentage, switch between advanced or basic property mode, specify grid settings, and more.
- Grid: Show or hide grid lines in the design area.
- Snap: Enable or disable report controls to snap to grids and guides when you drag them into the design area. You can also specify the size of the grid lines.
- Zoom: Set the zoom percentage of the design area by clicking the zoom-in and zoom-out buttons.
- Grid Unit: Switch to the measurement unit for the grid lines to 'centimeters'. By default, the grid unit is set to 'inches'.
- Properties Mode: Switch to advanced or basic properties mode. By default, basic properties mode is selected.


### Report Controls

The Toolbox in VSA 10's Report Designer offers several report controls and data regions that you use to create a report. 

You can drag these from the toolbox and drop them onto your reports. Each report control in the toolbox has its own sets of pre-defined settings which you can customize as per your requirements.

**The Textbox**: Textbox control is the most extensively used report control by the users. It is an input box that can be used to write any text in a report or display any textual data. 
- For example, you can use a textbox to write the title of the report or to display any data. 
- By default, all the cells of the Table and Tablix report control have textboxes. Also, when you drag and drop the fields from a dataset onto the report designer, text boxes are created automatically. You can edit and format the text in the textbox as well.
- You can also use expressions in the textbox. Right-click on the textbox and select the option **Expression**.
- Binding data to a textbox
	- Method 1:
		- From the Report Toolbox on the left, drag and drop the TextBox control onto the design area.
		- Select the textbox and from the fields selection adorner  , select a field from the list. If a numeric field is selected, then by default the Sum of the numeric field is taken. If the field selected is non-numeric, then the count of the field is taken. In the image below, we have taken two textboxes, one has a numeric field and another has a non-numeric field.
	- Method 2:
		- From the **Report Toolbox** on the left, drag and drop the **TextBox** control onto the design area.
		- From the **Data Binding** tab on the right, expand the dataset and drag-drop the desired field(s) onto the textbox.
	- Method 3:
		- From the **Data** tab on the right, click the **Select Fields** button next to the bound dataset and select the desired fields.
		- Drag-drop the selected fields onto the design area. A table with its column bound to the fields is created and the cells in the table have a textbox.
		- You can double-click in the table cell and the textbox will become editable and you can edit the font, size, color, etc. of the text.

## Tables

By default, a table has three columns and three rows, a total of nine cells, where each cell is filled with a text box. 

In a table, you can sort and filter the bound data, display a total row at the end of a table, merge rows and columns, freeze to keep certain rows and columns visible when scrolling the table, and more.

|Component|Function|
|---|---|
|Header Row|By default, a table has a header row that appears at the top of the table. It is typically used to label each column or add a header to the table. A table can have several header rows.|
|Group Header Row|Appears at the beginning of each group in the table. You can use a group header row to display the group's field value or summary value. A group can have several header rows.|
|Details Row|Repeats for each record in the bound dataset. If the details row is inside the row group, it will repeat once for each unique value of the group. A table can have more than one details row. Note that the details group is the innermost child group.|
|Group Footer Row|Appears at the end of each group in a table. You could use the group footer row to display the summary values. A group can have several footer rows.|
|Footer Row|By default, a table has a footer row that appears at the end of the table. You could use the footer rows to display grand totals or notes. A table can have several footer rows.|
|Row and Column Handlers|Use to add rows and columns to the table. Note that the added row can be a header row, details row, or footer row.|

VSA 10 supports interactive features like parameters, drill-down, filters, links, sorting, and document map.

With styles, you can enhance the appearance of report controls such as tables and charts, and with themes, you can enhance the overall appearance of your reports.

**To Apply Style to a Table**

1. Select the Table data region.
    
2. Go to the LAYOUT - Style property in the Properties pane.
    
3. Select a Style, say, Light Style 1 Accent 5, from the drop-down.
    
4. Preview the report.

**To Apply Theme to a Report**

1. Select Report from the ribbon menu at the top of the design area.
2. Click Switch Theme.
3. Select a theme, say, Cordial, or set the LAYOUT - Theme property of the report in the Properties pane. You can also pass expressions to display the report theme based on the organization or user context values, or the parameter values. Refer Using Expressions in Report Themes below for more details.
    
4. To preview the report with, click the Preview button on the top left side of your screen. Notice that, all the text content including No Data Content inherits the font and color of the applied theme.
