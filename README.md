# Personal-Travel-Tracker

## Overview
The Country Visited Tracker is a personal web application I built to help keep track of the countries I've visited and share my travel experiences with friends. The app allows users to log in, add countries to their visited list, and view other users' visited countries. The application leverages a PostgreSQL database to store user and country information and is built using Express.js for the backend and EJS for templating.

## Key Features

1. **User Management:**
   - Users can log in and out.
   - New users can be added to the system.
   - Each user has a unique ID and a personalized color associated with their profile.

2. **Country Tracking:**
   - Users can add countries to their visited list.
   - The application checks if the country is valid before adding it to the list.
   - The list of visited countries is displayed on the home page along with the total number of countries visited by the user.

3. **Database Integration:**
   - Utilizes PostgreSQL to store user information and visited countries.
   - Handles database queries for adding new countries, retrieving user data, and checking visited countries.

4. **Dynamic Rendering:**
   - The home page dynamically renders the list of visited countries and user information using EJS.
   - Provides error messages and feedback for user actions, such as adding a new country or handling duplicate entries.

## Technical Details

- **Backend:** 
  - Built using Express.js for handling HTTP requests and routing.
  - Uses body-parser middleware to parse URL-encoded bodies.
  - Connects to a PostgreSQL database using the `pg` library.

- **Frontend:**
  - Employs EJS for server-side templating.
  - Renders dynamic content based on user interactions and database queries.

- **Database Schema:**
  - **Users Table:** Stores user information including ID, name, and color.
  - **Countries Table:** Contains a list of countries with their respective codes.
  - **Visited Countries Table:** Records the relationship between users and the countries they have visited.

## Endpoints

- **GET /**: Renders the home page with the list of visited countries and users.
- **POST /add**: Adds a new country to the visited list for the current user.
- **POST /user**: Handles user switching and adding new users.
- **POST /new**: Adds a new user to the database.

## Error Handling
- Ensures robust error handling for database operations, such as querying country codes and inserting new users.
- Provides user-friendly error messages for common issues like duplicate entries and invalid country names.

## Usage

1. Start the server by running the application.
2. Navigate to the home page to view the list of visited countries.
3. Add new countries by entering the country name.
4. Switch users or add new users through the user management interface.

## Getting Started

1. Install the necessary dependencies using `npm install`.
2. Set up the PostgreSQL database and configure the connection details.
3. Start the server using `npm start`.
4. Access the application at `http://localhost:3000`.

This project is ideal for individuals or groups who enjoy traveling and want to keep a record of the countries they have visited. It also serves as a great example of integrating Express.js with PostgreSQL and EJS for dynamic web applications.
