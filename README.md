# Skill Swap Platform

A modern, responsive web application that allows users to exchange skills with each other. Built with React.js and Tailwind CSS.

## 🎯 Features

### Core Functionality
- **User Authentication**: Secure login/register with JWT support
- **Profile Management**: Create and edit profiles with photo upload
- **Skill Management**: Add, edit, and delete offered/wanted skills
- **Skill Discovery**: Search and filter users by skills, location, and availability
- **Swap Requests**: Send, accept, reject, and manage skill swap requests
- **Rating System**: Rate and review completed skill swaps
- **Responsive Design**: Mobile-first design that works on all devices

### User Experience
- **Modern UI**: Clean, intuitive interface with smooth animations
- **Real-time Updates**: Dynamic content updates without page refresh
- **Toast Notifications**: User-friendly feedback for all actions
- **Loading States**: Smooth loading indicators for better UX
- **Error Handling**: Comprehensive error handling and user feedback

## 🛠 Tech Stack

- **Frontend**: React.js 18.2.0
- **Styling**: Tailwind CSS 3.2.7
- **Routing**: React Router v6.8.0
- **State Management**: React Context API + useState
- **HTTP Client**: Axios 1.3.0
- **Icons**: Lucide React 0.263.1
- **Build Tool**: Create React App

## 📁 Project Structure

```
src/
├── assets/                 # Static assets
├── components/            # Reusable UI components
│   ├── Navbar.jsx        # Navigation component
│   ├── SkillCard.jsx     # Skill display card
│   ├── SwapRequestCard.jsx # Swap request card
│   ├── SearchBar.jsx     # Search and filter component
│   ├── ProtectedRoute.jsx # Route protection
│   └── Toast.jsx         # Notification component
├── contexts/             # React contexts
│   └── AuthContext.jsx   # Authentication state management
├── pages/               # Page components
│   ├── Landing.jsx      # Homepage
│   ├── Login.jsx        # Login page
│   ├── Register.jsx     # Registration page
│   ├── Dashboard.jsx    # User dashboard
│   ├── Explore.jsx      # Skill discovery
│   ├── Profile.jsx      # Profile settings
│   ├── Requests.jsx     # Swap requests management
│   └── Feedback.jsx     # Rating and reviews
├── App.js              # Main application component
├── index.js            # Application entry point
└── index.css           # Global styles and Tailwind imports
```

## 🚀 Getting Started

### Prerequisites
- Node.js (v14 or higher)
- npm or yarn

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd skill-swap-platform
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the development server**
   ```bash
   npm start
   ```

4. **Open your browser**
   Navigate to `http://localhost:3000`

### Available Scripts

- `npm start` - Start development server
- `npm build` - Build for production
- `npm test` - Run tests
- `npm eject` - Eject from Create React App

## 🎨 Design System

### Color Palette
- **Primary**: Orange (`#ffb347`) - Main brand color
- **Secondary**: Gray scale for text and backgrounds
- **Success**: Green for positive actions
- **Error**: Red for errors and warnings
- **Warning**: Yellow for pending states

### Typography
- **Headings**: Bold, large text for hierarchy
- **Body**: Regular weight for readability
- **Captions**: Small text for secondary information

### Components
- **Cards**: Rounded corners with subtle shadows
- **Buttons**: Consistent styling with hover effects
- **Forms**: Clean input fields with focus states
- **Modals**: Overlay dialogs for important actions

## 📱 Pages Overview

### Public Pages
1. **Landing Page** (`/`)
   - Welcome message and call-to-action
   - Feature highlights and statistics
   - How it works section

2. **Login** (`/login`)
   - User authentication form
   - Guest mode option
   - Password visibility toggle

3. **Register** (`/register`)
   - User registration form
   - Profile setup options
   - Availability preferences

### Protected Pages
4. **Dashboard** (`/dashboard`)
   - User profile overview
   - Skills management (offered/wanted)
   - Quick statistics
   - Recent activity

5. **Explore** (`/explore`)
   - Skill search and discovery
   - Advanced filtering options
   - User skill cards with request buttons

6. **Profile** (`/profile`)
   - Profile information editing
   - Photo upload functionality
   - Privacy settings
   - Password change

7. **Requests** (`/requests`)
   - Incoming and sent swap requests
   - Request status management
   - Action buttons (accept/reject/delete)

8. **Feedback** (`/feedback`)
   - Received and given reviews
   - Pending feedback to give
   - Rating system with comments

## 🔧 API Integration

The application is designed to work with a RESTful API. Key endpoints include:

### Authentication
- `POST /api/auth/login` - User login
- `POST /api/auth/register` - User registration

### User Management
- `GET /api/user/profile` - Get user profile
- `PUT /api/user/profile` - Update user profile

### Skills
- `GET /api/skills` - Get user skills
- `POST /api/skills` - Add new skill
- `DELETE /api/skills/:id` - Delete skill

### Search
- `GET /api/users/search?skill=JavaScript` - Search users by skill

### Requests
- `POST /api/requests` - Send swap request
- `GET /api/requests` - Get user requests
- `PUT /api/requests/:id/accept` - Accept request
- `PUT /api/requests/:id/reject` - Reject request
- `DELETE /api/requests/:id` - Delete request

### Feedback
- `POST /api/feedback` - Submit feedback

## 🎯 Key Features Explained

### Skill Management
Users can add skills they can teach and skills they want to learn. Each skill includes:
- Name and description
- Proficiency level (Beginner, Intermediate, Advanced, Expert)
- Tags for categorization
- Availability preferences

### Search and Discovery
Advanced search functionality allows users to find potential skill swap partners by:
- Skill name or description
- User location
- Availability (weekends, evenings, weekdays)
- Skill level requirements

### Swap Request System
Complete workflow for skill exchanges:
1. User finds someone with desired skill
2. Sends swap request with optional message
3. Recipient can accept, reject, or ignore
4. Accepted requests can be marked as completed
5. Both parties can rate the experience

### Rating and Feedback
Comprehensive feedback system:
- 1-5 star ratings
- Optional written comments
- Separate tracking for received and given feedback
- Pending feedback reminders

## 🔒 Security Features

- **Protected Routes**: Authentication required for sensitive pages
- **JWT Tokens**: Secure token-based authentication
- **Input Validation**: Client-side form validation
- **Error Handling**: Graceful error handling and user feedback

## 📱 Responsive Design

The application is fully responsive and optimized for:
- **Mobile**: Touch-friendly interface with collapsible navigation
- **Tablet**: Optimized layouts for medium screens
- **Desktop**: Full-featured interface with sidebar navigation

## 🚀 Deployment

### Build for Production
```bash
npm run build
```

### Environment Variables
Create a `.env` file in the root directory:
```
REACT_APP_API_URL=your-api-url
REACT_APP_ENVIRONMENT=production
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- **Tailwind CSS** for the utility-first CSS framework
- **Lucide React** for the beautiful icons
- **React Router** for client-side routing
- **Create React App** for the development setup

## 📞 Support

For support and questions, please open an issue in the GitHub repository or contact the development team.

---

**Built with ❤️ using React.js and Tailwind CSS** 