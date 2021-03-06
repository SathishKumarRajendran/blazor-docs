# Pointers

Pointers are used to indicate values on an axis. The value of a pointer can be modified using the [`Value`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.CircularGauge.CircularGaugePointer.html#Syncfusion_Blazor_CircularGauge_CircularGaugePointer_Value) property.

```csharp
@using Syncfusion.Blazor.CircularGauge

<SfCircularGauge>
    <CircularGaugeAxes>
        <CircularGaugeAxis>
            <CircularGaugePointers>
                <CircularGaugePointer Value="90">
                </CircularGaugePointer>
            </CircularGaugePointers>
        </CircularGaugeAxis>
    </CircularGaugeAxes>
</SfCircularGauge>
```

![Circular Gauge with pointer](./images/pointer.png)

The Circular Gauge supports three types of pointers such as [`Needle`](https://help.syncfusion.com/cr/aspnetcore-blazor/Syncfusion.Blazor.CircularGauge.PointerType.html), [`RangeBar`](https://help.syncfusion.com/cr/aspnetcore-blazor/Syncfusion.Blazor.CircularGauge.PointerType.html), and [`Marker`](https://help.syncfusion.com/cr/aspnetcore-blazor/Syncfusion.Blazor.CircularGauge.PointerType.html). You can choose any pointer using the [`Type`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.CircularGauge.CircularGaugePointer.html#Syncfusion_Blazor_CircularGauge_CircularGaugePointer_Type) property.

## Needle pointer

The circular gauge's default pointer type will be needle. A needle point contains three parts, a needle, a cap / knob, and a tail.

```csharp
@using Syncfusion.Blazor.CircularGauge

<SfCircularGauge>
    <CircularGaugeAxes>
        <CircularGaugeAxis>
            <CircularGaugePointers>
                <CircularGaugePointer Value="90">
                </CircularGaugePointer>
            </CircularGaugePointers>
        </CircularGaugeAxis>
    </CircularGaugeAxes>
</SfCircularGauge>
```

![Circular Gauge with needle pointer](./images/needle-pointer.png)

### Customization

The needle, tail and cap of the pointer can be customized with the following properties.

* [`CircularGaugePointer`](https://help.syncfusion.com/cr/aspnetcore-blazor/Syncfusion.Blazor.CircularGauge.CircularGaugePointer.html) - Customize the pointer's needle.
    * [`Radius`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.CircularGauge.CircularGaugePointer.html#Syncfusion_Blazor_CircularGauge_CircularGaugePointer_Radius) - sets the needle length
    * [`PointerWidth`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.CircularGauge.CircularGaugePointer.html#Syncfusion_Blazor_CircularGauge_CircularGaugePointer_PointerWidth) - sets the needle width
    * [`Color`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.CircularGauge.CircularGaugePointer.html#Syncfusion_Blazor_CircularGauge_CircularGaugePointer_Color) - sets the needle color
* [`CircularGaugeNeedleTail`](https://help.syncfusion.com/cr/aspnetcore-blazor/Syncfusion.Blazor.CircularGauge.CircularGaugeNeedleTail.html) -  Customize the pointer's tail.
    * [`Length`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.CircularGauge.CircularGaugeNeedleTail.html#Syncfusion_Blazor_CircularGauge_CircularGaugeNeedleTail_Length) - sets pointer's tail length
    * [`Color`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.CircularGauge.CircularGaugeNeedleTail.html#Syncfusion_Blazor_CircularGauge_CircularGaugeNeedleTail_Color) - sets pointer's tail color
    * [`CircularGaugeNeedleTailBorder`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.CircularGauge.CircularGaugeNeedleTail.html#Syncfusion_Blazor_CircularGauge_CircularGaugeNeedleTail_Border) -  Sets pointer's tail border
* [`CircularGaugeCap`](https://help.syncfusion.com/cr/aspnetcore-blazor/Syncfusion.Blazor.CircularGauge.CircularGaugeCap.html) -  Customize the pointer's cap.
    * [`Color`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.CircularGauge.CircularGaugeCap.html#Syncfusion_Blazor_CircularGauge_CircularGaugeCap_Color) - sets pointer's cap color
    * [`Radius`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.CircularGauge.CircularGaugeCap.html#Syncfusion_Blazor_CircularGauge_CircularGaugeCap_Radius) - sets pointer's cap radius
    * [`CircularGaugeCapBorder`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.CircularGauge.CircularGaugeCap.html#Syncfusion_Blazor_CircularGauge_CircularGaugeCap_Border) - sets pointer's cap border
    * [`Position`] - specifies the position of the Pointer. Its possible values are 'PointerRangePosition.Inside', 'PointerRangePosition.Outside' and 'PointerRangePosition.Cross'.

```csharp
@using Syncfusion.Blazor.CircularGauge

<SfCircularGauge Height="250px" Width="250px">
    <CircularGaugeAxes>
        <CircularGaugeAxis>
            <CircularGaugePointers>
                <CircularGaugePointer Value="90"
                                      Radius="40%"
                                      PointerWidth="30"
                                      Color="#007DD1"
                                      Position="PointerRangePosition.Inside">
                    <CircularGaugeCap Radius="15"
                                      Color="white">
                        <CircularGaugeCapBorder Width="4"
                                                Color="#007DD1">
                        </CircularGaugeCapBorder>
                    </CircularGaugeCap>
                    <CircularGaugeNeedleTail Length="35%"
                                             Color="#007DD1">
                    </CircularGaugeNeedleTail>
                </CircularGaugePointer>
            </CircularGaugePointers>
        </CircularGaugeAxis>
    </CircularGaugeAxes>
</SfCircularGauge>
```

![Circular Gauge with custom pointer](./images/customs.png)

<!-- markdownlint-disable MD010 -->

The appearance of the needle pointer can be customized by using [`NeedleStartWidth`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.CircularGauge.CircularGaugePointer.html#Syncfusion_Blazor_CircularGauge_CircularGaugePointer_NeedleStartWidth) and [`NeedleEndWidth`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.CircularGauge.CircularGaugePointer.html#Syncfusion_Blazor_CircularGauge_CircularGaugePointer_NeedleEndWidth).

```csharp
@using Syncfusion.Blazor.CircularGauge

<SfCircularGauge>
    <CircularGaugeAxes>
        <CircularGaugeAxis StartAngle="270" EndAngle="90" Radius="90%" Minimum="0" Maximum="100">
		<CircularGaugeAxisLineStyle Width="3" Color="#1E7145">
            </CircularGaugeAxisLineStyle>
			 <CircularGaugeAxisLabelStyle>
                <CircularGaugeAxisLabelFont Color="#1E7145" Size="0px">
                </CircularGaugeAxisLabelFont>
            </CircularGaugeAxisLabelStyle>
			<CircularGaugeAxisMajorTicks Interval="100"
                                         Height="0"
                                         Width="1">
            </CircularGaugeAxisMajorTicks>
            <CircularGaugeAxisMinorTicks Width="0"
                                         Height="0"
                                         >
            </CircularGaugeAxisMinorTicks>
            <CircularGaugePointers>
                <CircularGaugePointer Value="70"
                                      Radius="80%" Color="green" PointerWidth="2" NeedleStartWidth="4" NeedleEndWidth="4">
				 <CircularGaugeCap Radius="8" Color="green">
                    </CircularGaugeCap>
                    <CircularGaugeNeedleTail Length="0%">
                    </CircularGaugeNeedleTail>
                </CircularGaugePointer>
            </CircularGaugePointers>
			<CircularGaugeAnnotations>
                <CircularGaugeAnnotation Angle="180" ZIndex="1">
                    <ContentTemplate>
                        <div class="custom-annotation">Customized Needle</div>
                    </ContentTemplate>
                </CircularGaugeAnnotation>
            </CircularGaugeAnnotations>
        </CircularGaugeAxis>
    </CircularGaugeAxes>
</SfCircularGauge>
<style type="text/css">
    .custom-annotation {
        color: #757575;
        font-family:Roboto; font-size:14px;padding-top: 26px;
    }
</style>
```

## Range bar pointer

The range bar pointer is like a range in an axis that can be placed on gauge to mark the pointer value. The
range bar starts from the beginning of the gauge and ends at the pointer value. You can set the pointer type using `Type` property in `CircularGaugePointer`.

```csharp
@using Syncfusion.Blazor.CircularGauge

<SfCircularGauge>
    <CircularGaugeAxes>
        <CircularGaugeAxis>
            <CircularGaugePointers>
                <CircularGaugePointer Value="50"
                                      Type="PointerType.RangeBar">
                </CircularGaugePointer>
            </CircularGaugePointers>
        </CircularGaugeAxis>
    </CircularGaugeAxes>
</SfCircularGauge>
```

![Circular Gauge with range pointer](./images/rangebars.png)

### Customization

You can customize the range bar using the following properties.

* [`PointerWidth`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.CircularGauge.CircularGaugePointer.html#Syncfusion_Blazor_CircularGauge_CircularGaugePointer_PointerWidth) - Specifies the width of the range bar
* [`Color`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.CircularGauge.CircularGaugePointer.html#Syncfusion_Blazor_CircularGauge_CircularGaugePointer_Color) - Specifies the color of the range bar
* [`Radius`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.CircularGauge.CircularGaugePointer.html#Syncfusion_Blazor_CircularGauge_CircularGaugePointer_Radius) - Specifies the range bar radius
* [`RoundedCornerRadius`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.CircularGauge.CircularGaugePointer.html#Syncfusion_Blazor_CircularGauge_CircularGaugePointer_RoundedCornerRadius) - Specifies the rounded corner of the range bar
* [`CircularGaugePointerBorder`](https://help.syncfusion.com/cr/aspnetcore-blazor/Syncfusion.Blazor.CircularGauge.CircularGaugePointerBorder.html) - Specifies the border of the range bar

```csharp
@using Syncfusion.Blazor.CircularGauge

<SfCircularGauge>
    <CircularGaugeAxes>
        <CircularGaugeAxis>
            <CircularGaugePointers>
                <CircularGaugePointer Value="46"
                                      Type="PointerType.RangeBar"
                                      PointerWidth="8"
                                      Radius="95%"
                                      Color="lightgray">
                    <CircularGaugePointerBorder Color="darkgray"
                                                Width="2">
                    </CircularGaugePointerBorder>
                </CircularGaugePointer>
            </CircularGaugePointers>
        </CircularGaugeAxis>
    </CircularGaugeAxes>
</SfCircularGauge>
```

![Circular Gauge with custom range bar](./images/range-customs.png)

### Rounded corners

The start and end pointers of a range bar in the Circular Gauge are rounded to form arc using `RoundedCornerRadius` property.

```csharp
@using Syncfusion.Blazor.CircularGauge

<SfCircularGauge>
    <CircularGaugeAxes>
        <CircularGaugeAxis>
            <CircularGaugePointers>
                <CircularGaugePointer Value="46"
                                      RoundedCornerRadius="20"
                                      Type="PointerType.RangeBar">
                </CircularGaugePointer>
            </CircularGaugePointers>
        </CircularGaugeAxis>
    </CircularGaugeAxes>
</SfCircularGauge>
```

![Circular Gauge range bar with rounded corner](./images/range-round.png)

## Marker pointer

The different types of marker shapes can be used to mark the pointer value in an axis. You can change the marker shape using the [`MarkerShape`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.CircularGauge.CircularGaugePointer.html#Syncfusion_Blazor_CircularGauge_CircularGaugePointer_MarkerShape) property in pointer. The Circular Gauge supports the following marker shapes:
* Circle
* Rectangle
* Triangle
* InvertedTriangle
* Diamond

```csharp
@using Syncfusion.Blazor.CircularGauge

<SfCircularGauge>
    <CircularGaugeAxes>
        <CircularGaugeAxis>
            <CircularGaugePointers>
                <CircularGaugePointer Value="90"
                                      Type="PointerType.Marker"
                                      MarkerShape="GaugeShape.Diamond"
                                      MarkerHeight="15"
                                      MarkerWidth="15">
                </CircularGaugePointer>
            </CircularGaugePointers>
        </CircularGaugeAxis>
    </CircularGaugeAxes>
</SfCircularGauge>
```

![Circular Gauge with custom marker pointer](./images/InvertedTriangle.png)

### Customization

You can customize the marker pointer using the following properties.

* [`Color`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.CircularGauge.CircularGaugePointer.html#Syncfusion_Blazor_CircularGauge_CircularGaugePointer_Color) - specifies marker pointer color
* [`MarkerWidth`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.CircularGauge.CircularGaugePointer.html#Syncfusion_Blazor_CircularGauge_CircularGaugePointer_MarkerWidth)  - specifies marker pointer width
* [`MarkerHeight`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.CircularGauge.CircularGaugePointer.html#Syncfusion_Blazor_CircularGauge_CircularGaugePointer_MarkerHeight) - specifies marker pointer height
* [`Radius`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.CircularGauge.CircularGaugePointer.html#Syncfusion_Blazor_CircularGauge_CircularGaugePointer_Radius) - specifies marker pointer radius
* [`CircularGaugePointerBorder`](https://help.syncfusion.com/cr/aspnetcore-blazor/Syncfusion.Blazor.CircularGauge.CircularGaugePointerBorder.html) - specifies marker pointer's border color and width.

```csharp
@using Syncfusion.Blazor.CircularGauge

<SfCircularGauge>
    <CircularGaugeAxes>
        <CircularGaugeAxis>
            <CircularGaugePointers>
                <CircularGaugePointer Value="90"
                                      Type="PointerType.Marker"
                                      MarkerShape="GaugeShape.InvertedTriangle"
                                      MarkerHeight="15"
                                      MarkerWidth="15"
                                      Color="white"
                                      Radius="110%">
                    <CircularGaugePointerBorder Width="2" Color="#007DD1"></CircularGaugePointerBorder>
                </CircularGaugePointer>
            </CircularGaugePointers>
        </CircularGaugeAxis>
    </CircularGaugeAxes>
</SfCircularGauge>
```

![Circular Gauge with custom marker pointer](./images/Triangle.png)

### Image marker pointer

You can use image instead of rendering marker shape to denote the pointer value. It can be achieved by setting [`MarkerShape`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.CircularGauge.CircularGaugePointer.html#Syncfusion_Blazor_CircularGauge_CircularGaugePointer_MarkerShape) to 'GaugeShape.Image' and assigning image path to [`ImageUrl`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.CircularGauge.CircularGaugePointer.html#Syncfusion_Blazor_CircularGauge_CircularGaugePointer_ImageUrl) as shown in following example.

```csharp
@using Syncfusion.Blazor.CircularGauge

<SfCircularGauge>
    <CircularGaugeAxes>
        <CircularGaugeAxis>
            <CircularGaugePointers>
                <CircularGaugePointer Value="90"
                                      Type="PointerType.Marker"
                                      MarkerShape="GaugeShape.Image"
                                      ImageUrl="football.png"
                                      MarkerHeight="20"
                                      MarkerWidth="20"
                                      Radius="100%">
                </CircularGaugePointer>
            </CircularGaugePointers>
        </CircularGaugeAxis>
    </CircularGaugeAxes>
</SfCircularGauge>
```

![Circular gauge with image pointer](./images/pointer-with-image.png)

<!-- markdownlint-disable MD010 -->

## Dragging pointer

The pointers can be dragged over the axis values by clicking and dragging the same. To enable or disable the pointer drag, use the
[`EnablePointerDrag`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.CircularGauge.SfCircularGauge.html#Syncfusion_Blazor_CircularGauge_SfCircularGauge_EnablePointerDrag) property.

```csharp
@using Syncfusion.Blazor.CircularGauge

<SfCircularGauge EnablePointerDrag="true" Height="250px" Width="250px">
    <CircularGaugeAxes>
        <CircularGaugeAxis>
            <CircularGaugePointers>
                <CircularGaugePointer Value="50">
                </CircularGaugePointer>
            </CircularGaugePointers>
        </CircularGaugeAxis>
    </CircularGaugeAxes>
</SfCircularGauge>
```

![Circular Gauge with pointer drag](./images/drag-pointr.gif)

## Multiple pointers

In addition to the default pointer, you can add n number of pointers to an axis using the [`CircularGaugePointers`](https://help.syncfusion.com/cr/aspnetcore-blazor/Syncfusion.Blazor.CircularGauge.CircularGaugePointers.html) tag.

```csharp
@using Syncfusion.Blazor.CircularGauge

<SfCircularGauge>
    <CircularGaugeAxes>
        <CircularGaugeAxis>
            <CircularGaugePointers>
                <CircularGaugePointer Value="90"
                                      MarkerShape="GaugeShape.InvertedTriangle"
                                      Radius="100%"
                                      MarkerHeight="15"
                                      MarkerWidth="15">
                </CircularGaugePointer>
                <CircularGaugePointer Value="90"
                                      Type="PointerType.RangeBar"
                                      Radius="60%"
                                      MarkerWidth="10">
                </CircularGaugePointer>
                <CircularGaugePointer Value="90"
                                      Radius="50%"
                                      PointerWidth="25"
                                      Color="#007DD1">
                    <CircularGaugeCap Radius="15">
                        <CircularGaugeCapBorder Width="5">
                        </CircularGaugeCapBorder>
                    </CircularGaugeCap>
                    <CircularGaugeNeedleTail Length="25%">
                    </CircularGaugeNeedleTail>
                </CircularGaugePointer>
            </CircularGaugePointers>
            <CircularGaugeAxisLabelStyle UseRangeColor="true">
            </CircularGaugeAxisLabelStyle>
            <CircularGaugeAxisMinorTicks UseRangeColor="true"></CircularGaugeAxisMinorTicks>
        </CircularGaugeAxis>
    </CircularGaugeAxes>
</SfCircularGauge>
```

![Circular Gauge with multiple pointers](./images/multiple-pointers.png)

## Pointer animation

The pointers are animated on loading the gauge using the [`CircularGaugePointerAnimation`](https://help.syncfusion.com/cr/aspnetcore-blazor/Syncfusion.Blazor.CircularGauge.CircularGaugePointerAnimation.html) tag in pointer.
The [`Enable`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.CircularGauge.CircularGaugePointerAnimation.html#Syncfusion_Blazor_CircularGauge_CircularGaugePointerAnimation_Enable) property in animation allows you to enable or disable the animation.
The [`Duration`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.CircularGauge.CircularGaugePointerAnimation.html#Syncfusion_Blazor_CircularGauge_CircularGaugePointerAnimation_Duration) property specifies the duration of the animation in milliseconds.

```csharp
@using Syncfusion.Blazor.CircularGauge

<SfCircularGauge Height="250" Width="250">
    <CircularGaugeAxes>
        <CircularGaugeAxis>
            <CircularGaugePointers>
                <CircularGaugePointer Value="70">
                    <CircularGaugePointerAnimation Enable="true" Duration="1500">
                    </CircularGaugePointerAnimation>
                </CircularGaugePointer>
            </CircularGaugePointers>
        </CircularGaugeAxis>
    </CircularGaugeAxes>
</SfCircularGauge>
```

![Circular gauge with pointer animation](./images/pointr-animation.gif)

## Gradient Color

Gradient support allows to add multiple colors in the ranges and pointers of the circular gauge. The following gradient types are supported in the circular gauge.

* Linear Gradient
* Radial Gradient

### Linear Gradient

Using linear gradient, colors will be applied in a linear progression. The start value of the linear gradient can be set using the [`StartValue`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.CircularGauge.CircularGaugeLinearGradient.html#Syncfusion_Blazor_CircularGauge_CircularGaugeLinearGradient_StartValue) property. The end value of the linear gradient will be set using the [`EndValue`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.CircularGauge.CircularGaugeLinearGradient.html#Syncfusion_Blazor_CircularGauge_CircularGaugeLinearGradient_EndValue) property. The color stop values such as color, opacity and offset are set using [`ColorStop`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.CircularGauge.CircularGaugeLinearGradient.html#Syncfusion_Blazor_CircularGauge_CircularGaugeLinearGradient_ColorStop) property.

The linear gradient can be applied to all pointer types like marker, range bar and needle. To do so, follow the below code sample.

```csharp
@using Syncfusion.Blazor.CircularGauge

 <SfCircularGauge Height="250px" CenterY="40%">
    <CircularGaugeAxes>
    <CircularGaugeAxis StartAngle="270" EndAngle="90" Radius="90%" Minimum="0" Maximum="100">
       <CircularGaugeAxisLineStyle Width="3" Color="#E63B86"/>
            <CircularGaugeAxisLabelStyle>
            <CircularGaugeAxisLabelFont Size="0px"/>
             </CircularGaugeAxisLabelStyle>
                <CircularGaugeAxisMajorTicks Height="0.01"/>
                <CircularGaugeAxisMinorTicks Height="0.01"/>
                <CircularGaugePointers>
                <CircularGaugePointer Value="80" Radius="80%" PointerWidth="10" LinearGradient="@PointerLinearModel">
                <CircularGaugeCap Radius="8" Color="White">
                <CircularGaugeCapBorder Color="#E63B86" Width="1"/>
                </CircularGaugeCap>
                <CircularGaugeNeedleTail Length="20%" LinearGradient="@PointerLinearModel"/>
                <CircularGaugePointerAnimation Enable="true" Duration="1000"/>
                </CircularGaugePointer>
                <CircularGaugePointer Value="40" Radius="60%" MarkerWidth="5" MarkerHeight="5" LinearGradient="@PointerLinearModel" PointerWidth="10">
                <CircularGaugeCap Radius="8" Color="White">
                <CircularGaugeCapBorder Color="#E63B86" Width="1"/>
                </CircularGaugeCap>
                <CircularGaugeNeedleTail Length="20%" LinearGradient="@PointerLinearModel"/>
                <CircularGaugePointerAnimation Enable="true" Duration="1000"/>
                </CircularGaugePointer>
                </CircularGaugePointers>
    </CircularGaugeAxis>
    </CircularGaugeAxes>
</SfCircularGauge>
@code {
    public static LinearGradient PointerLinearModel = new LinearGradient() {
        StartValue = "1%",
        EndValue = "99%",
        ColorStop = new List<ColorStop>() {
            new ColorStop { Opacity=1, Color= "#fef3f9", Offset="1%" },
            new ColorStop { Opacity=1, Color= "#f54ea2", Offset="100%" }
        }
    };
}
```

### Radial Gradient

Using radial gradient, colors will be applied in circular progression. The inner circle position of the radial gradient will be set using the [`InnerPosition`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.CircularGauge.CircularGaugeRadialGradient.html#Syncfusion_Blazor_CircularGauge_CircularGaugeRadialGradient_InnerPosition) property. The outer circle position of the radial gradient can be set using the [`OuterPosition`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.CircularGauge.CircularGaugeRadialGradient.html#Syncfusion_Blazor_CircularGauge_CircularGaugeRadialGradient_OuterPosition) property. The color stop values such as color, opacity and offset are set using [`ColorStop`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.CircularGauge.CircularGaugeRadialGradient.html#Syncfusion_Blazor_CircularGauge_CircularGaugeRadialGradient_ColorStop) property.

The radial gradient can be applied to all pointer types like marker, range bar and needle. To do so, follow the below code sample.

```csharp
@using Syncfusion.Blazor.CircularGauge

 <SfCircularGauge Height="250px" CenterY="40%">
    <CircularGaugeAxes>
    <CircularGaugeAxis StartAngle="270" EndAngle="90" Radius="90%" Minimum="0" Maximum="100">
       <CircularGaugeAxisLineStyle Width="3" Color="#E63B86"/>
            <CircularGaugeAxisLabelStyle>
            <CircularGaugeAxisLabelFont Size="0px"/>
             </CircularGaugeAxisLabelStyle>
                <CircularGaugeAxisMajorTicks Height="0.01"/>
                <CircularGaugeAxisMinorTicks Height="0.01"/>
                <CircularGaugePointers>
                <CircularGaugePointer Value="80" Radius="80%" PointerWidth="10" RadialGradient="@PointerRadialModel">
                <CircularGaugeCap Radius="8" Color="White">
                <CircularGaugeCapBorder Color="#E63B86" Width="1"/>
                </CircularGaugeCap>
                <CircularGaugeNeedleTail Length="20%" RadialGradient="@PointerRadialModel"/>
                <CircularGaugePointerAnimation Enable="true" Duration="1000"/>
                </CircularGaugePointer>
                <CircularGaugePointer Value="40" Radius="60%" MarkerWidth="5" MarkerHeight="5" RadialGradient="@PointerRadialModel" PointerWidth="10">
                <CircularGaugeCap Radius="8" Color="White">
                <CircularGaugeCapBorder Color="#E63B86" Width="1"/>
                </CircularGaugeCap>
                <CircularGaugeNeedleTail Length="20%" RadialGradient="@PointerRadialModel"/>
                <CircularGaugePointerAnimation Enable="true" Duration="1000"/>
                </CircularGaugePointer>
                </CircularGaugePointers>
    </CircularGaugeAxis>
    </CircularGaugeAxes>
</SfCircularGauge>
@code {
    public static RadialGradient PointerRadialModel = new RadialGradient()
    {
        Radius = "60%",
        OuterPosition = new OuterPosition() { X="50%", Y="50%" },
        InnerPosition = new InnerPosition() { X="50%", Y="50%" },
        ColorStop = new List<ColorStop>() {
            new ColorStop { Opacity=0.9, Color= "#fff5f5", Offset="1%" },
            new ColorStop { Opacity=0.8, Color= "#f54ea2", Offset="99%" }
        }
    };
}
```

<!-- markdownlint-disable MD010 -->