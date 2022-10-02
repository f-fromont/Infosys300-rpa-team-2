# Infosys300-rpa-team-2
The implementation of a group RPA project for the Infosys300/softeng762 course

## Main tasks / Flow

1. Configuration Screen
- Allows for customisation of email to be sent to the students
- Set email header
- Set email body
- Selection of any modes or forms of communication, if implemented (lecturer screen use, or robot credentials perhaps)

2. Student group data collection
- Either through the lecturer being logged in, or through the robots own credentials, login to Canva
- Navigates to group tab
- Use HTML elements to select all tags and grab the id's of the student tags, this gives group id & user id
- Build up a dictionary which maps a group_id, to all the student id's
- Use HTML elements to select people tags, and grab all id's and user email's
- Build up a dictionary which maps a user_id, to an email address (possible extra identifiy information)
- Handle any cases where a user is not in a group, or does not have a form of communication

3. Emailing system
- Take in the email template shown at start
- Take in the maps build up
- For each group id, go through user_id's and grab emails, add to a list
- Create an email, 
- set the header to what lectuerer has specified,
- set the body to what the lecturer has specified,
- send the email,
- if any error, make sure to log and showcase to whoever is running bot

4. Email responses - optional
- maybe monitor any emails being returned and either send a automated no-response, or maybe send an email to designated lecturer
