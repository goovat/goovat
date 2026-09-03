OVIE — BACKEND ENGINEER PORTFOLIO

I'm OVIE — a backend-focused developer building scalable, reliable systems with Python, Django, FastAPI, PostgreSQL, Redis, Celery, REST APIs, asynchronous processing, financial infrastructure, real-time systems, and automated testing.

My portfolio focuses on production-oriented backend engineering rather than simple CRUD applications. I build systems around payments, money movement, accounting, asynchronous processing, API reliability, database integrity, idempotency, concurrency, observability, real-time communication, and CI/CD.

My current engineering portfolio includes four core backend systems:

- Payment Flow — payment processing and webhook infrastructure
- Transfer Engine — reliable wallet and money-transfer infrastructure
- LedgerCore — double-entry financial ledger and accounting engine
- AsyncAPI Engine — asynchronous API and background job-processing platform

I am also building MyCrony, a full-stack social networking and creator-economy platform combining social media, creator tools, content management, live video streaming, local voice and video calls, real-time communication, monetization, analytics, and payment infrastructure.

---

Portfolio

1. Payment Flow

Payment Flow is a production-oriented payment processing platform designed around reliable payment workflows and external payment-provider integrations.

The system demonstrates:

- Payment intent creation
- Payment confirmation
- Payment transaction tracking
- Stripe integration
- Webhook processing
- Webhook signature verification
- Idempotent payment operations
- Celery background processing
- Redis
- PostgreSQL
- Integration testing
- Automated CI/CD

The architecture emphasizes reliable interaction with external payment systems while maintaining consistent internal transaction state.

Engineering Focus

- Payment lifecycle management
- Idempotency
- Webhook reliability
- Asynchronous processing
- Celery workers
- Redis-backed background processing
- Transaction state management
- Integration testing
- CI/CD
- Production-oriented configuration

---

2. Transfer Engine

Transfer Engine is a financial transfer service focused on reliable movement of value between wallets.

The system demonstrates backend engineering principles required for financial transactions, including transactional balance management and database integrity.

Core Components

- Users
- Wallets
- Wallet balances
- Transfer workflows
- Balance services
- Transactional operations
- Validation
- Exception handling
- PostgreSQL
- Django
- Automated tests

Engineering Focus

- Atomic financial operations
- Balance integrity
- Transaction safety
- Database transactions
- Concurrency-aware design
- Service-layer architecture
- Automated testing

The project is designed to demonstrate that a financial backend must protect the correctness of balances rather than simply expose transfer endpoints.

---

3. LedgerCore

LedgerCore is a production-oriented double-entry accounting ledger engine.

It is designed to demonstrate financial-domain backend architecture beyond basic payment and transfer processing.

Core Components

- Accounts
- Ledgers
- Journal entries
- Journal lines
- Debit and credit operations
- Double-entry validation
- Account balances
- Transaction references
- Reconciliation
- Immutable financial records
- Audit events
- Database constraints
- Atomic operations

Financial Integrity

LedgerCore is built around fundamental accounting invariants.

Every journal entry must maintain balanced debits and credits.

Financial records are designed to be immutable rather than casually overwritten.

Database constraints and transactional operations are used to protect financial correctness at the persistence layer.

Engineering Focus

- Double-entry accounting
- Financial invariants
- PostgreSQL
- Django
- Database constraints
- Atomic transactions
- Auditability
- Reconciliation
- Automated testing
- CI/CD
- Production reliability

---

4. AsyncAPI Engine

AsyncAPI Engine is a FastAPI-based asynchronous job-processing platform designed around reliable background work and scalable API architecture.

Architecture

Client
  │
  ▼
FastAPI API
  │
  ▼
Job Service
  │
  ├── PostgreSQL
  │
  ├── Redis
  │
  └── Worker Processing
          │
          ▼
      Background Jobs

Core Capabilities

- FastAPI API layer
- Asynchronous job processing
- Job service architecture
- SQLAlchemy
- Alembic migrations
- PostgreSQL
- Redis
- Worker processing
- Authentication
- Idempotency
- Retry handling
- Failure management
- Observability
- Docker
- pytest
- CI/CD

Engineering Focus

- Async Python
- API architecture
- Background processing
- Reliable job execution
- Retry strategies
- Idempotency
- Redis-based infrastructure
- Database persistence
- Observability
- Containerization
- Automated testing

