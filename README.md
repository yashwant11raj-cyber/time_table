# Ex04 Time Table

# Date: 21/10/26

# AIM

To write a html webpage page to display your slot timetable.

# ALGORITHM

## STEP 1

Create a Django-admin Interface.

## STEP 2

Create a static folder and insert HTML code.

## STEP 3

Create a simple table using `<table>` tag in html.

## STEP 4

Add header row using `<th>` tag.

## STEP 5

Add your timetable using `<td>` tag.

## STEP 6

Execute the program using runserver command.

# PROGRAM

timetable.html

```
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Student Timetable</title>
    <style>
      body {
        font-family: Arial, sans-serif;
        background-color: #f4f4f4;
      }
      h1 {
        text-align: center;
        font-family: Arial, sans-serif;
      }

      table,
      th,
      td,
      tr {
        border: 2px solid black;
        border-collapse: collapse;
      }
      table td,
      table th {
        text-align: center;
        vertical-align: middle;
        padding: 8px;
      }
      table {
        margin-left: auto;
        margin-right: auto;
        margin-top: 20px;
        width: 90%;
      }
      span {
        writing-mode: vertical-rl;
        text-orientation: upright;
        letter-spacing: 2px;
      }
      .timetable-main {
        background-color: #00e5ff;
      }
      .timetable-main tr:first-child th {
        background-color: #ffff00;
        color: black;
      }
      .timetable-main td:first-child {
        background-color: #ffff00;
        font-weight: bold;
      }
      .subject-details {
        background-color: #ffffff;
      }
      .subject-details th {
        background-color: #ffffff;
        color: black;
      }
      .subject-details td {
        text-align: left;
        padding-left: 12px;
      }
      .subject-details td:first-child,
      .subject-details td:nth-child(2) {
        text-align: center;
        padding-left: 0;
      }
      .subject-details {
        margin-bottom: 40px;
      }
      .free {
        background-color: #c8f7c5;
        font-weight: bold;
      }
      .timetable-main tr:hover td:not(:first-child) {
        background-color: #80f0ff;
      }
    </style>
  </head>
  <body>
    <h1>Student Timetable - Semester 1</h1>
    <table class="timetable-main">
      <caption>
        <b>Weekly Timetable</b>
      </caption>
      <tr>
        <th>Day</th>
        <th>8:00 AM to 9:30 AM</th>
        <th>9:30 AM to 9:45 AM</th>
        <th>9:45 AM to 11:15 AM</th>
        <th>11:15 AM to 12:00 PM</th>
        <th>12:00 PM to 1:15 PM</th>
        <th>1:15 PM to 2:45 PM</th>
        <th>2:45 PM to 3:00 PM</th>
        <th>3:00 PM to 4:30 PM</th>
      </tr>
      <tr>
        <td><u>Monday</u></td>
        <td>FWAD</td>
        <td rowspan="6">
          <b><span>Break</span></b>
        </td>
        <td>Pyt</td>
        <td rowspan="6">
          <b><span>Lunch Break</span></b>
        </td>
        <td rowspan="6">
          <b><span>Mentor Meeting</span></b>
        </td>
        <td class="free">Free hour</td>
        <td rowspan="6">
          <b><span>Break</span></b>
        </td>
        <td>EMPD</td>
      </tr>
      <tr>
        <td><u>Tuesday</u></td>
        <td>FWAD</td>
        <td class="free">Free hour</td>
        <td>CCC</td>
        <td class="free">Free hour</td>
      </tr>
      <tr>
        <td><u>Wednesday</u></td>
        <td>CCC</td>
        <td class="free">Free hour</td>
        <td class="free">Free hour</td>
        <td class="free">Free hour</td>
      </tr>
      <tr>
        <td><u>Thursday</u></td>
        <td>Pyt</td>
        <td>Comp Arch</td>
        <td>Jap Lang</td>
        <td class="free">Free hour</td>
      </tr>
      <tr>
        <td><u>Friday</u></td>
        <td>Pyt</td>
        <td class="free">Free hour</td>
        <td>Jap Lang</td>
        <td class="free">Free hour</td>
      </tr>
      <tr>
        <td><u>Saturday</u></td>
        <td>Comp Arch</td>
        <td>CD</td>
        <td>FWAD</td>
        <td>EMPD</td>
      </tr>
    </table>
    <table class="subject-details">
      <caption>
        <b>Subject details</b>
      </caption>
      <tr>
        <th><b>Subject Code</b></th>
        <th><b>Subject Reference</b></th>
        <th><b>Subject Name</b></th>
        <th><b>Faculty</b></th>
      </tr>
      <tr>
        <td>19AI414</td>
        <td>FWAD</td>
        <td>Fundamentals of Web Application Development</td>
        <td>Berlin Magthalin R</td>
      </tr>
      <tr>
        <td>19AI301</td>
        <td>Pyt</td>
        <td>Python Programming</td>
        <td>Abi</td>
      </tr>
      <tr>
        <td>19CS418</td>
        <td>CCC</td>
        <td>Cyber law and compliance</td>
        <td>Ramesh K</td>
      </tr>
      <tr>
        <td>19CS305</td>
        <td>Comp Arch</td>
        <td>Computer Architecture</td>
        <td>Elangovan D</td>
      </tr>
      <tr>
        <td>19GE624</td>
        <td>Jap Lang</td>
        <td>Japanese Language</td>
        <td>Subashini D</td>
      </tr>
      <tr>
        <td>19AI303</td>
        <td>EMPD</td>
        <td>Engineering mechanics and Project Development</td>
        <td>Vinothraj U</td>
      </tr>
      <tr>
        <td>19EY708</td>
        <td>CD</td>
        <td>Career Development Skills</td>
        <td>Immanuel G</td>
      </tr>
    </table>
  </body>
</html>


```

# OUTPUT

Weekly Timetable Output:
![Weekly Timetable details](<Experiment-4/Screenshot 2026-11-26 101953.png>)
Subject details Output:
![Subject details](<Experiment-4/Screenshot 2026-11-26 102003.png>)

# RESULT

The program for creating slot timetable using basic HTML tags is executed successfully.
