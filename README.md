# Email-Tracker

Email-Tracker is a comprehensive email tracking solution that includes a tracking dashboard, a robust API, and a Chrome extension for Gmail integration. It empowers you to see exactly when and how your emails are opened.

## Features

- **Live Email Tracking:** Tracks email opens in real-time using an invisible 1x1 GIF pixel.
- **Analytics Dashboard:** A centralized interface built with Next.js to view all your tracked emails and detailed open statistics.
- **Gmail Chrome Extension:** Seamlessly integrates with Gmail to track emails directly from your inbox.
- **Advanced Insights:** Captures and analyzes recipient data, including IP address, User-Agent, device type, client type, and geographic location (country/city).
- **Bot Detection:** Intelligently filters out bot and proxy opens to ensure your analytics are accurate.
- **Real-time Notifications:** Supports webhook integrations to notify you instantly when an email is opened.
- **Robust API:** Extensible Next.js API endpoints for managing tracking IDs, streaming events, and logging open activity.

## Architecture

The platform is divided into three main components:

1. **Next.js Web Application:** The core dashboard and API interface, connected to MongoDB for data persistence.
2. **API Routes:** Handles pixel requests, webhook notifications, and live streaming of open events.
3. **Chrome Extension:** Injects tracking functionality into the Gmail web interface using background service workers and content scripts.

## Getting Started

### Prerequisites

- Node.js
- MongoDB

### Installation

1. Clone the repository.
2. Install dependencies:
   ```bash
   npm install
   ```
3. Set up your environment variables by copying `.env.example` to `.env.local` and configuring your `MONGODB_URI` and webhook settings.
4. Run the development server:
   ```bash
   npm run dev
   ```

### Chrome Extension Setup

1. Run the package script:
   ```bash
   npm run package-extension
   ```
2. Open Chrome and navigate to `chrome://extensions/`.
3. Enable Developer Mode.
4. Click "Load unpacked" and select the `extension` directory.

## License

This project is licensed under the MIT License.
