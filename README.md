# Syllabus Saver

Syllabus Saver is a full-stack web application that helps students turn course syllabi into organized course and task data. Users can upload a PDF syllabus, have it processed by an Azure serverless backend, and view extracted courses, assignments, due dates, task types, and workload insights through a simple web interface.

## Features

- Upload PDF syllabi through a browser interface
- Store uploaded files in Azure Blob Storage
- Process syllabus PDFs with an Azure Blob-triggered Function
- Extract structured course and task data using Azure OpenAI
- Store courses and tasks in Azure Cosmos DB
- View courses and assignments through dynamic frontend pages
- Add and delete courses and tasks
- View workload insights with summary cards and charts

## Tech Stack

- Frontend: HTML, CSS, JavaScript, Chart.js
- Backend: Azure Functions, Node.js
- Storage: Azure Blob Storage
- Database: Azure Cosmos DB
- AI: Azure OpenAI
- PDF parsing: pdf-parse

## Architecture

1. A user uploads a syllabus PDF from the frontend.
2. The upload endpoint stores the PDF in Azure Blob Storage.
3. A Blob-triggered Azure Function processes the uploaded syllabus.
4. The PDF text is extracted and sent to Azure OpenAI.
5. The model returns structured JSON containing course and task data.
6. The data is stored in Azure Cosmos DB.
7. The frontend retrieves and displays courses, tasks, and insights.

## Pages

- Home: Upload a syllabus PDF.
- Courses: View and delete extracted courses.
- Tasks: View, filter, add, and delete assignments.
- Insights: View course/task statistics and workload charts.

## Future Improvements

- Add user authentication
- Support multiple users instead of demo-user mode
- Improve date extraction accuracy
- Add calendar export
- Add edit functionality for extracted tasks
- Deploy frontend and backend publicly