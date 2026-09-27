Persona-Based News Filtering and Presentation using Agentic AI

Problem Statement

Most news platforms show the same articles to every reader, regardless of their interests, profession, or reading preference. This forces users to manually search through large volumes of unrelated news to find content relevant to them, which is time consuming and often leads to important updates being missed. There is a need for a system that can automatically understand a user's interests and deliver only relevant news, presented in a simple and easy to read format.

Proposed Solution

PersonaPulse is an Agentic AI pipeline that filters and reshapes news based on predefined user personas (for example, Tech Professional, Student, Finance Enthusiast, Sports Fan, and others). Instead of a single generic feed, each persona gets a personalized weekly digest of relevant news, rewritten in simple English bullet points, along with a short AI generated insight summarizing the key trends from that week's news for that persona.

Multiple specialized AI agents work together in sequence, each handling one step of the process, rather than a single model trying to do everything at once. This makes the system more reliable, transparent, and easy to improve.

Project Workflow

The system runs automatically once a week for each predefined persona.

Input — A fixed persona profile (interests, tone, exclusions) is selected from a predefined list of personas.
News Fetch Agent — Uses a news fetching tool (via MCP) to pull the last 7 days of articles matching the persona's topics.
Filtering and Ranking Agent — Removes irrelevant or duplicate articles and ranks the remaining ones by relevance, selecting the top 10.
Content Reshaping Agent — Rewrites each selected article into short, simple English bullet points.
Insight Generation Agent — Reads all 10 articles together and generates one short paragraph summarizing the week's key trends for that persona.
Presentation Agent — Packages the insight and bullet point articles into a final structured output, ready to be displayed to the user.
Output — A weekly, persona specific news digest (insight summary plus 10 simplified articles) is shown to the user through a simple web interface, where they can also give feedback (like or skip) to fine tune future results.
Tech Stack
Component	Technology
Core Language	Python
Agent Orchestration	LangGraph
LLMs	Groq (Llama 3.3) and Google Gemini (free tier)
Agent-Tool Connection	Model Context Protocol (MCP)
News Data Source	NewsAPI
Backend	FastAPI
Frontend	Plain HTML/JS
Data Format	JSON
Expected Result

The completed project will automatically generate a personalized, easy to read weekly news digest for each of 10 predefined user personas. Each digest will contain a short AI written insight paragraph highlighting the week's key trends, followed by 10 news articles simplified into bullet points relevant to that persona's interests. Users will be able to select their persona through a simple interface and view their weekly feed instantly, with the option to give feedback that improves future personalization.

The result is a working demonstration of a practical, multi-agent AI system that reduces information overload and delivers relevant news efficiently.# persona pulse
