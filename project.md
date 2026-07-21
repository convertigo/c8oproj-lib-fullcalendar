
# ![](https://github.com/convertigo/convertigo/blob/develop/engine/src/com/twinsoft/convertigo/beans/core/images/project_color_16x16.png?raw=true "Project") lib_FullCalendar

# This is the FullCalendar Library for Convertigo Low Code studio
Use this library to provide Calendar with multiple views to your applications. the library is based on the FullCalendar component https://fullcalendar.io/

![Convertigo FullCalendar](./docImg/FullCalendar.png)



<details><summary><span style="color:DarkGoldenRod"><i>Connectors</i></span></summary><blockquote><p>


## ![](https://github.com/convertigo/convertigo/blob/develop/engine/src/com/twinsoft/convertigo/beans/connectors/images/sqlconnector_color_16x16.png?raw=true "SqlConnector") void

void connector, replace or don't use it

<details><summary><span style="color:DarkGoldenRod"><i>Transactions</i></span></summary><blockquote><p>


### ![](https://github.com/convertigo/convertigo/blob/develop/engine/src/com/twinsoft/convertigo/beans/transactions/images/sqltransaction_color_16x16.png?raw=true "SqlTransaction") void

does nothing
</p></blockquote></details>
</p></blockquote></details>

<details><summary><span style="color:DarkGoldenRod"><i>Mobile Application</i></span></summary><blockquote><p>


## ![](https://github.com/convertigo/convertigo/blob/develop/engine/src/com/twinsoft/convertigo/beans/core/images/mobileapplication_color_16x16.png?raw=true "MobileApplication") Application

Describes the mobile application global properties

<details><summary><span style="color:DarkGoldenRod"><i>Pages</i></span></summary><blockquote><p>


### ![](https://github.com/convertigo/convertigo/blob/develop/engine/src/com/twinsoft/convertigo/beans/ngx/components/images/pagecomponent_color_16x16.png?raw=true "PageComponent") Page

My First Page as root page
</p></blockquote></details>

<details><summary><span style="color:DarkGoldenRod"><i>Shared Components</i></span></summary><blockquote><p>


### ![](https://github.com/convertigo/convertigo/blob/develop/engine/src/com/twinsoft/convertigo/beans/ngx/components/images/uisharedcomponent_16x16.png?raw=true "UISharedRegularComponent") FullCalendar

FullCalendar 7.0.1 Standard wrapper for Convertigo NGX.

Renders an interactive calendar through @fullcalendar/angular with the Classic theme and the bundled DayGrid, TimeGrid, List, MultiMonth and Interaction plugins. Premium Scheduler/resource views are not included.

All public inputs are applied at initialization. locale, initialView, headerToolbar, buttonText, selectable, calEvents, editable, height, initialDate and multiMonthMaxColumns are also handled reactively after initialization.

Outputs:
- DateClicked: emits the native JavaScript Date for a clicked date/time cell.
- EventChanged: emits a plain event object after an event change.
- calEventsChange: supports two-way binding when an editable event is changed.

FullCalendar documentation: https://fullcalendar.io/docs

<span style="color:DarkGoldenRod">Variables</span>

<table>
<tr>
<th>
name
</th>
<th>
comment
</th>
</tr>
<tr>
<td>
<img src="https://github.com/convertigo/convertigo/blob/develop/engine/src/com/twinsoft/convertigo/beans/ngx/components/images/uicompvariable_16x16.png?raw=true "  alt="UICompVariable" >&nbsp;buttonText
</td>
<td>
Compatibility input for toolbar button labels.

FullCalendar 7 removed the legacy buttonText option. This component converts this object into FullCalendar 7 buttons[name].text entries.

Supported generic aliases:
- today -> today
- month -> dayGridMonth
- week -> dayGridWeek and timeGridWeek
- day -> timeGridDay
- list -> listDay, listWeek, listMonth and listYear
- year -> multiMonthYear

Exact button/view names are also accepted, for example:
<pre>
{
  today: 'Today',
  dayGridMonth: 'Month',
  timeGridWeek: 'Week',
  listWeek: 'Agenda'
}
</pre>

Values must be display strings, not full button configuration objects. Reactive: changing this input reapplies the generated buttons option.

Documentation: https://fullcalendar.io/docs/buttons
</td>
</tr>
<tr>
<td>
<img src="https://github.com/convertigo/convertigo/blob/develop/engine/src/com/twinsoft/convertigo/beans/ngx/components/images/uicompvariable_16x16.png?raw=true "  alt="UICompVariable" >&nbsp;calEvents
</td>
<td>
Array of FullCalendar event input objects displayed by the calendar.

