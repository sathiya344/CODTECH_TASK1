index.html (HTML)
Purpose: This is the structure of your personal portfolio website.
Structure: It contains three primary sections:
Header: Contains a simple navigation bar with links to "About Me," "Projects," and "Blog."
Sections:
About Me: Where you can describe yourself (your skills, experience, etc.).
Projects: This is where your projects will be listed dynamically.
Blog: This is where your blog posts will be listed dynamically.
Footer: A simple copyright footer at the bottom of the page.
style.css (CSS)
Purpose: This file provides styling (visual design) for the HTML elements in your portfolio website.
Style Overview:
Body: Sets the font family, margin, padding, and background color.
Header: Styles the navigation bar with a dark background color and white text.
Sections: Each section has padding, a white background color, and a subtle shadow for a clean design.
Footer: Styled with a dark background and white text, positioned at the bottom.
script.js (JavaScript)
Purpose: This file handles dynamic content loading from the backend (Express.js) and populates the "Projects" and "Blog" sections with data.
Functionality:
fetchProjects(): Makes a GET request to /api/projects (from the backend) to fetch project data and displays it in the "Projects" section.
fetchBlogPosts(): Makes a GET request to /api/blog (from the backend) to fetch blog post data and displays it in the "Blog" section.
The data for projects and blog posts is dynamically added to the HTML, ensuring that you can update the content through the backend without changing the frontend.
Backend (Express.js)
The backend is written in Node.js using the Express.js framework, which serves the website’s static files and provides APIs to fetch project and blog post data.

server.js (Express.js)
Purpose: This file sets up the Express server and handles requests from the frontend.
Functionality:
Serving Static Files:
app.use(express.static('public')) serves the HTML, CSS, and JavaScript files (located in the public folder).
API Endpoints:
/api/projects: When the frontend requests project data, this API responds with a hardcoded list of projects.
/api/blog: Similarly, this API provides a list of blog posts in response to the frontend's request.
The server listens on port 3000, making the website accessible at http://localhost:3000 in your browser.
