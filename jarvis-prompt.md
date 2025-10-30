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
