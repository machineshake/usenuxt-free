# UseNuxt SaaS Starter Project 🚀

Welcome to UseNuxt, a comprehensive SaaS starter project built with Nuxt.js, designed to kickstart your project with all the essential features you need. With built-in team management, authentication, and more, UseNuxt provides a solid foundation for building robust SaaS applications.

## Features ✨

- **Team Management:** Easily manage team members and roles right out of the box.
- **Authentication:** Secure authentication system integrated.
- **Database Management:** Commands to manage your database schema and data.
- **Modern UI:** Utilizes @nuxt/ui for a sleek, modern user interface.
- **SEO Friendly:** Built-in SEO optimization for better visibility.
- **Fully Customizable:** Flexible codebase that allows for easy customization and scalability.

## Demo 🚀

Experience UseNuxt in action and see firsthand what it can do for your next project.

👉 [Visit the Demo](http://demo.usenuxt.com)

## Installation 🛠

Before you begin, ensure you have [Node.js](https://nodejs.org/) installed on your machine. Then, follow these steps to get UseNuxt up and running:

```bash
# Clone the repository
git clone https://yourrepository.com/nuxt-app.git

# Navigate into the project directory
cd nuxt-app

# Install dependencies
npm install

# Prepare your environment (husky hooks, etc.)
npm run prepare
```

## Environment Setup 🌳

1. Copy the `.env.example` file to `.env`:
   ```
   cp .env.example .env
   ```

2. Open the `.env` file and update the following variables:

   - `NUXT_PUBLIC_URL`: Set this to your local development URL (e.g., `http://localhost:3000`)
   - `NUXT_PUBLIC_NAME`: Set your project name
   - `NUXT_DATABASE_URL`: Set your PostgreSQL connection string

3. Obtain and set up the following API tokens:

   - Google OAuth credentials:
     - Go to the [Google Cloud Console](https://console.cloud.google.com/)
     - Create a new project or select an existing one
     - Enable the Google+ API
     - Create OAuth 2.0 credentials (Client ID and Client Secret)
     - Set `NUXT_GOOGLE_CLIENT_ID` and `NUXT_GOOGLE_CLIENT_SECRET` in your `.env` file

   - Stripe API keys:
     - Sign up for a [Stripe account](https://stripe.com) or log in to an existing one
     - Go to the Developers section and find your API keys
     - Set `NUXT_STRIPE_PUBLISHABLE_KEY` and `NUXT_STRIPE_SECRET_KEY` in your `.env` file
     - To get the `NUXT_STRIPE_WEBHOOK_SECRET`, you'll need to set up a webhook in the Stripe dashboard and use the provided secret

   - (Optional) Plausible Analytics:
     - If you want to use Plausible for analytics, sign up at [Plausible.io](https://plausible.io/)
     - Set `PLAUSIBLE_DOMAIN` and `PLAUSIBLE_API_HOST` in your `.env` file

Remember to keep your `.env` file secure and never commit it to version control.
## Database Setup 🗄️

This project uses PostgreSQL as its database. Follow these steps to set up your database:

1. Install PostgreSQL:
   - For macOS, you can use Homebrew: `brew install postgresql`
   - For Windows, download and install from the [official PostgreSQL website](https://www.postgresql.org/download/windows/)
   - For Linux, use your distribution's package manager (e.g., `sudo apt-get install postgresql` for Ubuntu)

2. Create a new PostgreSQL database for your project.

3. Update the `NUXT_DATABASE_URL` in your `.env` file with your PostgreSQL connection string. It should look something like this:
   ```
   NUXT_DATABASE_URL="postgresql://username:password@localhost:5432/database_name"
   ```

4. Run the database setup scripts:
   ```
   npm run db:push
   npm run db:gen
   ```
   These commands will create the necessary tables in your database and generate the required artifacts for Drizzle ORM.

The project uses Drizzle ORM to manage the database schema and operations. User management tables will be automatically created and managed by the Lucia auth library.

## Available Scripts 📜

UseNuxt comes with several pre-configured npm scripts to help with your development:

- `npm run dev`: Starts the development server.
- `npm run build`: Builds your application for production.
- `npm run preview`: Preview the generate static site.
- `npm run start`: Launches the built application.
- `npm run lint`: Lints and fixes files.
- `npm run db:push`: Pushes schema changes to your database.
- `npm run db:gen`: Generates database artifacts.

## Dependencies 📦

[The original dependencies section remains unchanged]

## Contributing 🤝

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License 📄

Distributed under the MIT License. See `LICENSE` for more information.