Common fields:
- id: stable unique identifier
- title: visible label
- start: Date or ISO 8601 value
- end: optional exclusive end Date/ISO value
- allDay: all-day display flag
- editable, color, className and extendedProps: optional event settings

For editable events, id is required for reliable two-way synchronization. After an eventChange, the component replaces the matching item immutably, emits calEventsChange and emits EventChanged. An unknown id is appended; an event without id only triggers EventChanged and cannot be synchronized into this array.

Replacing the input array reactively updates FullCalendar. Prefer a new array reference when changing events from the parent application.

Documentation: https://fullcalendar.io/docs/event-object
</td>
</tr>
<tr>
<td>
<img src="https://github.com/convertigo/convertigo/blob/develop/engine/src/com/twinsoft/convertigo/beans/ngx/components/images/uicompvariable_16x16.png?raw=true "  alt="UICompVariable" >&nbsp;editable
</td>
<td>
Controls whether calendar events can be modified by the user. Boolean, default: true.

When enabled, FullCalendar permits event dragging and duration resizing where supported by the active view. Individual events can override this setting with editable, startEditable or durationEditable.

A completed modification triggers EventChanged. With a stable event id, it also updates calEvents and emits calEventsChange.

Reactive: changing this input after initialization calls Calendar::setOption('editable', value).

Documentation: https://fullcalendar.io/docs/editable
</td>
</tr>
<tr>
<td>
<img src="https://github.com/convertigo/convertigo/blob/develop/engine/src/com/twinsoft/convertigo/beans/ngx/components/images/uicompvariable_16x16.png?raw=true "  alt="UICompVariable" >&nbsp;headerToolbar
</td>
<td>
FullCalendar header toolbar definition. Use left/center/right or start/center/end sections.

Example:
<pre>
{
  left: 'prev,next today',
  center: 'title',
  right: 'dayGridMonth,timeGridWeek,listWeek'
}
</pre>

Toolbar tokens include title, prev, next, prevYear, nextYear, today and exact view names.

Important FullCalendar 7 syntax:
- comma-separated tokens are rendered as adjacent buttons;
- space-separated tokens are rendered as separate groups with a gap;
- do not insert a space immediately after a comma, otherwise an empty toolbar item can be rendered.

Use an empty string for an empty section. FullCalendar also accepts false to hide the toolbar.

Reactive: changing this input after initialization calls Calendar::setOption('headerToolbar', value).

Documentation: https://fullcalendar.io/docs/headerToolbar
</td>
</tr>
<tr>
<td>
<img src="https://github.com/convertigo/convertigo/blob/develop/engine/src/com/twinsoft/convertigo/beans/ngx/components/images/uicompvariable_16x16.png?raw=true "  alt="UICompVariable" >&nbsp;height
</td>
<td>
Height of the complete calendar, including its toolbar. Default: '100%'.

Accepted values:
- integer: fixed pixel height
- 'auto': natural content height without internal scrollbars
- percentage or another valid CSS size such as '100%' or '600px'

With '100%', the parent container must itself have a resolved height.

Reactive: changing this input after initialization calls Calendar::setOption('height', value).

Documentation: https://fullcalendar.io/docs/height
</td>
</tr>
<tr>
<td>
<img src="https://github.com/convertigo/convertigo/blob/develop/engine/src/com/twinsoft/convertigo/beans/ngx/components/images/uicompvariable_16x16.png?raw=true "  alt="UICompVariable" >&nbsp;initialDate
</td>
<td>
Date initially displayed by the calendar.

Accepted values include a native JavaScript Date and values FullCalendar can parse, such as the ISO 8601 string '2026-07-21'. When empty or omitted, FullCalendar uses the current date.

Reactive: changing this input after initialization calls Calendar::gotoDate(value). Empty, null and undefined updates are ignored by gotoDate.

This controls the visible date, not the dates stored in calEvents.

Documentation: https://fullcalendar.io/docs/initialDate
</td>
</tr>
<tr>
<td>
<img src="https://github.com/convertigo/convertigo/blob/develop/engine/src/com/twinsoft/convertigo/beans/ngx/components/images/uicompvariable_16x16.png?raw=true "  alt="UICompVariable" >&nbsp;initialView
</td>
<td>
Exact FullCalendar view name displayed when the calendar starts. Default: 'dayGridMonth'.

