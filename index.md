# Camden Pendergrass

##IT, Programming, Web Development

## Languages
Python, C#, C++, JavaScript, HTML, CSS, MySQL, PostgreSQL

# Projects

## Repair Tracking Software
Repair Tracking Software is a full stack, serverside and front end website I built for Madison Academy in Python and Python/Flask. This software links with several different program API's, including Google, jotform, and FreshDesk, to streamline the IT department's device repair process.

### Server End
Once a repair request form has been submitted into Jotform, it is linked to a Google Sheets page. This page is checked 350 times a minute for new cells. If there are more cells than the previous check, the server iterates through the new cells and stores them into arrays. These arrays are then pushed through 3 main functions. 

1. The first takes a PNG file with a repair form on it and appends the information stored in the array. After modifications, the array contains a location variable for which repair station the form was filled out at. Each station has a printer that has been registered to the linux server. The variable calls the correct printer and prints out the PNG to be attached to the broken device.
2. The array is sent to a function that adds it to a sqlite database to be stored for long term use.
3. The program uses API calls in both the FreshDesk software, and in the website portion that is under development. A ticket is created for the repair with the name of the person, their unique ID, and the reason for repair, along with the PNG file.

### Front End
The front end is an internal website rts.macademy.org that's only viewable when on the campus LAN. On the main page there is a dashboard 3 main sections. A pie chart with the reason for repair percentages (currently broken screen is highest at 36%), a scrollable div that contains relevant information such as new repairs, modification to current repairs, and closed repairs, and a collapsable hamburger bar with quick solutions for repeated repairs. At the top there is a navigation bar that allows you to go to a sub page with a blog style ticket layout. From there you can open individual tickets and modify information, attach images, or close it. There is also a reports tab on the nav bar which allows you to run reports on cost, repair types, and each device with all its previous repair logs.

## Strength Programming

Full stack website in active development. Currently has secure logins with SHA256 encryption with salt and pepper and dynamic database creation for customers. When a new customer joins they are linked to a users database and a programs database. The programs database stores the unique ID for each program and allows for multiple users to join under one program, and store a super admin. After these SQL lines are added to those tables, the unique ID is used with a letter number conversion and then sent as an SQL statement to the PostgreSQL cluster to create a new database. When a user logs in it passes these through to grab the correct database for that user. From all my testing this is SQL injection proof, but if someone manages to pass an injection statement, they will be locked to only the database for that program. Currently working on live updating tables to the SQL database to allow for roster uploads, workout programs, and rack assignments.

## DiscordDND

DiscordDND is a discord bot programmed in Python. It allows for a person to add the bot DiscordDND#0625 to their server. After it is added it grabs the server ID and all channel ID's and stores them in a class object which is added to a database. It then asks if the admin would like the server to be configured for DND or if they would like to add a custom configuration. Either choice allows for specific channels to be stored and referenced under the class object. After setting themself ad DM they are able to assign PC roles to server users with the command ~setPC [discord name]. Once PC roles have been assigned, each user can go through the character upload, or character creation process. If they have chosen character upload, they are able to pass through all the stats for their character sheet and it is added to a class object under their Discord ID and stored in a database with the server it's being used in as a variable. If they chose character creation, the server responds with prompts and dropdown selections to walk newer players through a DND character sheet creation. After this it follows the same steps as the character upload. The character object can be refereced in different servers and will be cloned to allow characters stats to be modified per server. Currently under development and working on linking to an enemies api to allow for custom fighting with all math and stats handled on the server end.


<script src="http://code.jquery.com/jquery-1.4.2.min.js"></script> <script> var x = document.getElementsByClassName("creds"); setTimeout(() => { x[0].remove(); }, 10); </script>
