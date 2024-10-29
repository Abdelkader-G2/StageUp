
# Internship Finder

A web application built with Next.js and Prisma to help students and professionals find internship opportunities. Users can create profiles, browse internship listings, and apply to relevant positions directly through the platform.

## Features

- **User Registration and Authentication**: Secure sign-up and login for both students and employers.
- **Profile Management**: Users can create and update profiles, including skills, experience, and education.
- **Internship Listings**: Employers can post internship opportunities with job descriptions, requirements, and application deadlines.
- **Application System**: Students can apply to internships, and employers can review applications.
- **Search and Filtering**: Search internships based on keywords, location, and field of interest.

## Technologies Used

- **Next.js** - React-based framework for server-side rendering and static site generation.
- **Prisma** - ORM for managing and interacting with the database.
- **PostgreSQL** - Database for storing users, internships, and applications (or another relational database supported by Prisma).
- **Tailwind CSS** - Styling framework for a responsive and modern UI.
- **NextAuth.js** - Authentication for secure login and session management.
- **Vercel** - Deployment for the Next.js app.

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (version 14 or later)
- [PostgreSQL](https://www.postgresql.org/download/) (or another supported database)
- Optional: [Prisma CLI](https://www.prisma.io/docs/getting-started/setup-prisma/start-from-scratch-prisma-migrate)

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/internship-finder.git
   cd internship-finder
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Set up environment variables:**
   - Create a `.env` file in the root directory and add the following variables:
     ```plaintext
     DATABASE_URL="postgresql://USER:PASSWORD@localhost:5432/your-database-name"
     NEXTAUTH_SECRET="your_secret_key"
     NEXTAUTH_URL="http://localhost:3000"
     ```

4. **Set up the database:**
   - Use Prisma to migrate your database schema:
     ```bash
     npx prisma migrate dev --name init
     ```

5. **Seed the database (optional):**
   - If you have a `prisma/seed.js` or `prisma/seed.ts` file, you can seed the database with initial data:
     ```bash
     npx prisma db seed
     ```

6. **Run the development server:**
   ```bash
   npm run dev
   ```

   Open [http://localhost:3000](http://localhost:3000) to view the app in your browser.

### Environment Configuration

Make sure to update the following environment variables in `.env`:

- `DATABASE_URL`: Connection string for your database.
- `NEXTAUTH_SECRET`: A secret key for NextAuth.js.
- `NEXTAUTH_URL`: The base URL of your app (e.g., `http://localhost:3000` for local development).

### API Routes

This application uses Next.js API routes for backend functionality. Here are some key API routes:

| HTTP Method | Endpoint                  | Description                           |
|-------------|---------------------------|---------------------------------------|
| `POST`      | `/api/auth/signin`        | Authenticate users                    |
| `POST`      | `/api/auth/signup`        | Register a new user                   |
| `GET`       | `/api/internships`        | Retrieve a list of internships        |
| `POST`      | `/api/internships`        | Create a new internship listing       |
| `GET`       | `/api/internships/[id]`   | Get details of a specific internship  |
| `POST`      | `/api/internships/[id]/apply` | Apply for an internship              |
| `GET`       | `/api/applications`       | Get a list of user applications       |

### Running Tests

If you have tests set up, you can run them using:

```bash
npm test
```

or for continuous test running:

```bash
npm run test:watch
```

## Deployment

To deploy this app to Vercel:

1. **Push your code to GitHub**.
2. **Link the repository to Vercel** in the Vercel dashboard.
3. **Set environment variables** in the Vercel settings for the project.
4. Deploy the project, and Vercel will handle the build and hosting.

## Contributing

Contributions are welcome! Please fork the repository and create a pull request for any feature or bug fix.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/YourFeature`)
3. Commit your changes (`git commit -m 'Add your feature'`)
4. Push to the branch (`git push origin feature/YourFeature`)
5. Open a pull request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.




### Explanation

- **Installation**: Includes steps for setting up the environment, configuring the database, and running the app locally.
- **Environment Configuration**: Lists the required environment variables for both local and production environments.
- **API Routes**: Provides a list of main API endpoints for the internship app.
- **Deployment**: Brief instructions for deploying to Vercel, which is popular for Next.js apps.

You can customize sections based on specific features and configurations of your app.