Bundled view examples:
- dayGridMonth, dayGridWeek
- timeGridWeek, timeGridDay
- listDay, listWeek, listMonth, listYear
- multiMonthYear

The corresponding plugin must be bundled. This component includes DayGrid, TimeGrid, List and MultiMonth.

Reactive: changing this input after initialization calls Calendar::changeView(value).

Documentation: https://fullcalendar.io/docs/initialView
</td>
</tr>
<tr>
<td>
<img src="https://github.com/convertigo/convertigo/blob/develop/engine/src/com/twinsoft/convertigo/beans/ngx/components/images/uicompvariable_16x16.png?raw=true "  alt="UICompVariable" >&nbsp;locale
</td>
<td>
FullCalendar locale code or locale object. Default: 'en'.

Examples: 'en', 'fr', 'es', 'pt-br'. The locale affects month/day names, date formatting, button defaults, first day of week and other regional settings. The requested locale must be available to the generated application.

Reactive: changing this input after initialization calls Calendar::setOption('locale', value).

Custom labels supplied through buttonText take precedence for the mapped toolbar buttons.

Documentation: https://fullcalendar.io/docs/locale
</td>
</tr>
<tr>
<td>
<img src="https://github.com/convertigo/convertigo/blob/develop/engine/src/com/twinsoft/convertigo/beans/ngx/components/images/uicompvariable_16x16.png?raw=true "  alt="UICompVariable" >&nbsp;multiMonthMaxColumns
</td>
<td>
Maximum number of month columns attempted by the MultiMonth view. Number, default: 3.

This option applies to views such as multiMonthYear. FullCalendar may automatically use fewer columns when the available width is insufficient. Set 1 to force a single vertical column of months.

The MultiMonth plugin is bundled by this component.

Reactive: changing this input after initialization calls Calendar::setOption('multiMonthMaxColumns', value).

Documentation: https://fullcalendar.io/docs/multiMonthMaxColumns
</td>
</tr>
<tr>
<td>
<img src="https://github.com/convertigo/convertigo/blob/develop/engine/src/com/twinsoft/convertigo/beans/ngx/components/images/uicompvariable_16x16.png?raw=true "  alt="UICompVariable" >&nbsp;selectable
</td>
<td>
Enables FullCalendar date/time selection. Boolean, default: true.

When enabled, users can select date ranges and selectMirror is enabled by this component. The Interaction plugin is bundled.

Current wrapper limitation: no range-selection output is exposed. DateClicked emits individual date/time clicks only. Add a dedicated select callback/output if consumers need the selected range.

Reactive: changing this input after initialization calls Calendar::setOption('selectable', value).

Documentation: https://fullcalendar.io/docs/selectable
</td>
</tr>
</table>


<span style="color:DarkGoldenRod">Events</span>

<table>
<tr>
<th>
name
</th>
<th>
comment
</th>
</tr>
<tr>
<td>
<img src="https://github.com/convertigo/convertigo/blob/develop/engine/src/com/twinsoft/convertigo/beans/ngx/components/images/uicompevent_16x16.png?raw=true "  alt="UICompEvent" >&nbsp;DateClicked
</td>
<td>
Emitted when the user clicks a date or time cell.

Payload: only the native JavaScript Date from FullCalendar dateClickInfo.date, available in the Convertigo event output (out). The wrapper does not expose dateStr, allDay, jsEvent, dayEl or the current view.

The Interaction plugin required by dateClick is bundled. A click on a day heading in List view does not trigger dateClick.

Documentation: https://fullcalendar.io/docs/dateClick
</td>
</tr>
<tr>
<td>
<img src="https://github.com/convertigo/convertigo/blob/develop/engine/src/com/twinsoft/convertigo/beans/ngx/components/images/uicompevent_16x16.png?raw=true "  alt="UICompEvent" >&nbsp;EventChanged
</td>
<td>
Emitted after FullCalendar reports an eventChange, including drag, resize or an Event API setter update.

Payload: the updated event returned by Event::toPlainObject(). Read it from the Convertigo event output (out).

When the event has a stable id, calEvents is also updated immutably and calEventsChange is emitted for two-way binding. Events without id still emit EventChanged but are not written back into calEvents.

This output is not an event-click notification; it only reports modifications.

Documentation: https://fullcalendar.io/docs/eventChange
</td>
</tr>
</table>

</p></blockquote></details>
</p></blockquote></details>
