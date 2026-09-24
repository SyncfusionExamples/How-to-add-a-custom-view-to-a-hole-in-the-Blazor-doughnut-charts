# How to Add a Custom View Inside a Blazor Doughnut Chart Hole

## Overview

This sample demonstrates how to display custom HTML content inside the center hole of a Syncfusion [Blazor Charts](https://www.syncfusion.com/blazor-components/blazor-charts) doughnut chart. The implementation uses an accumulation chart configured as a doughnut chart and places an annotation within the series region to render custom UI content in the chart center.

By using chart annotations, developers can enrich doughnut charts with images, icons, KPI indicators, navigation controls, or other custom elements. This approach allows important contextual information to be displayed prominently without affecting the chart's underlying data visualization.

## Key Features

- Uses `SfAccumulationChart` to render an accumulation-based doughnut chart.
- Configures doughnut rendering through the `InnerRadius` property of `AccumulationChartSeries`.
- Binds data using:
  - `DataSource`
  - `XName`
  - `YName`
  - `Name`
- Sets the doughnut size with:
  - `InnerRadius`
  - `Radius`
- Hides the default legend using `AccumulationChartLegendSettings` with `Visible="false"`.
- Places custom content inside the doughnut hole using `AccumulationChartAnnotation`.
- Positions annotation content within the series area using:
  - `Region="Regions.Series"`
  - `X`
  - `Y`
- Renders custom HTML content through the annotation `ContentTemplate`.
- Demonstrates displaying an image inside the doughnut chart center.
- Uses a strongly typed data collection to populate browser usage statistics.

## Prerequisites

- [Visual Studio 2022](https://visualstudio.microsoft.com/vs/) or [Visual Studio Code](https://code.visualstudio.com/)
- [.NET SDK](https://dotnet.microsoft.com/en-us/download/dotnet) compatible with the project's target framework

## How to Run the Project

**Visual Studio 2022**

1. Clone or download this repository.
2. Open the project file:
   - `DoughnutView/DoughnutView.csproj`
3. Restore all NuGet packages.
4. Build the project.
5. Run the application using **Ctrl+F5**.

**Visual Studio Code**

1. Clone or download this repository.
2. Open the repository folder in Visual Studio Code.
3. Open the integrated terminal.
4. Navigate to the project directory:

```bash
cd DoughnutView
```

5. Restore NuGet packages:

```bash
dotnet restore
```

6. Run the application:

```bash
dotnet run
```

7. Open the URL shown in the terminal after the application starts.

## Project Structure

`DoughnutView/Pages/Index.razor` - Main sample page containing the `SfAccumulationChart`, doughnut chart series configuration, annotation definition, image template, and browser statistics data source.

## Support and Feedback

- For general product questions, visit the [Syncfusion Community Forum](https://www.syncfusion.com/forums) or [Syncfusion Support](https://www.syncfusion.com/support).
- To report an issue specific to this sample, open a GitHub issue in this repository.
- Official documentation for chart annotations: https://help.syncfusion.com/chart-sdk/blazor/accumulation-chart/annotation

## License

This is a Syncfusion sample project provided to demonstrate product usage. Review the [Syncfusion license terms](https://www.syncfusion.com/sales/pricing?category=ui-components) before using Syncfusion components in your own applications.