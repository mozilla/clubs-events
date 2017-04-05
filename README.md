# Welcome!

This is the Mozilla Clubs Event Reporting tool. It allows users to submit and browse through event reports.

## How does it work?

1. Users submit an event report using a Google Form
  * [The Google Form](http://goo.gl/forms/wDc7b8AqI3)
2. The data from the form is then added to the Spreadsheet
  * [The Spreadsheet](https://docs.google.com/spreadsheets/d/1QHl2bjBhMslyFzR5XXPzMLdzzx7oeSKTbgR5PM8qp64/edit#gid=1045576576)
3. We access the spreadsheet using a special URL and get the data
4. We display the data on the Dashboard
  * [Event Report Dashboard](http://mozilla.github.io/clubs-events/)

## Making your own

You can make your own version of the clubs event reporter by following the steps below.

### Setting up the form and spreadsheet

1. Create your own copy of the Google Form
    * Here is the blank form - [https://goo.gl/SsBlGq](https://goo.gl/SsBlGq)
  - On this form, select the 3-dot menu in the top-right corner and select ``Make a copy``
2. The new form should open in your browser
2. On the new form, select the **Responses Tab**
3. Click the green spreadsheet icon and click **Create** to make a new spreadsheet for your data
4. Your new spreadsheet should open in the browser
5. Open the **File** menu and then click **Publish to the web...**
6. Ensure that **Entire Document** and **Web Page** are selected and click **Publish**
  * Your spreadsheet will now be accessible by the event reporter tool
7. Submit an entry with your form and check that it made it to the spreadsheet.

### Setting up your own repo

1. Create your own version of the Event Reporter by forking this repo
  * To do so, click **Fork** in the top-right of the screen
2. You can view the event reporter in two ways...
  * You can look load the ``index.html`` page in your browser
  * Or, you can start a local server on your computer and view it via ``localhost``
    * On a mac, type ``python -m SimpleHTTPServer 8008`` in your terminal in the same folder as the event reporter
    * Now you'll be able to access it in your browser via ``localhost:8008``

### Connecting your event reporter to your spreadsheet

To do this, we'll need to find out the ID of your spreadsheet.

1. Open your spreadsheet and look at the URL, it might look something like this
  * ``https://docs.google.com/spreadsheets/d/1Nijr4qehpJ7LXuMGmQ4fNCprt2F8rCTVdOte9DXinTw/edit#gid=1720373540``
2. The ID is is the long string of numbers and letters after ``/d``
  * In our the example above, it's ``1Nijr4qehpJ7LXuMGmQ4fNCprt2F8rCTVdOte9DXinTw``
3. Copy that ID to your clipboard and open the ``js/config.js`` file
4. Change the ``sheetID`` variable to your new ID.
5. Now load up your event reporter, and see if your event appears.
  * If it doesn't, try using the other version of the ``sheetURL`` variable.
  * Just leave the one you want to try uncommented
  * Sometimes the URL needs to have a different syntax, so that's why we have a few options
6. Check your event reporter again to make sure it worked.

