# AI Agents/Vibe Coding Workshop

**[AiEdge Summit 2025](https://aiedgesummit.com)**
Workshop by Dan Klosterman and Shane Thomas

## Workshop Resources

### 📊 Workshop Slides

Access the presentation slides here:
[Workshop Slides](https://docs.google.com/presentation/d/1XaOjWcZegqDJE9z_PJ87czGq6hzsDQwQiK7PR292tRU/edit?usp=sharing)

### 💻 Replit.com Core Plan Activation

To get started with the workshop exercises:

1. Sign up or log in to [Replit.com](https://replit.com)
2. Click the "Upgrade to Replit Core" button in the bottom left
3. Click "Continue with Core"
4. Copy and paste the promo code:
   ```
   MASTRAAIEDGE
   ```
5. Enter your payment information
6. Your Replit Core plan is now active for the workshop

---

## Workshop Projects

### PROMPT 1: News Digest Agent

Copy and paste the following prompt to get started:

```
A time-based automation agent that researches and compiles Sioux Falls news from the past week, then emails a daily summary with relevant links every morning at 7am.

Core Capabilities:

Research current Sioux Falls news from multiple sources using web scraping
Filter and analyze news from the past 7 days for relevance
Generate concise summaries of key stories with source links
Send formatted email reports with news summaries and links
Required Tools/Integrations:

Web scraping tools for local Sioux Falls news sources
Email service integration (SMTP/email API)
News analysis and summarization capabilities
Date/time filtering for recent articles
Trigger Type: Time-based scheduling (daily at 7:00 AM)

Expected Autonomous Behavior:
The agent will automatically wake up at 7am daily, search for Sioux Falls news from the past week across multiple sources, analyze and summarize the most important stories, then compile and send an email report with headlines, summaries, and source links without any manual intervention.
```

---

### PROMPT 2: Jarvis AI Assistant

**Prerequisites:**
- Telegram account and [bot token](https://t.me/BotFather)
- [Exa API key](https://dashboard.exa.ai/home) for search

Copy and paste the following prompt to get started:

```
PROMPT:

Build a Telegram-based personal AI assistant named "Jarvis" (inspired by Iron Man's AI) using the agent_stack blueprint with the following exact specifications:

ARCHITECTURE REQUIREMENTS:

ONE Mastra Agent containing all business logic and tools
ONE Mastra Workflow with exactly TWO steps:
Step 1: Call agent.generate() only (no other logic)
Step 2: Send response to Telegram only (no other logic)
Telegram trigger registered to call the workflow on new messages

AGENT CONFIGURATION:

Name: "Jarvis - Personal AI Assistant"
Model: Use Replit AI Integrations with GPT-5 (no API key required, billed to credits)
Follow the OpenAI AI Integrations blueprint setup for Mastra/Agent Stack
Memory: PostgreSQL-backed conversation memory with thread support, generateTitle: true, lastMessages: 20
Personality: Professional yet personable assistant, efficient, occasionally witty, prioritizes user needs

THREE REQUIRED TOOLS:

Google Calendar Tool:

Read upcoming events from user's Google Calendar
Create new calendar events with attendee invites
Use Google Calendar integration

Gmail Tool:

Draft emails in user's Gmail account
Use Gmail integration

Research Tool:
- Use Exa search API (exa-js package already installed) for high-quality semantic web searches
- Ask for EXA_API_KEY secret and store it securely
- Perform semantic searches using exa.searchAndContents() method
- Combine Exa results with AI's built-in knowledge
- Provide summaries with sources and direct URLs to content

DEPLOYMENT FIX (CRITICAL):

Modify scripts/build.sh to include export NODE_OPTIONS="--max-old-space-size=4096" before exec mastra build to prevent memory errors during deployment

TELEGRAM INTEGRATION:

Bot responds to direct messages and mentions
React with hourglass emoji when processing
Use Telegram HTTP API for sending messages
Thread ID format: telegram/{chatId}

EXTENSIVE LOGGING:

Add detailed logger statements throughout all tools, agent, and workflow steps
Use emojis in logs (🔧, 📝, ✅, ❌, etc.) for easy tracking
After building, test the agent in the Playground tab, then suggest deployment. Make sure the bot will work immediately after deployment without "AI SDK v4 compatibility" errors.
```

---

## Getting Help

If you have questions during the workshop, please ask the instructors or refer to the workshop slides for additional guidance.
