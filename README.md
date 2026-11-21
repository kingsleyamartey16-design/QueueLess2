# QMS — Queue Management System (Frontend Prototype)

This is a browser-based frontend prototype based on the supplied QMS UI/UX design document. It demonstrates the customer, institution administrator and counter-staff journeys without a backend or database.

## Run locally

1. Extract the project folder if it was downloaded as a ZIP.
2. Open `index.html` in a modern browser (Chrome, Edge, Firefox or Safari).
3. Choose a customer, institution or staff sign-in path. Demo sign-in accepts any syntactically valid email and any password.

For a more consistent local development setup, serve the folder with a static file server, for example VS Code Live Server or `python -m http.server 8000`, then open `http://localhost:8000`.

## Project structure

- `index.html` — application entry point.
- `styles.css` — design system, page layouts and responsive styling.
- `app.js` — page rendering, demo data and frontend interactions.
- `assets/` — original QMS logo and illustration assets extracted from the supplied UI/UX PowerPoint.

## Included demo journeys

- Welcome, login and account-type selection screens.
- Customer dashboard, institution search, service selection, remote queue joining, live ticket view and appointment booking.
- Institution dashboard, service management, counters, staff and institution settings.
- Counter staff dashboard, queue management and queue history.
- Local demo state persisted in browser `localStorage`.

## Important limitations

This is a frontend-only prototype. Data is stored in the current browser and is not shared between devices or users. Login is simulated; there is no real authentication, email delivery, QR generation, push notification, server-side queue coordination or database. Queue values are demonstration data. A production implementation will need a backend API, persistent database, secure authentication/authorization, concurrency-safe ticket issuance, real-time updates and notification delivery.

## Design notes

The welcome page now follows the supplied split-screen composition: white content panel, pale-blue illustration panel, QMS logo, welcome message, primary actions and feature indicators. The PowerPoint's original logo and visual assets are included locally so they load without relying on external image URLs. Responsive breakpoints adapt the welcome/authentication layouts, navigation, cards and tables for smaller screens.
