# Scalable URL Shortener (Amazon SDE I Level)

A scalable URL shortening service built with **Python**, **FastAPI**, **SQLite**, and an **in-memory caching system**.  
This project demonstrates **backend engineering, distributed system concepts, caching, and rate limiting**, making it fully aligned with **Amazon SDE I University Hiring requirements**.

---

## Tech Stack
- **Language:** Python 3
- **Framework:** FastAPI
- **Database:** SQLite (easily replaceable with PostgreSQL/DynamoDB)
- **Caching:** In-memory LRU cache (simulates Redis)
- **Testing:** FastAPI TestClient
- **Other Concepts:** Rate limiting, collision handling, dependency injection

---

## Features
- Shorten long URLs to unique short codes
- Retrieve original URLs via short codes
- Persistent storage with SQLite
- In-memory caching for fast lookups
- Rate limiting per client to prevent abuse
- Collision handling for hash generation
- Modular and scalable architecture

---

## Architecture Overview
- GET requests first check cache; if miss, fetch from DB  
- POST requests write to DB and cache  
- Rate limiter ensures controlled API usage  
- Hashing ensures unique short codes  

---

## How to Run (Locally / Colab)
1. Install dependencies:
```bash
pip install fastapi pydantic sqlalchemy


