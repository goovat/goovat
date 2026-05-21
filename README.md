# MyCrony


I'm **Great (goovat)** — a backend-focused developer building scalable platforms with Python and Django.

Currently building **MyCrony**, a full-stack social networking and creator economy platform combining social media, monetization, creator tools, real-time communication, and payment infrastructure.

MyCrony is a full-stack social networking, creator economy, media sharing, and monetization platform built with Django. The project combines social media functionality, creator tools, content management, live interactions, personalized feeds, analytics, and payment infrastructure into one ecosystem.

The platform supports content creators, communities, media publishing, social interactions, monetization workflows, creator earnings, and real-time engagement systems.

---

# Table of Contents

- Overview
- Features
- Architecture
- Applications
- Core Modules
- Creator Economy
- Payment Infrastructure
- Feed System
- Real-Time Features
- Analytics
- Moderation & Administration
- Media Support
- Project Structure
- Technology Stack
- Installation
- Environment Setup
- Database Setup
- Running Development Server
- Running Background Services
- Static Files
- Media Files
- Stripe Integration
- WebSocket Support
- Creator Workflows
- API Structure
- Development Commands
- Deployment Notes
- Future Roadmap
- License

---

# Overview

MyCrony is designed as a creator-first social ecosystem providing:

- User profiles
- Social connections
- Posts and media publishing
- Reels and stories
- Live streaming
- Messaging
- Recommendation systems
- Creator monetization
- Earnings dashboards
- Subscription systems
- Financial reporting
- Payment processing
- Creator studio management

The project follows a modular Django architecture.

---

# Features

## User System

Authentication and account features include:

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
- Close friends support
- User discovery
- Creator onboarding

---

## Content Platform

Users can publish and manage:

### Posts

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

### Stories

Features include:

- Story publishing
- Story viewing
- Story highlights
- Temporary content support

### Reels

Supports:

- Reel creation
- Reel playback
- Reel feeds
- Reel interactions
- Duet functionality

### Galleries

Gallery system supports:

- Gallery creation
- Image collections
- Thumbnail generation
- Media previews

### Collections

Users may organize content into collections.

---

# Feed System

MyCrony includes a recommendation and ranking engine.

Implemented feed types:

- Following feed
- Discover feed
- Trending feed
- Personalized feed
- Live feed
- For-you feed

Ranking engines include:

- Chronological ranking
- Engagement ranking
- Popularity ranking
- Recency ranking
- Personalized ranking
- Hybrid ranking

Feed services include:

