![image](https://github.com/user-attachments/assets/01c75ef1-e894-4c66-afe8-837749d3f7d1)

![image og blog](https://github.com/user-attachments/assets/93be5b7f-9e58-4bdb-8722-1f7482158cdb)


# Project Setup Guide

## Backend Setup

1. **Navigate to the Backend Directory:**

   ```bash
   cd backend
   ```

2. **Install Dependencies:**

   Install all the necessary Node.js packages by running:

   ```bash
   npm install
   ```

3. **Configure the Environment Variables:**

   - **Update the `.env` file:** Add your database connection string to the `.env` file. It should look something like this:

     ```env
     DATABASE_URL="your-database-connection-string"
     ```

   - **Update the `wrangler.toml` file:** Configure the `wrangler.toml` file with your compatibility date and environment variables. Here’s an example of how it should look:

     ```toml
     compatibility_date = "2024-08-21"

     [vars]
     DATABASE_URL = "your-connection-pool-string"
     JWT_SECRET = "your-jwt-secret"
     ```

4. **Set Up Prisma:**

   Initialize and apply your Prisma schema migrations:

   ```bash
   npx prisma migrate dev --name init_schema
   ```

   Generate the Prisma client:

   ```bash
   npx prisma generate --no-engine
   ```

5. **Start the Backend Server:**

   Run the development server:

   ```bash
   npm run dev
   ```

6. **Test Your Backend:**

   Import the `medium.postman_collection` file into Postman to test your backend endpoints.

## Frontend Setup

1. **Navigate to the Frontend Directory:**

   ```bash
   cd frontend
   ```

2. **Install Dependencies:**

   Install all necessary Node.js packages for the frontend:

   ```bash
   npm install
   ```

3. **Start the Frontend Server:**

   Run the frontend development server:

   ```bash
   npm run dev
   ```
