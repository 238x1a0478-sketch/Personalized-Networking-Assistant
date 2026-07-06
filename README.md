# 🤝 Personalized Networking Assistant

## 📖 Overview

The **Personalized Networking Assistant** is an AI-powered web application designed to help professionals build meaningful connections at networking events, conferences, seminars, career fairs, and professional meetups. By leveraging **Natural Language Processing (NLP)** and **Generative AI**, the application generates personalized conversation starters based on an event's context and the user's professional interests, enabling users to confidently initiate engaging and relevant discussions.

The system first analyzes an event description using **DistilBERT Zero-Shot Classification** to identify the most relevant discussion themes. These extracted themes are then combined with the user's interests and processed through **GPT-2** to generate natural, context-aware conversation starters tailored to the networking scenario. This intelligent workflow eliminates the need for users to prepare conversation topics manually while ensuring that every suggestion remains relevant to the event.

To further enhance reliability, the application integrates a **Fact-Checking Service** powered by the Wikipedia REST API, allowing users to instantly verify topics before engaging in conversations. Every generated conversation is automatically stored in a conversation history, while a feedback system enables users to like or dislike generated suggestions, supporting future improvements to recommendation quality.

The application follows a modular **client-server architecture** consisting of a **FastAPI backend** and a **Streamlit frontend**. The backend manages AI inference, REST API endpoints, validation, history management, feedback logging, and business logic, whereas the frontend delivers an intuitive interface for interacting with all application features. FastAPI's automatic Swagger documentation further simplifies API testing and integration.

Designed with scalability and maintainability in mind, the project adopts a clean service-oriented architecture where each module is responsible for a single functionality, making the system easy to extend with additional AI models, authentication mechanisms, cloud deployment, databases, or recommendation engines in the future.

---

## 🚀 Workflow

```text
                User Input
     (Event Description + Interests)
                     │
                     ▼
      Event Theme Extraction (DistilBERT)
                     │
                     ▼
     AI Conversation Generation (GPT-2)
                     │
                     ▼
     Personalized Conversation Starters
          │                     │
          ▼                     ▼
 Fact Checking          History Logging
 (Wikipedia API)       Feedback Collection
          │                     │
          └──────────┬──────────┘
                     ▼
          Interactive Streamlit UI
```

---

## ✨ Key Features

- 🤖 AI-powered personalized conversation generation
- 🧠 Event theme extraction using DistilBERT Zero-Shot Classification
- 💬 Context-aware networking conversation starters using GPT-2
- 🔍 Integrated fact-checking using the Wikipedia REST API
- 📜 Automatic conversation history management
- 👍 User feedback collection for generated suggestions
- ⚡ FastAPI-powered REST API backend
- 🎨 Interactive Streamlit frontend
- 📖 Auto-generated Swagger API documentation
- ✅ Modular service-layer architecture
- 💾 Persistent JSON-based storage for conversations and feedback
- 🧪 Unit and integration testing support

---

## 🏗️ System Architecture

```text
                    Streamlit Frontend
                           │
                    REST API Requests
                           │
                    FastAPI Backend
                           │
      ┌────────────────────┼────────────────────┐
      │                    │                    │
      ▼                    ▼                    ▼
 Event Analyzer     Topic Generator      Fact Checker
   (DistilBERT)          (GPT-2)        (Wikipedia API)
      │                    │                    │
      └────────────────────┼────────────────────┘
                           ▼
          History Logger & Feedback Logger
                           │
                     JSON Data Storage
```

---

## 🛠️ Technology Stack

| Category | Technologies |
|----------|--------------|
| Programming Language | Python |
| Backend | FastAPI |
| Frontend | Streamlit |
| NLP Model | DistilBERT (Zero-Shot Classification) |
| Text Generation | GPT-2 |
| Fact Verification | Wikipedia REST API |
| Validation | Pydantic |
| API Documentation | Swagger UI |
| Data Storage | JSON |
| Testing | Pytest |

---

## 🎯 Objectives

- Help users initiate professional conversations confidently.
- Generate personalized networking topics using AI.
- Analyze event context automatically through NLP.
- Provide reliable fact verification before conversations.
- Store conversation history for future reference.
- Collect user feedback to improve recommendation quality.
- Demonstrate the practical integration of multiple AI technologies within a modern web application.

---

## 🌟 Project Highlights

- Combines **Natural Language Processing**, **Machine Learning**, and **Generative AI** into a complete end-to-end application.
- Uses **DistilBERT** to intelligently understand networking event contexts.
- Employs **GPT-2** to generate personalized and engaging conversation starters.
- Supports instant fact verification through Wikipedia integration.
- Implements a clean modular architecture following service-layer design principles.
- Provides both a user-friendly interface and production-style REST APIs.
- Built with scalability, maintainability, and extensibility as core design goals.
- Demonstrates practical integration of **FastAPI**, **Streamlit**, **Transformers**, **DistilBERT**, **GPT-2**, and external APIs within a real-world AI application.
