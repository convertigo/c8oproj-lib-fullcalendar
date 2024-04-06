


# lib_FullCalendar

# This is the FullCalendar Library for Convertigo Low Code studio
Use this library to provider Calendar with multiple views to your applications. the library is based on the FullCalendar component https://fullcalendar.io/




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
<td>calEvents</td><td>Locale such as 'en', 'fr', 'es' ..</td>
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
<td>initialView</td><td>InitialDisplay such as 'dayGridMonth', 'timeGridWeek', 'listWeek', 'dayGridWeek', 'multiMonthYear'
</td>
</tr>
<tr>
<td>locale</td><td>Locale such as 'en', 'fr', 'es' ..</td>
</tr>
<tr>
<td>selectable</td><td>Enables the user to select events can be true or false</td>
</tr>
</table>



