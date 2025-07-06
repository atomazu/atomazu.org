# atomazu.org

This repository contains the source code for my personal website and blog, [blog.atomazu.org](https://blog.atomazu.org).

Up to date as of [2b51f17](https://github.com/atomazu/atomazu.org/commit/2b51f17e2e8b227f98645a7580d9161893378780).

## Project Overview

This project is a dual-purpose repository that includes both the frontend and backend for the website.

-   **Frontend**: A static site built with HTML, CSS, and vanilla JavaScript. It fetches and displays blog posts from the backend API.
-   **Backend**: A Node.js application using Express.js. It serves a REST API for managing blog posts, which are stored as Markdown files with front-matter.

## Getting Started

### Installation

1.  Clone the repository:
    ```bash
    git clone https://github.com/atomazu/atomazu.org.git
    cd atomazu.org
    ```
2.  Install the dependencies:
    ```bash
    npm install
    ```

### Running the application

1.  Create a `.env` file in the root of the project and add the following environment variables:

    ```
    PORT=3000
    TOKEN=your_secret_token
    ```

2.  Start the server:

    ```bash
    npm start
    ```

The application will be available at `http://localhost:3000`.

#### I personally like to run it [declaratively](https://github.com/atomazu/my-nixos/blob/18a350105f59c80a1067dda656a361a43a1f9b3f/hosts/desktop/default.nix).

## API Endpoints

-   `GET /posts`: Get a list of all blog posts.
-   `GET /posts/:slug`: Get a single blog post by its slug.
-   `POST /posts`: Create a new blog post (requires authentication).
-   `PUT /posts/:slug`: Update a blog post (requires authentication).
-   `DELETE /posts/:slug`: Delete a blog post (requires authentication).
-   `POST /posts/:slug/like`: Increment the like count for a post.
-   `GET /auth/validate`: Validate the authentication token.

## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).
