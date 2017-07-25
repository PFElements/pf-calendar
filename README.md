# pf-elements
A Polymer 2.0 based collection of reusable web components. 

[![Join the chat at https://gitter.im/pf-elements/Lobby](https://badges.gitter.im/pf-elements/Lobby.svg)](https://gitter.im/pf-elements/Lobby?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)


[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/owner/my-element)

## Demo
[Click here for docs & demo](https://www.webcomponents.org/element/PFElements/pf-calendar/demo/demo/index.html)

| Element Name | Latest Version (Bower) | Npm version  | Build Status |
|--------------|------------------------|--------------|--------------|
| [pf-calendar](https://github.com/PFElements/pf-calendar) | [![GitHub version](https://badge.fury.io/gh/PFElements%2Fpf-calendar.svg)](https://badge.fury.io/gh/PFElements%2Fpf-calendar) | [![npm version](https://badge.fury.io/js/pf-calendar.svg)](https://www.npmjs.com/package/pf-calendar) |[![Build Status](https://travis-ci.org/PFElements/pf-calendar.svg?branch=master)](https://travis-ci.org/PFElements/pf-calendar) | | [pf-calendar-event]|

## Install the Polymer-CLI

First, make sure you have the [Polymer CLI](https://www.npmjs.com/package/polymer-cli) installed. Then run `polymer serve` to serve your application locally.

---
# A composite component
`<pf-calendar></pf-calendar>` makes use of two other components together to give you control over customizing the UI of the calendar and also to be able to customize the backend data for the calendar. To supply the data for the calendar this element makes use of Firebase as a backend. 

For referrence please see both of our other custom elements
`<pf-calendar-events></pf-calendar-events>` for the UI and `<pf-calendar-events-data></pf-calendar-events-data>` for manipulating the backend data in Firebase.

# Customization and usage

This custom element can be customized in a number of ways

## Customization of look and feel

By default you have two general options

a. material-calendar

b. classic-calendar

Once you decide you general look and feel then you can further customize the details, e.g. if you chose a Material Design look and feel and you want to change the width, hight, color etc. you can do that with the provided API. 
#### material Calendar Example
<!---
```
<custom-element-demo>
  <template>
    <script src="../webcomponentsjs/webcomponents-lite.js"></script>
    <link rel="import" href="pf-calendar-events.html">
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->
```html




 <pf-calendar-events
                  calendarstyle="material-calendar"
                  data='[
                          { "eventName": "Lunch Meeting w/ Mark", "calendar": "Work", "color": "orange","date":"1491322091394" },
                          { "eventName": "Giants vs Packers", "calendar": "sport", "color": "blue","date":"1499185140000" },
                          { "eventName": "Soccer", "calendar": "sport", "color": "blue","date":"1491581940000" },
                          { "eventName": "Public Holiday", "calendar": "holiday", "color": "green","date":"1494173940000" }]'
          >

          </pf-calendar-events>
```
#### Classic Calendar Example
<!---
```
<custom-element-demo>
  <template>
    <script src="../webcomponentsjs/webcomponents-lite.js"></script>
    <link rel="import" href="pf-calendar-events.html">
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->
```html
 <pf-calendar-events
                  calendarstyle="classic-calendar"
                  data='[
                          { "eventName": "Lunch Meeting w/ Mark", "calendar": "Work", "color": "orange","date":"1491322091394" },
                          { "eventName": "Giants vs Packers", "calendar": "sport", "color": "blue","date":"1499185140000" },
                          { "eventName": "Soccer", "calendar": "sport", "color": "blue","date":"1491581940000" },
                          { "eventName": "Public Holiday", "calendar": "holiday", "color": "green","date":"1494173940000" }]'
          >

          </pf-calendar-events>
```
default value of 'calendarstyle' is 'material-calendar'
### Types of calendar
You can define different types of calendar events (appointments, meetings, reminders, etc). e.g. you can define a "Sports" Calendar "Office Meeting" calendar, "Birthday Reminders" calendar. Distinct type of categories will appear in different colors.

### CRUD operations

Buttons / icons are provided to enable Adding, deleting or updating an event (meeting, reminder, appointment etc)
Material based button and icons are provided to enable these operations.
For firebase events data, please see our firebase element

## Customization of Calendar Events/Data (your meetings, appointments, reminders etc)

Of course if you cannot provide you own data then why even use a third party component, and you need events as well to notify you of the user interaction with the calendar

This custom element provides you two generic ways that again can be further customized

a. Data Through firebase custom element (Please see our firebase custom element that can be combined with this element to enable your data interaction from firebase

b. By providing an array of data. (Calendar events, appointments, meetings, reminders etc.)

### CRUD operations
Our custom element provides a way to hook your CRUD operations into our calendar, it provides a number of API hooks/events to notify you about an operation that is performed on a certain event.


Custom Event                     | Description                       
---------------------------------|----------------------------------------
`event-add`                      | Add event retuns current selected date ('e.detail.date'), fired when user press add event button  
`event-edit`                     | Edit event retuns event ('e.detail.event'),fired when user press edit event button
`event-delete`                   | Delete event retuns event ('e.detail.event'),fired when user press delete event button
`event-select`                   | Event Select retuns event ('e.detail.event'),fired when user click on any event            
`date-select`                    | Date Select retuns seleted date and events of date ('e.detail.date'and'e.detail.events'),fired when user click on any event             
  

### Methods
The following methods are available for crude events operation:

Methods                                 | Description                           
----------------------------------------|--------------------------
`addNewEvent(event)`                       |  Take event object and add as a into firebase 
`updateEvent(key,event)`                |  Take firebase data ref key and updated event object , update the given ref key node                          
`deleteEvent(key)`                      |  Take record ref key and delete that event                    
            

<!---
```
<custom-element-demo>
  <template>
    <script src="../webcomponentsjs/webcomponents-lite.js"></script>
    <link rel="import" href="pf-calendar-events.html">
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->
```html




 <pf-calendar-events
                  data='[
                          { "eventName": "Lunch Meeting w/ Mark", "calendar": "Work", "color": "orange","date":"1491322091394" },
                          { "eventName": "Giants vs Packers", "calendar": "sport", "color": "blue","date":"1499185140000" },
                          { "eventName": "Soccer", "calendar": "sport", "color": "blue","date":"1491581940000" },
                          { "eventName": "Public Holiday", "calendar": "holiday", "color": "green","date":"1494173940000" }]'
          >

          </pf-calendar-events>
```

### Styling
The following custom properties and mixins are available for styling:

Custom property                         | Description                             | Default
----------------------------------------|-----------------------------------------|-------------------------
`--pf-calendar-bg-color`                |  Calendar background                    | #4A4A4A
`--pf-calendar-width`                   |  Calendar Width                         | 420px
`--pf-calendar-height`                  |  Calendar Height                        | 570px
`--pf-calendar-header-background`       |  Calendar Header Background             | rgba(66, 66, 66, 1)
`--pf-calendar-header-height`           |  Calendar Header height                 | 50px
`--pf-calendar-month-title-font-size`   |   Font size of  month on header         | 20px
`--pf-calendar-month-title-line-height` |  Calendar Header title line Height      | rgba(66, 66, 66, 1)
`--pf-calendar-header-left-arrow-color` |  Previous Month arrow color             | rgba(160, 159, 160, 1)
`--pf-calendar-header-right-arrow-color`|  Next Month arrow color                 | rgba(160, 159, 160, 1)
`--pf-calendar-month-title-color`       |  Month Title color                      | #000
`--pf-calendar-week-bg`                 |  Background color of week               | #4A4A4A
`--pf-calendar-day-bg`                  |  Day Background                         | #4A4A4A
`--pf-calendar-day-color`               |  color of date                          | #000
`--pf-calendar-other-day-color`         |  color of previous and next month date  | rgba(255, 255, 255, .3)
`--pf-calendar-today-color`             |  Current date Color                     | rgba(156` 202, 235, 1)
`--pf-calendar-selected-date-bg`        |  Selected Date Background color         | #000
`--pf-calendar-selected-date-color`     |  Selected Date color                    | #fff
`--pf-calendar-day-name-color`          |  Name of Day color e.g(MON,TUE,WED)     | rgba(255` 255, 255, .5)
`--pf-calendar-event-detail-bg`         |  Event box background                   | rgba(164, 164, 164, 1)
`--pf-calendar-event-color`              |  color of label "Event"                | #000
`--pf-calendar-addevent-button-bg-color'|  Add Event Button color                 | rgba(164, 164, 164, 1)
`--pf-calendar-addevent-button-text-color`| Add Event text color                  | #fff
`--pf-calendar-addevent-button-hover-color`|  Add event button hover color        | rgba(170, 170, 170, 1)
`--pf-calendar-addbutton-disply`        |  to hide button set "none"              |inline-block
`--pf-calendar-deletebutton-disply`     |  to hide button set "none"              |inline
`--pf-calendar-editbutton-disply`       |  to hide button set "none"              |inline
`--pf-calendar-legend-bg`               |  Background color of legend bar         | rgba(60, 60, 60, 1)



## Install the Polymer-CLI

First, make sure you have the [Polymer CLI](https://www.npmjs.com/package/polymer-cli) installed. Then run `polymer serve` to serve your application locally.

## Viewing Your Application

```
$ polymer serve
```

## Building Your Application

```
$ polymer build
```

This will create a `build/` folder with `bundled/` and `unbundled/` sub-folders
containing a bundled (Vulcanized) and unbundled builds, both run through HTML,
CSS, and JS optimizers.

You can serve the built versions by giving `polymer serve` a folder to serve
from:

```
$ polymer serve build/bundled
```

## Running Tests

```
$ polymer test
```

Your application is already set up to be tested via [web-component-tester](https://github.com/Polymer/web-component-tester). Run `polymer test` to run your application's test suite locally.

## Learn more

See the list of elements, demos, and documentation by browsing this collection on webcomponents.org:

### [Go to webcomponents.org](https://www.webcomponents.org/collection/pfelements/pf-elements)

---

## Contributing

Comments, questions, suggestions, issues, and pull requests are all welcome.

### Get in touch with the team

Joing us at [![Join the chat at https://gitter.im/pf-elements/Lobby](https://badges.gitter.im/pf-elements/Lobby.svg)](https://gitter.im/pf-elements/Lobby?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

- [Twitter](<a href="https://twitter.com/polymerio" class="twitter-follow-button" data-show-count="false">Follow @polymerio</a>)
- [Facebook] (https://www.facebook.com/polymerjs)
- [Google+] (https://plus.google.com/116168214823506639166) 
- [YouTube] (https://www.youtube.com/channel/UCDKqvDyAn_QTBvCPvrZKTkw) 

### Some ways to help:

- **Test the elements and provide feedback**: We would love to hear your feedback on anything related to the elements, like features, API and design. The best way to start is by trying them out. And to get a quick response, either drop a question/comment on the chat or open an issue in GitHub.
- **Report bugs**: File issues for the elements in their respective GitHub projects.
- **Send pull requests**: If you want to contribute code, check out the development instructions below.

We encourage you to read the [contribution instructions by GitHub](https://guides.github.com/activities/contributing-to-open-source/#contributing) also.

## License

MIT License