```text
feeds/services/

Algorithms:

feeds/algorithms/

Feed interactions:

Likes

Saves

Shares

Comments

Reports

Follow actions

Blocks

Mutes



---

Creator Studio

Creator tools are available through the studio module.

Features:

Creator dashboard

Studio management

Draft management

Publishing workflows

Scheduling

Analytics dashboard

Audience monitoring

Content performance tracking


Studio module:

studio/


---

Creator Economy

MyCrony includes creator monetization infrastructure.

Supported systems:

Earnings

Earnings dashboard

Revenue tracking

Creator shares

Payment history

Financial summaries


Payouts

Supports:

Withdrawal requests

Payout schedules

Payout methods

Creator payments


Revenue Systems

Includes:

Revenue configuration

Creator percentage allocation

Promotion shares

Transparency reports


Subscription System

Subscription support includes:

Recurring plans

Membership flows

Subscription tracking


Financial Infrastructure

Economics module contains:

Invoice models

Tax models

Revenue models

Reports

Exchange models

Payment models

Webhooks

Financial analytics


Directory:

economics/


---

Stripe Payment Infrastructure

Stripe powers payment operations inside MyCrony.

Implemented payment support:

Payment processing

Subscription billing

Webhook integration

Revenue tracking

Creator payments

Transaction workflows


Stripe configuration files:

economics/webhooks/stripe_urls.py

Payment flow service:

economics/services/payment_flow.py

Webhook support:

economics/webhooks/

Supported providers:

Stripe

PayPal

Bank integrations



---

Real-Time Features

MyCrony supports real-time communication.

Messaging

Features:

Conversations

Inbox

Sent messages

Drafts

Forwarding

Search

Threads


Chat Features

Message bubbles

Reactions

Typing indicators


Calls

Supported:

Voice calls

Video calls

Call history


Live Streaming

Features:

Stream creation

Live rooms

Stream viewing

Stream thumbnails


Modules:

live/


---

Analytics

Analytics infrastructure includes:

Creator Analytics

Audience metrics

Revenue analytics

Content performance

Earnings reports


Content Analytics

Engagement reports

Feed metrics

Post performance


Financial Analytics

Revenue reports

Payment reports

Transparency metrics


Administrative Analytics

User activity

System monitoring

Platform statistics



---

Moderation & Administration

Moderation support includes:

Flagged content review

Reporting workflows

Copyright handling

Administrative dashboards

User monitoring

Shadow banning support

Access controls

Permissions


Administrative templates:

templates/moderation/


---

Media Support

Supported uploads include:

Images:

JPG

PNG


Video:

MP4


Audio:

Voice messages

Audio uploads


Directories:

media/

Media storage includes:

Avatars

Covers

Content media

Galleries

Voice messages

Draft thumbnails

Live thumbnails



---

Applications

users/          User management
content/        Posts and publishing
feeds/          Feed engine
economics/      Payments and monetization
studio/         Creator tools
live/           Live streaming
core/           Shared utilities
mycrony/        Project configuration


---

Project Structure

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

Backend:

Python

Django

Django Channels


Frontend:

HTML

CSS

JavaScript

Bootstrap


Database:

Development:

SQLite


Realtime:

WebSockets

ASGI


Background Processing:

Celery


Payments:

Stripe

PayPal


Server:

WSGI

ASGI



---

Installation

Clone repository:

git clone https://github.com/<username>/MyCrony.git

cd MyCrony

Create environment:

Linux:

python -m venv venv

source venv/bin/activate

Windows:

python -m venv venv

venv\Scripts\activate

Install dependencies:

pip install -r requirements.txt


---

Environment Setup

Create:

.env

Example:

DEBUG=True

SECRET_KEY=your_secret_key

STRIPE_SECRET_KEY=

STRIPE_PUBLISHABLE_KEY=

EMAIL_HOST=

EMAIL_PORT=

EMAIL_HOST_USER=

EMAIL_HOST_PASSWORD=


---

Database Setup

Run migrations:

python manage.py makemigrations

python manage.py migrate

Create admin:

python manage.py createsuperuser


---

Running Development Server

python manage.py runserver

Open:

http://127.0.0.1:8000


---

Running Background Services

Celery:

celery -A mycrony worker -l info

Scheduler:

celery -A mycrony beat -l info


---

Static Files

Collect static assets:

python manage.py collectstatic

Static directories:

static/
staticfiles/


---

Media Files

Media directory:

media/

Contains:

avatars

covers

posts

galleries

voice messages

live thumbnails



---

WebSocket Support

Realtime routing:

users/routing.py

feeds/routing.py

ASGI entry:

mycrony/asgi.py


---

Creator Workflow

Creator flow:

User Registration

↓

Profile Setup

↓

Creator Onboarding

↓

Content Publishing

↓

Audience Growth

↓

Analytics Tracking

↓

Revenue Generation

↓

Payout Processing


---

API Structure

API modules:

content/api_views/

feeds/views/api_views.py

feeds/services/views/api_views.py

Serialization support:

serializers.py


---

Development Commands

Run server:

python manage.py runserver

Migrations:

python manage.py makemigrations

python manage.py migrate

Create admin:

python manage.py createsuperuser

Collect static:

python manage.py collectstatic

Tests:

python manage.py test


---

Deployment Notes

Recommended production stack:

Nginx

Gunicorn

Daphne

Redis

PostgreSQL

Celery workers

Stripe webhooks


Development currently uses SQLite.

Production migration to PostgreSQL is recommended.


---

Future Roadmap

Planned improvements:

AI recommendations

Marketplace support

Advanced creator tools

Enhanced moderation

Distributed feeds

Recommendation optimization

Creator marketplace

Extended analytics



---

License

MIT License

MyCrony © 2026
