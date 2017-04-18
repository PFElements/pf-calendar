# pf-elements
A Polymer 2.0 based collection of reusable web components 

[![Join the chat at https://gitter.im/pf-elements/Lobby](https://badges.gitter.im/pf-elements/Lobby.svg)](https://gitter.im/pf-elements/Lobby?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)


[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/owner/my-element)

## Demo
[Click here for docs & demo](https://github.com/PFElements/pf-calendar/blob/master/demo/index.html)

| Element Name | Latest Version (Bower) | Npm version  | Build Status |
|--------------|------------------------|--------------|--------------|
| [pf-calendar](https://github.com/PFElements/pf-calendar) | [![GitHub version](https://badge.fury.io/gh/PFElements%2Fpf-calendar.svg)](https://badge.fury.io/gh/PFElements%2Fpf-calendar) | [![npm version](https://badge.fury.io/js/pf-calendar.svg)](https://www.npmjs.com/package/pf-calendar) |[![Build Status](https://travis-ci.org/PFElements/pf-calendar.svg?branch=master)](https://travis-ci.org/PFElements/pf-calendar) | | [pf-calendar-event]|

## Install the Polymer-CLI

First, make sure you have the [Polymer CLI](https://www.npmjs.com/package/polymer-cli) installed. Then run `polymer serve` to serve your application locally.


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

- [Twitter](<a href="https://twitter.com/polymerjs" class="twitter-follow-button" data-show-count="false">Follow @polymerjs</a>)
- [Facebook] (https://www.facebook.com/polymerjs)

### Some ways to help:

- **Test the elements and provide feedback**: We would love to hear your feedback on anything related to the elements, like features, API and design. The best way to start is by trying them out. And to get a quick response, either drop a question/comment on the chat or open an issue in GitHub.
- **Report bugs**: File issues for the elements in their respective GitHub projects.
- **Send pull requests**: If you want to contribute code, check out the development instructions below.

We encourage you to read the [contribution instructions by GitHub](https://guides.github.com/activities/contributing-to-open-source/#contributing) also.

## License

MIT License
