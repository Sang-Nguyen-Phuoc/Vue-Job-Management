# Job Management Project

This is a job management application built using **Vue.js** and **Tailwind CSS**. It allows users to manage job-related data with the following features:

- **Add new jobs**: Users can create new job entries.
- **Edit jobs**: Users can update existing job entries.
- **Delete jobs**: Users can remove job entries.
- **CRUD operations**: The project performs Create, Read, Update, and Delete operations using local mock data.
- **Axios for HTTP requests**: Axios is used to manage the CRUD data.
- **Routing views**: Multiple views are supported with Vue Router for navigation between different pages.

## Features

- **Add a Job**: Fill out a form to add a new job to the list.
- **Edit a Job**: Select a job from the list to modify its details.
- **Delete a Job**: Remove jobs from the list.
- **Mock Data**: The data is managed locally for this project, allowing for seamless CRUD operations.

## Tech Stack

- **Vue.js**: The progressive JavaScript framework used for building the user interface.
- **Tailwind CSS**: A utility-first CSS framework used for styling the application.
- **Axios**: Used for handling HTTP requests for CRUD operations.
- **Vue Router**: For handling routing and view navigation.

## Project Setup

1. Clone the repository:

   ```bash
   git clone [https://github.com/your-username/job-management-project.git](https://github.com/Sang-Nguyen-Phuoc/Vue-Job-Management.git)
   cd job-management-project
   ```

2. Install the dependencies:

   ```bash
   npm install
   ```

3. Run the development server:

   ```bash
   npm run serve
   ```

4. Open your browser and navigate to:

   ```bash
   http://localhost:8080
   ```

## Usage

- Navigate to the "Jobs" page to see the list of available jobs.
- Use the "Add Job" button to create a new job.
- Select a job from the list to edit or delete.

## Project Structure

```
├── src
│   ├── assets          # Static assets like images, fonts
│   ├── components      # Reusable Vue components
│   ├── views           # Application pages/views
│   ├── router          # Vue Router setup
│   ├── store           # Vuex store (if applicable)
│   ├── App.vue         # Main app component
│   └── main.js         # Entry point for Vue app
└── tailwind.config.js  # Tailwind CSS configuration
```

## Future Improvements

- Add user authentication for job management.
- Implement a backend for persistent data storage.
- Add pagination and filtering for job listings.

Feel free to adjust the content to suit the specifics of your project!
