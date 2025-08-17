# Flag Game Backend

This is the backend for the [Flag Game](https://github.com/neha-deepthi/flag-game/), a quiz application where users guess country names based on their flags. The backend is built with Node.js, Express, and PostgreSQL.

## Features

- Serves random flag quiz questions from a PostgreSQL database
- Tracks the user's score during the session
- Uses EJS for rendering quiz pages

## Prerequisites

- [Node.js](https://nodejs.org/)
- [PostgreSQL](https://www.postgresql.org/)
- A `flags` table in your `world` database with at least a `name` column and a flag image or data column

## Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/neha-deepthi/flag-game.git
   cd flag-game
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Configure the database:**
   - Update the database credentials in `index.js` if needed:
     ```js
     const db = new pg.Client({
       user: "postgres",
       host: "localhost",
       database: "world",
       password: "Neha@2005",
       port: 5432,
     });
     ```
   - Ensure your `flags` table is populated with country names and flag data.

4. **Start the server:**
   ```bash
   node index.js
   ```

5. **Open your browser:**
   - Visit [http://localhost:3000](http://localhost:3000)

## File Structure

- `index.js` — Main backend server file
- `views/index.ejs` — EJS template for the quiz page
- `public/` — Static assets (if any)

## Usage

- The home page displays a flag and asks for the country name.
- Submit your answer; your score updates with each correct answer.
