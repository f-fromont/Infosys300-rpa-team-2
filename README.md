# Infosys300-rpa-team-2

Software: UIPath 
Link to Github: [https://github.com/f-fromont/Infosys300-rpa-team-2](https://github.com/f-fromont/Infosys300-rpa-team-2)

## Bot Purpose

The following instructions will be used to access the Group mailer BOT created by Team 2 using UIPath. The purpose of the BOT is to streamline the process of group communication and create an email with all group memebers as a first point of contact


## Bot Process

Please ensure you are using the latest version of UIPath and all required dependencies are installed, these are outlines in the project.json, but also listed below:
- "Google.Apis.Gmail.v1": "[1.55.0.2510]",
- "Microsoft.Activities.Extensions": "[2.0.6.9]",
- "UiPath.Excel.Activities": "[2.11.4]",
- "UiPath.Mail.Activities": "[1.12.3]",
- "UiPath.System.Activities": "[21.10.5]",
- "UiPath.UIAutomation.Activities": "[21.10.6]"

Unzip the file if not already done so, and open the project in UIPath

1. The BOT will need to have access to a chome browser that is logged into a canvas course. We have setup a test course at [https://canvas.instructure.com/login/canvas](https://canvas.instructure.com/login/canvas)

The following login details can be used to access the course we used for testing
Login: rpa.informer@gmail.com 
Password: infosys300

2. Once logged in you can then start the UIPath process, running the "main.xaml" and the BOT will ask you to enter in some details to customise the email that is being sent out to students
Set the email header 
Set the email body
If you don't enter any text, a default text will be used instead.

3. You will then be shown a display of what the email will look like when being sent to students, press Okay to move onto the data collection step. You will be prompted to once again ensure that a chrome tab is open to a canvas course page, a screenshot is included to below to show what page the bot needs you to be on. You will also need to use a chrome that has the UIPath extension present.

![image](https://user-images.githubusercontent.com/66896513/196074923-ac2fd5a7-29a8-412b-a24c-170b3a97bce6.png)


4. The bot will then navigate to the people tab from the homepage, and from there it will go into the group tab where it will then download an excel spreadsheet that contains the student group data.

5. Once the file has been downloaded, the bot will begin processing the rows and build up a dictionary of the different groups with the group name as a key, and the value will be a list of strings, which are the student emails of each student in a particular group.

6. Once this collection is built up, it will return the information to the final step of the process. Follow the prompts to allow it to continue

7. The final step is where the bot uses a Gmail integration to send customised emails using the information set at the start, these emails will be sent one at a time to all the groups. You will need to login with the RPA gmail, and allow it to send emails, the checkboxes are shown below:
![image](https://user-images.githubusercontent.com/66896513/196076347-7abba8dd-6e4a-4ed5-8da4-b33d77b8ef89.png)


8. The bot will then inform you that it has finished executing, and emails will have been sent to the students, an example is shown below
![image](https://user-images.githubusercontent.com/66896513/196075156-369cedc0-9bca-4d8f-a8b1-3b12d9962dcf.png)

## Constraints

- Please be aware that the bot does need someone with lecturer or higher access of a canvas course where student information is visible.
- The bot also only works on chrome browsers
- The bot will also only work on default canvas course domains, the university of auckland domain for canvas courses is not supported.
- The bot will also need access to a gmail account, one was setup for this purpose and the credentials are listed below:

Gmail Account:
Email: rpa.informer@gmail.com
Password: infosys300



