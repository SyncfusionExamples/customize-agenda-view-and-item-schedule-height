# How to customize Agenda view and item height in Xamarin.Forms Schedule (SfSchedule)

You can customize the AgendaView height and item height of Xamarin.Forms [SfSchedule](https://help.syncfusion.com/xamarin/scheduler/overview).

Using the [AgendaViewHeight](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthViewSettings~AgendaViewHeight.html) property in MonthViewSettings, you can customize the agenda view height in MonthView, and you can customize the agenda view appointment height by setting the [ItemHeight](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthViewSettings~ItemHeight.html) in [AgendaViewStyle](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthViewSettings~AgendaViewStyle.html) property of [MonthViewSettings](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthViewSettings.html).

You can also refer to the following article.

https://www.syncfusion.com/kb/11864/how-to-customize-agenda-view-and-item-height-in-xamarin-forms-schedule-sfschedule

**XAML**

``` xml
<schedule:SfSchedule x:Name="Schedule"
                                 DataSource="{Binding Meetings}"
                                 ScheduleView="MonthView">

                <schedule:SfSchedule.MonthViewSettings>
                    <schedule:MonthViewSettings ShowAgendaView="true" AgendaViewHeight="300">
                        <schedule:MonthViewSettings.AgendaViewStyle>
                            <schedule:AgendaViewStyle ItemHeight="100"/>
                        </schedule:MonthViewSettings.AgendaViewStyle>
                    </schedule:MonthViewSettings>
                </schedule:SfSchedule.MonthViewSettings>

                <schedule:SfSchedule.AppointmentMapping>
                    <schedule:ScheduleAppointmentMapping
                        ColorMapping="Color"
                        EndTimeMapping="To"
                        StartTimeMapping="From"
                        SubjectMapping="EventName"
                        />
                </schedule:SfSchedule.AppointmentMapping>

                <schedule:SfSchedule.BindingContext>
                    <local:SchedulerViewModel/>
                </schedule:SfSchedule.BindingContext>
</schedule:SfSchedule>
```
**Output**

![AgendaHeightCustomization](https://github.com/SyncfusionExamples/customize-agenda-view-and-item-schedule-height/blob/master/ScreenShot/AgendaHeightCustomization.png)