---

MyCrony

MyCrony is a full-stack social networking, creator-economy, media-sharing, real-time communication, live-streaming, and monetization platform built with Django.

The project combines social media functionality, creator tools, content management, personalized feeds, analytics, live video streaming, local voice and video calls, real-time messaging, monetization, and payment infrastructure into one ecosystem.

The platform supports:

- Content creators
- Communities
- Media publishing
- Social interactions
- Monetization workflows
- Creator earnings
- Subscriptions
- Real-time engagement
- Live video streaming
- Local voice calls
- Local video calls
- Analytics
- Payment infrastructure

---

MyCrony Overview

MyCrony is designed as a creator-first social ecosystem providing:

- User profiles
- Social connections
- Posts and media publishing
- Reels and stories
- Live video streaming
- Live rooms
- Local voice calls
- Local video calls
- Real-time messaging
- Recommendation systems
- Creator monetization
- Earnings dashboards
- Subscription systems
- Financial reporting
- Payment processing
- Creator studio management

The project follows a modular Django architecture.

---

MyCrony Features

User System

Authentication and account functionality includes:

- User registration
- Login and logout
- Email verification
- Password reset
- Account recovery
- User profiles
- Avatar uploads
- Cover images
- Privacy settings
- Security settings
- Notification settings
- Profile editing
- Visitor tracking
- Friend system
- Followers and following
- Friend requests
- Close friends
- User discovery
- Creator onboarding

---

Content Platform

Users can publish and manage multiple forms of content.

Posts

- Text posts
- Image posts
- Video posts
- Audio content
- Post previews
- Draft workflows
- Scheduled publishing
- Content editing
- Content deletion
- Post analytics

Stories

- Story publishing
- Story viewing
- Story highlights
- Temporary content

Reels

- Reel creation
- Reel playback
- Reel feeds
- Reel interactions
- Duet functionality

Galleries

- Gallery creation
- Image collections
- Thumbnail generation
- Media previews

Collections

Users can organize content into collections.

---

Feed System

MyCrony includes recommendation and ranking infrastructure.

Implemented feed concepts include:

- Following feed
- Discover feed
- Trending feed
- Personalized feed
- Live feed
- For-you feed

Ranking strategies include:

- Chronological ranking
- Engagement ranking
- Popularity ranking
- Recency ranking
- Personalized ranking
- Hybrid ranking

Feed interactions include:

- Likes
- Saves
- Shares
- Comments
- Reports
- Follow actions
- Blocks
- Mutes

---

Creator Studio

Creator tools are provided through the studio module.

Features include:

- Creator dashboard
- Studio management
- Draft management
- Publishing workflows
- Scheduling
- Analytics dashboard
- Audience monitoring
- Content performance tracking

Module:

studio/

---

Creator Economy

MyCrony contains creator monetization infrastructure.

Earnings

- Earnings dashboard
- Revenue tracking
- Creator shares
- Payment history
- Financial summaries

Payouts

- Withdrawal requests
- Payout schedules
- Payout methods
- Creator payments

Revenue Systems

- Revenue configuration
- Creator percentage allocation
- Promotion shares
- Transparency reports

Subscriptions

- Recurring plans
- Membership flows
- Subscription tracking

Financial Infrastructure

The economics module contains financial functionality such as:

- Invoice models
- Tax models
- Revenue models
- Reports
- Exchange models
- Payment models
- Webhooks
- Financial analytics

Module:

economics/

---

Payment Infrastructure

MyCrony includes payment infrastructure supporting creator monetization and platform payment workflows.

Payment capabilities include:

- Payment processing
- Subscription billing
- Webhook integration
- Revenue tracking
- Creator payments
- Transaction workflows
- Payment state management
- Asynchronous payment workflows

The payment architecture includes dedicated payment-flow services and webhook handling.

---

Real-Time Features

MyCrony uses Django Channels, WebSockets, Redis, and asynchronous processing for real-time functionality.

The real-time layer covers messaging, local calls, and live video experiences.

Messaging

- Conversations
- Inbox
- Sent messages
- Drafts
- Forwarding
- Search
- Threads
- Real-time message delivery

Chat

- Message bubbles
- Reactions
- Typing indicators
- Real-time interactions

---

Local Voice & Video Calls

