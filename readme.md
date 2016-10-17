# Calendar Kata

This kata is a calendar rendering problem. The input is a list of
events and the output is a calendar display similar to Google Calendar.

*Part 1*

Transform a series of events for a single day.

Each event object consists of a start and end time (measured in minutes),
as well as a unique id. The start and end time of each event will be transformed
to cordinates from 0 to max height. And event width would be mapped from 0 to max width,
within the 1 day interval. The start time will be less than the end time.

Events will be placed in a grid. Grid is made of:
  - x axis, interval of 1 day
  - y axis, interval from 6am to 6pm

The objects should be laid out so that they do not visually overlap.
If there is only one event at a given time slot, its width should be maximum width.
If there are multiple events not visually overlaping they should be one bellow another one.

There are 3 major constraints:

    Every colliding event must be the same width as every other event that it collides width.
    An event should use the maximum width possible while still adhering to the first constraint.

Given events A B C and D, they should be layed out as:

    -------
    |  A  |-------
    -------|     |
           |  B  |
    -------|     |
    |  C  |-------
    -------

    --------------
    |      D     |
    --------------

*Part 2*

Use transformations from Part I to create a web page that is styled with the following calendar events:

  * An event that starts at 6:00 and ends at 11:30
  * An event that starts at 7:00 and ends at 13:20
  * An event that starts at 13:00 and ends at 19:00
  * An event that starts at 20:00 and ends at 21:00
