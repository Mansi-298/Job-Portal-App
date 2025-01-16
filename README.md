# Job Portal

A comprehensive web application designed to connect job seekers with employers. The platform streamlines the job search process by offering a user-friendly interface, advanced job search filters, and efficient application management.

## Features
- User Authentication: Secure login and registration for job seekers and employers.
- Job Listings: Employers can post job openings with detailed descriptions, requirements, and benefits.
- Search and Filter: Job seekers can search for jobs based on keywords, location, industry, and salary range.
- Resume Upload: Job seekers can upload their resumes for easy application submissions.
- Application Tracking: Employers can review, shortlist, and track applications in real-time.
- Admin Dashboard: Manage platform activities, monitor user interactions, and maintain job listings.

## Technologies Used
- Frontend: React (Vite), Shadcn UI, Redux Toolkit, Framer Motion
- Backend: Node.js, Express.js, MongoDB
- State Management: Redux Toolkit
- File Upload: Multer
- API Testing: Postman

## API Endpoints
1. User APIs
  - Register User:
    - POST /api/users/register
    - Body: { name, email, password, role }
    - Description: Register a new user (job seeker, employer, or admin).

  - Login User:
    - POST /api/users/login
    - Body: { email, password }
    - Description: Authenticate user and return JWT.

2. Company APIs
- Create Company:
    - POST /api/companies
    - Body: { name, location, description }
    - Auth: Employer Token
    - Description: Create a new company.
  
  - Get Company Details: 
    - GET /api/companies/:id
    - Auth: Public
    - Description: Retrieve details of a specific company.

3. Job APIs
  - Create Job:  
    - POST /api/jobs
    - Body: { title, description, salary, location }
    - Auth: Employer Token
    - Description: Post a new job under the authenticated employer's company.

  - Get Jobs: 
    - GET /api/jobs
    - Query: ?title=developer&location=remote
    - Auth: Public
    - Description: Retrieve jobs with optional filters.

4. Application APIs
  - Apply for a Job:
    - POST /api/applications
    - Body: { jobId }
    - Auth: Job Seeker Token
    - Description: Apply for a specific job.

  - Get Applications for a Job:
    - GET /api/applications/:jobId
    - Auth: Employer Token
    - Description: View all applications for a specific job.


## MongoDB Schema
- The MongoDB Atlas database stores records with the following fields:
  1. User Schema
  The User schema stores information about job seekers and employers.
  2. Company Schema
  The Company schema manages company-related information for employers.
  3. Job Schema
  The Job schema stores details about job postings.
  4. Application Schema
  The Application schema tracks job applications.

 ## Outputs


