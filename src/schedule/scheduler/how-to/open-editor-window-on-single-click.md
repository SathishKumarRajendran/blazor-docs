# Open Editor Window on Single Click

By default, the editor window will open on double clicking the cell or appointment. In the following code example, we have opened the editor window on single click using `OpenEditor` public method within `OnCellClick` and `OnEventClick` Scheduler events.

```csharp
@using Syncfusion.Blazor.Schedule

<SfSchedule @ref="ScheduleRef" TValue="AppointmentData" ShowQuickInfo="false" Height="550px" @bind-SelectedDate="@CurrentDate">
    <ScheduleEventSettings DataSource="@DataSource"></ScheduleEventSettings>
    <ScheduleEvents TValue="AppointmentData" OnCellClick="OnCellClick" OnEventClick="OnEventClick"></ScheduleEvents>
</SfSchedule>

@code{
    DateTime CurrentDate = new DateTime(2020, 3, 11);
    SfSchedule<AppointmentData> ScheduleRef;
    public async Task OnCellClick(CellClickEventArgs args)
    {
        args.Cancel = true;
        await ScheduleRef.OpenEditor(args, CurrentAction.Add); //to open the editor on cell click
    }
    public async Task OnEventClick(EventClickArgs<AppointmentData> args)
    {
        args.Cancel = true;
        await ScheduleRef.OpenEditor(args.Event, CurrentAction.Save); //to open the editor on event click
    }
    List<AppointmentData> DataSource = new List<AppointmentData>
    {
        new AppointmentData{ Id = 1, Subject = "Meeting", StartTime = new DateTime(2020, 3, 11, 9, 30, 0) , EndTime = new DateTime(2020, 3, 11, 11, 0, 0)}
    };
    public class AppointmentData
    {
        public int Id { get; set; }
        public string Subject { get; set; }
        public string Location { get; set; }
        public DateTime StartTime { get; set; }
        public DateTime EndTime { get; set; }
        public string Description { get; set; }
        public bool IsAllDay { get; set; }
        public string RecurrenceRule { get; set; }
        public string RecurrenceException { get; set; }
        public Nullable<int> RecurrenceID { get; set; }
    }
}
```