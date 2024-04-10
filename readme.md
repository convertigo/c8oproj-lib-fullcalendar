


# lib_FullCalendar

# This is the FullCalendar Library for Convertigo Low Code studio
Use this library to provide Calendar with multiple views to your applications. the library is based on the FullCalendar component https://fullcalendar.io/

![Convertigo FullCalendar](./docImg/FullCalendar.png)



For more technical informations : [documentation](./project.md)

- [Installation](#installation)
- [Mobile Library](#mobile-library)
    - [Shared Components](#shared-components)
        - [FullCalendar](#fullcalendar)


## Installation

1. In your Convertigo Studio click on ![](https://github.com/convertigo/convertigo/blob/develop/eclipse-plugin-studio/icons/studio/project_import.gif?raw=true "Import a project in treeview") to import a project in the treeview
2. In the import wizard

   ![](https://github.com/convertigo/convertigo/blob/develop/eclipse-plugin-studio/tomcat/webapps/convertigo/templates/ftl/project_import_wzd.png?raw=true "Import Project")
   
   paste the text below into the `Project remote URL` field:
   <table>
     <tr><td>Usage</td><td>Click the copy button at the end of the line</td></tr>
     <tr><td>To contribute</td><td>

     ```
     lib_FullCalendar=https://github.com/convertigo/c8oproj-lib-fullcalendar.git:branch=master
     ```
     </td></tr>
     <tr><td>To simply use</td><td>

     ```
     lib_FullCalendar=https://github.com/convertigo/c8oproj-lib-fullcalendar/archive/master.zip
     ```
     </td></tr>
    </table>
3. Click the `Finish` button. This will automatically import the __lib_FullCalendar__ project


## Mobile Library

Describes the mobile application global properties

### Shared Components

#### FullCalendar

FullCalendar providing Calendar, planning and schedules

**variables**

<table>
<tr>
<th>name</th><th>comment</th>
</tr>
<tr>
<td>buttonText</td><td>A JSON Object representing the Button labels 
<pre>
{
  today:    "Today",
  month:    'month',
  week:     'week',
  day:      'day',
  list:     'list'
}
</pre>

</td>
</tr>
<tr>
<td>calEvents</td><td>The initial events to be displayed in the calendar. An array of event objects of this structure :
<pre>
{
  id: 'a',
  title: 'my event',
  start: '2018-09-01'
}
</pre>
See Event documentation for details : https://fullcalendar.io/docs/event-object

Note that when a user resizes or modifies an event, this array will be automatically updated if you use two way binding.

</td>
</tr>
<tr>
<td>editable</td><td>Enables the user to edit events can be true or false</td>
</tr>
<tr>
<td>headerToolbar</td><td>A JSON Object representing the Header toolbar 
<pre>
{
    left: 'prev,next today',
    center: 'title',
    right: 'dayGridMonth,timeGridWeek,timeGridDay'
}
</pre>

</td>
</tr>
<tr>
<td>height</td><td>Sets the height of the entire calendar, including header and footer.

Integer, "auto", a CSS value like "100%"

By default, this option is unset and the calendar’s height is calculated by aspectRatio.

If an integer is specified, the height of the calendar will be guaranteed to be that exact pixel height. If the contents will not fit within the height, scrollbars will appear.

If "auto" is specified, the view’s contents will assume a natural height and no scrollbars will be used.

If "100%" is specified, the height of the calendar will match the height of its parent container element. See an example. Any other valid CSS value is accepted as well.
</td>
</tr>
<tr>
<td>initialDate</td><td>The initial date displayed when the calendar first loads.

Date

When not specified, this value defaults to the current date.

This value can be anything that can parse into a Date, including an ISO8601 date string like "2014-02-01".</td>
</tr>
<tr>
<td>initialView</td><td>InitialDisplay such as 'dayGridMonth', 'timeGridWeek', 'listWeek', 'dayGridWeek', 'multiMonthYear'
</td>
</tr>
<tr>
<td>locale</td><td>Locale such as 'en', 'fr', 'es' ..</td>
</tr>
<tr>
<td>multiMonthMaxColumns</td><td>The maximum columns of months that Multi-Month Grid will attempt to render.

Number, default: 3

By default, Multi-Month Grid will attempt to display 3 columns of mini-months. If there is insufficient space, requiring each month to be smaller than multiMonthMinWidth, fewer columns will be displayed.

To display one single column of months, set multiMonthMaxColumns to 1.</td>
</tr>
<tr>
<td>selectable</td><td>Enables the user to select events can be true or false</td>
</tr>
</table>

**events**

<table>
<tr>
<th>name</th><th>comment</th>
</tr>
<tr>
<td>DateClicked</td><td>Triggered when an event is modified by the user, the modified event object will be in the <pre>out</out>
</td>
</tr>
<tr>
<td>EventChanged</td><td>Triggered when an event is modified by the user, the modified event object will be in the <pre>out</out>
</td>
</tr>
</table>



