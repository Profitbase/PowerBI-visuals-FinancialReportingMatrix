# Financial Reporting Matrix by Profitbase

[![Get it from Microsoft AppSource](https://img.shields.io/badge/Microsoft_AppSource-Get_the_visual-0078D4?logo=microsoft&logoColor=white)](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA200000642?tab=Overview)
[![Latest GitHub release](https://img.shields.io/github/v/release/Profitbase/PowerBI-visuals-FinancialReportingMatrix?label=latest%20release)](https://github.com/Profitbase/PowerBI-visuals-FinancialReportingMatrix/releases)

**Build finance-ready Power BI reports with the calculation, layout, and formatting control that financial statements demand.**

Financial Reporting Matrix is a Power BI custom visual for income statements, balance sheets, cash flow statements, variance reports, and other structured financial reports.

[Get the visual](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA200000642?tab=Overview) · [Read the documentation](https://github.com/Profitbase/PowerBI-visuals-FinancialReportingMatrix/wiki) · [Watch the tutorials](https://github.com/Profitbase/PowerBI-visuals-FinancialReportingMatrix/wiki/Video-tutorials) · [View releases](https://github.com/Profitbase/PowerBI-visuals-FinancialReportingMatrix/releases)

![Example income statement built with Financial Reporting Matrix](assets/Demo_Screenshot.PNG)

## Why Financial Reporting Matrix?

Financial Reporting Matrix extends the standard Power BI matrix with the features needed to design and maintain polished financial reports:

| Capability | What you can do |
| --- | --- |
| **Structure financial statements** | Add [custom subtotal rows](https://docs.profitbase.com/articles/PowerBI/financial-reporting-matrix/custom-subtotals-rows.html), create [custom calculations](https://docs.profitbase.com/articles/PowerBI/financial-reporting-matrix/calculations.html), and place measures above columns or [display them as rows](https://docs.profitbase.com/articles/PowerBI/financial-reporting-matrix/measure-placement.html). |
| **Control the layout** | Expand and collapse [rows](https://docs.profitbase.com/articles/PowerBI/financial-reporting-matrix/row-expansion/row-expansion.html) and [columns](https://docs.profitbase.com/articles/PowerBI/financial-reporting-matrix/column-expansion/column-expansion.html), use [native drill-down](https://docs.profitbase.com/articles/PowerBI/financial-reporting-matrix/drill-down.html), sort hierarchies, and keep headers or [pinned columns](https://docs.profitbase.com/articles/PowerBI/financial-reporting-matrix/column-styling/pin-columns.html) visible while scrolling. |
| **Apply finance-specific formatting** | Style individual [rows](https://docs.profitbase.com/articles/PowerBI/financial-reporting-matrix/row-styles-appearance/customize-row-styles.html) and [columns](https://docs.profitbase.com/articles/PowerBI/financial-reporting-matrix/column-styling/individual-column-styles.html), apply [conditional formatting](https://docs.profitbase.com/articles/PowerBI/financial-reporting-matrix/formatting/conditional-formatting.html), set cell-level number formats, add [data bars](https://docs.profitbase.com/articles/PowerBI/financial-reporting-matrix/data-bars.html), and use report [themes](https://docs.profitbase.com/articles/PowerBI/financial-reporting-matrix/theming/theming.html). |
| **Work with Power BI** | Configure the visual through standard field wells and the Format pane, and use cross-filtering and cross-highlighting with other visuals. |
| **Export a presentation-ready workbook** | [Export to Excel](https://docs.profitbase.com/articles/PowerBI/financial-reporting-matrix/export-to-excel.html) with values, formatting, backgrounds, outlines, and grouped row hierarchies. |

Explore the [complete feature documentation](https://github.com/Profitbase/PowerBI-visuals-FinancialReportingMatrix/wiki).

## Get started

### 1. Install the visual

For most users, the recommended option is [Microsoft AppSource](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA200000642?tab=Overview).

| Source | Best for |
| --- | --- |
| [Microsoft AppSource](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA200000642?tab=Overview) | Standard production deployments |
| [Profitbase](https://www.profitbase.com/powerbi/) | The latest official package |
| [GitHub Releases](https://github.com/Profitbase/PowerBI-visuals-FinancialReportingMatrix/releases) | Evaluating fixes and features before they reach AppSource |

> [!IMPORTANT]
> Packages downloaded from Profitbase or GitHub should be registered by a Power BI administrator as an **Organizational visual**, then added from **Get more visuals → My organization**. See [Get the visual](https://github.com/Profitbase/PowerBI-visuals-FinancialReportingMatrix/wiki/Getting-the-visual) for deployment details.

### 2. Add data

Add Financial Reporting Matrix to a report page, then populate its field wells:

- **Rows:** Fields that define the report lines.
- **Columns:** Optional fields used to group or pivot the report.
- **Values:** At least one measure.

See [Adding data to the visual](https://docs.profitbase.com/articles/PowerBI/financial-reporting-matrix/adding-data-to-the-visual.html) for a detailed walkthrough.

### 3. Design the report

Use the Power BI Format pane for visual-wide settings. Open the visual's edit mode and contextual editors to configure individual rows, columns, calculations, and formatting rules.

Popular workflows:

- [Create custom subtotal rows](https://docs.profitbase.com/articles/PowerBI/financial-reporting-matrix/custom-subtotals-rows.html)
- [Add custom columns and calculations](https://docs.profitbase.com/articles/PowerBI/financial-reporting-matrix/calculations.html)
- [Apply conditional formatting](https://docs.profitbase.com/articles/PowerBI/financial-reporting-matrix/formatting/conditional-formatting.html)
- [Export the report to Excel](https://docs.profitbase.com/articles/PowerBI/financial-reporting-matrix/export-to-excel.html)

## Model-driven calculations and formatting

For advanced scenarios, Financial Reporting Matrix can read formulas, formats, and styles from the data model. This lets you manage report behavior as data instead of configuring every visual manually.

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

| Property | Purpose |
| --- | --- |
| `id` | Identifies the report line so formulas can reference it. |
| `displayName` | Sets the label displayed in the matrix. |
| `formula` | Calculates the report line using other line IDs. |
| `style` | Applies one or more space-separated styles. |
| `formatString` | Controls numeric display formatting. |
| `signFactor` | Adjusts the sign of the report line's values. |

Learn more about [calculations](https://docs.profitbase.com/articles/PowerBI/financial-reporting-matrix/calculations.html) and [cell-level formatting](https://docs.profitbase.com/articles/PowerBI/financial-reporting-matrix/formatting/cell-formatting-using-format-function.html).

## Licensing

Some capabilities require a paid license. See [Premium features](https://github.com/Profitbase/PowerBI-visuals-FinancialReportingMatrix/wiki/Premium-Features-%E2%80%90-Financial-Reporting-Matrix) and [license setup](https://github.com/Profitbase/PowerBI-visuals-FinancialReportingMatrix/wiki/Use-Premium-features) for current details, including Enterprise and Power BI Embedded deployments.

## Releases

AppSource updates go through Microsoft's submission and validation process, so fixes and new functionality may appear on [GitHub Releases](https://github.com/Profitbase/PowerBI-visuals-FinancialReportingMatrix/releases) first.

Before using a package from outside AppSource in production, confirm that your organization permits custom visual packages and follow the Organizational visual deployment process described above.

## Documentation and support

- [Documentation](https://github.com/Profitbase/PowerBI-visuals-FinancialReportingMatrix/wiki) — setup, feature guides, and reference material
- [Video tutorials](https://github.com/Profitbase/PowerBI-visuals-FinancialReportingMatrix/wiki/Video-tutorials) — guided walkthroughs
- [Discussions](https://github.com/Profitbase/PowerBI-visuals-FinancialReportingMatrix/discussions) — questions, feedback, and feature requests
- [Issues](https://github.com/Profitbase/PowerBI-visuals-FinancialReportingMatrix/issues) — reproducible bugs and technical problems

When reporting a problem, include the Financial Reporting Matrix version, Power BI version, steps to reproduce, and any relevant screenshots or sample data.
