Live Frontend (AWS):
http://15.206.128.232/

Live Backend (AWS – Django API):
http://13.233.178.226

A modern Employee Management System built with Next.js 14 (App Router) and integrated with a Django REST Framework API.
The system supports employee management, attendance tracking, and dashboard analytics using a scalable server/client architecture.

✨ Features

Employee dashboard with key statistics

Search & filter using URL query parameters

Employee CRUD operations

Attendance marking & viewing

Server-side rendering (SSR) with dynamic routing

Static & dynamic route optimization

Production deployment (Vercel + AWS)

🛠 Tech Stack
Frontend

Next.js 14 (App Router)

React

TypeScript

Tailwind CSS

Lucide Icons

date-fns

Backend

Django

Django REST Framework

Gunicorn

Nginx (recommended for production)

Deployment

Vercel (Frontend)

AWS EC2 Linux Server (Backend API)

📂 Project Structure (Frontend)
app/
 ├── page.tsx              # Dashboard (Server Component)
 ├── attendance/           # Attendance pages
 ├── employee/             # Employee dynamic routes

components/
 ├── employees/            # Employee UI components
 ├── shared/               # Shared components

lib/
 ├── api.ts                # Server-side API logic
 ├── types.ts              # Type definitions
🔑 Environment Variables

Create .env.local in root:

DJANGO_API_URL=http://13.233.178.226

⚠️ Do NOT wrap values in quotes
⚠️ Restart dev server after changes

🚀 Local Development

Install dependencies:

npm install

Run development server:

npm run dev

App runs at:

http://localhost:3000
🏗 Production Build
npm run build
npm start
🌐 Routing Strategy
Route	Type	Description
/	Dynamic	Dashboard with search params
/attendance	Static	Attendance overview
/employee/[id]	Dynamic	Employee profile

Next.js automatically determines static vs dynamic rendering based on data usage.

🧠 Architecture Decisions

useSearchParams() used only in Client Components

Client Components wrapped inside Server Components

API calls executed server-side

Environment variables never exposed to client

Secure backend URL handling

🔒 Security Considerations

Backend API URL handled server-side

No secrets exposed to browser

Server Components manage sensitive fetch calls

CORS configured on Django API

📦 Deployment Workflow
Frontend (Vercel)

Push code to GitHub

Import repository in Vercel

Add environment variables

Deploy

Backend (AWS EC2)

SSH into server

Pull latest code

Activate virtual environment

Restart Gunicorn

Reload Nginx

📌 Future Enhancements

Server-side pagination

Advanced filtering

Role-based access control

CSV / PDF export

Attendance analytics (charts)

JWT Authentication

👤 Author

Abdul Afjal
Full Stack Developer

