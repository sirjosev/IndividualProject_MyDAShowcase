# Interactive Data Analyst Portfolio

This is a single-file, zero-installation, interactive portfolio website designed to showcase data analyst projects. It's built with plain HTML, Tailwind CSS (via CDN), and Vanilla JavaScript, making it highly portable and easy to use. You can launch it directly from your local file system in any modern web browser.

## Overview

The portfolio features a modern, dark-themed, responsive design. It allows visitors to browse through project cards and view detailed information for each project in a modal window that mimics a Jupyter Notebook's cell-based layout (text cells, code snippet cells, visualization cells).

## Features

* **Single File Application:** The entire portfolio is contained within a single `.html` file.
* **Zero Installation:** No build process or server needed. Runs directly in a web browser from the file path.
* **Responsive Design:** Adapts to different screen sizes (desktop, tablet, mobile).
* **Dark Theme:** Modern and easy on the eyes.
* **Interactive Project Cards:** Displays a summary of each project.
* **Detailed Project Modal:**
    * Opens when a project card is clicked.
    * Presents project details in a "Jupyter Notebook" style.
    * Sections for Business Problem, Dataset, Tech Stack, Code Snippets, Key Findings, Visualizations, and Business Impact.
* **Smooth Animations:** Subtle fade-in animations for sections and modal transitions.
* **Easy to Customize (Data):** Project information is managed by editing a JavaScript array directly within the HTML file.

## Tech Stack

* **HTML5:** For the basic structure.
* **Tailwind CSS (via CDN):** For styling the user interface. *An internet connection is required for the first load to fetch Tailwind CSS styles.*
* **Vanilla JavaScript (ES6+):** For interactivity, dynamic content rendering, and modal functionality.

## How to Use

1.  **Save the File:**
    * Download or copy the entire code into a new file.
    * Save the file with an `.html` extension (e.g., `portfolio.html`).

2.  **Launch in Browser:**
    * Navigate to where you saved the file on your computer.
    * Double-click the `.html` file, or right-click and choose "Open with" your preferred web browser (Chrome, Firefox, Edge, Safari, etc.).
    * The portfolio will launch directly.

## Customization

All content and project data are embedded within the `portfolio.html` file. You'll need to edit this file with a text editor (like VS Code, Sublime Text, Notepad++, etc.) to make changes.

### 1. Personal Information

* **Hero Section (`<section id="beranda">`):**
    * Change the name "Yusuf Al-Rahman".
    * Update the profile image URL (`src` attribute of the `<img>` tag). The current one is a placeholder.
    * Modify the introductory paragraph.
    * Update GitHub and LinkedIn profile links.
* **Contact Section (`<section id="kontak">`):**
    * Update email address, LinkedIn URL, and WhatsApp number.
* **Footer (`<footer>`):**
    * Update the copyright year if necessary (though it's set dynamically by JavaScript).
    * Modify the "Portfolio Version" and "Last Updated" text as needed.

### 2. Project Data

This is the most crucial part. All project details are stored in a JavaScript array named `projectsData` found within the `<script>` tag towards the end of the HTML file.

The `projectsData` is an array of project objects. Each project object has the following structure:

```javascript
{
  id: "unique-project-id", // A unique identifier for the project (e.g., "flight-delay-prediction")
  title: "Project Title",
  description: "A short description for the project card.",
  businessProblem: "Detailed explanation of the business problem.",
  dataset: "Description of the dataset used.",
  techStack: ["Python", "Pandas", "SQL"], // Array of strings
  keyFindings: [ // Array of strings (each string is a bullet point)
    "Finding 1.",
    "Finding 2."
  ],
  businessImpact: "Description of the business impact.",
  projectUrl: "[https://github.com/yourusername/yourprojectrepo](https://github.com/yourusername/yourprojectrepo)", // Link to GitHub repo
  dashboardUrl: "#", // Link to a live dashboard, if any (use "#" if none)
  imageUrl: "[https://link-to-your-project-card-image.jpg](https://link-to-your-project-card-image.jpg)", // Image for the project card
  codeSnippets: [ // Array of code snippet objects
    {
      language: 'python', // Language for potential syntax highlighting (basic formatting provided)
      title: 'Descriptive Title for Code Snippet', // e.g., 'Loading Data'
      code: 'print("Hello World")\n# Your code here' // The actual code as a string. Use \n for newlines.
    }
  ],
  visualizations: [ // Array of visualization objects
    {
      title: "Title of Visualization 1",
      url: "[https://link-to-your-visualization-image1.jpg](https://link-to-your-visualization-image1.jpg)"
    },
    {
      title: "Title of Visualization 2",
      url: "[https://link-to-your-visualization-image2.jpg](https://link-to-your-visualization-image2.jpg)"
    }
  ]
}