# VueJobs

A modern job listing application built with Vue 3, Vite, and TailwindCSS. This application allows users to browse, add, edit, and delete job listings with a beautiful and responsive interface.

## 🚀 Features

- **Browse Jobs** - View all available job listings with detailed information
- **Job Details** - View comprehensive details about individual job positions
- **Add Jobs** - Create new job listings with company information
- **Edit Jobs** - Update existing job listings
- **Delete Jobs** - Remove job listings
- **Responsive Design** - Beautiful UI built with TailwindCSS
- **Toast Notifications** - User-friendly feedback for actions
- **Loading States** - Smooth loading indicators with vue-spinner
- **404 Page** - Custom not found page for invalid routes

## 🛠️ Tech Stack

- **Vue 3** - Progressive JavaScript framework
- **Vue Router** - Official router for Vue.js
- **Vite** - Next generation frontend tooling
- **TailwindCSS** - Utility-first CSS framework
- **Axios** - Promise-based HTTP client
- **JSON Server** - Mock REST API for development
- **Vue Toastification** - Toast notification library
- **PrimeIcons** - Icon library

## 📋 Prerequisites

- Node.js `^20.19.0 || >=22.12.0`
- npm or yarn package manager

## 🔧 Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd new
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

## 🚦 Running the Application

### Development Mode

To run the application in development mode with hot-reload:

```bash
npm run dev
```

The application will be available at `http://localhost:5173` (or another port if 5173 is in use).

### Mock API Server

The application uses JSON Server to provide a mock REST API. In a separate terminal, start the JSON server:

```bash
npm run server
```

The API server will run on `http://localhost:5000` and serve data from `src/jobs.json`.

> **Note**: You need to run both commands (in separate terminals) for the application to work correctly:
> - `npm run dev` - Runs the Vue.js frontend
> - `npm run server` - Runs the mock API backend

## 📦 Building for Production

To build the application for production:

```bash
npm run build
```

The optimized production files will be generated in the `dist` directory.

### Preview Production Build

To preview the production build locally:

```bash
npm run preview
```

## 📁 Project Structure

```
├── src/
│   ├── assets/          # Static assets (images, fonts, etc.)
│   ├── components/      # Reusable Vue components
│   │   ├── BackButton.vue
│   │   ├── Card.vue
│   │   ├── Hero.vue
│   │   ├── HomeCards.vue
│   │   ├── JobListing.vue
│   │   ├── JobListings.vue
│   │   └── Navbar.vue
│   ├── router/          # Vue Router configuration
│   │   └── index.js
│   ├── views/           # Page components
│   │   ├── AddJobView.vue
│   │   ├── EditJobView.vue
│   │   ├── HomeView.vue
│   │   ├── JobView.vue
│   │   ├── JobsView.vue
│   │   └── NotFound.vue
│   ├── App.vue          # Root component
│   ├── main.js          # Application entry point
│   ├── index.css        # Global styles
│   └── jobs.json        # Mock job data
├── public/              # Public static files
├── index.html           # HTML template
├── vite.config.js       # Vite configuration
├── tailwind.config.js   # TailwindCSS configuration
└── package.json         # Project dependencies and scripts
```

## 🎨 Development

### Recommended IDE Setup

- [VS Code](https://code.visualstudio.com/)
- [Vue (Official)](https://marketplace.visualstudio.com/items?itemName=Vue.volar) extension

Disable Vetur extension if you have it installed.

### Browser Extensions

**Chromium-based browsers (Chrome, Edge, Brave, etc.):**
- [Vue.js devtools](https://chromewebstore.google.com/detail/vuejs-devtools/nhdogjmejiglipccpnnnanhbledajbpd)
- [Turn on Custom Object Formatter in Chrome DevTools](http://bit.ly/object-formatters)

**Firefox:**
- [Vue.js devtools](https://addons.mozilla.org/en-US/firefox/addon/vue-js-devtools/)
- [Turn on Custom Object Formatter in Firefox DevTools](https://fxdx.dev/firefox-devtools-custom-object-formatters/)

## 🌐 API Routes

The JSON Server provides the following endpoints:

- `GET /jobs` - Get all jobs
- `GET /jobs/:id` - Get a specific job
- `POST /jobs` - Create a new job
- `PUT /jobs/:id` - Update a job
- `DELETE /jobs/:id` - Delete a job

## 🔗 Application Routes

- `/` - Home page
- `/jobs` - All jobs listing
- `/jobs/:id` - Individual job details
- `/jobs/add` - Add new job
- `/jobs/edit/:id` - Edit existing job

## 📝 Configuration

### Vite Configuration

See [Vite Configuration Reference](https://vite.dev/config/) for customization options.

### Tailwind Configuration

Modify `tailwind.config.js` to customize your design system, themes, and extend Tailwind's default configuration.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is private and not licensed for public use.

## 🐛 Troubleshooting

### Port Already in Use

If you get an error that port 5173 or 5000 is already in use:

- For Vite dev server, it will automatically try the next available port
- For JSON Server, you can change the port in `package.json` script: `--port 5001`

### API Connection Issues

Make sure the JSON Server is running on port 5000. Check that `src/jobs.json` exists and contains valid JSON data.
