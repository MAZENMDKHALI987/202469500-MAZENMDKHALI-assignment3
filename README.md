# Mazen Mdkhali Portfolio

A responsive personal portfolio website for Mazen Mdkhali, a computer science student and software developer. The site presents Mazen's profile, skills, selected projects, and contact information. It also demonstrates advanced front-end functionality including external API integration, client-side validation, theme persistence, and dynamic page feedback.

## Features

- Responsive layout for desktop, tablet, and mobile screens
- Random quote fetched dynamically from DummyJSON
- User-friendly loading and API error states
- Time-based greeting
- Persistent light/dark theme using `localStorage`
- Contact form validation for required fields and email format
- Accessible validation feedback with `aria-invalid` and `aria-live`
- Sent-message list stored in the current page session
- Accessible navigation and native `<details>` interaction
- No framework or build step required

## Technologies

- HTML5
- CSS3
- Vanilla JavaScript
- DummyJSON Quotes API
- Browser `localStorage`
- Google Fonts

## Project Structure

```text
.
├── index.html
├── css/
│   └── styles.css
├── js/
│   └── script.js
├── assets/
│   └── images/
├── docs/
│   ├── ai-usage-report.md
│   └── technical-documentation.md
├── README.md
└── .gitignore
```

## Run Locally

### Option 1: Open directly

1. Download or clone this repository.
2. Open `index.html` in a modern browser.

### Option 2: Use a local server

1. Open the project folder in VS Code.
2. Install and enable the Live Server extension if it is not already available.
3. Right-click `index.html` and select **Open with Live Server**.
4. Open the address shown by Live Server, usually `http://127.0.0.1:5500`.

An internet connection is required to load Google Fonts and fetch quotes from DummyJSON.

## Using the Website

- Use the navigation links to move to About, Projects, or Contact.
- Use the theme button to switch between light and dark mode. The choice is saved in the browser.
- Submit the contact form with and without valid values to observe the validation behavior.
- Open the Sent messages panel to review messages added during the current page session.
- Reloading the page clears the sent-message list.

## API and State Behavior

The hero section requests a random quote from `https://dummyjson.com/quotes/random`. While the request is in progress, the page shows loading text. If the request fails, it displays a clear fallback quote and author message.

The selected theme is saved under the `theme` key in `localStorage` and restored when the page loads. Submitted messages are DOM state only; this portfolio is a static front-end application and does not send or store messages on a server.

## Performance and Testing

- Images are local assets rather than runtime image downloads.
- The application has no framework or package overhead.
- CSS variables avoid repeated theme-value definitions.
- JavaScript listens only to the interactions used by the page.
- Accessibility feedback uses native HTML elements and a single live status region.

Tested behavior should include:

- Theme toggle and persistence after reload
- Required-field, email-format, and valid-form submissions
- Quote loading success and network failure fallback
- Mobile and desktop responsive layouts
- Keyboard navigation and form feedback

## AI Usage

GitHub Copilot was used to assist with documentation and code review. AI suggestions were reviewed and changed where needed; the implementation and final files were verified locally.

Full details, benefits and challenges, learning outcomes, and the usage log are available in [AI Usage Report](docs/ai-usage-report.md).

## Documentation

- [Technical Documentation](docs/technical-documentation.md)
- [AI Usage Report](docs/ai-usage-report.md)

## Live Deployment

No deployment link is currently included. The project can be deployed with GitHub Pages or any static hosting service that serves the repository files.

## Author

Mazen Mdkhali
Student ID: `202469500`
