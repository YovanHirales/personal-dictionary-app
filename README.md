# Personal Dictionary App

A full-stack web app that lets you build your own personal dictionary. Search for words, fetch their definitions automatically, and save them as browsable cards.

**Live Demo:** https://mydictionary-d5eae45bfa0c.herokuapp.com/

---

## Features

- Search for one or multiple words at once
- Auto-fetches definitions and parts of speech via the [Wordnik API](https://developer.wordnik.com/)
- Saves words to a PostgreSQL database
- Displays words as responsive cards with up to 2 definitions each
- Edit or delete individual words
- Quick "Learn More" link to Google for each word

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React, Material UI (MUI) |
| Backend | Node.js, Express |
| Database | PostgreSQL |
| External API | Wordnik Dictionary API |
| Deployment | Heroku |

## Getting Started

### Prerequisites

- Node.js & npm
- PostgreSQL running on port 5432
- A [Wordnik API key](https://developer.wordnik.com/)

### Setup

1. **Clone the repo**
   ```bash
   git clone <repo-url>
   cd personal-dictionary-app
   ```

2. **Install dependencies**
   ```bash
   npm install
   cd client && npm install && cd ..
   ```

3. **Create a `.env` file** in the root directory:
   ```
   DICT_KEY=your_wordnik_api_key
   PG_USER=your_postgres_username
   PG_HOST=localhost
   PG_DATABASE=wordlist
   PG_PORT=5432
   ```

4. **Set up the database**
   ```bash
   psql -U your_postgres_username < database.sql
   ```

5. **Run the app**

   In one terminal (backend):
   ```bash
   npm start
   ```

   In another terminal (frontend):
   ```bash
   cd client && npm start
   ```

   The app will be available at `http://localhost:3000`.
