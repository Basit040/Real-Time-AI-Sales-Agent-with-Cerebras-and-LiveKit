# Real-Time-AI-Sales-Agent-with-Cerebras-and-LiveKit
A sophisticated multi-agent voice AI system that enables natural conversations with potential customers using real-time voice interaction. This sales agent can intelligently transfer between specialized roles (sales, technical support, pricing) based on customer needs

## ✨ Features
Real-time Voice Conversations: Natural speech-to-text and text-to-speech interactions

Multi-Agent Architecture: Intelligent transfer between specialized agents

Context-Aware Responses: Uses company product data to provide accurate information

No Hallucinations: Strictly uses provided context - never makes up information

Enterprise Ready: Built on LiveKit for production-grade real-time communication

Fast Inference: Powered by Cerebras for the fastest LLM inference available

## 🏗️ Architecture
text
User Input → LiveKit → STT (Cartesia) → Cerebras LLM → TTS (Cartesia) → User Output
                     ↓
           Multi-Agent Orchestration
                     ↓
    Sales Agent ↔ Technical Agent ↔ Pricing Agent

## 🎯 Agent Specialties
### 🏷️ Sales Agent
General product information

Feature overviews

Initial customer engagement

Transfer triggers: "technical details", "pricing questions"

## 💻 Technical Specialist
Detailed specifications

Implementation guidance

Technical requirements

Transfer triggers: "pricing", "general questions"

## 💰 Pricing Specialist
Cost discussions

Budget planning

Value proposition

Transfer triggers: "technical specs", "sales questions"

## 🧪 Try It Out!
With this multi-agent setup, you can test the following conversation flows:

## 🎯 Conversation Flow 1: Basic Sales to Technical Transfer
text
User: "Tell me about your products"
Sales Agent: "Hello! I'm your sales representative. I can help you learn about our products..."

User: "I need technical details about the enterprise plan"
Sales Agent: "I'll transfer you to our technical specialist..."
Technical Agent: "Hello, I'm the technical specialist. The enterprise plan includes..."
## 🎯 Conversation Flow 2: Technical to Pricing Transfer
text
User: "Can you tell me about the technical specifications?"
Technical Agent: "The system supports 99.9% uptime with enterprise-grade security..."

User: "What does this cost?"
Technical Agent: "I'll connect you with our pricing specialist..."
Pricing Agent: "Hi there, I'm the pricing specialist. The enterprise plan starts at..."
## 🎯 Conversation Flow 3: Full Circle
text
Sales → Technical → Pricing → Sales
User: "Tell me about your products" (Sales)
User: "I need technical specs" (Technical)  
User: "Now let's talk pricing" (Pricing)
User: "Actually, I have more general questions" (Back to Sales)
🎤 What to Say to Test Transfers:
To Technical Specialist:

"I need technical details"

"Can you transfer me to technical support?"

"I have some technical questions"

"Let me speak to a technical expert"

To Pricing Specialist:

"Let's discuss pricing"

"I want to talk about costs"

"Can I speak to someone about budgets?"

"What are the payment options?"

Between Specialists:

"Actually, I'd like to discuss pricing instead"

"I need more technical specifications"

"Can I go back to sales?"

"Let me talk to the sales agent again"

## 🔍 What to Observe:
Different Voices: Each agent has a distinct voice (different Cartesia voice IDs)

Console Logging: Watch for agent change messages:

Current Agent: 🏷️ Sales Agent 🏷️

Current Agent: 💻 Technical Specialist 💻

Current Agent: 💰 Pricing Agent 💰

Specialized Responses: Each agent focuses on their area of expertise

Smooth Transfers: Natural conversation flow between specialists

## 💡 Pro Tips for Testing:
Speak naturally - the system understands conversational language

Try unexpected transfers to test robustness

Ask about specific products from your context file

Test edge cases like "I don't know what I need"

Notice how agents stay within their provided context
