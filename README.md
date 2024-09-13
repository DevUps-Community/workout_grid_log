# Workout Activity Tracker API (Github Style)

This project is an API built using Node.js to track daily workouts in a GitHub-style activity log grid. The API allows users to log and visualise the number of workouts (reps, sets completed) performed each day in a calendar format, similar to GitHub's contribution graph.

## Features

- **Daily Workout Logs**: Track the number of sets and reps completed each day.
- **GitHub-style Activity Grid**: Visual representation of workout activity in a grid format, highlighting workout intensity on each day.
- **RESTful API Endpoints**: Provides endpoints for adding, updating, and retrieving workout data.
- **Customisable Timeframes**: Supports querying workout activity by different time periods (daily, weekly, monthly).
- **User Authentication**: Secure authentication to keep workout logs private.
- **Data Aggregation**: Summarise workout data such as total sets and reps over specific timeframes.

## API Endpoints

### Authentication
- `POST /auth/signup`: Create a new user account.
- `POST /auth/login`: Log in with an existing user account.

### Workout Logs
- `POST /workouts`: Add a new workout log (reps, sets) for a specific day.
- `GET /workouts`: Retrieve all workouts for the logged-in user, displayed in a grid format.
- `PUT /workouts/:id`: Update a specific workout log.
- `DELETE /workouts/:id`: Delete a specific workout log.

### Stats & Visualisation
- `GET /workouts/grid`: Get a GitHub-style grid of workout activity.
- `GET /workouts/summary`: Get a summary of total reps and sets over a specified time range.

## Technologies Used

- **Node.js**: Backend API built with Express.js.
- **PostgreSQL**: Database for storing workout data.
- **GitHub Activity Grid Design**: Visualising daily workout activity.
- **Docker**: Containerised deployment for consistent development environments.
- **AWS (optional)**: Deployed using AWS Lambda and EC2 for scalability.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/workout-activity-tracker-api.git
   cd workout-activity-tracker-api
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Set up environment variables:
   - Create a `.env` file with the following variables:
     ```bash
     DB_HOST=your_postgresql_host
     DB_PORT=your_postgresql_port
     DB_NAME=your_database_name
     DB_USER=your_database_user
     DB_PASSWORD=your_database_password
     JWT_SECRET=your_secret_key
     ```

4. Run migrations to set up the database schema:
   ```bash
   npm run migrate
   ```

5. Start the server:
   ```bash
   npm start
   ```
