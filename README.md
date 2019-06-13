# Financial Reporting Matrix

#### An improved matrix visual with advanced formatting

The Financial Reporting Matrix custom visual provides calculations and conditional formatting for matrix style reports. It provides a number of features not available in the standard matrix visual, including line formatting, conditional formatting, subtotals, and more. Custom calculated lines and custom format specifications can be defined directly in the data model. Configured via the standard fields and formatting pane. Particularly suited for financial reports.

## Features

- Subtotals
- Line formatting
- Cross-highlighting / Cross-filtering
- Multiple column headers / Pivoting
- Sticky column and row headers
- Conditional formatting
- Configure via fields and formatting pane
- Supports formatting and calculations in data model

For any questions about this visual, please send an e-mail to our team at support@profitbase.no.

## Usage

The Financial Reporting Matrix has 3 bucket fields.

1. Rows - Drag on the column that represents the report line.
2. Columns - Drag on the columns to pivot on.
3. Values - Drag on at least one measure.

To add subtotals or line formatting click the edit link in the upper right menu of the visual.

In edit mode right click on any row header to add a new report line or update the style on the current line or right click on any column header to add conditional formatting.

## The JSON structure for formatting and calculations in data model

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

## Supported styles

- bold
- underline
- overline
- custom1
- custom2
- custom3
- hidden - Has no configuration. Only hides the report line

The styles can be configured via the formatting pane
