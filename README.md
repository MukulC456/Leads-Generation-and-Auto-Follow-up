# Leads-Generation-and-Auto-Follow-up

# Overview
I have created n8n workflow automation for leads generation and follow-up process. It captures leads through a form, enriches them with company data, classifies them into different categories, and sends appropriate follow-up sequences automatically.

# Key Features:
•	AI-powered lead classification (Demo-ready, Nurture, Drop)
•	Automatic lead enrichment with company data
•	Intelligent email responses and follow-up sequences
•	Automated demo scheduling for qualified leads
•	Complete lead logging in Google Sheets
•	AI assistant for immediate query responses

# Tools used
1.	n8n Instance: Self-hosted (future deployment in cloud)
2.	Google Gemini Key: For AI-powered features
3.	Google Workspace Account with:
•	Gmail access
•	Google Sheets
•	Google Calendar
4.	Basic understanding of your Ideal Customer Profile (ICP)

# Quick Start Guide:
Step 1: Import the Workflow
1.	Copy the workflow JSON
2.	Import into your n8n instance
3.	The workflow will appear with all nodes connected

Step 2: Configure Credentials
You'll need to set up the following credentials:
•	OpenAI API: For AI agents and classification
•	Gmail OAuth2: For sending emails
•	Google Sheets OAuth2: For lead logging
•	Google Calendar OAuth2: For demo scheduling

Step 3: Create Your Lead Log Sheet
Create a Google Sheet with these columns:
•	Date
•	Name
•	Email
•	Company
•	Job Title
•	Message
•	Number of Employees
•	Industry
•	Geography
•	Annual Revenue
•	Technology
•	Pain Points
•	Lead Classification

Step 4: Update Configuration Nodes
1.	Replace Sheet ID: Update all Google Sheets nodes with your sheet ID
2.	Set Escalation Email: Replace "your-email@company.com" with team's email
3.	Configure ICP Criteria: Edit the "Define ICP and Lead Criteria" node

# Lead Classification Setup
Define ICP (Ideal Customer Profile)
Edit the "Define ICP and Lead Criteria" node to set criteria:
ICP Criteria Example:
- Company Size: 50+ employees
- Industry: SaaS, Finance, Healthcare, Manufacturing
- Geography: North America, Europe
- Pain Points: Manual processes, compliance needs, scaling challenges
- Annual Revenue: $5M+
  
1.Demo-Ready Criteria:
High-intent prospects who meet multiple qualifying factors:
•	Large company size (your threshold)
•	Clear pain points mentioned
•	Urgent timeline
•	Budget authority indicated
•	Specific solution requests

2.Nurture Criteria:
Prospects with future potential:
•	Meet basic size requirements
•	In target industry
•	General interest expressed
•	Planning future implementation
•	Exploring options

3.Drop Criteria:
Only drop leads that clearly don't fit:
•	Outside target geography
•	Wrong industry (B2C if you're B2B)
•	Too small with no growth
•	Already with competitor
•	Spam or test messages

# Email Customization
Customize Follow-Up Sequences:
- Demo-Ready Sequence:
1.	Immediate calendar invitation
2.	Personalized demo confirmation
3.	Meeting reminder (optional)
- Nurture Sequence:
1.	Welcome email with resources
2.	Educational content (Day 2)
3.	Webinar/event invitation (Day 3)
4.	Demo offer (Day 4)
- Drop Message:
•	Polite acknowledgment
•	Clear explanation
•	Keep door open for future

# Calendar Integration:
•	Set available meeting times
•	Configure meeting duration
•	Add buffer times
•	Set timezone handling