MyCrony supports direct local communication between users on the platform.

Users can communicate through in-platform voice and video calls.

Call Features

- One-to-one voice calls
- One-to-one video calls
- Incoming calls
- Outgoing calls
- Call acceptance
- Call rejection
- Call termination
- Call history
- Real-time call signaling
- In-platform user-to-user communication

The goal is to provide direct communication within the MyCrony ecosystem without requiring users to leave the platform for ordinary voice or video conversations.

---

Live Video Streaming

MyCrony supports live video broadcasting, allowing creators to stream live video to audiences within the platform.

Live Streaming Features

- Live stream creation
- Live video broadcasting
- Live rooms
- Stream viewing
- Live audience participation
- Real-time interactions
- Stream thumbnails
- Stream metadata
- Live-session management
- Creator live sessions
- Live feed integration

The live-streaming functionality is separated from ordinary content publishing so live sessions can be treated as real-time platform events.

Module:

live/

---

MyCrony Real-Time Architecture

Conceptually, the real-time layer is structured around:

                         MyCrony
                            │
             ┌──────────────┼──────────────┐
             │              │              │
             ▼              ▼              ▼
        Messaging        Calls       Live Streaming
             │              │              │
             └──────────────┼──────────────┘
                            │
                            ▼
                    Django Channels
                            │
                            ▼
                       WebSockets
                            │
                            ▼
                          Redis
                            │
                            ▼
                  Asynchronous Processing
                            │
                            ▼
                         Celery

This allows MyCrony to combine conventional Django application functionality with real-time communication and asynchronous background processing.

---

MyCrony Background Processing

MyCrony uses Celery and Redis for asynchronous and background workloads.

Background processing can support areas such as:

- Scheduled content publishing
- Media processing
- Thumbnail generation
- Notification processing
- Analytics processing
- Email workflows
- Payment-related asynchronous tasks
- Creator-economy workflows
- Periodic maintenance tasks

Celery workers execute background jobs while Redis provides the supporting message-broker infrastructure.

Celery Beat can be used for scheduled and periodic workloads.

Conceptually:

                    MyCrony
                       │
          ┌────────────┼────────────┐
          │            │            │
          ▼            ▼            ▼
       Django       Channels      APIs
          │            │            │
          └────────────┼────────────┘
                       │
                       ▼
                     Redis
                       │
                       ▼
                    Celery
                       │
              ┌────────┴────────┐
              │                 │
              ▼                 ▼
          Workers          Celery Beat
              │                 │
              ▼                 ▼
       Background Jobs    Scheduled Tasks

---

Analytics

Analytics infrastructure covers multiple areas.

Creator Analytics

- Audience metrics
- Revenue analytics
- Content performance
- Earnings reports

Content Analytics

- Engagement reports
- Feed metrics
- Post performance

Financial Analytics

- Revenue reports
- Payment reports
- Transparency metrics

Administrative Analytics

- User activity
- System monitoring
- Platform statistics

---

Moderation & Administration

Moderation infrastructure includes:

- Flagged-content review
- Reporting workflows
- Copyright handling
- Administrative dashboards
- User monitoring
- Access controls
- Permissions

Administrative templates:

templates/moderation/

---

Media Support

MyCrony supports multiple media types.

Images

- JPG
- PNG

Video

- MP4
- Video posts
- Reels
- Live video

Audio

- Voice messages
- Audio uploads
- Voice-call support

Media storage includes:

- Avatars
- Covers
- Content media
- Galleries
- Voice messages
- Draft thumbnails
- Live thumbnails

---

MyCrony Applications

users/          User management
content/        Posts and publishing
feeds/          Feed engine
economics/      Payments and monetization
studio/         Creator tools
live/           Live streaming
core/           Shared utilities
mycrony/        Project configuration

---

MyCrony Project Structure

MyCrony/

users/
content/
feeds/
economics/
studio/
live/
core/
templates/
media/
static/
mycrony/

manage.py
requirements.txt

---

Technology Stack

Backend

- Python
- Django
- Django REST Framework
- Django Channels
- FastAPI
- SQLAlchemy
- Celery

Databases

- PostgreSQL
- SQLite for selected development environments

Infrastructure & Background Processing

- Redis
- Celery
- Celery Beat
- Asynchronous workers
- Background job processing
- Docker

APIs & Real-Time Communication

