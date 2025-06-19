# Database Schema for Personal Webpage Portfolio

## Overview
This schema is designed to support the MVP features of the personal webpage portfolio, including project showcase and contact form submissions. The site is primarily content-driven, so the schema is simple and can be implemented in a document-based database (e.g., MongoDB) or as markdown/static files for initial launch.

---

## Collections / Tables

### 1. Projects
- **_id**: ObjectId / UUID (Primary Key)
- **title**: String (Project title)
- **description**: String (Short project summary)
- **technologies**: [String] (List of technologies used)
- **githubUrl**: String (URL to code repository)
- **demoUrl**: String (URL to live demo, optional)
- **imageUrl**: String (Project image, optional)
- **date**: Date (Completion or published date)
- **featured**: Boolean (Showcase on homepage)

### 2. Resume
- **_id**: ObjectId / UUID (Primary Key)
- **content**: String (Markdown or HTML content of the resume)
- **lastUpdated**: Date

### 3. ContactSubmissions
- **_id**: ObjectId / UUID (Primary Key)
- **name**: String (Sender's name)
- **email**: String (Sender's email)
- **message**: String (Message content)
- **submittedAt**: Date
- **read**: Boolean (Has the message been read?)

---

## Example (MongoDB Document)

### Project
```json
{
  "_id": "...",
  "title": "Personal Portfolio Website",
  "description": "A website to showcase my projects and resume.",
  "technologies": ["React", "Tailwind CSS"],
  "githubUrl": "https://github.com/username/portfolio",
  "demoUrl": "https://username.com",
  "imageUrl": "/images/portfolio.png",
  "date": "2025-06-01T00:00:00Z",
  "featured": true
}
```

### Resume
```json
{
  "_id": "...",
  "content": "# Resume\n...markdown or HTML...",
  "lastUpdated": "2025-06-10T00:00:00Z"
}
```

### Contact Submission
```json
{
  "_id": "...",
  "name": "Jane Doe",
  "email": "jane@example.com",
  "message": "I am interested in working with you!",
  "submittedAt": "2025-06-19T12:00:00Z",
  "read": false
}
```

---

## Notes
- For a static site, projects and resume can be stored as markdown files instead of a database.
- For MVP, only the Projects and ContactSubmissions collections are strictly necessary; Resume can be static content.
