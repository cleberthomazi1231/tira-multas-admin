# Tiramulta Admin Panel

A comprehensive React-based admin panel for managing the Tiramulta business operations. This application provides a complete administrative interface for managing dealers, products, orders, users, and Q&A content.

## 🚀 Features

### Core Functionality
- **Authentication System**: Secure login with JWT token management
- **Dashboard**: Overview with key metrics and recent activity
- **Dealer Management**: Complete CRUD operations for dealers/resellers
- **Product Management**: Manage products and pricing
- **Order Management**: Track sales and order status
- **User Management**: Admin user management system
- **Q&A Management**: Content management for questions and answers

### Technical Features
- **Modern React**: Built with React 18 and TypeScript
- **UI Framework**: Chakra UI for consistent, accessible components
- **Form Handling**: Unform for advanced form management
- **Routing**: React Router for navigation
- **HTTP Client**: Axios with interceptors for API communication
- **Date Handling**: date-fns for date formatting
- **Rich Text**: TinyMCE integration for content editing
- **Responsive Design**: Mobile-friendly interface

## 📋 Prerequisites

Before running this project, make sure you have:

- **Node.js** (version 16 or higher)
- **npm** or **yarn** package manager
- **Git** for version control

## 🛠️ Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd admin
   ```

2. **Install dependencies**
   ```bash
   npm install
   # or
   yarn install
   ```

3. **Environment Configuration**
   
   Create a `.env` file in the root directory:
   ```env
   REACT_APP_API_URL=https://your-api-backend-url.com
   ```

4. **Start the development server**
   ```bash
   npm start
   # or
   yarn start
   ```

   The application will be available at `http://localhost:3000`

## 🏗️ Project Structure

```
src/
├── modules/                    # Feature modules
│   ├── auth/                  # Authentication
│   ├── dealers/               # Dealer management
│   ├── orders/                # Order management
│   ├── products/              # Product management
│   ├── questions/             # Q&A management
│   └── users/                 # User management
├── shared/                    # Shared components and utilities
│   ├── apis/                  # API configuration
│   ├── components/            # Reusable UI components
│   ├── constants/             # Application constants
│   ├── hooks/                 # Custom React hooks
│   ├── pages/                 # Shared pages
│   ├── routes/                # Routing configuration
│   ├── styles/                # Global styles and theme
│   └── utils/                 # Utility functions
└── assets/                    # Static assets
```

## 🔧 Available Scripts

- `npm start` - Start development server
- `npm build` - Build for production
- `npm test` - Run tests
- `npm eject` - Eject from Create React App

## 🌐 API Integration

The application integrates with a backend API through the following endpoints:

- **Authentication**: `/auth/user`
- **Dealers**: `/dealers`
- **Products**: `/resources`
- **Orders**: `/sales`
- **Users**: `/users`
- **Questions**: `/questions`

### API Configuration

The API base URL is configured via the `REACT_APP_API_URL` environment variable. The application includes:

- **Axios interceptors** for automatic token management
- **Error handling** for unauthorized requests
- **Automatic redirect** to login on authentication failure

## 🎨 UI Components

The application uses a custom component library built on Chakra UI:

- **Button**: Customizable buttons with various styles
- **Input**: Form inputs with validation
- **Card**: Information display cards
- **Modal**: Confirmation and form modals
- **Select**: Dropdown selections
- **TextEditor**: Rich text editing with TinyMCE
- **Calendar**: Date picker component

## 🔐 Authentication

The application implements JWT-based authentication:

1. **Login**: Users authenticate with email and password
2. **Token Storage**: JWT tokens are stored in localStorage
3. **Auto-logout**: Automatic logout on token expiration
4. **Protected Routes**: Routes are protected based on authentication status

## 📱 Responsive Design

The application is fully responsive and works on:
- Desktop computers
- Tablets
- Mobile devices

## 🚀 Deployment to Vercel

### Prerequisites for Vercel Deployment

1. **Vercel Account**: Create an account at [vercel.com](https://vercel.com)
2. **Git Repository**: Ensure your code is in a Git repository (GitHub, GitLab, or Bitbucket)
3. **Vercel CLI** (optional): Install for local deployment testing

### Deployment Steps

#### Method 1: Deploy via Vercel Dashboard

1. **Connect Repository**
   - Go to [vercel.com/dashboard](https://vercel.com/dashboard)
   - Click "New Project"
   - Import your Git repository
   - Select the repository containing this project

2. **Configure Project Settings**
   - **Framework Preset**: Create React App
   - **Root Directory**: `./` (or leave empty if project is in root)
   - **Build Command**: `npm run build`
   - **Output Directory**: `build`
   - **Install Command**: `npm install`

3. **Environment Variables**
   - Go to Project Settings → Environment Variables
   - Add the following variables:
     ```
     REACT_APP_API_URL=https://your-production-api-url.com
     ```

4. **Deploy**
   - Click "Deploy"
   - Vercel will automatically build and deploy your application

#### Method 2: Deploy via Vercel CLI

1. **Install Vercel CLI**
   ```bash
   npm i -g vercel
   ```

2. **Login to Vercel**
   ```bash
   vercel login
   ```

3. **Deploy from Project Directory**
   ```bash
   cd admin
   vercel
   ```

4. **Follow the CLI prompts**:
   - Link to existing project or create new
   - Set environment variables when prompted
   - Confirm deployment settings

### Environment Variables for Production

Set these environment variables in your Vercel project:

```env
REACT_APP_API_URL=https://your-production-api-backend.com
```

### Custom Domain (Optional)

1. **Add Custom Domain**:
   - Go to Project Settings → Domains
   - Add your custom domain
   - Configure DNS settings as instructed

2. **SSL Certificate**: Vercel automatically provides SSL certificates

### Continuous Deployment

Vercel automatically deploys when you push to your main branch:
- **Production**: Deploys from `main` or `master` branch
- **Preview**: Creates preview deployments for other branches

### Build Optimization

The application is optimized for production with:
- **Code splitting**: Automatic code splitting by routes
- **Tree shaking**: Unused code elimination
- **Minification**: JavaScript and CSS minification
- **Compression**: Gzip compression for faster loading

## 🔧 Troubleshooting

### Common Issues

1. **Build Failures**
   - Check that all dependencies are installed
   - Verify TypeScript compilation
   - Ensure environment variables are set

2. **API Connection Issues**
   - Verify `REACT_APP_API_URL` is correct
   - Check CORS settings on your backend
   - Ensure API endpoints are accessible

3. **Authentication Problems**
   - Clear browser localStorage
   - Check JWT token format
   - Verify API authentication endpoints

### Development Tips

1. **Hot Reload**: The development server supports hot reloading
2. **TypeScript**: Use TypeScript for better development experience
3. **ESLint**: Code linting is configured for code quality
4. **Prettier**: Code formatting is automatically applied

## 📄 License

This project is proprietary software. All rights reserved.

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📞 Support

For support and questions:
- Create an issue in the repository
- Contact the development team
- Check the documentation

---

**Note**: This is an admin panel for the Tiramulta business platform. Ensure proper access controls and security measures are in place before deploying to production. 