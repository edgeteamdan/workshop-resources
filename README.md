# AI Agents/Vibe Coding Workshop

**AiEdge Summit 2025**
Workshop by Dan Klosterman and Shane Thomas

🔗 [AiEdge Summit Website](https://aiedgesummit.com)

## Workshop Resources

### 📊 Workshop Slides

Access the presentation slides here:
[Workshop Slides](https://docs.google.com/presentation/d/1XaOjWcZegqDJE9z_PJ87czGq6hzsDQwQiK7PR292tRU/edit?usp=sharing)

### 💻 Replit.com Core Plan Activation

To get started with the workshop exercises:

1. Sign up or log in to [Replit.com](https://replit.com)
2. Navigate to your account settings
3. Go to the subscription/billing section
4. Apply the promo code: **MASTRAAIEDGE**
5. This will activate your Replit Core plan for the workshop

---

## Workshop Project: Jarvis AI Assistant

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