- REST APIs
- WebSockets
- ASGI
- Django Channels

Payments

- Stripe
- Payment webhook infrastructure
- Payment processing workflows

Testing

- pytest
- Django testing
- Integration testing
- Automated CI validation

DevOps

- Git
- GitHub
- GitHub Actions
- CI/CD
- Automated quality gates

Production Infrastructure

- Nginx
- Gunicorn
- Daphne
- PostgreSQL
- Redis
- Celery workers
- Celery Beat
- ASGI/WebSocket infrastructure

---

Backend Engineering Themes

Across these projects, my work focuses on several recurring engineering problems.

Reliability

Designing systems that remain correct when operations fail, retry, or execute concurrently.

Financial Integrity

Protecting balances, transactions, journal entries, and accounting invariants.

Idempotency

Preventing duplicate processing when clients or external systems retry requests.

Asynchronous Processing

Using Celery, Redis, background workers, and asynchronous Python to move expensive or failure-prone workloads away from synchronous request paths.

Real-Time Systems

Building real-time communication infrastructure for messaging, voice/video calls, and live video experiences using WebSockets and asynchronous server architecture.

API Architecture

Building structured APIs with clear service boundaries and predictable error handling.

Database Integrity

Using PostgreSQL transactions, constraints, and carefully designed persistence models to protect application invariants.

Testing

Using automated unit, integration, and system-level tests to verify critical behavior.

CI/CD

Automating testing and quality checks through GitHub Actions.

Observability

Designing systems so that failures, background processing, and system behavior can be understood and diagnosed.

---

Portfolio Architecture

The four backend portfolio systems demonstrate different layers of production engineering:

                    BACKEND ENGINEERING PORTFOLIO
                              │
          ┌───────────────────┼────────────────────┐
          │                   │                    │
     PAYMENT SYSTEMS     FINANCIAL SYSTEMS    ASYNC SYSTEMS
          │                   │                    │
          ▼                   ▼                    ▼
   Payment Flow         Transfer Engine      AsyncAPI Engine
          │                   │                    │
          │                   ▼                    │
          │              LedgerCore               │
          │                   │                    │
          └───────────────────┼────────────────────┘
                              │
                              ▼
                  Production Backend Principles
                              │
        ┌─────────────────────┼─────────────────────┐
        │                     │                     │
    Reliability          Data Integrity        Scalability
        │                     │                     │
    Idempotency          Transactions          Async Work
        │                     │                     │
     Testing               Auditability        Observability
        │                     │                     │
        └─────────────────────┼─────────────────────┘
                              │
                              ▼
                            CI/CD

MyCrony extends this portfolio into a large-scale application domain combining:

                         MyCrony
                            │
       ┌────────────────────┼────────────────────┐
       │                    │                    │
       ▼                    ▼                    ▼
   Social Platform     Creator Economy      Real-Time Systems
       │                    │                    │
       ▼                    ▼                    ▼
   Content/Feeds       Payments/Payouts    Messaging/Calls
                                                │
                                                ▼
                                         Live Video Streaming
                            │
                            ▼
                    Background Processing
                            │
                            ▼
                         Celery
                            │
                            ▼
                          Redis

---

Development Philosophy

I build backend systems around the principle that production software is more than making an endpoint return a successful response.

The important questions are:

- What happens when a request is retried?
- What happens when two operations happen concurrently?
- What happens when an external provider fails?
- How is financial state protected?
- How are transactions made atomic?
- How are background jobs retried safely?
- How are scheduled jobs handled?
- How are real-time connections managed?
- How are failures observed?
- How are changes tested automatically?
- How does the system behave under real operational conditions?

These principles guide the architecture of my portfolio projects.

---

Current Focus

My current focus is expanding these systems toward increasingly production-oriented architecture across:

- Financial infrastructure
- Payment systems
- Accounting systems
- API engineering
- Async Python
- Celery
- PostgreSQL
- Redis
- Distributed processing
- Real-time systems
- WebSockets
- Automated testing
- CI/CD
- Security
- Observability
- Reliable backend architecture

My goal is to demonstrate the ability to design and build real backend systems with strong correctness, reliability, maintainability, scalability, and operational characteristics rather than simply producing functional prototypes.

---

License

Individual portfolio projects may use their respective repository licenses.

MyCrony © 2026
