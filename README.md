User Profile Viewer - Configuration Error Simulation (Option C)
What I Built
A single-page "User Profile Viewer" web application using HTML, CSS, and JavaScript. The app's purpose is to fetch and display a user's profile information from a configured API endpoint.

Failure Type Chosen
Option C: Configuration Error (simulated). This specifically simulates a scenario where the application's API base URL configuration is incorrect, leading to an unreachable backend service.

How to Run
Save the provided code into a file named index.html.

Open index.html in your web browser. This application does not require a backend server as the API interaction, and its failure, are simulated directly in the browser.

How to Trigger the Failure
Open your browser's Developer Console (usually F12 or Ctrl+Shift+I) to observe the structured logs.

The application initially loads in the "happy path," fetching and displaying a mock user profile.

Check the "Simulate Configuration Error (Bad API URL)" checkbox.

Click the "Refresh Profile" button.

When the failure is triggered:

The application will attempt to fetch data from an intentionally unreachable URL (http://badhost:9999).

This will cause a network error (e.g., ERR_CONNECTION_REFUSED or Failed to fetch).

A prominent red error banner will appear at the top of the page, indicating the configuration issue.

A structured JSON log detailing the configuration error will be printed to the Developer Console.

Expected Log Example (JSON)
An example of the structured log printed to the console when the configuration error occurs:

JSON

{
  "timestamp": "2023-11-20T08:30:15.123Z",
  "configKey": "USERS_API_URL",
  "badValue": "http://badhost:9999/api/users/1",
  "errorCode": "CONFIG_ERROR",
  "lowLevelErrorMessage": "Failed to fetch (likely connection refused or host unreachable)"
}
