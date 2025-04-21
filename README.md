# WebReminder

 Google Auth + Local Events + SMS Notification System + Cron job
Overview
This project is a simple application that allows users to:

•	Authenticate using Google Sign-In

•	Add and manage events locally (stored in memory or a local database)

•	Send SMS notifications using a third-party SMS gateway API (like Twilio)

This part of the project runs a scheduled Cron job that:
•	Checks all stored events every hour (or custom schedule)
•	Filters events occurring within the next 24 hours
•	Sends SMS reminders to the associated phone numbers using your SMS API (like Twilio)


## Features
1.	Google OAuth 2.0 authentication

2.	add, view, edit, and delete local events

3.	Send SMS reminders or confirmations for events

simple, clean, modular code structure

created helpers and libraries 

 ##Tech Stack
 Framework codeigniter 3.1
 
Backend: PHP Mysql , Codeigniter

Frontend: Bootstrap

Authentication: Google OAuth 2.0

SMS API: Twilio

Database: MySql

📦 Installation

🔐 Google Authentication Setup
Go to Google Cloud Console

Create a new project or select an existing one

Navigate to APIs & Services > Credentials

Click Create Credentials > OAuth Client ID

Set the application type to Web Application

Add your Authorized redirect URIs


 Adding Events Locally
Events are stored locally (in memory, a file, or a lightweight database).
Each event should include:

Title

Date & Time

Description

Phone number (for SMS notifications)

Example Event JSON:

json
Copy
Edit
{
  "id": 1,
  "title": "Team Meeting",
  "datetime": "2025-04-22T14:00",
  "description": "Discuss quarterly roadmap",
  "phone": "+1234567890"
}
📲 Sending SMS
This project uses Twilio (or your preferred SMS provider) to send event-related messages.

SMS Workflow:

After adding or updating an event, an SMS notification is sent to the specified phone number.
"Reminder: Team Meeting on April 22 at 2:00 PM"
Make sure your SMS API credentials are correctly set in the .env file.

API Endpoints
GET /events — List all events

POST /events — Add new event

PUT /events/:id — Update event

DELETE /events/:id — Remove event

POST /send-sms — Send SMS manually




