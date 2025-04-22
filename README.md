# test_api

Here's a comprehensive README for your hotel cleaning service project:

# CleanStay - Hotel Cleaning Service Platform

CleanStay is a platform that connects hotels with cleaning service providers, streamlining the room cleaning request and fulfillment process.

## Overview

This project consists of two main components:
- **Web Dashboard**: For hotel managers to manage rooms and cleaning requests
- **Mobile App**: For cleaning staff to view, reserve, and complete cleaning tasks

### Tech Stack

#### Backend
- Ruby on Rails API (RESTful)
- PostgreSQL database
- JWT Authentication

#### Web Dashboard
- Rails views with Hotwire/Turbo
- JavaScript for enhanced interactivity

#### Mobile Application
- React
- React Router
- Axios for API communication

## Features

### For Hotel Managers
- Create and manage hotel properties and rooms
- Request cleaning services for specific rooms
- Track cleaning status in real-time
- View cleaning history and performance metrics

### For Cleaning Staff
- Browse available cleaning requests
- Reserve cleaning tasks
- Update cleaning status (start/complete)
- Manage personal schedule and task list

## Project Structure

```
/
├── api/                  # Rails API backend
│   ├── app/
│   │   ├── controllers/  # API endpoints
│   │   ├── models/       # Database models
│   │   └── services/     # Business logic
│   └── ...
│
├── web/                  # Hotel manager web dashboard
│   ├── app/
│   │   ├── controllers/  # Web controllers
│   │   ├── views/        # Hotwire/Turbo views
│   │   └── ...
│   └── ...
│
└── mobile/               # Cleaner mobile application
    ├── src/
    │   ├── components/   # React components
    │   ├── screens/      # Application screens
    │   ├── services/     # API integration
    │   └── ...
    └── ...
```

## Getting Started

### Prerequisites
- Ruby 3.2+
- Rails 7.0+
- Node.js 16+
- PostgreSQL 14+

### Backend Setup
```bash
# Clone the repository
git clone https://github.com/yourusername/cleanstay.git
cd cleanstay/api

# Install dependencies
bundle install

# Set up database
rails db:create db:migrate db:seed

# Start the server
rails server -p 3000
```

### Web Dashboard Setup
```bash
cd ../web

# Install dependencies
bundle install

# Start the server
rails server -p 3001
```

### Mobile App Setup
```bash
cd ../mobile

# Install dependencies
npm install

# Start development server
npm start
```

## API Documentation

The API documentation is available at `/api/docs` when the backend server is running.

Key endpoints include:

### Authentication
- `POST /api/v1/login` - Authenticate user
- `POST /api/v1/refresh` - Refresh authentication token

### Hotels & Rooms
- `GET /api/v1/hotels` - List hotels
- `GET /api/v1/hotels/:id/rooms` - List rooms for a hotel
- `POST /api/v1/hotels/:id/rooms` - Create a new room

### Cleaning Requests
- `POST /api/v1/cleaning_requests` - Create cleaning request
- `GET /api/v1/cleaning_requests/available` - List available jobs
- `PATCH /api/v1/cleaning_requests/:id/reserve` - Reserve a cleaning job
- `PATCH /api/v1/cleaning_requests/:id/start` - Start a cleaning job
- `PATCH /api/v1/cleaning_requests/:id/complete` - Complete a cleaning job

## Development Workflow

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## Testing

```bash
# Run backend tests
cd api
bundle exec rspec

# Run React component tests
cd ../mobile
npm test
```

## Deployment

Deployment instructions for each component:

### Backend API
The API can be deployed to Heroku:
```bash
heroku create cleanstay-api
git subtree push --prefix api heroku main
```

### Web Dashboard
The web dashboard can be deployed to Heroku:
```bash
heroku create cleanstay-web
git subtree push --prefix web heroku main
```

### Mobile App
The React app can be deployed to Vercel or Netlify.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- This project was created as a demonstration of a full-stack Rails API with React mobile application
- Special thanks to all contributors
