AI-Powered IT Support Chatbot

🚀 Overview

This project is an AI-driven IT Support Chatbot that helps IT teams troubleshoot issues automatically. The chatbot leverages GPT-4, LangChain, FastAPI, and Jira API integration to answer IT-related queries and even create Jira tickets for unresolved issues.

🔹 Features

✅ Uses GPT-4 & LangChain for IT problem diagnosis✅ Jira API Integration: Creates support tickets automatically✅ FastAPI Backend: Lightweight and high-performance API server✅ Deployable on Slack, Telegram, or Web Apps✅ Cloud Deployable: Run on AWS, Heroku, or any cloud platform

🛠️ Tech Stack

Backend: FastAPI (Python)

AI & NLP: OpenAI GPT-4, LangChain

Database (Optional): PostgreSQL / MongoDB

Integration: Jira API, Slack API

Deployment: AWS EC2, Heroku, Render, Railway

🚀 Installation & Setup

1️⃣ Clone the Repository

git clone https://github.com/Alisid07/AI-IT-Support-Chatbot.git
cd AI-IT-Support-Chatbot

2️⃣ Set Up a Virtual Environment

python -m venv venv
source venv/bin/activate  # macOS/Linux
venv\Scripts\activate  # Windows

3️⃣ Install Dependencies

pip install -r requirements.txt

4️⃣ Set Up Environment Variables

Create a .env file in the root directory and add:

OPENAI_API_KEY=your_openai_api_key
JIRA_API_URL=https://your-jira-instance.atlassian.net/rest/api/2/issue
JIRA_AUTH_EMAIL=your-email
JIRA_API_TOKEN=your-jira-api-token

5️⃣ Run the FastAPI Server

uvicorn main:app --reload

API is now running at: http://127.0.0.1:8000

🔥 API Endpoints

Endpoint

Method

Description

/chat

POST

Get AI response for IT queries

/create_ticket

POST

Create a Jira ticket for IT issues

☁️ Deployment Guide

🔹 Deploy on Heroku

Install the Heroku CLI:

npm install -g heroku
heroku login

Initialize a Git repository (if not already done):

git init
git add .
git commit -m "Deploying AI IT Chatbot"

Create a Heroku app and deploy:

heroku create ai-it-chatbot
git push heroku main

Open the deployed app:

heroku open

🔹 Deploy on AWS EC2

Launch an EC2 instance (Ubuntu recommended)

SSH into the server:

ssh ubuntu@your-ec2-ip-address

Install Python & dependencies:

sudo apt update && sudo apt install python3-pip -y
pip install fastapi uvicorn openai requests langchain python-dotenv

Clone the repo and start the server:

git clone https://github.com/Alisid07/AI-IT-Support-Chatbot.git
cd AI-IT-Support-Chatbot
uvicorn main:app --host 0.0.0.0 --port 8000

Open port 8000 in AWS Security Groups.

💬 Slack Integration (Optional)

Create a Slack App at Slack API

Enable chat:write and commands permissions

Install the bot into your Slack workspace

Add the Slack API token in .env:

SLACK_BOT_TOKEN=your-slack-bot-token

Modify main.py to send messages:

from slack_sdk import WebClient
slack_client = WebClient(token=os.getenv("SLACK_BOT_TOKEN"))

def send_slack_message(channel, message):
    slack_client.chat_postMessage(channel=channel, text=message)

🎯 Future Enhancements

✅ Add Database Support (MongoDB/PostgreSQL) for saving chat history✅ Enable AI-driven automated responses for Jira ticket handling✅ Extend support for multilingual responses✅ Add OAuth authentication for enhanced security

📜 License

This project is open-source under the MIT License.

🙌 Contributing

PRs are welcome! If you’d like to improve this chatbot, fork the repo and submit a pull request. 🚀

👨‍💻 Author

💡 Developed by: @Alisid07

🎉 Enjoy Your AI-Powered IT Support Chatbot! 
