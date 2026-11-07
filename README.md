# HelpDesk Lite: Student Support Tickets

CSE362c / CSE5531 | Fall 2026

## Team
- Ammar Essam Mohamed Ali El Banna, 233789, ammar.essam@msa.edu.eg (contact)
- Muhammed Tareq Mashhour, 230183, Muhammed.tareq@msa.edu.eg

## Summary
HelpDesk Lite is a small ServiceHub web app for student support. Students search an FAQ, submit support tickets and track their status. Support agents manage a queue, reply, and move tickets from Open to Closed.

## Scope
**Included:** login with two roles (student, agent); FAQ and ticket browsing with search and filters; ticket submission form; agent queue with assignment, replies and status changes; persistent database (CRUD); server-side validation; tests and security checks.

**Excluded:** email/SMS notifications, file attachments, live chat, analytics dashboards, cloud hosting, AI features.

## Three user journeys
- **J1 Browse:** a user searches and filters FAQs and tickets by keyword, category and status (`GET /api/faqs`, `GET /api/tickets`).
- **J2 Submit:** a student submits a ticket (title, category, priority, description). The server validates it and saves it (`POST /api/tickets`, returns 201).
- **J3 Update:** an agent assigns, replies to and changes the status of a ticket (`PATCH /api/tickets/:id`). Students get 403.

## Business rules
- A ticket cannot skip a status step (Open → In Progress → Resolved → Closed).
- A ticket cannot be closed without at least one agent reply.
- A student may have at most 5 open tickets.

## Tech stack
HTML, CSS, vanilla JavaScript (front end); Node.js + Express (API); SQLite (data).

## Prerequisites
- Node.js (version to be confirmed)

## Setup and run
_To be completed and tested before the final version._
```
npm install
npm start
```

## Project structure
```
public/   front end (HTML, CSS, JS modules)
server/   Express routes, validation, database code
db/       schema.sql and seed.sql
tests/    positive, negative and business-rule tests
evidence/ ui, http, validation, quality, security
docs/     report, slides, demo script
```
