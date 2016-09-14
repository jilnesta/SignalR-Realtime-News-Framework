# SignalR-Realtime-News-Framework
A framework for sending and acknowledging real-time news updates to users.

#Introduction
This Framework helps an organization or user to sends real time news to clients. The framework can be easily added to any webpage easily and supports all browsers. Data is integrated using SQL server/Web-client UI. News updates data can be sent either using a web-client HTML UI page or by adding data in the respective tables in the database directly.

#Setup
To setup the project, please install visual studio and open the SignalRChat.sln from the extracted folder. Also create an instance in you localhost database names 'signalr' and create two tables User_tbl  and News_tbl.
Basically you can categorize news into various categories like sports, entertainment etc. I have named them like 'CategoryA', 'CategoryB' etc. User can subscribe to any category they want to. These information is present in User_tbl. Kindly follow the attached images for the same.
News_tbl contains category and news data to be sent for this category. 
User_tbl stores the email ID’s of user along with the category they are subscribed to for news.

#Database Setup
To make the framework work with database. You need to set up service broker also as it uses the same to send news from database.
1. To setup service, just find and execute servicebroker.sql in your SQL server.

#Getting Started
To make this framework work you need to follow below simple steps.
1. Launch the visual studio project on any of the browser.
2. It will open a pop up that will ask you to fill a category. Type any valid category that should match with your News_tbl and User_tbl entries for the same.
3. Note down your port number on which your IIS hosted your solution on local browser. 
4. Open Client.html file from the extracted folder and replace your current port number with the hardcoded port number in that file i.e. 'http://localhost:13577/signalr'.
5 You will also observe that 'username' variable is hardcoded in Client.html file with value 'vishalsinghdeepak@gmail.com'. Change it to any valid id that is present in your User_tbl. You can also dynamically fetch user's email ID from user's current browser and replace username with that to make it work dynamically for all users.
6. Save and Launch Client.html file from the extracted folder in any browser. 
7. Send any message from index.html and you will observe that a pop up will come in Client.html.
8. You can also send messages from database by making entry in News_tbl. It will also send the news to Clent.html directly.
9. User can click on the green pop up to acknowledge the news and also can write any comments for the same.
10. You will observe index.html displays real-time acknowledgments of users also.

#Performance
The Framework is very smooth and sends updated in real-time. Even if you send news from database you won't feel any lag in data display. It also captures user's acknowledgement details and display on the server. It supports mostly all the browsers.

#Scalability
The framework works well for a large of user. You can plug-in client side code i.e Client.html easily anywhere on any webpage. As it contains mainly JavaScript code that can be plugged-in anywhere.
