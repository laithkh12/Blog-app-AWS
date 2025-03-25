
# BlogApp with AWS Amplify and Authentication

## Project Overview

This project is a blog application built with **Next.js** and **AWS Amplify**. It allows users to:

- View all blog posts.
- View a single blog post in detail.
- Edit and update blog posts.
- Add comments to blog posts.
- Upload and display cover images for each post.
- Authenticate users via AWS Cognito.

The app uses **AWS Amplify** to handle authentication, GraphQL API, and storage services like **AWS S3** for image uploads.

## Features

- **Post List**: Displays all the posts in a paginated list.
- **Post View**: View detailed content of a single post.
- **Post Edit**: Allows the creation and editing of blog posts.
- **Comments Section**: Users can leave comments on blog posts.
- **Cover Image**: Upload and display cover images for each post.
- **Authentication**: Login and register users using **AWS Cognito**.

## Technologies Used

- **Next.js**: React-based framework for server-side rendering.
- **AWS Amplify**: Managed backend for handling authentication, GraphQL API, and file storage.
- **AWS Cognito**: Provides user authentication and authorization.
- **AWS AppSync**: Managed GraphQL service to fetch and mutate data.
- **AWS S3**: Used to store cover images for the blog posts.

## Getting Started

### Prerequisites

Before you can run the app locally, ensure you have the following installed:

- **Node.js** (version 14 or higher)
- **npm** (Node package manager)
- **AWS Amplify CLI** (`npm install -g @aws-amplify/cli`)
- **Git** (for version control)

### Setting up the Project

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/blogapp.git
   cd blogapp
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Configure AWS Amplify:
   If you haven’t already, you need to set up Amplify in your project.
   - Initialize AWS Amplify with:
     ```bash
     amplify init
     ```
   - Add authentication and GraphQL API:
     ```bash
     amplify add auth
     amplify add api
     ```
   Follow the prompts to set up authentication (AWS Cognito) and the GraphQL API (AppSync).

4. Push the configuration to the cloud:
   ```bash
   amplify push
   ```

5. After the push completes, you'll receive details (like API URL and keys) that you can integrate into the project.

6. Run the app locally:
   ```bash
   npm run dev
   ```

   Visit `http://localhost:3000` in your browser to access the app.

### Environment Variables

Ensure your `.env.local` file has the necessary environment variables for AWS Amplify:

```env
NEXT_PUBLIC_AWS_REGION=your-aws-region
NEXT_PUBLIC_GRAPHQL_API_URL=your-graphql-api-url
NEXT_PUBLIC_AUTH_COGNITO_IDENTITY_POOL_ID=your-identity-pool-id
NEXT_PUBLIC_AUTH_COGNITO_USER_POOL_ID=your-user-pool-id
NEXT_PUBLIC_AUTH_COGNITO_APP_CLIENT_ID=your-app-client-id
```

### Running the App

Once the app is set up:

1. **Login/Signup**: Users can log in or sign up using **AWS Cognito** authentication.
2. **Create/Edit Posts**: Authorized users can create new blog posts or edit existing ones.
3. **View Posts**: Users can view a list of blog posts and read individual posts.
4. **Add Comments**: Users can comment on blog posts.
5. **Cover Images**: When creating/editing a post, users can upload a cover image, which is stored in **AWS S3**.

### Deployment

To deploy the app to production using **Vercel** or any other platform, follow these steps:

1. Install Vercel CLI:
   ```bash
   npm install -g vercel
   ```

2. Deploy:
   ```bash
   vercel
   ```

3. Follow the prompts to complete the deployment process.

## Contributing

1. Fork the repository.
2. Create your feature branch: `git checkout -b feature/your-feature`.
3. Commit your changes: `git commit -m 'Add your feature'`.
4. Push to the branch: `git push origin feature/your-feature`.
5. Open a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- **AWS Amplify**: Simplifies backend setup for authentication, API, and storage.
- **Next.js**: Powerful React framework for building server-rendered applications.
- **AWS Cognito**: Handles authentication and user management.
