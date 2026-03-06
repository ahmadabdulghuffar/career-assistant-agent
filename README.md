🤖 AI Career Assistant Chatbot
An intelligent conversational agent that represents my professional background, answers career questions, and captures leads using OpenAI function calling and Gradio.

Built by Ahmad Abdul Ghaffar | AI Agent Engineer | aibyahmad.com

🔗 Live Demo: HuggingFace Space = https://huggingface.co/spaces/ahmadsai/career_conversation

🎯 What This Does
This AI chatbot acts as my digital representative, providing:

✅ Automated Career Q&A - Answers questions about my background, skills, and experience
✅ Lead Capture - Records interested visitors' contact information
✅ Unknown Question Tracking - Logs questions it can't answer for future improvement
✅ Professional Engagement - Maintains consistent, engaging conversation tone
✅ Real-time Notifications - Sends alerts via Pushover when contacts are captured

Use Case:
Visitors come to my website → Chat with AI version of me → AI answers their questions → Captures their email if interested → I follow up personally

🏗️ How It Works
System Architecture
User Message
    ↓
AI reads context (LinkedIn PDF + Summary)
    ↓
AI decides action:
    ├─ Answer question directly
    ├─ Use record_user_details tool (if email provided)
    └─ Use record_unknown_question tool (if can't answer)
    ↓
Response sent to user
    ↓
Notification sent to me (Pushover)
Key Components
1. Context Loading

Extracts text from LinkedIn PDF
Loads professional summary from text file
Creates comprehensive system prompt
2. Function Calling (Tools)

record_user_details() - Captures name, email, notes
record_unknown_question() - Logs unanswered queries
3. Conversation Loop

Handles multi-turn conversations
Maintains chat history
Executes tool calls when needed
4. Notifications

Pushover integration for real-time alerts
Notifies me when someone shows interest
⚡ Key Features
1. Intelligent Context Awareness
Trained on my actual LinkedIn profile
Understands my career journey (Marketing → AI Engineering)
References specific achievements (11× sales growth, etc.)
2. Function Calling / Tool Use
AI decides WHEN to use tools (not hardcoded)
Captures leads naturally in conversation
Tracks knowledge gaps automatically
3. Professional Conversation Design
Stays in character as Ahmad Abdul Ghaffar
Professional yet approachable tone
Steers conversations toward contact capture
4. Real-time Lead Notifications
Instant Pushover alerts when email captured
Includes visitor's name, email, and context
Enables quick follow-up
5. Deployed & Production-Ready
Running live on HuggingFace Spaces
Handles concurrent users
Gradio UI for easy interaction
🛠️ Tech Stack
Core Technologies:

Python - Primary language
OpenAI GPT-4o-mini - Conversational AI model
Gradio - Web UI framework
PyPDF - PDF text extraction
Pushover API - Real-time notifications
Key Patterns:

Function calling / tool use
System prompt engineering
Multi-turn conversation handling
PDF data extraction
Environment variable management
📋 Code Structure
Main Components
Class: Me

python
class Me:
    def __init__(self):
        # Load LinkedIn PDF
        # Load summary text
        # Initialize OpenAI client
    
    def system_prompt(self):
        # Build context-aware system prompt
    
    def handle_tool_call(self, tool_calls):
        # Execute function calls from AI
    
    def chat(self, message, history):
        # Main conversation loop
Tools Definition

python
record_user_details_json = {
    "name": "record_user_details",
    "description": "Use this tool to record...",
    "parameters": {...}
}
Gradio Interface

python
gr.ChatInterface(me.chat, type="messages").launch()
🚀 Setup & Installation
Prerequisites
Python 3.8+
OpenAI API key
Pushover account (for notifications)
LinkedIn profile PDF
Professional summary text file
Installation
bash
# Clone the repository
git clone https://github.com/yourusername/ai-career-chatbot.git
cd ai-career-chatbot

# Install dependencies
pip install -r requirements.txt

# Create directory structure
mkdir me
# Add your linkedin.pdf to me/ folder
# Add your summary.txt to me/ folder

# Create .env file
cp .env.example .env
Environment Variables
Create a .env file:

properties
OPENAI_API_KEY=sk-your-key-here
PUSHOVER_TOKEN=your-pushover-app-token
PUSHOVER_USER=your-pushover-user-key
Required Files
me/linkedin.pdf

Your LinkedIn profile exported as PDF
Or any document with your career info
me/summary.txt

Brief professional summary
Key achievements
Skills and expertise
Run the Application
bash
python app.py
Then open the Gradio interface in your browser (usually http://localhost:7860).

💡 Use Cases
Personal Branding
24/7 availability on your website
Consistent messaging about your background
Captures leads while you sleep
Freelance/Consulting
Pre-qualifies potential clients
Answers common questions automatically
Collects contact info for follow-up
Job Search
Showcases technical skills to recruiters
Demonstrates AI engineering capabilities
Provides interactive portfolio piece
Networking
Scales your availability at events
Provides consistent elevator pitch
Captures connections automatically
🎓 What I Learned Building This
Technical Skills
✅ OpenAI function calling / tool use
✅ Gradio interface development
✅ PDF text extraction with PyPDF
✅ System prompt engineering
✅ Multi-turn conversation handling
✅ API integration (Pushover)
✅ Environment variable management
✅ HuggingFace Spaces deployment

AI Engineering Concepts
✅ Tool schema definition (JSON)
✅ Dynamic function execution
✅ Context management for LLMs
✅ Conversation state handling
✅ Production deployment strategies

Business Applications
✅ Lead generation automation
✅ Personal brand scaling
✅ 24/7 availability without human cost
✅ Data collection for improvement

🔮 Future Enhancements
Planned Features:

 Multi-language support
 Voice input/output
 Calendar integration for scheduling
 CRM integration (automatic contact sync)
 Analytics dashboard (conversation insights)
 Custom training on additional documents
 Response quality evaluation
 A/B testing different system prompts
📊 Example Conversation
User: "What's your experience with AI?"

AI: "I'm Ahmad Abdul Ghaffar, and I'm currently transitioning 
from Marketing Growth Expert to AI Agent Engineer. I recently 
completed projects including a multi-agent research system and 
this career assistant chatbot you're talking to!

My AI engineering skills include Python, OpenAI API, LangChain, 
multi-agent orchestration, and building production systems.

My background in marketing (11× sales growth in EV industry) 
gives me unique insight into building AI solutions that solve 
real business problems.

Are you interested in AI automation for your business? I'd love 
to discuss how I can help. What's your email?"

User: "Sure, it's john@example.com"

AI: [Uses record_user_details tool]
"Great! I've noted your interest. I'll reach out shortly to 
discuss how AI automation can help your business!"

[Pushover notification sent to Ahmad]
🤝 About the Developer
Ahmad Abdul Ghaffar
AI Agent Engineer | Marketing Growth Expert

Journey:

Started: Marketing & Growth (11× sales growth, 10% efficiency gains)
Transition: Learning Agentic AI Engineering
Current: Building intelligent automation systems
Location: Faisalabad, Pakistan → Serving global clients
Technical Focus:

Multi-agent systems
Business process automation
Marketing automation with AI
Custom chatbot development
Connect:


💼 LinkedIn: Ahmad Abdul Ghaffar
📧 Email: ahmadabdulghuffar@gmail.com
🤗 HuggingFace: ahmadsai ( https://huggingface.co/spaces/ahmadsai/career_conversation )
💼 Custom Development
Want a similar AI assistant for your business?

I build custom conversational AI solutions:

Career/business chatbots
Customer support agents
Lead qualification systems
Internal knowledge assistants
Multi-language support bots
Services:

Consultation & Requirements Analysis
Custom Agent Development
Training Data Preparation
Deployment & Integration
Ongoing Maintenance
Rate: $30/hour or project-based pricing

📧 Contact: ahmad@aibyahmad.com

📄 License
MIT License - See LICENSE file for details

🙏 Acknowledgments
Built as part of my journey learning Agentic AI Engineering.

Inspired by "The Complete Agentic AI Engineering Course (2025)" by Ed Donner.

Special thanks to the OpenAI and Gradio communities.

🔒 Privacy & Data
Important Notes:

This chatbot does NOT store conversation history permanently
Contact information is sent via Pushover only
No third-party analytics or tracking
Your LinkedIn PDF and summary remain private (not included in repo)
To use this for yourself:

Replace me/linkedin.pdf with your own
Replace me/summary.txt with your background
Update system prompt with your name
Deploy with your own API keys
⭐ If you build your own version, tag me! I'd love to see it!

🚀 Ready to automate your professional presence? Clone this repo and customize it!

