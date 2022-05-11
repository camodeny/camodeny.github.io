# Camden Pendergrass

IT, Programming, Web Development

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


```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

