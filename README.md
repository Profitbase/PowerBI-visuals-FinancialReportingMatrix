# Financial Reporting Matrix by Profitbase [![github releace](https://img.shields.io/github/release/Profitbase/PowerBI-visuals-FinancialReportingMatrix.svg)]

#### An improved matrix visual with advanced formatting

The Financial Reporting Matrix custom visual provides calculations and conditional formatting for matrix style reports. It provides a number of features not available in the standard matrix visual, including line formatting, conditional formatting, subtotals, and more. Custom calculated lines and custom format specifications can be defined directly in the data model. Configured via the standard fields and formatting pane. Particularly suited for financial reports.

![Income Statement](assets/Demo_Screenshot.PNG)

## Features

- Subtotals
- Line formatting
- Cross-highlighting / Cross-filtering
- Multiple column headers / Pivoting
- Sticky column and row headers
- Conditional formatting
- Configure via fields and formatting pane
- Supports formatting and calculations from the data model

For any questions about this visual, please send an e-mail to our team at support@profitbase.no.

## Getting started

### Video tutorial
[Demo - Create a basic income statement](https://youtu.be/MfbrkhQKSL4)

### Step-by-step guide

1. Install the Financial Reporting Matrix by Profitbase from AppSource.
2. Add your data source
3. Add the visual to the dashboard
4. Configure the bucket fields  
  1. Rows - Drag-drop the column(s) that represents the report line.
  2. Columns - Drag-drop the columns(s) to pivot on.
  3. Values - Drag-drop at least one measure.


#### Add subtotals
1. Click the edit link in the upper right menu of the visual.
2. Right click a row and select 'Add row'. This will add a (subtotal) row below the right-clicked row.
3. Provide a name.
4. Click the rows you want to include in the formula. By default, addition operators applied, but you can change this manually.

#### Add conditional formatting
1. Right click a column header and select 'Add conditional formatting'.
2. Using the editor that appears over the matrix, specify the rule and style to apply.
3. By default, the style 'custom 1' is selected. You can select a different style from the rule editor drop down.
4. From the 'Format' tool, modify the 'custom 1' style to meet your requirements.

## Calculations and formatting from the data model

```json
{
  "id": "L1Sum",
  "displayName": "1Sum - Reportline",
  "formula": "L10+L12+L13+L14+L15+L17+L19",
  "style": "bold overline",
  "formatString": "#,0",
  "signFactor": 1
}
```

- **id**: A short identifier for the report line.
- **displayName**: The description shown in the matrix.
- **formula**: The calculation to run on the report line. Use **id** references to other report lines. Simple mathematical formulas supported.
- **style**: A string of one or more styles to apply seperated with a space
- **formatString**: the format of how the values should be formatted.
- **signFactor**: the values on the reportline.
