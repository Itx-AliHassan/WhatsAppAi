# 🤖 WhatsApp AI — Business Representative

An AI-powered WhatsApp business representative designed to handle customer inquiries, communicate with potential clients, and represent a business through intelligent, context-aware conversations.

The assistant uses business-specific knowledge to answer questions about services, understand client requirements, and provide a professional customer experience — reducing the need for manual replies to every message.

## ✨ Features

- **AI-Powered Conversations** — Generate natural and context-aware responses using OpenAI.
- **Business Knowledge** — Understand business information, services, and communication guidelines.
- **Multilingual Support** — Communicate in English and Roman Urdu.
- **Customer Inquiries** — Answer questions and understand potential clients' requirements.
- **Conversation Management** — Maintain customer conversation history.
- **Human Takeover** — Allow the business owner to take control of conversations.
- **Automated Follow-ups** — Support follow-up messages for potential clients.
- **Business Representation** — Maintain a professional and consistent business identity.

> Note: Features are subject to implementation progress.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Node.js | JavaScript runtime |
| Express.js | Backend framework |
| MongoDB | Database |
| Mongoose | Database modeling |
| OpenAI API | AI intelligence |
| WhatsApp Cloud API | WhatsApp integration |
| Axios | HTTP requests |
| dotenv | Environment configuration |

## 🏗️ How It Works

The application follows this general workflow:

1. A customer sends a message to the WhatsApp Business number.
2. WhatsApp Cloud API forwards the message to the backend through a webhook.
3. The backend identifies the customer and retrieves relevant conversation context.
4. Business knowledge and instructions are provided to the AI.
5. OpenAI generates an appropriate response.
6. The backend sends the response through WhatsApp Cloud API.
7. Conversation information is stored in MongoDB for future reference.

## 📁 Project Structure

```text
WhatsAppAi/
│
├── src/
│   ├── config/
│   ├── controllers/
│   ├── services/
│   │   ├── ai.service.js
│   │   └── whatsapp.service.js
│   ├── models/
│   ├── routes/
│   ├── middlewares/
│   ├── prompts/
│   │   └── system.prompt.js
│   ├── utils/
│   └── app.js
│
├── .env
├── .env.example
├── .gitignore
├── package.json
└── README.md
```

*This is a proposed structure and can change as development progresses.*

## ⚙️ Getting Started

### Prerequisites

Make sure you have the following:

- Node.js
- MongoDB (local or MongoDB Atlas)
- OpenAI API key
- Meta Developer account
- WhatsApp Cloud API configuration

### 1. Clone the Repository

```bash
git clone https://github.com/Itx-AliHassan/WhatsAppAi.git
```

### 2. Navigate to the Project

```bash
cd WhatsAppAi
```

### 3. Install Dependencies

```bash
npm install
```

### 4. Configure Environment Variables

Create a `.env` file in the root directory:

```env
PORT=5000

MONGO_URI=your_mongodb_connection_string

OPENAI_API_KEY=your_openai_api_key

WHATSAPP_TOKEN=your_whatsapp_access_token
WHATSAPP_PHONE_NUMBER_ID=your_phone_number_id
WHATSAPP_VERIFY_TOKEN=your_webhook_verify_token

META_APP_SECRET=your_meta_app_secret
```

Never commit your `.env` file or expose your API keys.

### 5. Start the Development Server

```bash
npm run dev
```

Make sure your development script is configured in `package.json`.

## 🧠 AI Business Knowledge

The assistant is designed to understand the business it represents.

Its business knowledge includes:

- Business identity and introduction.
- Available development services.
- Service descriptions.
- Communication style and language preferences.
- Customer inquiry handling.
- Pricing and deadline policies.
- Escalation rules for situations requiring human assistance.

The goal is to provide relevant, accurate, and business-specific responses rather than generic chatbot replies.

## 🔐 Security

Security is an important part of this project.

- Store API keys in environment variables.
- Verify incoming WhatsApp webhook requests.
- Validate incoming messages.
- Protect customer conversation data.
- Avoid exposing internal business information.
- Handle API errors and failed message deliveries.

## 🗺️ Roadmap

- [ ] Set up Express backend.
- [ ] Connect MongoDB.
- [ ] Integrate WhatsApp Cloud API.
- [ ] Configure incoming message webhooks.
- [ ] Integrate OpenAI API.
- [ ] Create business-specific AI instructions.
- [ ] Implement conversation history.
- [ ] Implement customer management.
- [ ] Add human takeover functionality.
- [ ] Implement automated follow-ups.
- [ ] Improve error handling and logging.
- [ ] Test real-world customer conversations.

## 🎯 Project Goal

The primary goal is to build an intelligent business representative capable of independently handling routine customer interactions, understanding potential clients, and reducing the amount of manual communication required from the business owner.

This project is also an opportunity to explore AI integration, conversational systems, WhatsApp automation, backend architecture, and database-driven context management.

## 👨‍💻 Author

**Ali Hassan**

Full-Stack Web & Mobile App Developer

- GitHub: [@Itx-AliHassan](https://github.com/Itx-AliHassan)
- LinkedIn: [Ali Hassan](https://www.linkedin.com/in/itx-ali-hassan/)

## ⭐ Support

If you find this project interesting, consider giving the repository a star!

---

**Built with JavaScript, curiosity, and AI.**
