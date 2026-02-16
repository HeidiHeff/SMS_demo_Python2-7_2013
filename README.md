**SMS Healthcare Quiz Demo (2013)**
A Flask + Twilio SMS demonstration application built in 2013 to showcase interactive text-based quizzes using the Twilio API.

Originally demonstrated at Coding Dojo on September 27, 2013.

**Overview**
This project is a server-side SMS quiz application that:
  - Accepts inbound SMS messages via Twilio
  - Tracks user session state
  - Runs a 5-question healthcare knowledge quiz
  - Scores responses and returns results via SMS
  - Was deployed to Heroku using Gunicorn

It demonstrates early integration of:
  - REST API consumption
  - Stateful session management in Flask
  - Twilio’s TwiML response system
  - Cloud deployment via Heroku

**Tech Stack (Historical Context)**
Python 2.7.4
Flask 0.10.1
Twilio Python SDK 3.5.4
Gunicorn 18.0
Heroku (PaaS)
Linux (Ubuntu 13.04 dev environment)

**How It Works**
1) A user sends a text message to a Twilio phone number.
2) Twilio makes an HTTP request to the /sms/ route.
3) The Flask app:
  - Tracks question state in session
  - Compares submitted answers
  - Maintains a running score
4) The application responds with TwiML to send SMS messages back to the user.
The quiz consists of five multiple-choice questions related to U.S. healthcare policy at the time.

**Project Structure**
Procfile
app_sms_demo.py
requirements.txt
- app_sms_demo.py — Main Flask application
- Procfile — Gunicorn entry point for Heroku
- requirements.txt — Pinned dependency versions (2013 era)

**Running This Project (Historical Setup)**
⚠️ This project was built using Python 2.7 and outdated package versions.
To run today you would need:
  - A Python 2.7 virtual environment
  - Twilio account credentials configured via environment variables
  - Updated Twilio SDK usage (modern Twilio uses different imports)
Example (legacy style):
pip install -r requirements.txt
gunicorn app_sms_demo:app

**Modernization Notes**
To bring this project up to date today, you would:
  - Upgrade to Python 3.11+
  - Refactor Twilio integration using twilio.twiml.messaging_response
  - Replace TwilioRestClient with Client
  - Remove hardcoded SECRET_KEY
  - Add environment variable configuration
  - Update Flask session security
  - Replace deprecated TwiML response patterns
This repository is preserved as a historical demo artifact rather than an actively maintained production application.

**Why This Project Matters**
At the time of development (2013), this project demonstrated:
  - Real-time SMS API interaction
  - Cloud deployment
  - Stateful web architecture
  - Working REST integrations
  - Public demo capability
  - It reflects early full-stack development skills and API integration experience.

**Status**
Archived. Educational / historical reference.
