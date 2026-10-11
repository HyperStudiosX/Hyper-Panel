# Hyper Panel — Frontend Prototype (Milestone 1)

A responsive, no-build frontend prototype for a Pterodactyl-inspired hosting control panel. Includes a dashboard, admin navigation, sample servers/nodes/users, activity, application API-key metadata, allocations, theme manager, settings, and a demo sign-in screen.

## Run locally

Open `index.html` in a modern browser. For best results, serve the folder with any static HTTP server, for example:

```bash
python -m http.server 8080
```

Then visit `http://localhost:8080`.

## Demo interactions

- Navigate from the left sidebar.
- Toggle light/dark appearance (saved in local browser storage).
- Search tables, export sample data, add demo server/node/user records, and open detail dialogs.
- Open the demo sign-in page by visiting `index.html#login`.

## Important security and implementation notes

This is a **frontend-only prototype**. All server, node, user, allocation, activity, and resource data is mock data held in browser memory. Demo CRUD actions do not contact a daemon or backend. The sign-in page accepts any non-empty credentials and is not authentication. No real API keys are generated or stored. Do not enter real credentials or deploy this as a production panel.

The next milestone should integrate this UI with a maintained Pterodactyl Panel codebase and a backend enforcing authentication, authorization, CSRF protections, validation, audit logging, secure secret storage, and rate limits. Privileged server operations should go through the trusted panel API and Wings-compatible infrastructure rather than browser-only code.
