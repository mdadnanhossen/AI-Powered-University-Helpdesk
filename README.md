# AI-Powered University Helpdesk

> **Status: Proposal stage.** This repository currently contains project planning only. No application code has been developed yet, and every feature listed below is **planned**, not implemented.

**Course:** CSE4104 – Software Development III
**University:** Northern University of Business and Technology, Khulna
**Department:** Computer Science and Engineering
**Team:** CSE4104-7F-T09 (Section 7F)
**Course Teacher:** Md. Riaz Mahmud, Assistant Professor

---

## Project Description

AI-Powered University Helpdesk is a planned full-stack web application that gives students quick answers to university-related questions. Students will log in and ask questions about admission procedures, course registration, tuition and fee payments, examination schedules, academic rules, campus facilities, and university departments and services.

The system will use the Google Gemini API to understand natural-language questions and generate answers based on university information maintained by the admin. Conversations will be stored in MongoDB so students can review their chat history. An admin panel will let university staff monitor conversations, view unresolved queries, manage student accounts, and manage university information. The application will be responsive on desktop and mobile devices.

## Problem Summary

University information is often spread across websites, notice boards, social media groups, and department offices. Static FAQ pages cannot handle differently worded or follow-up questions, and manual support depends on office hours and staff availability. This project aims to provide one centralized helpdesk where students can ask questions in their own words, and where the university can see which questions remain unanswered.

## Proposed Features

### Student
- Registration and login
- AI chatbot for university-related questions
- Chat history
- Helpful / not helpful feedback on answers
- Responsive interface

### AI
- Natural-language question understanding
- Gemini-powered answer generation
- Conversation context for follow-up questions
- Retrieval of relevant entries from admin-managed university information
- Safe handling of unknown or unsupported questions (marked as unresolved)

### Admin
- Admin login with role-based access
- Manage student accounts
- Monitor conversations
- View and resolve unresolved queries
- Manage university information

### Planned Extensions (optional, not in core scope)
- Document/PDF-based question answering (RAG)
- Semantic search using embeddings
- Bengali and English bilingual support
- Dashboard of frequently asked topics

## Technology Stack

| Layer | Technology |
|---|---|
| Frontend | React.js, Next.js, Tailwind CSS |
| Backend | Node.js, Express.js |
| Database | MongoDB Atlas |
| AI Integration | Google Gemini API |
| Version Control | Git, GitHub |
| Deployment | Vercel |
| UI Design | Figma |

The frontend will be one Next.js project (Next.js is a framework built on React) that calls a separate Express.js REST API. The Gemini API key will be kept only on the server.

## Planned System Flow

1. The student sends a question from the Next.js chat page to the Express API.
2. The backend verifies the login token and finds relevant university information in MongoDB.
3. The backend sends the question, recent messages, and relevant information to the Gemini API.
4. The answer is saved in MongoDB and returned to the student. If no reliable answer exists, the question is marked as unresolved for the admin.

## Planned Project Structure

```text
AI-Powered-University-Helpdesk/
|-- README.md
|-- .gitignore
|-- client/                  (planned: Next.js + Tailwind CSS frontend)
|-- server/                  (planned: Node.js + Express.js backend)
`-- docs/
    |-- proposal/            Week 02 proposal and team information
    |-- design/              Figma links, architecture and schema diagrams
    `-- reports/             test report, user guide, final report
```

Detailed `client/` and `server/` subfolders are described in the project proposal and will be added as development starts.

## Development Status

- [x] Team formation and idea selection (Week 01)
- [x] Project proposal prepared (Week 02)
- [ ] Requirement analysis and research
- [ ] UI/UX and system architecture design
- [ ] Frontend development
- [ ] Backend and database development
- [ ] Gemini AI integration
- [ ] Admin dashboard and chat history
- [ ] Integration and testing
- [ ] Deployment and documentation

## Getting Started

Setup instructions are not available yet because the application code has not been added. They will be written here once the `client/` and `server/` projects are uploaded.

## Team

| No. | Name | Student ID | Role |
|---|---|---|---|
| 01 | Md. Adnan Hossen (Team Leader) | 11230121135 | Team Leader / Backend Developer / Authentication |
| 02 | Sheikh Mirazur Rahman Nayon | 11230121131 | Frontend / AI Integration |
| 03 | Jaber | 11230121105 | Database / Testing |
| 04 | Sazid Hasan | 11230121122 | Documentation / Deployment |

## Team Workflow

- Work on feature branches (for example `feature/chat-ui`) and open a pull request into `main`.
- Another team member reviews the pull request before merging.
- Never commit `.env` files or API keys. Share only `.env.example` files.
- Track tasks with GitHub Issues.

## License

No license has been selected yet.

