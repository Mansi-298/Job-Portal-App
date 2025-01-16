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
![Image](https://github.com/user-attachments/assets/e5fc9434-7883-42e5-b7be-2fb48372c169)

![Image](https://github.com/user-attachments/assets/4029aaa9-14ee-4a6c-9c66-8ecc1670a435)

![Image](https://github.com/user-attachments/assets/06de3fcc-4870-4827-ac88-031b8cb

![Image](https://github.com/user-attachments/assets/c86da73b-3bd7-4ed6-ba8a-8e6b99c2ecdd)

![Image](https://github.com/user-attachments/assets/f08aae53-839d-472d-985a-5fca87252419)

![Image](https://github.com/user-attachments/assets/c3ec0d31-299b-48fc-ae82-fcc9c1cb5179)

![Image](https://github.com/user-attachments/assets/fd936087-01a2-4dae-b7b7-25d04fa9430e)

