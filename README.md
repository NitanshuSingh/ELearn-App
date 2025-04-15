# ELearn-App
📦 Project Description Project Name: Elearn Platform Tech Stack:  Backend: ASP.NET Core (.NET 8)  Frontend: React.js  Containerization: Docker  Web Server: Nginx (for frontend), ASP.NET Kestrel (for backend)
🔧 Overview
This project is a full-stack e-learning platform containerized using Docker for efficient development, deployment, and scalability.

🗄️ Database (MySQL)
A lightweight MySQL Docker container serves as the primary database.
Stores users, courses, enrollments, progress tracking, and other app data.
Environment variables like MYSQL_ROOT_PASSWORD, MYSQL_DATABASE, MYSQL_USER, and MYSQL_PASSWORD are configured for secure setup.
![image](https://github.com/user-attachments/assets/edd57336-bb8f-49d4-bfdb-adc603689db3)
![image](https://github.com/user-attachments/assets/fcc48c02-4751-4e63-b6bb-d367688b6f31)

🧠 Backend (.NET 8)
Developed using ASP.NET Core (.NET 8).
Contains business logic, API endpoints, and integration with databases or external services.
Published and optimized using dotnet publish in a multi-stage Docker build to reduce image size.
Final runtime image uses mcr.microsoft.com/dotnet/aspnet:8.0, ensuring only necessary files are included for production.

🎨 Frontend (React.js)
Built using modern React with a focus on responsive and user-friendly UI.
Compiled into static files using npm run build.
Served via a lightweight Nginx web server in a minimal Alpine-based container.
Frontend build is optimized for performance and size.

🚀 Deployment
The app is containerized with Docker using multi-stage builds for both frontend and backend.
Backend runs as a self-contained ASP.NET Core app.
Frontend is served statically using Nginx.
DNS and networking between containers are handled using Docker custom bridge networks
