# How-to-add-a-custom-view-to-a-hole-in-the-Blazor-doughnut-charts

This article explains how to add a custom view to a hole in Blazor doughnut chart.

**Adding custom view in doughnut chart using Annotations**

[Blazor chart](https://www.syncfusion.com/blazor-components/blazor-charts) provide the support to add custom view to a hole in doughnut chart. This can be achieved by using[Annotations](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.AccumulationChartAnnotation.html).

Annotations are texts, shapes, or images that are used to highlight a specific region of interest in a chart. The [AccumulationChartAnnotation](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.AccumulationChartAnnotation.html) property allows to add annotations to the chart. Specify the element that needs to be displayed in the accumulation chart area by using the [Content](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.AccumulationChartAnnotation.html#Syncfusion_Blazor_Charts_AccumulationChartAnnotation_Content) property of the annotation.

The following code example illustrate how to add an image link into the hole of doughnut chart.

**C#**

```cshtml

@using Syncfusion.Blazor.Charts

<SfAccumulationChart Title="Mobile Browser Statistics">

    <AccumulationChartSeriesCollection>
        <AccumulationChartSeries DataSource="@StatisticsDetails" XName="Browser" YName="Users" Name="Browser" InnerRadius="40%" Radius="200">
        </AccumulationChartSeries>
    </AccumulationChartSeriesCollection>

    <AccumulationChartLegendSettings Visible="false"></AccumulationChartLegendSettings>

    <AccumulationChartAnnotations>
        <AccumulationChartAnnotation Region="Regions.Series" X="43%" Y="43%">
            <ContentTemplate>
                <div id="back" style="visibility:visible; cursor:pointer;padding:3px;width:30px; height:30px;">                     
                    <img src="https://i.pinimg.com/564x/9a/31/96/9a31966df8f450c8df5435c8a064274f.jpg" alt="Girl in a jacket" width="80" height="80">
                </div>
            </ContentTemplate>
        </AccumulationChartAnnotation>
    </AccumulationChartAnnotations>

</SfAccumulationChart>
 
@code {

    public class Statistics
    {
        public string Browser { get; set; }
        public double Users { get; set; }
    }

    public List<Statistics> StatisticsDetails = new List<Statistics>
    {
        new Statistics { Browser = "Chrome", Users = 37 },
        new Statistics { Browser = "UC Browser", Users = 17 },
        new Statistics { Browser = "iPhone", Users = 19 },
        new Statistics { Browser = "Others", Users = 4  },
        new Statistics { Browser = "Opera", Users = 11 },
        new Statistics { Browser = "Android", Users = 12 },
    };
}
```


The following screenshot illustrate the output of the above code
snippet.

**Output:**

![](/custom-view-in-doughnut-hole.png) 
 
**Conclusion**

I hope you enjoyed learning how to add custom view inside the hole of doughnut of Blazor Chart Component.

You can refer to our [Blazor Chart feature tour](https://www.syncfusion.com/blazor-components/blazor-charts) page to know about its other groundbreaking feature representations and [documentation](https://blazor.syncfusion.com/documentation/chart/getting-started), and how to quickly get started for configuration specifications. You can also explore our [Blazor Chart example](https://blazor.syncfusion.com/demos/chart/line?theme=bootstrap5) to understand how to create and manipulate data.

For current customers, you can check out our components from the [License and Downloads](https://www.syncfusion.com/sales/teamlicense) page. If you are new to Syncfusion, you can try our 30-day [free trial](https://www.syncfusion.com/downloads/blazor) to check out our other controls.

If you have any queries or require clarifications, please let us know in the comments section below. You can also contact us through our [support forums](https://www.syncfusion.com/forums), [support portal](https://support.syncfusion.com/create), or [feedback portal](https://www.syncfusion.com/feedback/blazor-components?control=charts). We are always happy to assist you!