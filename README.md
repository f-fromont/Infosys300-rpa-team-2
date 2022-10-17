# Infosys300-rpa-team-2

Software: UIPath 

## Bot Purpose

The following instructions will be used to access the Group mailer BOT created by Team 2 using UIPath. The purpose of the BOT is to streamline the process of group communication and create an email with all group memebers as a first point of contact

## Bot Process

The BOT will need to have access to a chome browser that is logged into a canvas course. We have setup a test course at [https://canvas.instructure.com/login/canvas](https://canvas.instructure.com/login/canvas)

The following login details can be used to access the course we used for testing
Login: rpa.informer@gmail.com 
Password: infosys300

Once logged in you can then start the UIPath process and the BOT will ask you to enter in some details to customise the email that is being sent out to students
Set the email header 
Set the email body

If you don't enter any text, a default text will be used instead.

You will then be shown a display of what the email will look like when being sent to students, press Okay to move onto the data collection step. You will be prompted to once again ensure that a chrome tab is open to a canvas course page, a screenshot is included to below to show what page the bot needs you to be on. You will also need to use a chrome that has the UIPath extension present.

![image](https://user-images.githubusercontent.com/66896513/196074923-ac2fd5a7-29a8-412b-a24c-170b3a97bce6.png)


The bot will then navigate to the people tab from the homepage, and from there it will go into the group tab where it will then download an excel spreadsheet that contains the student group data.

Once the file has been downloaded, the bot will begin processing the rows and build up a dictionary of the different groups with the group name as a key, and the value will be a list of strings, which are the student emails of each student in a particular group.

Once this collection is built up, it will return the information to the final step of the process. 

The final step is where the bot uses a Gmail integration to send customised emails using the information set at the start, these emails will be sent one at a time to all the groups.

The bot will then inform you that it has finished executing.

## Constraints

- Please be aware that the bot does need someone with lecturer or higher access of a canvas course where student information is visible.
- The bot also only works on chrome browsers
- The bot will also only work on default canvas course domains, the university of auckland domain for canvas courses is not supported.
- The bot will also need access to a gmail account, one was setup for this purpose and the credentials are listed below:

Gmail Account:
Email: rpa.informer@gmail.com
Password: infosys300



