# Job-Board

This Laravel-based Job Board application allows employers to post jobs, manage applications, and applicants to apply for jobs with salary expectations and CV uploads.

## Table of contents

- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Routes](#routes)
- [Middleware](#middleware)
- [Seeder](#seeder)
- [Usage](#usage)
- [Project Demo](#project-demo)


### Features

**Employer:**

- Post a job: Employers can add new jobs listing with details such as
  title, description, location, salary, etc.
- Edit a job: Employers can modify the details of the posted job only if the job has no applications.
- Soft delete: Employers can soft-delete their jobs.

**Applicant:**

- Apply for a job: Applicants can apply for specific jobs by providing their salary expectations and uploading their CV.
- View applied jobs: Applicants can see a list of jobs they have applied for, along with the salary they specified and the time since the application.
- Prevent duplicate applications: Applicants cannot apply for the same job multiple times.
- Cancel application: The applicant may change his mind and cancel his application for a particular job.

### Requirements

- PHP 8.0/late
- [Composer](https://getcomposer.org/)
- [Docker](https://www.docker.com/) and [Docker Compose](https://docs.docker.com/compose/)
- [Alpine.js](https://alpinejs.dev/)
- [Tailwind](https://tailwindcss.com/)
- [Laravel 10](https://laravel.com/)

### Installation

**1. Clone the repository:**
````angular2html
git clone https://github.com/Victoria-ElenaLazar/Job-Board
````
**2. Navigate to the project root directory:**
````angular2html
cd job_board
````
**3. Copy the '.env.example' file to create your own**

**4. Configure your database connection**

**5. Install dependencies:**
````angular2html
composer install
````
**6. Generate the application key:**
````angular2html
php artisan key:generate
````
**7. Start Docker containers:**
````angular2html
docker-compose up -d
````
**8. Run the migration and seed the database**
````angular2html
php artisan migrate --seed
````
**9. Start the development server**
````angular2html
php artisan serve
````
Follow the link to open the application.

### Routes
**Applicant**
- /auth/create
- /job/{job}/application
- /job/{job}/application/create
- jobs
- jobs/{job}


**Employer**
- /auth/create
- /employer/create
- jobs
- jobs/{job}
- my-job-applications
- my-job-applications/{my_job_application}
- my-jobs
- my-jobs/create
- my-jobs/{my_job}

### Middleware

- 'Check roles': Ensure that only employers may access certain routes.

### Seeder

- 'Database Seeder': Seeds the database with initial data.

### Usage

- Follow the installation steps mentioned above.
- Navigate to the application in your browser at http://localhost:8000.
- Log in. For the user to be an employer, he should register his company in the 'My jobs' section. If the user has not been registered with a company,
  he will be redirected to the specific form.
- Explore the available features based on your role.

## Project Demo


[Watch the video](public/job-board.mov)

Or [download the video](public/job-board.mov) to watch it.
