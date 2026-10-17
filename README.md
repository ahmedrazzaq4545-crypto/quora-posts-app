# Quora-Inspired Posts Application

A simple web application inspired by Quora, built to practice backend web development using Node.js, Express.js, and EJS. Users can create posts, view all posts, explore individual post details, edit existing content, and delete posts.

## Features

- **Create Posts:** Add a username and post content through a form.
- **View All Posts:** Display all available posts on the main page.
- **View Post Details:** Open an individual post and view its details and unique ID.
- **Edit Posts:** Update the content of an existing post.
- **Delete Posts:** Remove posts from the list.
- **Unique Post IDs:** Generate unique identifiers using UUID.
- **Server-Side Rendering:** Render dynamic pages using EJS templates.
- **Custom Styling:** Apply CSS to style the posts and page layout.

## Tech Stack

- **Runtime:** Node.js
- **Backend Framework:** Express.js
- **Templating Engine:** EJS
- **Frontend:** HTML and CSS
- **Packages:** `method-override`, `uuid`

## Project Structure

```text
quora-posts-app/
├── public/
│   └── style.css
├── views/
│   ├── index.ejs
│   ├── new.ejs
│   ├── show.ejs
│   └── edit.ejs
├── index.js
├── package.json
├── package-lock.json
└── README.md
```

## Getting Started

### Prerequisites

- Node.js and npm installed on your computer.
- A code editor such as Visual Studio Code.

### Installation

1. Clone the repository:

   ```bash
   git clone <your-repository-url>
   ```

2. Navigate to the project directory:

   ```bash
   cd <your-project-folder>
   ```

3. Install the dependencies:

   ```bash
   npm install
   ```

### Run the Application

Start the server using:

```bash
node index.js
```

Alternatively, if Nodemon is installed, run:

```bash
nodemon index.js
```

Open the following URL in your browser:

**http://localhost:8080/posts**

## How It Works

The application uses Express.js routes to handle post operations and EJS templates to display dynamic content.

| Operation | HTTP Method | Route |
|---|---|---|
| View all posts | GET | `/posts` |
| Display the new-post form | GET | `/posts/new` |
| Create a post | POST | `/posts` |
| View an individual post | GET | `/posts/:id` |
| Display the edit form | GET | `/posts/:id/edit` |
| Update a post | PATCH | `/posts/:id` |
| Delete a post | DELETE | `/posts/:id` |

## Data Storage

Currently, posts are stored in an in-memory JavaScript array. Each post contains a unique ID, username, and content.

**Note:** Posts are not permanently stored. The array resets when the server restarts, so newly created or modified posts may be lost.

## What I Learned

Building this project helped me practice:

- Creating RESTful routes with Express.js.
- Implementing CRUD operations.
- Passing data from Express routes to EJS templates.
- Handling form submissions with `req.body`.
- Using route parameters with `req.params`.
- Generating unique IDs with UUID.
- Using `method-override` to handle PATCH and DELETE requests from HTML forms.
- Organizing views, static files, and backend logic.

## Future Improvements

- Add database integration for persistent storage.
- Improve the UI and make it fully responsive.
- Add user authentication and authorization.
- Add input validation and error handling.

## License

This project is currently intended for learning and practice.
